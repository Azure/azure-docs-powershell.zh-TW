---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: a1e5a8b33ab9df4e48495d00b6a27e105088f4fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901706"
---
# <span data-ttu-id="90f7b-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90f7b-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="90f7b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="90f7b-103">移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="90f7b-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="90f7b-104">語法</span><span class="sxs-lookup"><span data-stu-id="90f7b-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f7b-105">描述</span><span class="sxs-lookup"><span data-stu-id="90f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="90f7b-106">**Remove-AzNotificationHubsNamespace** Cmdlet 會從您的部署移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="90f7b-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="90f7b-107">命名空間是邏輯容器，可協助組織及管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="90f7b-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="90f7b-108">**Remove-AzNotificationHubsNamespace** Cmdlet 會從您的部署移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="90f7b-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="90f7b-109">當您執行此 Cmdlet 時，指定的命名空間會連同與該命名空間相關聯的所有通知中樞一併刪除。</span><span class="sxs-lookup"><span data-stu-id="90f7b-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="90f7b-110">例子</span><span class="sxs-lookup"><span data-stu-id="90f7b-110">EXAMPLES</span></span>

### <span data-ttu-id="90f7b-111">範例 1：移除通知中樞命名空間</span><span class="sxs-lookup"><span data-stu-id="90f7b-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="90f7b-112">此命令會移除名為 ContosoNamespace 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="90f7b-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="90f7b-113">您必須指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="90f7b-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="90f7b-114">參數</span><span class="sxs-lookup"><span data-stu-id="90f7b-114">PARAMETERS</span></span>

### <span data-ttu-id="90f7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f7b-115">-DefaultProfile</span></span>
<span data-ttu-id="90f7b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="90f7b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90f7b-117">-強制</span><span class="sxs-lookup"><span data-stu-id="90f7b-117">-Force</span></span>
<span data-ttu-id="90f7b-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="90f7b-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="90f7b-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="90f7b-119">-Namespace</span></span>
<span data-ttu-id="90f7b-120">指定此 Cmdlet 移除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="90f7b-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="90f7b-121">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="90f7b-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="90f7b-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90f7b-122">-ResourceGroup</span></span>
<span data-ttu-id="90f7b-123">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="90f7b-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="90f7b-124">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="90f7b-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="90f7b-125">-確認</span><span class="sxs-lookup"><span data-stu-id="90f7b-125">-Confirm</span></span>
<span data-ttu-id="90f7b-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90f7b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f7b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f7b-127">-WhatIf</span></span>
<span data-ttu-id="90f7b-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90f7b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90f7b-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90f7b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f7b-130">CommonParameters</span></span>
<span data-ttu-id="90f7b-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90f7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f7b-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="90f7b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f7b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="90f7b-133">INPUTS</span></span>

### <span data-ttu-id="90f7b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="90f7b-134">System.String</span></span>

## <span data-ttu-id="90f7b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="90f7b-135">OUTPUTS</span></span>

### <span data-ttu-id="90f7b-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="90f7b-136">System.Void</span></span>

## <span data-ttu-id="90f7b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="90f7b-137">NOTES</span></span>

## <span data-ttu-id="90f7b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="90f7b-138">RELATED LINKS</span></span>

[<span data-ttu-id="90f7b-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90f7b-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="90f7b-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90f7b-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="90f7b-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90f7b-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


