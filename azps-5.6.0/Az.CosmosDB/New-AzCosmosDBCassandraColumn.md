---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 634a6a8e1e6b921703603ee7f2bfd345aa64608c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916772"
---
# <span data-ttu-id="6ff2d-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="6ff2d-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="6ff2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ff2d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff2d-103">建立新一個花式資料庫的卡薩德拉直條圖。</span><span class="sxs-lookup"><span data-stu-id="6ff2d-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="6ff2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ff2d-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ff2d-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ff2d-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff2d-106">**New-AzCosmosDBCassandraColumn** 會建立新一個以一欄為標題的一欄。</span><span class="sxs-lookup"><span data-stu-id="6ff2d-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="6ff2d-107">例子</span><span class="sxs-lookup"><span data-stu-id="6ff2d-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff2d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6ff2d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="6ff2d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6ff2d-109">PARAMETERS</span></span>

### <span data-ttu-id="6ff2d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff2d-110">-DefaultProfile</span></span>
<span data-ttu-id="6ff2d-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ff2d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff2d-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ff2d-112">-Name</span></span>
<span data-ttu-id="6ff2d-113">雅可拉欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ff2d-113">Name of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff2d-114">-類型</span><span class="sxs-lookup"><span data-stu-id="6ff2d-114">-Type</span></span>
<span data-ttu-id="6ff2d-115">卡薩蘭拉欄的類型。</span><span class="sxs-lookup"><span data-stu-id="6ff2d-115">Type of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff2d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff2d-116">CommonParameters</span></span>
<span data-ttu-id="6ff2d-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ff2d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff2d-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ff2d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff2d-119">輸入</span><span class="sxs-lookup"><span data-stu-id="6ff2d-119">INPUTS</span></span>

### <span data-ttu-id="6ff2d-120">沒有</span><span class="sxs-lookup"><span data-stu-id="6ff2d-120">None</span></span>

## <span data-ttu-id="6ff2d-121">輸出</span><span class="sxs-lookup"><span data-stu-id="6ff2d-121">OUTPUTS</span></span>

### <span data-ttu-id="6ff2d-122">Microsoft.Azure.Commands.AzsDB.models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="6ff2d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="6ff2d-123">筆記</span><span class="sxs-lookup"><span data-stu-id="6ff2d-123">NOTES</span></span>

## <span data-ttu-id="6ff2d-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ff2d-124">RELATED LINKS</span></span>
