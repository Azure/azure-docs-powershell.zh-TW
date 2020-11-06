---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: eaf9a89a8c610d8666a356e563681accfced4a7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612447"
---
# <span data-ttu-id="036d2-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="036d2-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="036d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="036d2-102">SYNOPSIS</span></span>
<span data-ttu-id="036d2-103">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="036d2-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="036d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="036d2-104">SYNTAX</span></span>

### <span data-ttu-id="036d2-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="036d2-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="036d2-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="036d2-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="036d2-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="036d2-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036d2-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="036d2-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="036d2-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="036d2-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="036d2-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="036d2-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="036d2-111">說明</span><span class="sxs-lookup"><span data-stu-id="036d2-111">DESCRIPTION</span></span>
<span data-ttu-id="036d2-112">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="036d2-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="036d2-113">這可以用來更新現有事件訂閱的篩選、目的地或標籤。</span><span class="sxs-lookup"><span data-stu-id="036d2-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="036d2-114">示例</span><span class="sxs-lookup"><span data-stu-id="036d2-114">EXAMPLES</span></span>

### <span data-ttu-id="036d2-115">範例1</span><span class="sxs-lookup"><span data-stu-id="036d2-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="036d2-116">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="036d2-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="036d2-117">範例2</span><span class="sxs-lookup"><span data-stu-id="036d2-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="036d2-118">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="036d2-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="036d2-119">範例3</span><span class="sxs-lookup"><span data-stu-id="036d2-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="036d2-120">更新 EventHub namespace ContosoNamespace 的事件訂閱 \` ES1 的屬性，並將新的 [端點為] 與 \` \` https://requestb.in/1kxxoui1\ 新的 SubjectEndsWith 篩選為 \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="036d2-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="036d2-121">範例4</span><span class="sxs-lookup"><span data-stu-id="036d2-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="036d2-122">更新資源群組 MyResourceGroupName 的事件訂閱 ES1 的屬性， \` \` 新 \` 的 \` 標籤會 $labels。</span><span class="sxs-lookup"><span data-stu-id="036d2-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="036d2-123">參數</span><span class="sxs-lookup"><span data-stu-id="036d2-123">PARAMETERS</span></span>

