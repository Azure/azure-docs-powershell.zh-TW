---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: dc8515cb37d18a36fa00c6803fda06a1e4d1f1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914846"
---
# <span data-ttu-id="e1d97-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d97-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="e1d97-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1d97-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d97-103">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1d97-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="e1d97-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1d97-104">SYNTAX</span></span>

### <span data-ttu-id="e1d97-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e1d97-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d97-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d97-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d97-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d97-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1d97-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d97-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d97-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d97-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d97-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d97-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d97-111">描述</span><span class="sxs-lookup"><span data-stu-id="e1d97-111">DESCRIPTION</span></span>
<span data-ttu-id="e1d97-112">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1d97-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="e1d97-113">這可以用來更新現有事件訂閱的篩選、目的地或標籤。</span><span class="sxs-lookup"><span data-stu-id="e1d97-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="e1d97-114">例子</span><span class="sxs-lookup"><span data-stu-id="e1d97-114">EXAMPLES</span></span>

### <span data-ttu-id="e1d97-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="e1d97-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="e1d97-116">將資源群組 \` \` \` \` \` MyResourceGroupName 中主題 1 的事件訂閱 ES1 端點更新 \` 為 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="e1d97-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="e1d97-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="e1d97-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="e1d97-118">將資源群組 \` \` \` \` \` MyResourceGroupName 中主題 1 的事件訂閱 ES1 端點更新 \` 為 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="e1d97-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="e1d97-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="e1d97-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="e1d97-120">將 EventHub 命名空間 ContosoNamespace 的事件訂閱 ES1 屬性更新為 ' 的新端點，以及新的 \` \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith 篩選為 \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="e1d97-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="e1d97-121">範例 4</span><span class="sxs-lookup"><span data-stu-id="e1d97-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="e1d97-122">將資源群組 \` \` \` MyResourceGroupName 的事件訂閱 ES1 屬性更新為新的 \` $labels。</span><span class="sxs-lookup"><span data-stu-id="e1d97-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="e1d97-123">參數</span><span class="sxs-lookup"><span data-stu-id="e1d97-123">PARAMETERS</span></span>

