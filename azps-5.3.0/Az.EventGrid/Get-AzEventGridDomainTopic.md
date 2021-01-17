---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286244"
---
# <span data-ttu-id="378c5-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="378c5-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="378c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="378c5-102">SYNOPSIS</span></span>
<span data-ttu-id="378c5-103">取得事件 Grid 網域主題的詳細資料，或取得目前 Azure 訂閱中特定事件 Grid 網域底下的所有事件網格域主題清單。</span><span class="sxs-lookup"><span data-stu-id="378c5-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="378c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="378c5-104">SYNTAX</span></span>

### <span data-ttu-id="378c5-105">DomainTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="378c5-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="378c5-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="378c5-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="378c5-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="378c5-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="378c5-108">說明</span><span class="sxs-lookup"><span data-stu-id="378c5-108">DESCRIPTION</span></span>
<span data-ttu-id="378c5-109">Get-AzEventGridDomainTopic Cmdlet 會取得指定事件 Grid 網域主題的詳細資料，或目前 Azure 訂閱中特定網域下所有事件網格域主題的清單。</span><span class="sxs-lookup"><span data-stu-id="378c5-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="378c5-110">如果提供網域主題名稱，則會傳回單一事件 Grid 網域主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="378c5-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="378c5-111">如果未提供網域主題名稱，則會傳回指定功能變數名稱下的網域主題清單。</span><span class="sxs-lookup"><span data-stu-id="378c5-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="378c5-112">此清單中傳回的元素數目由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="378c5-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="378c5-113">如果未指定 Top 值或 $null，則清單將會包含所有網域主題專案。</span><span class="sxs-lookup"><span data-stu-id="378c5-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="378c5-114">否則，Top 會指出清單中要傳回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="378c5-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="378c5-115">如果仍有更多網域主題可供使用，則會在下一個呼叫中使用 NextLink 中的值，以取得網域主題的下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="378c5-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="378c5-116">最後，ODataQuery 參數是用來執行搜尋結果篩選。</span><span class="sxs-lookup"><span data-stu-id="378c5-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="378c5-117">篩選查詢遵循 OData 語法，只使用 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="378c5-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="378c5-118">支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="378c5-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="378c5-119">示例</span><span class="sxs-lookup"><span data-stu-id="378c5-119">EXAMPLES</span></span>

### <span data-ttu-id="378c5-120">範例1</span><span class="sxs-lookup"><span data-stu-id="378c5-120">Example 1</span></span>

<span data-ttu-id="378c5-121">取得 [ \` \` \` \` 資源群組 MyResourceGroupName] 中事件 grid 網域 Domain1 底下 \` 的事件網格網域主題 DomainTopic1 的詳細資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="378c5-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="378c5-122">範例2</span><span class="sxs-lookup"><span data-stu-id="378c5-122">Example 2</span></span>

<span data-ttu-id="378c5-123">取得事件格線的詳細資料 \` DomainTopic1 [ \` 資源群組 MyResourceGroupName] 中的 [事件格線網域 Domain1] 底下， \` \` \` \` 使用 [ResourceId] 選項。</span><span class="sxs-lookup"><span data-stu-id="378c5-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="378c5-124">範例3</span><span class="sxs-lookup"><span data-stu-id="378c5-124">Example 3</span></span>

<span data-ttu-id="378c5-125">列出 [事件格線 Domain1] 底下的 [事件格線網域] 主題在 [ \` \` 資源群組 MyResourceGroupName] 中， \` \` 沒有分頁 (所有的結果都會以一個快照) 傳回。</span><span class="sxs-lookup"><span data-stu-id="378c5-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="378c5-126">範例4</span><span class="sxs-lookup"><span data-stu-id="378c5-126">Example 4</span></span>

<span data-ttu-id="378c5-127">列出 [事件格線 Domain1] 底下的 [事件格線網域] 主題 [ \` \` 資源群組 \` \`)  (MyResourceGroupName]</span><span class="sxs-lookup"><span data-stu-id="378c5-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="378c5-128">範例5</span><span class="sxs-lookup"><span data-stu-id="378c5-128">Example 5</span></span>

<span data-ttu-id="378c5-129">列出事件格線的主題 (如果資源群組 MyResourceGroupName 中的 [網域 Domain1] 下是否有任何) \` \` \` \` ，且符合 $odataFilter 查詢10個網域主題一次。</span><span class="sxs-lookup"><span data-stu-id="378c5-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="378c5-130">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="378c5-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="378c5-131">若要取得下一頁 (s) 的網域主題，使用者應該重新呼叫 Get-AzEventGridDomainTopic 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="378c5-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="378c5-132">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="378c5-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="378c5-133">參數</span><span class="sxs-lookup"><span data-stu-id="378c5-133">PARAMETERS</span></span>

### <span data-ttu-id="378c5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378c5-134">-DefaultProfile</span></span>
<span data-ttu-id="378c5-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="378c5-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="378c5-136">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="378c5-136">-DomainName</span></span>
<span data-ttu-id="378c5-137">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="378c5-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378c5-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="378c5-138">-Name</span></span>
<span data-ttu-id="378c5-139">EventGrid [網域主題名稱]。</span><span class="sxs-lookup"><span data-stu-id="378c5-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378c5-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="378c5-140">-NextLink</span></span>
<span data-ttu-id="378c5-141">要取得的下一頁資源連結。</span><span class="sxs-lookup"><span data-stu-id="378c5-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="378c5-142">當仍有更多資源可供查詢時，會使用第一個 Get-AzEventGrid Cmdlet 呼叫來取得此值。</span><span class="sxs-lookup"><span data-stu-id="378c5-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="378c5-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="378c5-143">-ODataQuery</span></span>
<span data-ttu-id="378c5-144">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="378c5-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="378c5-145">目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="378c5-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378c5-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378c5-146">-ResourceGroupName</span></span>
<span data-ttu-id="378c5-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="378c5-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378c5-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="378c5-148">-ResourceId</span></span>
<span data-ttu-id="378c5-149">代表事件 Grid 網域或 Grid 網域的資源識別碼主題。</span><span class="sxs-lookup"><span data-stu-id="378c5-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378c5-150">-上方</span><span class="sxs-lookup"><span data-stu-id="378c5-150">-Top</span></span>
<span data-ttu-id="378c5-151">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="378c5-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="378c5-152">目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="378c5-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378c5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378c5-153">CommonParameters</span></span>
<span data-ttu-id="378c5-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="378c5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378c5-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="378c5-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378c5-156">輸入</span><span class="sxs-lookup"><span data-stu-id="378c5-156">INPUTS</span></span>

### <span data-ttu-id="378c5-157">System.object</span><span class="sxs-lookup"><span data-stu-id="378c5-157">System.String</span></span>

### <span data-ttu-id="378c5-158">System.object</span><span class="sxs-lookup"><span data-stu-id="378c5-158">System.Int32</span></span>

## <span data-ttu-id="378c5-159">輸出</span><span class="sxs-lookup"><span data-stu-id="378c5-159">OUTPUTS</span></span>

### <span data-ttu-id="378c5-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="378c5-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="378c5-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="378c5-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="378c5-162">筆記</span><span class="sxs-lookup"><span data-stu-id="378c5-162">NOTES</span></span>

## <span data-ttu-id="378c5-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="378c5-163">RELATED LINKS</span></span>
