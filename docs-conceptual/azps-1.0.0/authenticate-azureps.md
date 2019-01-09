---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786674"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="380f6-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="380f6-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="380f6-104">Azure PowerShell 支援數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="380f6-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="380f6-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="380f6-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="380f6-106">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="380f6-106">Sign in interactively</span></span>

<span data-ttu-id="380f6-107">若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="380f6-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="380f6-108">執行時，此 Cmdlet 會出示權杖字串。</span><span class="sxs-lookup"><span data-stu-id="380f6-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="380f6-109">若要登入，請複製這個字串並將它貼至瀏覽器中的 https://microsoft.com/devicelogin。</span><span class="sxs-lookup"><span data-stu-id="380f6-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="380f6-110">PowerShell 工作階段接著會進行驗證以便連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="380f6-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="380f6-111">此驗證的效用限於目前的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="380f6-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="380f6-112">只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="380f6-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="380f6-113">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="380f6-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="380f6-114">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="380f6-114">Sign in with a service principal</span></span>

<span data-ttu-id="380f6-115">服務主體為非互動式 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="380f6-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="380f6-116">如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。</span><span class="sxs-lookup"><span data-stu-id="380f6-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="380f6-117">藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。</span><span class="sxs-lookup"><span data-stu-id="380f6-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="380f6-118">若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="380f6-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="380f6-119">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="380f6-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="380f6-120">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="380f6-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="380f6-121">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="380f6-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="380f6-122">這個 Cmdlet 會顯示請您輸入服務主體使用者識別碼和密碼的提示。</span><span class="sxs-lookup"><span data-stu-id="380f6-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="380f6-123">使用 Azure 受控服務識別登入</span><span class="sxs-lookup"><span data-stu-id="380f6-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="380f6-124">適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。</span><span class="sxs-lookup"><span data-stu-id="380f6-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="380f6-125">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="380f6-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="380f6-126">受控識別僅適用於在 Azure 雲端中執行的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="380f6-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="380f6-127">若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="380f6-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="380f6-128">以雲端解決方案提供者 (CSP) 身分登入</span><span class="sxs-lookup"><span data-stu-id="380f6-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="380f6-129">[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) 登入需要使用 `-TenantId`。</span><span class="sxs-lookup"><span data-stu-id="380f6-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="380f6-130">一般來說，此參數可以提供作為租用戶識別碼或網域名稱。</span><span class="sxs-lookup"><span data-stu-id="380f6-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="380f6-131">不過，如果是 CSP 登入，則必須提供為**租用戶識別碼**。</span><span class="sxs-lookup"><span data-stu-id="380f6-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="380f6-132">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="380f6-132">Sign in to another Cloud</span></span>

<span data-ttu-id="380f6-133">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="380f6-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="380f6-134">針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。</span><span class="sxs-lookup"><span data-stu-id="380f6-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="380f6-135">例如，如果您的帳戶位於中國雲端：</span><span class="sxs-lookup"><span data-stu-id="380f6-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="380f6-136">下列命令可取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="380f6-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="380f6-137">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="380f6-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="380f6-138">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="380f6-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="380f6-139">可用來管理角色的 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="380f6-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="380f6-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="380f6-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="380f6-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="380f6-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="380f6-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="380f6-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="380f6-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="380f6-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="380f6-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="380f6-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="380f6-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="380f6-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="380f6-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="380f6-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
