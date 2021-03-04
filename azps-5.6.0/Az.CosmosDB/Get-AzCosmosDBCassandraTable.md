---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 2d784a82974f47c67bae89d55042b81c9c83e273
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908606"
---
# <span data-ttu-id="1b6d5-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="1b6d5-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="1b6d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6d5-103">獲得一個花式表格。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="1b6d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b6d5-104">SYNTAX</span></span>

### <span data-ttu-id="1b6d5-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1b6d5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b6d5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b6d5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b6d5-107">描述</span><span class="sxs-lookup"><span data-stu-id="1b6d5-107">DESCRIPTION</span></span>
<span data-ttu-id="1b6d5-108">**Get-AzCosmosDBCassandraTable** Cmdlet 會建立一個新或更新現有的一個OsosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1b6d5-109">例子</span><span class="sxs-lookup"><span data-stu-id="1b6d5-109">EXAMPLES</span></span>

### <span data-ttu-id="1b6d5-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1b6d5-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="1b6d5-111">{{ Get-AzCosmosDBCassandraTable會獲得現有 CassandraKeyspace 的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="1b6d5-112">您可以展開資源以取得 DefaultTtl、架構、_etag、_ts、_rid屬性}}</span><span class="sxs-lookup"><span data-stu-id="1b6d5-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="1b6d5-113">參數</span><span class="sxs-lookup"><span data-stu-id="1b6d5-113">PARAMETERS</span></span>

### <span data-ttu-id="1b6d5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b6d5-114">-AccountName</span></span>
<span data-ttu-id="1b6d5-115">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b6d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6d5-116">-DefaultProfile</span></span>
<span data-ttu-id="1b6d5-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b6d5-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="1b6d5-118">-KeyspaceName</span></span>
<span data-ttu-id="1b6d5-119">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="1b6d5-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1b6d5-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b6d5-120">-Name</span></span>
<span data-ttu-id="1b6d5-121">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="1b6d5-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1b6d5-122">-ParentObject</span></span>
<span data-ttu-id="1b6d5-123">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="1b6d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b6d5-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1b6d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6d5-126">CommonParameters</span></span>
<span data-ttu-id="1b6d5-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b6d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6d5-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b6d5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6d5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1b6d5-129">INPUTS</span></span>

### <span data-ttu-id="1b6d5-130">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1b6d5-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1b6d5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1b6d5-131">OUTPUTS</span></span>

### <span data-ttu-id="1b6d5-132">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1b6d5-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="1b6d5-133">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1b6d5-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1b6d5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1b6d5-134">NOTES</span></span>

## <span data-ttu-id="1b6d5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b6d5-135">RELATED LINKS</span></span>
