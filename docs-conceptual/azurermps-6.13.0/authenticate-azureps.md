---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a42217c47c1e5101a708da87c15fc14004f2069
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259423"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="864f7-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="864f7-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="864f7-104">Azure PowerShell 支援數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="864f7-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="864f7-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="864f7-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="864f7-106">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="864f7-106">Sign in interactively</span></span>

<span data-ttu-id="864f7-107">若要以互動方式登入，請使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864f7-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="864f7-108">執行時，此 Cmdlet 會顯示對話方塊，提示您輸入與 Azure 帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="864f7-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="864f7-109">此驗證的效用限於目前的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="864f7-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="864f7-110">從 Azure PowerShell 6.3.0 開始，只要您保持登入 Windows，您的認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="864f7-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="864f7-111">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="864f7-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="864f7-112">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="864f7-112">Sign in with a service principal</span></span>

<span data-ttu-id="864f7-113">服務主體為非互動式 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="864f7-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="864f7-114">如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。</span><span class="sxs-lookup"><span data-stu-id="864f7-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="864f7-115">藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。</span><span class="sxs-lookup"><span data-stu-id="864f7-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="864f7-116">若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="864f7-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="864f7-117">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzureRmAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864f7-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="864f7-118">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="864f7-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="864f7-119">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864f7-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="864f7-120">這個 Cmdlet 會顯示對話方塊，讓您在其中輸入服務主體使用者識別碼和密碼。</span><span class="sxs-lookup"><span data-stu-id="864f7-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="864f7-121">使用 Azure 受控服務識別登入</span><span class="sxs-lookup"><span data-stu-id="864f7-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="864f7-122">適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。</span><span class="sxs-lookup"><span data-stu-id="864f7-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="864f7-123">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="864f7-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="864f7-124">受控識別僅適用於在 Azure 雲端中執行的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="864f7-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="864f7-125">若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="864f7-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="864f7-126">以雲端解決方案提供者 (CSP) 身分登入</span><span class="sxs-lookup"><span data-stu-id="864f7-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="864f7-127">[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) 登入需要使用 `-TenantId`。</span><span class="sxs-lookup"><span data-stu-id="864f7-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="864f7-128">一般來說，此參數可以提供作為租用戶識別碼或網域名稱。</span><span class="sxs-lookup"><span data-stu-id="864f7-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="864f7-129">不過，如果是 CSP 登入，則必須提供為**租用戶識別碼**。</span><span class="sxs-lookup"><span data-stu-id="864f7-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="864f7-130">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="864f7-130">Sign in to another Cloud</span></span>

<span data-ttu-id="864f7-131">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="864f7-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="864f7-132">針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。</span><span class="sxs-lookup"><span data-stu-id="864f7-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="864f7-133">例如，如果您的帳戶位於中國雲端：</span><span class="sxs-lookup"><span data-stu-id="864f7-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="864f7-134">下列命令可取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="864f7-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="864f7-135">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="864f7-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="864f7-136">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="864f7-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="864f7-137">可用來管理角色的 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="864f7-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="864f7-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="864f7-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="864f7-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="864f7-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="864f7-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="864f7-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="864f7-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="864f7-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="864f7-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="864f7-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="864f7-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="864f7-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="864f7-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="864f7-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)