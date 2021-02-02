---
title: 透過 Azure PowerShell 使用 Azure 服務主體
description: 了解如何搭配 Azure PowerShell 來建立和使用服務主體。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 196af9721ed8ab5141451159b12a8a1e5a5b1f3d
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251857"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>使用 Azure PowerShell 來建立 Azure 服務主體

使用 Azure 服務的自動化工具應一律具有權限限制。 Azure 提供的服務主體，可替代以具有完整權限的使用者身分登入應用程式。

Azure 服務主體是一種身分識別，建立目的是為了搭配應用程式、託管服務及自動化工具來存取 Azure 資源。 此存取會受限於指派給服務主體的角色，以便您控制可存取的資源，以及在哪個層級上存取。 基於安全理由，我們建議您一律搭配自動化工具使用服務主體，而不是讓服務主體透過使用者身分識別來登入。

本文會示範搭配 Azure PowerShell 建立服務主體，以及擷取其資訊和重設服務主體的步驟。

> [!WARNING]
> 當您使用 [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) 命令建立服務主體時，輸出中會包含您必須保護的認證。 或者，您也可以考慮使用[受控識別](/azure/active-directory/managed-identities-azure-resources/overview)以避免需要使用認證。
>
> 根據預設，[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) 會將[參與者](/azure/role-based-access-control/built-in-roles#contributor)角色指派給訂用帳戶範圍中的服務主體。 若要降低服務主體遭到入侵的風險，請指派更具體的角色，並將範圍縮小至資源或資源群組。 如需相關資訊，請參閱[新增角色指派的步驟](/azure/role-based-access-control/role-assignments-steps)。

## <a name="create-a-service-principal"></a>建立服務主體

使用 [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) Cmdlet 建立服務主體。 建立服務主體時，您可以選擇其所用的登入驗證類型。

> [!NOTE]
> 如果您的帳戶沒有建立服務主體的權限，`New-AzADServicePrincipal` 會傳回「權限不足，無法完成作業」的錯誤訊息。
> 請連絡您的 Azure Active Directory 管理員，以建立服務主體。

有兩種驗證類型可用於服務主體：密碼式驗證和憑證式驗證。

### <a name="password-based-authentication"></a>密碼式驗證

> [!IMPORTANT]
> 密碼型驗證服務主體的預設角色是 [參與者]。 此角色具有讀取和寫入至 Azure 帳戶的完整權限。 如需管理角色指派的詳細資訊，請參閱[管理服務主體角色](#manage-service-principal-roles)。

密碼式驗證沒有任何其他驗證參數，而是搭配使用為您建立的隨機密碼。 如果您想使用密碼式驗證，建議使用這個方法。

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

傳回的物件包含 `Secret` 成員，其為包含所產生密碼的 `SecureString`。 請確定您將此值儲存在安全的位置，以便驗證服務主體。 該值 _不會_ 顯示在主控台輸出。 如果您遺失密碼，[請重設服務主體認證](#reset-credentials)。

下列程式碼可讓您匯出祕密：

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

對於使用者提供的密碼，`-PasswordCredential` 引數會採用 `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` 物件。 這些物件必須具有有效的 `StartDate` 和 `EndDate`，並採取純文字 `Password`。 建立密碼時，請務必遵循 [Azure Active Directory 密碼規則和限制](/azure/active-directory/active-directory-passwords-policy)。
請勿使用弱式密碼或重複使用密碼。

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

從 `New-AzADServicePrincipal` 傳回的物件包含 `Id` 和 `DisplayName` 成員，兩者都可用於使用服務主體登入。

> [!IMPORTANT]
> 使用服務主體登入需要在其下建立服務主體的租用戶識別碼。 若要在建立服務主體時取得作用中的租用戶，請在建立服務主體 _之後立即_ 執行下列命令：

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>憑證式驗證

> [!IMPORTANT]
> 建立憑證型驗證服務主體時，並未指派任何預設角色。 如需管理角色指派的詳細資訊，請參閱[管理服務主體角色](#manage-service-principal-roles)。

使用憑證式驗證的服務主體會使用 `-CertValue` 參數建立。 這個參數會採用公開憑證的 base64 編碼 ASCII 字串。 這會以 PEM 檔案，或文字編碼 CRT 或 CER 表示。 不支援公開憑證的二進位編碼。 這些指示會假設您已經有可用的憑證。

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

您也可以使用 `-KeyCredential` 參數，其採用 `PSADKeyCredential` 物件。 這些物件必須具有有效的 `StartDate`、`EndDate`，而且 `CertValue` 成員設定為公開憑證的 base64 編碼 ASCII 字串。

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

從 `New-AzADServicePrincipal` 傳回的物件包含 `Id` 和 `DisplayName` 成員，兩者都可用於使用服務主體登入。 使用服務主體登入的用戶端也需要存取憑證的私密金鑰。

> [!IMPORTANT]
> 使用服務主體登入需要在其下建立服務主體的租用戶識別碼。 若要在建立服務主體時取得作用中的租用戶，請在建立服務主體 _之後立即_ 執行下列命令：

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>取得現有的服務主體

您可以使用 [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) 擷取作用中租用戶的服務主體清單。 依預設，此命令會傳回租用戶中的「所有」服務主體。 若為大型組織，可能需要很長的時間才會傳回結果。 建議使用選擇性伺服器端篩選引數的其中一個：

- `-DisplayNameBeginsWith` 會要求服務主體的 _前置詞_ 符合所提供的值。 服務主體的顯示名稱是建立期間使用 `-DisplayName` 所設定的值。
- `-DisplayName` 要求服務主體名稱 _完全相符_。

## <a name="manage-service-principal-roles"></a>管理服務主體角色

Azure PowerShell 提供下列 Cmdlet 以供您管理角色指派：

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

密碼型驗證服務主體的預設角色是 [參與者]。 此角色具有讀取和寫入至 Azure 帳戶的完整權限。 **讀者** 角色的權限較為侷限，僅有唯讀存取權。 如需角色型存取控制 (RBAC) 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。

此範例會新增 **讀者** 角色，並移除 **參與者** 角色：

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> 角色指派 Cmdlet 不需要服務主體物件識別碼。 該 Cmdlet 需要在建立時所產生的相關聯應用程式識別碼。 若要取得服務主體的應用程式識別碼，請使用 `Get-AzADServicePrincipal`。

> [!NOTE]
> 如果您的帳戶沒有足夠權限可指派角色，您會看到錯誤訊息，這表示您的帳戶「沒有執行 'Microsoft.Authorization/roleAssignments/write' 動作的權限」。 請連絡您的 Azure Active Directory 管理員，以管理角色。

新增角色「不會」限制之前指派的權限。 限制服務主體的權限時，應移除「參與者」角色。

列出指派的角色可以驗證變更：

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>使用服務主體來登入

藉由登入來測試新服務主體的認證和權限。 若要使用服務主體登入，您需要相關聯的 `applicationId` 值，以及在其下建立的租用戶。

透過服務主體來使用密碼登入：

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

憑證式驗證要求 Azure PowerShell 可從以憑證指紋為基礎的本機憑證存放區擷取資訊。

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

如需將憑證匯入 PowerShell 可存取的認證存放區指示，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>重設認證

如果您忘記服務主體的認證，請使用 [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) 來新增具有隨機密碼的認證。 在重設密碼時，此 Cmdlet 不支援使用者定義的認證。

> [!IMPORTANT]
> 在指派任何新認證之前，您需要移除現有的認證，以避免使用這些認證登入。 若要這樣做，請使用 [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) Cmdlet：

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>疑難排解

如果您收到錯誤：「New-AzADServicePrincipal：已經存在另一個具有相同 identifierUris 屬性值的物件。」，請確認尚未有同名的服務主體存在。

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

如果不再需要現有的服務主體，您可使用下列範例予以移除。

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

如果先前已建立 Azure Active Directory 應用程式的服務主體，也可能發生此錯誤。 如果您移除服務主體，仍可使用該應用程式。 此應用程式可防止您建立另一個同名的服務主體。

您可使用下列範例來確認不存在同名的 Azure Active Directory 應用程式：

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

如果有同名的應用程式存在，而且不再需要該應用程式，您可使用下列範例予以移除。

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

否則，請為您嘗試建立的新服務主體選擇替代名稱。
