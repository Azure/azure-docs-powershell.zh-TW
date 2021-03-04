---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 500bd1203f7f70b5749986a6b4ff1ab8d5978185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908254"
---
# <span data-ttu-id="4aea8-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="4aea8-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="4aea8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4aea8-102">SYNOPSIS</span></span>
<span data-ttu-id="4aea8-103">更新一些更新的一些資訊。</span><span class="sxs-lookup"><span data-stu-id="4aea8-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="4aea8-104">讀取現有的 Graph 以執行用戶端修補作業。</span><span class="sxs-lookup"><span data-stu-id="4aea8-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="4aea8-105">語法</span><span class="sxs-lookup"><span data-stu-id="4aea8-105">SYNTAX</span></span>

### <span data-ttu-id="4aea8-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4aea8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aea8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aea8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aea8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aea8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aea8-109">描述</span><span class="sxs-lookup"><span data-stu-id="4aea8-109">DESCRIPTION</span></span>
<span data-ttu-id="4aea8-110">更新一些更新的一些資訊。</span><span class="sxs-lookup"><span data-stu-id="4aea8-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="4aea8-111">讀取現有的 Graph 以執行用戶端修補作業。</span><span class="sxs-lookup"><span data-stu-id="4aea8-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="4aea8-112">例子</span><span class="sxs-lookup"><span data-stu-id="4aea8-112">EXAMPLES</span></span>

### <span data-ttu-id="4aea8-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="4aea8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="4aea8-114">參數</span><span class="sxs-lookup"><span data-stu-id="4aea8-114">PARAMETERS</span></span>

### <span data-ttu-id="4aea8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4aea8-115">-AccountName</span></span>
<span data-ttu-id="4aea8-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aea8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4aea8-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4aea8-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4aea8-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="4aea8-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4aea8-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4aea8-119">-Confirm</span></span>
<span data-ttu-id="4aea8-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4aea8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aea8-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4aea8-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="4aea8-122">類型 PSConflictResolutionPolicy 的 ConflictResolutionPolicy 物件，如果提供此選項，則設為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="4aea8-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="4aea8-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="4aea8-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="4aea8-124">可以有值：LastWriterWins，自訂，手動。</span><span class="sxs-lookup"><span data-stu-id="4aea8-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="4aea8-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="4aea8-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="4aea8-126">當類型為 LastWriterWins 時提供。</span><span class="sxs-lookup"><span data-stu-id="4aea8-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="4aea8-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="4aea8-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="4aea8-128">在自訂類型時提供。</span><span class="sxs-lookup"><span data-stu-id="4aea8-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="4aea8-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4aea8-129">-DatabaseName</span></span>
<span data-ttu-id="4aea8-130">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4aea8-130">Database name.</span></span>

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

### <span data-ttu-id="4aea8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aea8-131">-DefaultProfile</span></span>
<span data-ttu-id="4aea8-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4aea8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aea8-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="4aea8-133">-IndexingPolicy</span></span>
<span data-ttu-id="4aea8-134">類型為 Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy 的索引策略物件。</span><span class="sxs-lookup"><span data-stu-id="4aea8-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="4aea8-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aea8-135">-InputObject</span></span>
<span data-ttu-id="4aea8-136">億萬繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="4aea8-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="4aea8-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="4aea8-137">-Name</span></span>
<span data-ttu-id="4aea8-138">百分百圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="4aea8-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="4aea8-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4aea8-139">-ParentObject</span></span>
<span data-ttu-id="4aea8-140">資料表資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="4aea8-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="4aea8-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="4aea8-141">-PartitionKeyKind</span></span>
<span data-ttu-id="4aea8-142">用於分割的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="4aea8-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="4aea8-143">可能的值包括：'雜湊'、'範圍'</span><span class="sxs-lookup"><span data-stu-id="4aea8-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="4aea8-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="4aea8-144">-PartitionKeyPath</span></span>
<span data-ttu-id="4aea8-145">分割鍵路徑，例如'/address/zipcode'。</span><span class="sxs-lookup"><span data-stu-id="4aea8-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="4aea8-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4aea8-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="4aea8-147">分割鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="4aea8-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="4aea8-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aea8-148">-ResourceGroupName</span></span>
<span data-ttu-id="4aea8-149">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aea8-149">Name of resource group.</span></span>

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

### <span data-ttu-id="4aea8-150">-輸送量</span><span class="sxs-lookup"><span data-stu-id="4aea8-150">-Throughput</span></span>
<span data-ttu-id="4aea8-151">在 Ru/s (中，) 。</span><span class="sxs-lookup"><span data-stu-id="4aea8-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="4aea8-152">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="4aea8-152">Default value is 400.</span></span>

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

### <span data-ttu-id="4aea8-153">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="4aea8-153">-TtlInSeconds</span></span>
<span data-ttu-id="4aea8-154">預設 Ttl ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="4aea8-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="4aea8-155">如果值遺失或設為 - 1，專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="4aea8-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="4aea8-156">如果值設為 n，則專案會在上次修改時間之後的第 n 秒過期。</span><span class="sxs-lookup"><span data-stu-id="4aea8-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="4aea8-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4aea8-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="4aea8-158">類型為 Microsoft.Azure.Commands.代斯DB.PSUniqueKeyPolicy 的 UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="4aea8-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="4aea8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aea8-159">-WhatIf</span></span>
<span data-ttu-id="4aea8-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4aea8-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aea8-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4aea8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aea8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aea8-162">CommonParameters</span></span>
<span data-ttu-id="4aea8-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4aea8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aea8-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aea8-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aea8-165">輸入</span><span class="sxs-lookup"><span data-stu-id="4aea8-165">INPUTS</span></span>

### <span data-ttu-id="4aea8-166">Microsoft.Azure.Commands.AzsDB.models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="4aea8-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="4aea8-167">Microsoft.Azure.Commands.AzsDB.models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4aea8-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="4aea8-168">Microsoft.Azure.Commands.AzsDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4aea8-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="4aea8-169">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4aea8-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="4aea8-170">Microsoft.Azure.Commands.AzsDB.models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="4aea8-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="4aea8-171">輸出</span><span class="sxs-lookup"><span data-stu-id="4aea8-171">OUTPUTS</span></span>

### <span data-ttu-id="4aea8-172">Microsoft.Azure.Commands.AzsDB.models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="4aea8-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="4aea8-173">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="4aea8-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="4aea8-174">筆記</span><span class="sxs-lookup"><span data-stu-id="4aea8-174">NOTES</span></span>

## <span data-ttu-id="4aea8-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="4aea8-175">RELATED LINKS</span></span>
