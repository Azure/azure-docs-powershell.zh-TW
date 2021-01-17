---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446048"
---
# <span data-ttu-id="41208-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="41208-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="41208-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41208-102">SYNOPSIS</span></span>
<span data-ttu-id="41208-103">建立新的 CosmosDB Sql IndexingPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="41208-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="41208-104">句法</span><span class="sxs-lookup"><span data-stu-id="41208-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41208-105">說明</span><span class="sxs-lookup"><span data-stu-id="41208-105">DESCRIPTION</span></span>
<span data-ttu-id="41208-106">**新的-AzCosmosDBSqlIndexingPolicy** Cmdlet 會建立 PSSqlIndexingPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="41208-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="41208-107">示例</span><span class="sxs-lookup"><span data-stu-id="41208-107">EXAMPLES</span></span>

### <span data-ttu-id="41208-108">範例1</span><span class="sxs-lookup"><span data-stu-id="41208-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="41208-109">參數</span><span class="sxs-lookup"><span data-stu-id="41208-109">PARAMETERS</span></span>

### <span data-ttu-id="41208-110">-自動</span><span class="sxs-lookup"><span data-stu-id="41208-110">-Automatic</span></span>
<span data-ttu-id="41208-111">以 Bool 表示索引原則是否為自動</span><span class="sxs-lookup"><span data-stu-id="41208-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="41208-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="41208-112">-CompositePath</span></span>
<span data-ttu-id="41208-113">PSCompositePath 的物件陣列的陣列（CosmosDB）。</span><span class="sxs-lookup"><span data-stu-id="41208-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="41208-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41208-114">-DefaultProfile</span></span>
<span data-ttu-id="41208-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41208-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41208-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="41208-116">-ExcludedPath</span></span>
<span data-ttu-id="41208-117">包含 excludedPath 的字串陣列 (指定 JSON 檔內要排除在 Azure Cosmos DB 服務中的路徑。 ) 元素。</span><span class="sxs-lookup"><span data-stu-id="41208-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="41208-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="41208-118">-IncludedPath</span></span>
<span data-ttu-id="41208-119">包含 includedPath 的字串陣列 (指定 JSON 檔內要包含在 Azure Cosmos DB 服務中的路徑。 ) 元素。</span><span class="sxs-lookup"><span data-stu-id="41208-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="41208-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="41208-120">-IndexingMode</span></span>
<span data-ttu-id="41208-121">表示索引模式。</span><span class="sxs-lookup"><span data-stu-id="41208-121">indicates the indexing mode.</span></span>
<span data-ttu-id="41208-122">可能的值包括： [一致 "、" Lazy "、" None "</span><span class="sxs-lookup"><span data-stu-id="41208-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="41208-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="41208-123">-SpatialSpec</span></span>
<span data-ttu-id="41208-124">CosmosDB 類型的物件陣列。 PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="41208-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="41208-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41208-125">CommonParameters</span></span>
<span data-ttu-id="41208-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41208-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41208-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41208-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41208-128">輸入</span><span class="sxs-lookup"><span data-stu-id="41208-128">INPUTS</span></span>

### <span data-ttu-id="41208-129">所有</span><span class="sxs-lookup"><span data-stu-id="41208-129">None</span></span>

## <span data-ttu-id="41208-130">輸出</span><span class="sxs-lookup"><span data-stu-id="41208-130">OUTPUTS</span></span>

### <span data-ttu-id="41208-131">PSSqlIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="41208-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="41208-132">筆記</span><span class="sxs-lookup"><span data-stu-id="41208-132">NOTES</span></span>

## <span data-ttu-id="41208-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="41208-133">RELATED LINKS</span></span>
