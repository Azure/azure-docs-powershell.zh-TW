---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958027"
---
# <span data-ttu-id="98c77-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="98c77-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="98c77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98c77-102">SYNOPSIS</span></span>
<span data-ttu-id="98c77-103">建立 PSIndexes 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="98c77-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="98c77-104">您可以將它作為 AzCosmosDBGremlinIncludedPath 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="98c77-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="98c77-105">句法</span><span class="sxs-lookup"><span data-stu-id="98c77-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c77-106">說明</span><span class="sxs-lookup"><span data-stu-id="98c77-106">DESCRIPTION</span></span>
<span data-ttu-id="98c77-107">與 Gremlin API 的 IncludedPath's 索引相對應的物件。</span><span class="sxs-lookup"><span data-stu-id="98c77-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="98c77-108">示例</span><span class="sxs-lookup"><span data-stu-id="98c77-108">EXAMPLES</span></span>

### <span data-ttu-id="98c77-109">範例1</span><span class="sxs-lookup"><span data-stu-id="98c77-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="98c77-110">參數</span><span class="sxs-lookup"><span data-stu-id="98c77-110">PARAMETERS</span></span>

### <span data-ttu-id="98c77-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="98c77-111">-DataType</span></span>
<span data-ttu-id="98c77-112">要套用索引行為的資料類型。</span><span class="sxs-lookup"><span data-stu-id="98c77-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="98c77-113">可能的值包括： "String"、"Number"、"Point"、"多邊形"、"LineString"、"MultiPolygon"</span><span class="sxs-lookup"><span data-stu-id="98c77-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="98c77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c77-114">-DefaultProfile</span></span>
<span data-ttu-id="98c77-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98c77-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c77-116">類型</span><span class="sxs-lookup"><span data-stu-id="98c77-116">-Kind</span></span>
<span data-ttu-id="98c77-117">指出索引的類型。</span><span class="sxs-lookup"><span data-stu-id="98c77-117">Indicates the type of index.</span></span>
<span data-ttu-id="98c77-118">可能的值包括： "Hash"，"範圍"，"空間"</span><span class="sxs-lookup"><span data-stu-id="98c77-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="98c77-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="98c77-119">-Precision</span></span>
<span data-ttu-id="98c77-120">索引的精確度。</span><span class="sxs-lookup"><span data-stu-id="98c77-120">The precision of the index.</span></span>
<span data-ttu-id="98c77-121">-1 是最大精確度。</span><span class="sxs-lookup"><span data-stu-id="98c77-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="98c77-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c77-122">CommonParameters</span></span>
<span data-ttu-id="98c77-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98c77-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c77-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98c77-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c77-125">輸入</span><span class="sxs-lookup"><span data-stu-id="98c77-125">INPUTS</span></span>

### <span data-ttu-id="98c77-126">所有</span><span class="sxs-lookup"><span data-stu-id="98c77-126">None</span></span>

## <span data-ttu-id="98c77-127">輸出</span><span class="sxs-lookup"><span data-stu-id="98c77-127">OUTPUTS</span></span>

### <span data-ttu-id="98c77-128">PSIndexes 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="98c77-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="98c77-129">筆記</span><span class="sxs-lookup"><span data-stu-id="98c77-129">NOTES</span></span>

## <span data-ttu-id="98c77-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="98c77-130">RELATED LINKS</span></span>