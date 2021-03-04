---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: fb387adafa1a1a71d9a42b09b8c7255955eccd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908609"
---
# <span data-ttu-id="29080-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="29080-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="29080-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29080-102">SYNOPSIS</span></span>
<span data-ttu-id="29080-103">獲得一個部科西斯DB 加薩德拉鍵格。</span><span class="sxs-lookup"><span data-stu-id="29080-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="29080-104">語法</span><span class="sxs-lookup"><span data-stu-id="29080-104">SYNTAX</span></span>

### <span data-ttu-id="29080-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29080-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29080-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29080-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29080-107">描述</span><span class="sxs-lookup"><span data-stu-id="29080-107">DESCRIPTION</span></span>
<span data-ttu-id="29080-108">**Get-AzCosmosDBCassandraKeyspace** Cmdlet 會建立一個新或更新現有的一個OsosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="29080-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="29080-109">例子</span><span class="sxs-lookup"><span data-stu-id="29080-109">EXAMPLES</span></span>

### <span data-ttu-id="29080-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="29080-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="29080-111">Get-AzCosmosDBCassandraKeyspace現有 CassandraKeyspace 的屬性。</span><span class="sxs-lookup"><span data-stu-id="29080-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="29080-112">您可以展開資源以取得_etag、_ts_rid屬性。</span><span class="sxs-lookup"><span data-stu-id="29080-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="29080-113">參數</span><span class="sxs-lookup"><span data-stu-id="29080-113">PARAMETERS</span></span>

### <span data-ttu-id="29080-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="29080-114">-AccountName</span></span>
<span data-ttu-id="29080-115">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="29080-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="29080-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29080-116">-DefaultProfile</span></span>
<span data-ttu-id="29080-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="29080-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29080-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="29080-118">-Name</span></span>
<span data-ttu-id="29080-119">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="29080-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="29080-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="29080-120">-ParentObject</span></span>
<span data-ttu-id="29080-121">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="29080-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29080-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29080-122">-ResourceGroupName</span></span>
<span data-ttu-id="29080-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29080-123">Name of resource group.</span></span>

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

### <span data-ttu-id="29080-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29080-124">CommonParameters</span></span>
<span data-ttu-id="29080-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29080-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29080-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29080-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29080-127">輸入</span><span class="sxs-lookup"><span data-stu-id="29080-127">INPUTS</span></span>

### <span data-ttu-id="29080-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="29080-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="29080-129">輸出</span><span class="sxs-lookup"><span data-stu-id="29080-129">OUTPUTS</span></span>

### <span data-ttu-id="29080-130">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="29080-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="29080-131">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="29080-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="29080-132">筆記</span><span class="sxs-lookup"><span data-stu-id="29080-132">NOTES</span></span>

## <span data-ttu-id="29080-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="29080-133">RELATED LINKS</span></span>
