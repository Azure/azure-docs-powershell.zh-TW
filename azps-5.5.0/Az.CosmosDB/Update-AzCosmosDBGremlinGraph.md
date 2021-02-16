---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129647"
---
# <span data-ttu-id="f331e-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f331e-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f331e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f331e-102">SYNOPSIS</span></span>
<span data-ttu-id="f331e-103">更新 CosmosDB Gremlin 圖形。</span><span class="sxs-lookup"><span data-stu-id="f331e-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="f331e-104">透過讀取現有的圖形來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="f331e-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="f331e-105">句法</span><span class="sxs-lookup"><span data-stu-id="f331e-105">SYNTAX</span></span>

### <span data-ttu-id="f331e-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f331e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f331e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f331e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f331e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f331e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f331e-109">說明</span><span class="sxs-lookup"><span data-stu-id="f331e-109">DESCRIPTION</span></span>
<span data-ttu-id="f331e-110">更新 CosmosDB Gremlin 圖形。</span><span class="sxs-lookup"><span data-stu-id="f331e-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="f331e-111">透過讀取現有的圖形來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="f331e-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="f331e-112">示例</span><span class="sxs-lookup"><span data-stu-id="f331e-112">EXAMPLES</span></span>

### <span data-ttu-id="f331e-113">範例1</span><span class="sxs-lookup"><span data-stu-id="f331e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="f331e-114">參數</span><span class="sxs-lookup"><span data-stu-id="f331e-114">PARAMETERS</span></span>

### <span data-ttu-id="f331e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f331e-115">-AccountName</span></span>
<span data-ttu-id="f331e-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f331e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f331e-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f331e-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f331e-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="f331e-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f331e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f331e-119">-Confirm</span></span>
<span data-ttu-id="f331e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f331e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f331e-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f331e-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f331e-122">PSConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="f331e-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f331e-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f331e-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f331e-124">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="f331e-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f331e-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f331e-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f331e-126">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="f331e-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f331e-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f331e-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f331e-128">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="f331e-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f331e-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f331e-129">-DatabaseName</span></span>
<span data-ttu-id="f331e-130">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f331e-130">Database name.</span></span>

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

### <span data-ttu-id="f331e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f331e-131">-DefaultProfile</span></span>
<span data-ttu-id="f331e-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f331e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f331e-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f331e-133">-IndexingPolicy</span></span>
<span data-ttu-id="f331e-134">PSIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="f331e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f331e-135">-InputObject</span></span>
<span data-ttu-id="f331e-136">Gremlin Graph 物件。</span><span class="sxs-lookup"><span data-stu-id="f331e-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f331e-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="f331e-137">-Name</span></span>
<span data-ttu-id="f331e-138">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="f331e-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f331e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f331e-139">-ParentObject</span></span>
<span data-ttu-id="f331e-140">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="f331e-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f331e-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f331e-141">-PartitionKeyKind</span></span>
<span data-ttu-id="f331e-142">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="f331e-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f331e-143">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="f331e-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f331e-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f331e-144">-PartitionKeyPath</span></span>
<span data-ttu-id="f331e-145">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="f331e-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f331e-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f331e-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="f331e-147">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="f331e-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f331e-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f331e-148">-ResourceGroupName</span></span>
<span data-ttu-id="f331e-149">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f331e-149">Name of resource group.</span></span>

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

### <span data-ttu-id="f331e-150">-輸送量</span><span class="sxs-lookup"><span data-stu-id="f331e-150">-Throughput</span></span>
<span data-ttu-id="f331e-151">Gremlin 圖的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="f331e-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f331e-152">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="f331e-152">Default value is 400.</span></span>

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

### <span data-ttu-id="f331e-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f331e-153">-TtlInSeconds</span></span>
<span data-ttu-id="f331e-154">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f331e-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="f331e-155">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="f331e-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f331e-156">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="f331e-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f331e-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f331e-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f331e-158">CosmosDB PSUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="f331e-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f331e-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f331e-159">-WhatIf</span></span>
<span data-ttu-id="f331e-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f331e-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f331e-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f331e-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f331e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f331e-162">CommonParameters</span></span>
<span data-ttu-id="f331e-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f331e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f331e-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f331e-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f331e-165">輸入</span><span class="sxs-lookup"><span data-stu-id="f331e-165">INPUTS</span></span>

### <span data-ttu-id="f331e-166">PSIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="f331e-167">PSUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="f331e-168">PSConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="f331e-169">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="f331e-170">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="f331e-171">輸出</span><span class="sxs-lookup"><span data-stu-id="f331e-171">OUTPUTS</span></span>

### <span data-ttu-id="f331e-172">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f331e-173">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f331e-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f331e-174">筆記</span><span class="sxs-lookup"><span data-stu-id="f331e-174">NOTES</span></span>

## <span data-ttu-id="f331e-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="f331e-175">RELATED LINKS</span></span>
