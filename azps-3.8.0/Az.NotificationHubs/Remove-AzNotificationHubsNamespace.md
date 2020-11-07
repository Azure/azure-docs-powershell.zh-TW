---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958713"
---
# <span data-ttu-id="b2d28-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b2d28-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="b2d28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2d28-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d28-103">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2d28-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="b2d28-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2d28-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d28-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2d28-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d28-106">**AzNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2d28-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="b2d28-107">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="b2d28-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="b2d28-108">**AzNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2d28-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="b2d28-109">當您執行此 Cmdlet 時，會刪除指定的命名空間，以及與該命名空間關聯的所有通知中樞。</span><span class="sxs-lookup"><span data-stu-id="b2d28-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="b2d28-110">示例</span><span class="sxs-lookup"><span data-stu-id="b2d28-110">EXAMPLES</span></span>

### <span data-ttu-id="b2d28-111">範例1：移除通知中心命名空間</span><span class="sxs-lookup"><span data-stu-id="b2d28-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="b2d28-112">這個命令會移除名為 ContosoNamespace 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2d28-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="b2d28-113">您必須指定命名空間的指派資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2d28-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="b2d28-114">參數</span><span class="sxs-lookup"><span data-stu-id="b2d28-114">PARAMETERS</span></span>

### <span data-ttu-id="b2d28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d28-115">-DefaultProfile</span></span>
<span data-ttu-id="b2d28-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b2d28-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2d28-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b2d28-117">-Force</span></span>
<span data-ttu-id="b2d28-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b2d28-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b2d28-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b2d28-119">-Namespace</span></span>
<span data-ttu-id="b2d28-120">指定此 Cmdlet 移除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2d28-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="b2d28-121">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="b2d28-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b2d28-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2d28-122">-ResourceGroup</span></span>
<span data-ttu-id="b2d28-123">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2d28-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b2d28-124">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="b2d28-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b2d28-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b2d28-125">-Confirm</span></span>
<span data-ttu-id="b2d28-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2d28-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d28-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d28-127">-WhatIf</span></span>
<span data-ttu-id="b2d28-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2d28-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2d28-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2d28-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d28-130">CommonParameters</span></span>
<span data-ttu-id="b2d28-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2d28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d28-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2d28-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d28-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b2d28-133">INPUTS</span></span>

### <span data-ttu-id="b2d28-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b2d28-134">System.String</span></span>

## <span data-ttu-id="b2d28-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b2d28-135">OUTPUTS</span></span>

### <span data-ttu-id="b2d28-136">System.void</span><span class="sxs-lookup"><span data-stu-id="b2d28-136">System.Void</span></span>

## <span data-ttu-id="b2d28-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b2d28-137">NOTES</span></span>

## <span data-ttu-id="b2d28-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2d28-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2d28-139">AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b2d28-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b2d28-140">新-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b2d28-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b2d28-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b2d28-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


