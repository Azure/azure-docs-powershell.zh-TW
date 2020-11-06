---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448674"
---
# <span data-ttu-id="46522-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="46522-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="46522-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46522-102">SYNOPSIS</span></span>
<span data-ttu-id="46522-103">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="46522-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46522-104">句法</span><span class="sxs-lookup"><span data-stu-id="46522-104">SYNTAX</span></span>

### <span data-ttu-id="46522-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46522-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46522-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="46522-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46522-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46522-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46522-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="46522-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46522-109">說明</span><span class="sxs-lookup"><span data-stu-id="46522-109">DESCRIPTION</span></span>
<span data-ttu-id="46522-110">更新事件格線事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="46522-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="46522-111">這可以用來更新現有事件訂閱的篩選、目的地或標籤。</span><span class="sxs-lookup"><span data-stu-id="46522-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="46522-112">示例</span><span class="sxs-lookup"><span data-stu-id="46522-112">EXAMPLES</span></span>

### <span data-ttu-id="46522-113">範例1</span><span class="sxs-lookup"><span data-stu-id="46522-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="46522-114">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="46522-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="46522-115">範例2</span><span class="sxs-lookup"><span data-stu-id="46522-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="46522-116">更新 [ \` \` 資源群組 MyResourceGroupName] 中 [主題 Topic1] 的 [事件訂閱 ES1] 端點 \` \` \` \` ，以 \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="46522-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="46522-117">範例3</span><span class="sxs-lookup"><span data-stu-id="46522-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="46522-118">更新 EventHub namespace ContosoNamespace 的事件訂閱 \` ES1 的屬性，並將新的 [端點為] 與 \` \` https://requestb.in/1kxxoui1\ 新的 SubjectEndsWith 篩選為 \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="46522-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="46522-119">範例4</span><span class="sxs-lookup"><span data-stu-id="46522-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="46522-120">更新資源群組 MyResourceGroupName 的事件訂閱 ES1 的屬性， \` \` 新 \` 的 \` 標籤會 $labels。</span><span class="sxs-lookup"><span data-stu-id="46522-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="46522-121">參數</span><span class="sxs-lookup"><span data-stu-id="46522-121">PARAMETERS</span></span>

### <span data-ttu-id="46522-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46522-122">-DefaultProfile</span></span>
<span data-ttu-id="46522-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46522-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46522-124">-端點</span><span class="sxs-lookup"><span data-stu-id="46522-124">-Endpoint</span></span>
<span data-ttu-id="46522-125">事件訂閱目的地端點。</span><span class="sxs-lookup"><span data-stu-id="46522-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="46522-126">這可以是 webhook URL 或 EventHub 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46522-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46522-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="46522-127">-EndpointType</span></span>
<span data-ttu-id="46522-128">端點類型。</span><span class="sxs-lookup"><span data-stu-id="46522-128">Endpoint Type.</span></span>
<span data-ttu-id="46522-129">此可以是 webhook 或 eventhub</span><span class="sxs-lookup"><span data-stu-id="46522-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46522-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="46522-130">-EventSubscriptionName</span></span>
<span data-ttu-id="46522-131">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="46522-131">The name of the event subscription</span></span>

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

### <span data-ttu-id="46522-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="46522-132">-IncludedEventType</span></span>
<span data-ttu-id="46522-133">[篩選]：指定要包含的事件種類清單。如果未指定，將會包含所有事件種類。</span><span class="sxs-lookup"><span data-stu-id="46522-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46522-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46522-134">-InputObject</span></span>
<span data-ttu-id="46522-135">EventGridSubscription 物件。</span><span class="sxs-lookup"><span data-stu-id="46522-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46522-136">-標籤</span><span class="sxs-lookup"><span data-stu-id="46522-136">-Label</span></span>
<span data-ttu-id="46522-137">事件訂閱的標籤</span><span class="sxs-lookup"><span data-stu-id="46522-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46522-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46522-138">-ResourceGroupName</span></span>
<span data-ttu-id="46522-139">主題的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="46522-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46522-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46522-140">-ResourceId</span></span>
<span data-ttu-id="46522-141">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="46522-141">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="46522-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="46522-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="46522-143">[篩選] 指定只會包含符合指定 subject 首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="46522-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="46522-144">如果未指定，將會包含所有主語首碼的事件。</span><span class="sxs-lookup"><span data-stu-id="46522-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46522-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="46522-145">-SubjectEndsWith</span></span>
<span data-ttu-id="46522-146">[篩選] 指定只會包含符合指定 subject 尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="46522-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="46522-147">如果未指定，將會包含所有主語尾碼的事件。</span><span class="sxs-lookup"><span data-stu-id="46522-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46522-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="46522-148">-TopicName</span></span>
<span data-ttu-id="46522-149">要在其中建立事件訂閱的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="46522-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46522-150">-確認</span><span class="sxs-lookup"><span data-stu-id="46522-150">-Confirm</span></span>
<span data-ttu-id="46522-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46522-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46522-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46522-152">-WhatIf</span></span>
<span data-ttu-id="46522-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46522-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46522-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46522-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46522-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46522-155">CommonParameters</span></span>
<span data-ttu-id="46522-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46522-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46522-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46522-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46522-158">輸入</span><span class="sxs-lookup"><span data-stu-id="46522-158">INPUTS</span></span>

### <span data-ttu-id="46522-159">System.object</span><span class="sxs-lookup"><span data-stu-id="46522-159">System.String</span></span>
<span data-ttu-id="46522-160">PSEventSubscription System.object. EventGrid [] （String） []</span><span class="sxs-lookup"><span data-stu-id="46522-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="46522-161">輸出</span><span class="sxs-lookup"><span data-stu-id="46522-161">OUTPUTS</span></span>

### <span data-ttu-id="46522-162">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="46522-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="46522-163">筆記</span><span class="sxs-lookup"><span data-stu-id="46522-163">NOTES</span></span>

## <span data-ttu-id="46522-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="46522-164">RELATED LINKS</span></span>

