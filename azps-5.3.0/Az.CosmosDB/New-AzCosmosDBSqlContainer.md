---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446052"
---
# <span data-ttu-id="55f0a-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="55f0a-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="55f0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="55f0a-103">建立新的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="55f0a-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="55f0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="55f0a-104">SYNTAX</span></span>

### <span data-ttu-id="55f0a-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="55f0a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f0a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f0a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55f0a-107">說明</span><span class="sxs-lookup"><span data-stu-id="55f0a-107">DESCRIPTION</span></span>
<span data-ttu-id="55f0a-108">建立新的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="55f0a-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="55f0a-109">示例</span><span class="sxs-lookup"><span data-stu-id="55f0a-109">EXAMPLES</span></span>

### <span data-ttu-id="55f0a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="55f0a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="55f0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="55f0a-111">PARAMETERS</span></span>

### <span data-ttu-id="55f0a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55f0a-112">-AccountName</span></span>
<span data-ttu-id="55f0a-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="55f0a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55f0a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="55f0a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="55f0a-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="55f0a-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="55f0a-116">-確認</span><span class="sxs-lookup"><span data-stu-id="55f0a-116">-Confirm</span></span>
<span data-ttu-id="55f0a-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55f0a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f0a-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="55f0a-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="55f0a-119">PSSqlConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="55f0a-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="55f0a-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="55f0a-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="55f0a-121">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="55f0a-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="55f0a-122">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="55f0a-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="55f0a-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="55f0a-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="55f0a-124">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="55f0a-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="55f0a-125">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="55f0a-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="55f0a-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="55f0a-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="55f0a-127">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="55f0a-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="55f0a-128">如果隨同 ConflictResolutionPolicy 參數一起提供，則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="55f0a-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="55f0a-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55f0a-129">-DatabaseName</span></span>
<span data-ttu-id="55f0a-130">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="55f0a-130">Database name.</span></span>

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

### <span data-ttu-id="55f0a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f0a-131">-DefaultProfile</span></span>
<span data-ttu-id="55f0a-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55f0a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f0a-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="55f0a-133">-IndexingPolicy</span></span>
<span data-ttu-id="55f0a-134">PSSqlIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="55f0a-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="55f0a-135">-Name</span></span>
<span data-ttu-id="55f0a-136">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="55f0a-136">Container name.</span></span>

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

### <span data-ttu-id="55f0a-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55f0a-137">-ParentObject</span></span>
<span data-ttu-id="55f0a-138">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="55f0a-138">Sql Database object.</span></span>

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

### <span data-ttu-id="55f0a-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="55f0a-139">-PartitionKeyKind</span></span>
<span data-ttu-id="55f0a-140">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="55f0a-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="55f0a-141">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="55f0a-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="55f0a-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="55f0a-142">-PartitionKeyPath</span></span>
<span data-ttu-id="55f0a-143">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="55f0a-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="55f0a-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="55f0a-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="55f0a-145">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="55f0a-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="55f0a-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f0a-146">-ResourceGroupName</span></span>
<span data-ttu-id="55f0a-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55f0a-147">Name of resource group.</span></span>

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

### <span data-ttu-id="55f0a-148">-輸送量</span><span class="sxs-lookup"><span data-stu-id="55f0a-148">-Throughput</span></span>
<span data-ttu-id="55f0a-149">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="55f0a-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="55f0a-150">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="55f0a-150">Default value is 400.</span></span>

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

### <span data-ttu-id="55f0a-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="55f0a-151">-TtlInSeconds</span></span>
<span data-ttu-id="55f0a-152">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="55f0a-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="55f0a-153">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="55f0a-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="55f0a-154">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="55f0a-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="55f0a-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="55f0a-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="55f0a-156">CosmosDB PSSqlUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="55f0a-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="55f0a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f0a-157">-WhatIf</span></span>
<span data-ttu-id="55f0a-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55f0a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f0a-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55f0a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f0a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f0a-160">CommonParameters</span></span>
<span data-ttu-id="55f0a-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55f0a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f0a-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55f0a-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f0a-163">輸入</span><span class="sxs-lookup"><span data-stu-id="55f0a-163">INPUTS</span></span>

### <span data-ttu-id="55f0a-164">PSSqlIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="55f0a-165">PSSqlUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="55f0a-166">PSSqlConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="55f0a-167">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="55f0a-168">輸出</span><span class="sxs-lookup"><span data-stu-id="55f0a-168">OUTPUTS</span></span>

### <span data-ttu-id="55f0a-169">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="55f0a-170">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="55f0a-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="55f0a-171">筆記</span><span class="sxs-lookup"><span data-stu-id="55f0a-171">NOTES</span></span>

## <span data-ttu-id="55f0a-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="55f0a-172">RELATED LINKS</span></span>
