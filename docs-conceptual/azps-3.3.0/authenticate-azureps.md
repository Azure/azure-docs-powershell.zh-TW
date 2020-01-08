---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 614cce77deb4390ea158a48ae2d48b7b983224f2
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "75720913"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ba3d5-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="ba3d5-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="ba3d5-104">Azure PowerShell 支援數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="ba3d5-105">要開始使用的最簡單方法是透過 [Azure Cloud Shell](/azure/cloud-shell/overview)，這會自動將您登入。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="ba3d5-106">您可以使用本機安裝，以互動方式透過瀏覽器登入。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="ba3d5-107">在撰寫自動化指令碼時，建議的方法是使用[服務主體](create-azure-service-principal-azureps.md)搭配必要權限。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="ba3d5-108">當您依自身的使用案例儘可能地限制登入權限時，同時也是在協助維護 Azure 資源的安全。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="ba3d5-109">在登入之後，系統會針對您的預設訂用帳戶來執行命令。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="ba3d5-110">若要變更工作階段作用中的訂用帳戶，請使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="ba3d5-111">若要變更登入 Azure PowerShell 時使用的預設訂用帳戶，請使用 [Set-AzDefault](/powershell/module/az.accounts/set-azdefault)。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ba3d5-112">只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="ba3d5-113">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ba3d5-114">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="ba3d5-114">Sign in interactively</span></span>

<span data-ttu-id="ba3d5-115">若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="ba3d5-116">執行時，此 Cmdlet 會出示權杖字串。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="ba3d5-117">若要登入，請複製這個字串並將它貼至瀏覽器中的 https://microsoft.com/devicelogin 。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="ba3d5-118">PowerShell 工作階段會進行驗證以便連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ba3d5-119">由於 Active Directory 授權實作與安全性考量中的變更，已在 Azure PowerShell 中移除使用者名稱/密碼認證授權。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="ba3d5-120">如果您將認證授權用於自動化用途，請[建立服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="ba3d5-121">使用服務主體 <a name="sp-signin"/> 來登入</span><span class="sxs-lookup"><span data-stu-id="ba3d5-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="ba3d5-122">服務主體為非互動式 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="ba3d5-123">如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="ba3d5-124">藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="ba3d5-125">若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ba3d5-126">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="ba3d5-127">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="ba3d5-128">您使用服務主體登入的方式將取決於其設定為密碼式或憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="ba3d5-129">密碼式驗證</span><span class="sxs-lookup"><span data-stu-id="ba3d5-129">Password-based authentication</span></span>

<span data-ttu-id="ba3d5-130">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ba3d5-131">此 Cmdlet 會顯示使用者名稱和密碼的提示。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="ba3d5-132">使用使用者名稱的服務主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="ba3d5-133">在自動化的情況下，您需要從使用者名稱和安全字串建立認證：</span><span class="sxs-lookup"><span data-stu-id="ba3d5-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="ba3d5-134">請確定在自動化服務主體連線時，您使用安全的密碼儲存體做法。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="ba3d5-135">憑證式驗證</span><span class="sxs-lookup"><span data-stu-id="ba3d5-135">Certificate-based authentication</span></span>

<span data-ttu-id="ba3d5-136">憑證式驗證要求 Azure PowerShell 可從以憑證指紋為基礎的本機憑證存放區擷取資訊。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="ba3d5-137">若使用的是服務主體而非已註冊的應用程式，請新增 `-ServicePrincipal` 引數並提供服務主體的識別碼作為 `-ApplicationId` 參數值。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-137">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="ba3d5-138">在 PowerShell 5.1 中，憑證存放區可透過 [PKI](/powershell/module/pkiclient) 模組進行管理及檢查。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-138">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="ba3d5-139">PowerShell Core 6.x 和更新版本的程序更複雜。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-139">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="ba3d5-140">下列指令碼會示範如何將現有憑證匯入至 PowerShell 可存取的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-140">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="ba3d5-141">在 PowerShell 5.1 中匯入憑證</span><span class="sxs-lookup"><span data-stu-id="ba3d5-141">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="ba3d5-142">在 PowerShell Core 6.x 和更新版本中匯入憑證</span><span class="sxs-lookup"><span data-stu-id="ba3d5-142">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="ba3d5-143">使用受控識別登入</span><span class="sxs-lookup"><span data-stu-id="ba3d5-143">Sign in using a managed identity</span></span>

<span data-ttu-id="ba3d5-144">受控識別是 Azure Active Directory 的功能。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-144">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="ba3d5-145">受控識別是指派給在 Azure 中執行之資源的服務主體。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-145">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="ba3d5-146">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-146">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ba3d5-147">只有在 Azure 雲端中執行的虛擬機器才能使用受控識別。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-147">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="ba3d5-148">此命令會使用主機環境的受控識別來連線。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-148">This command connects using the managed identity of the host environment.</span></span> <span data-ttu-id="ba3d5-149">例如，如果在具有指派受控服務識別的 VirtualMachine 上執行，這可讓程式碼使用該指派的身分識別來登入。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-149">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="ba3d5-150">以非預設租用戶或雲端解決方案提供者 (CSP) 登入</span><span class="sxs-lookup"><span data-stu-id="ba3d5-150">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="ba3d5-151">如果您的帳戶與多個租用戶相關聯，則需要使用連線時的 `-Tenant` 參數方可登入。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-151">If your account is associated with more than one tenant, sign-in requires the use of the `-Tenant` parameter when connecting.</span></span> <span data-ttu-id="ba3d5-152">此參數也適用於其他所有登入方法。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-152">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="ba3d5-153">登入時，此參數值可以是租用戶的 Azure 物件識別碼 (租用戶識別碼)，或租用戶的完整的網域名稱。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-153">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="ba3d5-154">如果您是[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/)，則 `-Tenant` 值**必須**是租用戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-154">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ba3d5-155">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="ba3d5-155">Sign in to another Cloud</span></span>

<span data-ttu-id="ba3d5-156">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-156">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="ba3d5-157">針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-157">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="ba3d5-158">此參數也適用於其他所有登入方法。</span><span class="sxs-lookup"><span data-stu-id="ba3d5-158">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="ba3d5-159">例如，如果您的帳戶位於中國雲端：</span><span class="sxs-lookup"><span data-stu-id="ba3d5-159">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ba3d5-160">下列命令可取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="ba3d5-160">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
