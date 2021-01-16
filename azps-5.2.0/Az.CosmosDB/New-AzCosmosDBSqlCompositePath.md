---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282960"
---
# <span data-ttu-id="0b98c-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="0b98c-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="0b98c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b98c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b98c-103">建立 PSCompositePath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="0b98c-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="0b98c-104">您可以將它作為 AzCosmosDBSqlContainer 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="0b98c-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="0b98c-105">句法</span><span class="sxs-lookup"><span data-stu-id="0b98c-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b98c-106">說明</span><span class="sxs-lookup"><span data-stu-id="0b98c-106">DESCRIPTION</span></span>
<span data-ttu-id="0b98c-107">與 Sql API 的 CompositePath 相對應的物件。</span><span class="sxs-lookup"><span data-stu-id="0b98c-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="0b98c-108">示例</span><span class="sxs-lookup"><span data-stu-id="0b98c-108">EXAMPLES</span></span>

### <span data-ttu-id="0b98c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="0b98c-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="0b98c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b98c-110">PARAMETERS</span></span>

### <span data-ttu-id="0b98c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b98c-111">-DefaultProfile</span></span>
<span data-ttu-id="0b98c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b98c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b98c-113">-訂單</span><span class="sxs-lookup"><span data-stu-id="0b98c-113">-Order</span></span>
<span data-ttu-id="0b98c-114">取得或設定複合路徑的排序次序。</span><span class="sxs-lookup"><span data-stu-id="0b98c-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="0b98c-115">可能的值包括： [昇冪]、"遞減"</span><span class="sxs-lookup"><span data-stu-id="0b98c-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="0b98c-116">-Path</span><span class="sxs-lookup"><span data-stu-id="0b98c-116">-Path</span></span>
<span data-ttu-id="0b98c-117">要套用索引行為的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b98c-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="0b98c-118">索引路徑通常是從 root 開始，並以萬用字元 (/path/\* ) </span><span class="sxs-lookup"><span data-stu-id="0b98c-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="0b98c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b98c-119">CommonParameters</span></span>
<span data-ttu-id="0b98c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b98c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b98c-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b98c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b98c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0b98c-122">INPUTS</span></span>

### <span data-ttu-id="0b98c-123">所有</span><span class="sxs-lookup"><span data-stu-id="0b98c-123">None</span></span>

## <span data-ttu-id="0b98c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0b98c-124">OUTPUTS</span></span>

### <span data-ttu-id="0b98c-125">PSCompositePath 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="0b98c-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="0b98c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0b98c-126">NOTES</span></span>

## <span data-ttu-id="0b98c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b98c-127">RELATED LINKS</span></span>
