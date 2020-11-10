---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395317"
---
# <span data-ttu-id="6296c-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6296c-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="6296c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6296c-102">SYNOPSIS</span></span>
<span data-ttu-id="6296c-103">針對主題、Azure 資源、Azure 訂閱或資源群組建立新的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="6296c-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="6296c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6296c-104">SYNTAX</span></span>

### <span data-ttu-id="6296c-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6296c-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6296c-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6296c-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6296c-113">說明</span><span class="sxs-lookup"><span data-stu-id="6296c-113">DESCRIPTION</span></span>
<span data-ttu-id="6296c-114">建立 Azure 事件格線主題（支援的 Azure 資源、Azure 訂閱或資源群組）的新事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="6296c-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="6296c-115">若要建立目前所選 Azure 訂閱的事件訂閱，請指定事件訂閱名稱和目標端點。</span><span class="sxs-lookup"><span data-stu-id="6296c-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="6296c-116">若要建立資源群組的事件訂閱，除了事件訂閱名稱和目的地端點之外，還可以指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6296c-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="6296c-117">若要建立 Azure 事件格線主題的事件訂閱，請同時指定主題名稱。</span><span class="sxs-lookup"><span data-stu-id="6296c-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="6296c-118">若要建立支援的 Azure 資源的事件訂閱，請指定資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6296c-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="6296c-119">若要查看受支援類型的清單，請執行 Get-AzEventGridTopicType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6296c-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="6296c-120">示例</span><span class="sxs-lookup"><span data-stu-id="6296c-120">EXAMPLES</span></span>

### <span data-ttu-id="6296c-121">範例1</span><span class="sxs-lookup"><span data-stu-id="6296c-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6296c-122">\` \` \` \` \` \` 使用 webhook 目的地端點在資源群組 MyResourceGroupName 中 Topic1 Azure 事件格線主題建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="6296c-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6296c-123">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="6296c-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6296c-124">範例2</span><span class="sxs-lookup"><span data-stu-id="6296c-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6296c-125">\` \` \` \` 使用 webhook 目的地端點的資源群組 MyResourceGroupName 建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="6296c-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6296c-126">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="6296c-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6296c-127">範例3</span><span class="sxs-lookup"><span data-stu-id="6296c-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6296c-128">\` \` 使用 webhook 目的地端點，為目前選取的 Azure 訂閱建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="6296c-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6296c-129">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="6296c-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6296c-130">範例4</span><span class="sxs-lookup"><span data-stu-id="6296c-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="6296c-131">\` \` 使用 webhook 目的地端點，為目前選取的 Azure 訂閱建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="6296c-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6296c-132">這個事件訂閱會指定事件種類和主旨的其他篩選，只有符合這些篩選準則的事件才會傳送到目的地端點。</span><span class="sxs-lookup"><span data-stu-id="6296c-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="6296c-133">範例5</span><span class="sxs-lookup"><span data-stu-id="6296c-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="6296c-134">在目前選取的 Azure 訂閱中建立新的事件訂閱 \` EventSubscription1， \` 並將指定的事件中樞做為事件的目的地。</span><span class="sxs-lookup"><span data-stu-id="6296c-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="6296c-135">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="6296c-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6296c-136">範例6</span><span class="sxs-lookup"><span data-stu-id="6296c-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6296c-137">\` \` 使用指定的 webhook 目的地端點，為 EventHub 命名空間建立新的事件訂閱 EventSubscription1 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="6296c-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6296c-138">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="6296c-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="6296c-139">參數</span><span class="sxs-lookup"><span data-stu-id="6296c-139">PARAMETERS</span></span>

