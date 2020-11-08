---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128341"
---
# <span data-ttu-id="46006-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="46006-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="46006-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46006-102">SYNOPSIS</span></span>
<span data-ttu-id="46006-103">取得 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="46006-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="46006-104">句法</span><span class="sxs-lookup"><span data-stu-id="46006-104">SYNTAX</span></span>

### <span data-ttu-id="46006-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46006-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46006-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46006-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46006-107">說明</span><span class="sxs-lookup"><span data-stu-id="46006-107">DESCRIPTION</span></span>
<span data-ttu-id="46006-108">**AzCosmosDBCassandraKeyspace** Cmdlet 會建立新的或更新現有的 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="46006-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="46006-109">示例</span><span class="sxs-lookup"><span data-stu-id="46006-109">EXAMPLES</span></span>

### <span data-ttu-id="46006-110">範例1</span><span class="sxs-lookup"><span data-stu-id="46006-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="46006-111">Get-AzCosmosDBCassandraKeyspace 取得現有 CassandraKeyspace 的屬性。</span><span class="sxs-lookup"><span data-stu-id="46006-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="46006-112">您可以展開資源以取得 _etag、_ts _rid 屬性。</span><span class="sxs-lookup"><span data-stu-id="46006-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="46006-113">參數</span><span class="sxs-lookup"><span data-stu-id="46006-113">PARAMETERS</span></span>

### <span data-ttu-id="46006-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46006-114">-AccountName</span></span>
<span data-ttu-id="46006-115">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="46006-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46006-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46006-116">-DefaultProfile</span></span>
<span data-ttu-id="46006-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46006-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46006-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="46006-118">-Name</span></span>
<span data-ttu-id="46006-119">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="46006-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="46006-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46006-120">-ParentObject</span></span>
<span data-ttu-id="46006-121">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="46006-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="46006-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46006-122">-ResourceGroupName</span></span>
<span data-ttu-id="46006-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46006-123">Name of resource group.</span></span>

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

### <span data-ttu-id="46006-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46006-124">CommonParameters</span></span>
<span data-ttu-id="46006-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46006-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46006-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46006-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46006-127">輸入</span><span class="sxs-lookup"><span data-stu-id="46006-127">INPUTS</span></span>

### <span data-ttu-id="46006-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="46006-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="46006-129">輸出</span><span class="sxs-lookup"><span data-stu-id="46006-129">OUTPUTS</span></span>

### <span data-ttu-id="46006-130">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="46006-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="46006-131">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="46006-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="46006-132">筆記</span><span class="sxs-lookup"><span data-stu-id="46006-132">NOTES</span></span>

## <span data-ttu-id="46006-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="46006-133">RELATED LINKS</span></span>
