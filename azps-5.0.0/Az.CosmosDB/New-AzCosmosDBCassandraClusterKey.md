---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285534"
---
# <span data-ttu-id="b15af-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="b15af-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="b15af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b15af-102">SYNOPSIS</span></span>
<span data-ttu-id="b15af-103">建立新的 CosmosDB Cassandra 群集金鑰。</span><span class="sxs-lookup"><span data-stu-id="b15af-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="b15af-104">句法</span><span class="sxs-lookup"><span data-stu-id="b15af-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b15af-105">說明</span><span class="sxs-lookup"><span data-stu-id="b15af-105">DESCRIPTION</span></span>
<span data-ttu-id="b15af-106">**新的-AzCosmosDBCassandraClusterKey** 會建立新的 CosmosDB Cassandra 群集金鑰。</span><span class="sxs-lookup"><span data-stu-id="b15af-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="b15af-107">示例</span><span class="sxs-lookup"><span data-stu-id="b15af-107">EXAMPLES</span></span>

### <span data-ttu-id="b15af-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b15af-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="b15af-109">參數</span><span class="sxs-lookup"><span data-stu-id="b15af-109">PARAMETERS</span></span>

### <span data-ttu-id="b15af-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15af-110">-DefaultProfile</span></span>
<span data-ttu-id="b15af-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b15af-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15af-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="b15af-112">-Name</span></span>
<span data-ttu-id="b15af-113">Cassandra 群集金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="b15af-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="b15af-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b15af-114">-OrderBy</span></span>
<span data-ttu-id="b15af-115">Cassandra 群集金鑰的順序。</span><span class="sxs-lookup"><span data-stu-id="b15af-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="b15af-116">可能的值包括： "Asc"，"Desc"</span><span class="sxs-lookup"><span data-stu-id="b15af-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="b15af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15af-117">CommonParameters</span></span>
<span data-ttu-id="b15af-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b15af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15af-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b15af-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15af-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b15af-120">INPUTS</span></span>

### <span data-ttu-id="b15af-121">所有</span><span class="sxs-lookup"><span data-stu-id="b15af-121">None</span></span>

## <span data-ttu-id="b15af-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b15af-122">OUTPUTS</span></span>

### <span data-ttu-id="b15af-123">PSClusterKey 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b15af-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="b15af-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b15af-124">NOTES</span></span>

## <span data-ttu-id="b15af-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b15af-125">RELATED LINKS</span></span>
