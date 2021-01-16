---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278761"
---
# <span data-ttu-id="a259c-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a259c-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="a259c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a259c-102">SYNOPSIS</span></span>
<span data-ttu-id="a259c-103">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="a259c-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a259c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a259c-104">SYNTAX</span></span>

### <span data-ttu-id="a259c-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a259c-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a259c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a259c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a259c-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a259c-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a259c-108">說明</span><span class="sxs-lookup"><span data-stu-id="a259c-108">DESCRIPTION</span></span>
<span data-ttu-id="a259c-109">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="a259c-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a259c-110">示例</span><span class="sxs-lookup"><span data-stu-id="a259c-110">EXAMPLES</span></span>

### <span data-ttu-id="a259c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a259c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="a259c-112">移除 [ \` \` 資源] 群組 MyResourceGroupName 中的事件格線主題 Topic1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="a259c-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a259c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a259c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="a259c-114">移除 [ \` \` 資源] 群組 MyResourceGroupName 中的事件格線主題 Topic1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="a259c-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a259c-115">參數</span><span class="sxs-lookup"><span data-stu-id="a259c-115">PARAMETERS</span></span>

### <span data-ttu-id="a259c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a259c-116">-DefaultProfile</span></span>
<span data-ttu-id="a259c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a259c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a259c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a259c-118">-InputObject</span></span>
<span data-ttu-id="a259c-119">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="a259c-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a259c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a259c-120">-Name</span></span>
<span data-ttu-id="a259c-121">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="a259c-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a259c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a259c-122">-PassThru</span></span>
<span data-ttu-id="a259c-123">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="a259c-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a259c-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a259c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a259c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a259c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a259c-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a259c-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="a259c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a259c-127">-ResourceId</span></span>
<span data-ttu-id="a259c-128">EventGrid 主題 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="a259c-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="a259c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a259c-129">-Confirm</span></span>
<span data-ttu-id="a259c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a259c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a259c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a259c-131">-WhatIf</span></span>
<span data-ttu-id="a259c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a259c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a259c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a259c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a259c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a259c-134">CommonParameters</span></span>
<span data-ttu-id="a259c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a259c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a259c-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a259c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a259c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a259c-137">INPUTS</span></span>

### <span data-ttu-id="a259c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a259c-138">System.String</span></span>

### <span data-ttu-id="a259c-139">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="a259c-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a259c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a259c-140">OUTPUTS</span></span>

### <span data-ttu-id="a259c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a259c-141">System.Boolean</span></span>

## <span data-ttu-id="a259c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a259c-142">NOTES</span></span>

## <span data-ttu-id="a259c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a259c-143">RELATED LINKS</span></span>
