---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: b3d7591bf5dd83967230f6c96c3ca5b02232e316
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907901"
---
# <span data-ttu-id="f5c2a-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f5c2a-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="f5c2a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c2a-103">建立新一個管理物件。建立一個新的管理中心 SQL IndexingPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="f5c2a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5c2a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c2a-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c2a-106">**New-AzCosmosDBSqlIndexingPolicy** Cmdlet 會建立 PSSqlIndexingPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="f5c2a-107">例子</span><span class="sxs-lookup"><span data-stu-id="f5c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="f5c2a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5c2a-108">Example 1</span></span>
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

## <span data-ttu-id="f5c2a-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5c2a-109">PARAMETERS</span></span>

### <span data-ttu-id="f5c2a-110">-自動</span><span class="sxs-lookup"><span data-stu-id="f5c2a-110">-Automatic</span></span>
<span data-ttu-id="f5c2a-111">布林值以指出索引編制政策是否自動</span><span class="sxs-lookup"><span data-stu-id="f5c2a-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="f5c2a-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="f5c2a-112">-CompositePath</span></span>
<span data-ttu-id="f5c2a-113">類型為 Microsoft.Azure.Commands.AzsDB.PSCompositePath 的物件陣列</span><span class="sxs-lookup"><span data-stu-id="f5c2a-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="f5c2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c2a-114">-DefaultProfile</span></span>
<span data-ttu-id="f5c2a-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c2a-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="f5c2a-116">-ExcludedPath</span></span>
<span data-ttu-id="f5c2a-117">包含排除Path 的字串陣列 (指定 JSON 檔內要排除在 Azure 一些 Db service.) 元素中的路徑。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="f5c2a-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="f5c2a-118">-IncludedPath</span></span>
<span data-ttu-id="f5c2a-119">包含 includedPath 的字串陣列 (指定要包含在 AzureAzings DB service.) 元素中的 JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="f5c2a-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="f5c2a-120">-IndexingMode</span></span>
<span data-ttu-id="f5c2a-121">表示索引模式。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-121">indicates the indexing mode.</span></span>
<span data-ttu-id="f5c2a-122">可能的值包括：'一致'、'延遲'、'無'</span><span class="sxs-lookup"><span data-stu-id="f5c2a-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="f5c2a-123">-空間分析</span><span class="sxs-lookup"><span data-stu-id="f5c2a-123">-SpatialSpec</span></span>
<span data-ttu-id="f5c2a-124">類型為 Microsoft.Azure.Commands.AzsDB.PSSpatialSpec 的物件陣列</span><span class="sxs-lookup"><span data-stu-id="f5c2a-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="f5c2a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c2a-125">CommonParameters</span></span>
<span data-ttu-id="f5c2a-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5c2a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c2a-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5c2a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c2a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f5c2a-128">INPUTS</span></span>

### <span data-ttu-id="f5c2a-129">沒有</span><span class="sxs-lookup"><span data-stu-id="f5c2a-129">None</span></span>

## <span data-ttu-id="f5c2a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f5c2a-130">OUTPUTS</span></span>

### <span data-ttu-id="f5c2a-131">Microsoft.Azure.Commands.AzsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f5c2a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="f5c2a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f5c2a-132">NOTES</span></span>

## <span data-ttu-id="f5c2a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5c2a-133">RELATED LINKS</span></span>