### <span data-ttu-id="6296c-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="6296c-140">-AdvancedFilter</span></span>
<span data-ttu-id="6296c-141">[高級篩選] 指定多個 Hashtable 值的陣列，這些值用於以屬性為基礎的篩選。</span><span class="sxs-lookup"><span data-stu-id="6296c-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="6296c-142">每個 Hashtable 值都具有下列鍵值資訊： Operation、Key 及 Value。</span><span class="sxs-lookup"><span data-stu-id="6296c-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="6296c-143">運算子可以是下列其中一個值： NumberIn、NumberNotIn、NumberLessThan、NumberGreaterThan、NumberLessThanOrEquals、NumberGreaterThanOrEquals、BoolEquals、StringIn、StringNotIn、StringBeginsWith、StringEndsWith、StringContains、、、、、或。</span><span class="sxs-lookup"><span data-stu-id="6296c-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="6296c-144">Key 代表套用高級篩選原則的 [載荷] 屬性。</span><span class="sxs-lookup"><span data-stu-id="6296c-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="6296c-145">最後，值或值代表要相符的值或一組值。</span><span class="sxs-lookup"><span data-stu-id="6296c-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="6296c-146">這個值可以是對應類型的單一值或值的陣列。</span><span class="sxs-lookup"><span data-stu-id="6296c-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="6296c-147">作為 [高級篩選] 參數的範例： $AdvancedFilters = @ ($AdvFilter 1、$AdvFilter 2) ，其中 $AdvFilter 1 = @ {運算子 = "NumberIn"; key = "資料. 1";值 = @ (1，2) } and $AdvFilter 2 = @ {運算子 = "StringBringsWith"; key = "Subject";值 = @ ( "SubjectPrefix1"，"SubjectPrefix2" ) }</span><span class="sxs-lookup"><span data-stu-id="6296c-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="6296c-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="6296c-149">Azure Active Directory (AAD) 應用程式識別碼或 Uri 來取得存取權杖，並將在傳遞要求中包含為載體權杖。僅適用于 webhook 作為目的地。</span><span class="sxs-lookup"><span data-stu-id="6296c-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="6296c-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="6296c-151">Azure Active Directory (AAD) 租使用者識別碼，以取得存取權杖，並將在傳遞要求中包含為載體權杖。僅適用于 webhook 作為目的地。</span><span class="sxs-lookup"><span data-stu-id="6296c-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="6296c-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="6296c-153">用來儲存未傳遞事件的端點。</span><span class="sxs-lookup"><span data-stu-id="6296c-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="6296c-154">指定 [儲存 blob] 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6296c-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="6296c-155">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[[容器]]。</span><span class="sxs-lookup"><span data-stu-id="6296c-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6296c-156">-DefaultProfile</span></span>
<span data-ttu-id="6296c-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6296c-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6296c-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="6296c-158">-DeliverySchema</span></span>
<span data-ttu-id="6296c-159">將事件傳送至目的地時要使用的架構。</span><span class="sxs-lookup"><span data-stu-id="6296c-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="6296c-160">可能的值為： eventgridschema、CustomInputSchema 或 cloudeventv01schema。</span><span class="sxs-lookup"><span data-stu-id="6296c-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="6296c-161">預設值為 CustomInputSchema。</span><span class="sxs-lookup"><span data-stu-id="6296c-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="6296c-162">-DomainInputObject</span></span>
<span data-ttu-id="6296c-163">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="6296c-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="6296c-164">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="6296c-164">-DomainName</span></span>
<span data-ttu-id="6296c-165">要在其中建立事件訂閱的事件網格網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6296c-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="6296c-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="6296c-167">EventGrid [網域] 主題物件。</span><span class="sxs-lookup"><span data-stu-id="6296c-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="6296c-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="6296c-168">-DomainTopicName</span></span>
<span data-ttu-id="6296c-169">要建立事件訂閱之網域主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="6296c-169">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-170">-端點</span><span class="sxs-lookup"><span data-stu-id="6296c-170">-Endpoint</span></span>
<span data-ttu-id="6296c-171">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="6296c-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="6296c-172">這可以是 webhook URL，或 EventHub、storage queue、hybridconnection 或 servicebusqueue 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6296c-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="6296c-173">例如，混合式連接的資源識別碼會採用下列形式：/subscriptions/[Azure 訂閱 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="6296c-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="6296c-174">在執行任何事件格線 Cmdlet 前，預期要建立目的地端點，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="6296c-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6296c-175">-EndpointType</span></span>
<span data-ttu-id="6296c-176">端點類型。</span><span class="sxs-lookup"><span data-stu-id="6296c-176">Endpoint Type.</span></span>
<span data-ttu-id="6296c-177">此可以是 webhook、eventhub、storagequeue、hybridconnection 或 servicebusqueue。</span><span class="sxs-lookup"><span data-stu-id="6296c-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="6296c-178">預設值為 webhook。</span><span class="sxs-lookup"><span data-stu-id="6296c-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6296c-179">-EventSubscriptionName</span></span>
<span data-ttu-id="6296c-180">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="6296c-180">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
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

