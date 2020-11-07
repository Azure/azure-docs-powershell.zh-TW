---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965566"
---
# <span data-ttu-id="46e8c-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="46e8c-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="46e8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="46e8c-103">取得 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="46e8c-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="46e8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="46e8c-104">SYNTAX</span></span>

### <span data-ttu-id="46e8c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46e8c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="46e8c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46e8c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46e8c-107">說明</span><span class="sxs-lookup"><span data-stu-id="46e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="46e8c-108">**AzCosmosDBMongoDBCollection** Cmdlet 會取得 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="46e8c-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="46e8c-109">示例</span><span class="sxs-lookup"><span data-stu-id="46e8c-109">EXAMPLES</span></span>

### <span data-ttu-id="46e8c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="46e8c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="46e8c-111">資源物件包含 MongoIndexes、_rid、_ts _etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="46e8c-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="46e8c-112">參數</span><span class="sxs-lookup"><span data-stu-id="46e8c-112">PARAMETERS</span></span>

### <span data-ttu-id="46e8c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46e8c-113">-AccountName</span></span>
<span data-ttu-id="46e8c-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="46e8c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46e8c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46e8c-115">-DatabaseName</span></span>
<span data-ttu-id="46e8c-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="46e8c-116">Database name.</span></span>

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

### <span data-ttu-id="46e8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e8c-117">-DefaultProfile</span></span>
<span data-ttu-id="46e8c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46e8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e8c-119">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="46e8c-119">-Detailed</span></span>
<span data-ttu-id="46e8c-120">如果提供此選項，則 Cmdlet 會傳回具有對應的輸送量值的集合。</span><span class="sxs-lookup"><span data-stu-id="46e8c-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e8c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46e8c-121">-InputObject</span></span>
<span data-ttu-id="46e8c-122">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="46e8c-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="46e8c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="46e8c-123">-Name</span></span>
<span data-ttu-id="46e8c-124">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="46e8c-124">Collection name.</span></span>

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

### <span data-ttu-id="46e8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="46e8c-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46e8c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="46e8c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e8c-127">CommonParameters</span></span>
<span data-ttu-id="46e8c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46e8c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e8c-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46e8c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e8c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="46e8c-130">INPUTS</span></span>

### <span data-ttu-id="46e8c-131">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="46e8c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="46e8c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="46e8c-132">OUTPUTS</span></span>

### <span data-ttu-id="46e8c-133">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="46e8c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="46e8c-134">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="46e8c-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="46e8c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="46e8c-135">NOTES</span></span>

## <span data-ttu-id="46e8c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="46e8c-136">RELATED LINKS</span></span>
