---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133258"
---
# <span data-ttu-id="3e226-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3e226-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="3e226-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e226-102">SYNOPSIS</span></span>
<span data-ttu-id="3e226-103">移除 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e226-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="3e226-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e226-104">SYNTAX</span></span>

### <span data-ttu-id="3e226-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3e226-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e226-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e226-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e226-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e226-114">說明</span><span class="sxs-lookup"><span data-stu-id="3e226-114">DESCRIPTION</span></span>
<span data-ttu-id="3e226-115">移除 Azure 事件格線主題、資源、Azure 訂閱或資源群組的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e226-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="3e226-116">示例</span><span class="sxs-lookup"><span data-stu-id="3e226-116">EXAMPLES</span></span>

### <span data-ttu-id="3e226-117">範例1</span><span class="sxs-lookup"><span data-stu-id="3e226-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3e226-118">移除 [ \` \` \` 資源群組 MyResourceGroupName] 中 Topic1 Azure 事件格線主題的事件訂閱 EventSubscription1 \` \` \` 。</span><span class="sxs-lookup"><span data-stu-id="3e226-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3e226-119">範例2</span><span class="sxs-lookup"><span data-stu-id="3e226-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3e226-120">移除 \` \` 資源群組 MyResourceGroupName 的事件訂閱 EventSubscription1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="3e226-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3e226-121">範例3</span><span class="sxs-lookup"><span data-stu-id="3e226-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3e226-122">移除 \` 預設 Azure 訂閱 EventSubscription1 的事件訂閱 \` 。</span><span class="sxs-lookup"><span data-stu-id="3e226-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="3e226-123">範例4</span><span class="sxs-lookup"><span data-stu-id="3e226-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3e226-124">移除 \` \` 事件中心命名空間的事件訂閱 EventSubscription1。</span><span class="sxs-lookup"><span data-stu-id="3e226-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="3e226-125">範例5</span><span class="sxs-lookup"><span data-stu-id="3e226-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3e226-126">移除 \` \` 事件格線主題的事件訂閱 EventSubscription1。</span><span class="sxs-lookup"><span data-stu-id="3e226-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="3e226-127">參數</span><span class="sxs-lookup"><span data-stu-id="3e226-127">PARAMETERS</span></span>

### <span data-ttu-id="3e226-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e226-128">-DefaultProfile</span></span>
<span data-ttu-id="3e226-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3e226-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e226-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="3e226-130">-DomainInputObject</span></span>
<span data-ttu-id="3e226-131">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="3e226-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e226-132">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="3e226-132">-DomainName</span></span>
<span data-ttu-id="3e226-133">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="3e226-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e226-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="3e226-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="3e226-135">EventGrid [網域] 主題物件。</span><span class="sxs-lookup"><span data-stu-id="3e226-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e226-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="3e226-136">-DomainTopicName</span></span>
<span data-ttu-id="3e226-137">EventGrid [網域主題名稱]。</span><span class="sxs-lookup"><span data-stu-id="3e226-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e226-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3e226-138">-EventSubscriptionName</span></span>
<span data-ttu-id="3e226-139">需要移除之事件訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e226-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e226-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e226-140">-InputObject</span></span>
<span data-ttu-id="3e226-141">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="3e226-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="3e226-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e226-142">-PassThru</span></span>
<span data-ttu-id="3e226-143">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="3e226-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="3e226-144">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3e226-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e226-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e226-145">-ResourceGroupName</span></span>
<span data-ttu-id="3e226-146">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3e226-146">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e226-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e226-147">-ResourceId</span></span>
<span data-ttu-id="3e226-148">需要移除其事件訂閱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e226-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="3e226-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3e226-149">-TopicName</span></span>
<span data-ttu-id="3e226-150">事件格線主題名稱。</span><span class="sxs-lookup"><span data-stu-id="3e226-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="3e226-151">-確認</span><span class="sxs-lookup"><span data-stu-id="3e226-151">-Confirm</span></span>
<span data-ttu-id="3e226-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e226-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e226-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e226-153">-WhatIf</span></span>
<span data-ttu-id="3e226-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e226-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e226-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e226-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e226-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e226-156">CommonParameters</span></span>
<span data-ttu-id="3e226-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e226-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e226-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3e226-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e226-159">輸入</span><span class="sxs-lookup"><span data-stu-id="3e226-159">INPUTS</span></span>

### <span data-ttu-id="3e226-160">System.object</span><span class="sxs-lookup"><span data-stu-id="3e226-160">System.String</span></span>

### <span data-ttu-id="3e226-161">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="3e226-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="3e226-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="3e226-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="3e226-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3e226-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="3e226-164">輸出</span><span class="sxs-lookup"><span data-stu-id="3e226-164">OUTPUTS</span></span>

### <span data-ttu-id="3e226-165">System.object</span><span class="sxs-lookup"><span data-stu-id="3e226-165">System.Boolean</span></span>

## <span data-ttu-id="3e226-166">筆記</span><span class="sxs-lookup"><span data-stu-id="3e226-166">NOTES</span></span>

## <span data-ttu-id="3e226-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e226-167">RELATED LINKS</span></span>
