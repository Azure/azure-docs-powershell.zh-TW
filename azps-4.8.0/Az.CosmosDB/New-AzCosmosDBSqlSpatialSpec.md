---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136066"
---
# <span data-ttu-id="ae2cd-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ae2cd-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="ae2cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2cd-103">建立 PSSpatialSpec 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="ae2cd-104">您可以將它作為 AzCosmosDBSqlIndexingPolicy 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="ae2cd-105">句法</span><span class="sxs-lookup"><span data-stu-id="ae2cd-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae2cd-106">說明</span><span class="sxs-lookup"><span data-stu-id="ae2cd-106">DESCRIPTION</span></span>
<span data-ttu-id="ae2cd-107">建立與 Sql API 的 SpatialSpec 相對應的物件。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="ae2cd-108">示例</span><span class="sxs-lookup"><span data-stu-id="ae2cd-108">EXAMPLES</span></span>

### <span data-ttu-id="ae2cd-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ae2cd-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="ae2cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="ae2cd-110">PARAMETERS</span></span>

### <span data-ttu-id="ae2cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2cd-111">-DefaultProfile</span></span>
<span data-ttu-id="ae2cd-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2cd-113">-Path</span><span class="sxs-lookup"><span data-stu-id="ae2cd-113">-Path</span></span>
<span data-ttu-id="ae2cd-114">要建立索引的 JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="ae2cd-115">-類型</span><span class="sxs-lookup"><span data-stu-id="ae2cd-115">-Type</span></span>
<span data-ttu-id="ae2cd-116">含可接受值的字串陣列： Point、LineString、多邊、MultiPolygon。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="ae2cd-117">代表的路徑空間類型。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="ae2cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2cd-118">CommonParameters</span></span>
<span data-ttu-id="ae2cd-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2cd-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2cd-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ae2cd-121">INPUTS</span></span>

### <span data-ttu-id="ae2cd-122">所有</span><span class="sxs-lookup"><span data-stu-id="ae2cd-122">None</span></span>

## <span data-ttu-id="ae2cd-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ae2cd-123">OUTPUTS</span></span>

### <span data-ttu-id="ae2cd-124">PSSpatialSpec 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="ae2cd-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="ae2cd-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ae2cd-125">NOTES</span></span>

## <span data-ttu-id="ae2cd-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae2cd-126">RELATED LINKS</span></span>