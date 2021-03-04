---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 13db3232c7d3f2245c6a99ac9a5d38054d885a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911982"
---
# <span data-ttu-id="02c41-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="02c41-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="02c41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02c41-102">SYNOPSIS</span></span>
<span data-ttu-id="02c41-103">為主題、Azure 資源、Azure 訂閱或資源群組建立新 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="02c41-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="02c41-104">語法</span><span class="sxs-lookup"><span data-stu-id="02c41-104">SYNTAX</span></span>

### <span data-ttu-id="02c41-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="02c41-105">ResourceGroupNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="02c41-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c41-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c41-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
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

### <span data-ttu-id="02c41-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
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

### <span data-ttu-id="02c41-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-110">CustomTopicEventSubscriptionParameterSet</span></span>
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

### <span data-ttu-id="02c41-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-111">DomainEventSubscriptionParameterSet</span></span>
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

### <span data-ttu-id="02c41-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c41-112">DomainTopicEventSubscriptionParameterSet</span></span>
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

## <span data-ttu-id="02c41-113">描述</span><span class="sxs-lookup"><span data-stu-id="02c41-113">DESCRIPTION</span></span>
<span data-ttu-id="02c41-114">為 Azure 事件格線主題 、支援的 Azure 資源、Azure 訂閱或資源群組建立新事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="02c41-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="02c41-115">若要建立目前所選 Azure 訂閱的事件訂閱，請指定事件訂閱名稱和目的地端點。</span><span class="sxs-lookup"><span data-stu-id="02c41-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="02c41-116">若要建立資源群組的事件訂閱，除了事件訂閱名稱和目的地端點之外，請指定資源組名。</span><span class="sxs-lookup"><span data-stu-id="02c41-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="02c41-117">若要建立 Azure 事件格線主題的事件訂閱，請同時指定主題名稱。</span><span class="sxs-lookup"><span data-stu-id="02c41-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="02c41-118">若要建立受支援 Azure 資源的事件訂閱，請指定資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="02c41-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="02c41-119">若要查看支援類型的清單，請執行 Get-AzEventGridTopicType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02c41-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="02c41-120">例子</span><span class="sxs-lookup"><span data-stu-id="02c41-120">EXAMPLES</span></span>

### <span data-ttu-id="02c41-121">範例 1</span><span class="sxs-lookup"><span data-stu-id="02c41-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="02c41-122">在資源群組 MyResourceGroupName 中建立新事件訂閱 \` EventSubscription1 至 \` Azure 事件格線主題 \` Topic1，並包含 \` \` \` webaz 目的地端點 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="02c41-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="02c41-123">此事件訂閱使用預設篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="02c41-124">範例 2</span><span class="sxs-lookup"><span data-stu-id="02c41-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="02c41-125">將事件訂閱 \` EventSubscription1 新建立至 \` 具有 web一文目的地端點的資源群組 \` MyResourceGroupName。 \` `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="02c41-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="02c41-126">此事件訂閱使用預設篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="02c41-127">範例 3</span><span class="sxs-lookup"><span data-stu-id="02c41-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="02c41-128">將事件訂閱 EventSubscription1 新建立至目前選取的 Azure 訂閱，並包含 \` \` webaz 目的地端點 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="02c41-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="02c41-129">此事件訂閱使用預設篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="02c41-130">範例 4</span><span class="sxs-lookup"><span data-stu-id="02c41-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="02c41-131">將事件訂閱 EventSubscription1 新建立至目前選取的 Azure 訂閱，並包含 \` \` webaz 目的地端點 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="02c41-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="02c41-132">此事件訂閱會指定事件種類和主題的額外篩選，且只有符合這些篩選的事件會傳送至目的地端點。</span><span class="sxs-lookup"><span data-stu-id="02c41-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="02c41-133">範例 5</span><span class="sxs-lookup"><span data-stu-id="02c41-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="02c41-134">將新事件訂閱 EventSubscription1 建立至目前選取的 Azure 訂閱，並指定事件 \` \` 中樞做為事件的目的地。</span><span class="sxs-lookup"><span data-stu-id="02c41-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="02c41-135">此事件訂閱使用預設篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="02c41-136">範例 6</span><span class="sxs-lookup"><span data-stu-id="02c41-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="02c41-137">建立事件訂閱 \` EventSubscription1 至 \` 具有指定 web一文目的地端點的 EventHub 命名空間 `https://requestb.in/19qlscd1` 。</span><span class="sxs-lookup"><span data-stu-id="02c41-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="02c41-138">此事件訂閱使用預設篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="02c41-139">參數</span><span class="sxs-lookup"><span data-stu-id="02c41-139">PARAMETERS</span></span>

