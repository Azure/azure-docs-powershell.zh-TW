---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965869"
---
# <span data-ttu-id="fc7ea-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="fc7ea-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="fc7ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7ea-103">更新 CosmosDB Cassandra 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="fc7ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc7ea-104">SYNTAX</span></span>

### <span data-ttu-id="fc7ea-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc7ea-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc7ea-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc7ea-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc7ea-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc7ea-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7ea-108">示例</span><span class="sxs-lookup"><span data-stu-id="fc7ea-108">EXAMPLES</span></span>

### <span data-ttu-id="fc7ea-109">範例1</span><span class="sxs-lookup"><span data-stu-id="fc7ea-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="fc7ea-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc7ea-110">PARAMETERS</span></span>

### <span data-ttu-id="fc7ea-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc7ea-111">-AccountName</span></span>
<span data-ttu-id="fc7ea-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fc7ea-113">-確認</span><span class="sxs-lookup"><span data-stu-id="fc7ea-113">-Confirm</span></span>
<span data-ttu-id="fc7ea-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7ea-115">-DefaultProfile</span></span>
<span data-ttu-id="fc7ea-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc7ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc7ea-117">-InputObject</span></span>
<span data-ttu-id="fc7ea-118">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-118">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ea-119">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="fc7ea-119">-KeyspaceName</span></span>
<span data-ttu-id="fc7ea-120">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="fc7ea-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc7ea-121">-Name</span></span>
<span data-ttu-id="fc7ea-122">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="fc7ea-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fc7ea-123">-ParentObject</span></span>
<span data-ttu-id="fc7ea-124">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="fc7ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc7ea-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-126">Name of resource group.</span></span>

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

### <span data-ttu-id="fc7ea-127">-輸送量</span><span class="sxs-lookup"><span data-stu-id="fc7ea-127">-Throughput</span></span>
<span data-ttu-id="fc7ea-128">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="fc7ea-129">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7ea-130">-WhatIf</span></span>
<span data-ttu-id="fc7ea-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7ea-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7ea-133">CommonParameters</span></span>
<span data-ttu-id="fc7ea-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7ea-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7ea-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fc7ea-136">INPUTS</span></span>

### <span data-ttu-id="fc7ea-137">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="fc7ea-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fc7ea-138">OUTPUTS</span></span>

### <span data-ttu-id="fc7ea-139">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="fc7ea-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fc7ea-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fc7ea-140">NOTES</span></span>

## <span data-ttu-id="fc7ea-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc7ea-141">RELATED LINKS</span></span>
