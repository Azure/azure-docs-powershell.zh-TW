---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138539"
---
# <span data-ttu-id="e2440-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="e2440-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="e2440-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2440-102">SYNOPSIS</span></span>
<span data-ttu-id="e2440-103">取得 CosmosDB Cassandra 資料表。</span><span class="sxs-lookup"><span data-stu-id="e2440-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="e2440-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2440-104">SYNTAX</span></span>

### <span data-ttu-id="e2440-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e2440-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2440-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2440-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2440-107">說明</span><span class="sxs-lookup"><span data-stu-id="e2440-107">DESCRIPTION</span></span>
<span data-ttu-id="e2440-108">**AzCosmosDBCassandraTable** Cmdlet 會建立新的或更新現有的 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="e2440-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="e2440-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2440-109">EXAMPLES</span></span>

### <span data-ttu-id="e2440-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e2440-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="e2440-111">{{Get-AzCosmosDBCassandraTable 取得現有 CassandraKeyspace 的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2440-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="e2440-112">您可以展開資源以取得 DefaultTtl、Schema、_etag、_ts、_rid 屬性。}}</span><span class="sxs-lookup"><span data-stu-id="e2440-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="e2440-113">參數</span><span class="sxs-lookup"><span data-stu-id="e2440-113">PARAMETERS</span></span>

### <span data-ttu-id="e2440-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2440-114">-AccountName</span></span>
<span data-ttu-id="e2440-115">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2440-115">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2440-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2440-116">-DefaultProfile</span></span>
<span data-ttu-id="e2440-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2440-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2440-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="e2440-118">-KeyspaceName</span></span>
<span data-ttu-id="e2440-119">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="e2440-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2440-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2440-120">-Name</span></span>
<span data-ttu-id="e2440-121">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="e2440-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="e2440-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e2440-122">-ParentObject</span></span>
<span data-ttu-id="e2440-123">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="e2440-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2440-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2440-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2440-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2440-125">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2440-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2440-126">CommonParameters</span></span>
<span data-ttu-id="e2440-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2440-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2440-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2440-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2440-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e2440-129">INPUTS</span></span>

### <span data-ttu-id="e2440-130">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e2440-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e2440-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e2440-131">OUTPUTS</span></span>

### <span data-ttu-id="e2440-132">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e2440-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="e2440-133">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e2440-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e2440-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e2440-134">NOTES</span></span>

## <span data-ttu-id="e2440-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2440-135">RELATED LINKS</span></span>