### <span data-ttu-id="02c41-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="02c41-140">-AdvancedFilter</span></span>
<span data-ttu-id="02c41-141">指定用於屬性型篩選之多個雜湊表值的陣列的進一級篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="02c41-142">每個雜湊表值都有下列索引鍵值資訊：運算、索引鍵和值或值。</span><span class="sxs-lookup"><span data-stu-id="02c41-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="02c41-143">運算子可以是下列其中一個值：NumberIn、NumberNotIn、NumberLessQual、NumberGreaterQual、NumberLessQualOrEquals、NumberGreaterQualOrEquals、BoolEquals、StringIn、StringNotIn、StringBeginsWith、StringEndsWith 或 StringContains。</span><span class="sxs-lookup"><span data-stu-id="02c41-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="02c41-144">Key 代表已使用進位篩選原則的負載屬性。</span><span class="sxs-lookup"><span data-stu-id="02c41-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="02c41-145">最後，值或值代表要相符的值或一組值。</span><span class="sxs-lookup"><span data-stu-id="02c41-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="02c41-146">這可以是對應類型的單一值或值陣列。</span><span class="sxs-lookup"><span data-stu-id="02c41-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="02c41-147">做為進一步篩選參數的範例：$AdvancedFilters=@ ($AdvFilter 1、$AdvFilter 2) 其中 $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1";Values=@ (1，2) } 和 $AdvFilter 2=@{operator="StringBringsWith"; key="Subject";Values=@ ("SubjectPrefix1"，"SubjectPrefix2") }</span><span class="sxs-lookup"><span data-stu-id="02c41-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="02c41-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="02c41-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="02c41-149">Azure Active Directory (AAD) 應用程式識別碼或 Uri，以取得會包含在傳遞要求中的承載權杖的存取權杖。僅適用于 web下一個目的地。</span><span class="sxs-lookup"><span data-stu-id="02c41-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="02c41-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="02c41-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="02c41-151">Azure Active Directory (AAD) 租使用者識別碼，以取得將包含在傳遞要求中的承載權杖的存取權杖。僅適用于 web下一個目的地。</span><span class="sxs-lookup"><span data-stu-id="02c41-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="02c41-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="02c41-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="02c41-153">用來儲存未送達事件的端點。</span><span class="sxs-lookup"><span data-stu-id="02c41-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="02c41-154">指定儲存 Blob 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="02c41-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="02c41-155">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName]。</span><span class="sxs-lookup"><span data-stu-id="02c41-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="02c41-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c41-156">-DefaultProfile</span></span>
<span data-ttu-id="02c41-157">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="02c41-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02c41-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="02c41-158">-DeliverySchema</span></span>
<span data-ttu-id="02c41-159">將事件傳遞至目的地時所使用的架構。</span><span class="sxs-lookup"><span data-stu-id="02c41-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="02c41-160">可能的值為：eventgridschema、CustomInputSchema 或 cloudeventv01schema。</span><span class="sxs-lookup"><span data-stu-id="02c41-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="02c41-161">預設值為 CustomInputSchema。</span><span class="sxs-lookup"><span data-stu-id="02c41-161">Default value is CustomInputSchema.</span></span>

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

### <span data-ttu-id="02c41-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="02c41-162">-DomainInputObject</span></span>
<span data-ttu-id="02c41-163">EventGrid 網域物件。</span><span class="sxs-lookup"><span data-stu-id="02c41-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="02c41-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="02c41-164">-DomainName</span></span>
<span data-ttu-id="02c41-165">事件訂閱應建立之事件格線網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="02c41-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="02c41-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="02c41-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="02c41-167">EventGrid 網域主題物件。</span><span class="sxs-lookup"><span data-stu-id="02c41-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="02c41-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="02c41-168">-DomainTopicName</span></span>
<span data-ttu-id="02c41-169">事件訂閱應建立之網域主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="02c41-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="02c41-170">-端點</span><span class="sxs-lookup"><span data-stu-id="02c41-170">-Endpoint</span></span>
<span data-ttu-id="02c41-171">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="02c41-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="02c41-172">這可以是 Webection URL，或是 EventHub、儲存佇列、混合式連接或 servicebusqueue 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="02c41-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="02c41-173">例如，混合式連接的資源識別碼採用下列形式：/subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/命名空間/[命名空間Name]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="02c41-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="02c41-174">執行任何事件格線 Cmdlet 之前，預期會建立目的端點並可供使用。</span><span class="sxs-lookup"><span data-stu-id="02c41-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="02c41-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="02c41-175">-EndpointType</span></span>
<span data-ttu-id="02c41-176">端點類型。</span><span class="sxs-lookup"><span data-stu-id="02c41-176">Endpoint Type.</span></span>
<span data-ttu-id="02c41-177">這可以是 webection、eventhub、storagequeue、hybridconnection 或 servicebusqueue。</span><span class="sxs-lookup"><span data-stu-id="02c41-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="02c41-178">預設值為 web一。</span><span class="sxs-lookup"><span data-stu-id="02c41-178">Default value is webhook.</span></span>

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

