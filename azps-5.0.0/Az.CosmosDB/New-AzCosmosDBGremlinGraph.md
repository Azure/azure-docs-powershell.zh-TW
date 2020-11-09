---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285517"
---
# <span data-ttu-id="2cb72-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="2cb72-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="2cb72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cb72-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb72-103">建立新的 CosmosDB Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="2cb72-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="2cb72-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cb72-104">SYNTAX</span></span>

### <span data-ttu-id="2cb72-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2cb72-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cb72-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cb72-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cb72-107">說明</span><span class="sxs-lookup"><span data-stu-id="2cb72-107">DESCRIPTION</span></span>
<span data-ttu-id="2cb72-108">建立新的 CosmosDB Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="2cb72-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="2cb72-109">示例</span><span class="sxs-lookup"><span data-stu-id="2cb72-109">EXAMPLES</span></span>

### <span data-ttu-id="2cb72-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2cb72-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="2cb72-111">參數</span><span class="sxs-lookup"><span data-stu-id="2cb72-111">PARAMETERS</span></span>

### <span data-ttu-id="2cb72-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2cb72-112">-AccountName</span></span>
<span data-ttu-id="2cb72-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cb72-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2cb72-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2cb72-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2cb72-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="2cb72-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2cb72-116">-確認</span><span class="sxs-lookup"><span data-stu-id="2cb72-116">-Confirm</span></span>
<span data-ttu-id="2cb72-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2cb72-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cb72-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cb72-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="2cb72-119">PSConflictResolutionPolicy 類型的 ConflictResolutionPolicy 物件（如果有的話）會設定為容器的 ConflictResolutionPolicy。</span><span class="sxs-lookup"><span data-stu-id="2cb72-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="2cb72-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="2cb72-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="2cb72-121">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="2cb72-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="2cb72-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="2cb72-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="2cb72-123">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="2cb72-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="2cb72-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="2cb72-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="2cb72-125">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="2cb72-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="2cb72-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2cb72-126">-DatabaseName</span></span>
<span data-ttu-id="2cb72-127">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2cb72-127">Database name.</span></span>

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

### <span data-ttu-id="2cb72-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb72-128">-DefaultProfile</span></span>
<span data-ttu-id="2cb72-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cb72-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cb72-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2cb72-130">-IndexingPolicy</span></span>
<span data-ttu-id="2cb72-131">PSIndexingPolicy 的索引原則物件。 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2cb72-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="2cb72-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cb72-132">-Name</span></span>
<span data-ttu-id="2cb72-133">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="2cb72-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="2cb72-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2cb72-134">-ParentObject</span></span>
<span data-ttu-id="2cb72-135">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="2cb72-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="2cb72-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="2cb72-136">-PartitionKeyKind</span></span>
<span data-ttu-id="2cb72-137">用於分區的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="2cb72-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="2cb72-138">可能的值包括： "Hash"，"Range"</span><span class="sxs-lookup"><span data-stu-id="2cb72-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="2cb72-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="2cb72-139">-PartitionKeyPath</span></span>
<span data-ttu-id="2cb72-140">分區鍵路徑，例如 "/address/zipcode"。</span><span class="sxs-lookup"><span data-stu-id="2cb72-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="2cb72-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2cb72-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="2cb72-142">分區鍵定義的版本</span><span class="sxs-lookup"><span data-stu-id="2cb72-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="2cb72-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb72-143">-ResourceGroupName</span></span>
<span data-ttu-id="2cb72-144">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cb72-144">Name of resource group.</span></span>

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

### <span data-ttu-id="2cb72-145">-輸送量</span><span class="sxs-lookup"><span data-stu-id="2cb72-145">-Throughput</span></span>
<span data-ttu-id="2cb72-146">Gremlin 圖的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="2cb72-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="2cb72-147">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="2cb72-147">Default value is 400.</span></span>

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

### <span data-ttu-id="2cb72-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2cb72-148">-TtlInSeconds</span></span>
<span data-ttu-id="2cb72-149">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2cb72-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="2cb72-150">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="2cb72-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="2cb72-151">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="2cb72-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="2cb72-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2cb72-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="2cb72-153">CosmosDB PSUniqueKeyPolicy 的 UniqueKeyPolicy 物件類型。</span><span class="sxs-lookup"><span data-stu-id="2cb72-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="2cb72-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cb72-154">-WhatIf</span></span>
<span data-ttu-id="2cb72-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2cb72-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb72-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cb72-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cb72-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb72-157">CommonParameters</span></span>
<span data-ttu-id="2cb72-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cb72-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb72-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2cb72-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb72-160">輸入</span><span class="sxs-lookup"><span data-stu-id="2cb72-160">INPUTS</span></span>

### <span data-ttu-id="2cb72-161">PSIndexingPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2cb72-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="2cb72-162">PSUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2cb72-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="2cb72-163">PSConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2cb72-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="2cb72-164">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2cb72-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="2cb72-165">輸出</span><span class="sxs-lookup"><span data-stu-id="2cb72-165">OUTPUTS</span></span>

### <span data-ttu-id="2cb72-166">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2cb72-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="2cb72-167">Exception</span><span class="sxs-lookup"><span data-stu-id="2cb72-167">System.Exception</span></span>

## <span data-ttu-id="2cb72-168">筆記</span><span class="sxs-lookup"><span data-stu-id="2cb72-168">NOTES</span></span>

## <span data-ttu-id="2cb72-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cb72-169">RELATED LINKS</span></span>
