---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: f4dc14fd922852fa67085588c78847623eb5eb64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448994"
---
# <span data-ttu-id="d1d22-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d1d22-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="d1d22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1d22-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d22-103">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d1d22-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1d22-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1d22-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d22-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1d22-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d22-106">**AzureRmNotificationHub** Cmdlet 會移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d1d22-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="d1d22-107">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="d1d22-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="d1d22-108">平臺包括但不限於： iOS、Android、Windows Phone 8 和 Windows 市集中。</span><span class="sxs-lookup"><span data-stu-id="d1d22-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="d1d22-109">通知中樞大致相當於個別的應用程式：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d1d22-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="d1d22-110">您可以使用 **AzureRmNotificationHub** Cmdlet 來移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d1d22-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="d1d22-111">在已移除中樞之後，您將無法再使用該中樞傳送推播通知給使用者。</span><span class="sxs-lookup"><span data-stu-id="d1d22-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="d1d22-112">示例</span><span class="sxs-lookup"><span data-stu-id="d1d22-112">EXAMPLES</span></span>

### <span data-ttu-id="d1d22-113">範例1：移除通知中樞</span><span class="sxs-lookup"><span data-stu-id="d1d22-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="d1d22-114">這個命令會移除名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d1d22-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="d1d22-115">若要移除中樞，您必須指定中樞所在的命名空間，以及該中樞所指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d1d22-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="d1d22-116">參數</span><span class="sxs-lookup"><span data-stu-id="d1d22-116">PARAMETERS</span></span>

### <span data-ttu-id="d1d22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d22-117">-DefaultProfile</span></span>
<span data-ttu-id="d1d22-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d1d22-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1d22-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d1d22-119">-Force</span></span>
<span data-ttu-id="d1d22-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d1d22-120">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d22-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d1d22-121">-Namespace</span></span>
<span data-ttu-id="d1d22-122">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="d1d22-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d1d22-123">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="d1d22-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d1d22-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d1d22-124">-NotificationHub</span></span>
<span data-ttu-id="d1d22-125">指定要移除的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="d1d22-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="d1d22-126">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="d1d22-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d22-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d1d22-127">-ResourceGroup</span></span>
<span data-ttu-id="d1d22-128">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="d1d22-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="d1d22-129">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="d1d22-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d1d22-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d1d22-130">-Confirm</span></span>
<span data-ttu-id="d1d22-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1d22-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d22-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d22-132">-WhatIf</span></span>
<span data-ttu-id="d1d22-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1d22-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1d22-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1d22-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d22-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d22-135">CommonParameters</span></span>
<span data-ttu-id="d1d22-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1d22-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d22-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1d22-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d22-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d1d22-138">INPUTS</span></span>

### <span data-ttu-id="d1d22-139">System.object</span><span class="sxs-lookup"><span data-stu-id="d1d22-139">System.String</span></span>

## <span data-ttu-id="d1d22-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d1d22-140">OUTPUTS</span></span>

### <span data-ttu-id="d1d22-141">System.void</span><span class="sxs-lookup"><span data-stu-id="d1d22-141">System.Void</span></span>

## <span data-ttu-id="d1d22-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d1d22-142">NOTES</span></span>

## <span data-ttu-id="d1d22-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1d22-143">RELATED LINKS</span></span>

[<span data-ttu-id="d1d22-144">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d1d22-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="d1d22-145">新-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d1d22-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="d1d22-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d1d22-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


