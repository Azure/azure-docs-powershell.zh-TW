---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: fd872830f82f1d75f0b3c5f60ba6b129d7edd6f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622312"
---
# <span data-ttu-id="ce055-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ce055-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="ce055-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce055-102">SYNOPSIS</span></span>
<span data-ttu-id="ce055-103">移除 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce055-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="ce055-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce055-104">SYNTAX</span></span>

### <span data-ttu-id="ce055-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ce055-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce055-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce055-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce055-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce055-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce055-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce055-108">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce055-109">說明</span><span class="sxs-lookup"><span data-stu-id="ce055-109">DESCRIPTION</span></span>
<span data-ttu-id="ce055-110">移除 Azure 事件格線主題、資源、Azure 訂閱或資源群組的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce055-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="ce055-111">示例</span><span class="sxs-lookup"><span data-stu-id="ce055-111">EXAMPLES</span></span>

### <span data-ttu-id="ce055-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ce055-112">Example 1</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ce055-113">移除 [ \` \` \` 資源群組 MyResourceGroupName] 中 Topic1 Azure 事件格線主題的事件訂閱 EventSubscription1 \` \` \` 。</span><span class="sxs-lookup"><span data-stu-id="ce055-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ce055-114">範例2</span><span class="sxs-lookup"><span data-stu-id="ce055-114">Example 2</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ce055-115">移除 \` \` 資源群組 MyResourceGroupName 的事件訂閱 EventSubscription1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="ce055-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ce055-116">範例3</span><span class="sxs-lookup"><span data-stu-id="ce055-116">Example 3</span></span>
```
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ce055-117">移除 \` 預設 Azure 訂閱 EventSubscription1 的事件訂閱 \` 。</span><span class="sxs-lookup"><span data-stu-id="ce055-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="ce055-118">範例4</span><span class="sxs-lookup"><span data-stu-id="ce055-118">Example 4</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ce055-119">移除 \` \` 事件中心命名空間的事件訂閱 EventSubscription1。</span><span class="sxs-lookup"><span data-stu-id="ce055-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="ce055-120">範例5</span><span class="sxs-lookup"><span data-stu-id="ce055-120">Example 5</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ce055-121">移除 \` \` 事件格線主題的事件訂閱 EventSubscription1。</span><span class="sxs-lookup"><span data-stu-id="ce055-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="ce055-122">參數</span><span class="sxs-lookup"><span data-stu-id="ce055-122">PARAMETERS</span></span>

### <span data-ttu-id="ce055-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce055-123">-DefaultProfile</span></span>
<span data-ttu-id="ce055-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce055-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce055-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ce055-125">-EventSubscriptionName</span></span>
<span data-ttu-id="ce055-126">需要移除之事件訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce055-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce055-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce055-127">-InputObject</span></span>
<span data-ttu-id="ce055-128">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="ce055-128">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce055-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce055-129">-PassThru</span></span>
<span data-ttu-id="ce055-130">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="ce055-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ce055-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ce055-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce055-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce055-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce055-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ce055-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce055-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce055-134">-ResourceId</span></span>
<span data-ttu-id="ce055-135">需要移除其事件訂閱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce055-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce055-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ce055-136">-TopicName</span></span>
<span data-ttu-id="ce055-137">事件格線主題名稱。</span><span class="sxs-lookup"><span data-stu-id="ce055-137">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce055-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ce055-138">-Confirm</span></span>
<span data-ttu-id="ce055-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce055-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce055-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce055-140">-WhatIf</span></span>
<span data-ttu-id="ce055-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce055-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce055-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce055-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce055-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce055-143">CommonParameters</span></span>
<span data-ttu-id="ce055-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce055-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce055-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce055-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce055-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ce055-146">INPUTS</span></span>

### <span data-ttu-id="ce055-147">System.object</span><span class="sxs-lookup"><span data-stu-id="ce055-147">System.String</span></span>

### <span data-ttu-id="ce055-148">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="ce055-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ce055-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ce055-149">OUTPUTS</span></span>

### <span data-ttu-id="ce055-150">System.object</span><span class="sxs-lookup"><span data-stu-id="ce055-150">System.Boolean</span></span>

## <span data-ttu-id="ce055-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ce055-151">NOTES</span></span>

## <span data-ttu-id="ce055-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce055-152">RELATED LINKS</span></span>
