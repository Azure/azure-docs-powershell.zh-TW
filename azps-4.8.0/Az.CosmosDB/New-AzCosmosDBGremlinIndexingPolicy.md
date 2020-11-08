---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971183"
---
# <span data-ttu-id="bb6ba-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="bb6ba-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="bb6ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6ba-103">建立新的 CosmosDB IndexingPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="bb6ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb6ba-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb6ba-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb6ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bb6ba-106">**新的-AzCosmosDBGremlinIndexingPolicy** Cmdlet 會建立 PSIndexingPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="bb6ba-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb6ba-107">EXAMPLES</span></span>

### <span data-ttu-id="bb6ba-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb6ba-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="bb6ba-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="bb6ba-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bb6ba-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb6ba-110">PARAMETERS</span></span>

### <span data-ttu-id="bb6ba-111">-自動</span><span class="sxs-lookup"><span data-stu-id="bb6ba-111">-Automatic</span></span>
<span data-ttu-id="bb6ba-112">以 Bool 表示索引原則是否為自動</span><span class="sxs-lookup"><span data-stu-id="bb6ba-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="bb6ba-113">-CompositePath</span></span>
<span data-ttu-id="bb6ba-114">PSCompositePath 的物件陣列的陣列（CosmosDB）。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6ba-115">-DefaultProfile</span></span>
<span data-ttu-id="bb6ba-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="bb6ba-117">-ExcludedPath</span></span>
<span data-ttu-id="bb6ba-118">包含 excludedPath 的字串陣列 (指定 JSON 檔內要排除在 Azure Cosmos DB 服務中的路徑。 ) 元素。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="bb6ba-119">-IncludedPath</span></span>
<span data-ttu-id="bb6ba-120">包含 includedPath 的字串陣列 (指定 JSON 檔內要包含在 Azure Cosmos DB 服務中的路徑。 ) 元素。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="bb6ba-121">-IndexingMode</span></span>
<span data-ttu-id="bb6ba-122">表示索引模式。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="bb6ba-123">可能的值包括： [一致 "、" Lazy "、" None "</span><span class="sxs-lookup"><span data-stu-id="bb6ba-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="bb6ba-124">-SpatialSpec</span></span>
<span data-ttu-id="bb6ba-125">CosmosDB 類型的物件陣列。 PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="bb6ba-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6ba-126">CommonParameters</span></span>
<span data-ttu-id="bb6ba-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6ba-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6ba-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bb6ba-129">INPUTS</span></span>

### <span data-ttu-id="bb6ba-130">所有</span><span class="sxs-lookup"><span data-stu-id="bb6ba-130">None</span></span>

## <span data-ttu-id="bb6ba-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bb6ba-131">OUTPUTS</span></span>

### <span data-ttu-id="bb6ba-132">PSIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="bb6ba-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="bb6ba-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bb6ba-133">NOTES</span></span>

## <span data-ttu-id="bb6ba-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb6ba-134">RELATED LINKS</span></span>
