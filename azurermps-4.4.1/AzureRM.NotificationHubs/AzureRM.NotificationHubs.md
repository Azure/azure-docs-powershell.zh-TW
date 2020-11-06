---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: 2997b465f02801e2b01004d45209e95af7998ff6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442124"
---
# <span data-ttu-id="6272b-101">AzureRM NotificationHubs Module</span><span class="sxs-lookup"><span data-stu-id="6272b-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="6272b-102">說明</span><span class="sxs-lookup"><span data-stu-id="6272b-102">Description</span></span>
<span data-ttu-id="6272b-103">本主題顯示 Azure 通知中樞 Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="6272b-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="6272b-104">通知中樞是用來傳送推播通知給多個用戶端，而不考慮平臺 (iOS、Android、Windows Phone 8、Windows 市集中等等。 ) 由這些用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="6272b-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="6272b-105">這些中樞大致相當於個別 app：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6272b-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="6272b-106">通知中心是組織在稱為命名空間的邏輯容器中，而共用存取簽章 (SAS) 授權規則是用來管理中樞和命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="6272b-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="6272b-107">所有這些元素都可以使用通知中心 Cmdlet 來管理。</span><span class="sxs-lookup"><span data-stu-id="6272b-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="6272b-108">AzureRM NotificationHubs Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6272b-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="6272b-109">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6272b-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="6272b-110">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6272b-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="6272b-111">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="6272b-112">取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6272b-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="6272b-113">AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="6272b-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="6272b-114">取得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="6272b-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="6272b-115">AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="6272b-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="6272b-116">取得通知中樞的 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="6272b-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="6272b-117">AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6272b-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="6272b-118">取得通知中心命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6272b-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-119">AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="6272b-120">取得與通知中心命名空間相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6272b-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-121">AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="6272b-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="6272b-122">取得與通知中心命名空間授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="6272b-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="6272b-123">新-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6272b-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="6272b-124">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6272b-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="6272b-125">新-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="6272b-126">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6272b-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="6272b-127">新-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="6272b-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="6272b-128">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="6272b-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="6272b-129">新-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6272b-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="6272b-130">建立通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="6272b-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-131">新-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="6272b-132">建立授權規則，並將該規則指派給通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="6272b-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-133">新-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="6272b-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="6272b-134">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="6272b-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="6272b-135">移除-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6272b-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="6272b-136">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6272b-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="6272b-137">移除-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="6272b-138">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="6272b-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="6272b-139">移除-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6272b-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="6272b-140">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6272b-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-141">移除-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="6272b-142">從通知中心命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="6272b-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6272b-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="6272b-144">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6272b-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="6272b-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="6272b-146">設定通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="6272b-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="6272b-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6272b-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="6272b-148">設定通知中心命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6272b-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="6272b-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6272b-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="6272b-150">設定通知中心命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="6272b-150">Sets authorization rules for a notification hub namespace.</span></span>

