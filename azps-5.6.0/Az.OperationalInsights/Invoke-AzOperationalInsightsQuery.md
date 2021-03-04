---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: bdba6d4da6df49d1975e2cfd1cc6e47f6ce6d776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916712"
---
# <span data-ttu-id="5536c-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="5536c-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="5536c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5536c-102">SYNOPSIS</span></span>
<span data-ttu-id="5536c-103">根據指定的參數，返回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="5536c-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="5536c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5536c-104">SYNTAX</span></span>

### <span data-ttu-id="5536c-105">ByWorkspaceId (預設) </span><span class="sxs-lookup"><span data-stu-id="5536c-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5536c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5536c-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5536c-107">描述</span><span class="sxs-lookup"><span data-stu-id="5536c-107">DESCRIPTION</span></span>
<span data-ttu-id="5536c-108">**Invoke-AzOperationalInsightsQuery** Cmdlet 會根據指定的參數，會返回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="5536c-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="5536c-109">您可以在所返回物件的中繼資料屬性中存取搜尋的狀態。</span><span class="sxs-lookup"><span data-stu-id="5536c-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="5536c-110">如果狀態為擱置中，則搜尋尚未完成，且結果會來自該檔案。</span><span class="sxs-lookup"><span data-stu-id="5536c-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="5536c-111">您可以從所返回物件的 Value 屬性中，取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="5536c-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="5536c-112">請在這裡查看一般查詢限制的詳細資料 https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language ：。</span><span class="sxs-lookup"><span data-stu-id="5536c-112">Please check detail of general query limits here: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="5536c-113">例子</span><span class="sxs-lookup"><span data-stu-id="5536c-113">EXAMPLES</span></span>

### <span data-ttu-id="5536c-114">範例 1：使用查詢取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="5536c-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="5536c-115">一旦被$queryResults，$queryResults.Results 會包含來自查詢的所有結果資料列。</span><span class="sxs-lookup"><span data-stu-id="5536c-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="5536c-116">範例 2：轉換$results。陣列可編號的結果</span><span class="sxs-lookup"><span data-stu-id="5536c-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="5536c-117">某些查詢可能會導致系統退回非常大型的資料集。</span><span class="sxs-lookup"><span data-stu-id="5536c-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="5536c-118">因此，Cmdlet 的預設行為是，會以 IEnumnumnumable 來降低記憶體成本。</span><span class="sxs-lookup"><span data-stu-id="5536c-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="5536c-119">如果您想要使用結果陣列，可以使用 LINQ Enumerable.ToArray () 擴充方法，將 IEnumnumnumable 轉換為數組。</span><span class="sxs-lookup"><span data-stu-id="5536c-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="5536c-120">範例 3：使用特定時間範圍的查詢取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="5536c-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="5536c-121">此查詢的結果將限制為過去 24 小時。</span><span class="sxs-lookup"><span data-stu-id="5536c-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="5536c-122">範例 4：在查詢結果&呈現資料統計</span><span class="sxs-lookup"><span data-stu-id="5536c-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="5536c-123">請參閱 [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) 有關呈現和統計資料的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5536c-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="5536c-124">參數</span><span class="sxs-lookup"><span data-stu-id="5536c-124">PARAMETERS</span></span>

### <span data-ttu-id="5536c-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5536c-125">-AsJob</span></span>
<span data-ttu-id="5536c-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5536c-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5536c-127">-DefaultProfile</span></span>
<span data-ttu-id="5536c-128">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5536c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5536c-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="5536c-129">-IncludeRender</span></span>
<span data-ttu-id="5536c-130">如果指定，表示公制查詢的資訊會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="5536c-130">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="5536c-131">-IncludeStatistics</span></span>
<span data-ttu-id="5536c-132">如果指定，查詢統計資料會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="5536c-132">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-133">-查詢</span><span class="sxs-lookup"><span data-stu-id="5536c-133">-Query</span></span>
<span data-ttu-id="5536c-134">要執行的查詢。</span><span class="sxs-lookup"><span data-stu-id="5536c-134">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-135">-時間窗格</span><span class="sxs-lookup"><span data-stu-id="5536c-135">-Timespan</span></span>
<span data-ttu-id="5536c-136">將查詢繫結的時數。</span><span class="sxs-lookup"><span data-stu-id="5536c-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-137">-等待</span><span class="sxs-lookup"><span data-stu-id="5536c-137">-Wait</span></span>
<span data-ttu-id="5536c-138">將上限放在伺服器處理查詢所花的時間量。</span><span class="sxs-lookup"><span data-stu-id="5536c-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="5536c-139">看到： https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="5536c-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-140">-工作區</span><span class="sxs-lookup"><span data-stu-id="5536c-140">-Workspace</span></span>
<span data-ttu-id="5536c-141">工作區</span><span class="sxs-lookup"><span data-stu-id="5536c-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="5536c-142">-WorkspaceId</span></span>
<span data-ttu-id="5536c-143">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="5536c-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5536c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5536c-144">CommonParameters</span></span>
<span data-ttu-id="5536c-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5536c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5536c-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5536c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5536c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5536c-147">INPUTS</span></span>

### <span data-ttu-id="5536c-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5536c-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="5536c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="5536c-149">OUTPUTS</span></span>

### <span data-ttu-id="5536c-150">Microsoft.Azure.Commands.OperationalInsights.models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="5536c-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="5536c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="5536c-151">NOTES</span></span>

## <span data-ttu-id="5536c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5536c-152">RELATED LINKS</span></span>