### <span data-ttu-id="e1d97-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="e1d97-124">-AdvancedFilter</span></span>
<span data-ttu-id="e1d97-125">指定用於屬性型篩選之多個雜湊表值的陣列的進一級篩選。</span><span class="sxs-lookup"><span data-stu-id="e1d97-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="e1d97-126">每個雜湊表值都有下列索引鍵值資訊：運算、索引鍵和值或值。</span><span class="sxs-lookup"><span data-stu-id="e1d97-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="e1d97-127">運算子可以是下列其中一個值：NumberIn、NumberNotIn、NumberLessQual、NumberGreaterQual、NumberLessQualOrEquals、NumberGreaterQualOrEquals、BoolEquals、StringIn、StringNotIn、StringBeginsWith、StringEndsWith 或 StringContains。</span><span class="sxs-lookup"><span data-stu-id="e1d97-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="e1d97-128">Key 代表已使用進位篩選原則的負載屬性。</span><span class="sxs-lookup"><span data-stu-id="e1d97-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="e1d97-129">最後，值或值代表要相符的值或一組值。</span><span class="sxs-lookup"><span data-stu-id="e1d97-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="e1d97-130">這可以是對應類型的單一值或值陣列。</span><span class="sxs-lookup"><span data-stu-id="e1d97-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="e1d97-131">做為進一步篩選參數的範例：$AdvancedFilters=@ ($AdvFilter 1、$AdvFilter 2) 其中 $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1";Values=@ (1，2) } 和 $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject";Values=@ ("SubjectPrefix1"，"SubjectPrefix2") }</span><span class="sxs-lookup"><span data-stu-id="e1d97-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="e1d97-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="e1d97-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="e1d97-133">Azure Active Directory (AAD) 應用程式識別碼或 Uri，以取得會包含在傳遞要求中的承載權杖的存取權杖。僅適用于 web下一個目的地。</span><span class="sxs-lookup"><span data-stu-id="e1d97-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="e1d97-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="e1d97-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="e1d97-135">Azure Active Directory (AAD) 租使用者識別碼，以取得將包含在傳遞要求中的承載權杖的存取權杖。僅適用于 web下一個目的地。</span><span class="sxs-lookup"><span data-stu-id="e1d97-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="e1d97-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1d97-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="e1d97-137">用來儲存未送達事件的端點。</span><span class="sxs-lookup"><span data-stu-id="e1d97-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="e1d97-138">指定儲存 Blob 容器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1d97-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="e1d97-139">例如：/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName]。</span><span class="sxs-lookup"><span data-stu-id="e1d97-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="e1d97-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d97-140">-DefaultProfile</span></span>
<span data-ttu-id="e1d97-141">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1d97-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d97-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e1d97-142">-DomainName</span></span>
<span data-ttu-id="e1d97-143">事件訂閱應建立之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d97-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e1d97-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="e1d97-144">-DomainTopicName</span></span>
<span data-ttu-id="e1d97-145">事件訂閱應建立之網域主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d97-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e1d97-146">-端點</span><span class="sxs-lookup"><span data-stu-id="e1d97-146">-Endpoint</span></span>
<span data-ttu-id="e1d97-147">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="e1d97-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="e1d97-148">這可以是 Webection URL，或是 EventHub、儲存佇列、混合式連接或 servicebusqueue 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1d97-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="e1d97-149">例如，混合式連接的資源識別碼採用下列形式：/subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/命名空間/[命名空間Name]/hybridConnections/[HybridConnectionName]。</span><span class="sxs-lookup"><span data-stu-id="e1d97-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="e1d97-150">執行任何事件格線 Cmdlet 之前，預期會建立目的端點並可供使用。</span><span class="sxs-lookup"><span data-stu-id="e1d97-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="e1d97-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e1d97-151">-EndpointType</span></span>
<span data-ttu-id="e1d97-152">端點類型。</span><span class="sxs-lookup"><span data-stu-id="e1d97-152">Endpoint Type.</span></span>
<span data-ttu-id="e1d97-153">這可以是 webection、eventhub、storagequeue、hybridconnection 或 servicebusqueue。</span><span class="sxs-lookup"><span data-stu-id="e1d97-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="e1d97-154">預設值為 web一。</span><span class="sxs-lookup"><span data-stu-id="e1d97-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="e1d97-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e1d97-155">-EventSubscriptionName</span></span>
<span data-ttu-id="e1d97-156">活動訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="e1d97-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="e1d97-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="e1d97-157">-EventTtl</span></span>
<span data-ttu-id="e1d97-158">活動傳遞的時間 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="e1d97-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="e1d97-159">此值必須介於 1 到 1440 之間</span><span class="sxs-lookup"><span data-stu-id="e1d97-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="e1d97-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="e1d97-160">-ExpirationDate</span></span>
<span data-ttu-id="e1d97-161">決定活動訂閱的到期日日期時間，活動訂閱將在之後淘汰。</span><span class="sxs-lookup"><span data-stu-id="e1d97-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="e1d97-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="e1d97-162">-IncludedEventType</span></span>
<span data-ttu-id="e1d97-163">指定要包含的事件種類清單的篩選。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="e1d97-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="e1d97-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1d97-164">-InputObject</span></span>
<span data-ttu-id="e1d97-165">EventGridSubscription 物件。</span><span class="sxs-lookup"><span data-stu-id="e1d97-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="e1d97-166">-標籤</span><span class="sxs-lookup"><span data-stu-id="e1d97-166">-Label</span></span>
<span data-ttu-id="e1d97-167">活動訂閱的標號</span><span class="sxs-lookup"><span data-stu-id="e1d97-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="e1d97-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="e1d97-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="e1d97-169">傳遞活動的嘗試次數上限。</span><span class="sxs-lookup"><span data-stu-id="e1d97-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="e1d97-170">此值必須介於 1 到 30 之間</span><span class="sxs-lookup"><span data-stu-id="e1d97-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="e1d97-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="e1d97-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="e1d97-172">批次中事件的數量上限。</span><span class="sxs-lookup"><span data-stu-id="e1d97-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="e1d97-173">此值必須介於 1 到 5000 之間。</span><span class="sxs-lookup"><span data-stu-id="e1d97-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="e1d97-174">此參數在 EnDPInt 類型為 Web一次時有效。</span><span class="sxs-lookup"><span data-stu-id="e1d97-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="e1d97-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="e1d97-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="e1d97-176">這是偏好的批次大小 ，以 KB 為單位。</span><span class="sxs-lookup"><span data-stu-id="e1d97-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="e1d97-177">此值必須介於 1 到 1024 之間。</span><span class="sxs-lookup"><span data-stu-id="e1d97-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="e1d97-178">此參數在 EnDPInt 類型為 Web一次時有效。</span><span class="sxs-lookup"><span data-stu-id="e1d97-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="e1d97-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d97-179">-ResourceGroupName</span></span>
<span data-ttu-id="e1d97-180">主題的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e1d97-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="e1d97-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1d97-181">-ResourceId</span></span>
<span data-ttu-id="e1d97-182">建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1d97-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="e1d97-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="e1d97-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="e1d97-184">指定只包含符合指定主題首碼的事件的篩選。</span><span class="sxs-lookup"><span data-stu-id="e1d97-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="e1d97-185">如果未指定，會包含具有所有主體首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="e1d97-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="e1d97-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="e1d97-186">-SubjectEndsWith</span></span>
<span data-ttu-id="e1d97-187">指定只包含符合指定主題尾碼的事件的篩選。</span><span class="sxs-lookup"><span data-stu-id="e1d97-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="e1d97-188">如果未指定，會包含具有所有主體尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="e1d97-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="e1d97-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e1d97-189">-TopicName</span></span>
<span data-ttu-id="e1d97-190">應建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d97-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e1d97-191">-確認</span><span class="sxs-lookup"><span data-stu-id="e1d97-191">-Confirm</span></span>
<span data-ttu-id="e1d97-192">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e1d97-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d97-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d97-193">-WhatIf</span></span>
<span data-ttu-id="e1d97-194">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1d97-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d97-195">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1d97-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d97-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d97-196">CommonParameters</span></span>
<span data-ttu-id="e1d97-197">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1d97-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d97-198">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1d97-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d97-199">輸入</span><span class="sxs-lookup"><span data-stu-id="e1d97-199">INPUTS</span></span>

### <span data-ttu-id="e1d97-200">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d97-200">System.String</span></span>

### <span data-ttu-id="e1d97-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d97-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e1d97-202">輸出</span><span class="sxs-lookup"><span data-stu-id="e1d97-202">OUTPUTS</span></span>

### <span data-ttu-id="e1d97-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e1d97-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e1d97-204">筆記</span><span class="sxs-lookup"><span data-stu-id="e1d97-204">NOTES</span></span>

## <span data-ttu-id="e1d97-205">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1d97-205">RELATED LINKS</span></span>
