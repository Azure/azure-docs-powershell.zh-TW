---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136075"
---
# <span data-ttu-id="32887-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="32887-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="32887-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32887-102">SYNOPSIS</span></span>
<span data-ttu-id="32887-103">建立新的 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="32887-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="32887-104">句法</span><span class="sxs-lookup"><span data-stu-id="32887-104">SYNTAX</span></span>

### <span data-ttu-id="32887-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="32887-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32887-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32887-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32887-107">說明</span><span class="sxs-lookup"><span data-stu-id="32887-107">DESCRIPTION</span></span>
<span data-ttu-id="32887-108">建立新的 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="32887-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="32887-109">示例</span><span class="sxs-lookup"><span data-stu-id="32887-109">EXAMPLES</span></span>

### <span data-ttu-id="32887-110">範例1</span><span class="sxs-lookup"><span data-stu-id="32887-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="32887-111">參數</span><span class="sxs-lookup"><span data-stu-id="32887-111">PARAMETERS</span></span>

### <span data-ttu-id="32887-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="32887-112">-AccountName</span></span>
<span data-ttu-id="32887-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="32887-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="32887-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="32887-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="32887-115">分析儲存空間的 TTL。</span><span class="sxs-lookup"><span data-stu-id="32887-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="32887-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="32887-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="32887-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="32887-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="32887-118">-確認</span><span class="sxs-lookup"><span data-stu-id="32887-118">-Confirm</span></span>
<span data-ttu-id="32887-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32887-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32887-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32887-120">-DatabaseName</span></span>
<span data-ttu-id="32887-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="32887-121">Database name.</span></span>

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

### <span data-ttu-id="32887-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32887-122">-DefaultProfile</span></span>
<span data-ttu-id="32887-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32887-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32887-124">-索引</span><span class="sxs-lookup"><span data-stu-id="32887-124">-Index</span></span>
<span data-ttu-id="32887-125">PSMongoIndex 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="32887-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="32887-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="32887-126">-Name</span></span>
<span data-ttu-id="32887-127">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="32887-127">Collection name.</span></span>

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

### <span data-ttu-id="32887-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="32887-128">-ParentObject</span></span>
<span data-ttu-id="32887-129">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="32887-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="32887-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32887-130">-ResourceGroupName</span></span>
<span data-ttu-id="32887-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32887-131">Name of resource group.</span></span>

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

### <span data-ttu-id="32887-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="32887-132">-Shard</span></span>
<span data-ttu-id="32887-133">Sharding 鍵路徑。</span><span class="sxs-lookup"><span data-stu-id="32887-133">Sharding key path.</span></span>

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

### <span data-ttu-id="32887-134">-輸送量</span><span class="sxs-lookup"><span data-stu-id="32887-134">-Throughput</span></span>
<span data-ttu-id="32887-135">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="32887-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="32887-136">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="32887-136">Default value is 400.</span></span>

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

### <span data-ttu-id="32887-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32887-137">-WhatIf</span></span>
<span data-ttu-id="32887-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32887-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32887-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32887-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32887-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32887-140">CommonParameters</span></span>
<span data-ttu-id="32887-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32887-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32887-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32887-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32887-143">輸入</span><span class="sxs-lookup"><span data-stu-id="32887-143">INPUTS</span></span>

### <span data-ttu-id="32887-144">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="32887-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="32887-145">輸出</span><span class="sxs-lookup"><span data-stu-id="32887-145">OUTPUTS</span></span>

### <span data-ttu-id="32887-146">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="32887-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="32887-147">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="32887-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="32887-148">筆記</span><span class="sxs-lookup"><span data-stu-id="32887-148">NOTES</span></span>

## <span data-ttu-id="32887-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="32887-149">RELATED LINKS</span></span>
