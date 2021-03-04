---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: c9a50c833de9290e08ac211b52586d25e5082c59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904134"
---
# <span data-ttu-id="6dcad-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="6dcad-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="6dcad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6dcad-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcad-103">建立 PSIndexes 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="6dcad-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="6dcad-104">它可以傳遞為 Set-AzCosmosDBSqlIncludedPath 的參數值。</span><span class="sxs-lookup"><span data-stu-id="6dcad-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="6dcad-105">語法</span><span class="sxs-lookup"><span data-stu-id="6dcad-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dcad-106">描述</span><span class="sxs-lookup"><span data-stu-id="6dcad-106">DESCRIPTION</span></span>
<span data-ttu-id="6dcad-107">與 Sql API 的 IncludedPath 索引對應的物件。</span><span class="sxs-lookup"><span data-stu-id="6dcad-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="6dcad-108">例子</span><span class="sxs-lookup"><span data-stu-id="6dcad-108">EXAMPLES</span></span>

### <span data-ttu-id="6dcad-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="6dcad-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="6dcad-110">參數</span><span class="sxs-lookup"><span data-stu-id="6dcad-110">PARAMETERS</span></span>

### <span data-ttu-id="6dcad-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="6dcad-111">-DataType</span></span>
<span data-ttu-id="6dcad-112">已對之使用索引行為的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6dcad-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="6dcad-113">可能的值包括：'String'， 'Number'， 'Point'， '多邊形'， 'LineString'， 'MultiPolygon'</span><span class="sxs-lookup"><span data-stu-id="6dcad-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="6dcad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcad-114">-DefaultProfile</span></span>
<span data-ttu-id="6dcad-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dcad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dcad-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="6dcad-116">-Kind</span></span>
<span data-ttu-id="6dcad-117">表示索引的類型。</span><span class="sxs-lookup"><span data-stu-id="6dcad-117">Indicates the type of index.</span></span>
<span data-ttu-id="6dcad-118">可能的值包括：'雜湊'、'Range'、'空間'</span><span class="sxs-lookup"><span data-stu-id="6dcad-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="6dcad-119">-精確度</span><span class="sxs-lookup"><span data-stu-id="6dcad-119">-Precision</span></span>
<span data-ttu-id="6dcad-120">索引的精確度。</span><span class="sxs-lookup"><span data-stu-id="6dcad-120">The precision of the index.</span></span>
<span data-ttu-id="6dcad-121">-1 為最大精確度。</span><span class="sxs-lookup"><span data-stu-id="6dcad-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcad-122">CommonParameters</span></span>
<span data-ttu-id="6dcad-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6dcad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcad-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dcad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcad-125">輸入</span><span class="sxs-lookup"><span data-stu-id="6dcad-125">INPUTS</span></span>

### <span data-ttu-id="6dcad-126">沒有</span><span class="sxs-lookup"><span data-stu-id="6dcad-126">None</span></span>

## <span data-ttu-id="6dcad-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6dcad-127">OUTPUTS</span></span>

### <span data-ttu-id="6dcad-128">Microsoft.Azure.Commands.AzesDB.models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="6dcad-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="6dcad-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6dcad-129">NOTES</span></span>

## <span data-ttu-id="6dcad-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dcad-130">RELATED LINKS</span></span>
