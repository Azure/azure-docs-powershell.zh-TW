---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965568"
---
# <span data-ttu-id="5eea3-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="5eea3-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="5eea3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5eea3-102">SYNOPSIS</span></span>
<span data-ttu-id="5eea3-103">取得 CosmosDB Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="5eea3-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5eea3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5eea3-104">SYNTAX</span></span>

### <span data-ttu-id="5eea3-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5eea3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="5eea3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5eea3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eea3-107">說明</span><span class="sxs-lookup"><span data-stu-id="5eea3-107">DESCRIPTION</span></span>
<span data-ttu-id="5eea3-108">**AzCosmosDBGremlinGraph** Cmdlet 會取得 CosmosDB Gremlin 圖形屬性。</span><span class="sxs-lookup"><span data-stu-id="5eea3-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="5eea3-109">示例</span><span class="sxs-lookup"><span data-stu-id="5eea3-109">EXAMPLES</span></span>

### <span data-ttu-id="5eea3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5eea3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="5eea3-111">資源物件包含 IndexingPolicy、PartitionKey、DefaultTtl、UniqueKeyPolicy、ConflictResolutionPolicy、_rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="5eea3-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="5eea3-112">參數</span><span class="sxs-lookup"><span data-stu-id="5eea3-112">PARAMETERS</span></span>

### <span data-ttu-id="5eea3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5eea3-113">-AccountName</span></span>
<span data-ttu-id="5eea3-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5eea3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5eea3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5eea3-115">-DatabaseName</span></span>
<span data-ttu-id="5eea3-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5eea3-116">Database name.</span></span>

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

### <span data-ttu-id="5eea3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eea3-117">-DefaultProfile</span></span>
<span data-ttu-id="5eea3-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5eea3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eea3-119">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="5eea3-119">-Detailed</span></span>
<span data-ttu-id="5eea3-120">如果提供此選項，則 Cmdlet 會以對應的輸送量值傳回 Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="5eea3-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="5eea3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eea3-121">-InputObject</span></span>
<span data-ttu-id="5eea3-122">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5eea3-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5eea3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5eea3-123">-Name</span></span>
<span data-ttu-id="5eea3-124">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="5eea3-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5eea3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eea3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5eea3-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5eea3-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5eea3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eea3-127">CommonParameters</span></span>
<span data-ttu-id="5eea3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5eea3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eea3-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5eea3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eea3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5eea3-130">INPUTS</span></span>

### <span data-ttu-id="5eea3-131">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5eea3-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5eea3-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5eea3-132">OUTPUTS</span></span>

### <span data-ttu-id="5eea3-133">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5eea3-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="5eea3-134">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5eea3-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5eea3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5eea3-135">NOTES</span></span>

## <span data-ttu-id="5eea3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5eea3-136">RELATED LINKS</span></span>
