---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435164"
---
# <span data-ttu-id="e2a52-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e2a52-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="e2a52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2a52-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a52-103">取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="e2a52-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="e2a52-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2a52-104">SYNTAX</span></span>

### <span data-ttu-id="e2a52-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e2a52-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2a52-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a52-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2a52-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a52-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2a52-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a52-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2a52-109">說明</span><span class="sxs-lookup"><span data-stu-id="e2a52-109">DESCRIPTION</span></span>
<span data-ttu-id="e2a52-110">Get-AzEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="e2a52-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="e2a52-111">如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e2a52-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="e2a52-112">如果未提供主題名稱，則會傳回主題的清單。</span><span class="sxs-lookup"><span data-stu-id="e2a52-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="e2a52-113">此清單中傳回的元素數目由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="e2a52-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="e2a52-114">如果未指定 Top 值或 $null，則清單將會包含所有主題專案。</span><span class="sxs-lookup"><span data-stu-id="e2a52-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="e2a52-115">否則，Top 會指出清單中要傳回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="e2a52-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="e2a52-116">如果仍有更多主題可供使用，則會在下一個呼叫中使用 NextLink 中的值，以取得下一個主題頁面。</span><span class="sxs-lookup"><span data-stu-id="e2a52-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="e2a52-117">最後，ODataQuery 參數是用來執行搜尋結果篩選。</span><span class="sxs-lookup"><span data-stu-id="e2a52-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="e2a52-118">篩選查詢遵循 OData 語法，只使用 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2a52-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="e2a52-119">支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="e2a52-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="e2a52-120">示例</span><span class="sxs-lookup"><span data-stu-id="e2a52-120">EXAMPLES</span></span>

### <span data-ttu-id="e2a52-121">範例1</span><span class="sxs-lookup"><span data-stu-id="e2a52-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e2a52-122">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="e2a52-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e2a52-123">範例2</span><span class="sxs-lookup"><span data-stu-id="e2a52-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="e2a52-124">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="e2a52-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e2a52-125">範例3</span><span class="sxs-lookup"><span data-stu-id="e2a52-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="e2a52-126">列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題（ \` \` 無分頁）。</span><span class="sxs-lookup"><span data-stu-id="e2a52-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="e2a52-127">範例4</span><span class="sxs-lookup"><span data-stu-id="e2a52-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="e2a52-128">如果資源群組 MyResourceGroupName 中有任何 \` \` 滿足 $odataFilter 查詢的) ，請列出前10個事件格線 (主題。</span><span class="sxs-lookup"><span data-stu-id="e2a52-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="e2a52-129">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="e2a52-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="e2a52-130">若要取得下一頁 (的主題) ，使用者應該重新呼叫 Get-AzEventGridTopic 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="e2a52-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="e2a52-131">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="e2a52-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="e2a52-132">範例5</span><span class="sxs-lookup"><span data-stu-id="e2a52-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="e2a52-133">在不分頁的情況下，列出訂閱中的所有事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="e2a52-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="e2a52-134">範例6</span><span class="sxs-lookup"><span data-stu-id="e2a52-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="e2a52-135">如果訂閱中有任何滿足 $odataFilter 查詢的) ，請列出前10個事件格線主題 (。</span><span class="sxs-lookup"><span data-stu-id="e2a52-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="e2a52-136">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="e2a52-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="e2a52-137">若要取得下一頁 (的主題) ，使用者應該重新呼叫 Get-AzEventGridTopic 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="e2a52-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="e2a52-138">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="e2a52-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="e2a52-139">參數</span><span class="sxs-lookup"><span data-stu-id="e2a52-139">PARAMETERS</span></span>

### <span data-ttu-id="e2a52-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a52-140">-DefaultProfile</span></span>
<span data-ttu-id="e2a52-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e2a52-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2a52-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2a52-142">-Name</span></span>
<span data-ttu-id="e2a52-143">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="e2a52-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="e2a52-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="e2a52-144">-NextLink</span></span>
<span data-ttu-id="e2a52-145">要取得的下一頁資源連結。</span><span class="sxs-lookup"><span data-stu-id="e2a52-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="e2a52-146">當仍有更多資源可供查詢時，會使用第一個 Get-AzEventGrid Cmdlet 呼叫來取得此值。</span><span class="sxs-lookup"><span data-stu-id="e2a52-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="e2a52-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e2a52-147">-ODataQuery</span></span>
<span data-ttu-id="e2a52-148">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="e2a52-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="e2a52-149">目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="e2a52-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="e2a52-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a52-150">-ResourceGroupName</span></span>
<span data-ttu-id="e2a52-151">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e2a52-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2a52-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2a52-152">-ResourceId</span></span>
<span data-ttu-id="e2a52-153">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2a52-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="e2a52-154">-上方</span><span class="sxs-lookup"><span data-stu-id="e2a52-154">-Top</span></span>
<span data-ttu-id="e2a52-155">要取得的資源數目上限。</span><span class="sxs-lookup"><span data-stu-id="e2a52-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="e2a52-156">有效值介於1到100。</span><span class="sxs-lookup"><span data-stu-id="e2a52-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="e2a52-157">如果已指定 top 值，但仍有更多結果，結果將會包含下一個頁面的連結，以在 NextLink 中查詢。</span><span class="sxs-lookup"><span data-stu-id="e2a52-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="e2a52-158">如果未指定 Top 值，就會一次傳回完整的資源清單。</span><span class="sxs-lookup"><span data-stu-id="e2a52-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="e2a52-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a52-159">CommonParameters</span></span>
<span data-ttu-id="e2a52-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2a52-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a52-161">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2a52-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a52-162">輸入</span><span class="sxs-lookup"><span data-stu-id="e2a52-162">INPUTS</span></span>

### <span data-ttu-id="e2a52-163">System.object</span><span class="sxs-lookup"><span data-stu-id="e2a52-163">System.String</span></span>

### <span data-ttu-id="e2a52-164">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e2a52-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e2a52-165">輸出</span><span class="sxs-lookup"><span data-stu-id="e2a52-165">OUTPUTS</span></span>

### <span data-ttu-id="e2a52-166">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="e2a52-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="e2a52-167">PSTopicListInstance 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="e2a52-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="e2a52-168">筆記</span><span class="sxs-lookup"><span data-stu-id="e2a52-168">NOTES</span></span>

## <span data-ttu-id="e2a52-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2a52-169">RELATED LINKS</span></span>
