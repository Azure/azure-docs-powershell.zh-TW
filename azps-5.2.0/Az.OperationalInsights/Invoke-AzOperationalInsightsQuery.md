---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281294"
---
# <span data-ttu-id="220ba-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="220ba-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="220ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="220ba-102">SYNOPSIS</span></span>
<span data-ttu-id="220ba-103">根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="220ba-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="220ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="220ba-104">SYNTAX</span></span>

### <span data-ttu-id="220ba-105">ByWorkspaceId (預設) </span><span class="sxs-lookup"><span data-stu-id="220ba-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220ba-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="220ba-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="220ba-107">說明</span><span class="sxs-lookup"><span data-stu-id="220ba-107">DESCRIPTION</span></span>
<span data-ttu-id="220ba-108">**AzOperationalInsightsQuery** Cmdlet 會根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="220ba-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="220ba-109">您可以在傳回物件的 Metadata 屬性中，存取搜尋的狀態。</span><span class="sxs-lookup"><span data-stu-id="220ba-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="220ba-110">如果狀態為 [待處理]，則搜尋尚未完成，結果則會從封存。</span><span class="sxs-lookup"><span data-stu-id="220ba-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="220ba-111">您可以從傳回物件的 Value 屬性中取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="220ba-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="220ba-112">請在此處查看一般查詢限制的詳細資料： https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language 。</span><span class="sxs-lookup"><span data-stu-id="220ba-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="220ba-113">示例</span><span class="sxs-lookup"><span data-stu-id="220ba-113">EXAMPLES</span></span>

### <span data-ttu-id="220ba-114">範例1：使用查詢取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="220ba-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="220ba-115">呼叫後，$queryResults。結果將包含查詢中所有產生的資料列。</span><span class="sxs-lookup"><span data-stu-id="220ba-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="220ba-116">範例2：轉換 $results。向陣列產生 IEnumerable</span><span class="sxs-lookup"><span data-stu-id="220ba-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="220ba-117">某些查詢會傳回非常大的資料集。</span><span class="sxs-lookup"><span data-stu-id="220ba-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="220ba-118">因此，此 Cmdlet 的預設行為是返回 IEnumerable 來減少記憶體成本。</span><span class="sxs-lookup"><span data-stu-id="220ba-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="220ba-119">如果您想要有結果陣列，您可以使用 LINQ ToArray ( # A1 延伸方法，將 IEnumerable 轉換成陣列。</span><span class="sxs-lookup"><span data-stu-id="220ba-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="220ba-120">範例3：使用查詢針對特定時間範圍取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="220ba-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="220ba-121">此查詢的結果將限制為過去24小時。</span><span class="sxs-lookup"><span data-stu-id="220ba-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="220ba-122">範例4：在查詢結果中加入轉譯 & 統計資料</span><span class="sxs-lookup"><span data-stu-id="220ba-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="220ba-123">如需轉譯 [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) 與統計資訊的詳細資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="220ba-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="220ba-124">參數</span><span class="sxs-lookup"><span data-stu-id="220ba-124">PARAMETERS</span></span>

### <span data-ttu-id="220ba-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="220ba-125">-AsJob</span></span>
<span data-ttu-id="220ba-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="220ba-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="220ba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220ba-127">-DefaultProfile</span></span>
<span data-ttu-id="220ba-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="220ba-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="220ba-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="220ba-129">-IncludeRender</span></span>
<span data-ttu-id="220ba-130">如果已指定，度量查詢的轉譯資訊將會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="220ba-130">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="220ba-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="220ba-131">-IncludeStatistics</span></span>
<span data-ttu-id="220ba-132">如果已指定，查詢的統計資料就會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="220ba-132">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="220ba-133">-Query</span><span class="sxs-lookup"><span data-stu-id="220ba-133">-Query</span></span>
<span data-ttu-id="220ba-134">要執行的查詢。</span><span class="sxs-lookup"><span data-stu-id="220ba-134">The query to execute.</span></span>

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

### <span data-ttu-id="220ba-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="220ba-135">-Timespan</span></span>
<span data-ttu-id="220ba-136">要與查詢系結的 timespan。</span><span class="sxs-lookup"><span data-stu-id="220ba-136">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="220ba-137">-稍候</span><span class="sxs-lookup"><span data-stu-id="220ba-137">-Wait</span></span>
<span data-ttu-id="220ba-138">會將上限放在伺服器處理查詢時花費的時間長度。</span><span class="sxs-lookup"><span data-stu-id="220ba-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="220ba-139">請參閱 https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="220ba-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="220ba-140">-工作區</span><span class="sxs-lookup"><span data-stu-id="220ba-140">-Workspace</span></span>
<span data-ttu-id="220ba-141">工作區</span><span class="sxs-lookup"><span data-stu-id="220ba-141">The workspace</span></span>

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

### <span data-ttu-id="220ba-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="220ba-142">-WorkspaceId</span></span>
<span data-ttu-id="220ba-143">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="220ba-143">The workspace ID.</span></span>

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

### <span data-ttu-id="220ba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220ba-144">CommonParameters</span></span>
<span data-ttu-id="220ba-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="220ba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220ba-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="220ba-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220ba-147">輸入</span><span class="sxs-lookup"><span data-stu-id="220ba-147">INPUTS</span></span>

### <span data-ttu-id="220ba-148">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="220ba-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="220ba-149">輸出</span><span class="sxs-lookup"><span data-stu-id="220ba-149">OUTPUTS</span></span>

### <span data-ttu-id="220ba-150">PSQueryResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="220ba-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="220ba-151">筆記</span><span class="sxs-lookup"><span data-stu-id="220ba-151">NOTES</span></span>

## <span data-ttu-id="220ba-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="220ba-152">RELATED LINKS</span></span>
