---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: b7932eb4f5d68986033243bc3e5e5161861a0bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901710"
---
# <span data-ttu-id="a440c-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a440c-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="a440c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a440c-102">SYNOPSIS</span></span>
<span data-ttu-id="a440c-103">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a440c-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="a440c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a440c-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a440c-105">描述</span><span class="sxs-lookup"><span data-stu-id="a440c-105">DESCRIPTION</span></span>
<span data-ttu-id="a440c-106">**Remove-AzNotificationHub** Cmdlet 會移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a440c-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="a440c-107">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="a440c-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="a440c-108">平臺包括但不限於：iOS、Android、Windows Phone 8 和 Windows Store。</span><span class="sxs-lookup"><span data-stu-id="a440c-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="a440c-109">通知中樞大致相當於個別的應用程式：每一個 App 通常會有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a440c-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="a440c-110">您可以使用 **Remove-AzNotificationHub** Cmdlet 移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a440c-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="a440c-111">移除中樞後，您無法再使用該中樞來傳送推入通知給使用者。</span><span class="sxs-lookup"><span data-stu-id="a440c-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="a440c-112">例子</span><span class="sxs-lookup"><span data-stu-id="a440c-112">EXAMPLES</span></span>

### <span data-ttu-id="a440c-113">範例 1：移除通知中樞</span><span class="sxs-lookup"><span data-stu-id="a440c-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="a440c-114">此命令會移除名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a440c-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="a440c-115">若要移除中樞，您必須指定中樞所在的命名空間，以及中樞指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a440c-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="a440c-116">參數</span><span class="sxs-lookup"><span data-stu-id="a440c-116">PARAMETERS</span></span>

### <span data-ttu-id="a440c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a440c-117">-DefaultProfile</span></span>
<span data-ttu-id="a440c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a440c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a440c-119">-強制</span><span class="sxs-lookup"><span data-stu-id="a440c-119">-Force</span></span>
<span data-ttu-id="a440c-120">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="a440c-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a440c-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a440c-121">-Namespace</span></span>
<span data-ttu-id="a440c-122">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="a440c-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a440c-123">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="a440c-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a440c-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a440c-124">-NotificationHub</span></span>
<span data-ttu-id="a440c-125">指定要移除的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a440c-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="a440c-126">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="a440c-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="a440c-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a440c-127">-ResourceGroup</span></span>
<span data-ttu-id="a440c-128">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a440c-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="a440c-129">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="a440c-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a440c-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a440c-130">-Confirm</span></span>
<span data-ttu-id="a440c-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a440c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a440c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a440c-132">-WhatIf</span></span>
<span data-ttu-id="a440c-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a440c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a440c-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a440c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a440c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a440c-135">CommonParameters</span></span>
<span data-ttu-id="a440c-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a440c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a440c-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a440c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a440c-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a440c-138">INPUTS</span></span>

### <span data-ttu-id="a440c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a440c-139">System.String</span></span>

## <span data-ttu-id="a440c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a440c-140">OUTPUTS</span></span>

### <span data-ttu-id="a440c-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="a440c-141">System.Void</span></span>

## <span data-ttu-id="a440c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a440c-142">NOTES</span></span>

## <span data-ttu-id="a440c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a440c-143">RELATED LINKS</span></span>

[<span data-ttu-id="a440c-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a440c-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="a440c-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a440c-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="a440c-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a440c-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


