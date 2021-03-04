---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 2458c31ba75470c5d2b5bb2b73d817eb58c5bc61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908249"
---
# <span data-ttu-id="5f326-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5f326-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5f326-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5f326-102">SYNOPSIS</span></span>
<span data-ttu-id="5f326-103">更新代斯DB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="5f326-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="5f326-104">讀取現有的集合以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="5f326-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="5f326-105">語法</span><span class="sxs-lookup"><span data-stu-id="5f326-105">SYNTAX</span></span>

### <span data-ttu-id="5f326-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5f326-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f326-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f326-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f326-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f326-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f326-109">描述</span><span class="sxs-lookup"><span data-stu-id="5f326-109">DESCRIPTION</span></span>
<span data-ttu-id="5f326-110">更新代斯DB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="5f326-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="5f326-111">讀取現有的集合以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="5f326-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="5f326-112">例子</span><span class="sxs-lookup"><span data-stu-id="5f326-112">EXAMPLES</span></span>

### <span data-ttu-id="5f326-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="5f326-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="5f326-114">參數</span><span class="sxs-lookup"><span data-stu-id="5f326-114">PARAMETERS</span></span>

### <span data-ttu-id="5f326-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f326-115">-AccountName</span></span>
<span data-ttu-id="5f326-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f326-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5f326-117">-分析StorageTtl</span><span class="sxs-lookup"><span data-stu-id="5f326-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="5f326-118">用於分析儲存的 TTL。</span><span class="sxs-lookup"><span data-stu-id="5f326-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="5f326-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5f326-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5f326-120">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="5f326-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5f326-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5f326-121">-Confirm</span></span>
<span data-ttu-id="5f326-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5f326-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f326-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f326-123">-DatabaseName</span></span>
<span data-ttu-id="5f326-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5f326-124">Database name.</span></span>

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

### <span data-ttu-id="5f326-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f326-125">-DefaultProfile</span></span>
<span data-ttu-id="5f326-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f326-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f326-127">-索引</span><span class="sxs-lookup"><span data-stu-id="5f326-127">-Index</span></span>
<span data-ttu-id="5f326-128">PSMongoIndex 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="5f326-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="5f326-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f326-129">-InputObject</span></span>
<span data-ttu-id="5f326-130">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="5f326-130">Sql Container object.</span></span>

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

### <span data-ttu-id="5f326-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f326-131">-Name</span></span>
<span data-ttu-id="5f326-132">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="5f326-132">Collection name.</span></span>

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

### <span data-ttu-id="5f326-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5f326-133">-ParentObject</span></span>
<span data-ttu-id="5f326-134">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="5f326-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="5f326-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f326-135">-ResourceGroupName</span></span>
<span data-ttu-id="5f326-136">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f326-136">Name of resource group.</span></span>

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

### <span data-ttu-id="5f326-137">-S一</span><span class="sxs-lookup"><span data-stu-id="5f326-137">-Shard</span></span>
<span data-ttu-id="5f326-138">Singing 鍵路徑。</span><span class="sxs-lookup"><span data-stu-id="5f326-138">Sharding key path.</span></span>

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

### <span data-ttu-id="5f326-139">-輸送量</span><span class="sxs-lookup"><span data-stu-id="5f326-139">-Throughput</span></span>
<span data-ttu-id="5f326-140">SQL 容器的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="5f326-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="5f326-141">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="5f326-141">Default value is 400.</span></span>

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

### <span data-ttu-id="5f326-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f326-142">-WhatIf</span></span>
<span data-ttu-id="5f326-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f326-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f326-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f326-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f326-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f326-145">CommonParameters</span></span>
<span data-ttu-id="5f326-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5f326-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f326-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f326-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f326-148">輸入</span><span class="sxs-lookup"><span data-stu-id="5f326-148">INPUTS</span></span>

### <span data-ttu-id="5f326-149">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5f326-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="5f326-150">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5f326-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="5f326-151">輸出</span><span class="sxs-lookup"><span data-stu-id="5f326-151">OUTPUTS</span></span>

### <span data-ttu-id="5f326-152">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5f326-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="5f326-153">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5f326-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5f326-154">筆記</span><span class="sxs-lookup"><span data-stu-id="5f326-154">NOTES</span></span>

## <span data-ttu-id="5f326-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f326-155">RELATED LINKS</span></span>
