---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286223"
---
# <span data-ttu-id="008fa-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="008fa-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="008fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="008fa-102">SYNOPSIS</span></span>
<span data-ttu-id="008fa-103">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="008fa-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="008fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="008fa-104">SYNTAX</span></span>

### <span data-ttu-id="008fa-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="008fa-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008fa-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="008fa-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008fa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="008fa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="008fa-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="008fa-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008fa-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="008fa-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008fa-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="008fa-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="008fa-111">說明</span><span class="sxs-lookup"><span data-stu-id="008fa-111">DESCRIPTION</span></span>
<span data-ttu-id="008fa-112">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="008fa-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="008fa-113">這可以用來更新現有事件訂閱的篩選、目的地或標籤。</span><span class="sxs-lookup"><span data-stu-id="008fa-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="008fa-114">示例</span><span class="sxs-lookup"><span data-stu-id="008fa-114">EXAMPLES</span></span>

### <span data-ttu-id="008fa-115">範例1</span><span class="sxs-lookup"><span data-stu-id="008fa-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="008fa-116">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="008fa-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="008fa-117">範例2</span><span class="sxs-lookup"><span data-stu-id="008fa-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="008fa-118">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="008fa-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="008fa-119">範例3</span><span class="sxs-lookup"><span data-stu-id="008fa-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="008fa-120">更新 EventHub namespace ContosoNamespace 的事件訂閱 \` ES1 的屬性，並將新的 [端點為] 與 \` \` https://requestb.in/1kxxoui1\ 新的 SubjectEndsWith 篩選為 \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="008fa-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="008fa-121">範例4</span><span class="sxs-lookup"><span data-stu-id="008fa-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="008fa-122">更新資源群組 MyResourceGroupName 的事件訂閱 ES1 的屬性， \` \` 新 \` 的 \` 標籤會 $labels。</span><span class="sxs-lookup"><span data-stu-id="008fa-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="008fa-123">參數</span><span class="sxs-lookup"><span data-stu-id="008fa-123">PARAMETERS</span></span>

