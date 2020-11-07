---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965571"
---
# <span data-ttu-id="e2056-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e2056-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e2056-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2056-102">SYNOPSIS</span></span>
<span data-ttu-id="e2056-103">取得 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e2056-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e2056-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2056-104">SYNTAX</span></span>

### <span data-ttu-id="e2056-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e2056-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2056-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2056-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2056-107">說明</span><span class="sxs-lookup"><span data-stu-id="e2056-107">DESCRIPTION</span></span>
<span data-ttu-id="e2056-108">**AzCosmosDBGremlinDatabase** Cmdlet 會取得 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e2056-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e2056-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2056-109">EXAMPLES</span></span>

### <span data-ttu-id="e2056-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e2056-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="e2056-111">資源物件包含 _rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="e2056-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="e2056-112">參數</span><span class="sxs-lookup"><span data-stu-id="e2056-112">PARAMETERS</span></span>

### <span data-ttu-id="e2056-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2056-113">-AccountName</span></span>
<span data-ttu-id="e2056-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2056-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e2056-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2056-115">-DefaultProfile</span></span>
<span data-ttu-id="e2056-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2056-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2056-117">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="e2056-117">-Detailed</span></span>
<span data-ttu-id="e2056-118">如果提供此選項，則 Cmdlet 會傳回具有對應的輸送量值的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e2056-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="e2056-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2056-119">-InputObject</span></span>
<span data-ttu-id="e2056-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e2056-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2056-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2056-121">-Name</span></span>
<span data-ttu-id="e2056-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e2056-122">Database name.</span></span>

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

### <span data-ttu-id="e2056-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2056-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2056-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2056-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e2056-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2056-125">CommonParameters</span></span>
<span data-ttu-id="e2056-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2056-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2056-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2056-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2056-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e2056-128">INPUTS</span></span>

### <span data-ttu-id="e2056-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e2056-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e2056-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e2056-130">OUTPUTS</span></span>

### <span data-ttu-id="e2056-131">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e2056-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e2056-132">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e2056-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e2056-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e2056-133">NOTES</span></span>

## <span data-ttu-id="e2056-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2056-134">RELATED LINKS</span></span>
