---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 919d8d0557fd6bb57cc826da8ac18bc71b911c62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910105"
---
# <span data-ttu-id="d101e-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d101e-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="d101e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d101e-102">SYNOPSIS</span></span>
<span data-ttu-id="d101e-103">獲得事件格線網域的詳細資訊，或獲得目前 Azure 訂閱中所有事件格線網域的清單。</span><span class="sxs-lookup"><span data-stu-id="d101e-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="d101e-104">語法</span><span class="sxs-lookup"><span data-stu-id="d101e-104">SYNTAX</span></span>

### <span data-ttu-id="d101e-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d101e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d101e-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d101e-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d101e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d101e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d101e-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="d101e-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d101e-109">描述</span><span class="sxs-lookup"><span data-stu-id="d101e-109">DESCRIPTION</span></span>
<span data-ttu-id="d101e-110">此Get-AzEventGridDomain Cmdlet 會獲得指定事件格線網域的詳細資訊，或目前 Azure 訂閱中所有事件格線網域的清單。</span><span class="sxs-lookup"><span data-stu-id="d101e-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="d101e-111">如果提供功能變數名稱，系統即會返回單一事件格線網域的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d101e-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="d101e-112">如果未提供功能變數名稱，系統即會返回網域清單。</span><span class="sxs-lookup"><span data-stu-id="d101e-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="d101e-113">此清單所返回的元素數目是由 Top 參數控制。</span><span class="sxs-lookup"><span data-stu-id="d101e-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="d101e-114">如果未指定頂端值或$null，清單會包含一次返回的所有網域專案。</span><span class="sxs-lookup"><span data-stu-id="d101e-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="d101e-115">否則，Top 會指出清單中要返回的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="d101e-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="d101e-116">如果仍有更多網域可用，則 NextLink 中的值應該用於下一個通話中，以取得下一頁的網域。</span><span class="sxs-lookup"><span data-stu-id="d101e-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="d101e-117">最後，ODataQuery 參數是用來執行搜尋結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="d101e-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="d101e-118">篩選查詢只會使用 Name 屬性遵循 OData 語法。</span><span class="sxs-lookup"><span data-stu-id="d101e-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="d101e-119">支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="d101e-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="d101e-120">例子</span><span class="sxs-lookup"><span data-stu-id="d101e-120">EXAMPLES</span></span>

### <span data-ttu-id="d101e-121">範例 1</span><span class="sxs-lookup"><span data-stu-id="d101e-121">Example 1</span></span>

