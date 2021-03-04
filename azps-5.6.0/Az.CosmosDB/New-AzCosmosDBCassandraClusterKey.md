---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: 9afcffc281c48e0235c814b352e65ae47e5f4337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916644"
---
# <span data-ttu-id="3f50b-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="3f50b-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="3f50b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f50b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f50b-103">建立新一個集中式集區鍵。</span><span class="sxs-lookup"><span data-stu-id="3f50b-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="3f50b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f50b-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f50b-105">描述</span><span class="sxs-lookup"><span data-stu-id="3f50b-105">DESCRIPTION</span></span>
<span data-ttu-id="3f50b-106">**New-AzCosmosDBCassandraClusterKey** 會建立一個新的一個花式資料庫卡薩德拉叢集鍵。</span><span class="sxs-lookup"><span data-stu-id="3f50b-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="3f50b-107">例子</span><span class="sxs-lookup"><span data-stu-id="3f50b-107">EXAMPLES</span></span>

### <span data-ttu-id="3f50b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3f50b-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="3f50b-109">參數</span><span class="sxs-lookup"><span data-stu-id="3f50b-109">PARAMETERS</span></span>

### <span data-ttu-id="3f50b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f50b-110">-DefaultProfile</span></span>
<span data-ttu-id="3f50b-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f50b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f50b-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f50b-112">-Name</span></span>
<span data-ttu-id="3f50b-113">Cassandra Cluster Key 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f50b-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="3f50b-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="3f50b-114">-OrderBy</span></span>
<span data-ttu-id="3f50b-115">成序的雅甘拉集區鍵。</span><span class="sxs-lookup"><span data-stu-id="3f50b-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="3f50b-116">可能的值包括：'Asc'，'Desc'</span><span class="sxs-lookup"><span data-stu-id="3f50b-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="3f50b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f50b-117">CommonParameters</span></span>
<span data-ttu-id="3f50b-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f50b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f50b-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f50b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f50b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3f50b-120">INPUTS</span></span>

### <span data-ttu-id="3f50b-121">沒有</span><span class="sxs-lookup"><span data-stu-id="3f50b-121">None</span></span>

## <span data-ttu-id="3f50b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="3f50b-122">OUTPUTS</span></span>

### <span data-ttu-id="3f50b-123">Microsoft.Azure.Commands.AzsDB.models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="3f50b-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="3f50b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3f50b-124">NOTES</span></span>

## <span data-ttu-id="3f50b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f50b-125">RELATED LINKS</span></span>