### <span data-ttu-id="02c41-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="02c41-179">-EventSubscriptionName</span></span>
<span data-ttu-id="02c41-180">活動訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="02c41-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="02c41-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="02c41-181">-EventTtl</span></span>
<span data-ttu-id="02c41-182">活動傳遞的時間 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="02c41-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="02c41-183">此值必須介於 1 到 1440 之間</span><span class="sxs-lookup"><span data-stu-id="02c41-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="02c41-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="02c41-184">-ExpirationDate</span></span>
<span data-ttu-id="02c41-185">決定活動訂閱的到期日日期時間，活動訂閱將在之後淘汰。</span><span class="sxs-lookup"><span data-stu-id="02c41-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="02c41-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="02c41-186">-IncludedEventType</span></span>
<span data-ttu-id="02c41-187">指定要包含的事件種類清單的篩選。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="02c41-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="02c41-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c41-188">-InputObject</span></span>
<span data-ttu-id="02c41-189">EventGrid Topic 物件。</span><span class="sxs-lookup"><span data-stu-id="02c41-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="02c41-190">-標籤</span><span class="sxs-lookup"><span data-stu-id="02c41-190">-Label</span></span>
<span data-ttu-id="02c41-191">活動訂閱的標號</span><span class="sxs-lookup"><span data-stu-id="02c41-191">Labels for the event subscription</span></span>

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

### <span data-ttu-id="02c41-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="02c41-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="02c41-193">傳遞活動的嘗試次數上限。</span><span class="sxs-lookup"><span data-stu-id="02c41-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="02c41-194">此值必須介於 1 到 30 之間</span><span class="sxs-lookup"><span data-stu-id="02c41-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="02c41-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="02c41-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="02c41-196">批次中事件的數量上限。</span><span class="sxs-lookup"><span data-stu-id="02c41-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="02c41-197">此值必須介於 1 到 5000 之間。</span><span class="sxs-lookup"><span data-stu-id="02c41-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="02c41-198">此參數在 EnDPInt 類型為 Web一次時有效。</span><span class="sxs-lookup"><span data-stu-id="02c41-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="02c41-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="02c41-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="02c41-200">這是偏好的批次大小 ，以 KB 為單位。</span><span class="sxs-lookup"><span data-stu-id="02c41-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="02c41-201">此值必須介於 1 到 1024 之間。</span><span class="sxs-lookup"><span data-stu-id="02c41-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="02c41-202">此參數在 EnDPInt 類型為 Web一次時有效。</span><span class="sxs-lookup"><span data-stu-id="02c41-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="02c41-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c41-203">-ResourceGroupName</span></span>
<span data-ttu-id="02c41-204">主題的資源群組。</span><span class="sxs-lookup"><span data-stu-id="02c41-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="02c41-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02c41-205">-ResourceId</span></span>
<span data-ttu-id="02c41-206">應建立事件訂閱之資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="02c41-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="02c41-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="02c41-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="02c41-208">指定只包含符合指定主題首碼的事件的篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="02c41-209">如果未指定，會包含具有所有主體首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="02c41-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="02c41-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="02c41-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="02c41-211">指定以區分大小寫的方式比較主題欄位的篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="02c41-212">如果未指定，主題會以不區分大小寫的方式進行比較。</span><span class="sxs-lookup"><span data-stu-id="02c41-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="02c41-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="02c41-213">-SubjectEndsWith</span></span>
<span data-ttu-id="02c41-214">指定只包含符合指定主題尾碼的事件的篩選。</span><span class="sxs-lookup"><span data-stu-id="02c41-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="02c41-215">如果未指定，會包含具有所有主體尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="02c41-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="02c41-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="02c41-216">-TopicName</span></span>
<span data-ttu-id="02c41-217">應建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="02c41-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="02c41-218">-確認</span><span class="sxs-lookup"><span data-stu-id="02c41-218">-Confirm</span></span>
<span data-ttu-id="02c41-219">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="02c41-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c41-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c41-220">-WhatIf</span></span>
<span data-ttu-id="02c41-221">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02c41-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c41-222">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02c41-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c41-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c41-223">CommonParameters</span></span>
<span data-ttu-id="02c41-224">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02c41-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c41-225">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02c41-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c41-226">輸入</span><span class="sxs-lookup"><span data-stu-id="02c41-226">INPUTS</span></span>

### <span data-ttu-id="02c41-227">System.String</span><span class="sxs-lookup"><span data-stu-id="02c41-227">System.String</span></span>

### <span data-ttu-id="02c41-228">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="02c41-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="02c41-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="02c41-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="02c41-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="02c41-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="02c41-231">System.String[]</span><span class="sxs-lookup"><span data-stu-id="02c41-231">System.String[]</span></span>

### <span data-ttu-id="02c41-232">System.Int32</span><span class="sxs-lookup"><span data-stu-id="02c41-232">System.Int32</span></span>

## <span data-ttu-id="02c41-233">輸出</span><span class="sxs-lookup"><span data-stu-id="02c41-233">OUTPUTS</span></span>

### <span data-ttu-id="02c41-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="02c41-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="02c41-235">筆記</span><span class="sxs-lookup"><span data-stu-id="02c41-235">NOTES</span></span>

## <span data-ttu-id="02c41-236">相關連結</span><span class="sxs-lookup"><span data-stu-id="02c41-236">RELATED LINKS</span></span>
