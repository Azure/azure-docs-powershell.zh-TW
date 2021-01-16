---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279177"
---
# <span data-ttu-id="3d693-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="3d693-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="3d693-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d693-102">SYNOPSIS</span></span>
<span data-ttu-id="3d693-103">取得 CosmosDB Gremlin 圖。</span><span class="sxs-lookup"><span data-stu-id="3d693-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="3d693-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d693-104">SYNTAX</span></span>

### <span data-ttu-id="3d693-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3d693-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="3d693-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d693-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d693-107">說明</span><span class="sxs-lookup"><span data-stu-id="3d693-107">DESCRIPTION</span></span>
<span data-ttu-id="3d693-108">**AzCosmosDBGremlinGraph** Cmdlet 會取得 CosmosDB Gremlin 圖形屬性。</span><span class="sxs-lookup"><span data-stu-id="3d693-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="3d693-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d693-109">EXAMPLES</span></span>

### <span data-ttu-id="3d693-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3d693-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="3d693-111">資源物件包含 IndexingPolicy、PartitionKey、DefaultTtl、UniqueKeyPolicy、ConflictResolutionPolicy、_rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="3d693-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="3d693-112">參數</span><span class="sxs-lookup"><span data-stu-id="3d693-112">PARAMETERS</span></span>

### <span data-ttu-id="3d693-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d693-113">-AccountName</span></span>
<span data-ttu-id="3d693-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d693-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3d693-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d693-115">-DatabaseName</span></span>
<span data-ttu-id="3d693-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3d693-116">Database name.</span></span>

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

### <span data-ttu-id="3d693-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d693-117">-DefaultProfile</span></span>
<span data-ttu-id="3d693-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d693-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d693-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d693-119">-Name</span></span>
<span data-ttu-id="3d693-120">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="3d693-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="3d693-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d693-121">-ParentObject</span></span>
<span data-ttu-id="3d693-122">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="3d693-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="3d693-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d693-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d693-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d693-124">Name of resource group.</span></span>

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

### <span data-ttu-id="3d693-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d693-125">CommonParameters</span></span>
<span data-ttu-id="3d693-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d693-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d693-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d693-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d693-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3d693-128">INPUTS</span></span>

### <span data-ttu-id="3d693-129">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3d693-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="3d693-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3d693-130">OUTPUTS</span></span>

### <span data-ttu-id="3d693-131">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3d693-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="3d693-132">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3d693-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3d693-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3d693-133">NOTES</span></span>

## <span data-ttu-id="3d693-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d693-134">RELATED LINKS</span></span>
