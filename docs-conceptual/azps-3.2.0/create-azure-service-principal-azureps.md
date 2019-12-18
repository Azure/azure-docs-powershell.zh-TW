---
title: 透過 Azure PowerShell 使用 Azure 服務主體
description: 了解如何搭配 Azure PowerShell 來建立和使用服務主體。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182395"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>使用 Azure PowerShell 來建立 Azure 服務主體

使用 Azure 服務的自動化工具應一律具有權限限制。 Azure 提供的服務主體，可替代以具有完整權限的使用者身分登入應用程式。

Azure 服務主體是一種身分識別，建立目的是為了搭配應用程式、託管服務及自動化工具來存取 Azure 資源。 此存取會受限於指派給服務主體的角色，以便您控制可存取的資源，以及在哪個層級上存取。 基於安全理由，我們建議您一律搭配自動化工具使用服務主體，而不是讓服務主體透過使用者身分識別來登入。

本文會示範搭配 Azure PowerShell 建立服務主體，以及擷取其資訊和重設服務主體的步驟。

## <a name="create-a-service-principal"></a>建立服務主體

使用 [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) Cmdlet 建立服務主體。 建立服務主體時，您可以選擇其所用的登入驗證類型。

> [!NOTE]
>
> 如果您的帳戶沒有建立服務主體的權限，`New-AzADServicePrincipal` 會傳回「權限不足，無法完成作業」的錯誤訊息。 請連絡您的 Azure Active Directory 管理員，以建立服務主體。

有兩種驗證類型可用於服務主體：密碼式驗證和憑證式驗證。

### <a name="password-based-authentication"></a>密碼式驗證

密碼式驗證沒有任何其他驗證參數，而是搭配使用為您建立的隨機密碼。 如果您想使用密碼式驗證，建議使用這個方法。

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

傳回的物件包含 `Secret` 成員，其為包含所產生密碼的 `SecureString`。 請確定您將此值儲存在安全的位置，以便驗證服務主體。 該值__不會__顯示在主控台輸出。 如果您遺失密碼，[請重設服務主體認證](#reset-credentials)。

下列程式碼可讓您匯出祕密：

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

對於使用者提供的密碼，`-PasswordCredential` 引數會採用 `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` 物件。 這些物件必須具有有效的 `StartDate` 和 `EndDate`，並採取純文字 `Password`。 建立密碼時，請務必遵循 [Azure Active Directory 密碼規則和限制](/azure/active-directory/active-directory-passwords-policy)。 請勿使用弱式密碼或重複使用密碼。

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

從 `New-AzADServicePrincipal` 傳回的物件包含 `Id` 和 `DisplayName` 成員，兩者都可用於使用服務主體登入。

> [!IMPORTANT]
>
> 使用服務主體登入需要在其下建立服務主體的租用戶識別碼。 若要在建立服務主體時取得作用中的租用戶，請在建立服務主體__之後立即__執行下列命令：
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>憑證式驗證

使用憑證式驗證的服務主體會使用 `-CertValue` 參數建立。 這個參數會採用公開憑證的 base64 編碼 ASCII 字串。 這會以 PEM 檔案，或文字編碼 CRT 或 CER 表示。 不支援公開憑證的二進位編碼。 這些指示會假設您已經有可用的憑證。

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

您也可以使用 `-KeyCredential` 參數，其採用 `PSADKeyCredential` 物件。 這些物件必須具有有效的 `StartDate`、`EndDate`，而且 `CertValue` 成員設定為公開憑證的 base64 編碼 ASCII 字串。

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

從 `New-AzADServicePrincipal` 傳回的物件包含 `Id` 和 `DisplayName` 成員，兩者都可用於使用服務主體登入。 使用服務主體登入的用戶端也需要存取憑證的私密金鑰。

> [!IMPORTANT]
>
> 使用服務主體登入需要在其下建立服務主體的租用戶識別碼。 若要在建立服務主體時取得作用中的租用戶，請在建立服務主體__之後立即__執行下列命令：
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>取得現有的服務主體

您可以使用 [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) 擷取目前作用中租用戶的服務主體清單。 依預設，此命令會傳回租用戶中的__所有__服務主體，因此對於大型組織，可能需要長時間來傳回結果。 建議使用選擇性伺服器端篩選引數的其中一個：

* `-DisplayNameBeginsWith` 會要求服務主體的_前置詞_符合所提供的值。 服務主體的顯示名稱是建立期間使用 `-DisplayName` 所設定的值。
* `-DisplayName` 要求服務主體名稱_完全相符_。

## <a name="manage-service-principal-roles"></a>管理服務主體角色

Azure PowerShell 提供下列 Cmdlet 以供您管理角色指派：

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

服務主體的預設角色是**參與者**。 此角色具有讀取和寫入至 Azure 帳戶的完整權限。 **讀者**角色的權限較為侷限，僅有唯讀存取權。  如需角色型存取控制 (RBAC) 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。

此範例會新增**讀者**角色，並移除**參與者**角色：

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> 角色指派 Cmdlet 不需要服務主體物件識別碼。 該 Cmdlet 需要在建立時所產生的相關聯應用程式識別碼。 若要取得服務主體的應用程式識別碼，請使用 `Get-AzADServicePrincipal`。

> [!NOTE]
> 如果您的帳戶沒有足夠權限可指派角色，您會看到錯誤訊息，這表示您的帳戶「沒有執行 'Microsoft.Authorization/roleAssignments/write' 動作的權限」。請連絡您的 Azure Active Directory 管理員，以管理角色。

新增角色「不會」  限制之前指派的權限。 限制服務主體的權限時，應移除「參與者」  角色。

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

如果您忘記服務主體的認證，請使用 [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) 新增認證。 此 Cmdlet 會採用與 `New-AzADServicePrincipal` 相同的認證引數和類型。 會建立新的 `PasswordCredential` 搭配隨機密碼，且不具任何認證引數。

> [!IMPORTANT]
> 在指派任何新認證之前，您需要移除現有的認證，以避免使用這些認證登入。 若要這樣做，請使用 [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) Cmdlet：
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
