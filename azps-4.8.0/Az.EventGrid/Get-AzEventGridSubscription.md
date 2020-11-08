---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128186"
---
# <span data-ttu-id="564cb-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="564cb-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="564cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="564cb-102">SYNOPSIS</span></span>
<span data-ttu-id="564cb-103">取得事件訂閱的詳細資料，或取得目前 Azure 訂閱中的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="564cb-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="564cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="564cb-104">SYNTAX</span></span>

### <span data-ttu-id="564cb-105">EventSubscriptionTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="564cb-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564cb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564cb-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564cb-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="564cb-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564cb-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564cb-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564cb-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="564cb-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="564cb-113">說明</span><span class="sxs-lookup"><span data-stu-id="564cb-113">DESCRIPTION</span></span>
<span data-ttu-id="564cb-114">Get-AzEventGridSubscription Cmdlet 會取得指定事件格線訂閱的詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="564cb-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="564cb-115">如果提供了事件訂閱名稱，則會傳回單一事件格線訂閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="564cb-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="564cb-116">如果未提供事件訂閱名稱，則會傳回所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="564cb-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="564cb-117">此清單中傳回的元素數目由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="564cb-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="564cb-118">如果未指定 Top 值或 $null，則清單將會包含所有事件訂閱專案。</span><span class="sxs-lookup"><span data-stu-id="564cb-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="564cb-119">否則，Top 會指出清單中要傳回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="564cb-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="564cb-120">如果仍有更多事件訂閱可用，則會在下一個呼叫中使用 NextLink 中的值，以取得事件訂閱的下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="564cb-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="564cb-121">最後，ODataQuery 參數是用來執行搜尋結果篩選。</span><span class="sxs-lookup"><span data-stu-id="564cb-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="564cb-122">篩選查詢遵循 OData 語法，只使用 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="564cb-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="564cb-123">支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="564cb-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="564cb-124">示例</span><span class="sxs-lookup"><span data-stu-id="564cb-124">EXAMPLES</span></span>

### <span data-ttu-id="564cb-125">範例1</span><span class="sxs-lookup"><span data-stu-id="564cb-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="564cb-126">取得 \` \` \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的 \` \` 事件訂閱 EventSubscription1 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="564cb-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="564cb-127">範例2</span><span class="sxs-lookup"><span data-stu-id="564cb-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="564cb-128">取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` \` \` ，包括完整的端點 URL （如果它是以 webhook 為基礎的事件訂閱）。</span><span class="sxs-lookup"><span data-stu-id="564cb-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="564cb-129">範例3</span><span class="sxs-lookup"><span data-stu-id="564cb-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="564cb-130">取得 \` \` 在沒有分頁的資源群組 MyResourceGroupName 中為主題 Topic1 所建立的所有事件訂閱清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="564cb-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="564cb-131">範例4</span><span class="sxs-lookup"><span data-stu-id="564cb-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-132">如果針對 \` \` 資源群組 \` MyResourceGroupName 中 \` 滿足 $odataFilter 查詢的主題 Topic1 建立任何) ，請列出前10個事件訂閱 (。</span><span class="sxs-lookup"><span data-stu-id="564cb-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-133">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-134">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-135">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="564cb-136">範例5</span><span class="sxs-lookup"><span data-stu-id="564cb-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="564cb-137">取得 \` \` 針對資源群組 MyResourceGroupName 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="564cb-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="564cb-138">範例6</span><span class="sxs-lookup"><span data-stu-id="564cb-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="564cb-139">取得 \` \` 目前所選 Azure 訂閱所建立之事件訂閱 EventSubscription1 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="564cb-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="564cb-140">範例7</span><span class="sxs-lookup"><span data-stu-id="564cb-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="564cb-141">取得在未分頁的資源群組 MyResourceGroupName 下所建立的所有全域事件訂閱清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="564cb-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="564cb-142">範例8</span><span class="sxs-lookup"><span data-stu-id="564cb-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-143">如果在 [資源群組 MyResourceGroupName] 下建立 \` \` 滿足 $odataFilter 查詢的任何) ，請列出前5個事件訂閱 (。</span><span class="sxs-lookup"><span data-stu-id="564cb-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-144">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-145">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-146">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="564cb-147">範例9</span><span class="sxs-lookup"><span data-stu-id="564cb-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="564cb-148">取得目前選取的 Azure 訂閱（不分頁）下所建立的所有全域事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="564cb-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="564cb-149">範例10</span><span class="sxs-lookup"><span data-stu-id="564cb-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-150">列出前15個全域事件訂閱 (如果在目前所選的 Azure 訂閱中建立的任何) 都符合 $odataFilter 查詢。</span><span class="sxs-lookup"><span data-stu-id="564cb-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-151">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-152">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-153">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="564cb-154">範例11</span><span class="sxs-lookup"><span data-stu-id="564cb-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="564cb-155">取得在 \` \` 未分頁的指定位置 westus2 中，在 [資源群組 MyResourceGroupName] 下所建立的所有區域事件訂閱清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="564cb-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="564cb-156">範例12</span><span class="sxs-lookup"><span data-stu-id="564cb-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-157">列出前15個地區性事件訂閱 (如果在 [資源群組] MyResourceGroupName 中建立的任何) \` \` \` \` ，都必須符合 $odataFilter 查詢的指定位置 westus2。</span><span class="sxs-lookup"><span data-stu-id="564cb-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-158">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-159">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-160">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="564cb-161">範例13</span><span class="sxs-lookup"><span data-stu-id="564cb-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="564cb-162">取得不需分頁的指定 EventHub 命名空間所建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="564cb-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="564cb-163">範例14</span><span class="sxs-lookup"><span data-stu-id="564cb-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-164">列出前25個事件訂閱 (如果針對指定的 EventHub 命名空間所建立的任何) （滿足 $odataFilter 查詢）。</span><span class="sxs-lookup"><span data-stu-id="564cb-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-165">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-166">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-167">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="564cb-168">範例15</span><span class="sxs-lookup"><span data-stu-id="564cb-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="564cb-169">取得在指定位置中針對指定的主題類型 (EventHub 命名空間) 中所建立之所有事件訂閱的清單（不需要分頁）。</span><span class="sxs-lookup"><span data-stu-id="564cb-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="564cb-170">範例16</span><span class="sxs-lookup"><span data-stu-id="564cb-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-171">清單前15個事件訂閱 (如果針對指定的主題類型建立的任何) ， (EventHub 命名空間) 于指定位置中，以滿足 $odataFilter 查詢。</span><span class="sxs-lookup"><span data-stu-id="564cb-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-172">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-173">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-174">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="564cb-175">範例17</span><span class="sxs-lookup"><span data-stu-id="564cb-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="564cb-176">取得針對特定資源群組（不分頁）所建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="564cb-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="564cb-177">範例18</span><span class="sxs-lookup"><span data-stu-id="564cb-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="564cb-178">列出第一個100事件訂閱 (如果針對滿足 $odataFilter 查詢的特定資源群組所建立的任何) 。</span><span class="sxs-lookup"><span data-stu-id="564cb-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="564cb-179">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="564cb-180">若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="564cb-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="564cb-181">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="564cb-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="564cb-182">參數</span><span class="sxs-lookup"><span data-stu-id="564cb-182">PARAMETERS</span></span>