### <span data-ttu-id="6296c-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="6296c-181">-EventTtl</span></span>
<span data-ttu-id="6296c-182">事件傳送的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="6296c-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="6296c-183">此值必須介於1與1440之間</span><span class="sxs-lookup"><span data-stu-id="6296c-183">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="6296c-184">-ExpirationDate</span></span>
<span data-ttu-id="6296c-185">決定事件訂閱在停用之後的到期日期時間。</span><span class="sxs-lookup"><span data-stu-id="6296c-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="6296c-186">-IncludedEventType</span></span>
<span data-ttu-id="6296c-187">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="6296c-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6296c-188">-InputObject</span></span>
<span data-ttu-id="6296c-189">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="6296c-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6296c-190">-標籤</span><span class="sxs-lookup"><span data-stu-id="6296c-190">-Label</span></span>
<span data-ttu-id="6296c-191">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="6296c-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="6296c-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="6296c-193">嘗試傳遞事件的次數上限。</span><span class="sxs-lookup"><span data-stu-id="6296c-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="6296c-194">此值必須介於1和30之間</span><span class="sxs-lookup"><span data-stu-id="6296c-194">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="6296c-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="6296c-196">批次中的最大事件數。</span><span class="sxs-lookup"><span data-stu-id="6296c-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="6296c-197">此值必須介於1到5000。</span><span class="sxs-lookup"><span data-stu-id="6296c-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="6296c-198">此參數在 EnDPInt 類型為 webhook 時有效。</span><span class="sxs-lookup"><span data-stu-id="6296c-198">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="6296c-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="6296c-200">偏好的批次大小（kb）。</span><span class="sxs-lookup"><span data-stu-id="6296c-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="6296c-201">此值必須介於1到1024。</span><span class="sxs-lookup"><span data-stu-id="6296c-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="6296c-202">此參數在 EnDPInt 類型為 webhook 時有效。</span><span class="sxs-lookup"><span data-stu-id="6296c-202">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6296c-203">-ResourceGroupName</span></span>
<span data-ttu-id="6296c-204">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="6296c-204">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6296c-205">-ResourceId</span></span>
<span data-ttu-id="6296c-206">要建立事件訂閱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6296c-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6296c-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="6296c-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="6296c-208">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="6296c-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="6296c-209">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="6296c-209">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="6296c-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="6296c-211">指定 [subject] 欄位應在區分大小寫的方式下進行比較的篩選。</span><span class="sxs-lookup"><span data-stu-id="6296c-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="6296c-212">如果沒有指定，則會以不區分大小寫的方式來比較主語。</span><span class="sxs-lookup"><span data-stu-id="6296c-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="6296c-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="6296c-213">-SubjectEndsWith</span></span>
<span data-ttu-id="6296c-214">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="6296c-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="6296c-215">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="6296c-215">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6296c-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6296c-216">-TopicName</span></span>
<span data-ttu-id="6296c-217">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="6296c-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6296c-218">-確認</span><span class="sxs-lookup"><span data-stu-id="6296c-218">-Confirm</span></span>
<span data-ttu-id="6296c-219">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6296c-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6296c-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6296c-220">-WhatIf</span></span>
<span data-ttu-id="6296c-221">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6296c-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6296c-222">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6296c-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6296c-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6296c-223">CommonParameters</span></span>
<span data-ttu-id="6296c-224">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6296c-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6296c-225">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6296c-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6296c-226">輸入</span><span class="sxs-lookup"><span data-stu-id="6296c-226">INPUTS</span></span>

### <span data-ttu-id="6296c-227">System.object</span><span class="sxs-lookup"><span data-stu-id="6296c-227">System.String</span></span>

### <span data-ttu-id="6296c-228">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="6296c-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="6296c-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="6296c-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="6296c-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6296c-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="6296c-231">System.object []</span><span class="sxs-lookup"><span data-stu-id="6296c-231">System.String[]</span></span>

### <span data-ttu-id="6296c-232">System.object</span><span class="sxs-lookup"><span data-stu-id="6296c-232">System.Int32</span></span>

## <span data-ttu-id="6296c-233">輸出</span><span class="sxs-lookup"><span data-stu-id="6296c-233">OUTPUTS</span></span>

### <span data-ttu-id="6296c-234">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="6296c-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="6296c-235">筆記</span><span class="sxs-lookup"><span data-stu-id="6296c-235">NOTES</span></span>

## <span data-ttu-id="6296c-236">相關連結</span><span class="sxs-lookup"><span data-stu-id="6296c-236">RELATED LINKS</span></span>
