---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131995"
---
# <span data-ttu-id="88379-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="88379-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="88379-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88379-102">SYNOPSIS</span></span>
<span data-ttu-id="88379-103">取得事件網格網域的詳細資料，或取得目前 Azure 訂閱中所有事件網格網域的清單。</span><span class="sxs-lookup"><span data-stu-id="88379-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="88379-104">句法</span><span class="sxs-lookup"><span data-stu-id="88379-104">SYNTAX</span></span>

### <span data-ttu-id="88379-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="88379-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88379-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88379-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88379-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="88379-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88379-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="88379-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88379-109">說明</span><span class="sxs-lookup"><span data-stu-id="88379-109">DESCRIPTION</span></span>
<span data-ttu-id="88379-110">Get-AzEventGridDomain Cmdlet 會取得指定事件格線網域的詳細資料，或目前 Azure 訂閱中所有事件網格網域的清單。</span><span class="sxs-lookup"><span data-stu-id="88379-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="88379-111">如果提供了功能變數名稱，則會傳回單一事件格線網域的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="88379-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="88379-112">如果未提供功能變數名稱，則會傳回網域清單。</span><span class="sxs-lookup"><span data-stu-id="88379-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="88379-113">此清單中傳回的元素數目由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="88379-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="88379-114">如果未指定 Top 值或 $null，則清單將會包含一次傳回的所有網域專案。</span><span class="sxs-lookup"><span data-stu-id="88379-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="88379-115">否則，Top 會指出清單中要傳回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="88379-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="88379-116">如果仍有更多網域可供使用，則會在下一個呼叫中使用 NextLink 中的值，以取得網域的下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="88379-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="88379-117">最後，ODataQuery 參數是用來執行搜尋結果篩選。</span><span class="sxs-lookup"><span data-stu-id="88379-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="88379-118">篩選查詢遵循 OData 語法，只使用 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="88379-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="88379-119">支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="88379-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="88379-120">示例</span><span class="sxs-lookup"><span data-stu-id="88379-120">EXAMPLES</span></span>

### <span data-ttu-id="88379-121">範例1</span><span class="sxs-lookup"><span data-stu-id="88379-121">Example 1</span></span>

<span data-ttu-id="88379-122">取得 \` \` 資源群組 MyResourceGroupName 中事件網格網域 Domain1 的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="88379-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="88379-123">範例2</span><span class="sxs-lookup"><span data-stu-id="88379-123">Example 2</span></span>

<span data-ttu-id="88379-124">取得 \` \` \` 使用 ResourceId 選項的資源群組 MyResourceGroupName 中事件網格網域 Domain1 的詳細資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="88379-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="88379-125">範例3</span><span class="sxs-lookup"><span data-stu-id="88379-125">Example 3</span></span>

<span data-ttu-id="88379-126">列出 [資源群組 MyResourceGroupName] 中的所有事件格線（ \` \` 不分頁） (所有網域都會傳回一個快照) </span><span class="sxs-lookup"><span data-stu-id="88379-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="88379-127">範例4</span><span class="sxs-lookup"><span data-stu-id="88379-127">Example 4</span></span>

<span data-ttu-id="88379-128">如果資源群組 MyResourceGroupName 中的任何) \` \` 一次都滿足 $odataFilter 查詢10個網域，請列出 [事件格線網域] (。</span><span class="sxs-lookup"><span data-stu-id="88379-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="88379-129">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="88379-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="88379-130">若要) 網域的 [下一頁] (，使用者應該重新呼叫 Get-AzEventGridDomain 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="88379-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="88379-131">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="88379-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="88379-132">範例5</span><span class="sxs-lookup"><span data-stu-id="88379-132">Example 5</span></span>

<span data-ttu-id="88379-133">列出 Azure 訂閱中的所有事件格線（不分頁） (所有網域都會以一個快照傳回) </span><span class="sxs-lookup"><span data-stu-id="88379-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="88379-134">範例6</span><span class="sxs-lookup"><span data-stu-id="88379-134">Example 6</span></span>

<span data-ttu-id="88379-135">如果 Azure 訂閱中有一次滿足 $odataFilter 查詢20個網域的任何) ，請列出事件 Grid 網域 (。</span><span class="sxs-lookup"><span data-stu-id="88379-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="88379-136">如果有更多結果可供使用，$result。NextLink 不會 $null。</span><span class="sxs-lookup"><span data-stu-id="88379-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="88379-137">若要) 網域的 [下一頁] (，使用者應該重新呼叫 Get-AzEventGridDomain 並使用結果。從先前的呼叫取得的 NextLink。</span><span class="sxs-lookup"><span data-stu-id="88379-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="88379-138">當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。</span><span class="sxs-lookup"><span data-stu-id="88379-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="88379-139">參數</span><span class="sxs-lookup"><span data-stu-id="88379-139">PARAMETERS</span></span>

### <span data-ttu-id="88379-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88379-140">-DefaultProfile</span></span>
<span data-ttu-id="88379-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88379-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88379-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="88379-142">-Name</span></span>
<span data-ttu-id="88379-143">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="88379-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88379-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="88379-144">-NextLink</span></span>
<span data-ttu-id="88379-145">要取得的下一頁資源連結。</span><span class="sxs-lookup"><span data-stu-id="88379-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="88379-146">當仍有更多資源可供查詢時，會使用第一個 Get-AzEventGrid Cmdlet 呼叫來取得此值。</span><span class="sxs-lookup"><span data-stu-id="88379-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="88379-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="88379-147">-ODataQuery</span></span>
<span data-ttu-id="88379-148">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="88379-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="88379-149">目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。</span><span class="sxs-lookup"><span data-stu-id="88379-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88379-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88379-150">-ResourceGroupName</span></span>
<span data-ttu-id="88379-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88379-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88379-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88379-152">-ResourceId</span></span>
<span data-ttu-id="88379-153">代表事件網格網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88379-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="88379-154">-上方</span><span class="sxs-lookup"><span data-stu-id="88379-154">-Top</span></span>
<span data-ttu-id="88379-155">要取得的資源數目上限。</span><span class="sxs-lookup"><span data-stu-id="88379-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="88379-156">有效值介於1到100。</span><span class="sxs-lookup"><span data-stu-id="88379-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="88379-157">如果已指定 top 值，但仍有更多結果，結果將會包含下一個頁面的連結，以在 NextLink 中查詢。</span><span class="sxs-lookup"><span data-stu-id="88379-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="88379-158">如果未指定 Top 值，就會一次傳回完整的資源清單。</span><span class="sxs-lookup"><span data-stu-id="88379-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88379-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88379-159">CommonParameters</span></span>
<span data-ttu-id="88379-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88379-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88379-161">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88379-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88379-162">輸入</span><span class="sxs-lookup"><span data-stu-id="88379-162">INPUTS</span></span>

### <span data-ttu-id="88379-163">System.object</span><span class="sxs-lookup"><span data-stu-id="88379-163">System.String</span></span>

## <span data-ttu-id="88379-164">輸出</span><span class="sxs-lookup"><span data-stu-id="88379-164">OUTPUTS</span></span>

### <span data-ttu-id="88379-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="88379-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="88379-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="88379-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="88379-167">筆記</span><span class="sxs-lookup"><span data-stu-id="88379-167">NOTES</span></span>

## <span data-ttu-id="88379-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="88379-168">RELATED LINKS</span></span>
