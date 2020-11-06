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
ms.openlocfilehash: e9f6fce095bd7ea4c494cf778587c3853f347c38
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611244"
---
# <span data-ttu-id="cd4fd-101">AzureRM NotificationHubs Module</span><span class="sxs-lookup"><span data-stu-id="cd4fd-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="cd4fd-102">說明</span><span class="sxs-lookup"><span data-stu-id="cd4fd-102">Description</span></span>
<span data-ttu-id="cd4fd-103">本主題顯示 Azure 通知中樞 Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="cd4fd-104">通知中樞是用來傳送推播通知給多個用戶端，而不考慮平臺 (iOS、Android、Windows Phone 8、Windows 市集中等等。 ) 由這些用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="cd4fd-105">這些中樞大致相當於個別 app：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="cd4fd-106">通知中心是組織在稱為命名空間的邏輯容器中，而共用存取簽章 (SAS) 授權規則是用來管理中樞和命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="cd4fd-107">所有這些元素都可以使用通知中心 Cmdlet 來管理。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="cd4fd-108">AzureRM NotificationHubs Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd4fd-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="cd4fd-109">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cd4fd-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="cd4fd-110">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="cd4fd-111">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="cd4fd-112">取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-113">AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="cd4fd-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="cd4fd-114">取得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="cd4fd-115">AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="cd4fd-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="cd4fd-116">取得通知中樞的 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-117">AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cd4fd-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="cd4fd-118">取得通知中心命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-119">AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="cd4fd-120">取得與通知中心命名空間相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-121">AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="cd4fd-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="cd4fd-122">取得與通知中心命名空間授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="cd4fd-123">新-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cd4fd-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="cd4fd-124">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-125">新-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="cd4fd-126">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-127">新-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="cd4fd-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="cd4fd-128">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="cd4fd-129">新-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cd4fd-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="cd4fd-130">建立通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-131">新-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="cd4fd-132">建立授權規則，並將該規則指派給通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-133">新-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="cd4fd-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="cd4fd-134">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="cd4fd-135">移除-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cd4fd-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="cd4fd-136">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="cd4fd-137">移除-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="cd4fd-138">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-139">移除-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cd4fd-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="cd4fd-140">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-141">移除-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="cd4fd-142">從通知中心命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cd4fd-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="cd4fd-144">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="cd4fd-146">設定通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="cd4fd-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cd4fd-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="cd4fd-148">設定通知中心命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="cd4fd-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cd4fd-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="cd4fd-150">設定通知中心命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="cd4fd-150">Sets authorization rules for a notification hub namespace.</span></span>

