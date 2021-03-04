---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909829"
---
# <span data-ttu-id="7cde6-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="7cde6-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="7cde6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7cde6-102">SYNOPSIS</span></span>
<span data-ttu-id="7cde6-103">獲得花格DB 的美分圖形。</span><span class="sxs-lookup"><span data-stu-id="7cde6-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="7cde6-104">語法</span><span class="sxs-lookup"><span data-stu-id="7cde6-104">SYNTAX</span></span>

### <span data-ttu-id="7cde6-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7cde6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="7cde6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cde6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cde6-107">描述</span><span class="sxs-lookup"><span data-stu-id="7cde6-107">DESCRIPTION</span></span>
<span data-ttu-id="7cde6-108">**Get-AzCosmosDBGremlinGraph** Cmdlet 會取得一些圖形屬性。。</span><span class="sxs-lookup"><span data-stu-id="7cde6-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="7cde6-109">例子</span><span class="sxs-lookup"><span data-stu-id="7cde6-109">EXAMPLES</span></span>

### <span data-ttu-id="7cde6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="7cde6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="7cde6-111">資源物件包含 IndexingPolicy、PartitionKey、DefaultTtl、UniqueKeyPolicy、ConflictResolutionPolicy、_rid、_ts、_etag。</span><span class="sxs-lookup"><span data-stu-id="7cde6-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="7cde6-112">參數</span><span class="sxs-lookup"><span data-stu-id="7cde6-112">PARAMETERS</span></span>

### <span data-ttu-id="7cde6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7cde6-113">-AccountName</span></span>
<span data-ttu-id="7cde6-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cde6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7cde6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7cde6-115">-DatabaseName</span></span>
<span data-ttu-id="7cde6-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7cde6-116">Database name.</span></span>

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

### <span data-ttu-id="7cde6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cde6-117">-DefaultProfile</span></span>
<span data-ttu-id="7cde6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cde6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cde6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7cde6-119">-Name</span></span>
<span data-ttu-id="7cde6-120">百分百圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="7cde6-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="7cde6-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7cde6-121">-ParentObject</span></span>
<span data-ttu-id="7cde6-122">資料表資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="7cde6-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="7cde6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cde6-123">-ResourceGroupName</span></span>
<span data-ttu-id="7cde6-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cde6-124">Name of resource group.</span></span>

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

### <span data-ttu-id="7cde6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cde6-125">CommonParameters</span></span>
<span data-ttu-id="7cde6-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7cde6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cde6-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cde6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cde6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7cde6-128">INPUTS</span></span>

### <span data-ttu-id="7cde6-129">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7cde6-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="7cde6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7cde6-130">OUTPUTS</span></span>

### <span data-ttu-id="7cde6-131">Microsoft.Azure.Commands.AzsDB.models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="7cde6-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="7cde6-132">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7cde6-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7cde6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7cde6-133">NOTES</span></span>

## <span data-ttu-id="7cde6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cde6-134">RELATED LINKS</span></span>
