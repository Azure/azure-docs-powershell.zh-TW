---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904530"
---
# <span data-ttu-id="8544e-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="8544e-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="8544e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8544e-102">SYNOPSIS</span></span>
<span data-ttu-id="8544e-103">建立 PSIncludedPath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="8544e-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="8544e-104">它可以傳遞為 Set-AzCosmosDBSqlContainer 的參數值。</span><span class="sxs-lookup"><span data-stu-id="8544e-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="8544e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8544e-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8544e-106">描述</span><span class="sxs-lookup"><span data-stu-id="8544e-106">DESCRIPTION</span></span>
<span data-ttu-id="8544e-107">對應至 Sql API 的 IncludedPath 的物件。</span><span class="sxs-lookup"><span data-stu-id="8544e-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="8544e-108">例子</span><span class="sxs-lookup"><span data-stu-id="8544e-108">EXAMPLES</span></span>

### <span data-ttu-id="8544e-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="8544e-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="8544e-110">參數</span><span class="sxs-lookup"><span data-stu-id="8544e-110">PARAMETERS</span></span>

### <span data-ttu-id="8544e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8544e-111">-DefaultProfile</span></span>
<span data-ttu-id="8544e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8544e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8544e-113">-索引</span><span class="sxs-lookup"><span data-stu-id="8544e-113">-Index</span></span>
<span data-ttu-id="8544e-114">此路徑的索引清單</span><span class="sxs-lookup"><span data-stu-id="8544e-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="8544e-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="8544e-115">-Path</span></span>
<span data-ttu-id="8544e-116">索引行為所適用的路徑。</span><span class="sxs-lookup"><span data-stu-id="8544e-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="8544e-117">索引路徑通常是從根目錄開始，結尾是萬用字元 (/path/\*) </span><span class="sxs-lookup"><span data-stu-id="8544e-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="8544e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8544e-118">CommonParameters</span></span>
<span data-ttu-id="8544e-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8544e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8544e-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8544e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8544e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8544e-121">INPUTS</span></span>

### <span data-ttu-id="8544e-122">沒有</span><span class="sxs-lookup"><span data-stu-id="8544e-122">None</span></span>

## <span data-ttu-id="8544e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8544e-123">OUTPUTS</span></span>

### <span data-ttu-id="8544e-124">Microsoft.Azure.Commands.AzsDB.models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="8544e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="8544e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8544e-125">NOTES</span></span>

## <span data-ttu-id="8544e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8544e-126">RELATED LINKS</span></span>
