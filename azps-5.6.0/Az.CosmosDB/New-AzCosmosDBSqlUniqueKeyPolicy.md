---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910726"
---
# <span data-ttu-id="4ec9a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4ec9a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="4ec9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ec9a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec9a-103">建立新一代的代斯DB SqlUniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="4ec9a-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="4ec9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ec9a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec9a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4ec9a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec9a-106">**New-AzCosmosDBSqlUniqueKeyPolicy** Cmdlet 會建立 PSSqlUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="4ec9a-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="4ec9a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4ec9a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec9a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4ec9a-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="4ec9a-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ec9a-109">PARAMETERS</span></span>

### <span data-ttu-id="4ec9a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec9a-110">-DefaultProfile</span></span>
<span data-ttu-id="4ec9a-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ec9a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec9a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="4ec9a-112">-UniqueKey</span></span>
<span data-ttu-id="4ec9a-113">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4ec9a-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec9a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec9a-114">CommonParameters</span></span>
<span data-ttu-id="4ec9a-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ec9a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec9a-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ec9a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec9a-117">輸入</span><span class="sxs-lookup"><span data-stu-id="4ec9a-117">INPUTS</span></span>

### <span data-ttu-id="4ec9a-118">沒有</span><span class="sxs-lookup"><span data-stu-id="4ec9a-118">None</span></span>

## <span data-ttu-id="4ec9a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="4ec9a-119">OUTPUTS</span></span>

### <span data-ttu-id="4ec9a-120">Microsoft.Azure.Commands.AzsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4ec9a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="4ec9a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="4ec9a-121">NOTES</span></span>

## <span data-ttu-id="4ec9a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ec9a-122">RELATED LINKS</span></span>
