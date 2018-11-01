---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: c19d9ade0f69f4af9f14c68ad22b327c27c8ccfd
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738201"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="439ae-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="439ae-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="439ae-104">Azure PowerShell 支援數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="439ae-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="439ae-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="439ae-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="439ae-106">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="439ae-106">Sign in interactively</span></span>

<span data-ttu-id="439ae-107">若要以互動方式登入，請使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="439ae-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="439ae-108">執行時，此 Cmdlet 會顯示對話方塊，提示您輸入與 Azure 帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="439ae-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="439ae-109">此驗證的效用限於目前的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="439ae-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="439ae-110">從 Azure PowerShell 6.3.0 開始，只要您保持登入 Windows，您的認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="439ae-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="439ae-111">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="439ae-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="439ae-112">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="439ae-112">Sign in with a service principal</span></span>

<span data-ttu-id="439ae-113">服務主體為非互動式 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="439ae-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="439ae-114">如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。</span><span class="sxs-lookup"><span data-stu-id="439ae-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="439ae-115">藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。</span><span class="sxs-lookup"><span data-stu-id="439ae-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="439ae-116">若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="439ae-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="439ae-117">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzureRmAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="439ae-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="439ae-118">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="439ae-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="439ae-119">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="439ae-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="439ae-120">這個 Cmdlet 會顯示對話方塊，讓您在其中輸入服務主體使用者識別碼和密碼。</span><span class="sxs-lookup"><span data-stu-id="439ae-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="439ae-121">使用 Azure 受控服務識別登入</span><span class="sxs-lookup"><span data-stu-id="439ae-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="439ae-122">適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。</span><span class="sxs-lookup"><span data-stu-id="439ae-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="439ae-123">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="439ae-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="439ae-124">受控識別僅適用於在 Azure 雲端中執行的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="439ae-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="439ae-125">若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="439ae-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="439ae-126">以雲端解決方案提供者 (CSP) 身分登入</span><span class="sxs-lookup"><span data-stu-id="439ae-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="439ae-127">[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) 登入需要使用 `-TenantId`。</span><span class="sxs-lookup"><span data-stu-id="439ae-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="439ae-128">一般來說，此參數可以提供作為租用戶識別碼或網域名稱。</span><span class="sxs-lookup"><span data-stu-id="439ae-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="439ae-129">不過，如果是 CSP 登入，則必須提供為**租用戶識別碼**。</span><span class="sxs-lookup"><span data-stu-id="439ae-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="439ae-130">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="439ae-130">Sign in to another Cloud</span></span>

<span data-ttu-id="439ae-131">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="439ae-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="439ae-132">針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。</span><span class="sxs-lookup"><span data-stu-id="439ae-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="439ae-133">例如，如果您的帳戶位於中國雲端：</span><span class="sxs-lookup"><span data-stu-id="439ae-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="439ae-134">下列命令可取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="439ae-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="439ae-135">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="439ae-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="439ae-136">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="439ae-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="439ae-137">可用來管理角色的 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="439ae-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="439ae-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="439ae-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="439ae-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="439ae-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="439ae-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="439ae-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="439ae-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="439ae-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="439ae-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="439ae-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="439ae-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="439ae-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="439ae-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="439ae-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
