---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965871"
---
# <span data-ttu-id="6c251-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="6c251-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="6c251-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c251-102">SYNOPSIS</span></span>
<span data-ttu-id="6c251-103">建立新的或更新現有的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="6c251-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="6c251-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c251-104">SYNTAX</span></span>

### <span data-ttu-id="6c251-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c251-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c251-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c251-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c251-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c251-107">DESCRIPTION</span></span>
<span data-ttu-id="6c251-108">**AzCosmosDBSqlContainer** Cmdlet 會建立新的或更新現有的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="6c251-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="6c251-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c251-109">EXAMPLES</span></span>

### <span data-ttu-id="6c251-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6c251-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="6c251-111">參數</span><span class="sxs-lookup"><span data-stu-id="6c251-111">PARAMETERS</span></span>

### <span data-ttu-id="6c251-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c251-112">-AccountName</span></span>
<span data-ttu-id="6c251-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c251-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6c251-114">-確認</span><span class="sxs-lookup"><span data-stu-id="6c251-114">-Confirm</span></span>
<span data-ttu-id="6c251-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c251-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c251-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c251-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="6c251-117">PSSqlConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="6c251-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="6c251-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="6c251-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="6c251-119">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="6c251-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="6c251-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="6c251-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="6c251-121">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="6c251-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="6c251-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="6c251-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="6c251-123">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="6c251-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="6c251-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c251-124">-DatabaseName</span></span>
<span data-ttu-id="6c251-125">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6c251-125">Database name.</span></span>

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

### <span data-ttu-id="6c251-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c251-126">-DefaultProfile</span></span>
<span data-ttu-id="6c251-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c251-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c251-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6c251-128">-IndexingPolicy</span></span>
<span data-ttu-id="6c251-129">PSSqlIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6c251-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="6c251-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c251-130">-InputObject</span></span>
<span data-ttu-id="6c251-131">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="6c251-131">Sql Database object.</span></span>

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

### <span data-ttu-id="6c251-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c251-132">-Name</span></span>
<span data-ttu-id="6c251-133">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6c251-133">Container name.</span></span>

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

### <span data-ttu-id="6c251-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="6c251-134">-PartitionKeyKind</span></span>
<span data-ttu-id="6c251-135">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="6c251-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="6c251-136">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="6c251-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="6c251-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="6c251-137">-PartitionKeyPath</span></span>
<span data-ttu-id="6c251-138">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="6c251-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="6c251-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="6c251-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="6c251-140">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="6c251-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="6c251-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c251-141">-ResourceGroupName</span></span>
<span data-ttu-id="6c251-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c251-142">Name of resource group.</span></span>

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

### <span data-ttu-id="6c251-143">-輸送量</span><span class="sxs-lookup"><span data-stu-id="6c251-143">-Throughput</span></span>
<span data-ttu-id="6c251-144">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="6c251-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="6c251-145">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="6c251-145">Default value is 400.</span></span>

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

### <span data-ttu-id="6c251-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="6c251-146">-TtlInSeconds</span></span>
<span data-ttu-id="6c251-147">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c251-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="6c251-148">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="6c251-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="6c251-149">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="6c251-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="6c251-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6c251-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="6c251-151">CosmosDB PSSqlUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="6c251-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="6c251-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c251-152">-WhatIf</span></span>
<span data-ttu-id="6c251-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c251-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c251-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c251-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c251-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c251-155">CommonParameters</span></span>
<span data-ttu-id="6c251-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c251-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c251-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c251-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c251-158">輸入</span><span class="sxs-lookup"><span data-stu-id="6c251-158">INPUTS</span></span>

### <span data-ttu-id="6c251-159">所有</span><span class="sxs-lookup"><span data-stu-id="6c251-159">None</span></span>

## <span data-ttu-id="6c251-160">輸出</span><span class="sxs-lookup"><span data-stu-id="6c251-160">OUTPUTS</span></span>

### <span data-ttu-id="6c251-161">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6c251-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="6c251-162">筆記</span><span class="sxs-lookup"><span data-stu-id="6c251-162">NOTES</span></span>

## <span data-ttu-id="6c251-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c251-163">RELATED LINKS</span></span>
