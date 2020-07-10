---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.openlocfilehash: 7ac723202ca9e81c8ef4cba5e844d46b98ba4b67
ms.sourcegitcommit: 7b368a9be1cea2ac4e7d269e1a51529271269a42
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/08/2020
ms.locfileid: "86098801"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 登入

Azure PowerShell 支援數種驗證方法。 要開始使用的最簡單方法是透過 [Azure Cloud Shell](/azure/cloud-shell/overview)，這會自動將您登入。 您可以使用本機安裝，以互動方式透過瀏覽器登入。 在撰寫自動化指令碼時，建議的方法是使用[服務主體](create-azure-service-principal-azureps.md)搭配必要權限。 當您依自身的使用案例儘可能地限制登入權限時，同時也是在協助維護 Azure 資源的安全。

如果您一開始有多個訂用帳戶的存取權，則您會登入第一個 Azure 傳回的訂用帳戶。 依據預設會針對此訂用帳戶執行命令。 若要變更工作階段作用中的訂用帳戶，請使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。 若要變更使用中的訂用帳戶，並將其保存在相同系統上的工作階段之間，請使用 [Select-AzContext](/powershell/module/az.accounts/select-azcontext) Cmdlet。

> [!IMPORTANT]
> 只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。
> 如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。

## <a name="sign-in-interactively"></a>以互動方式登入

若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。

```azurepowershell-interactive
Connect-AzAccount
```

從 PowerShell 第 6 版和更新版本執行時，此 Cmdlet 會呈現權杖字串。 若要登入，請複製此字串並將其貼入網頁瀏覽器中的 [microsoft.com/devicelogin](https://microsoft.com/devicelogin)。 PowerShell 工作階段會進行驗證以便連線至 Azure。 您可以指定 `UseDeviceAuthentication` 參數，以在 Windows PowerShell 上接收權杖字串。

> [!IMPORTANT]
> 由於 Active Directory 授權實作與安全性考量中的變更，已在 Azure PowerShell 中移除使用者名稱/密碼認證授權。 如果您將認證授權用於自動化用途，請[建立服務主體](create-azure-service-principal-azureps.md)。

使用 [Get-AzContext](/powershell/module/az.accounts/get-azcontext) Cmdlet，將您的租用戶識別碼儲存在本文後續兩節所用的變數中。

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>使用服務主體 <a name="sp-signin"/> 來登入

服務主體為非互動式 Azure 帳戶。 如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。 藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。

若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。

若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。 您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。 您使用服務主體登入的方式將取決於其設定為密碼式或憑證式驗證。

### <a name="password-based-authentication"></a>密碼式驗證

建立要在本節的範例中使用的服務主體。 如需有關建立服務主體的詳細資訊，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](/powershell/azure/create-azure-service-principal-azureps)。

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。 此 Cmdlet 會顯示使用者名稱和密碼的提示。 使用服務主體的 `applicationID` 作為使用者名稱，並將其 `secret` 轉換為純文字以取得密碼。

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

在自動化的情況下，您需要從服務主體的 `applicationId` 和 `secret` 建立認證：

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

請確定在自動化服務主體連線時，您使用安全的密碼儲存體做法。

### <a name="certificate-based-authentication"></a>憑證式驗證

憑證式驗證要求 Azure PowerShell 可從以憑證指紋為基礎的本機憑證存放區擷取資訊。

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

若使用的是服務主體而非已註冊的應用程式，請新增 `-ServicePrincipal` 引數並提供服務主體的應用程式識別碼作為 `-ApplicationId` 參數值。

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

在 PowerShell 5.1 中，憑證存放區可透過 [PKI](/powershell/module/pkiclient) 模組進行管理及檢查。 PowerShell Core 6.x 和更新版本的程序更複雜。 下列指令碼會示範如何將現有憑證匯入至 PowerShell 可存取的憑證存放區。

#### <a name="import-a-certificate-in-powershell-51"></a>在 PowerShell 5.1 中匯入憑證

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>在 PowerShell Core 6.x 和更新版本中匯入憑證

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>使用受控識別登入

受控識別是 Azure Active Directory 的功能。 受控識別是指派給在 Azure 中執行之資源的服務主體。 您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。 只有在 Azure 雲端中執行的虛擬機器才能使用受控識別。

此範例會使用主機環境的受控識別來連線。 例如，如果在具有指派受控服務識別的 VirtualMachine 上執行，這可讓程式碼使用該指派的身分識別來登入。

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>以非預設租用戶或雲端解決方案提供者 (CSP) 登入

如果您的帳戶與多個租用戶相關聯，則需要使用連線時指定的 `-Tenant` 參數方可登入。 此參數適用於其他所有登入方法。 登入時，此參數值可以是租用戶的 Azure 物件識別碼 (租用戶識別碼)，或租用戶的完整的網域名稱。

如果您是[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/)，則 `-Tenant` 值**必須**是租用戶的識別碼。

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供符合區域資料處理法規的環境。 針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。 此參數適用於其他所有登入方法。 例如，如果您的帳戶位於中國雲端：

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

下列命令可取得可用環境的清單：

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
