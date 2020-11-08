---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971201"
---
# <span data-ttu-id="cc1b3-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="cc1b3-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="cc1b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1b3-103">建立新的 CosmosDB Cassandra 群集金鑰。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cc1b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc1b3-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc1b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1b3-106">**新的-AzCosmosDBCassandraClusterKey** 會建立新的 CosmosDB Cassandra 群集金鑰。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cc1b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc1b3-107">EXAMPLES</span></span>

### <span data-ttu-id="cc1b3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cc1b3-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="cc1b3-109">參數</span><span class="sxs-lookup"><span data-stu-id="cc1b3-109">PARAMETERS</span></span>

### <span data-ttu-id="cc1b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1b3-110">-DefaultProfile</span></span>
<span data-ttu-id="cc1b3-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc1b3-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc1b3-112">-Name</span></span>
<span data-ttu-id="cc1b3-113">Cassandra 群集金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="cc1b3-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="cc1b3-114">-OrderBy</span></span>
<span data-ttu-id="cc1b3-115">Cassandra 群集金鑰的順序。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="cc1b3-116">可能的值包括： "Asc"，"Desc"</span><span class="sxs-lookup"><span data-stu-id="cc1b3-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="cc1b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1b3-117">CommonParameters</span></span>
<span data-ttu-id="cc1b3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1b3-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1b3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="cc1b3-120">INPUTS</span></span>

### <span data-ttu-id="cc1b3-121">所有</span><span class="sxs-lookup"><span data-stu-id="cc1b3-121">None</span></span>

## <span data-ttu-id="cc1b3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="cc1b3-122">OUTPUTS</span></span>

### <span data-ttu-id="cc1b3-123">PSClusterKey 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="cc1b3-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="cc1b3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="cc1b3-124">NOTES</span></span>

## <span data-ttu-id="cc1b3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc1b3-125">RELATED LINKS</span></span>
