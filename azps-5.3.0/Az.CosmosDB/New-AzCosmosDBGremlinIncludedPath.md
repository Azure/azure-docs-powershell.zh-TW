---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446083"
---
# <span data-ttu-id="f7875-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="f7875-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="f7875-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7875-102">SYNOPSIS</span></span>
<span data-ttu-id="f7875-103">建立 PSIncludedPath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="f7875-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="f7875-104">您可以將它作為 AzCosmosDBGremlinGraph 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="f7875-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="f7875-105">句法</span><span class="sxs-lookup"><span data-stu-id="f7875-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7875-106">說明</span><span class="sxs-lookup"><span data-stu-id="f7875-106">DESCRIPTION</span></span>
<span data-ttu-id="f7875-107">對應至 Gremlin API IncludedPath 的物件。</span><span class="sxs-lookup"><span data-stu-id="f7875-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="f7875-108">示例</span><span class="sxs-lookup"><span data-stu-id="f7875-108">EXAMPLES</span></span>

### <span data-ttu-id="f7875-109">範例1</span><span class="sxs-lookup"><span data-stu-id="f7875-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="f7875-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7875-110">PARAMETERS</span></span>

### <span data-ttu-id="f7875-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7875-111">-DefaultProfile</span></span>
<span data-ttu-id="f7875-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7875-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7875-113">-索引</span><span class="sxs-lookup"><span data-stu-id="f7875-113">-Index</span></span>
<span data-ttu-id="f7875-114">此路徑的索引清單</span><span class="sxs-lookup"><span data-stu-id="f7875-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="f7875-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f7875-115">-Path</span></span>
<span data-ttu-id="f7875-116">要套用索引行為的路徑。</span><span class="sxs-lookup"><span data-stu-id="f7875-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="f7875-117">索引路徑通常是從 root 開始，並以萬用字元 (/path/\* ) </span><span class="sxs-lookup"><span data-stu-id="f7875-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="f7875-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7875-118">CommonParameters</span></span>
<span data-ttu-id="f7875-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7875-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7875-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f7875-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7875-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f7875-121">INPUTS</span></span>

### <span data-ttu-id="f7875-122">所有</span><span class="sxs-lookup"><span data-stu-id="f7875-122">None</span></span>

## <span data-ttu-id="f7875-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f7875-123">OUTPUTS</span></span>

### <span data-ttu-id="f7875-124">PSIncludedPath 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f7875-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="f7875-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f7875-125">NOTES</span></span>

## <span data-ttu-id="f7875-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7875-126">RELATED LINKS</span></span>
