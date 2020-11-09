---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285583"
---
# <span data-ttu-id="f12f7-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="f12f7-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="f12f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f12f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f12f7-103">取得 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="f12f7-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="f12f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="f12f7-104">SYNTAX</span></span>

### <span data-ttu-id="f12f7-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f12f7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="f12f7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f12f7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f12f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="f12f7-107">DESCRIPTION</span></span>
<span data-ttu-id="f12f7-108">**AzCosmosDBMongoDBCollection** Cmdlet 會取得 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="f12f7-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="f12f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="f12f7-109">EXAMPLES</span></span>

### <span data-ttu-id="f12f7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f12f7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="f12f7-111">資源物件包含 MongoIndexes、_rid、_ts _etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="f12f7-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="f12f7-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f12f7-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="f12f7-113">這個範例會取得所檢索之集合的 ShardKey</span><span class="sxs-lookup"><span data-stu-id="f12f7-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="f12f7-114">參數</span><span class="sxs-lookup"><span data-stu-id="f12f7-114">PARAMETERS</span></span>

### <span data-ttu-id="f12f7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f12f7-115">-AccountName</span></span>
<span data-ttu-id="f12f7-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f12f7-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f12f7-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f12f7-117">-DatabaseName</span></span>
<span data-ttu-id="f12f7-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f12f7-118">Database name.</span></span>

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

### <span data-ttu-id="f12f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12f7-119">-DefaultProfile</span></span>
<span data-ttu-id="f12f7-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f12f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f12f7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f12f7-121">-Name</span></span>
<span data-ttu-id="f12f7-122">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="f12f7-122">Collection name.</span></span>

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

### <span data-ttu-id="f12f7-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f12f7-123">-ParentObject</span></span>
<span data-ttu-id="f12f7-124">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="f12f7-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="f12f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f12f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f12f7-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f12f7-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f12f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12f7-127">CommonParameters</span></span>
<span data-ttu-id="f12f7-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f12f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12f7-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f12f7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12f7-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f12f7-130">INPUTS</span></span>

### <span data-ttu-id="f12f7-131">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f12f7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="f12f7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f12f7-132">OUTPUTS</span></span>

### <span data-ttu-id="f12f7-133">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f12f7-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="f12f7-134">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f12f7-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f12f7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f12f7-135">NOTES</span></span>

## <span data-ttu-id="f12f7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f12f7-136">RELATED LINKS</span></span>
