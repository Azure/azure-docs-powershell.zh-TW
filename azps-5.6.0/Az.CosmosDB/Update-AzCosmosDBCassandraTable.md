---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 3f41c44c6abffaf5147ffba17fe3ec84561315b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908278"
---
# <span data-ttu-id="07881-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="07881-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="07881-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07881-102">SYNOPSIS</span></span>
<span data-ttu-id="07881-103">更新了一個更新的一個資料表。</span><span class="sxs-lookup"><span data-stu-id="07881-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="07881-104">讀取現有的表格以執行用戶端修補作業。</span><span class="sxs-lookup"><span data-stu-id="07881-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="07881-105">語法</span><span class="sxs-lookup"><span data-stu-id="07881-105">SYNTAX</span></span>

### <span data-ttu-id="07881-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="07881-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07881-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07881-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07881-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07881-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07881-109">描述</span><span class="sxs-lookup"><span data-stu-id="07881-109">DESCRIPTION</span></span>
<span data-ttu-id="07881-110">更新了一個更新的一個資料表。</span><span class="sxs-lookup"><span data-stu-id="07881-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="07881-111">讀取現有的表格以執行用戶端修補作業。</span><span class="sxs-lookup"><span data-stu-id="07881-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="07881-112">例子</span><span class="sxs-lookup"><span data-stu-id="07881-112">EXAMPLES</span></span>

### <span data-ttu-id="07881-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="07881-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="07881-114">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="07881-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="07881-115">參數</span><span class="sxs-lookup"><span data-stu-id="07881-115">PARAMETERS</span></span>

### <span data-ttu-id="07881-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07881-116">-AccountName</span></span>
<span data-ttu-id="07881-117">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="07881-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="07881-118">-分析StorageTtl</span><span class="sxs-lookup"><span data-stu-id="07881-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="07881-119">分析儲存空間 TTL。</span><span class="sxs-lookup"><span data-stu-id="07881-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="07881-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="07881-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="07881-121">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="07881-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="07881-122">-確認</span><span class="sxs-lookup"><span data-stu-id="07881-122">-Confirm</span></span>
<span data-ttu-id="07881-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="07881-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07881-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07881-124">-DefaultProfile</span></span>
<span data-ttu-id="07881-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07881-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07881-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07881-126">-InputObject</span></span>
<span data-ttu-id="07881-127">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="07881-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="07881-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="07881-128">-KeyspaceName</span></span>
<span data-ttu-id="07881-129">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="07881-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="07881-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="07881-130">-Name</span></span>
<span data-ttu-id="07881-131">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="07881-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="07881-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="07881-132">-ParentObject</span></span>
<span data-ttu-id="07881-133">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="07881-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="07881-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07881-134">-ResourceGroupName</span></span>
<span data-ttu-id="07881-135">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07881-135">Name of resource group.</span></span>

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

### <span data-ttu-id="07881-136">-架構</span><span class="sxs-lookup"><span data-stu-id="07881-136">-Schema</span></span>
<span data-ttu-id="07881-137">PSCassandraSchema 物件。</span><span class="sxs-lookup"><span data-stu-id="07881-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="07881-138">使用New-AzCosmosDBCassandraSchema建立此物件。</span><span class="sxs-lookup"><span data-stu-id="07881-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="07881-139">-輸送量</span><span class="sxs-lookup"><span data-stu-id="07881-139">-Throughput</span></span>
<span data-ttu-id="07881-140">Cassandra Keyspace (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="07881-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="07881-141">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="07881-141">Default value is 400.</span></span>

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

### <span data-ttu-id="07881-142">-TtlIn用秒</span><span class="sxs-lookup"><span data-stu-id="07881-142">-TtlInSeconds</span></span>
<span data-ttu-id="07881-143">預設 Ttl ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="07881-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="07881-144">如果值遺失或設為 - 1，專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="07881-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="07881-145">如果值設為 n，則專案會在上次修改時間之後的第 n 秒過期。</span><span class="sxs-lookup"><span data-stu-id="07881-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="07881-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07881-146">-WhatIf</span></span>
<span data-ttu-id="07881-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07881-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07881-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07881-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07881-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07881-149">CommonParameters</span></span>
<span data-ttu-id="07881-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07881-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07881-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07881-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07881-152">輸入</span><span class="sxs-lookup"><span data-stu-id="07881-152">INPUTS</span></span>

### <span data-ttu-id="07881-153">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="07881-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="07881-154">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="07881-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="07881-155">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="07881-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="07881-156">輸出</span><span class="sxs-lookup"><span data-stu-id="07881-156">OUTPUTS</span></span>

### <span data-ttu-id="07881-157">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="07881-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="07881-158">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="07881-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="07881-159">筆記</span><span class="sxs-lookup"><span data-stu-id="07881-159">NOTES</span></span>

## <span data-ttu-id="07881-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="07881-160">RELATED LINKS</span></span>
