---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: 0c5c0f0f9739a2f9481989a69ece9aa29f0c67e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451512"
---
# <span data-ttu-id="0a7cd-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a7cd-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="0a7cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7cd-103">針對主題、Azure 資源、Azure 訂閱或資源群組建立新的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a7cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a7cd-104">SYNTAX</span></span>

### <span data-ttu-id="0a7cd-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0a7cd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a7cd-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a7cd-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a7cd-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0a7cd-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a7cd-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a7cd-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a7cd-109">說明</span><span class="sxs-lookup"><span data-stu-id="0a7cd-109">DESCRIPTION</span></span>
<span data-ttu-id="0a7cd-110">建立 Azure 事件格線主題（支援的 Azure 資源、Azure 訂閱或資源群組）的新事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="0a7cd-111">若要建立目前所選 Azure 訂閱的事件訂閱，請指定事件訂閱名稱和目標端點。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0a7cd-112">若要建立資源群組的事件訂閱，除了事件訂閱名稱和目的地端點之外，還可以指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0a7cd-113">若要建立 Azure 事件格線主題的事件訂閱，請同時指定主題名稱。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="0a7cd-114">若要建立支援的 Azure 資源的事件訂閱，請指定資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="0a7cd-115">若要查看受支援類型的清單，請執行 Get-AzureRmEventGridTopicType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="0a7cd-116">示例</span><span class="sxs-lookup"><span data-stu-id="0a7cd-116">EXAMPLES</span></span>

### <span data-ttu-id="0a7cd-117">範例1</span><span class="sxs-lookup"><span data-stu-id="0a7cd-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0a7cd-118">\` \` \` \` \` \` 使用 webhook 目的地端點在資源群組 MyResourceGroupName 中 Topic1 Azure 事件格線主題建立新的事件訂閱 EventSubscription1 https://requestb.in/19qlscd1 。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0a7cd-119">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0a7cd-120">範例2</span><span class="sxs-lookup"><span data-stu-id="0a7cd-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0a7cd-121">\` \` \` \` 使用 webhook 目的地端點的資源群組 MyResourceGroupName 建立新的事件訂閱 EventSubscription1 https://requestb.in/19qlscd1 。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0a7cd-122">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0a7cd-123">範例3</span><span class="sxs-lookup"><span data-stu-id="0a7cd-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0a7cd-124">\` \` 使用 webhook 目的地端點，為目前選取的 Azure 訂閱建立新的事件訂閱 EventSubscription1 https://requestb.in/19qlscd1 。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0a7cd-125">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0a7cd-126">範例4</span><span class="sxs-lookup"><span data-stu-id="0a7cd-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="0a7cd-127">\` \` 使用 webhook 目的地端點，為目前選取的 Azure 訂閱建立新的事件訂閱 EventSubscription1 https://requestb.in/19qlscd1 。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0a7cd-128">這個事件訂閱會指定事件種類和主旨的其他篩選，只有符合這些篩選準則的事件才會傳送到目的地端點。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="0a7cd-129">範例5</span><span class="sxs-lookup"><span data-stu-id="0a7cd-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="0a7cd-130">在目前選取的 Azure 訂閱中建立新的事件訂閱 \` EventSubscription1， \` 並將指定的事件中樞做為事件的目的地。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="0a7cd-131">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0a7cd-132">範例6</span><span class="sxs-lookup"><span data-stu-id="0a7cd-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0a7cd-133">建立一個新的事件訂閱 \` EventSubscription1 \` 至 EventHub 命名空間，具有指定的 webhhok 目標端點 https://requestb.in/19qlscd1 。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0a7cd-134">這個事件訂閱使用預設篩選器。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="0a7cd-135">參數</span><span class="sxs-lookup"><span data-stu-id="0a7cd-135">PARAMETERS</span></span>

### <span data-ttu-id="0a7cd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7cd-136">-DefaultProfile</span></span>
<span data-ttu-id="0a7cd-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0a7cd-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-138">-端點</span><span class="sxs-lookup"><span data-stu-id="0a7cd-138">-Endpoint</span></span>
<span data-ttu-id="0a7cd-139">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-139">Event subscription destination endpoint.</span></span>
<span data-ttu-id="0a7cd-140">這可以是 webhook URL 或 EventHub 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-140">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-141">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0a7cd-141">-EndpointType</span></span>
<span data-ttu-id="0a7cd-142">端點類型。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-142">Endpoint Type.</span></span>
<span data-ttu-id="0a7cd-143">此可以是 webhook 或 eventhub</span><span class="sxs-lookup"><span data-stu-id="0a7cd-143">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-144">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0a7cd-144">-EventSubscriptionName</span></span>
<span data-ttu-id="0a7cd-145">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="0a7cd-145">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-146">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="0a7cd-146">-IncludedEventType</span></span>
<span data-ttu-id="0a7cd-147">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-147">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a7cd-148">-InputObject</span></span>
<span data-ttu-id="0a7cd-149">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-149">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-150">-標籤</span><span class="sxs-lookup"><span data-stu-id="0a7cd-150">-Label</span></span>
<span data-ttu-id="0a7cd-151">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="0a7cd-151">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a7cd-152">-ResourceGroupName</span></span>
<span data-ttu-id="0a7cd-153">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-153">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a7cd-154">-ResourceId</span></span>
<span data-ttu-id="0a7cd-155">要建立事件訂閱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-155">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-156">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0a7cd-156">-SubjectBeginsWith</span></span>
<span data-ttu-id="0a7cd-157">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-157">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="0a7cd-158">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-158">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-159">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="0a7cd-159">-SubjectCaseSensitive</span></span>
<span data-ttu-id="0a7cd-160">指定 [subject] 欄位應在區分大小寫的方式下進行比較的篩選。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-160">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="0a7cd-161">如果沒有指定，則會以不區分大小寫的方式來比較主語。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-161">If not specified, subject will be compared in a case insensitive manner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-162">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="0a7cd-162">-SubjectEndsWith</span></span>
<span data-ttu-id="0a7cd-163">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-163">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="0a7cd-164">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-164">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0a7cd-165">-TopicName</span></span>
<span data-ttu-id="0a7cd-166">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-166">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-167">-確認</span><span class="sxs-lookup"><span data-stu-id="0a7cd-167">-Confirm</span></span>
<span data-ttu-id="0a7cd-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a7cd-169">-WhatIf</span></span>
<span data-ttu-id="0a7cd-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a7cd-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7cd-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7cd-172">CommonParameters</span></span>
<span data-ttu-id="0a7cd-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7cd-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7cd-175">輸入</span><span class="sxs-lookup"><span data-stu-id="0a7cd-175">INPUTS</span></span>

### <span data-ttu-id="0a7cd-176">System.object</span><span class="sxs-lookup"><span data-stu-id="0a7cd-176">System.String</span></span>
<span data-ttu-id="0a7cd-177">PSTopic EventGrid. SwitchParameter. String [] （）. 字串 []</span><span class="sxs-lookup"><span data-stu-id="0a7cd-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="0a7cd-178">輸出</span><span class="sxs-lookup"><span data-stu-id="0a7cd-178">OUTPUTS</span></span>

### <span data-ttu-id="0a7cd-179">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="0a7cd-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0a7cd-180">筆記</span><span class="sxs-lookup"><span data-stu-id="0a7cd-180">NOTES</span></span>

## <span data-ttu-id="0a7cd-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a7cd-181">RELATED LINKS</span></span>

