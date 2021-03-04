---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912013"
---
# <span data-ttu-id="7cc89-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7cc89-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="7cc89-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7cc89-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc89-103">獲得事件訂閱的詳細資訊，或獲得目前 Azure 訂閱中所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="7cc89-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="7cc89-104">語法</span><span class="sxs-lookup"><span data-stu-id="7cc89-104">SYNTAX</span></span>

### <span data-ttu-id="7cc89-105">EventSubscriptionTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7cc89-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc89-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc89-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc89-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cc89-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc89-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc89-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc89-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc89-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cc89-113">描述</span><span class="sxs-lookup"><span data-stu-id="7cc89-113">DESCRIPTION</span></span>
<span data-ttu-id="7cc89-114">此Get-AzEventGridSubscription Cmdlet 會獲得指定的事件格線訂閱詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="7cc89-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="7cc89-115">如果提供事件訂閱名稱，系統即會返回單一事件格線訂閱的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7cc89-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="7cc89-116">如果未提供事件訂閱名稱，會返回所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="7cc89-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="7cc89-117">此清單所返回的元素數目是由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="7cc89-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="7cc89-118">如果未指定頂端值或$null，清單會包含所有事件訂閱專案。</span><span class="sxs-lookup"><span data-stu-id="7cc89-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="7cc89-119">否則，Top 會指出清單中要返回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="7cc89-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="7cc89-120">如果仍有更多活動訂閱可用，則 NextLink 中的值應該用於下一個通話中，以取得活動訂閱的下一頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="7cc89-121">最後，ODataQuery 參數是用來執行搜尋結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="7cc89-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="7cc89-122">篩選查詢只會使用 Name 屬性遵循 OData 語法。</span><span class="sxs-lookup"><span data-stu-id="7cc89-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="7cc89-123">支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="7cc89-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="7cc89-124">例子</span><span class="sxs-lookup"><span data-stu-id="7cc89-124">EXAMPLES</span></span>

### <span data-ttu-id="7cc89-125">範例 1</span><span class="sxs-lookup"><span data-stu-id="7cc89-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7cc89-126">在資源群組 MyResourceGroupName 中，為 Topic1 建立的事件訂閱 \` \` \` \` \` EventSubscription1 詳細資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="7cc89-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7cc89-127">範例 2</span><span class="sxs-lookup"><span data-stu-id="7cc89-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="7cc89-128">在資源群組 \` \` \` \` \` MyResourceGroupName 中，針對主題主題 1 建立的事件訂閱 EventSubscription1 詳細資料，包括完整端點 URL ，如果它是 \` Web一型事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cc89-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="7cc89-129">範例 3</span><span class="sxs-lookup"><span data-stu-id="7cc89-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="7cc89-130">在資源群組 \` \` \` MyResourceGroupName 中取得為主題 1 建立的所有事件訂閱清單，而不 \` 分頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="7cc89-131">範例 4</span><span class="sxs-lookup"><span data-stu-id="7cc89-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-132">在資源群組 \` \` \` MyResourceGroupName) 中 (主題 1 建立的主題 1 時，列出前 10 個事件訂閱，$odataFilter \` 查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-133">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-134">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-135">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="7cc89-136">範例 5</span><span class="sxs-lookup"><span data-stu-id="7cc89-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7cc89-137">為資源群組 \` MyResourceGroupName 建立的事件訂閱 EventSubscription1 \` \` 詳細資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="7cc89-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7cc89-138">範例 6</span><span class="sxs-lookup"><span data-stu-id="7cc89-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7cc89-139">瞭解目前選取的 Azure 訂閱所建立的事件訂閱 \` EventSubscription1 \` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7cc89-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="7cc89-140">範例 7</span><span class="sxs-lookup"><span data-stu-id="7cc89-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="7cc89-141">在資源群組 MyResourceGroupName 下建立的所有全域事件訂閱清單，而不 \` \` 分頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="7cc89-142">範例 8</span><span class="sxs-lookup"><span data-stu-id="7cc89-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-143">如果資源群組 MyResourceGroupName (，請列出前 5 個事件訂閱，) 資源群組 MyResourceGroupName 下建立的任何專案，$odataFilter \` \` 查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-144">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-145">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-146">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="7cc89-147">範例 9</span><span class="sxs-lookup"><span data-stu-id="7cc89-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="7cc89-148">在目前選取的 Azure 訂閱下建立的所有全域事件訂閱清單，而不分頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="7cc89-149">範例 10</span><span class="sxs-lookup"><span data-stu-id="7cc89-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-150">列出前 15 個全域事件訂閱 (如果) 目前選取的 Azure 訂閱所建立的任何訂閱，$odataFilter查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-151">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-152">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-153">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="7cc89-154">範例 11</span><span class="sxs-lookup"><span data-stu-id="7cc89-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="7cc89-155">在指定的 westus2 資源群組 MyResourceGroupName 下建立的所有地區事件訂閱清單，而不 \` \` \` \` 分頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="7cc89-156">範例 12</span><span class="sxs-lookup"><span data-stu-id="7cc89-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-157">列出前 15 個區域事件訂閱 (如果資源群組 MyResourceGroupName) 于指定的位置 \` westus2 中建立，以滿足 $odataFilter \` \` \` 查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-158">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-159">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-160">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="7cc89-161">範例 13</span><span class="sxs-lookup"><span data-stu-id="7cc89-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="7cc89-162">獲得為指定的 EventHub 命名空間建立的所有事件訂閱清單，而不分頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="7cc89-163">範例 14</span><span class="sxs-lookup"><span data-stu-id="7cc89-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-164">如果為指定的 EventHub 命名空間建立 (，請) 前 25 個事件訂閱，$odataFilter查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-165">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-166">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-167">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="7cc89-168">範例 15</span><span class="sxs-lookup"><span data-stu-id="7cc89-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="7cc89-169">為指定的主題類型建立的所有事件訂閱清單， (EventHub 命名空間) 指定位置中，而不分頁。</span><span class="sxs-lookup"><span data-stu-id="7cc89-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="7cc89-170">範例 16</span><span class="sxs-lookup"><span data-stu-id="7cc89-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-171">在滿足 $odataFilter 查詢的指定位置中 () 為指定主題類型 (EventHub 命名空間) 建立的任何活動訂閱清單前 15 個事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cc89-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-172">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-173">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-174">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="7cc89-175">範例 17</span><span class="sxs-lookup"><span data-stu-id="7cc89-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="7cc89-176">無需分頁，即可獲得為特定資源群組建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="7cc89-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="7cc89-177">範例 18</span><span class="sxs-lookup"><span data-stu-id="7cc89-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="7cc89-178">針對滿足查詢的特定資源 (建立) ，請列出前 100 個$odataFilter訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cc89-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="7cc89-179">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="7cc89-180">為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="7cc89-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="7cc89-181">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="7cc89-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="7cc89-182">參數</span><span class="sxs-lookup"><span data-stu-id="7cc89-182">PARAMETERS</span></span>

