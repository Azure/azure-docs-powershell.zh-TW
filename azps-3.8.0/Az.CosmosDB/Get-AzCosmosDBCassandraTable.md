---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965573"
---
# <span data-ttu-id="7cb4d-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="7cb4d-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="7cb4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb4d-103">取得 CosmosDB Cassandra 資料表。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="7cb4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cb4d-104">SYNTAX</span></span>

### <span data-ttu-id="7cb4d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7cb4d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb4d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb4d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cb4d-107">說明</span><span class="sxs-lookup"><span data-stu-id="7cb4d-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb4d-108">**AzCosmosDBCassandraTable** Cmdlet 會建立新的或更新現有的 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="7cb4d-109">示例</span><span class="sxs-lookup"><span data-stu-id="7cb4d-109">EXAMPLES</span></span>

### <span data-ttu-id="7cb4d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7cb4d-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="7cb4d-111">{{Get-AzCosmosDBCassandraTable 取得現有 CassandraKeyspace 的屬性。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="7cb4d-112">您可以展開資源以取得 DefaultTtl、Schema、_etag、_ts、_rid 屬性。}}</span><span class="sxs-lookup"><span data-stu-id="7cb4d-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="7cb4d-113">參數</span><span class="sxs-lookup"><span data-stu-id="7cb4d-113">PARAMETERS</span></span>

### <span data-ttu-id="7cb4d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7cb4d-114">-AccountName</span></span>
<span data-ttu-id="7cb4d-115">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7cb4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb4d-116">-DefaultProfile</span></span>
<span data-ttu-id="7cb4d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb4d-118">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7cb4d-118">-Detailed</span></span>
<span data-ttu-id="7cb4d-119">如果提供此選項，則 Cmdlet 會以對應的輸送量值傳回 Cassandra 資料表。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb4d-120">-InputObject</span></span>
<span data-ttu-id="7cb4d-121">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-121">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="7cb4d-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="7cb4d-122">-KeyspaceName</span></span>
<span data-ttu-id="7cb4d-123">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7cb4d-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="7cb4d-124">-Name</span></span>
<span data-ttu-id="7cb4d-125">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="7cb4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7cb4d-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-127">Name of resource group.</span></span>

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

### <span data-ttu-id="7cb4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb4d-128">CommonParameters</span></span>
<span data-ttu-id="7cb4d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb4d-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb4d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7cb4d-131">INPUTS</span></span>

### <span data-ttu-id="7cb4d-132">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="7cb4d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7cb4d-133">OUTPUTS</span></span>

### <span data-ttu-id="7cb4d-134">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="7cb4d-135">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7cb4d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7cb4d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7cb4d-136">NOTES</span></span>

## <span data-ttu-id="7cb4d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cb4d-137">RELATED LINKS</span></span>