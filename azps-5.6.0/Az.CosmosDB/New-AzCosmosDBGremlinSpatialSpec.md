---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 8285afa9ba3764058f12ef0d8bfae009735a5ca3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903285"
---
# <span data-ttu-id="6a49a-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="6a49a-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="6a49a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a49a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a49a-103">建立 PSSpatialSpec 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="6a49a-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="6a49a-104">它可以傳遞為 Set-AzCosmosDBGremlinIndexingPolicy 的參數值。</span><span class="sxs-lookup"><span data-stu-id="6a49a-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="6a49a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a49a-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a49a-106">描述</span><span class="sxs-lookup"><span data-stu-id="6a49a-106">DESCRIPTION</span></span>
<span data-ttu-id="6a49a-107">建立對應到亞美林 API 的可空間Spec 的物件。</span><span class="sxs-lookup"><span data-stu-id="6a49a-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="6a49a-108">例子</span><span class="sxs-lookup"><span data-stu-id="6a49a-108">EXAMPLES</span></span>

### <span data-ttu-id="6a49a-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="6a49a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="6a49a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6a49a-110">PARAMETERS</span></span>

### <span data-ttu-id="6a49a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a49a-111">-DefaultProfile</span></span>
<span data-ttu-id="6a49a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a49a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a49a-113">-路徑</span><span class="sxs-lookup"><span data-stu-id="6a49a-113">-Path</span></span>
<span data-ttu-id="6a49a-114">JSON 檔中要編制索引的路徑。</span><span class="sxs-lookup"><span data-stu-id="6a49a-114">Path in JSON document to index.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a49a-115">-類型</span><span class="sxs-lookup"><span data-stu-id="6a49a-115">-Type</span></span>
<span data-ttu-id="6a49a-116">包含可接受值的字串陣列：Point、LineString、多邊形、MultiPolygon。</span><span class="sxs-lookup"><span data-stu-id="6a49a-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="6a49a-117">代表路徑的空間類型。</span><span class="sxs-lookup"><span data-stu-id="6a49a-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a49a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a49a-118">CommonParameters</span></span>
<span data-ttu-id="6a49a-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a49a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a49a-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a49a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a49a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="6a49a-121">INPUTS</span></span>

### <span data-ttu-id="6a49a-122">沒有</span><span class="sxs-lookup"><span data-stu-id="6a49a-122">None</span></span>

## <span data-ttu-id="6a49a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6a49a-123">OUTPUTS</span></span>

### <span data-ttu-id="6a49a-124">Microsoft.Azure.Commands.AzsDB.models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="6a49a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="6a49a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="6a49a-125">NOTES</span></span>

## <span data-ttu-id="6a49a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a49a-126">RELATED LINKS</span></span>
