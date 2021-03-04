---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: b172c5e22c26cba8d88d188198868da720d611d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911717"
---
# <span data-ttu-id="76879-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="76879-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="76879-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76879-102">SYNOPSIS</span></span>
<span data-ttu-id="76879-103">建立新一個一次管理中心 SQL UniqueKey 物件。</span><span class="sxs-lookup"><span data-stu-id="76879-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="76879-104">語法</span><span class="sxs-lookup"><span data-stu-id="76879-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76879-105">描述</span><span class="sxs-lookup"><span data-stu-id="76879-105">DESCRIPTION</span></span>
<span data-ttu-id="76879-106">**New-AzCosmosDBSqlUniqueKey** Cmdlet 會建立 PSUniqueKey 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="76879-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="76879-107">例子</span><span class="sxs-lookup"><span data-stu-id="76879-107">EXAMPLES</span></span>

### <span data-ttu-id="76879-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="76879-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="76879-109">參數</span><span class="sxs-lookup"><span data-stu-id="76879-109">PARAMETERS</span></span>

### <span data-ttu-id="76879-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76879-110">-DefaultProfile</span></span>
<span data-ttu-id="76879-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76879-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76879-112">-路徑</span><span class="sxs-lookup"><span data-stu-id="76879-112">-Path</span></span>
<span data-ttu-id="76879-113">路徑值字串陣列</span><span class="sxs-lookup"><span data-stu-id="76879-113">Array of string of path values</span></span>

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

### <span data-ttu-id="76879-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76879-114">CommonParameters</span></span>
<span data-ttu-id="76879-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76879-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76879-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76879-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76879-117">輸入</span><span class="sxs-lookup"><span data-stu-id="76879-117">INPUTS</span></span>

### <span data-ttu-id="76879-118">沒有</span><span class="sxs-lookup"><span data-stu-id="76879-118">None</span></span>

## <span data-ttu-id="76879-119">輸出</span><span class="sxs-lookup"><span data-stu-id="76879-119">OUTPUTS</span></span>

### <span data-ttu-id="76879-120">Microsoft.Azure.Commands.AzsDB.models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="76879-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="76879-121">筆記</span><span class="sxs-lookup"><span data-stu-id="76879-121">NOTES</span></span>

## <span data-ttu-id="76879-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="76879-122">RELATED LINKS</span></span>
