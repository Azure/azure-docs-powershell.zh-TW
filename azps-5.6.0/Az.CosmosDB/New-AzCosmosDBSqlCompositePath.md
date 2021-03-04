---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: de91a7bb3fc1f4321cf344aa975c14c3976dfdbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908598"
---
# <span data-ttu-id="47f98-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="47f98-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="47f98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47f98-102">SYNOPSIS</span></span>
<span data-ttu-id="47f98-103">建立 PSCompositePath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="47f98-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="47f98-104">它可以傳遞為 Set-AzCosmosDBSqlContainer 的參數值。</span><span class="sxs-lookup"><span data-stu-id="47f98-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="47f98-105">語法</span><span class="sxs-lookup"><span data-stu-id="47f98-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47f98-106">描述</span><span class="sxs-lookup"><span data-stu-id="47f98-106">DESCRIPTION</span></span>
<span data-ttu-id="47f98-107">與 Sql API 的 CompositePath 對應的物件。</span><span class="sxs-lookup"><span data-stu-id="47f98-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="47f98-108">例子</span><span class="sxs-lookup"><span data-stu-id="47f98-108">EXAMPLES</span></span>

### <span data-ttu-id="47f98-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="47f98-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="47f98-110">參數</span><span class="sxs-lookup"><span data-stu-id="47f98-110">PARAMETERS</span></span>

### <span data-ttu-id="47f98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f98-111">-DefaultProfile</span></span>
<span data-ttu-id="47f98-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47f98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47f98-113">-訂單</span><span class="sxs-lookup"><span data-stu-id="47f98-113">-Order</span></span>
<span data-ttu-id="47f98-114">為複合路徑獲取或設定排序次序。</span><span class="sxs-lookup"><span data-stu-id="47f98-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="47f98-115">可能的值包括：'遞增'，'遞減'</span><span class="sxs-lookup"><span data-stu-id="47f98-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="47f98-116">-路徑</span><span class="sxs-lookup"><span data-stu-id="47f98-116">-Path</span></span>
<span data-ttu-id="47f98-117">索引行為所適用的路徑。</span><span class="sxs-lookup"><span data-stu-id="47f98-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="47f98-118">索引路徑通常是從根目錄開始，結尾是萬用字元 (/path/\*) </span><span class="sxs-lookup"><span data-stu-id="47f98-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="47f98-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f98-119">CommonParameters</span></span>
<span data-ttu-id="47f98-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47f98-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f98-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47f98-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f98-122">輸入</span><span class="sxs-lookup"><span data-stu-id="47f98-122">INPUTS</span></span>

### <span data-ttu-id="47f98-123">沒有</span><span class="sxs-lookup"><span data-stu-id="47f98-123">None</span></span>

## <span data-ttu-id="47f98-124">輸出</span><span class="sxs-lookup"><span data-stu-id="47f98-124">OUTPUTS</span></span>

### <span data-ttu-id="47f98-125">Microsoft.Azure.Commands.AzosDB.models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="47f98-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="47f98-126">筆記</span><span class="sxs-lookup"><span data-stu-id="47f98-126">NOTES</span></span>

## <span data-ttu-id="47f98-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="47f98-127">RELATED LINKS</span></span>
