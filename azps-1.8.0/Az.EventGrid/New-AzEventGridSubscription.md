---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395181"
---
# <span data-ttu-id="1822a-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1822a-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="1822a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1822a-102">SYNOPSIS</span></span>
<span data-ttu-id="1822a-103">針對主題、Azure 資源、Azure 訂閱或資源群組建立新的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="1822a-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="1822a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1822a-104">SYNTAX</span></span>

### <span data-ttu-id="1822a-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1822a-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1822a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1822a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1822a-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1822a-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1822a-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1822a-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1822a-109">說明</span><span class="sxs-lookup"><span data-stu-id="1822a-109">DESCRIPTION</span></span>
<span data-ttu-id="1822a-110">建立 Azure 事件格線主題（支援的 Azure 資源、Azure 訂閱或資源群組）的新事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="1822a-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="1822a-111">若要建立目前所選 Azure 訂閱的事件訂閱，請指定事件訂閱名稱和目標端點。</span><span class="sxs-lookup"><span data-stu-id="1822a-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="1822a-112">若要建立資源群組的事件訂閱，除了事件訂閱名稱和目的地端點之外，還可以指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1822a-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="1822a-113">若要建立 Azure 事件格線主題的事件訂閱，請同時指定主題名稱。</span><span class="sxs-lookup"><span data-stu-id="1822a-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="1822a-114">若要建立支援的 Azure 資源的事件訂閱，請指定資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1822a-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="1822a-115">若要查看受支援類型的清單，請執行 Get-AzEventGridTopicType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1822a-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="1822a-116">示例</span><span class="sxs-lookup"><span data-stu-id="1822a-116">EXAMPLES</span></span>

### <span data-ttu-id="1822a-117">範例1</span><span class="sxs-lookup"><span data-stu-id="1822a-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1822a-118">\` \` \` \` \` \` 使用 webhook 目的地端點在資源群組 MyResourceGroupName 中 Topic1 Azure 事件格線主題建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="1822a-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="1822a-119">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="1822a-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="1822a-120">範例2</span><span class="sxs-lookup"><span data-stu-id="1822a-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1822a-121">\` \` \` \` 使用 webhook 目的地端點的資源群組 MyResourceGroupName 建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="1822a-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="1822a-122">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="1822a-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="1822a-123">範例3</span><span class="sxs-lookup"><span data-stu-id="1822a-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1822a-124">\` \` 使用 webhook 目的地端點，為目前選取的 Azure 訂閱建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="1822a-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="1822a-125">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="1822a-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="1822a-126">範例4</span><span class="sxs-lookup"><span data-stu-id="1822a-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="1822a-127">\` \` 使用 webhook 目的地端點，為目前選取的 Azure 訂閱建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="1822a-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="1822a-128">這個事件訂閱會指定事件種類和主旨的其他篩選，只有符合這些篩選準則的事件才會傳送到目的地端點。</span><span class="sxs-lookup"><span data-stu-id="1822a-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="1822a-129">範例5</span><span class="sxs-lookup"><span data-stu-id="1822a-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="1822a-130">在目前選取的 Azure 訂閱中建立新的事件訂閱 \` EventSubscription1， \` 並將指定的事件中樞做為事件的目的地。</span><span class="sxs-lookup"><span data-stu-id="1822a-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="1822a-131">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="1822a-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="1822a-132">範例6</span><span class="sxs-lookup"><span data-stu-id="1822a-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1822a-133">\` \` 使用指定的 webhook 目的地端點，為 EventHub 命名空間建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="1822a-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="1822a-134">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="1822a-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="1822a-135">參數</span><span class="sxs-lookup"><span data-stu-id="1822a-135">PARAMETERS</span></span>