### <span data-ttu-id="008fa-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="008fa-124">-AdvancedFilter</span></span>
<span data-ttu-id="008fa-125">[高級篩選] 指定多個 Hashtable 值的陣列，這些值用於以屬性為基礎的篩選。</span><span class="sxs-lookup"><span data-stu-id="008fa-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="008fa-126">每個 Hashtable 值都具有下列鍵值資訊： Operation、Key 及 Value。</span><span class="sxs-lookup"><span data-stu-id="008fa-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="008fa-127">運算子可以是下列其中一個值： NumberIn、NumberNotIn、NumberLessThan、NumberGreaterThan、NumberLessThanOrEquals、NumberGreaterThanOrEquals、BoolEquals、StringIn、StringNotIn、StringBeginsWith、StringEndsWith、StringContains、、、、、或。</span><span class="sxs-lookup"><span data-stu-id="008fa-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="008fa-128">Key 代表套用高級篩選原則的 [載荷] 屬性。</span><span class="sxs-lookup"><span data-stu-id="008fa-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="008fa-129">最後，值或值代表要相符的值或一組值。</span><span class="sxs-lookup"><span data-stu-id="008fa-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="008fa-130">這個值可以是對應類型的單一值或值的陣列。</span><span class="sxs-lookup"><span data-stu-id="008fa-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="008fa-131">作為 [高級篩選] 參數的範例： $AdvancedFilters = @ ($AdvFilter 1、$AdvFilter 2) ，其中 $AdvFilter 1 = @ {運算子 = "NumberIn"; key = "資料. 1";值 = @ (1，2) } and $AdvFilter 2 = @ {運算子 = "StringBeginsWith"; key = "Subject";值 = @ ( "SubjectPrefix1"，"SubjectPrefix2" ) }</span><span class="sxs-lookup"><span data-stu-id="008fa-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="008fa-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="008fa-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="008fa-133">Azure Active Directory (AAD) 應用程式識別碼或 Uri 來取得存取權杖，並將在傳遞要求中包含為載體權杖。僅適用于 webhook 作為目的地。</span><span class="sxs-lookup"><span data-stu-id="008fa-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008fa-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="008fa-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="008fa-135">Azure Active Directory (AAD) 租使用者識別碼，以取得存取權杖，並將在傳遞要求中包含為載體權杖。僅適用于 webhook 作為目的地。</span><span class="sxs-lookup"><span data-stu-id="008fa-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008fa-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="008fa-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="008fa-137">用來儲存未傳遞事件的端點。</span><span class="sxs-lookup"><span data-stu-id="008fa-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="008fa-138">指定 [儲存 blob] 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="008fa-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="008fa-139">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[[容器]]。</span><span class="sxs-lookup"><span data-stu-id="008fa-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="008fa-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008fa-140">-DefaultProfile</span></span>
<span data-ttu-id="008fa-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="008fa-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="008fa-142">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="008fa-142">-DomainName</span></span>
<span data-ttu-id="008fa-143">要建立事件訂閱之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="008fa-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="008fa-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="008fa-144">-DomainTopicName</span></span>
<span data-ttu-id="008fa-145">要建立事件訂閱之網域主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="008fa-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="008fa-146">-端點</span><span class="sxs-lookup"><span data-stu-id="008fa-146">-Endpoint</span></span>
<span data-ttu-id="008fa-147">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="008fa-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="008fa-148">這可以是 webhook URL，或 EventHub、storage queue、hybridconnection 或 servicebusqueue 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="008fa-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="008fa-149">例如，混合式連接的資源識別碼會採用下列形式：/subscriptions/[Azure 訂閱 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="008fa-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="008fa-150">在執行任何事件格線 Cmdlet 前，預期要建立目的地端點，且可供使用。</span><span class="sxs-lookup"><span data-stu-id="008fa-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="008fa-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="008fa-151">-EndpointType</span></span>
<span data-ttu-id="008fa-152">端點類型。</span><span class="sxs-lookup"><span data-stu-id="008fa-152">Endpoint Type.</span></span>
<span data-ttu-id="008fa-153">此可以是 webhook、eventhub、storagequeue、hybridconnection 或 servicebusqueue。</span><span class="sxs-lookup"><span data-stu-id="008fa-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="008fa-154">預設值為 webhook。</span><span class="sxs-lookup"><span data-stu-id="008fa-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008fa-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="008fa-155">-EventSubscriptionName</span></span>
<span data-ttu-id="008fa-156">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="008fa-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="008fa-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="008fa-157">-EventTtl</span></span>
<span data-ttu-id="008fa-158">事件傳送的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="008fa-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="008fa-159">此值必須介於1與1440之間</span><span class="sxs-lookup"><span data-stu-id="008fa-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="008fa-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="008fa-160">-ExpirationDate</span></span>
<span data-ttu-id="008fa-161">決定事件訂閱在停用之後的到期日期時間。</span><span class="sxs-lookup"><span data-stu-id="008fa-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="008fa-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="008fa-162">-IncludedEventType</span></span>
<span data-ttu-id="008fa-163">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="008fa-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="008fa-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="008fa-164">-InputObject</span></span>
<span data-ttu-id="008fa-165">EventGridSubscription 物件。</span><span class="sxs-lookup"><span data-stu-id="008fa-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="008fa-166">-標籤</span><span class="sxs-lookup"><span data-stu-id="008fa-166">-Label</span></span>
<span data-ttu-id="008fa-167">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="008fa-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="008fa-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="008fa-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="008fa-169">嘗試傳遞事件的次數上限。</span><span class="sxs-lookup"><span data-stu-id="008fa-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="008fa-170">此值必須介於1和30之間</span><span class="sxs-lookup"><span data-stu-id="008fa-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="008fa-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="008fa-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="008fa-172">批次中的最大事件數。</span><span class="sxs-lookup"><span data-stu-id="008fa-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="008fa-173">此值必須介於1到5000。</span><span class="sxs-lookup"><span data-stu-id="008fa-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="008fa-174">此參數在 EnDPInt 類型為 webhook 時有效。</span><span class="sxs-lookup"><span data-stu-id="008fa-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="008fa-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="008fa-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="008fa-176">偏好的批次大小（kb）。</span><span class="sxs-lookup"><span data-stu-id="008fa-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="008fa-177">此值必須介於1到1024。</span><span class="sxs-lookup"><span data-stu-id="008fa-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="008fa-178">此參數在 EnDPInt 類型為 webhook 時有效。</span><span class="sxs-lookup"><span data-stu-id="008fa-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="008fa-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008fa-179">-ResourceGroupName</span></span>
<span data-ttu-id="008fa-180">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="008fa-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="008fa-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="008fa-181">-ResourceId</span></span>
<span data-ttu-id="008fa-182">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="008fa-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="008fa-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="008fa-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="008fa-184">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="008fa-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="008fa-185">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="008fa-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="008fa-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="008fa-186">-SubjectEndsWith</span></span>
<span data-ttu-id="008fa-187">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="008fa-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="008fa-188">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="008fa-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="008fa-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="008fa-189">-TopicName</span></span>
<span data-ttu-id="008fa-190">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="008fa-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="008fa-191">-確認</span><span class="sxs-lookup"><span data-stu-id="008fa-191">-Confirm</span></span>
<span data-ttu-id="008fa-192">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="008fa-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="008fa-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008fa-193">-WhatIf</span></span>
<span data-ttu-id="008fa-194">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="008fa-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="008fa-195">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="008fa-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="008fa-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008fa-196">CommonParameters</span></span>
<span data-ttu-id="008fa-197">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="008fa-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008fa-198">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="008fa-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008fa-199">輸入</span><span class="sxs-lookup"><span data-stu-id="008fa-199">INPUTS</span></span>

### <span data-ttu-id="008fa-200">System.object</span><span class="sxs-lookup"><span data-stu-id="008fa-200">System.String</span></span>

### <span data-ttu-id="008fa-201">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="008fa-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="008fa-202">輸出</span><span class="sxs-lookup"><span data-stu-id="008fa-202">OUTPUTS</span></span>

### <span data-ttu-id="008fa-203">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="008fa-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="008fa-204">筆記</span><span class="sxs-lookup"><span data-stu-id="008fa-204">NOTES</span></span>

## <span data-ttu-id="008fa-205">相關連結</span><span class="sxs-lookup"><span data-stu-id="008fa-205">RELATED LINKS</span></span>
