---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: e22c8931cf70fba970e71b7a2d099cda725287d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915534"
---
# <span data-ttu-id="52ff7-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="52ff7-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="52ff7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="52ff7-103">建立 PSSpatialSpec 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="52ff7-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="52ff7-104">它可以傳遞為 Set-AzCosmosDBSqlIndexingPolicy 的參數值。</span><span class="sxs-lookup"><span data-stu-id="52ff7-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="52ff7-105">語法</span><span class="sxs-lookup"><span data-stu-id="52ff7-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52ff7-106">描述</span><span class="sxs-lookup"><span data-stu-id="52ff7-106">DESCRIPTION</span></span>
<span data-ttu-id="52ff7-107">建立對應至 Sql API 的空間Spec 的物件。</span><span class="sxs-lookup"><span data-stu-id="52ff7-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="52ff7-108">例子</span><span class="sxs-lookup"><span data-stu-id="52ff7-108">EXAMPLES</span></span>

### <span data-ttu-id="52ff7-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="52ff7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="52ff7-110">參數</span><span class="sxs-lookup"><span data-stu-id="52ff7-110">PARAMETERS</span></span>

### <span data-ttu-id="52ff7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ff7-111">-DefaultProfile</span></span>
<span data-ttu-id="52ff7-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="52ff7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ff7-113">-路徑</span><span class="sxs-lookup"><span data-stu-id="52ff7-113">-Path</span></span>
<span data-ttu-id="52ff7-114">JSON 檔中要編制索引的路徑。</span><span class="sxs-lookup"><span data-stu-id="52ff7-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="52ff7-115">-類型</span><span class="sxs-lookup"><span data-stu-id="52ff7-115">-Type</span></span>
<span data-ttu-id="52ff7-116">包含可接受值的字串陣列：Point、LineString、多邊形、MultiPolygon。</span><span class="sxs-lookup"><span data-stu-id="52ff7-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="52ff7-117">代表路徑的空間類型。</span><span class="sxs-lookup"><span data-stu-id="52ff7-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="52ff7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ff7-118">CommonParameters</span></span>
<span data-ttu-id="52ff7-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52ff7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ff7-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52ff7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ff7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="52ff7-121">INPUTS</span></span>

### <span data-ttu-id="52ff7-122">沒有</span><span class="sxs-lookup"><span data-stu-id="52ff7-122">None</span></span>

## <span data-ttu-id="52ff7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="52ff7-123">OUTPUTS</span></span>

### <span data-ttu-id="52ff7-124">Microsoft.Azure.Commands.AzsDB.models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="52ff7-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="52ff7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="52ff7-125">NOTES</span></span>

## <span data-ttu-id="52ff7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="52ff7-126">RELATED LINKS</span></span>
