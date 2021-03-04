---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7251b4b928bb0adc94bc42da9d5bcef063c86259
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916426"
---
# <span data-ttu-id="54c68-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="54c68-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="54c68-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54c68-102">SYNOPSIS</span></span>
<span data-ttu-id="54c68-103">建立新一個一次的科西斯DB 卡薩德拉表格。</span><span class="sxs-lookup"><span data-stu-id="54c68-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="54c68-104">語法</span><span class="sxs-lookup"><span data-stu-id="54c68-104">SYNTAX</span></span>

### <span data-ttu-id="54c68-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="54c68-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c68-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54c68-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54c68-107">描述</span><span class="sxs-lookup"><span data-stu-id="54c68-107">DESCRIPTION</span></span>
<span data-ttu-id="54c68-108">建立新一個一次的科西斯DB 卡薩德拉表格。</span><span class="sxs-lookup"><span data-stu-id="54c68-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="54c68-109">例子</span><span class="sxs-lookup"><span data-stu-id="54c68-109">EXAMPLES</span></span>

### <span data-ttu-id="54c68-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="54c68-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="54c68-111">參數</span><span class="sxs-lookup"><span data-stu-id="54c68-111">PARAMETERS</span></span>

### <span data-ttu-id="54c68-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54c68-112">-AccountName</span></span>
<span data-ttu-id="54c68-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c68-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="54c68-114">-分析StorageTtl</span><span class="sxs-lookup"><span data-stu-id="54c68-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="54c68-115">分析儲存空間 TTL。</span><span class="sxs-lookup"><span data-stu-id="54c68-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="54c68-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="54c68-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="54c68-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="54c68-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="54c68-118">-確認</span><span class="sxs-lookup"><span data-stu-id="54c68-118">-Confirm</span></span>
<span data-ttu-id="54c68-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54c68-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c68-120">-DefaultProfile</span></span>
<span data-ttu-id="54c68-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54c68-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c68-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="54c68-122">-KeyspaceName</span></span>
<span data-ttu-id="54c68-123">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="54c68-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="54c68-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="54c68-124">-Name</span></span>
<span data-ttu-id="54c68-125">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="54c68-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="54c68-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="54c68-126">-ParentObject</span></span>
<span data-ttu-id="54c68-127">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="54c68-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="54c68-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c68-128">-ResourceGroupName</span></span>
<span data-ttu-id="54c68-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c68-129">Name of resource group.</span></span>

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

### <span data-ttu-id="54c68-130">-架構</span><span class="sxs-lookup"><span data-stu-id="54c68-130">-Schema</span></span>
<span data-ttu-id="54c68-131">PSCassandraSchema 物件。</span><span class="sxs-lookup"><span data-stu-id="54c68-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="54c68-132">使用New-AzCosmosDBCassandraSchema建立此物件。</span><span class="sxs-lookup"><span data-stu-id="54c68-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-133">-輸送量</span><span class="sxs-lookup"><span data-stu-id="54c68-133">-Throughput</span></span>
<span data-ttu-id="54c68-134">Cassandra Keyspace (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="54c68-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="54c68-135">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="54c68-135">Default value is 400.</span></span>

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

### <span data-ttu-id="54c68-136">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="54c68-136">-TtlInSeconds</span></span>
<span data-ttu-id="54c68-137">預設 Ttl ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="54c68-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="54c68-138">如果值遺失或設為 - 1，專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="54c68-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="54c68-139">如果值設為 n，則專案會在上次修改時間之後的第 n 秒過期。</span><span class="sxs-lookup"><span data-stu-id="54c68-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="54c68-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c68-140">-WhatIf</span></span>
<span data-ttu-id="54c68-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54c68-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c68-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54c68-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c68-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c68-143">CommonParameters</span></span>
<span data-ttu-id="54c68-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54c68-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c68-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54c68-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c68-146">輸入</span><span class="sxs-lookup"><span data-stu-id="54c68-146">INPUTS</span></span>

### <span data-ttu-id="54c68-147">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="54c68-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="54c68-148">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="54c68-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="54c68-149">輸出</span><span class="sxs-lookup"><span data-stu-id="54c68-149">OUTPUTS</span></span>

### <span data-ttu-id="54c68-150">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="54c68-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="54c68-151">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="54c68-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="54c68-152">筆記</span><span class="sxs-lookup"><span data-stu-id="54c68-152">NOTES</span></span>

## <span data-ttu-id="54c68-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="54c68-153">RELATED LINKS</span></span>
