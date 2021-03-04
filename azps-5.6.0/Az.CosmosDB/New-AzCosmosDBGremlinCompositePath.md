---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: c88cde11d277a4a2e0473d41f83e1b62e13216bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916425"
---
# <span data-ttu-id="ad746-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="ad746-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="ad746-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad746-102">SYNOPSIS</span></span>
<span data-ttu-id="ad746-103">建立 PSCompositePath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="ad746-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="ad746-104">它可以傳遞為 Set-AzCosmosDBGremlinGraph 的參數值。</span><span class="sxs-lookup"><span data-stu-id="ad746-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="ad746-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad746-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad746-106">描述</span><span class="sxs-lookup"><span data-stu-id="ad746-106">DESCRIPTION</span></span>
<span data-ttu-id="ad746-107">對應至亞美林 API 的 CompositePath 的物件。</span><span class="sxs-lookup"><span data-stu-id="ad746-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="ad746-108">例子</span><span class="sxs-lookup"><span data-stu-id="ad746-108">EXAMPLES</span></span>

### <span data-ttu-id="ad746-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="ad746-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="ad746-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad746-110">PARAMETERS</span></span>

### <span data-ttu-id="ad746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad746-111">-DefaultProfile</span></span>
<span data-ttu-id="ad746-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad746-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad746-113">-訂單</span><span class="sxs-lookup"><span data-stu-id="ad746-113">-Order</span></span>
<span data-ttu-id="ad746-114">為複合路徑獲取或設定排序次序。</span><span class="sxs-lookup"><span data-stu-id="ad746-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="ad746-115">可能的值包括：'遞增'，'遞減'</span><span class="sxs-lookup"><span data-stu-id="ad746-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="ad746-116">-路徑</span><span class="sxs-lookup"><span data-stu-id="ad746-116">-Path</span></span>
<span data-ttu-id="ad746-117">索引行為所適用的路徑。</span><span class="sxs-lookup"><span data-stu-id="ad746-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="ad746-118">索引路徑通常是從根目錄開始，結尾是萬用字元 (/path/\*) </span><span class="sxs-lookup"><span data-stu-id="ad746-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="ad746-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad746-119">CommonParameters</span></span>
<span data-ttu-id="ad746-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad746-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad746-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad746-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad746-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ad746-122">INPUTS</span></span>

### <span data-ttu-id="ad746-123">沒有</span><span class="sxs-lookup"><span data-stu-id="ad746-123">None</span></span>

## <span data-ttu-id="ad746-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ad746-124">OUTPUTS</span></span>

### <span data-ttu-id="ad746-125">Microsoft.Azure.Commands.AzosDB.models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="ad746-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="ad746-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ad746-126">NOTES</span></span>

## <span data-ttu-id="ad746-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad746-127">RELATED LINKS</span></span>
