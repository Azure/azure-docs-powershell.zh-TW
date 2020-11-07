---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965883"
---
# <span data-ttu-id="d3099-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="d3099-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="d3099-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3099-102">SYNOPSIS</span></span>
<span data-ttu-id="d3099-103">設定 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="d3099-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="d3099-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3099-104">SYNTAX</span></span>

### <span data-ttu-id="d3099-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3099-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3099-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3099-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3099-107">說明</span><span class="sxs-lookup"><span data-stu-id="d3099-107">DESCRIPTION</span></span>
<span data-ttu-id="d3099-108">**AzCosmosDBMongoDBCollection** Cmdlet 會設定 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="d3099-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="d3099-109">示例</span><span class="sxs-lookup"><span data-stu-id="d3099-109">EXAMPLES</span></span>

### <span data-ttu-id="d3099-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d3099-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="d3099-111">資源物件包含 MongoIndexes、_rid、_ts _etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3099-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="d3099-112">參數</span><span class="sxs-lookup"><span data-stu-id="d3099-112">PARAMETERS</span></span>

### <span data-ttu-id="d3099-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3099-113">-AccountName</span></span>
<span data-ttu-id="d3099-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3099-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3099-115">-確認</span><span class="sxs-lookup"><span data-stu-id="d3099-115">-Confirm</span></span>
<span data-ttu-id="d3099-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3099-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3099-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3099-117">-DatabaseName</span></span>
<span data-ttu-id="d3099-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d3099-118">Database name.</span></span>

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

### <span data-ttu-id="d3099-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3099-119">-DefaultProfile</span></span>
<span data-ttu-id="d3099-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3099-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3099-121">-索引</span><span class="sxs-lookup"><span data-stu-id="d3099-121">-Index</span></span>
<span data-ttu-id="d3099-122">PSMongoIndex 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="d3099-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="d3099-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3099-123">-InputObject</span></span>
<span data-ttu-id="d3099-124">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="d3099-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="d3099-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3099-125">-Name</span></span>
<span data-ttu-id="d3099-126">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="d3099-126">Collection name.</span></span>

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

### <span data-ttu-id="d3099-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3099-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3099-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3099-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d3099-129">-Shard</span><span class="sxs-lookup"><span data-stu-id="d3099-129">-Shard</span></span>
<span data-ttu-id="d3099-130">Sharding 鍵路徑。</span><span class="sxs-lookup"><span data-stu-id="d3099-130">Sharding key path.</span></span>

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

### <span data-ttu-id="d3099-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="d3099-131">-Throughput</span></span>
<span data-ttu-id="d3099-132">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="d3099-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="d3099-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="d3099-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d3099-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3099-134">-WhatIf</span></span>
<span data-ttu-id="d3099-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3099-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3099-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3099-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3099-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3099-137">CommonParameters</span></span>
<span data-ttu-id="d3099-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3099-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3099-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3099-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3099-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d3099-140">INPUTS</span></span>

### <span data-ttu-id="d3099-141">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d3099-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="d3099-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d3099-142">OUTPUTS</span></span>

### <span data-ttu-id="d3099-143">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d3099-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="d3099-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d3099-144">NOTES</span></span>

## <span data-ttu-id="d3099-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3099-145">RELATED LINKS</span></span>
