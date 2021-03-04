---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 989035c1478228eb8895a2f99779129c605b2f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908277"
---
# <span data-ttu-id="54c90-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="54c90-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="54c90-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54c90-102">SYNOPSIS</span></span>
<span data-ttu-id="54c90-103">更新一個更新了一個更新的輸送量值。。</span><span class="sxs-lookup"><span data-stu-id="54c90-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="54c90-104">語法</span><span class="sxs-lookup"><span data-stu-id="54c90-104">SYNTAX</span></span>

### <span data-ttu-id="54c90-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="54c90-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c90-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54c90-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c90-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54c90-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c90-108">描述</span><span class="sxs-lookup"><span data-stu-id="54c90-108">DESCRIPTION</span></span>
<span data-ttu-id="54c90-109">更新一個更新了一個更新的輸送量值。。</span><span class="sxs-lookup"><span data-stu-id="54c90-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="54c90-110">例子</span><span class="sxs-lookup"><span data-stu-id="54c90-110">EXAMPLES</span></span>

### <span data-ttu-id="54c90-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="54c90-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="54c90-112">參數</span><span class="sxs-lookup"><span data-stu-id="54c90-112">PARAMETERS</span></span>

### <span data-ttu-id="54c90-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54c90-113">-AccountName</span></span>
<span data-ttu-id="54c90-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c90-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="54c90-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="54c90-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="54c90-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="54c90-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="54c90-117">-確認</span><span class="sxs-lookup"><span data-stu-id="54c90-117">-Confirm</span></span>
<span data-ttu-id="54c90-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54c90-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c90-119">-DefaultProfile</span></span>
<span data-ttu-id="54c90-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54c90-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c90-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54c90-121">-InputObject</span></span>
<span data-ttu-id="54c90-122">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="54c90-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="54c90-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="54c90-123">-KeyspaceName</span></span>
<span data-ttu-id="54c90-124">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="54c90-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="54c90-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="54c90-125">-Name</span></span>
<span data-ttu-id="54c90-126">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="54c90-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="54c90-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="54c90-127">-ParentObject</span></span>
<span data-ttu-id="54c90-128">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="54c90-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="54c90-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c90-129">-ResourceGroupName</span></span>
<span data-ttu-id="54c90-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c90-130">Name of resource group.</span></span>

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

### <span data-ttu-id="54c90-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="54c90-131">-Throughput</span></span>
<span data-ttu-id="54c90-132">Cassandra Keyspace (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="54c90-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="54c90-133">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="54c90-133">Default value is 400.</span></span>

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

### <span data-ttu-id="54c90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c90-134">-WhatIf</span></span>
<span data-ttu-id="54c90-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54c90-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c90-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54c90-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c90-137">CommonParameters</span></span>
<span data-ttu-id="54c90-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54c90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c90-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54c90-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c90-140">輸入</span><span class="sxs-lookup"><span data-stu-id="54c90-140">INPUTS</span></span>

### <span data-ttu-id="54c90-141">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="54c90-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="54c90-142">輸出</span><span class="sxs-lookup"><span data-stu-id="54c90-142">OUTPUTS</span></span>

### <span data-ttu-id="54c90-143">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="54c90-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="54c90-144">筆記</span><span class="sxs-lookup"><span data-stu-id="54c90-144">NOTES</span></span>

## <span data-ttu-id="54c90-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="54c90-145">RELATED LINKS</span></span>
