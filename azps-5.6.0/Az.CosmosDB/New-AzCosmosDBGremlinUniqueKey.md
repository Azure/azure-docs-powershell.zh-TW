---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914134"
---
# <span data-ttu-id="0a9b2-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0a9b2-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="0a9b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9b2-103">建立一個新的部格DB UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="0a9b2-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="0a9b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a9b2-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a9b2-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="0a9b2-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet 會建立 PSUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="0a9b2-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="0a9b2-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a9b2-107">EXAMPLES</span></span>

### <span data-ttu-id="0a9b2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0a9b2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="0a9b2-109">參數</span><span class="sxs-lookup"><span data-stu-id="0a9b2-109">PARAMETERS</span></span>

### <span data-ttu-id="0a9b2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9b2-110">-DefaultProfile</span></span>
<span data-ttu-id="0a9b2-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a9b2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a9b2-112">-路徑</span><span class="sxs-lookup"><span data-stu-id="0a9b2-112">-Path</span></span>
<span data-ttu-id="0a9b2-113">路徑值字串陣列</span><span class="sxs-lookup"><span data-stu-id="0a9b2-113">Array of string of path values</span></span>

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

### <span data-ttu-id="0a9b2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9b2-114">CommonParameters</span></span>
<span data-ttu-id="0a9b2-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a9b2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9b2-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a9b2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9b2-117">輸入</span><span class="sxs-lookup"><span data-stu-id="0a9b2-117">INPUTS</span></span>

### <span data-ttu-id="0a9b2-118">沒有</span><span class="sxs-lookup"><span data-stu-id="0a9b2-118">None</span></span>

## <span data-ttu-id="0a9b2-119">輸出</span><span class="sxs-lookup"><span data-stu-id="0a9b2-119">OUTPUTS</span></span>

### <span data-ttu-id="0a9b2-120">Microsoft.Azure.Commands.AzsDB.models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0a9b2-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="0a9b2-121">筆記</span><span class="sxs-lookup"><span data-stu-id="0a9b2-121">NOTES</span></span>

## <span data-ttu-id="0a9b2-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a9b2-122">RELATED LINKS</span></span>
