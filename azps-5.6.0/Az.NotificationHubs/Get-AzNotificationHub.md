---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: fe2949e5b7eb8c3c5f1261072e755bcbb0b6eb00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901777"
---
# <span data-ttu-id="00950-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00950-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="00950-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00950-102">SYNOPSIS</span></span>
<span data-ttu-id="00950-103">獲得有關通知中樞的資訊。</span><span class="sxs-lookup"><span data-stu-id="00950-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="00950-104">語法</span><span class="sxs-lookup"><span data-stu-id="00950-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00950-105">描述</span><span class="sxs-lookup"><span data-stu-id="00950-105">DESCRIPTION</span></span>
<span data-ttu-id="00950-106">**Get-AzNotificationHub** Cmdlet 會取得指定命名空間中通知中樞的資訊，並指派給指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="00950-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="00950-107">例如，您可以取得命名空間 ContosoNamespace 中所有通知中樞的資訊，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="00950-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="00950-108">或者，您可以使用 *NotificationHub* 參數，將所返回的資料限制為特定通知中樞的資訊。</span><span class="sxs-lookup"><span data-stu-id="00950-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="00950-109">通知中樞可用來傳送推入通知給多個用戶端，而不管這些用戶端所使用的平臺是 iOS、Android、Windows Phone 8 和 Windows 市集。</span><span class="sxs-lookup"><span data-stu-id="00950-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="00950-110">這些中樞大致相當於個別的應用程式，而且每一個 App 通常會有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="00950-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="00950-111">此 Cmdlet 只會獲得中樞本身的資訊。</span><span class="sxs-lookup"><span data-stu-id="00950-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="00950-112">其他 Cmdlet ，例如 Get-AzNotificationHubAuthorizationRules、Get-AzNotificationHubListKeys 和 Get-AzNotificationHubPNSCredentials，都需要取得中樞的授權規則、連接字串和平臺通知服務認證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="00950-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="00950-113">例子</span><span class="sxs-lookup"><span data-stu-id="00950-113">EXAMPLES</span></span>

### <span data-ttu-id="00950-114">範例 1：取得特定命名空間中所有通知中樞的資訊</span><span class="sxs-lookup"><span data-stu-id="00950-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="00950-115">此命令會獲得名稱為 ContosoNamespace 之命名空間中所有已指派給資源群組 ContosoNotificationsGroup 的通知中樞資訊。</span><span class="sxs-lookup"><span data-stu-id="00950-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="00950-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="00950-116">Example 2</span></span>

<span data-ttu-id="00950-117">獲得有關通知中樞的資訊。</span><span class="sxs-lookup"><span data-stu-id="00950-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="00950-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="00950-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="00950-119">參數</span><span class="sxs-lookup"><span data-stu-id="00950-119">PARAMETERS</span></span>

### <span data-ttu-id="00950-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00950-120">-DefaultProfile</span></span>
<span data-ttu-id="00950-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="00950-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00950-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="00950-122">-Namespace</span></span>
<span data-ttu-id="00950-123">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="00950-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="00950-124">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="00950-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="00950-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="00950-125">-NotificationHub</span></span>
<span data-ttu-id="00950-126">指定此 Cmdlet 獲得的通知中樞名稱。</span><span class="sxs-lookup"><span data-stu-id="00950-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="00950-127">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="00950-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="00950-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00950-128">-ResourceGroup</span></span>
<span data-ttu-id="00950-129">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="00950-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="00950-130">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="00950-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="00950-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00950-131">CommonParameters</span></span>
<span data-ttu-id="00950-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00950-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00950-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00950-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00950-134">輸入</span><span class="sxs-lookup"><span data-stu-id="00950-134">INPUTS</span></span>

### <span data-ttu-id="00950-135">System.String</span><span class="sxs-lookup"><span data-stu-id="00950-135">System.String</span></span>

## <span data-ttu-id="00950-136">輸出</span><span class="sxs-lookup"><span data-stu-id="00950-136">OUTPUTS</span></span>

### <span data-ttu-id="00950-137">Microsoft.Azure.Commands.NotificationHubs.models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="00950-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="00950-138">筆記</span><span class="sxs-lookup"><span data-stu-id="00950-138">NOTES</span></span>

## <span data-ttu-id="00950-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="00950-139">RELATED LINKS</span></span>

[<span data-ttu-id="00950-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="00950-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="00950-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="00950-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="00950-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="00950-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="00950-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00950-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="00950-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00950-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="00950-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00950-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


