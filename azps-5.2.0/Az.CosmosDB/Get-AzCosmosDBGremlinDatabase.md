---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279180"
---
# <span data-ttu-id="a29d9-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="a29d9-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="a29d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a29d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a29d9-103">取得 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a29d9-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a29d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a29d9-104">SYNTAX</span></span>

### <span data-ttu-id="a29d9-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a29d9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a29d9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a29d9-107">說明</span><span class="sxs-lookup"><span data-stu-id="a29d9-107">DESCRIPTION</span></span>
<span data-ttu-id="a29d9-108">**AzCosmosDBGremlinDatabase** Cmdlet 會取得 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a29d9-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a29d9-109">示例</span><span class="sxs-lookup"><span data-stu-id="a29d9-109">EXAMPLES</span></span>

### <span data-ttu-id="a29d9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a29d9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="a29d9-111">資源物件包含 _rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="a29d9-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="a29d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="a29d9-112">PARAMETERS</span></span>

### <span data-ttu-id="a29d9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a29d9-113">-AccountName</span></span>
<span data-ttu-id="a29d9-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a29d9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a29d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29d9-115">-DefaultProfile</span></span>
<span data-ttu-id="a29d9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a29d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a29d9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a29d9-117">-Name</span></span>
<span data-ttu-id="a29d9-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a29d9-118">Database name.</span></span>

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

### <span data-ttu-id="a29d9-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a29d9-119">-ParentObject</span></span>
<span data-ttu-id="a29d9-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a29d9-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="a29d9-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a29d9-122">Name of resource group.</span></span>

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

### <span data-ttu-id="a29d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29d9-123">CommonParameters</span></span>
<span data-ttu-id="a29d9-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a29d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29d9-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a29d9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29d9-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a29d9-126">INPUTS</span></span>

### <span data-ttu-id="a29d9-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a29d9-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a29d9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a29d9-128">OUTPUTS</span></span>

### <span data-ttu-id="a29d9-129">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="a29d9-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="a29d9-130">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="a29d9-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a29d9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a29d9-131">NOTES</span></span>

## <span data-ttu-id="a29d9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a29d9-132">RELATED LINKS</span></span>
