---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3960f73d115b881bdffab89c225a9321e19af067
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911958"
---
# <span data-ttu-id="982ea-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="982ea-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="982ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="982ea-102">SYNOPSIS</span></span>
<span data-ttu-id="982ea-103">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="982ea-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="982ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="982ea-104">SYNTAX</span></span>

### <span data-ttu-id="982ea-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="982ea-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982ea-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="982ea-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982ea-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="982ea-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982ea-108">描述</span><span class="sxs-lookup"><span data-stu-id="982ea-108">DESCRIPTION</span></span>
<span data-ttu-id="982ea-109">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="982ea-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="982ea-110">例子</span><span class="sxs-lookup"><span data-stu-id="982ea-110">EXAMPLES</span></span>

### <span data-ttu-id="982ea-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="982ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="982ea-112">移除資源群組 \` \` \` MyResourceGroupName 中的事件格線主題 \` 1。</span><span class="sxs-lookup"><span data-stu-id="982ea-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="982ea-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="982ea-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="982ea-114">移除資源群組 \` \` \` MyResourceGroupName 中的事件格線主題 \` 1。</span><span class="sxs-lookup"><span data-stu-id="982ea-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="982ea-115">參數</span><span class="sxs-lookup"><span data-stu-id="982ea-115">PARAMETERS</span></span>

### <span data-ttu-id="982ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982ea-116">-DefaultProfile</span></span>
<span data-ttu-id="982ea-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="982ea-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="982ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="982ea-118">-InputObject</span></span>
<span data-ttu-id="982ea-119">EventGrid Topic 物件。</span><span class="sxs-lookup"><span data-stu-id="982ea-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="982ea-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="982ea-120">-Name</span></span>
<span data-ttu-id="982ea-121">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="982ea-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="982ea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="982ea-122">-PassThru</span></span>
<span data-ttu-id="982ea-123">會返回移除作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="982ea-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="982ea-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="982ea-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="982ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="982ea-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="982ea-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="982ea-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="982ea-127">-ResourceId</span></span>
<span data-ttu-id="982ea-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="982ea-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="982ea-129">-確認</span><span class="sxs-lookup"><span data-stu-id="982ea-129">-Confirm</span></span>
<span data-ttu-id="982ea-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="982ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982ea-131">-WhatIf</span></span>
<span data-ttu-id="982ea-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="982ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982ea-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="982ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982ea-134">CommonParameters</span></span>
<span data-ttu-id="982ea-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="982ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982ea-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="982ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982ea-137">輸入</span><span class="sxs-lookup"><span data-stu-id="982ea-137">INPUTS</span></span>

### <span data-ttu-id="982ea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="982ea-138">System.String</span></span>

### <span data-ttu-id="982ea-139">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="982ea-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="982ea-140">輸出</span><span class="sxs-lookup"><span data-stu-id="982ea-140">OUTPUTS</span></span>

### <span data-ttu-id="982ea-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="982ea-141">System.Boolean</span></span>

## <span data-ttu-id="982ea-142">筆記</span><span class="sxs-lookup"><span data-stu-id="982ea-142">NOTES</span></span>

## <span data-ttu-id="982ea-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="982ea-143">RELATED LINKS</span></span>