<span data-ttu-id="d101e-122">在資源群組 \` \` MyResourceGroupName 中，獲得事件格線網域網域1 \` 的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="d101e-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="d101e-123">範例 2</span><span class="sxs-lookup"><span data-stu-id="d101e-123">Example 2</span></span>

<span data-ttu-id="d101e-124">使用 ResourceId 選項，在資源群組 \` \` \` MyResourceGroupName 中，獲得事件格線網域網域1 \` 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d101e-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="d101e-125">範例 3</span><span class="sxs-lookup"><span data-stu-id="d101e-125">Example 3</span></span>

<span data-ttu-id="d101e-126">在資源群組 \` MyResourceGroupName 中列出所有事件格線網域，但不分頁 (所有網域都一次 \`) </span><span class="sxs-lookup"><span data-stu-id="d101e-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="d101e-127">範例 4</span><span class="sxs-lookup"><span data-stu-id="d101e-127">Example 4</span></span>

<span data-ttu-id="d101e-128">如果資源群組 MyResourceGroup $odataFilter Name (群組中) 一次滿足查詢 10 個網域，請列出事件格線 \` \` 網域。</span><span class="sxs-lookup"><span data-stu-id="d101e-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="d101e-129">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="d101e-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d101e-130">為了取得下一頁 (網) ，使用者預期會重新呼叫Get-AzEventGridDomain並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="d101e-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d101e-131">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="d101e-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="d101e-132">範例 5</span><span class="sxs-lookup"><span data-stu-id="d101e-132">Example 5</span></span>

<span data-ttu-id="d101e-133">在 Azure 訂閱中列出所有事件格線網域，而不分頁 (所有網域都一次) </span><span class="sxs-lookup"><span data-stu-id="d101e-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="d101e-134">範例 6</span><span class="sxs-lookup"><span data-stu-id="d101e-134">Example 6</span></span>

<span data-ttu-id="d101e-135">如果 Azure 訂閱 ($odataFilter任一) 同時滿足查詢 20 個網域，請列出事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="d101e-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="d101e-136">如果有更多的結果可用，$result。NextLink 將不會$null。</span><span class="sxs-lookup"><span data-stu-id="d101e-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d101e-137">為了取得下一頁 (網) ，使用者預期會重新呼叫Get-AzEventGridDomain並使用結果。從上一個通話取得 NextLink。</span><span class="sxs-lookup"><span data-stu-id="d101e-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d101e-138">結果時，來電者應該停止。NextLink 會變成$null。</span><span class="sxs-lookup"><span data-stu-id="d101e-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="d101e-139">參數</span><span class="sxs-lookup"><span data-stu-id="d101e-139">PARAMETERS</span></span>

### <span data-ttu-id="d101e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d101e-140">-DefaultProfile</span></span>
<span data-ttu-id="d101e-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d101e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d101e-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="d101e-142">-Name</span></span>
<span data-ttu-id="d101e-143">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d101e-143">EventGrid domain name.</span></span>

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

### <span data-ttu-id="d101e-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="d101e-144">-NextLink</span></span>
<span data-ttu-id="d101e-145">這是要取得之資源下一頁的連結。</span><span class="sxs-lookup"><span data-stu-id="d101e-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="d101e-146">當仍有更多資源可供查詢Get-AzEventGrid Cmdlet 呼叫時，會取得此值。</span><span class="sxs-lookup"><span data-stu-id="d101e-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="d101e-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d101e-147">-ODataQuery</span></span>
<span data-ttu-id="d101e-148">用來篩選清單結果的 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="d101e-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="d101e-149">目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。</span><span class="sxs-lookup"><span data-stu-id="d101e-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="d101e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d101e-150">-ResourceGroupName</span></span>
<span data-ttu-id="d101e-151">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d101e-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="d101e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d101e-152">-ResourceId</span></span>
<span data-ttu-id="d101e-153">代表事件格線網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d101e-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="d101e-154">-頂端</span><span class="sxs-lookup"><span data-stu-id="d101e-154">-Top</span></span>
<span data-ttu-id="d101e-155">要取得的資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="d101e-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="d101e-156">有效的值介於 1 到 100 之間。</span><span class="sxs-lookup"><span data-stu-id="d101e-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="d101e-157">如果已指定頂端值，且仍有更多結果可用，則結果會包含下一頁的連結，可在 NextLink 中查詢。</span><span class="sxs-lookup"><span data-stu-id="d101e-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="d101e-158">如果未指定 Top 值，將會一次返回完整的資源清單。</span><span class="sxs-lookup"><span data-stu-id="d101e-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="d101e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d101e-159">CommonParameters</span></span>
<span data-ttu-id="d101e-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d101e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d101e-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d101e-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d101e-162">輸入</span><span class="sxs-lookup"><span data-stu-id="d101e-162">INPUTS</span></span>

### <span data-ttu-id="d101e-163">System.String</span><span class="sxs-lookup"><span data-stu-id="d101e-163">System.String</span></span>

## <span data-ttu-id="d101e-164">輸出</span><span class="sxs-lookup"><span data-stu-id="d101e-164">OUTPUTS</span></span>

### <span data-ttu-id="d101e-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d101e-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="d101e-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="d101e-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="d101e-167">筆記</span><span class="sxs-lookup"><span data-stu-id="d101e-167">NOTES</span></span>

## <span data-ttu-id="d101e-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="d101e-168">RELATED LINKS</span></span>
