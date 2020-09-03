---
title: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
description: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: cfe5833bd8bbfac53f65695f8bdfbd7b946a8852
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240653"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="2a612-103">使用多個 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="2a612-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="2a612-104">大部分的 Azure 使用者永遠只會有單一訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a612-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="2a612-105">不過，如果您是多個組織的成員，或貴組織跨多個群組分割了特定資源的存取權，您可能會在 Azure 中擁有多個訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a612-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="2a612-106">CLI 支援全域及依命令選取訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a612-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="2a612-107">如需訂用帳戶、帳單與成本管理的詳細資訊，請參閱[帳單與成本管理文件](/azure/billing/)。</span><span class="sxs-lookup"><span data-stu-id="2a612-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="2a612-108">租用戶、使用者和訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="2a612-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="2a612-109">您可能對於 Azure 中租用戶、使用者和訂用帳戶之間的差異感到混淆。</span><span class="sxs-lookup"><span data-stu-id="2a612-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="2a612-110">_租用戶_是指包含整個組織的 Azure Active Directory 實體。</span><span class="sxs-lookup"><span data-stu-id="2a612-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="2a612-111">租用戶至少有一個_訂用帳戶_和_使用者_。</span><span class="sxs-lookup"><span data-stu-id="2a612-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="2a612-112">使用者為個人，且只與一個租用戶相關，也就是其所屬的組織。</span><span class="sxs-lookup"><span data-stu-id="2a612-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="2a612-113">使用者是會登入 Azure 來建立、管理並使用資源的帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a612-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="2a612-114">使用者可能擁有多個_訂用帳戶_的存取權，訂用帳戶是與 Microsoft 的協議，可使用包括 Azure 等雲端服務。</span><span class="sxs-lookup"><span data-stu-id="2a612-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="2a612-115">每個資源會與訂用帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="2a612-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="2a612-116">若要深入了解租用戶、使用者和訂用帳戶之間的差異，請參閱 [Azure 雲端術語字典](/azure/azure-glossary-cloud-terminology)。</span><span class="sxs-lookup"><span data-stu-id="2a612-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="2a612-117">若要了解如何將新訂用帳戶新增至您的 Azure Active Directory 租用戶，請參閱[如何將 Azure 訂用帳戶新增至 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。</span><span class="sxs-lookup"><span data-stu-id="2a612-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="2a612-118">若要了解如何登入特定租用戶，請參閱[使用 Azure PowerShell 登入](/powershell/azure/authenticate-azureps)。</span><span class="sxs-lookup"><span data-stu-id="2a612-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="2a612-119">變更使用中的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="2a612-119">Change the active subscription</span></span>

<span data-ttu-id="2a612-120">在 Azure PowerShell 中，存取訂用帳戶資源需要變更與目前 Azure 工作階段相關聯的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a612-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="2a612-121">可透過修改使用中工作階段內容、租用戶資訊、訂用帳戶及應該執行的使用者 Cmdlet 完成。</span><span class="sxs-lookup"><span data-stu-id="2a612-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="2a612-122">為了變更訂用帳戶，首先需要使用 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) 擷取 Azure PowerShell Context 物件，並使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) 變更目前內容。</span><span class="sxs-lookup"><span data-stu-id="2a612-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="2a612-123">接下來的範例顯示如何取得目前使用中租用戶中的訂用帳戶，並將其設為使用中工作階段：</span><span class="sxs-lookup"><span data-stu-id="2a612-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="2a612-124">若要了解更多 Azure PowerShell 內容的詳細資訊，包含如何儲存並快速在不同內容間切換以輕鬆搭配多個訂用帳戶使用，請參閱[用 Azure PowerShell 內容保存認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="2a612-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
