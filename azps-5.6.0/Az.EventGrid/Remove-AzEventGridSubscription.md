---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 1625e3325164156b1809640c54d4b75698ae7363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911965"
---
# <span data-ttu-id="a6bfa-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6bfa-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="a6bfa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bfa-103">移除 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="a6bfa-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6bfa-104">SYNTAX</span></span>

### <span data-ttu-id="a6bfa-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a6bfa-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bfa-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bfa-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6bfa-114">描述</span><span class="sxs-lookup"><span data-stu-id="a6bfa-114">DESCRIPTION</span></span>
<span data-ttu-id="a6bfa-115">移除 Azure 事件格線主題、資源、Azure 訂閱或資源群組的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="a6bfa-116">例子</span><span class="sxs-lookup"><span data-stu-id="a6bfa-116">EXAMPLES</span></span>

### <span data-ttu-id="a6bfa-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="a6bfa-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a6bfa-118">將事件訂閱 \` EventSubscription1 移除 \` 至資源群組 \` \` \` MyResourceGroupName 中的 Azure 事件格線主題 \` Topic1。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a6bfa-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="a6bfa-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a6bfa-120">將事件訂閱 \` EventSubscription1 移除 \` 至資源群組 \` MyResourceGroupName。 \`</span><span class="sxs-lookup"><span data-stu-id="a6bfa-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a6bfa-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="a6bfa-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a6bfa-122">將事件訂閱 \` EventSubscription1 \` 移除至預設的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="a6bfa-123">範例 4</span><span class="sxs-lookup"><span data-stu-id="a6bfa-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a6bfa-124">將事件訂閱 \` EventSubscription1 \` 移除至事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="a6bfa-125">範例 5</span><span class="sxs-lookup"><span data-stu-id="a6bfa-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a6bfa-126">將事件訂閱 \` EventSubscription1 \` 移除至事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="a6bfa-127">參數</span><span class="sxs-lookup"><span data-stu-id="a6bfa-127">PARAMETERS</span></span>

### <span data-ttu-id="a6bfa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bfa-128">-DefaultProfile</span></span>
<span data-ttu-id="a6bfa-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a6bfa-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6bfa-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a6bfa-130">-DomainInputObject</span></span>
<span data-ttu-id="a6bfa-131">EventGrid 網域物件。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a6bfa-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a6bfa-132">-DomainName</span></span>
<span data-ttu-id="a6bfa-133">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="a6bfa-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a6bfa-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="a6bfa-135">EventGrid 網域主題物件。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="a6bfa-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a6bfa-136">-DomainTopicName</span></span>
<span data-ttu-id="a6bfa-137">EventGrid 網域主題名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="a6bfa-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a6bfa-138">-EventSubscriptionName</span></span>
<span data-ttu-id="a6bfa-139">需要移除的活動訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="a6bfa-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6bfa-140">-InputObject</span></span>
<span data-ttu-id="a6bfa-141">EventGrid Topic 物件。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a6bfa-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bfa-142">-PassThru</span></span>
<span data-ttu-id="a6bfa-143">會返回移除作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a6bfa-144">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a6bfa-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bfa-145">-ResourceGroupName</span></span>
<span data-ttu-id="a6bfa-146">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6bfa-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6bfa-147">-ResourceId</span></span>
<span data-ttu-id="a6bfa-148">需要移除其事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="a6bfa-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a6bfa-149">-TopicName</span></span>
<span data-ttu-id="a6bfa-150">事件格線主題名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="a6bfa-151">-確認</span><span class="sxs-lookup"><span data-stu-id="a6bfa-151">-Confirm</span></span>
<span data-ttu-id="a6bfa-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bfa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bfa-153">-WhatIf</span></span>
<span data-ttu-id="a6bfa-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bfa-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bfa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bfa-156">CommonParameters</span></span>
<span data-ttu-id="a6bfa-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6bfa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bfa-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6bfa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bfa-159">輸入</span><span class="sxs-lookup"><span data-stu-id="a6bfa-159">INPUTS</span></span>

### <span data-ttu-id="a6bfa-160">System.String</span><span class="sxs-lookup"><span data-stu-id="a6bfa-160">System.String</span></span>

### <span data-ttu-id="a6bfa-161">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="a6bfa-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a6bfa-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a6bfa-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a6bfa-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a6bfa-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="a6bfa-164">輸出</span><span class="sxs-lookup"><span data-stu-id="a6bfa-164">OUTPUTS</span></span>

### <span data-ttu-id="a6bfa-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6bfa-165">System.Boolean</span></span>

## <span data-ttu-id="a6bfa-166">筆記</span><span class="sxs-lookup"><span data-stu-id="a6bfa-166">NOTES</span></span>

## <span data-ttu-id="a6bfa-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6bfa-167">RELATED LINKS</span></span>
