---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 4fc4bd816511132d5a4fd5d317069e3baf9d9225
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905594"
---
# <span data-ttu-id="bd737-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="bd737-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="bd737-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd737-102">SYNOPSIS</span></span>
<span data-ttu-id="bd737-103">建立一個新的集區DB Sql Container。</span><span class="sxs-lookup"><span data-stu-id="bd737-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="bd737-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd737-104">SYNTAX</span></span>

### <span data-ttu-id="bd737-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd737-105">ByNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="bd737-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd737-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd737-107">描述</span><span class="sxs-lookup"><span data-stu-id="bd737-107">DESCRIPTION</span></span>
<span data-ttu-id="bd737-108">建立一個新的集區DB Sql Container。</span><span class="sxs-lookup"><span data-stu-id="bd737-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="bd737-109">例子</span><span class="sxs-lookup"><span data-stu-id="bd737-109">EXAMPLES</span></span>

### <span data-ttu-id="bd737-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="bd737-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="bd737-111">參數</span><span class="sxs-lookup"><span data-stu-id="bd737-111">PARAMETERS</span></span>

### <span data-ttu-id="bd737-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd737-112">-AccountName</span></span>
<span data-ttu-id="bd737-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd737-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bd737-114">-分析StorageTtl</span><span class="sxs-lookup"><span data-stu-id="bd737-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="bd737-115">用於分析儲存空間的 TTL (秒) 。</span><span class="sxs-lookup"><span data-stu-id="bd737-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="bd737-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bd737-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bd737-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="bd737-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bd737-118">-確認</span><span class="sxs-lookup"><span data-stu-id="bd737-118">-Confirm</span></span>
<span data-ttu-id="bd737-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bd737-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd737-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd737-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="bd737-121">類型 PSSqlConflictResolutionPolicy 的 ConflictResolutionPolicy 物件，如果提供此選項，則設為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="bd737-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="bd737-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="bd737-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="bd737-123">可以有值：LastWriterWins，自訂，手動。</span><span class="sxs-lookup"><span data-stu-id="bd737-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="bd737-124">如果與 ConflictResolutionPolicy 參數一起提供，則忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="bd737-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="bd737-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="bd737-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="bd737-126">當類型為 LastWriterWins 時提供。</span><span class="sxs-lookup"><span data-stu-id="bd737-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="bd737-127">如果與 ConflictResolutionPolicy 參數一起提供，則忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="bd737-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="bd737-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="bd737-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="bd737-129">在自訂類型時提供。</span><span class="sxs-lookup"><span data-stu-id="bd737-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="bd737-130">如果與 ConflictResolutionPolicy 參數一起提供，則忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="bd737-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="bd737-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd737-131">-DatabaseName</span></span>
<span data-ttu-id="bd737-132">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="bd737-132">Database name.</span></span>

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

### <span data-ttu-id="bd737-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd737-133">-DefaultProfile</span></span>
<span data-ttu-id="bd737-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd737-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd737-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="bd737-135">-IndexingPolicy</span></span>
<span data-ttu-id="bd737-136">類型為 Microsoft.Azure.Commands.AzsDB.PSSqlIndexingPolicy 的索引策略物件。</span><span class="sxs-lookup"><span data-stu-id="bd737-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="bd737-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd737-137">-Name</span></span>
<span data-ttu-id="bd737-138">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="bd737-138">Container name.</span></span>

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

### <span data-ttu-id="bd737-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd737-139">-ParentObject</span></span>
<span data-ttu-id="bd737-140">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="bd737-140">Sql Database object.</span></span>

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

### <span data-ttu-id="bd737-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="bd737-141">-PartitionKeyKind</span></span>
<span data-ttu-id="bd737-142">用於分割的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="bd737-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="bd737-143">可能的值包括：'雜湊'、'範圍'</span><span class="sxs-lookup"><span data-stu-id="bd737-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="bd737-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="bd737-144">-PartitionKeyPath</span></span>
<span data-ttu-id="bd737-145">分割鍵路徑，例如'/address/zipcode'。</span><span class="sxs-lookup"><span data-stu-id="bd737-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="bd737-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="bd737-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="bd737-147">分割鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="bd737-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="bd737-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd737-148">-ResourceGroupName</span></span>
<span data-ttu-id="bd737-149">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd737-149">Name of resource group.</span></span>

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

### <span data-ttu-id="bd737-150">-輸送量</span><span class="sxs-lookup"><span data-stu-id="bd737-150">-Throughput</span></span>
<span data-ttu-id="bd737-151">SQL 容器的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="bd737-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="bd737-152">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="bd737-152">Default value is 400.</span></span>

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

### <span data-ttu-id="bd737-153">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="bd737-153">-TtlInSeconds</span></span>
<span data-ttu-id="bd737-154">預設 Ttl ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="bd737-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="bd737-155">如果值遺失或設為 - 1，專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="bd737-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="bd737-156">如果值設為 n，則專案會在上次修改時間之後的第 n 秒過期。</span><span class="sxs-lookup"><span data-stu-id="bd737-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="bd737-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="bd737-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="bd737-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.代斯DB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="bd737-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="bd737-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd737-159">-WhatIf</span></span>
<span data-ttu-id="bd737-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd737-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd737-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd737-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd737-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd737-162">CommonParameters</span></span>
<span data-ttu-id="bd737-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd737-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd737-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd737-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd737-165">輸入</span><span class="sxs-lookup"><span data-stu-id="bd737-165">INPUTS</span></span>

### <span data-ttu-id="bd737-166">Microsoft.Azure.Commands.AzsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="bd737-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="bd737-167">Microsoft.Azure.Commands.AzsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="bd737-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="bd737-168">Microsoft.Azure.Commands.AzsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd737-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="bd737-169">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bd737-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="bd737-170">輸出</span><span class="sxs-lookup"><span data-stu-id="bd737-170">OUTPUTS</span></span>

### <span data-ttu-id="bd737-171">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bd737-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="bd737-172">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bd737-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bd737-173">筆記</span><span class="sxs-lookup"><span data-stu-id="bd737-173">NOTES</span></span>

## <span data-ttu-id="bd737-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd737-174">RELATED LINKS</span></span>
