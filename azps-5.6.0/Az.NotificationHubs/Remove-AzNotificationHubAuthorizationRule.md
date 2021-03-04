---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: afbe8f904a8a1dad2d39a38817959e4ed4b5bad4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901709"
---
# <span data-ttu-id="e0a51-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0a51-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="e0a51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a51-103">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="e0a51-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="e0a51-104">語法</span><span class="sxs-lookup"><span data-stu-id="e0a51-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0a51-105">描述</span><span class="sxs-lookup"><span data-stu-id="e0a51-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a51-106">**Remove-AzNotificationHubAuthorizationRule** Cmdlet 會從通知 (SAS) 授權規則移除共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="e0a51-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="e0a51-107">授權規則會依據不同的許可權等級，透過建立連結作為 URI 來管理通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="e0a51-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="e0a51-108">許可權等級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="e0a51-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="e0a51-109">聽</span><span class="sxs-lookup"><span data-stu-id="e0a51-109">Listen</span></span>
- <span data-ttu-id="e0a51-110">發送</span><span class="sxs-lookup"><span data-stu-id="e0a51-110">Send</span></span>
- <span data-ttu-id="e0a51-111">管理用戶端會依據適當的許可權等級，導向至其中一個 URI。</span><span class="sxs-lookup"><span data-stu-id="e0a51-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="e0a51-112">例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="e0a51-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="e0a51-113">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="e0a51-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="e0a51-114">例子</span><span class="sxs-lookup"><span data-stu-id="e0a51-114">EXAMPLES</span></span>

### <span data-ttu-id="e0a51-115">範例 1：從通知中樞移除授權規則</span><span class="sxs-lookup"><span data-stu-id="e0a51-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="e0a51-116">此命令會從名為 ContosoExternalHub 的通知中樞移除名為 ListenRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="e0a51-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="e0a51-117">當您執行此命令時，您必須同時指定中樞指派的命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="e0a51-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="e0a51-118">參數</span><span class="sxs-lookup"><span data-stu-id="e0a51-118">PARAMETERS</span></span>

### <span data-ttu-id="e0a51-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0a51-119">-AuthorizationRule</span></span>
<span data-ttu-id="e0a51-120">指定此 Cmdlet 移除的 SAS 驗證規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e0a51-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a51-121">-DefaultProfile</span></span>
<span data-ttu-id="e0a51-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e0a51-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0a51-123">-強制</span><span class="sxs-lookup"><span data-stu-id="e0a51-123">-Force</span></span>
<span data-ttu-id="e0a51-124">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="e0a51-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e0a51-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e0a51-125">-Namespace</span></span>
<span data-ttu-id="e0a51-126">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e0a51-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="e0a51-127">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="e0a51-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e0a51-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e0a51-128">-NotificationHub</span></span>
<span data-ttu-id="e0a51-129">指定指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e0a51-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="e0a51-130">通知中樞可用來傳送推入通知給多個用戶端，無論平臺如何。</span><span class="sxs-lookup"><span data-stu-id="e0a51-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="e0a51-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0a51-131">-ResourceGroup</span></span>
<span data-ttu-id="e0a51-132">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e0a51-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="e0a51-133">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="e0a51-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e0a51-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e0a51-134">-Confirm</span></span>
<span data-ttu-id="e0a51-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e0a51-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0a51-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a51-136">-WhatIf</span></span>
<span data-ttu-id="e0a51-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0a51-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0a51-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0a51-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0a51-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a51-139">CommonParameters</span></span>
<span data-ttu-id="e0a51-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e0a51-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a51-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e0a51-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a51-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e0a51-142">INPUTS</span></span>

### <span data-ttu-id="e0a51-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e0a51-143">System.String</span></span>

## <span data-ttu-id="e0a51-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e0a51-144">OUTPUTS</span></span>

### <span data-ttu-id="e0a51-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="e0a51-145">System.Void</span></span>

## <span data-ttu-id="e0a51-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e0a51-146">NOTES</span></span>

## <span data-ttu-id="e0a51-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0a51-147">RELATED LINKS</span></span>

[<span data-ttu-id="e0a51-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0a51-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e0a51-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0a51-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e0a51-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0a51-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


