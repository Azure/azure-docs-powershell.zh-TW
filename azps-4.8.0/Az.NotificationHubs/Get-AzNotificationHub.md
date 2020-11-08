---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135753"
---
# <span data-ttu-id="e3476-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e3476-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="e3476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3476-102">SYNOPSIS</span></span>
<span data-ttu-id="e3476-103">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3476-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="e3476-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3476-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3476-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3476-105">DESCRIPTION</span></span>
<span data-ttu-id="e3476-106">**AzNotificationHub** Cmdlet 會取得指定命名空間中的通知中心相關資訊，並指派給指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e3476-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="e3476-107">例如，您可以取得命名空間 ContosoNamespace 中所有通知中心的資訊，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="e3476-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="e3476-108">或者，您也可以使用 *NotificationHub* 參數，將傳回的資料限制為特定通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3476-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="e3476-109">通知中樞是用來傳送推播通知給多個用戶端，而不論平臺為何（例如 iOS、Android、Windows Phone 8 和 Windows Store）都是由這些用戶端所使用。</span><span class="sxs-lookup"><span data-stu-id="e3476-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="e3476-110">這些中樞大致相當於個別應用程式，而您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e3476-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="e3476-111">這個 Cmdlet 只會取得中心本身的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3476-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="e3476-112">您需要使用其他 Cmdlet （例如 AzNotificationHubAuthorizationRules、AzNotificationHubListKeys 和 AzNotificationHubPNSCredentials）來取得中樞的授權規則、連接字串及平臺通知服務認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3476-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="e3476-113">示例</span><span class="sxs-lookup"><span data-stu-id="e3476-113">EXAMPLES</span></span>

### <span data-ttu-id="e3476-114">範例1：取得特定命名空間中所有通知中心的相關資訊</span><span class="sxs-lookup"><span data-stu-id="e3476-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="e3476-115">這個命令會取得名為 ContosoNamespace 的命名空間中已指派給資源群組 ContosoNotificationsGroup 的所有通知中心的資訊。</span><span class="sxs-lookup"><span data-stu-id="e3476-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="e3476-116">參數</span><span class="sxs-lookup"><span data-stu-id="e3476-116">PARAMETERS</span></span>

### <span data-ttu-id="e3476-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3476-117">-DefaultProfile</span></span>
<span data-ttu-id="e3476-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e3476-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e3476-119">-Namespace</span></span>
<span data-ttu-id="e3476-120">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="e3476-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="e3476-121">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="e3476-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e3476-122">-NotificationHub</span></span>
<span data-ttu-id="e3476-123">指定此 Cmdlet 所取得之通知中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3476-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="e3476-124">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="e3476-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3476-125">-ResourceGroup</span></span>
<span data-ttu-id="e3476-126">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="e3476-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="e3476-127">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="e3476-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3476-128">CommonParameters</span></span>
<span data-ttu-id="e3476-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3476-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3476-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3476-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3476-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e3476-131">INPUTS</span></span>

### <span data-ttu-id="e3476-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e3476-132">System.String</span></span>

## <span data-ttu-id="e3476-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e3476-133">OUTPUTS</span></span>

### <span data-ttu-id="e3476-134">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="e3476-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="e3476-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e3476-135">NOTES</span></span>

## <span data-ttu-id="e3476-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3476-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3476-137">AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e3476-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e3476-138">AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="e3476-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="e3476-139">AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="e3476-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="e3476-140">新-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e3476-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="e3476-141">移除-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e3476-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="e3476-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e3476-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


