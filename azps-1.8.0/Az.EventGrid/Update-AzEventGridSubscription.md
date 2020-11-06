---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622308"
---
# <span data-ttu-id="251c8-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="251c8-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="251c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="251c8-102">SYNOPSIS</span></span>
<span data-ttu-id="251c8-103">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="251c8-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="251c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="251c8-104">SYNTAX</span></span>

### <span data-ttu-id="251c8-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="251c8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="251c8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="251c8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="251c8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="251c8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="251c8-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="251c8-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="251c8-109">說明</span><span class="sxs-lookup"><span data-stu-id="251c8-109">DESCRIPTION</span></span>
<span data-ttu-id="251c8-110">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="251c8-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="251c8-111">這可以用來更新現有事件訂閱的篩選、目的地或標籤。</span><span class="sxs-lookup"><span data-stu-id="251c8-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="251c8-112">示例</span><span class="sxs-lookup"><span data-stu-id="251c8-112">EXAMPLES</span></span>

### <span data-ttu-id="251c8-113">範例1</span><span class="sxs-lookup"><span data-stu-id="251c8-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="251c8-114">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="251c8-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="251c8-115">範例2</span><span class="sxs-lookup"><span data-stu-id="251c8-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="251c8-116">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="251c8-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="251c8-117">範例3</span><span class="sxs-lookup"><span data-stu-id="251c8-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="251c8-118">更新 EventHub namespace ContosoNamespace 的事件訂閱 \` ES1 的屬性，並將新的 [端點為] 與 \` \` https://requestb.in/1kxxoui1\ 新的 SubjectEndsWith 篩選為 \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="251c8-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="251c8-119">範例4</span><span class="sxs-lookup"><span data-stu-id="251c8-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="251c8-120">更新資源群組 MyResourceGroupName 的事件訂閱 ES1 的屬性， \` \` 新 \` 的 \` 標籤會 $labels。</span><span class="sxs-lookup"><span data-stu-id="251c8-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="251c8-121">參數</span><span class="sxs-lookup"><span data-stu-id="251c8-121">PARAMETERS</span></span>

### <span data-ttu-id="251c8-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="251c8-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="251c8-123">用來儲存未傳遞事件的端點。</span><span class="sxs-lookup"><span data-stu-id="251c8-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="251c8-124">指定 [儲存 blob] 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="251c8-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="251c8-125">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[[容器]]。</span><span class="sxs-lookup"><span data-stu-id="251c8-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251c8-126">-DefaultProfile</span></span>
<span data-ttu-id="251c8-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="251c8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="251c8-128">-端點</span><span class="sxs-lookup"><span data-stu-id="251c8-128">-Endpoint</span></span>
<span data-ttu-id="251c8-129">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="251c8-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="251c8-130">這可以是 webhook URL，或 EventHub、storage queue 或 hybridconnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="251c8-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="251c8-131">例如，混合式連接的資源識別碼會採用下列形式：/subscriptions/[Azure 訂閱 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="251c8-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="251c8-132">在執行任何事件格線 Cmdlet 前，預期要建立目的地端點，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="251c8-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="251c8-133">-EndpointType</span></span>
<span data-ttu-id="251c8-134">端點類型。</span><span class="sxs-lookup"><span data-stu-id="251c8-134">Endpoint Type.</span></span>
<span data-ttu-id="251c8-135">此可以是 webhook、eventhub、storagequeue 或 hybridconnection。</span><span class="sxs-lookup"><span data-stu-id="251c8-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="251c8-136">預設值為 webhook。</span><span class="sxs-lookup"><span data-stu-id="251c8-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="251c8-137">-EventSubscriptionName</span></span>
<span data-ttu-id="251c8-138">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="251c8-138">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="251c8-139">-EventTtl</span></span>
<span data-ttu-id="251c8-140">事件傳送的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="251c8-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="251c8-141">此值必須介於1與1440之間</span><span class="sxs-lookup"><span data-stu-id="251c8-141">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="251c8-142">-IncludedEventType</span></span>
<span data-ttu-id="251c8-143">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="251c8-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="251c8-144">-InputObject</span></span>
<span data-ttu-id="251c8-145">EventGridSubscription 物件。</span><span class="sxs-lookup"><span data-stu-id="251c8-145">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-146">-標籤</span><span class="sxs-lookup"><span data-stu-id="251c8-146">-Label</span></span>
<span data-ttu-id="251c8-147">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="251c8-147">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="251c8-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="251c8-149">嘗試傳遞事件的次數上限。</span><span class="sxs-lookup"><span data-stu-id="251c8-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="251c8-150">此值必須介於1和30之間</span><span class="sxs-lookup"><span data-stu-id="251c8-150">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251c8-151">-ResourceGroupName</span></span>
<span data-ttu-id="251c8-152">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="251c8-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="251c8-153">-ResourceId</span></span>
<span data-ttu-id="251c8-154">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="251c8-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="251c8-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="251c8-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="251c8-156">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="251c8-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="251c8-157">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="251c8-157">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="251c8-158">-SubjectEndsWith</span></span>
<span data-ttu-id="251c8-159">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="251c8-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="251c8-160">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="251c8-160">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-161">-TopicName</span><span class="sxs-lookup"><span data-stu-id="251c8-161">-TopicName</span></span>
<span data-ttu-id="251c8-162">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="251c8-162">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="251c8-163">-確認</span><span class="sxs-lookup"><span data-stu-id="251c8-163">-Confirm</span></span>
<span data-ttu-id="251c8-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="251c8-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="251c8-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="251c8-165">-WhatIf</span></span>
<span data-ttu-id="251c8-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="251c8-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="251c8-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="251c8-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="251c8-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251c8-168">CommonParameters</span></span>
<span data-ttu-id="251c8-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="251c8-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251c8-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="251c8-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251c8-171">輸入</span><span class="sxs-lookup"><span data-stu-id="251c8-171">INPUTS</span></span>

### <span data-ttu-id="251c8-172">System.object</span><span class="sxs-lookup"><span data-stu-id="251c8-172">System.String</span></span>

### <span data-ttu-id="251c8-173">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="251c8-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="251c8-174">輸出</span><span class="sxs-lookup"><span data-stu-id="251c8-174">OUTPUTS</span></span>

### <span data-ttu-id="251c8-175">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="251c8-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="251c8-176">筆記</span><span class="sxs-lookup"><span data-stu-id="251c8-176">NOTES</span></span>

## <span data-ttu-id="251c8-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="251c8-177">RELATED LINKS</span></span>
