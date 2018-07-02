---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者、服務主體身分登入，或使用 MSI 登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: e2eb6767d16dd15529b35b7a4134f4dcdd257d60
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237642"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="db316-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="db316-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="db316-104">Azure PowerShell 支援多種登入方法。</span><span class="sxs-lookup"><span data-stu-id="db316-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="db316-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="db316-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="db316-106">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="db316-106">Sign in interactively</span></span>

<span data-ttu-id="db316-107">若要以互動方式登入，請使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db316-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="db316-108">執行時，此 Cmdlet 會顯示對話方塊，提示您輸入與 Azure 帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="db316-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="db316-109">驗證時，會針對目前的 PowerShell 工作階段儲存該資訊，關閉對話方塊，您就具有所有 Azure PowerShell Cmdlet 的存取權。</span><span class="sxs-lookup"><span data-stu-id="db316-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db316-110">此登入_僅_適用於目前的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="db316-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="db316-111">若要在多個工作階段之間保持登入，請參閱[持續性認證](context-persistence.md)上的文章。</span><span class="sxs-lookup"><span data-stu-id="db316-111">To persist the login across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="db316-112">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="db316-112">Sign in with a service principal</span></span>

<span data-ttu-id="db316-113">服務主體提供您建立非互動式帳戶的方式，以用來操控資源。</span><span class="sxs-lookup"><span data-stu-id="db316-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="db316-114">服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。</span><span class="sxs-lookup"><span data-stu-id="db316-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="db316-115">僅授與服務主體所需的最低權限，可確保您的自動化指令碼會更加安全。</span><span class="sxs-lookup"><span data-stu-id="db316-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="db316-116">如果您需要建立服務主體以便與 Azure PowerShell 搭配使用，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="db316-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="db316-117">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzureRmAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db316-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="db316-118">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="db316-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="db316-119">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db316-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="db316-120">這個 Cmdlet 會顯示對話方塊，讓您在其中輸入服務主體使用者識別碼和密碼。</span><span class="sxs-lookup"><span data-stu-id="db316-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="db316-121">使用 Azure 虛擬機受控服務識別登入</span><span class="sxs-lookup"><span data-stu-id="db316-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="db316-122">受控服務識別 (MSI) 是 Azure Active Directory 的預覽功能。</span><span class="sxs-lookup"><span data-stu-id="db316-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="db316-123">您可以使用 MSI 服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="db316-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="db316-124">MSI 僅適用於在 Azure 雲端中執行的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="db316-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="db316-125">如需 MSI 的詳細資訊，請參閱[如何使用 Azure VM 受控服務識別登入 (MSI) 進行登入和取得權杖](/azure/active-directory/msi-how-to-get-access-token-using-msi)。</span><span class="sxs-lookup"><span data-stu-id="db316-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="db316-126">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="db316-126">Sign in to another Cloud</span></span>

<span data-ttu-id="db316-127">Azure 雲端服務提供不同的環境，以遵循各個區域的資料處理法規。</span><span class="sxs-lookup"><span data-stu-id="db316-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="db316-128">如果您的 Azure 帳戶位於與其中一個區域相關聯的雲端，則需要在登入時指定環境。</span><span class="sxs-lookup"><span data-stu-id="db316-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="db316-129">例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：</span><span class="sxs-lookup"><span data-stu-id="db316-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="db316-130">使用下列命令來取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="db316-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="db316-131">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="db316-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="db316-132">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="db316-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="db316-133">可用來管理角色的 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db316-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="db316-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db316-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="db316-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="db316-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="db316-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db316-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="db316-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="db316-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="db316-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db316-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="db316-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="db316-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="db316-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="db316-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
