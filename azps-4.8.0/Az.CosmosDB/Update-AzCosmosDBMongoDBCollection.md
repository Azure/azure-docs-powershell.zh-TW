---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128804"
---
# <span data-ttu-id="3423e-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="3423e-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="3423e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3423e-102">SYNOPSIS</span></span>
<span data-ttu-id="3423e-103">更新 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="3423e-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="3423e-104">讀取現有集合以執行用戶端修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="3423e-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="3423e-105">句法</span><span class="sxs-lookup"><span data-stu-id="3423e-105">SYNTAX</span></span>

### <span data-ttu-id="3423e-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3423e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3423e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3423e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3423e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3423e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3423e-109">說明</span><span class="sxs-lookup"><span data-stu-id="3423e-109">DESCRIPTION</span></span>
<span data-ttu-id="3423e-110">更新 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="3423e-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="3423e-111">讀取現有集合以執行用戶端修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="3423e-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="3423e-112">示例</span><span class="sxs-lookup"><span data-stu-id="3423e-112">EXAMPLES</span></span>

### <span data-ttu-id="3423e-113">範例1</span><span class="sxs-lookup"><span data-stu-id="3423e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="3423e-114">參數</span><span class="sxs-lookup"><span data-stu-id="3423e-114">PARAMETERS</span></span>

### <span data-ttu-id="3423e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3423e-115">-AccountName</span></span>
<span data-ttu-id="3423e-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3423e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3423e-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="3423e-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="3423e-118">分析儲存空間的 TTL。</span><span class="sxs-lookup"><span data-stu-id="3423e-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="3423e-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3423e-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3423e-120">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="3423e-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3423e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3423e-121">-Confirm</span></span>
<span data-ttu-id="3423e-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3423e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3423e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3423e-123">-DatabaseName</span></span>
<span data-ttu-id="3423e-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3423e-124">Database name.</span></span>

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

### <span data-ttu-id="3423e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3423e-125">-DefaultProfile</span></span>
<span data-ttu-id="3423e-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3423e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3423e-127">-索引</span><span class="sxs-lookup"><span data-stu-id="3423e-127">-Index</span></span>
<span data-ttu-id="3423e-128">PSMongoIndex 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="3423e-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3423e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3423e-129">-InputObject</span></span>
<span data-ttu-id="3423e-130">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="3423e-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3423e-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="3423e-131">-Name</span></span>
<span data-ttu-id="3423e-132">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="3423e-132">Collection name.</span></span>

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

### <span data-ttu-id="3423e-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3423e-133">-ParentObject</span></span>
<span data-ttu-id="3423e-134">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="3423e-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3423e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3423e-135">-ResourceGroupName</span></span>
<span data-ttu-id="3423e-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3423e-136">Name of resource group.</span></span>

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

### <span data-ttu-id="3423e-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="3423e-137">-Shard</span></span>
<span data-ttu-id="3423e-138">Sharding 鍵路徑。</span><span class="sxs-lookup"><span data-stu-id="3423e-138">Sharding key path.</span></span>

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

### <span data-ttu-id="3423e-139">-輸送量</span><span class="sxs-lookup"><span data-stu-id="3423e-139">-Throughput</span></span>
<span data-ttu-id="3423e-140">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="3423e-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="3423e-141">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="3423e-141">Default value is 400.</span></span>

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

### <span data-ttu-id="3423e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3423e-142">-WhatIf</span></span>
<span data-ttu-id="3423e-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3423e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3423e-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3423e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3423e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3423e-145">CommonParameters</span></span>
<span data-ttu-id="3423e-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3423e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3423e-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3423e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3423e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3423e-148">INPUTS</span></span>

### <span data-ttu-id="3423e-149">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3423e-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="3423e-150">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3423e-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="3423e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3423e-151">OUTPUTS</span></span>

### <span data-ttu-id="3423e-152">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3423e-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="3423e-153">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3423e-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="3423e-154">筆記</span><span class="sxs-lookup"><span data-stu-id="3423e-154">NOTES</span></span>

## <span data-ttu-id="3423e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="3423e-155">RELATED LINKS</span></span>
