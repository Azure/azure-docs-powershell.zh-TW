---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449524"
---
# <span data-ttu-id="1a68b-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="1a68b-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="1a68b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a68b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a68b-103">更新 CosmosDB Cassandra 資料表。</span><span class="sxs-lookup"><span data-stu-id="1a68b-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="1a68b-104">讀取現有的資料表，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="1a68b-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1a68b-105">句法</span><span class="sxs-lookup"><span data-stu-id="1a68b-105">SYNTAX</span></span>

### <span data-ttu-id="1a68b-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1a68b-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a68b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a68b-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a68b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a68b-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a68b-109">說明</span><span class="sxs-lookup"><span data-stu-id="1a68b-109">DESCRIPTION</span></span>
<span data-ttu-id="1a68b-110">更新 CosmosDB Cassandra 資料表。</span><span class="sxs-lookup"><span data-stu-id="1a68b-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="1a68b-111">讀取現有的資料表，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="1a68b-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1a68b-112">示例</span><span class="sxs-lookup"><span data-stu-id="1a68b-112">EXAMPLES</span></span>

### <span data-ttu-id="1a68b-113">範例1</span><span class="sxs-lookup"><span data-stu-id="1a68b-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="1a68b-114">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="1a68b-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="1a68b-115">參數</span><span class="sxs-lookup"><span data-stu-id="1a68b-115">PARAMETERS</span></span>

### <span data-ttu-id="1a68b-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a68b-116">-AccountName</span></span>
<span data-ttu-id="1a68b-117">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a68b-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1a68b-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="1a68b-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="1a68b-119">分析儲存 TTL。</span><span class="sxs-lookup"><span data-stu-id="1a68b-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="1a68b-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1a68b-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1a68b-121">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="1a68b-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1a68b-122">-確認</span><span class="sxs-lookup"><span data-stu-id="1a68b-122">-Confirm</span></span>
<span data-ttu-id="1a68b-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a68b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a68b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a68b-124">-DefaultProfile</span></span>
<span data-ttu-id="1a68b-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a68b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a68b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a68b-126">-InputObject</span></span>
<span data-ttu-id="1a68b-127">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="1a68b-127">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a68b-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="1a68b-128">-KeyspaceName</span></span>
<span data-ttu-id="1a68b-129">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="1a68b-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1a68b-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a68b-130">-Name</span></span>
<span data-ttu-id="1a68b-131">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="1a68b-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="1a68b-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1a68b-132">-ParentObject</span></span>
<span data-ttu-id="1a68b-133">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="1a68b-133">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a68b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a68b-134">-ResourceGroupName</span></span>
<span data-ttu-id="1a68b-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a68b-135">Name of resource group.</span></span>

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

### <span data-ttu-id="1a68b-136">-架構</span><span class="sxs-lookup"><span data-stu-id="1a68b-136">-Schema</span></span>
<span data-ttu-id="1a68b-137">PSCassandraSchema 物件。</span><span class="sxs-lookup"><span data-stu-id="1a68b-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="1a68b-138">使用 New-AzCosmosDBCassandraSchema 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="1a68b-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a68b-139">-輸送量</span><span class="sxs-lookup"><span data-stu-id="1a68b-139">-Throughput</span></span>
<span data-ttu-id="1a68b-140">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="1a68b-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="1a68b-141">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="1a68b-141">Default value is 400.</span></span>

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

### <span data-ttu-id="1a68b-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="1a68b-142">-TtlInSeconds</span></span>
<span data-ttu-id="1a68b-143">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a68b-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="1a68b-144">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="1a68b-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="1a68b-145">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="1a68b-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="1a68b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a68b-146">-WhatIf</span></span>
<span data-ttu-id="1a68b-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a68b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a68b-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a68b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a68b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a68b-149">CommonParameters</span></span>
<span data-ttu-id="1a68b-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a68b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a68b-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a68b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a68b-152">輸入</span><span class="sxs-lookup"><span data-stu-id="1a68b-152">INPUTS</span></span>

### <span data-ttu-id="1a68b-153">PSCassandraSchema 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1a68b-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="1a68b-154">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1a68b-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="1a68b-155">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1a68b-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="1a68b-156">輸出</span><span class="sxs-lookup"><span data-stu-id="1a68b-156">OUTPUTS</span></span>

### <span data-ttu-id="1a68b-157">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1a68b-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="1a68b-158">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1a68b-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1a68b-159">筆記</span><span class="sxs-lookup"><span data-stu-id="1a68b-159">NOTES</span></span>

## <span data-ttu-id="1a68b-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a68b-160">RELATED LINKS</span></span>