### <span data-ttu-id="7cc89-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc89-183">-DefaultProfile</span></span>
<span data-ttu-id="7cc89-184">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7cc89-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc89-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="7cc89-185">-DomainInputObject</span></span>
<span data-ttu-id="7cc89-186">EventGrid 網域物件。</span><span class="sxs-lookup"><span data-stu-id="7cc89-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="7cc89-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="7cc89-187">-DomainName</span></span>
<span data-ttu-id="7cc89-188">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc89-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="7cc89-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="7cc89-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="7cc89-190">EventGrid 網域主題物件。</span><span class="sxs-lookup"><span data-stu-id="7cc89-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="7cc89-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="7cc89-191">-DomainTopicName</span></span>
<span data-ttu-id="7cc89-192">EventGrid 網域主題名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc89-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="7cc89-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7cc89-193">-EventSubscriptionName</span></span>
<span data-ttu-id="7cc89-194">活動訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="7cc89-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="7cc89-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="7cc89-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="7cc89-196">包含活動訂閱目的地的完整端點 URL。</span><span class="sxs-lookup"><span data-stu-id="7cc89-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="7cc89-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cc89-197">-InputObject</span></span>
<span data-ttu-id="7cc89-198">EventGrid Topic 物件。</span><span class="sxs-lookup"><span data-stu-id="7cc89-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7cc89-199">-位置</span><span class="sxs-lookup"><span data-stu-id="7cc89-199">-Location</span></span>
<span data-ttu-id="7cc89-200">位置</span><span class="sxs-lookup"><span data-stu-id="7cc89-200">Location</span></span>

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

### <span data-ttu-id="7cc89-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="7cc89-201">-NextLink</span></span>
<span data-ttu-id="7cc89-202">這是要取得之資源下一頁的連結。</span><span class="sxs-lookup"><span data-stu-id="7cc89-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="7cc89-203">當仍有更多資源可供查詢Get-AzEventGrid Cmdlet 呼叫時，會取得此值。</span><span class="sxs-lookup"><span data-stu-id="7cc89-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="7cc89-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7cc89-204">-ODataQuery</span></span>
<span data-ttu-id="7cc89-205">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="7cc89-206">目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="7cc89-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="7cc89-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc89-207">-ResourceGroupName</span></span>
<span data-ttu-id="7cc89-208">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7cc89-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="7cc89-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc89-209">-ResourceId</span></span>
<span data-ttu-id="7cc89-210">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7cc89-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="7cc89-211">-頂端</span><span class="sxs-lookup"><span data-stu-id="7cc89-211">-Top</span></span>
<span data-ttu-id="7cc89-212">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="7cc89-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="7cc89-213">目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="7cc89-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="7cc89-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7cc89-214">-TopicName</span></span>
<span data-ttu-id="7cc89-215">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc89-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="7cc89-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="7cc89-216">-TopicTypeName</span></span>
<span data-ttu-id="7cc89-217">TopicType 名稱</span><span class="sxs-lookup"><span data-stu-id="7cc89-217">TopicType name</span></span>

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

### <span data-ttu-id="7cc89-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc89-218">CommonParameters</span></span>
<span data-ttu-id="7cc89-219">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7cc89-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc89-220">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cc89-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc89-221">輸入</span><span class="sxs-lookup"><span data-stu-id="7cc89-221">INPUTS</span></span>

### <span data-ttu-id="7cc89-222">System.String</span><span class="sxs-lookup"><span data-stu-id="7cc89-222">System.String</span></span>

### <span data-ttu-id="7cc89-223">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="7cc89-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="7cc89-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="7cc89-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="7cc89-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7cc89-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="7cc89-226">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7cc89-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7cc89-227">輸出</span><span class="sxs-lookup"><span data-stu-id="7cc89-227">OUTPUTS</span></span>

### <span data-ttu-id="7cc89-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="7cc89-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="7cc89-229">筆記</span><span class="sxs-lookup"><span data-stu-id="7cc89-229">NOTES</span></span>

## <span data-ttu-id="7cc89-230">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cc89-230">RELATED LINKS</span></span>
