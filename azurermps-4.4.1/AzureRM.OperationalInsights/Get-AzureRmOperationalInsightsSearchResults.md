---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 161365ee947a118221fa922ab9e7d05486d3908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625117"
---
# <span data-ttu-id="2604e-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="2604e-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="2604e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2604e-102">SYNOPSIS</span></span>
<span data-ttu-id="2604e-103">根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2604e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2604e-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2604e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2604e-105">DESCRIPTION</span></span>
<span data-ttu-id="2604e-106">**AzureRmOperationalInsightsSearchResults** Cmdlet 會根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="2604e-107">您可以在傳回物件的 Metadata 屬性中，存取搜尋的狀態。</span><span class="sxs-lookup"><span data-stu-id="2604e-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="2604e-108">如果狀態為 [待處理]，則搜尋尚未完成，結果則會從封存。</span><span class="sxs-lookup"><span data-stu-id="2604e-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="2604e-109">您可以從傳回物件的 Value 屬性中取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="2604e-110">示例</span><span class="sxs-lookup"><span data-stu-id="2604e-110">EXAMPLES</span></span>

### <span data-ttu-id="2604e-111">範例1：使用查詢取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="2604e-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="2604e-112">這個命令會使用查詢來取得所有搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="2604e-113">範例2：使用識別碼取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="2604e-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="2604e-114">這個命令會使用識別碼來取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="2604e-115">範例3：在顯示結果前等候搜尋完成</span><span class="sxs-lookup"><span data-stu-id="2604e-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="2604e-116">此腳本會啟動搜尋並等到它完成後，才會顯示結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="2604e-117">參數</span><span class="sxs-lookup"><span data-stu-id="2604e-117">PARAMETERS</span></span>

### <span data-ttu-id="2604e-118">-結束</span><span class="sxs-lookup"><span data-stu-id="2604e-118">-End</span></span>
<span data-ttu-id="2604e-119">所查詢時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="2604e-119">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2604e-120">-Id</span></span>
<span data-ttu-id="2604e-121">如果提供識別碼，就會使用原始的查詢參數來檢索該識別碼的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2604e-121">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-122">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="2604e-122">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-123">-PreHighlight</span><span class="sxs-lookup"><span data-stu-id="2604e-123">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-124">-Query</span><span class="sxs-lookup"><span data-stu-id="2604e-124">-Query</span></span>
<span data-ttu-id="2604e-125">將執行的搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="2604e-125">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2604e-126">-ResourceGroupName</span></span>
<span data-ttu-id="2604e-127">包含工作區之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2604e-127">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-128">-開始</span><span class="sxs-lookup"><span data-stu-id="2604e-128">-Start</span></span>
<span data-ttu-id="2604e-129">所查詢時間範圍的開始日期。</span><span class="sxs-lookup"><span data-stu-id="2604e-129">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-130">-上方</span><span class="sxs-lookup"><span data-stu-id="2604e-130">-Top</span></span>
<span data-ttu-id="2604e-131">要傳回的結果數目上限，限制在5000。</span><span class="sxs-lookup"><span data-stu-id="2604e-131">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2604e-132">-WorkspaceName</span></span>
<span data-ttu-id="2604e-133">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2604e-133">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2604e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2604e-134">-DefaultProfile</span></span>
<span data-ttu-id="2604e-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2604e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2604e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2604e-136">CommonParameters</span></span>
<span data-ttu-id="2604e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2604e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2604e-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2604e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2604e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2604e-139">INPUTS</span></span>

## <span data-ttu-id="2604e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2604e-140">OUTPUTS</span></span>

### <span data-ttu-id="2604e-141">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="2604e-141">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="2604e-142">**PSSearchGetSearchResultsResponse** 物件包含 Value 屬性，其中包含從搜尋中以 JSON 格式傳回的記錄，以及包含有關搜尋結果之資訊的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="2604e-142">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="2604e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2604e-143">NOTES</span></span>

## <span data-ttu-id="2604e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2604e-144">RELATED LINKS</span></span>

[<span data-ttu-id="2604e-145">AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="2604e-145">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


