---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284788"
---
# <span data-ttu-id="da058-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="da058-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="da058-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da058-102">SYNOPSIS</span></span>
<span data-ttu-id="da058-103">更新 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="da058-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="da058-104">讀取現有的容器，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="da058-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="da058-105">句法</span><span class="sxs-lookup"><span data-stu-id="da058-105">SYNTAX</span></span>

### <span data-ttu-id="da058-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="da058-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da058-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da058-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da058-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da058-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da058-109">說明</span><span class="sxs-lookup"><span data-stu-id="da058-109">DESCRIPTION</span></span>
<span data-ttu-id="da058-110">更新 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="da058-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="da058-111">讀取現有的容器，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="da058-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="da058-112">示例</span><span class="sxs-lookup"><span data-stu-id="da058-112">EXAMPLES</span></span>

### <span data-ttu-id="da058-113">範例1</span><span class="sxs-lookup"><span data-stu-id="da058-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="da058-114">參數</span><span class="sxs-lookup"><span data-stu-id="da058-114">PARAMETERS</span></span>

### <span data-ttu-id="da058-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da058-115">-AccountName</span></span>
<span data-ttu-id="da058-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="da058-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="da058-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="da058-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="da058-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="da058-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="da058-119">-確認</span><span class="sxs-lookup"><span data-stu-id="da058-119">-Confirm</span></span>
<span data-ttu-id="da058-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da058-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da058-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="da058-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="da058-122">PSSqlConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="da058-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="da058-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="da058-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="da058-124">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="da058-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="da058-125">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="da058-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="da058-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="da058-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="da058-127">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="da058-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="da058-128">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="da058-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="da058-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="da058-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="da058-130">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="da058-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="da058-131">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="da058-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="da058-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da058-132">-DatabaseName</span></span>
<span data-ttu-id="da058-133">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="da058-133">Database name.</span></span>

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

### <span data-ttu-id="da058-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da058-134">-DefaultProfile</span></span>
<span data-ttu-id="da058-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da058-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da058-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="da058-136">-IndexingPolicy</span></span>
<span data-ttu-id="da058-137">PSSqlIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="da058-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da058-138">-InputObject</span></span>
<span data-ttu-id="da058-139">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="da058-139">Sql Container object.</span></span>

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

### <span data-ttu-id="da058-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="da058-140">-Name</span></span>
<span data-ttu-id="da058-141">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="da058-141">Container name.</span></span>

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

### <span data-ttu-id="da058-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="da058-142">-ParentObject</span></span>
<span data-ttu-id="da058-143">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="da058-143">Sql Database object.</span></span>

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

### <span data-ttu-id="da058-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="da058-144">-PartitionKeyKind</span></span>
<span data-ttu-id="da058-145">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="da058-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="da058-146">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="da058-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="da058-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="da058-147">-PartitionKeyPath</span></span>
<span data-ttu-id="da058-148">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="da058-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="da058-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="da058-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="da058-150">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="da058-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="da058-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da058-151">-ResourceGroupName</span></span>
<span data-ttu-id="da058-152">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="da058-152">Name of resource group.</span></span>

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

### <span data-ttu-id="da058-153">-輸送量</span><span class="sxs-lookup"><span data-stu-id="da058-153">-Throughput</span></span>
<span data-ttu-id="da058-154">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="da058-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="da058-155">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="da058-155">Default value is 400.</span></span>

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

### <span data-ttu-id="da058-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="da058-156">-TtlInSeconds</span></span>
<span data-ttu-id="da058-157">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="da058-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="da058-158">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="da058-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="da058-159">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="da058-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="da058-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="da058-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="da058-161">CosmosDB PSSqlUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="da058-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="da058-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da058-162">-WhatIf</span></span>
<span data-ttu-id="da058-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da058-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da058-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da058-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da058-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da058-165">CommonParameters</span></span>
<span data-ttu-id="da058-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da058-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da058-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da058-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da058-168">輸入</span><span class="sxs-lookup"><span data-stu-id="da058-168">INPUTS</span></span>

### <span data-ttu-id="da058-169">PSSqlIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="da058-170">PSSqlUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="da058-171">PSSqlConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="da058-172">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="da058-173">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="da058-174">輸出</span><span class="sxs-lookup"><span data-stu-id="da058-174">OUTPUTS</span></span>

### <span data-ttu-id="da058-175">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="da058-176">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="da058-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="da058-177">筆記</span><span class="sxs-lookup"><span data-stu-id="da058-177">NOTES</span></span>

## <span data-ttu-id="da058-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="da058-178">RELATED LINKS</span></span>
