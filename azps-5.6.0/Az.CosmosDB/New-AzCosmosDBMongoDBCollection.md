---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 3864693c5fd6da8c96557aac6f1626329f4e906f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902614"
---
# <span data-ttu-id="9bf60-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="9bf60-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="9bf60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9bf60-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf60-103">建立新一代的GosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="9bf60-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="9bf60-104">語法</span><span class="sxs-lookup"><span data-stu-id="9bf60-104">SYNTAX</span></span>

### <span data-ttu-id="9bf60-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9bf60-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf60-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf60-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf60-107">描述</span><span class="sxs-lookup"><span data-stu-id="9bf60-107">DESCRIPTION</span></span>
<span data-ttu-id="9bf60-108">建立新一代的GosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="9bf60-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="9bf60-109">例子</span><span class="sxs-lookup"><span data-stu-id="9bf60-109">EXAMPLES</span></span>

### <span data-ttu-id="9bf60-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="9bf60-110">Example 1</span></span>
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

## <span data-ttu-id="9bf60-111">參數</span><span class="sxs-lookup"><span data-stu-id="9bf60-111">PARAMETERS</span></span>

### <span data-ttu-id="9bf60-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9bf60-112">-AccountName</span></span>
<span data-ttu-id="9bf60-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf60-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9bf60-114">-分析StorageTtl</span><span class="sxs-lookup"><span data-stu-id="9bf60-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="9bf60-115">用於分析儲存的 TTL。</span><span class="sxs-lookup"><span data-stu-id="9bf60-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="9bf60-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9bf60-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9bf60-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="9bf60-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9bf60-118">-確認</span><span class="sxs-lookup"><span data-stu-id="9bf60-118">-Confirm</span></span>
<span data-ttu-id="9bf60-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9bf60-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf60-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bf60-120">-DatabaseName</span></span>
<span data-ttu-id="9bf60-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf60-121">Database name.</span></span>

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

### <span data-ttu-id="9bf60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf60-122">-DefaultProfile</span></span>
<span data-ttu-id="9bf60-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bf60-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf60-124">-索引</span><span class="sxs-lookup"><span data-stu-id="9bf60-124">-Index</span></span>
<span data-ttu-id="9bf60-125">PSMongoIndex 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="9bf60-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="9bf60-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9bf60-126">-Name</span></span>
<span data-ttu-id="9bf60-127">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf60-127">Collection name.</span></span>

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

### <span data-ttu-id="9bf60-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9bf60-128">-ParentObject</span></span>
<span data-ttu-id="9bf60-129">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="9bf60-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="9bf60-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf60-130">-ResourceGroupName</span></span>
<span data-ttu-id="9bf60-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf60-131">Name of resource group.</span></span>

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

### <span data-ttu-id="9bf60-132">-S一</span><span class="sxs-lookup"><span data-stu-id="9bf60-132">-Shard</span></span>
<span data-ttu-id="9bf60-133">Singing 鍵路徑。</span><span class="sxs-lookup"><span data-stu-id="9bf60-133">Sharding key path.</span></span>

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

### <span data-ttu-id="9bf60-134">-輸送量</span><span class="sxs-lookup"><span data-stu-id="9bf60-134">-Throughput</span></span>
<span data-ttu-id="9bf60-135">SQL 容器的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="9bf60-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="9bf60-136">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="9bf60-136">Default value is 400.</span></span>

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

### <span data-ttu-id="9bf60-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf60-137">-WhatIf</span></span>
<span data-ttu-id="9bf60-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bf60-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf60-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bf60-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf60-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf60-140">CommonParameters</span></span>
<span data-ttu-id="9bf60-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9bf60-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf60-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bf60-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf60-143">輸入</span><span class="sxs-lookup"><span data-stu-id="9bf60-143">INPUTS</span></span>

### <span data-ttu-id="9bf60-144">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9bf60-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="9bf60-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9bf60-145">OUTPUTS</span></span>

### <span data-ttu-id="9bf60-146">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="9bf60-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="9bf60-147">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="9bf60-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="9bf60-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9bf60-148">NOTES</span></span>

## <span data-ttu-id="9bf60-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bf60-149">RELATED LINKS</span></span>
