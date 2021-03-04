---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901778"
---
# <span data-ttu-id="7ab2e-101">Az.NotificationHubs 模組</span><span class="sxs-lookup"><span data-stu-id="7ab2e-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="7ab2e-102">描述</span><span class="sxs-lookup"><span data-stu-id="7ab2e-102">Description</span></span>
<span data-ttu-id="7ab2e-103">本主題顯示 Azure 通知中樞 Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="7ab2e-104">通知中樞可用來傳送推入通知給多個用戶端 (不論這些用戶端所使用的平臺 (iOS、Android、Windows Phone 8、Windows 市集等 ) 。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="7ab2e-105">這些中樞大致相當於個別的應用程式：每一個 App 通常會有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="7ab2e-106">通知中樞是組織在稱為命名空間的邏輯容器內，而共用存取簽章 (SAS) 授權規則則用來管理中樞和命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="7ab2e-107">所有這些元素都可以使用通知中樞 Cmdlet 來管理。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="7ab2e-108">Az.NotificationHubs Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ab2e-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="7ab2e-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ab2e-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="7ab2e-110">獲得有關通知中樞的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="7ab2e-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7ab2e-112">獲得與通知中樞相關聯的授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="7ab2e-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="7ab2e-114">獲得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="7ab2e-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="7ab2e-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="7ab2e-116">獲得通知中樞的 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ab2e-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="7ab2e-118">獲得通知中樞命名空間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7ab2e-120">與通知中樞命名空間相關聯的授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="7ab2e-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="7ab2e-122">獲得與通知中樞命名空間授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="7ab2e-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ab2e-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="7ab2e-124">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7ab2e-126">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="7ab2e-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="7ab2e-128">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="7ab2e-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ab2e-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="7ab2e-130">建立通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7ab2e-132">建立授權規則，並將該規則指派給通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="7ab2e-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="7ab2e-134">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="7ab2e-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ab2e-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="7ab2e-136">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="7ab2e-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7ab2e-138">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ab2e-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="7ab2e-140">移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7ab2e-142">從通知中樞命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ab2e-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="7ab2e-144">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7ab2e-146">設定通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="7ab2e-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ab2e-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="7ab2e-148">設定通知中樞命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="7ab2e-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ab2e-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7ab2e-150">設定通知中樞命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7ab2e-150">Sets authorization rules for a notification hub namespace.</span></span>