### <span data-ttu-id="036d2-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="036d2-124">-AdvancedFilter</span></span>
<span data-ttu-id="036d2-125">[高級篩選] 指定多個 Hashtable 值的陣列，這些值用於以屬性為基礎的篩選。</span><span class="sxs-lookup"><span data-stu-id="036d2-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="036d2-126">每個 Hashtable 值都具有下列鍵值資訊： Operation、Key 及 Value。</span><span class="sxs-lookup"><span data-stu-id="036d2-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="036d2-127">運算子可以是下列其中一個值： NumberIn、NumberNotIn、NumberLessThan、NumberGreaterThan、NumberLessThanOrEquals、NumberGreaterThanOrEquals、BoolEquals、StringIn、StringNotIn、StringBeginsWith、StringEndsWith、StringContains、、、、、或。</span><span class="sxs-lookup"><span data-stu-id="036d2-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="036d2-128">Key 代表套用高級篩選原則的 [載荷] 屬性。</span><span class="sxs-lookup"><span data-stu-id="036d2-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="036d2-129">最後，值或值代表要相符的值或一組值。</span><span class="sxs-lookup"><span data-stu-id="036d2-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="036d2-130">這個值可以是對應類型的單一值或值的陣列。</span><span class="sxs-lookup"><span data-stu-id="036d2-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="036d2-131">作為 [高級篩選] 參數的範例： $AdvancedFilters = @ ($AdvFilter 1、$AdvFilter 2) ，其中 $AdvFilter 1 = @ {運算子 = "NumberIn"; key = "資料. 1";值 = @ (1，2) } and $AdvFilter 2 = @ {運算子 = "StringBringsWith"; key = "Subject";值 = @ ( "SubjectPrefix1"，"SubjectPrefix2" ) }</span><span class="sxs-lookup"><span data-stu-id="036d2-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="036d2-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="036d2-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="036d2-133">用來儲存未傳遞事件的端點。</span><span class="sxs-lookup"><span data-stu-id="036d2-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="036d2-134">指定 [儲存 blob] 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="036d2-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="036d2-135">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[[容器]]。</span><span class="sxs-lookup"><span data-stu-id="036d2-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="036d2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036d2-136">-DefaultProfile</span></span>
<span data-ttu-id="036d2-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="036d2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="036d2-138">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="036d2-138">-DomainName</span></span>
<span data-ttu-id="036d2-139">要建立事件訂閱之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="036d2-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="036d2-140">-DomainTopicName</span></span>
<span data-ttu-id="036d2-141">要建立事件訂閱之網域主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="036d2-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-142">-端點</span><span class="sxs-lookup"><span data-stu-id="036d2-142">-Endpoint</span></span>
<span data-ttu-id="036d2-143">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="036d2-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="036d2-144">這可以是 webhook URL，或 EventHub、storage queue、hybridconnection 或 servicebusqueue 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="036d2-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="036d2-145">例如，混合式連接的資源識別碼會採用下列形式：/subscriptions/[Azure 訂閱 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="036d2-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="036d2-146">在執行任何事件格線 Cmdlet 前，預期要建立目的地端點，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="036d2-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="036d2-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="036d2-147">-EndpointType</span></span>
<span data-ttu-id="036d2-148">端點類型。</span><span class="sxs-lookup"><span data-stu-id="036d2-148">Endpoint Type.</span></span>
<span data-ttu-id="036d2-149">此可以是 webhook、eventhub、storagequeue、hybridconnection 或 servicebusqueue。</span><span class="sxs-lookup"><span data-stu-id="036d2-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="036d2-150">預設值為 webhook。</span><span class="sxs-lookup"><span data-stu-id="036d2-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="036d2-151">-EventSubscriptionName</span></span>
<span data-ttu-id="036d2-152">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="036d2-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="036d2-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="036d2-153">-EventTtl</span></span>
<span data-ttu-id="036d2-154">事件傳送的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="036d2-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="036d2-155">此值必須介於1與1440之間</span><span class="sxs-lookup"><span data-stu-id="036d2-155">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="036d2-156">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="036d2-156">-ExpirationDate</span></span>
<span data-ttu-id="036d2-157">決定事件訂閱在停用之後的到期日期時間。</span><span class="sxs-lookup"><span data-stu-id="036d2-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="036d2-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="036d2-158">-IncludedEventType</span></span>
<span data-ttu-id="036d2-159">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="036d2-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="036d2-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="036d2-160">-InputObject</span></span>
<span data-ttu-id="036d2-161">EventGridSubscription 物件。</span><span class="sxs-lookup"><span data-stu-id="036d2-161">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="036d2-162">-標籤</span><span class="sxs-lookup"><span data-stu-id="036d2-162">-Label</span></span>
<span data-ttu-id="036d2-163">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="036d2-163">Labels for the event subscription</span></span>

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

### <span data-ttu-id="036d2-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="036d2-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="036d2-165">嘗試傳遞事件的次數上限。</span><span class="sxs-lookup"><span data-stu-id="036d2-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="036d2-166">此值必須介於1和30之間</span><span class="sxs-lookup"><span data-stu-id="036d2-166">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="036d2-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="036d2-167">-ResourceGroupName</span></span>
<span data-ttu-id="036d2-168">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="036d2-168">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="036d2-169">-ResourceId</span></span>
<span data-ttu-id="036d2-170">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="036d2-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="036d2-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="036d2-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="036d2-172">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="036d2-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="036d2-173">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="036d2-173">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="036d2-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="036d2-174">-SubjectEndsWith</span></span>
<span data-ttu-id="036d2-175">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="036d2-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="036d2-176">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="036d2-176">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="036d2-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="036d2-177">-TopicName</span></span>
<span data-ttu-id="036d2-178">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="036d2-178">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="036d2-179">-確認</span><span class="sxs-lookup"><span data-stu-id="036d2-179">-Confirm</span></span>
<span data-ttu-id="036d2-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="036d2-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036d2-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036d2-181">-WhatIf</span></span>
<span data-ttu-id="036d2-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="036d2-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036d2-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="036d2-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036d2-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036d2-184">CommonParameters</span></span>
<span data-ttu-id="036d2-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="036d2-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036d2-186">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="036d2-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036d2-187">輸入</span><span class="sxs-lookup"><span data-stu-id="036d2-187">INPUTS</span></span>

### <span data-ttu-id="036d2-188">System.object</span><span class="sxs-lookup"><span data-stu-id="036d2-188">System.String</span></span>

### <span data-ttu-id="036d2-189">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="036d2-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="036d2-190">輸出</span><span class="sxs-lookup"><span data-stu-id="036d2-190">OUTPUTS</span></span>

### <span data-ttu-id="036d2-191">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="036d2-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="036d2-192">筆記</span><span class="sxs-lookup"><span data-stu-id="036d2-192">NOTES</span></span>

## <span data-ttu-id="036d2-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="036d2-193">RELATED LINKS</span></span>
