---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135637"
---
# <span data-ttu-id="df94e-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="df94e-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="df94e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df94e-102">SYNOPSIS</span></span>
<span data-ttu-id="df94e-103">更新 CosmosDB Cassandra 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="df94e-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="df94e-104">句法</span><span class="sxs-lookup"><span data-stu-id="df94e-104">SYNTAX</span></span>

### <span data-ttu-id="df94e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="df94e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df94e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df94e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df94e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df94e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df94e-108">說明</span><span class="sxs-lookup"><span data-stu-id="df94e-108">DESCRIPTION</span></span>
<span data-ttu-id="df94e-109">更新 CosmosDB Cassandra 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="df94e-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="df94e-110">示例</span><span class="sxs-lookup"><span data-stu-id="df94e-110">EXAMPLES</span></span>

### <span data-ttu-id="df94e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="df94e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="df94e-112">參數</span><span class="sxs-lookup"><span data-stu-id="df94e-112">PARAMETERS</span></span>

### <span data-ttu-id="df94e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df94e-113">-AccountName</span></span>
<span data-ttu-id="df94e-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="df94e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="df94e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="df94e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="df94e-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="df94e-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df94e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="df94e-117">-Confirm</span></span>
<span data-ttu-id="df94e-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df94e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df94e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df94e-119">-DefaultProfile</span></span>
<span data-ttu-id="df94e-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df94e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df94e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df94e-121">-InputObject</span></span>
<span data-ttu-id="df94e-122">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="df94e-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="df94e-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="df94e-123">-KeyspaceName</span></span>
<span data-ttu-id="df94e-124">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="df94e-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="df94e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="df94e-125">-Name</span></span>
<span data-ttu-id="df94e-126">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="df94e-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="df94e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df94e-127">-ParentObject</span></span>
<span data-ttu-id="df94e-128">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="df94e-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="df94e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df94e-129">-ResourceGroupName</span></span>
<span data-ttu-id="df94e-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df94e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="df94e-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="df94e-131">-Throughput</span></span>
<span data-ttu-id="df94e-132">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="df94e-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="df94e-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="df94e-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df94e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df94e-134">-WhatIf</span></span>
<span data-ttu-id="df94e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df94e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df94e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df94e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df94e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df94e-137">CommonParameters</span></span>
<span data-ttu-id="df94e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df94e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df94e-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df94e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df94e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="df94e-140">INPUTS</span></span>

### <span data-ttu-id="df94e-141">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="df94e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="df94e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="df94e-142">OUTPUTS</span></span>

### <span data-ttu-id="df94e-143">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="df94e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="df94e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="df94e-144">NOTES</span></span>

## <span data-ttu-id="df94e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="df94e-145">RELATED LINKS</span></span>