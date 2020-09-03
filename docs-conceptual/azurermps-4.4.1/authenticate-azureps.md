---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7a79af082ac7c3ffe923a7f0a1c7854b7a562df7
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244359"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="e9ed8-103">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="e9ed8-103">Sign in with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="e9ed8-104">Azure PowerShell 支援多種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="e9ed8-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="e9ed8-106">以互動方式登入</span><span class="sxs-lookup"><span data-stu-id="e9ed8-106">Sign in interactively</span></span>

<span data-ttu-id="e9ed8-107">若要以互動方式登入，請使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="e9ed8-108">執行時，此 Cmdlet 會顯示對話方塊，提示您輸入與 Azure 帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="e9ed8-109">驗證時，會針對目前的 PowerShell 工作階段儲存該資訊，關閉對話方塊，您就具有所有 Azure PowerShell Cmdlet 的存取權。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9ed8-110">從 Azure PowerShell 6.3.0 開始，只要您保持登入 Windows，您的認證就會在多個 PowerShell 工作階段之間共用。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="e9ed8-111">如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="e9ed8-112">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="e9ed8-112">Sign in with a service principal</span></span>

<span data-ttu-id="e9ed8-113">服務主體提供您建立非互動式帳戶的方式，以用來操控資源。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="e9ed8-114">服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="e9ed8-115">僅授與服務主體所需的最低權限，可確保您的自動化指令碼會更加安全。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="e9ed8-116">如果您需要建立服務主體以便與 Azure PowerShell 搭配使用，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="e9ed8-117">若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzureRmAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="e9ed8-118">您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="e9ed8-119">若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="e9ed8-120">這個 Cmdlet 會顯示對話方塊，讓您在其中輸入服務主體使用者識別碼和密碼。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="e9ed8-121">使用適用於 Azure 資源的受控識別登入</span><span class="sxs-lookup"><span data-stu-id="e9ed8-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="e9ed8-122">適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="e9ed8-123">您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="e9ed8-124">受控識別僅適用於在 Azure 雲端中執行的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="e9ed8-125">若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="e9ed8-126">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="e9ed8-126">Sign in to another Cloud</span></span>

<span data-ttu-id="e9ed8-127">Azure 雲端服務提供不同的環境，以遵循各個區域的資料處理法規。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="e9ed8-128">如果您的 Azure 帳戶位於與其中一個區域相關聯的雲端，則需要在登入時指定環境。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="e9ed8-129">例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：</span><span class="sxs-lookup"><span data-stu-id="e9ed8-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="e9ed8-130">使用下列命令來取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="e9ed8-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="e9ed8-131">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="e9ed8-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="e9ed8-132">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="e9ed8-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="e9ed8-133">可用來管理角色的 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e9ed8-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="e9ed8-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e9ed8-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="e9ed8-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e9ed8-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="e9ed8-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e9ed8-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="e9ed8-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e9ed8-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="e9ed8-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e9ed8-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="e9ed8-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e9ed8-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="e9ed8-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e9ed8-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
