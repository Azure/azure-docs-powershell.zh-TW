---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: 6672bb6f788b06896fdfe9cde44c68639077e5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448286"
---
# <span data-ttu-id="4e0d2-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="4e0d2-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="4e0d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0d2-103">根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e0d2-104">SYNTAX</span></span>

### <span data-ttu-id="4e0d2-105">ByWorkspaceId (預設) </span><span class="sxs-lookup"><span data-stu-id="4e0d2-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e0d2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4e0d2-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e0d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="4e0d2-107">DESCRIPTION</span></span>
<span data-ttu-id="4e0d2-108">**AzureRmOperationalInsightsQuery** Cmdlet 會根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="4e0d2-109">您可以在傳回物件的 Metadata 屬性中，存取搜尋的狀態。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="4e0d2-110">如果狀態為 [待處理]，則搜尋尚未完成，結果則會從封存。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="4e0d2-111">您可以從傳回物件的 Value 屬性中取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="4e0d2-112">示例</span><span class="sxs-lookup"><span data-stu-id="4e0d2-112">EXAMPLES</span></span>

### <span data-ttu-id="4e0d2-113">範例1：使用查詢取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="4e0d2-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="4e0d2-114">呼叫後，$queryResults。結果將包含查詢中所有產生的資料列。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="4e0d2-115">範例2：轉換 $results。結果 IEnumberable 至陣列</span><span class="sxs-lookup"><span data-stu-id="4e0d2-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="4e0d2-116">某些查詢會傳回非常大的資料集。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="4e0d2-117">因此，此 Cmdlet 的預設行為是返回 IEnumerable 來減少記憶體成本。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="4e0d2-118">如果您想要有結果陣列，您可以使用 LINQ ToArray ( # A1 延伸方法，將 IEnumerable 轉換成陣列。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="4e0d2-119">範例3：使用查詢針對特定時間範圍取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="4e0d2-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="4e0d2-120">此查詢的結果將限制為過去24小時。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="4e0d2-121">範例4：在查詢結果中加入轉譯 & 統計資料</span><span class="sxs-lookup"><span data-stu-id="4e0d2-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="4e0d2-122">如需轉譯 [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) 與統計資訊的詳細資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="4e0d2-123">參數</span><span class="sxs-lookup"><span data-stu-id="4e0d2-123">PARAMETERS</span></span>

### <span data-ttu-id="4e0d2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e0d2-124">-AsJob</span></span>
<span data-ttu-id="4e0d2-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4e0d2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e0d2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0d2-126">-DefaultProfile</span></span>
<span data-ttu-id="4e0d2-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0d2-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="4e0d2-128">-IncludeRender</span></span>
<span data-ttu-id="4e0d2-129">如果已指定，度量查詢的轉譯資訊將會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="4e0d2-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="4e0d2-130">-IncludeStatistics</span></span>
<span data-ttu-id="4e0d2-131">如果已指定，查詢的統計資料就會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="4e0d2-132">-Query</span><span class="sxs-lookup"><span data-stu-id="4e0d2-132">-Query</span></span>
<span data-ttu-id="4e0d2-133">要執行的查詢。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-133">The query to execute.</span></span>

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

### <span data-ttu-id="4e0d2-134">-Timespan</span><span class="sxs-lookup"><span data-stu-id="4e0d2-134">-Timespan</span></span>
<span data-ttu-id="4e0d2-135">要與查詢系結的 timespan。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="4e0d2-136">-稍候</span><span class="sxs-lookup"><span data-stu-id="4e0d2-136">-Wait</span></span>
<span data-ttu-id="4e0d2-137">會將上限放在伺服器處理查詢時花費的時間長度。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="4e0d2-138">請參閱 https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="4e0d2-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="4e0d2-139">-工作區</span><span class="sxs-lookup"><span data-stu-id="4e0d2-139">-Workspace</span></span>
<span data-ttu-id="4e0d2-140">工作區</span><span class="sxs-lookup"><span data-stu-id="4e0d2-140">The workspace</span></span>

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

### <span data-ttu-id="4e0d2-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4e0d2-141">-WorkspaceId</span></span>
<span data-ttu-id="4e0d2-142">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-142">The workspace ID.</span></span>

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

### <span data-ttu-id="4e0d2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0d2-143">CommonParameters</span></span>
<span data-ttu-id="4e0d2-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0d2-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0d2-146">輸入</span><span class="sxs-lookup"><span data-stu-id="4e0d2-146">INPUTS</span></span>

### <span data-ttu-id="4e0d2-147">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="4e0d2-148">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4e0d2-148">Parameters: Workspace (ByValue)</span></span>

## <span data-ttu-id="4e0d2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="4e0d2-149">OUTPUTS</span></span>

### <span data-ttu-id="4e0d2-150">PSQueryResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="4e0d2-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="4e0d2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="4e0d2-151">NOTES</span></span>

## <span data-ttu-id="4e0d2-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e0d2-152">RELATED LINKS</span></span>