### <span data-ttu-id="564cb-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564cb-183">-DefaultProfile</span></span>
<span data-ttu-id="564cb-184">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="564cb-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="564cb-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="564cb-185">-DomainInputObject</span></span>
<span data-ttu-id="564cb-186">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="564cb-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="564cb-187">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="564cb-187">-DomainName</span></span>
<span data-ttu-id="564cb-188">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="564cb-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="564cb-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="564cb-190">EventGrid [網域] 主題物件。</span><span class="sxs-lookup"><span data-stu-id="564cb-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="564cb-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="564cb-191">-DomainTopicName</span></span>
<span data-ttu-id="564cb-192">EventGrid [網域主題名稱]。</span><span class="sxs-lookup"><span data-stu-id="564cb-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="564cb-193">-EventSubscriptionName</span></span>
<span data-ttu-id="564cb-194">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="564cb-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="564cb-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="564cb-196">包含事件訂閱目的地的完整端點 URL。</span><span class="sxs-lookup"><span data-stu-id="564cb-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="564cb-197">-InputObject</span></span>
<span data-ttu-id="564cb-198">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="564cb-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="564cb-199">-位置</span><span class="sxs-lookup"><span data-stu-id="564cb-199">-Location</span></span>
<span data-ttu-id="564cb-200">位於</span><span class="sxs-lookup"><span data-stu-id="564cb-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="564cb-201">-NextLink</span></span>
<span data-ttu-id="564cb-202">要取得的下一頁資源連結。</span><span class="sxs-lookup"><span data-stu-id="564cb-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="564cb-203">當仍有更多資源可供查詢時，會使用第一個 Get-AzEventGrid Cmdlet 呼叫來取得此值。</span><span class="sxs-lookup"><span data-stu-id="564cb-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="564cb-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="564cb-204">-ODataQuery</span></span>
<span data-ttu-id="564cb-205">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="564cb-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="564cb-206">目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="564cb-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564cb-207">-ResourceGroupName</span></span>
<span data-ttu-id="564cb-208">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="564cb-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="564cb-209">-ResourceId</span></span>
<span data-ttu-id="564cb-210">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="564cb-210">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-211">-上方</span><span class="sxs-lookup"><span data-stu-id="564cb-211">-Top</span></span>
<span data-ttu-id="564cb-212">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="564cb-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="564cb-213">目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="564cb-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="564cb-214">-TopicName</span></span>
<span data-ttu-id="564cb-215">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="564cb-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="564cb-216">-TopicTypeName</span></span>
<span data-ttu-id="564cb-217">TopicType 名稱</span><span class="sxs-lookup"><span data-stu-id="564cb-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="564cb-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564cb-218">CommonParameters</span></span>
<span data-ttu-id="564cb-219">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="564cb-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564cb-220">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="564cb-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564cb-221">輸入</span><span class="sxs-lookup"><span data-stu-id="564cb-221">INPUTS</span></span>

### <span data-ttu-id="564cb-222">System.object</span><span class="sxs-lookup"><span data-stu-id="564cb-222">System.String</span></span>

### <span data-ttu-id="564cb-223">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="564cb-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="564cb-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="564cb-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="564cb-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="564cb-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="564cb-226">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="564cb-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="564cb-227">輸出</span><span class="sxs-lookup"><span data-stu-id="564cb-227">OUTPUTS</span></span>

### <span data-ttu-id="564cb-228">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="564cb-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="564cb-229">筆記</span><span class="sxs-lookup"><span data-stu-id="564cb-229">NOTES</span></span>

## <span data-ttu-id="564cb-230">相關連結</span><span class="sxs-lookup"><span data-stu-id="564cb-230">RELATED LINKS</span></span>
