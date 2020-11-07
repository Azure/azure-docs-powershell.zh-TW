---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797293"
---
# <span data-ttu-id="19b81-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="19b81-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="19b81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19b81-102">SYNOPSIS</span></span>
<span data-ttu-id="19b81-103">取得 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="19b81-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="19b81-104">句法</span><span class="sxs-lookup"><span data-stu-id="19b81-104">SYNTAX</span></span>

### <span data-ttu-id="19b81-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="19b81-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b81-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b81-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19b81-107">說明</span><span class="sxs-lookup"><span data-stu-id="19b81-107">DESCRIPTION</span></span>
<span data-ttu-id="19b81-108">**AzCosmosDBCassandraKeyspace** Cmdlet 會建立新的或更新現有的 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="19b81-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="19b81-109">示例</span><span class="sxs-lookup"><span data-stu-id="19b81-109">EXAMPLES</span></span>

### <span data-ttu-id="19b81-110">範例1</span><span class="sxs-lookup"><span data-stu-id="19b81-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="19b81-111">Get-AzCosmosDBCassandraKeyspace 取得現有 CassandraKeyspace 的屬性。</span><span class="sxs-lookup"><span data-stu-id="19b81-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="19b81-112">您可以展開資源以取得 _etag、_ts _rid 屬性。</span><span class="sxs-lookup"><span data-stu-id="19b81-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="19b81-113">參數</span><span class="sxs-lookup"><span data-stu-id="19b81-113">PARAMETERS</span></span>

### <span data-ttu-id="19b81-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="19b81-114">-AccountName</span></span>
<span data-ttu-id="19b81-115">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="19b81-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="19b81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b81-116">-DefaultProfile</span></span>
<span data-ttu-id="19b81-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19b81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b81-118">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="19b81-118">-Detailed</span></span>
<span data-ttu-id="19b81-119">如果提供此選項，則 Cmdlet 會以對應的輸送量值傳回 Keyspace。</span><span class="sxs-lookup"><span data-stu-id="19b81-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="19b81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19b81-120">-InputObject</span></span>
<span data-ttu-id="19b81-121">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="19b81-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19b81-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="19b81-122">-Name</span></span>
<span data-ttu-id="19b81-123">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="19b81-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="19b81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b81-124">-ResourceGroupName</span></span>
<span data-ttu-id="19b81-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="19b81-125">Name of resource group.</span></span>

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

### <span data-ttu-id="19b81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b81-126">CommonParameters</span></span>
<span data-ttu-id="19b81-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19b81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b81-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="19b81-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b81-129">輸入</span><span class="sxs-lookup"><span data-stu-id="19b81-129">INPUTS</span></span>

### <span data-ttu-id="19b81-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="19b81-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="19b81-131">輸出</span><span class="sxs-lookup"><span data-stu-id="19b81-131">OUTPUTS</span></span>

### <span data-ttu-id="19b81-132">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="19b81-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="19b81-133">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="19b81-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="19b81-134">筆記</span><span class="sxs-lookup"><span data-stu-id="19b81-134">NOTES</span></span>

## <span data-ttu-id="19b81-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="19b81-135">RELATED LINKS</span></span>
