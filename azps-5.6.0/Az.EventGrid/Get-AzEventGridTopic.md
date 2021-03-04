---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2af8125f91618cd929a9389d9327532376e92af1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912005"
---
# <span data-ttu-id="87aa9-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="87aa9-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="87aa9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="87aa9-103">獲得事件格線主題的詳細資訊，或獲得目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="87aa9-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="87aa9-104">語法</span><span class="sxs-lookup"><span data-stu-id="87aa9-104">SYNTAX</span></span>

### <span data-ttu-id="87aa9-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="87aa9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87aa9-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87aa9-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87aa9-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="87aa9-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87aa9-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="87aa9-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87aa9-109">描述</span><span class="sxs-lookup"><span data-stu-id="87aa9-109">DESCRIPTION</span></span>
<span data-ttu-id="87aa9-110">此Get-AzEventGridTopic Cmdlet 會獲得指定事件格線主題的詳細資訊，或目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="87aa9-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="87aa9-111">如果提供主題名稱，則會返回單一事件格線主題的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="87aa9-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="87aa9-112">如果未提供主題名稱，會返回主題清單。</span><span class="sxs-lookup"><span data-stu-id="87aa9-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="87aa9-113">此清單所返回的元素數目是由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="87aa9-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="87aa9-114">如果未指定頂端值或$null，清單會包含所有主題專案。</span><span class="sxs-lookup"><span data-stu-id="87aa9-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="87aa9-115">否則，Top 會指出清單中要返回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="87aa9-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="87aa9-116">如果仍有更多主題可用，則 NextLink 中的值應該用於下一個通話中，以取得下一頁的主題。</span><span class="sxs-lookup"><span data-stu-id="87aa9-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="87aa9-117">最後，ODataQuery 參數是用來執行搜尋結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="87aa9-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="87aa9-118">篩選查詢只會使用 Name 屬性遵循 OData 語法。</span><span class="sxs-lookup"><span data-stu-id="87aa9-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="87aa9-119">支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="87aa9-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="87aa9-120">例子</span><span class="sxs-lookup"><span data-stu-id="87aa9-120">EXAMPLES</span></span>

### <span data-ttu-id="87aa9-121">範例 1</span><span class="sxs-lookup"><span data-stu-id="87aa9-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="87aa9-122">在資源群組 \` \` \` MyResourceGroupName 中，獲得事件格線主題 Topic1 的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="87aa9-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="87aa9-123">範例 2</span><span class="sxs-lookup"><span data-stu-id="87aa9-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="87aa9-124">在資源群組 \` \` \` MyResourceGroupName 中，獲得事件格線主題 Topic1 的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="87aa9-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="87aa9-125">範例 3</span><span class="sxs-lookup"><span data-stu-id="87aa9-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="87aa9-126">在資源群組 MyResourceGroupName 中列出所有事件格線主題， \` \` 而不分頁。</span><span class="sxs-lookup"><span data-stu-id="87aa9-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="87aa9-127">範例 4</span><span class="sxs-lookup"><span data-stu-id="87aa9-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="87aa9-128">在資源群組 MyResourceGroupName (，列出前 10 個事件格線主題) 滿足該查詢$odataFilter \` \` 主題。</span><span class="sxs-lookup"><span data-stu-id="87aa9-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="87aa9-129">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="87aa9-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="87aa9-130">為了取得下一頁 () ，使用者預期會重新撥打Get-AzEventGridTopic並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="87aa9-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="87aa9-131">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="87aa9-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="87aa9-132">範例 5</span><span class="sxs-lookup"><span data-stu-id="87aa9-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="87aa9-133">在訂閱中列出所有事件格線主題，而不分頁。</span><span class="sxs-lookup"><span data-stu-id="87aa9-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="87aa9-134">範例 6</span><span class="sxs-lookup"><span data-stu-id="87aa9-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="87aa9-135">如果訂閱中有任何符合 (查詢) ，請列出前 10 個事件格線主題$odataFilter主題。</span><span class="sxs-lookup"><span data-stu-id="87aa9-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="87aa9-136">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="87aa9-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="87aa9-137">為了取得下一頁 () ，使用者預期會重新撥打Get-AzEventGridTopic並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="87aa9-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="87aa9-138">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="87aa9-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="87aa9-139">參數</span><span class="sxs-lookup"><span data-stu-id="87aa9-139">PARAMETERS</span></span>

### <span data-ttu-id="87aa9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87aa9-140">-DefaultProfile</span></span>
<span data-ttu-id="87aa9-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="87aa9-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87aa9-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="87aa9-142">-Name</span></span>
<span data-ttu-id="87aa9-143">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="87aa9-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87aa9-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="87aa9-144">-NextLink</span></span>
<span data-ttu-id="87aa9-145">這是要取得之資源下一頁的連結。</span><span class="sxs-lookup"><span data-stu-id="87aa9-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="87aa9-146">當仍有更多資源可供查詢Get-AzEventGrid Cmdlet 呼叫時，會取得此值。</span><span class="sxs-lookup"><span data-stu-id="87aa9-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87aa9-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="87aa9-147">-ODataQuery</span></span>
<span data-ttu-id="87aa9-148">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="87aa9-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="87aa9-149">目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="87aa9-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87aa9-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87aa9-150">-ResourceGroupName</span></span>
<span data-ttu-id="87aa9-151">資源組名。</span><span class="sxs-lookup"><span data-stu-id="87aa9-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87aa9-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87aa9-152">-ResourceId</span></span>
<span data-ttu-id="87aa9-153">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="87aa9-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="87aa9-154">-頂端</span><span class="sxs-lookup"><span data-stu-id="87aa9-154">-Top</span></span>
<span data-ttu-id="87aa9-155">要取得的資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="87aa9-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="87aa9-156">有效的值介於 1 到 100 之間。</span><span class="sxs-lookup"><span data-stu-id="87aa9-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="87aa9-157">如果已指定頂端值，且仍有更多結果可用，則結果會包含下一頁的連結，可在 NextLink 中查詢。</span><span class="sxs-lookup"><span data-stu-id="87aa9-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="87aa9-158">如果未指定 Top 值，將會一次返回完整的資源清單。</span><span class="sxs-lookup"><span data-stu-id="87aa9-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87aa9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87aa9-159">CommonParameters</span></span>
<span data-ttu-id="87aa9-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87aa9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87aa9-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87aa9-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87aa9-162">輸入</span><span class="sxs-lookup"><span data-stu-id="87aa9-162">INPUTS</span></span>

### <span data-ttu-id="87aa9-163">System.String</span><span class="sxs-lookup"><span data-stu-id="87aa9-163">System.String</span></span>

### <span data-ttu-id="87aa9-164">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="87aa9-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="87aa9-165">輸出</span><span class="sxs-lookup"><span data-stu-id="87aa9-165">OUTPUTS</span></span>

### <span data-ttu-id="87aa9-166">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="87aa9-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="87aa9-167">Microsoft.Azure.Commands.EventGrid.models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="87aa9-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="87aa9-168">筆記</span><span class="sxs-lookup"><span data-stu-id="87aa9-168">NOTES</span></span>

## <span data-ttu-id="87aa9-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="87aa9-169">RELATED LINKS</span></span>
