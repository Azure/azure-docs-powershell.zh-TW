---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: 2bb7d6f6addbbbf91f7f9f93e7e30de9cb3ece81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456556"
---
# <span data-ttu-id="d954a-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d954a-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="d954a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d954a-102">SYNOPSIS</span></span>
<span data-ttu-id="d954a-103">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d954a-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d954a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d954a-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d954a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d954a-105">DESCRIPTION</span></span>
<span data-ttu-id="d954a-106">**AzureRmNotificationHub** Cmdlet 會取得指定命名空間中的通知中心相關資訊，並指派給指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d954a-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="d954a-107">例如，您可以取得命名空間 ContosoNamespace 中所有通知中心的資訊，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="d954a-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="d954a-108">或者，您也可以使用 *NotificationHub* 參數，將傳回的資料限制為特定通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d954a-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="d954a-109">通知中樞是用來傳送推播通知給多個用戶端，而不論平臺為何（例如 iOS、Android、Windows Phone 8 和 Windows Store）都是由這些用戶端所使用。</span><span class="sxs-lookup"><span data-stu-id="d954a-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="d954a-110">這些中樞大致相當於個別應用程式，而您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d954a-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="d954a-111">這個 Cmdlet 只會取得中心本身的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d954a-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="d954a-112">您需要使用其他 Cmdlet （例如 AzureRmNotificationHubAuthorizationRules、AzureRmNotificationHubListKeys 和 AzureRmNotificationHubPNSCredentials）來取得中樞的授權規則、連接字串及平臺通知服務認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d954a-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="d954a-113">示例</span><span class="sxs-lookup"><span data-stu-id="d954a-113">EXAMPLES</span></span>

### <span data-ttu-id="d954a-114">範例1：取得特定命名空間中所有通知中心的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d954a-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="d954a-115">這個命令會取得名為 ContosoNamespace 的命名空間中已指派給資源群組 ContosoNotificationsGroup 的所有通知中心的資訊。</span><span class="sxs-lookup"><span data-stu-id="d954a-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="d954a-116">參數</span><span class="sxs-lookup"><span data-stu-id="d954a-116">PARAMETERS</span></span>

### <span data-ttu-id="d954a-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d954a-117">-Namespace</span></span>
<span data-ttu-id="d954a-118">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="d954a-118">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="d954a-119">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="d954a-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d954a-120">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d954a-120">-NotificationHub</span></span>
<span data-ttu-id="d954a-121">指定此 Cmdlet 所取得之通知中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="d954a-121">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="d954a-122">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="d954a-122">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="d954a-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d954a-123">-ResourceGroup</span></span>
<span data-ttu-id="d954a-124">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="d954a-124">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="d954a-125">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="d954a-125">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d954a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d954a-126">-DefaultProfile</span></span>
<span data-ttu-id="d954a-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d954a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d954a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d954a-128">CommonParameters</span></span>
<span data-ttu-id="d954a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d954a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d954a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d954a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d954a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d954a-131">INPUTS</span></span>

## <span data-ttu-id="d954a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d954a-132">OUTPUTS</span></span>

### <span data-ttu-id="d954a-133">[System.object]. 清單 ' 1 [NotificationHubs]。 NotificationHubAttributes]</span><span class="sxs-lookup"><span data-stu-id="d954a-133">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="d954a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d954a-134">NOTES</span></span>

## <span data-ttu-id="d954a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d954a-135">RELATED LINKS</span></span>

[<span data-ttu-id="d954a-136">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d954a-136">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d954a-137">AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="d954a-137">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="d954a-138">AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="d954a-138">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="d954a-139">新-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d954a-139">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="d954a-140">移除-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d954a-140">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="d954a-141">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d954a-141">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


