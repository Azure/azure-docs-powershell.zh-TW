---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 897bc20721305c03a0545bc236fa91292861ef1e
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363667"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 登入

Azure PowerShell 支援數種驗證方法。 要開始使用的最簡單方法是透過 [Azure Cloud Shell](/azure/cloud-shell/overview)，這會自動將您登入。 您可以使用本機安裝，以互動方式透過瀏覽器登入。 在撰寫自動化指令碼時，建議的方法是使用[服務主體](create-azure-service-principal-azureps.md)搭配必要權限。 當您依自身的使用案例儘可能地限制登入權限時，同時也是在協助維護 Azure 資源的安全。

在登入之後，系統會針對您的預設訂用帳戶來執行命令。 若要變更工作階段作用中的訂用帳戶，請使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。 若要變更登入 Azure PowerShell 時使用的預設訂用帳戶，請使用 [Set-AzDefault](/powershell/module/az.accounts/set-azdefault)。

> [!IMPORTANT]
>
> 只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。
> 如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。

## <a name="sign-in-interactively"></a>以互動方式登入

若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。

```azurepowershell-interactive
Connect-AzAccount
```

執行時，此 Cmdlet 會出示權杖字串。 若要登入，請複製這個字串並將它貼至瀏覽器中的 https://microsoft.com/devicelogin。 PowerShell 工作階段會進行驗證以便連線至 Azure。

> [!IMPORTANT]
>
> 由於 Active Directory 授權實作與安全性考量中的變更，已在 Azure PowerShell 中移除使用者名稱/密碼認證授權。
> 如果您將認證授權用於自動化用途，請[建立服務主體](create-azure-service-principal-azureps.md)。

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a>使用服務主體 <a name="sp-signin"/> 來登入

服務主體為非互動式 Azure 帳戶。 如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。 藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。

若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。

若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。 您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。 您使用服務主體登入的方式將取決於其設定為密碼式或憑證式驗證。

### <a name="password-based-authentication"></a>密碼式驗證

若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。 此 Cmdlet 會顯示使用者名稱和密碼的提示。 使用使用者名稱的服務主體識別碼。

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

在自動化的情況下，您需要從使用者名稱和安全字串建立認證：

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

請確定在自動化服務主體連線時，您使用安全的密碼儲存體做法。

### <a name="certificate-based-authentication"></a>憑證式驗證

憑證式驗證要求 Azure PowerShell 可從以憑證指紋為基礎的本機憑證存放區擷取資訊。
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

在 PowerShell 5 中，憑證存放區可透過 [PKI](/powershell/module/pkiclient) 模組進行管理及檢查。 PowerShell 6 的程序更複雜。 下列指令碼會示範如何將現有憑證匯入至 PowerShell 可存取的憑證存放區。

#### <a name="import-a-certificate-in-powershell-5"></a>在 PowerShell 5 中匯入憑證

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-6"></a>在 PowerShell 6 中匯入憑證

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

若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>以非預設租用戶或雲端解決方案提供者 (CSP) 登入

如果您的帳戶與多個租用戶相關聯，則需要使用連線時的 `-TenantId` 參數方可登入。 此參數可使用任何其他登入方法。 登入時，此參數值可以是租用戶的 Azure 物件識別碼 (租用戶識別碼)，或租用戶的完整的網域名稱。

如果您是[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/)，則 `-TenantId` 值**必須**是租用戶的識別碼。

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供符合區域資料處理法規的環境。
針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。
例如，如果您的帳戶位於中國雲端：

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

下列命令可取得可用環境的清單：

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
