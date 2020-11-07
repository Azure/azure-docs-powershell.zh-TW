---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958718"
---
# <span data-ttu-id="96a85-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="96a85-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="96a85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96a85-102">SYNOPSIS</span></span>
<span data-ttu-id="96a85-103">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="96a85-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="96a85-104">句法</span><span class="sxs-lookup"><span data-stu-id="96a85-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a85-105">說明</span><span class="sxs-lookup"><span data-stu-id="96a85-105">DESCRIPTION</span></span>
<span data-ttu-id="96a85-106">**AzNotificationHub** Cmdlet 會移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="96a85-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="96a85-107">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="96a85-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="96a85-108">平臺包括但不限於： iOS、Android、Windows Phone 8 和 Windows 市集中。</span><span class="sxs-lookup"><span data-stu-id="96a85-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="96a85-109">通知中樞大致相當於個別的應用程式：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="96a85-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="96a85-110">您可以使用 **AzNotificationHub** Cmdlet 來移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="96a85-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="96a85-111">在已移除中樞之後，您將無法再使用該中樞傳送推播通知給使用者。</span><span class="sxs-lookup"><span data-stu-id="96a85-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="96a85-112">示例</span><span class="sxs-lookup"><span data-stu-id="96a85-112">EXAMPLES</span></span>

### <span data-ttu-id="96a85-113">範例1：移除通知中樞</span><span class="sxs-lookup"><span data-stu-id="96a85-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="96a85-114">這個命令會移除名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="96a85-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="96a85-115">若要移除中樞，您必須指定中樞所在的命名空間，以及該中樞所指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="96a85-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="96a85-116">參數</span><span class="sxs-lookup"><span data-stu-id="96a85-116">PARAMETERS</span></span>

### <span data-ttu-id="96a85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a85-117">-DefaultProfile</span></span>
<span data-ttu-id="96a85-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="96a85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96a85-119">-Force</span><span class="sxs-lookup"><span data-stu-id="96a85-119">-Force</span></span>
<span data-ttu-id="96a85-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="96a85-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="96a85-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="96a85-121">-Namespace</span></span>
<span data-ttu-id="96a85-122">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="96a85-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="96a85-123">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="96a85-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="96a85-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="96a85-124">-NotificationHub</span></span>
<span data-ttu-id="96a85-125">指定要移除的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="96a85-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="96a85-126">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="96a85-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="96a85-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96a85-127">-ResourceGroup</span></span>
<span data-ttu-id="96a85-128">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="96a85-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="96a85-129">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="96a85-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="96a85-130">-確認</span><span class="sxs-lookup"><span data-stu-id="96a85-130">-Confirm</span></span>
<span data-ttu-id="96a85-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96a85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a85-132">-WhatIf</span></span>
<span data-ttu-id="96a85-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96a85-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96a85-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96a85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a85-135">CommonParameters</span></span>
<span data-ttu-id="96a85-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96a85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a85-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96a85-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a85-138">輸入</span><span class="sxs-lookup"><span data-stu-id="96a85-138">INPUTS</span></span>

### <span data-ttu-id="96a85-139">System.object</span><span class="sxs-lookup"><span data-stu-id="96a85-139">System.String</span></span>

## <span data-ttu-id="96a85-140">輸出</span><span class="sxs-lookup"><span data-stu-id="96a85-140">OUTPUTS</span></span>

### <span data-ttu-id="96a85-141">System.void</span><span class="sxs-lookup"><span data-stu-id="96a85-141">System.Void</span></span>

## <span data-ttu-id="96a85-142">筆記</span><span class="sxs-lookup"><span data-stu-id="96a85-142">NOTES</span></span>

## <span data-ttu-id="96a85-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="96a85-143">RELATED LINKS</span></span>

[<span data-ttu-id="96a85-144">AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="96a85-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="96a85-145">新-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="96a85-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="96a85-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="96a85-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


