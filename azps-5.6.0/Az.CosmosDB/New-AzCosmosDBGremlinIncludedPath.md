---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: c3022ea8f2ddbfbf0fc2a51bfd63706c4a8ea884
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903286"
---
# <span data-ttu-id="25551-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="25551-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="25551-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25551-102">SYNOPSIS</span></span>
<span data-ttu-id="25551-103">建立 PSIncludedPath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="25551-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="25551-104">它可以傳遞為 Set-AzCosmosDBGremlinGraph 的參數值。</span><span class="sxs-lookup"><span data-stu-id="25551-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="25551-105">語法</span><span class="sxs-lookup"><span data-stu-id="25551-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25551-106">描述</span><span class="sxs-lookup"><span data-stu-id="25551-106">DESCRIPTION</span></span>
<span data-ttu-id="25551-107">對應到資料 Api 的 IncludedPath 的物件。</span><span class="sxs-lookup"><span data-stu-id="25551-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="25551-108">例子</span><span class="sxs-lookup"><span data-stu-id="25551-108">EXAMPLES</span></span>

### <span data-ttu-id="25551-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="25551-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="25551-110">參數</span><span class="sxs-lookup"><span data-stu-id="25551-110">PARAMETERS</span></span>

### <span data-ttu-id="25551-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25551-111">-DefaultProfile</span></span>
<span data-ttu-id="25551-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25551-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25551-113">-索引</span><span class="sxs-lookup"><span data-stu-id="25551-113">-Index</span></span>
<span data-ttu-id="25551-114">此路徑的索引清單</span><span class="sxs-lookup"><span data-stu-id="25551-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25551-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="25551-115">-Path</span></span>
<span data-ttu-id="25551-116">索引行為所適用的路徑。</span><span class="sxs-lookup"><span data-stu-id="25551-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="25551-117">索引路徑通常是從根目錄開始，結尾是萬用字元 (/path/\*) </span><span class="sxs-lookup"><span data-stu-id="25551-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="25551-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25551-118">CommonParameters</span></span>
<span data-ttu-id="25551-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25551-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25551-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25551-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25551-121">輸入</span><span class="sxs-lookup"><span data-stu-id="25551-121">INPUTS</span></span>

### <span data-ttu-id="25551-122">沒有</span><span class="sxs-lookup"><span data-stu-id="25551-122">None</span></span>

## <span data-ttu-id="25551-123">輸出</span><span class="sxs-lookup"><span data-stu-id="25551-123">OUTPUTS</span></span>

### <span data-ttu-id="25551-124">Microsoft.Azure.Commands.AzsDB.models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="25551-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="25551-125">筆記</span><span class="sxs-lookup"><span data-stu-id="25551-125">NOTES</span></span>

## <span data-ttu-id="25551-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="25551-126">RELATED LINKS</span></span>
