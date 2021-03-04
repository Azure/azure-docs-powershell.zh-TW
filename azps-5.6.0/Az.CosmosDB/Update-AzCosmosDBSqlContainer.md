---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: a36222b3a6cacf567fd0b5e7541c2dc53a44fa22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908238"
---
# <span data-ttu-id="48264-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="48264-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="48264-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48264-102">SYNOPSIS</span></span>
<span data-ttu-id="48264-103">更新一些更新的一些 Sql Container。</span><span class="sxs-lookup"><span data-stu-id="48264-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="48264-104">讀取現有的容器以執行用戶端修補作業。</span><span class="sxs-lookup"><span data-stu-id="48264-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="48264-105">語法</span><span class="sxs-lookup"><span data-stu-id="48264-105">SYNTAX</span></span>

### <span data-ttu-id="48264-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="48264-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48264-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48264-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48264-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48264-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48264-109">描述</span><span class="sxs-lookup"><span data-stu-id="48264-109">DESCRIPTION</span></span>
<span data-ttu-id="48264-110">更新一些更新的一些 Sql Container。</span><span class="sxs-lookup"><span data-stu-id="48264-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="48264-111">讀取現有的容器以執行用戶端修補作業。</span><span class="sxs-lookup"><span data-stu-id="48264-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="48264-112">例子</span><span class="sxs-lookup"><span data-stu-id="48264-112">EXAMPLES</span></span>

### <span data-ttu-id="48264-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="48264-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="48264-114">參數</span><span class="sxs-lookup"><span data-stu-id="48264-114">PARAMETERS</span></span>

### <span data-ttu-id="48264-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48264-115">-AccountName</span></span>
<span data-ttu-id="48264-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="48264-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="48264-117">-分析StorageTtl</span><span class="sxs-lookup"><span data-stu-id="48264-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="48264-118">用於分析儲存空間的 TTL (秒) 。</span><span class="sxs-lookup"><span data-stu-id="48264-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="48264-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="48264-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="48264-120">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="48264-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="48264-121">-確認</span><span class="sxs-lookup"><span data-stu-id="48264-121">-Confirm</span></span>
<span data-ttu-id="48264-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="48264-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48264-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="48264-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="48264-124">類型 PSSqlConflictResolutionPolicy 的 ConflictResolutionPolicy 物件，如果提供此選項，則設為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="48264-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="48264-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="48264-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="48264-126">可以有值：LastWriterWins，自訂，手動。</span><span class="sxs-lookup"><span data-stu-id="48264-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="48264-127">如果與 ConflictResolutionPolicy 參數一起提供，則忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="48264-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="48264-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="48264-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="48264-129">當類型為 LastWriterWins 時提供。</span><span class="sxs-lookup"><span data-stu-id="48264-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="48264-130">如果與 ConflictResolutionPolicy 參數一起提供，則忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="48264-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="48264-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="48264-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="48264-132">在自訂類型時提供。</span><span class="sxs-lookup"><span data-stu-id="48264-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="48264-133">如果與 ConflictResolutionPolicy 參數一起提供，則忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="48264-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="48264-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48264-134">-DatabaseName</span></span>
<span data-ttu-id="48264-135">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="48264-135">Database name.</span></span>

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

### <span data-ttu-id="48264-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48264-136">-DefaultProfile</span></span>
<span data-ttu-id="48264-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="48264-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48264-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="48264-138">-IndexingPolicy</span></span>
<span data-ttu-id="48264-139">類型為 Microsoft.Azure.Commands.AzsDB.PSSqlIndexingPolicy 的索引策略物件。</span><span class="sxs-lookup"><span data-stu-id="48264-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="48264-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48264-140">-InputObject</span></span>
<span data-ttu-id="48264-141">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="48264-141">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48264-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="48264-142">-Name</span></span>
<span data-ttu-id="48264-143">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="48264-143">Container name.</span></span>

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

### <span data-ttu-id="48264-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="48264-144">-ParentObject</span></span>
<span data-ttu-id="48264-145">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="48264-145">Sql Database object.</span></span>

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

### <span data-ttu-id="48264-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="48264-146">-PartitionKeyKind</span></span>
<span data-ttu-id="48264-147">用於分割的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="48264-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="48264-148">可能的值包括：'雜湊'、'範圍'</span><span class="sxs-lookup"><span data-stu-id="48264-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="48264-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="48264-149">-PartitionKeyPath</span></span>
<span data-ttu-id="48264-150">分割鍵路徑，例如'/address/zipcode'。</span><span class="sxs-lookup"><span data-stu-id="48264-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48264-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="48264-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="48264-152">分割鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="48264-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="48264-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48264-153">-ResourceGroupName</span></span>
<span data-ttu-id="48264-154">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48264-154">Name of resource group.</span></span>

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

### <span data-ttu-id="48264-155">-輸送量</span><span class="sxs-lookup"><span data-stu-id="48264-155">-Throughput</span></span>
<span data-ttu-id="48264-156">SQL 容器的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="48264-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="48264-157">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="48264-157">Default value is 400.</span></span>

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

### <span data-ttu-id="48264-158">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="48264-158">-TtlInSeconds</span></span>
<span data-ttu-id="48264-159">預設 Ttl ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="48264-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="48264-160">如果值遺失或設為 - 1，專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="48264-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="48264-161">如果值設為 n，則專案會在上次修改時間之後的第 n 秒過期。</span><span class="sxs-lookup"><span data-stu-id="48264-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="48264-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="48264-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="48264-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.代斯DB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="48264-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="48264-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48264-164">-WhatIf</span></span>
<span data-ttu-id="48264-165">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48264-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48264-166">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48264-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48264-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48264-167">CommonParameters</span></span>
<span data-ttu-id="48264-168">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48264-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48264-169">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48264-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48264-170">輸入</span><span class="sxs-lookup"><span data-stu-id="48264-170">INPUTS</span></span>

### <span data-ttu-id="48264-171">Microsoft.Azure.Commands.AzsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="48264-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="48264-172">Microsoft.Azure.Commands.AzsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="48264-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="48264-173">Microsoft.Azure.Commands.AzsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="48264-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="48264-174">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="48264-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="48264-175">Microsoft.Azure.Commands.AzsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="48264-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="48264-176">輸出</span><span class="sxs-lookup"><span data-stu-id="48264-176">OUTPUTS</span></span>

### <span data-ttu-id="48264-177">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="48264-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="48264-178">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="48264-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="48264-179">筆記</span><span class="sxs-lookup"><span data-stu-id="48264-179">NOTES</span></span>

## <span data-ttu-id="48264-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="48264-180">RELATED LINKS</span></span>
