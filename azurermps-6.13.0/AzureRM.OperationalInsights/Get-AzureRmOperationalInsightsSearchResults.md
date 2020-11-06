---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 547988d2079f35b82af3638e3e4f09b101d8fbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443763"
---
# <span data-ttu-id="09ec2-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="09ec2-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="09ec2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="09ec2-103">根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ec2-104">句法</span><span class="sxs-lookup"><span data-stu-id="09ec2-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09ec2-105">說明</span><span class="sxs-lookup"><span data-stu-id="09ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="09ec2-106">**AzureRmOperationalInsightsSearchResults** Cmdlet 會根據指定的參數傳回搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="09ec2-107">您可以在傳回物件的 Metadata 屬性中，存取搜尋的狀態。</span><span class="sxs-lookup"><span data-stu-id="09ec2-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="09ec2-108">如果狀態為 [待處理]，則搜尋尚未完成，結果則會從封存。</span><span class="sxs-lookup"><span data-stu-id="09ec2-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="09ec2-109">您可以從傳回物件的 Value 屬性中取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="09ec2-110">示例</span><span class="sxs-lookup"><span data-stu-id="09ec2-110">EXAMPLES</span></span>

### <span data-ttu-id="09ec2-111">範例1：使用查詢取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="09ec2-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="09ec2-112">這個命令會使用查詢來取得所有搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="09ec2-113">範例2：使用識別碼取得搜尋結果</span><span class="sxs-lookup"><span data-stu-id="09ec2-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="09ec2-114">這個命令會使用識別碼來取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="09ec2-115">範例3：在顯示結果前等候搜尋完成</span><span class="sxs-lookup"><span data-stu-id="09ec2-115">Example 3: Wait for a search to complete before displaying results</span></span>
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

<span data-ttu-id="09ec2-116">此腳本會啟動搜尋並等到它完成後，才會顯示結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="09ec2-117">參數</span><span class="sxs-lookup"><span data-stu-id="09ec2-117">PARAMETERS</span></span>

### <span data-ttu-id="09ec2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ec2-118">-DefaultProfile</span></span>
<span data-ttu-id="09ec2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="09ec2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09ec2-120">-結束</span><span class="sxs-lookup"><span data-stu-id="09ec2-120">-End</span></span>
<span data-ttu-id="09ec2-121">所查詢時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="09ec2-121">End of the queried time range.</span></span>

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

### <span data-ttu-id="09ec2-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="09ec2-122">-Id</span></span>
<span data-ttu-id="09ec2-123">如果提供識別碼，就會使用原始的查詢參數來檢索該識別碼的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="09ec2-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

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

### <span data-ttu-id="09ec2-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="09ec2-124">-PostHighlight</span></span>
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

### <span data-ttu-id="09ec2-125">-PreHighlight</span><span class="sxs-lookup"><span data-stu-id="09ec2-125">-PreHighlight</span></span>
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

### <span data-ttu-id="09ec2-126">-Query</span><span class="sxs-lookup"><span data-stu-id="09ec2-126">-Query</span></span>
<span data-ttu-id="09ec2-127">將執行的搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="09ec2-127">The search query that will be executed.</span></span>

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

### <span data-ttu-id="09ec2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ec2-128">-ResourceGroupName</span></span>
<span data-ttu-id="09ec2-129">包含工作區之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09ec2-129">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="09ec2-130">-開始</span><span class="sxs-lookup"><span data-stu-id="09ec2-130">-Start</span></span>
<span data-ttu-id="09ec2-131">所查詢時間範圍的開始日期。</span><span class="sxs-lookup"><span data-stu-id="09ec2-131">Start of the queried time range.</span></span>

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

### <span data-ttu-id="09ec2-132">-上方</span><span class="sxs-lookup"><span data-stu-id="09ec2-132">-Top</span></span>
<span data-ttu-id="09ec2-133">要傳回的結果數目上限，限制在5000。</span><span class="sxs-lookup"><span data-stu-id="09ec2-133">The maximum number of results to be returned, limited to 5000.</span></span>

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

### <span data-ttu-id="09ec2-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09ec2-134">-WorkspaceName</span></span>
<span data-ttu-id="09ec2-135">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="09ec2-135">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="09ec2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ec2-136">CommonParameters</span></span>
<span data-ttu-id="09ec2-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09ec2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ec2-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09ec2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ec2-139">輸入</span><span class="sxs-lookup"><span data-stu-id="09ec2-139">INPUTS</span></span>

### <span data-ttu-id="09ec2-140">System.object</span><span class="sxs-lookup"><span data-stu-id="09ec2-140">System.String</span></span>

### <span data-ttu-id="09ec2-141">System.object</span><span class="sxs-lookup"><span data-stu-id="09ec2-141">System.Int64</span></span>

### <span data-ttu-id="09ec2-142">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09ec2-142">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="09ec2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="09ec2-143">OUTPUTS</span></span>

### <span data-ttu-id="09ec2-144">PSSearchGetSearchResultsResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="09ec2-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="09ec2-145">筆記</span><span class="sxs-lookup"><span data-stu-id="09ec2-145">NOTES</span></span>

## <span data-ttu-id="09ec2-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="09ec2-146">RELATED LINKS</span></span>

[<span data-ttu-id="09ec2-147">AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="09ec2-147">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


