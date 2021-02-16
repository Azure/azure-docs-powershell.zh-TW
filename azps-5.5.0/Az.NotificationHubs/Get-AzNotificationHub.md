---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135647"
---
# <span data-ttu-id="3edea-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edea-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="3edea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3edea-102">SYNOPSIS</span></span>
<span data-ttu-id="3edea-103">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3edea-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="3edea-104">句法</span><span class="sxs-lookup"><span data-stu-id="3edea-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3edea-105">說明</span><span class="sxs-lookup"><span data-stu-id="3edea-105">DESCRIPTION</span></span>
<span data-ttu-id="3edea-106">**AzNotificationHub** Cmdlet 會取得指定命名空間中的通知中心相關資訊，並指派給指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3edea-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="3edea-107">例如，您可以取得命名空間 ContosoNamespace 中所有通知中心的資訊，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="3edea-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="3edea-108">或者，您也可以使用 *NotificationHub* 參數，將傳回的資料限制為特定通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3edea-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="3edea-109">通知中樞是用來傳送推播通知給多個用戶端，而不論平臺為何（例如 iOS、Android、Windows Phone 8 和 Windows Store）都是由這些用戶端所使用。</span><span class="sxs-lookup"><span data-stu-id="3edea-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="3edea-110">這些中樞大致相當於個別應用程式，而您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="3edea-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="3edea-111">這個 Cmdlet 只會取得中心本身的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3edea-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="3edea-112">您需要使用其他 Cmdlet （例如 AzNotificationHubAuthorizationRules、AzNotificationHubListKeys 和 AzNotificationHubPNSCredentials）來取得中樞的授權規則、連接字串及平臺通知服務認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3edea-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="3edea-113">示例</span><span class="sxs-lookup"><span data-stu-id="3edea-113">EXAMPLES</span></span>

### <span data-ttu-id="3edea-114">範例1：取得特定命名空間中所有通知中心的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3edea-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="3edea-115">這個命令會取得名為 ContosoNamespace 的命名空間中已指派給資源群組 ContosoNotificationsGroup 的所有通知中心的資訊。</span><span class="sxs-lookup"><span data-stu-id="3edea-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="3edea-116">範例2</span><span class="sxs-lookup"><span data-stu-id="3edea-116">Example 2</span></span>

<span data-ttu-id="3edea-117">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3edea-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="3edea-118"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="3edea-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="3edea-119">參數</span><span class="sxs-lookup"><span data-stu-id="3edea-119">PARAMETERS</span></span>

### <span data-ttu-id="3edea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edea-120">-DefaultProfile</span></span>
<span data-ttu-id="3edea-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3edea-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3edea-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3edea-122">-Namespace</span></span>
<span data-ttu-id="3edea-123">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="3edea-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3edea-124">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="3edea-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3edea-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edea-125">-NotificationHub</span></span>
<span data-ttu-id="3edea-126">指定此 Cmdlet 所取得之通知中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="3edea-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="3edea-127">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="3edea-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3edea-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3edea-128">-ResourceGroup</span></span>
<span data-ttu-id="3edea-129">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="3edea-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3edea-130">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="3edea-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3edea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edea-131">CommonParameters</span></span>
<span data-ttu-id="3edea-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3edea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edea-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3edea-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edea-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3edea-134">INPUTS</span></span>

### <span data-ttu-id="3edea-135">System.object</span><span class="sxs-lookup"><span data-stu-id="3edea-135">System.String</span></span>

## <span data-ttu-id="3edea-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3edea-136">OUTPUTS</span></span>

### <span data-ttu-id="3edea-137">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="3edea-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="3edea-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3edea-138">NOTES</span></span>

## <span data-ttu-id="3edea-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3edea-139">RELATED LINKS</span></span>

[<span data-ttu-id="3edea-140">AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3edea-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3edea-141">AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="3edea-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="3edea-142">AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="3edea-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="3edea-143">新-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edea-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="3edea-144">移除-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edea-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="3edea-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edea-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


