---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912037"
---
# <span data-ttu-id="35315-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="35315-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="35315-102">簡介</span><span class="sxs-lookup"><span data-stu-id="35315-102">SYNOPSIS</span></span>
<span data-ttu-id="35315-103">建立新一代的GosDB MongoDB 索引。</span><span class="sxs-lookup"><span data-stu-id="35315-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="35315-104">語法</span><span class="sxs-lookup"><span data-stu-id="35315-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35315-105">描述</span><span class="sxs-lookup"><span data-stu-id="35315-105">DESCRIPTION</span></span>
<span data-ttu-id="35315-106">**New-AzCosmosDBMongoDBIndex** 會建立一個新的一個代斯DB MongoDB 索引。</span><span class="sxs-lookup"><span data-stu-id="35315-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="35315-107">例子</span><span class="sxs-lookup"><span data-stu-id="35315-107">EXAMPLES</span></span>

### <span data-ttu-id="35315-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="35315-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="35315-109">參數</span><span class="sxs-lookup"><span data-stu-id="35315-109">PARAMETERS</span></span>

### <span data-ttu-id="35315-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35315-110">-DefaultProfile</span></span>
<span data-ttu-id="35315-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="35315-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35315-112">-Key</span><span class="sxs-lookup"><span data-stu-id="35315-112">-Key</span></span>
<span data-ttu-id="35315-113">以字串表示的索引鍵值陣列。</span><span class="sxs-lookup"><span data-stu-id="35315-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="35315-114">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="35315-114">-TtlInSeconds</span></span>
<span data-ttu-id="35315-115">索引到期後的秒數。</span><span class="sxs-lookup"><span data-stu-id="35315-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="35315-116">-唯一</span><span class="sxs-lookup"><span data-stu-id="35315-116">-Unique</span></span>
<span data-ttu-id="35315-117">布林值以指出索引是否是唯一的。</span><span class="sxs-lookup"><span data-stu-id="35315-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="35315-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35315-118">CommonParameters</span></span>
<span data-ttu-id="35315-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="35315-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35315-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35315-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35315-121">輸入</span><span class="sxs-lookup"><span data-stu-id="35315-121">INPUTS</span></span>

### <span data-ttu-id="35315-122">沒有</span><span class="sxs-lookup"><span data-stu-id="35315-122">None</span></span>

## <span data-ttu-id="35315-123">輸出</span><span class="sxs-lookup"><span data-stu-id="35315-123">OUTPUTS</span></span>

### <span data-ttu-id="35315-124">Microsoft.Azure.Commands.AzsDB.models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="35315-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="35315-125">筆記</span><span class="sxs-lookup"><span data-stu-id="35315-125">NOTES</span></span>

## <span data-ttu-id="35315-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="35315-126">RELATED LINKS</span></span>
