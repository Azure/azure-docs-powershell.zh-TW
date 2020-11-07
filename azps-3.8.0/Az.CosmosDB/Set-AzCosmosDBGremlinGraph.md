---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965884"
---
# <span data-ttu-id="8436f-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="8436f-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="8436f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8436f-102">SYNOPSIS</span></span>
<span data-ttu-id="8436f-103">設定 CosmosDB Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="8436f-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="8436f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8436f-104">SYNTAX</span></span>

### <span data-ttu-id="8436f-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8436f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8436f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8436f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8436f-107">說明</span><span class="sxs-lookup"><span data-stu-id="8436f-107">DESCRIPTION</span></span>
<span data-ttu-id="8436f-108">**AzCosmosDBGremlinGraph** Cmdlet 會設定 CosmosDB Gremlin 圖形。</span><span class="sxs-lookup"><span data-stu-id="8436f-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="8436f-109">示例</span><span class="sxs-lookup"><span data-stu-id="8436f-109">EXAMPLES</span></span>

### <span data-ttu-id="8436f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8436f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="8436f-111">資源物件包含 IndexingPolicy、PartitionKey、DefaultTtl、UniqueKeyPolicy、ConflictResolutionPolicy、_rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="8436f-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="8436f-112">參數</span><span class="sxs-lookup"><span data-stu-id="8436f-112">PARAMETERS</span></span>

### <span data-ttu-id="8436f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8436f-113">-AccountName</span></span>
<span data-ttu-id="8436f-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8436f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8436f-115">-確認</span><span class="sxs-lookup"><span data-stu-id="8436f-115">-Confirm</span></span>
<span data-ttu-id="8436f-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8436f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8436f-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8436f-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="8436f-118">PSConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="8436f-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8436f-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="8436f-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="8436f-120">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="8436f-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="8436f-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="8436f-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="8436f-122">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="8436f-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="8436f-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="8436f-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="8436f-124">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="8436f-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="8436f-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8436f-125">-DatabaseName</span></span>
<span data-ttu-id="8436f-126">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8436f-126">Database name.</span></span>

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

### <span data-ttu-id="8436f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8436f-127">-DefaultProfile</span></span>
<span data-ttu-id="8436f-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8436f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8436f-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="8436f-129">-IndexingPolicy</span></span>
<span data-ttu-id="8436f-130">PSSqlIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="8436f-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8436f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8436f-131">-InputObject</span></span>
<span data-ttu-id="8436f-132">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="8436f-132">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8436f-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="8436f-133">-Name</span></span>
<span data-ttu-id="8436f-134">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="8436f-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="8436f-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="8436f-135">-PartitionKeyKind</span></span>
<span data-ttu-id="8436f-136">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="8436f-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="8436f-137">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="8436f-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="8436f-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="8436f-138">-PartitionKeyPath</span></span>
<span data-ttu-id="8436f-139">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="8436f-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="8436f-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8436f-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="8436f-141">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="8436f-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="8436f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8436f-142">-ResourceGroupName</span></span>
<span data-ttu-id="8436f-143">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8436f-143">Name of resource group.</span></span>

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

### <span data-ttu-id="8436f-144">-輸送量</span><span class="sxs-lookup"><span data-stu-id="8436f-144">-Throughput</span></span>
<span data-ttu-id="8436f-145">Gremlin 圖的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="8436f-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="8436f-146">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="8436f-146">Default value is 400.</span></span>

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

### <span data-ttu-id="8436f-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="8436f-147">-TtlInSeconds</span></span>
<span data-ttu-id="8436f-148">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8436f-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="8436f-149">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="8436f-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="8436f-150">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="8436f-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="8436f-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8436f-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="8436f-152">CosmosDB PSSqlUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="8436f-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8436f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8436f-153">-WhatIf</span></span>
<span data-ttu-id="8436f-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8436f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8436f-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8436f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8436f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8436f-156">CommonParameters</span></span>
<span data-ttu-id="8436f-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8436f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8436f-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8436f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8436f-159">輸入</span><span class="sxs-lookup"><span data-stu-id="8436f-159">INPUTS</span></span>

### <span data-ttu-id="8436f-160">PSIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="8436f-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="8436f-161">PSUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="8436f-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="8436f-162">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="8436f-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="8436f-163">輸出</span><span class="sxs-lookup"><span data-stu-id="8436f-163">OUTPUTS</span></span>

### <span data-ttu-id="8436f-164">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="8436f-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="8436f-165">筆記</span><span class="sxs-lookup"><span data-stu-id="8436f-165">NOTES</span></span>

## <span data-ttu-id="8436f-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="8436f-166">RELATED LINKS</span></span>
