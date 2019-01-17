---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341953"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="fad0d-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="fad0d-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="fad0d-104">Azure PowerShell 支援數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="fad0d-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="fad0d-105">要開始使用的最簡單方法是透過 [Azure Cloud Shell](/azure/cloud-shell/overview)，這會自動將您登入。</span><span class="sxs-lookup"><span data-stu-id="fad0d-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="fad0d-106">您可以使用本機安裝，以互動方式透過瀏覽器登入。</span><span class="sxs-lookup"><span data-stu-id="fad0d-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="fad0d-107">在撰寫自動化指令碼時，建議的方法是使用[服務主體](create-azure-service-principal-azureps.md)搭配必要權限。</span><span class="sxs-lookup"><span data-stu-id="fad0d-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="fad0d-108">當您依自身的使用案例儘可能地限制登入權限時，同時也是在協助維護 Azure 資源的安全。</span><span class="sxs-lookup"><span data-stu-id="fad0d-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="fad0d-109">在登入之後，系統會針對您的預設訂用帳戶來執行命令。</span><span class="sxs-lookup"><span data-stu-id="fad0d-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="fad0d-110">若要變更工作階段作用中的訂用帳戶，請使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fad0d-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="fad0d-111">若要變更登入 Azure PowerShell 時使用的預設訂用帳戶，請使用 [Set-AzDefault](/powershell/module/az.accounts/set-azdefault)。</span><span class="sxs-lookup"><span data-stu-id="fad0d-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="fad0d-112">只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="fad0d-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="fad0d-113">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="fad0d-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="fad0d-114">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="fad0d-114">Sign in interactively</span></span>

<span data-ttu-id="fad0d-115">若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fad0d-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="fad0d-116">執行時，此 Cmdlet 會出示權杖字串。</span><span class="sxs-lookup"><span data-stu-id="fad0d-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="fad0d-117">若要登入，請複製這個字串並將它貼至瀏覽器中的 https://microsoft.com/devicelogin。</span><span class="sxs-lookup"><span data-stu-id="fad0d-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="fad0d-118">PowerShell 工作階段會進行驗證以便連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="fad0d-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="fad0d-119">使用認證登入</span><span class="sxs-lookup"><span data-stu-id="fad0d-119">Sign in with credentials</span></span>

<span data-ttu-id="fad0d-120">您也可以使用已授權的 `PSCredential` 物件登入，以連線到 Azure。</span><span class="sxs-lookup"><span data-stu-id="fad0d-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="fad0d-121">取得認證物件最簡單的方式是使用[](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fad0d-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="fad0d-122">執行時，此 Cmdlet 會提示您輸入使用者名稱/密碼認證組。</span><span class="sxs-lookup"><span data-stu-id="fad0d-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="fad0d-123">這個方法不適用於 Microsoft 帳戶或啟用雙重要素驗證的帳戶。</span><span class="sxs-lookup"><span data-stu-id="fad0d-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="fad0d-124">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="fad0d-124">Sign in with a service principal</span></span>

<span data-ttu-id="fad0d-125">服務主體為非互動式 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fad0d-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="fad0d-126">如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。</span><span class="sxs-lookup"><span data-stu-id="fad0d-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="fad0d-127">藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。</span><span class="sxs-lookup"><span data-stu-id="fad0d-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="fad0d-128">若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="fad0d-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="fad0d-129">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fad0d-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="fad0d-130">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="fad0d-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="fad0d-131">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fad0d-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="fad0d-132">這個 Cmdlet 會顯示請您輸入服務主體使用者識別碼和密碼的提示。</span><span class="sxs-lookup"><span data-stu-id="fad0d-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="fad0d-133">使用受控識別登入</span><span class="sxs-lookup"><span data-stu-id="fad0d-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="fad0d-134">受控識別是 Azure Active Directory 的功能。</span><span class="sxs-lookup"><span data-stu-id="fad0d-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="fad0d-135">受控識別是指派給在 Azure 中執行之資源的服務主體。</span><span class="sxs-lookup"><span data-stu-id="fad0d-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="fad0d-136">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="fad0d-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="fad0d-137">只有在 Azure 雲端中執行的虛擬機器才能使用受控識別。</span><span class="sxs-lookup"><span data-stu-id="fad0d-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="fad0d-138">若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="fad0d-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="fad0d-139">以非預設租用戶或雲端解決方案提供者 (CSP) 登入</span><span class="sxs-lookup"><span data-stu-id="fad0d-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="fad0d-140">如果您的帳戶與多個租用戶相關聯，則需要使用連線時的 `-TenantId` 參數方可登入。</span><span class="sxs-lookup"><span data-stu-id="fad0d-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="fad0d-141">此參數可使用任何其他登入方法。</span><span class="sxs-lookup"><span data-stu-id="fad0d-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="fad0d-142">登入時，此參數值可以是租用戶的 Azure 物件識別碼 (租用戶識別碼)，或租用戶的完整的網域名稱。</span><span class="sxs-lookup"><span data-stu-id="fad0d-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="fad0d-143">如果您是[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/)，則 `-TenantId` 值**必須**是租用戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fad0d-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="fad0d-144">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="fad0d-144">Sign in to another Cloud</span></span>

<span data-ttu-id="fad0d-145">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="fad0d-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="fad0d-146">針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。</span><span class="sxs-lookup"><span data-stu-id="fad0d-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="fad0d-147">例如，如果您的帳戶位於中國雲端：</span><span class="sxs-lookup"><span data-stu-id="fad0d-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="fad0d-148">下列命令可取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="fad0d-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```