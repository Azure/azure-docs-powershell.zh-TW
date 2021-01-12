---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 46e5e84b6718cc7a700ef2df4e82647e8cb60941
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893678"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="6ef6e-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="6ef6e-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="6ef6e-104">Azure PowerShell 支援數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="6ef6e-105">要開始使用的最簡單方法是透過 [Azure Cloud Shell](/azure/cloud-shell/overview)，這會自動將您登入。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="6ef6e-106">您可以使用本機安裝，以互動方式透過瀏覽器登入。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="6ef6e-107">在撰寫自動化指令碼時，建議的方法是使用[服務主體](create-azure-service-principal-azureps.md)搭配必要權限。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="6ef6e-108">當您依自身的使用案例儘可能地限制登入權限時，同時也是在協助維護 Azure 資源的安全。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="6ef6e-109">如果您一開始有多個訂用帳戶的存取權，則您會登入第一個 Azure 傳回的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="6ef6e-110">依據預設會針對此訂用帳戶執行命令。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="6ef6e-111">若要變更工作階段作用中的訂用帳戶，請使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="6ef6e-112">若要變更使用中的訂用帳戶，並將其保存在相同系統上的工作階段之間，請使用 [Select-AzContext](/powershell/module/az.accounts/select-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ef6e-113">只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="6ef6e-114">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="6ef6e-115">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="6ef6e-115">Sign in interactively</span></span>

<span data-ttu-id="6ef6e-116">若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="6ef6e-117">從 Az PowerShell 模組 5.0.0 版開始，此 Cmdlet 依預設會提供互動式瀏覽器型登入提示。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-117">Beginning with Az PowerShell module version 5.0.0, this cmdlet presents an interactive browser based login prompt by default.</span></span> <span data-ttu-id="6ef6e-118">您可以指定 `UseDeviceAuthentication` 參數以接收權杖字串，該權杖字串先前為 PowerShell 第 6 版和更新版本的預設字串。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-118">You can specify the `UseDeviceAuthentication` parameter to receive a token string which was previously the default for PowerShell version 6 and higher.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ef6e-119">由於 Active Directory 授權實作與安全性考量中的變更，已在 Azure PowerShell 中移除使用者名稱/密碼認證授權。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="6ef6e-120">如果您將認證授權用於自動化用途，請[建立服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="6ef6e-121">使用 [Get-AzContext](/powershell/module/az.accounts/get-azcontext) Cmdlet，將您的租用戶識別碼儲存在本文後續兩節所用的變數中。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-121">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="6ef6e-122">使用服務主體 <a name="sp-signin"/> 來登入</span><span class="sxs-lookup"><span data-stu-id="6ef6e-122">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="6ef6e-123">服務主體為非互動式 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-123">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="6ef6e-124">如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-124">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="6ef6e-125">藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-125">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="6ef6e-126">若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-126">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="6ef6e-127">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-127">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="6ef6e-128">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-128">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="6ef6e-129">您使用服務主體登入的方式將取決於其設定為密碼式或憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-129">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="6ef6e-130">密碼式驗證</span><span class="sxs-lookup"><span data-stu-id="6ef6e-130">Password-based authentication</span></span>

<span data-ttu-id="6ef6e-131">建立要在本節的範例中使用的服務主體。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-131">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="6ef6e-132">如需有關建立服務主體的詳細資訊，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](/powershell/azure/create-azure-service-principal-azureps)。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-132">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="6ef6e-133">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-133">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="6ef6e-134">此 Cmdlet 會顯示使用者名稱和密碼的提示。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-134">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="6ef6e-135">使用服務主體的 `applicationID` 作為使用者名稱，並將其 `secret` 轉換為純文字以取得密碼。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-135">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="6ef6e-136">在自動化的情況下，您需要從服務主體的 `applicationId` 和 `secret` 建立認證：</span><span class="sxs-lookup"><span data-stu-id="6ef6e-136">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="6ef6e-137">請確定在自動化服務主體連線時，您使用安全的密碼儲存體做法。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-137">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="6ef6e-138">憑證式驗證</span><span class="sxs-lookup"><span data-stu-id="6ef6e-138">Certificate-based authentication</span></span>

<span data-ttu-id="6ef6e-139">憑證式驗證要求 Azure PowerShell 可從以憑證指紋為基礎的本機憑證存放區擷取資訊。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-139">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="6ef6e-140">若使用的是服務主體而非已註冊的應用程式，請新增 `-ServicePrincipal` 引數並提供服務主體的應用程式識別碼作為 `-ApplicationId` 參數值。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-140">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="6ef6e-141">在 PowerShell 5.1 中，憑證存放區可透過 [PKI](/powershell/module/pkiclient) 模組進行管理及檢查。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-141">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="6ef6e-142">PowerShell Core 6.x 和更新版本的程序更複雜。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-142">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="6ef6e-143">下列指令碼會示範如何將現有憑證匯入至 PowerShell 可存取的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-143">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="6ef6e-144">在 PowerShell 5.1 中匯入憑證</span><span class="sxs-lookup"><span data-stu-id="6ef6e-144">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="6ef6e-145">在 PowerShell Core 6.x 和更新版本中匯入憑證</span><span class="sxs-lookup"><span data-stu-id="6ef6e-145">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="6ef6e-146">使用受控識別登入</span><span class="sxs-lookup"><span data-stu-id="6ef6e-146">Sign in using a managed identity</span></span>

<span data-ttu-id="6ef6e-147">受控識別是 Azure Active Directory 的功能。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-147">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="6ef6e-148">受控識別是指派給在 Azure 中執行之資源的服務主體。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-148">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="6ef6e-149">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-149">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="6ef6e-150">只有在 Azure 雲端中執行的虛擬機器才能使用受控識別。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-150">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="6ef6e-151">此範例會使用主機環境的受控識別來連線。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-151">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="6ef6e-152">例如，如果在具有指派受控服務識別的 VirtualMachine 上執行，這可讓程式碼使用該指派的身分識別來登入。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-152">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="6ef6e-153">以非預設租用戶或雲端解決方案提供者 (CSP) 登入</span><span class="sxs-lookup"><span data-stu-id="6ef6e-153">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="6ef6e-154">如果您的帳戶與多個租用戶相關聯，則需要使用連線時指定的 `-Tenant` 參數方可登入。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-154">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="6ef6e-155">此參數適用於其他所有登入方法。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-155">This parameter works with any sign-in method.</span></span> <span data-ttu-id="6ef6e-156">登入時，此參數值可以是租用戶的 Azure 物件識別碼 (租用戶識別碼)，或租用戶的完整的網域名稱。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-156">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="6ef6e-157">如果您是 [雲端解決方案提供者 (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/)，則 `-Tenant` 值 **必須** 是租用戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-157">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="6ef6e-158">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="6ef6e-158">Sign in to another Cloud</span></span>

<span data-ttu-id="6ef6e-159">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-159">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="6ef6e-160">針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-160">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="6ef6e-161">此參數適用於其他所有登入方法。</span><span class="sxs-lookup"><span data-stu-id="6ef6e-161">This parameter works with any sign-in method.</span></span> <span data-ttu-id="6ef6e-162">例如，如果您的帳戶位於中國雲端：</span><span class="sxs-lookup"><span data-stu-id="6ef6e-162">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="6ef6e-163">下列命令可取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="6ef6e-163">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```