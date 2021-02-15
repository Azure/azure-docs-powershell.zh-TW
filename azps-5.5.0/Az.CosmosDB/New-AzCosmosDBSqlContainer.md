---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 7b773bd51a928c21761900cf1f6f8c34e73c2d0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127638"
---
# <span data-ttu-id="f5ebd-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="f5ebd-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="f5ebd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ebd-103">建立新的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f5ebd-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5ebd-104">SYNTAX</span></span>

### <span data-ttu-id="f5ebd-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f5ebd-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5ebd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5ebd-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ebd-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="f5ebd-108">建立新的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f5ebd-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5ebd-109">EXAMPLES</span></span>

### <span data-ttu-id="f5ebd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f5ebd-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="f5ebd-111">參數</span><span class="sxs-lookup"><span data-stu-id="f5ebd-111">PARAMETERS</span></span>

### <span data-ttu-id="f5ebd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5ebd-112">-AccountName</span></span>
<span data-ttu-id="f5ebd-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5ebd-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f5ebd-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f5ebd-115">分析儲存空間的 TTL (以秒為單位) 。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="f5ebd-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f5ebd-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f5ebd-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f5ebd-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f5ebd-118">-Confirm</span></span>
<span data-ttu-id="f5ebd-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ebd-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5ebd-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f5ebd-121">PSSqlConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ebd-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f5ebd-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f5ebd-123">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="f5ebd-124">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f5ebd-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f5ebd-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f5ebd-126">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="f5ebd-127">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f5ebd-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f5ebd-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f5ebd-129">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="f5ebd-130">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f5ebd-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5ebd-131">-DatabaseName</span></span>
<span data-ttu-id="f5ebd-132">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-132">Database name.</span></span>

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

### <span data-ttu-id="f5ebd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ebd-133">-DefaultProfile</span></span>
<span data-ttu-id="f5ebd-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ebd-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f5ebd-135">-IndexingPolicy</span></span>
<span data-ttu-id="f5ebd-136">PSSqlIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ebd-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5ebd-137">-Name</span></span>
<span data-ttu-id="f5ebd-138">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-138">Container name.</span></span>

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

### <span data-ttu-id="f5ebd-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5ebd-139">-ParentObject</span></span>
<span data-ttu-id="f5ebd-140">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-140">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ebd-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f5ebd-141">-PartitionKeyKind</span></span>
<span data-ttu-id="f5ebd-142">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f5ebd-143">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="f5ebd-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f5ebd-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f5ebd-144">-PartitionKeyPath</span></span>
<span data-ttu-id="f5ebd-145">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ebd-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f5ebd-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="f5ebd-147">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="f5ebd-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f5ebd-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ebd-148">-ResourceGroupName</span></span>
<span data-ttu-id="f5ebd-149">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-149">Name of resource group.</span></span>

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

### <span data-ttu-id="f5ebd-150">-輸送量</span><span class="sxs-lookup"><span data-stu-id="f5ebd-150">-Throughput</span></span>
<span data-ttu-id="f5ebd-151">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f5ebd-152">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-152">Default value is 400.</span></span>

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

### <span data-ttu-id="f5ebd-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f5ebd-153">-TtlInSeconds</span></span>
<span data-ttu-id="f5ebd-154">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="f5ebd-155">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f5ebd-156">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f5ebd-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f5ebd-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f5ebd-158">CosmosDB PSSqlUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ebd-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ebd-159">-WhatIf</span></span>
<span data-ttu-id="f5ebd-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ebd-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ebd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ebd-162">CommonParameters</span></span>
<span data-ttu-id="f5ebd-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ebd-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ebd-165">輸入</span><span class="sxs-lookup"><span data-stu-id="f5ebd-165">INPUTS</span></span>

### <span data-ttu-id="f5ebd-166">PSSqlIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="f5ebd-167">PSSqlUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="f5ebd-168">PSSqlConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="f5ebd-169">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f5ebd-170">輸出</span><span class="sxs-lookup"><span data-stu-id="f5ebd-170">OUTPUTS</span></span>

### <span data-ttu-id="f5ebd-171">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f5ebd-172">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f5ebd-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f5ebd-173">筆記</span><span class="sxs-lookup"><span data-stu-id="f5ebd-173">NOTES</span></span>

## <span data-ttu-id="f5ebd-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5ebd-174">RELATED LINKS</span></span>