### <span data-ttu-id="1822a-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="1822a-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="1822a-137">用來儲存未傳遞事件的端點。</span><span class="sxs-lookup"><span data-stu-id="1822a-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="1822a-138">指定 [儲存 blob] 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1822a-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="1822a-139">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[[容器]]。</span><span class="sxs-lookup"><span data-stu-id="1822a-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1822a-140">-DefaultProfile</span></span>
<span data-ttu-id="1822a-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1822a-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1822a-142">-端點</span><span class="sxs-lookup"><span data-stu-id="1822a-142">-Endpoint</span></span>
<span data-ttu-id="1822a-143">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="1822a-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="1822a-144">這可以是 webhook URL，或 EventHub、storage queue 或 hybridconnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1822a-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="1822a-145">例如，混合式連接的資源識別碼會採用下列形式：/subscriptions/[Azure 訂閱 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="1822a-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="1822a-146">在執行任何事件格線 Cmdlet 前，預期要建立目的地端點，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="1822a-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="1822a-147">-EndpointType</span></span>
<span data-ttu-id="1822a-148">端點類型。</span><span class="sxs-lookup"><span data-stu-id="1822a-148">Endpoint Type.</span></span>
<span data-ttu-id="1822a-149">此可以是 webhook、eventhub、storagequeue 或 hybridconnection。</span><span class="sxs-lookup"><span data-stu-id="1822a-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="1822a-150">預設值為 webhook。</span><span class="sxs-lookup"><span data-stu-id="1822a-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1822a-151">-EventSubscriptionName</span></span>
<span data-ttu-id="1822a-152">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="1822a-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="1822a-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="1822a-153">-EventTtl</span></span>
<span data-ttu-id="1822a-154">事件傳送的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="1822a-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="1822a-155">此值必須介於1與1440之間</span><span class="sxs-lookup"><span data-stu-id="1822a-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="1822a-156">-IncludedEventType</span></span>
<span data-ttu-id="1822a-157">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="1822a-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1822a-158">-InputObject</span></span>
<span data-ttu-id="1822a-159">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="1822a-159">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="1822a-160">-標籤</span><span class="sxs-lookup"><span data-stu-id="1822a-160">-Label</span></span>
<span data-ttu-id="1822a-161">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="1822a-161">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="1822a-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="1822a-163">嘗試傳遞事件的次數上限。</span><span class="sxs-lookup"><span data-stu-id="1822a-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="1822a-164">此值必須介於1和30之間</span><span class="sxs-lookup"><span data-stu-id="1822a-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1822a-165">-ResourceGroupName</span></span>
<span data-ttu-id="1822a-166">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="1822a-166">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1822a-167">-ResourceId</span></span>
<span data-ttu-id="1822a-168">要建立事件訂閱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1822a-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="1822a-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="1822a-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="1822a-170">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="1822a-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="1822a-171">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="1822a-171">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="1822a-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="1822a-173">指定 [subject] 欄位應在區分大小寫的方式下進行比較的篩選。</span><span class="sxs-lookup"><span data-stu-id="1822a-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="1822a-174">如果沒有指定，則會以不區分大小寫的方式來比較主語。</span><span class="sxs-lookup"><span data-stu-id="1822a-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="1822a-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="1822a-175">-SubjectEndsWith</span></span>
<span data-ttu-id="1822a-176">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="1822a-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="1822a-177">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="1822a-177">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="1822a-178">-TopicName</span></span>
<span data-ttu-id="1822a-179">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="1822a-179">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1822a-180">-確認</span><span class="sxs-lookup"><span data-stu-id="1822a-180">-Confirm</span></span>
<span data-ttu-id="1822a-181">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1822a-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1822a-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1822a-182">-WhatIf</span></span>
<span data-ttu-id="1822a-183">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1822a-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1822a-184">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1822a-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1822a-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1822a-185">CommonParameters</span></span>
<span data-ttu-id="1822a-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1822a-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1822a-187">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1822a-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1822a-188">輸入</span><span class="sxs-lookup"><span data-stu-id="1822a-188">INPUTS</span></span>

### <span data-ttu-id="1822a-189">System.object</span><span class="sxs-lookup"><span data-stu-id="1822a-189">System.String</span></span>

### <span data-ttu-id="1822a-190">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="1822a-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="1822a-191">System.object []</span><span class="sxs-lookup"><span data-stu-id="1822a-191">System.String[]</span></span>

## <span data-ttu-id="1822a-192">輸出</span><span class="sxs-lookup"><span data-stu-id="1822a-192">OUTPUTS</span></span>

### <span data-ttu-id="1822a-193">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="1822a-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="1822a-194">筆記</span><span class="sxs-lookup"><span data-stu-id="1822a-194">NOTES</span></span>

## <span data-ttu-id="1822a-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="1822a-195">RELATED LINKS</span></span>
