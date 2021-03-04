---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 464dbb54a96f7f543607cd2f053a0e7360eba344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917341"
---
# <span data-ttu-id="020df-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="020df-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="020df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="020df-102">SYNOPSIS</span></span>
<span data-ttu-id="020df-103">建立新一個管理中心Db 的一個圖形。</span><span class="sxs-lookup"><span data-stu-id="020df-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="020df-104">語法</span><span class="sxs-lookup"><span data-stu-id="020df-104">SYNTAX</span></span>

### <span data-ttu-id="020df-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="020df-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020df-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="020df-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="020df-107">描述</span><span class="sxs-lookup"><span data-stu-id="020df-107">DESCRIPTION</span></span>
<span data-ttu-id="020df-108">建立新一個管理中心Db 的一個圖形。</span><span class="sxs-lookup"><span data-stu-id="020df-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="020df-109">例子</span><span class="sxs-lookup"><span data-stu-id="020df-109">EXAMPLES</span></span>

### <span data-ttu-id="020df-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="020df-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="020df-111">參數</span><span class="sxs-lookup"><span data-stu-id="020df-111">PARAMETERS</span></span>

### <span data-ttu-id="020df-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="020df-112">-AccountName</span></span>
<span data-ttu-id="020df-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="020df-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="020df-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="020df-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="020df-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="020df-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="020df-116">-確認</span><span class="sxs-lookup"><span data-stu-id="020df-116">-Confirm</span></span>
<span data-ttu-id="020df-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="020df-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020df-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="020df-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="020df-119">類型 PSConflictResolutionPolicy 的 ConflictResolutionPolicy 物件，如果提供此選項，則設為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="020df-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="020df-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="020df-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="020df-121">可以有值：LastWriterWins，自訂，手動。</span><span class="sxs-lookup"><span data-stu-id="020df-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="020df-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="020df-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="020df-123">當類型為 LastWriterWins 時提供。</span><span class="sxs-lookup"><span data-stu-id="020df-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="020df-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="020df-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="020df-125">在自訂類型時提供。</span><span class="sxs-lookup"><span data-stu-id="020df-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="020df-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="020df-126">-DatabaseName</span></span>
<span data-ttu-id="020df-127">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="020df-127">Database name.</span></span>

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

### <span data-ttu-id="020df-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020df-128">-DefaultProfile</span></span>
<span data-ttu-id="020df-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="020df-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020df-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="020df-130">-IndexingPolicy</span></span>
<span data-ttu-id="020df-131">類型為 Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy 的索引策略物件。</span><span class="sxs-lookup"><span data-stu-id="020df-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="020df-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="020df-132">-Name</span></span>
<span data-ttu-id="020df-133">百分百圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="020df-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="020df-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="020df-134">-ParentObject</span></span>
<span data-ttu-id="020df-135">資料表資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="020df-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="020df-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="020df-136">-PartitionKeyKind</span></span>
<span data-ttu-id="020df-137">用於分割的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="020df-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="020df-138">可能的值包括：'雜湊'、'範圍'</span><span class="sxs-lookup"><span data-stu-id="020df-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="020df-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="020df-139">-PartitionKeyPath</span></span>
<span data-ttu-id="020df-140">分割鍵路徑，例如'/address/zipcode'。</span><span class="sxs-lookup"><span data-stu-id="020df-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="020df-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="020df-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="020df-142">分割鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="020df-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="020df-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020df-143">-ResourceGroupName</span></span>
<span data-ttu-id="020df-144">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="020df-144">Name of resource group.</span></span>

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

### <span data-ttu-id="020df-145">-輸送量</span><span class="sxs-lookup"><span data-stu-id="020df-145">-Throughput</span></span>
<span data-ttu-id="020df-146">在 Ru/s (中，) 。</span><span class="sxs-lookup"><span data-stu-id="020df-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="020df-147">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="020df-147">Default value is 400.</span></span>

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

### <span data-ttu-id="020df-148">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="020df-148">-TtlInSeconds</span></span>
<span data-ttu-id="020df-149">預設 Ttl ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="020df-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="020df-150">如果值遺失或設為 - 1，專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="020df-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="020df-151">如果值設為 n，則專案會在上次修改時間之後的第 n 秒過期。</span><span class="sxs-lookup"><span data-stu-id="020df-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="020df-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="020df-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="020df-153">類型為 Microsoft.Azure.Commands.代斯DB.PSUniqueKeyPolicy 的 UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="020df-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="020df-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020df-154">-WhatIf</span></span>
<span data-ttu-id="020df-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="020df-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="020df-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="020df-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020df-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020df-157">CommonParameters</span></span>
<span data-ttu-id="020df-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="020df-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020df-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="020df-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020df-160">輸入</span><span class="sxs-lookup"><span data-stu-id="020df-160">INPUTS</span></span>

### <span data-ttu-id="020df-161">Microsoft.Azure.Commands.AzsDB.models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="020df-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="020df-162">Microsoft.Azure.Commands.AzsDB.models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="020df-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="020df-163">Microsoft.Azure.Commands.AzsDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="020df-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="020df-164">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="020df-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="020df-165">輸出</span><span class="sxs-lookup"><span data-stu-id="020df-165">OUTPUTS</span></span>

### <span data-ttu-id="020df-166">Microsoft.Azure.Commands.AzsDB.models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="020df-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="020df-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="020df-167">System.Exception</span></span>

## <span data-ttu-id="020df-168">筆記</span><span class="sxs-lookup"><span data-stu-id="020df-168">NOTES</span></span>

## <span data-ttu-id="020df-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="020df-169">RELATED LINKS</span></span>
