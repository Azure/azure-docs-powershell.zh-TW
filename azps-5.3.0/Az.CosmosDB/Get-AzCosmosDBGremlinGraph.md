---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449602"
---
# <span data-ttu-id="dc8aa-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="dc8aa-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="dc8aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8aa-103">取得 CosmosDB Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="dc8aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc8aa-104">SYNTAX</span></span>

### <span data-ttu-id="dc8aa-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc8aa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="dc8aa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc8aa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc8aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="dc8aa-108">**AzCosmosDBGremlinGraph** Cmdlet 會取得 CosmosDB Gremlin 圖形屬性。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="dc8aa-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc8aa-109">EXAMPLES</span></span>

### <span data-ttu-id="dc8aa-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dc8aa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="dc8aa-111">資源物件包含 IndexingPolicy、PartitionKey、DefaultTtl、UniqueKeyPolicy、ConflictResolutionPolicy、_rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="dc8aa-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc8aa-112">PARAMETERS</span></span>

### <span data-ttu-id="dc8aa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc8aa-113">-AccountName</span></span>
<span data-ttu-id="dc8aa-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc8aa-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc8aa-115">-DatabaseName</span></span>
<span data-ttu-id="dc8aa-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-116">Database name.</span></span>

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

### <span data-ttu-id="dc8aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8aa-117">-DefaultProfile</span></span>
<span data-ttu-id="dc8aa-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8aa-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc8aa-119">-Name</span></span>
<span data-ttu-id="dc8aa-120">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="dc8aa-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc8aa-121">-ParentObject</span></span>
<span data-ttu-id="dc8aa-122">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="dc8aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc8aa-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-124">Name of resource group.</span></span>

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

### <span data-ttu-id="dc8aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8aa-125">CommonParameters</span></span>
<span data-ttu-id="dc8aa-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8aa-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8aa-128">輸入</span><span class="sxs-lookup"><span data-stu-id="dc8aa-128">INPUTS</span></span>

### <span data-ttu-id="dc8aa-129">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="dc8aa-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dc8aa-130">OUTPUTS</span></span>

### <span data-ttu-id="dc8aa-131">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="dc8aa-132">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dc8aa-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dc8aa-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dc8aa-133">NOTES</span></span>

## <span data-ttu-id="dc8aa-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc8aa-134">RELATED LINKS</span></span>
