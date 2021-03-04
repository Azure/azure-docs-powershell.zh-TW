---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: ce554f3591f022bdbc375c12a50ea9dae85b8baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914141"
---
# <span data-ttu-id="25759-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="25759-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="25759-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25759-102">SYNOPSIS</span></span>
<span data-ttu-id="25759-103">建立一個新的管理中心DB IndexingPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="25759-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="25759-104">語法</span><span class="sxs-lookup"><span data-stu-id="25759-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25759-105">描述</span><span class="sxs-lookup"><span data-stu-id="25759-105">DESCRIPTION</span></span>
<span data-ttu-id="25759-106">**New-AzCosmosDBGremlinIndexingPolidlet** 會建立 PSIndexingPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="25759-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="25759-107">例子</span><span class="sxs-lookup"><span data-stu-id="25759-107">EXAMPLES</span></span>

### <span data-ttu-id="25759-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="25759-108">Example 1</span></span>
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

<span data-ttu-id="25759-109">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="25759-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="25759-110">參數</span><span class="sxs-lookup"><span data-stu-id="25759-110">PARAMETERS</span></span>

### <span data-ttu-id="25759-111">-自動</span><span class="sxs-lookup"><span data-stu-id="25759-111">-Automatic</span></span>
<span data-ttu-id="25759-112">布林值以指出索引編制政策是否自動</span><span class="sxs-lookup"><span data-stu-id="25759-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="25759-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="25759-113">-CompositePath</span></span>
<span data-ttu-id="25759-114">類型為 Microsoft.Azure.Commands.AzsDB.PSCompositePath 的物件陣列</span><span class="sxs-lookup"><span data-stu-id="25759-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="25759-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25759-115">-DefaultProfile</span></span>
<span data-ttu-id="25759-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25759-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25759-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="25759-117">-ExcludedPath</span></span>
<span data-ttu-id="25759-118">包含排除Path 的字串陣列 (指定 JSON 檔內要排除在 Azure 一些 Db service.) 元素中的路徑。</span><span class="sxs-lookup"><span data-stu-id="25759-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="25759-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="25759-119">-IncludedPath</span></span>
<span data-ttu-id="25759-120">包含 includedPath 的字串陣列 (指定要包含在 AzureAzings DB service.) 元素中的 JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="25759-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="25759-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="25759-121">-IndexingMode</span></span>
<span data-ttu-id="25759-122">表示索引模式。</span><span class="sxs-lookup"><span data-stu-id="25759-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="25759-123">可能的值包括：'一致'、'延遲'、'無'</span><span class="sxs-lookup"><span data-stu-id="25759-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="25759-124">-空間分析</span><span class="sxs-lookup"><span data-stu-id="25759-124">-SpatialSpec</span></span>
<span data-ttu-id="25759-125">類型為 Microsoft.Azure.Commands.AzsDB.PSSpatialSpec 的物件陣列</span><span class="sxs-lookup"><span data-stu-id="25759-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="25759-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25759-126">CommonParameters</span></span>
<span data-ttu-id="25759-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25759-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25759-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25759-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25759-129">輸入</span><span class="sxs-lookup"><span data-stu-id="25759-129">INPUTS</span></span>

### <span data-ttu-id="25759-130">沒有</span><span class="sxs-lookup"><span data-stu-id="25759-130">None</span></span>

## <span data-ttu-id="25759-131">輸出</span><span class="sxs-lookup"><span data-stu-id="25759-131">OUTPUTS</span></span>

### <span data-ttu-id="25759-132">Microsoft.Azure.Commands.AzsDB.models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="25759-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="25759-133">筆記</span><span class="sxs-lookup"><span data-stu-id="25759-133">NOTES</span></span>

## <span data-ttu-id="25759-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="25759-134">RELATED LINKS</span></span>
