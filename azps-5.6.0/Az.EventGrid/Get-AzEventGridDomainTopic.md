---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 053c9a503b6cb7d3833d214208ae7fe6bd60fe45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910097"
---
# <span data-ttu-id="884ee-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="884ee-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="884ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="884ee-102">SYNOPSIS</span></span>
<span data-ttu-id="884ee-103">獲得事件格線網域主題的詳細資訊，或在目前 Azure 訂閱中特定事件格線網域下，獲得所有事件格線網域主題的清單。</span><span class="sxs-lookup"><span data-stu-id="884ee-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="884ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="884ee-104">SYNTAX</span></span>

### <span data-ttu-id="884ee-105">DomainTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="884ee-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="884ee-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="884ee-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="884ee-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="884ee-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="884ee-108">描述</span><span class="sxs-lookup"><span data-stu-id="884ee-108">DESCRIPTION</span></span>
<span data-ttu-id="884ee-109">此Get-AzEventGridDomainTopic Cmdlet 會獲得指定事件格線網域主題的詳細資訊，或目前 Azure 訂閱中特定網域下的所有事件格線網域主題清單。</span><span class="sxs-lookup"><span data-stu-id="884ee-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="884ee-110">如果提供網域主題名稱，則系統會返回單一事件格線網域主題的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="884ee-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="884ee-111">如果未提供網域主題名稱，則會返回指定功能變數名稱下的網域主題清單。</span><span class="sxs-lookup"><span data-stu-id="884ee-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="884ee-112">此清單所返回的元素數目是由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="884ee-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="884ee-113">如果未指定頂端值或$null，清單會包含所有網域主題專案。</span><span class="sxs-lookup"><span data-stu-id="884ee-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="884ee-114">否則，Top 會指出清單中要返回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="884ee-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="884ee-115">如果仍然可以使用更多網域主題，則下一個通話應該會使用 NextLink 中的值，以取得網域主題的下一頁。</span><span class="sxs-lookup"><span data-stu-id="884ee-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="884ee-116">最後，ODataQuery 參數是用來執行搜尋結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="884ee-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="884ee-117">篩選查詢只會使用 Name 屬性遵循 OData 語法。</span><span class="sxs-lookup"><span data-stu-id="884ee-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="884ee-118">支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="884ee-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="884ee-119">例子</span><span class="sxs-lookup"><span data-stu-id="884ee-119">EXAMPLES</span></span>

### <span data-ttu-id="884ee-120">範例 1</span><span class="sxs-lookup"><span data-stu-id="884ee-120">Example 1</span></span>

<span data-ttu-id="884ee-121">在資源群組 MyResourceGroupName 的 Event Grid 網域網域1 下，獲得 Event Grid 網域主題 \` \` \` \` \` DomainTopic1 的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="884ee-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="884ee-122">範例 2</span><span class="sxs-lookup"><span data-stu-id="884ee-122">Example 2</span></span>

<span data-ttu-id="884ee-123">使用 ResourceId 選項，在資源群組 MyResourceGroupName 的 Event Grid 網域1 下，獲得 Event Grid 網域主題 \` \` \` \` \` \` DomainTopic1 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="884ee-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="884ee-124">範例 3</span><span class="sxs-lookup"><span data-stu-id="884ee-124">Example 3</span></span>

<span data-ttu-id="884ee-125">在資源群組 \` \` \` MyResourceGroupName 中，在事件格線網域 1 下列出所有事件格線網域主題，而不分頁 (所有結果會以單一快照 \`) 。</span><span class="sxs-lookup"><span data-stu-id="884ee-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="884ee-126">範例 4</span><span class="sxs-lookup"><span data-stu-id="884ee-126">Example 4</span></span>

<span data-ttu-id="884ee-127">在資源群組 \` \` \` MyResourceGroupName 中，在事件格線網域網域1 下列出所有事件格線網域主題，而不分頁 (所有結果會使用 ResourceId 選項) 一次 \` 返回</span><span class="sxs-lookup"><span data-stu-id="884ee-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="884ee-128">範例 5</span><span class="sxs-lookup"><span data-stu-id="884ee-128">Example 5</span></span>

<span data-ttu-id="884ee-129">在資源群組 \` \` MyResourceGroupName () Domain Domain1 下，列出事件格線網域主題$odataFilter同時滿足 $odataFilter 查詢 10 個網域 \` \` 主題。</span><span class="sxs-lookup"><span data-stu-id="884ee-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="884ee-130">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="884ee-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="884ee-131">為了取得網域 (頁面) ，使用者預期會重新撥打Get-AzEventGridDomainTopic並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="884ee-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="884ee-132">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="884ee-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="884ee-133">參數</span><span class="sxs-lookup"><span data-stu-id="884ee-133">PARAMETERS</span></span>

### <span data-ttu-id="884ee-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884ee-134">-DefaultProfile</span></span>
<span data-ttu-id="884ee-135">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="884ee-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884ee-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="884ee-136">-DomainName</span></span>
<span data-ttu-id="884ee-137">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="884ee-137">EventGrid domain name.</span></span>

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

### <span data-ttu-id="884ee-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="884ee-138">-Name</span></span>
<span data-ttu-id="884ee-139">EventGrid 網域主題名稱。</span><span class="sxs-lookup"><span data-stu-id="884ee-139">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="884ee-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="884ee-140">-NextLink</span></span>
<span data-ttu-id="884ee-141">這是要取得之資源下一頁的連結。</span><span class="sxs-lookup"><span data-stu-id="884ee-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="884ee-142">當仍有更多資源可供查詢Get-AzEventGrid Cmdlet 呼叫時，會取得此值。</span><span class="sxs-lookup"><span data-stu-id="884ee-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="884ee-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="884ee-143">-ODataQuery</span></span>
<span data-ttu-id="884ee-144">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="884ee-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="884ee-145">目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="884ee-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="884ee-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884ee-146">-ResourceGroupName</span></span>
<span data-ttu-id="884ee-147">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="884ee-147">The name of the resource group.</span></span>

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

### <span data-ttu-id="884ee-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="884ee-148">-ResourceId</span></span>
<span data-ttu-id="884ee-149">代表事件格線網域或格線網域主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="884ee-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="884ee-150">-頂端</span><span class="sxs-lookup"><span data-stu-id="884ee-150">-Top</span></span>
<span data-ttu-id="884ee-151">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="884ee-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="884ee-152">目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="884ee-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="884ee-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884ee-153">CommonParameters</span></span>
<span data-ttu-id="884ee-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="884ee-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884ee-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="884ee-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884ee-156">輸入</span><span class="sxs-lookup"><span data-stu-id="884ee-156">INPUTS</span></span>

### <span data-ttu-id="884ee-157">System.String</span><span class="sxs-lookup"><span data-stu-id="884ee-157">System.String</span></span>

### <span data-ttu-id="884ee-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="884ee-158">System.Int32</span></span>

## <span data-ttu-id="884ee-159">輸出</span><span class="sxs-lookup"><span data-stu-id="884ee-159">OUTPUTS</span></span>

### <span data-ttu-id="884ee-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="884ee-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="884ee-161">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="884ee-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="884ee-162">筆記</span><span class="sxs-lookup"><span data-stu-id="884ee-162">NOTES</span></span>

## <span data-ttu-id="884ee-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="884ee-163">RELATED LINKS</span></span>
