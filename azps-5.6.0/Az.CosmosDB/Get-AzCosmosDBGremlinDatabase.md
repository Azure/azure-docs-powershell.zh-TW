---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 7268eff2163e408975b1711dcac4fbf8454f0b76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915546"
---
# <span data-ttu-id="918cb-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="918cb-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="918cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="918cb-102">SYNOPSIS</span></span>
<span data-ttu-id="918cb-103">獲得一個一文不值的資料庫。</span><span class="sxs-lookup"><span data-stu-id="918cb-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="918cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="918cb-104">SYNTAX</span></span>

### <span data-ttu-id="918cb-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="918cb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="918cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="918cb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="918cb-107">描述</span><span class="sxs-lookup"><span data-stu-id="918cb-107">DESCRIPTION</span></span>
<span data-ttu-id="918cb-108">**Get-AzCosmosDBGremlinDatabase** Cmdlet 會取得一個OsosDB 的維琪百科資料庫。</span><span class="sxs-lookup"><span data-stu-id="918cb-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="918cb-109">例子</span><span class="sxs-lookup"><span data-stu-id="918cb-109">EXAMPLES</span></span>

### <span data-ttu-id="918cb-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="918cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="918cb-111">資源物件包含_rid、_ts、_etag。</span><span class="sxs-lookup"><span data-stu-id="918cb-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="918cb-112">參數</span><span class="sxs-lookup"><span data-stu-id="918cb-112">PARAMETERS</span></span>

### <span data-ttu-id="918cb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="918cb-113">-AccountName</span></span>
<span data-ttu-id="918cb-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="918cb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="918cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918cb-115">-DefaultProfile</span></span>
<span data-ttu-id="918cb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="918cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="918cb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="918cb-117">-Name</span></span>
<span data-ttu-id="918cb-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="918cb-118">Database name.</span></span>

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

### <span data-ttu-id="918cb-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="918cb-119">-ParentObject</span></span>
<span data-ttu-id="918cb-120">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="918cb-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="918cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="918cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="918cb-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="918cb-122">Name of resource group.</span></span>

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

### <span data-ttu-id="918cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918cb-123">CommonParameters</span></span>
<span data-ttu-id="918cb-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="918cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918cb-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="918cb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918cb-126">輸入</span><span class="sxs-lookup"><span data-stu-id="918cb-126">INPUTS</span></span>

### <span data-ttu-id="918cb-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="918cb-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="918cb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="918cb-128">OUTPUTS</span></span>

### <span data-ttu-id="918cb-129">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="918cb-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="918cb-130">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="918cb-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="918cb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="918cb-131">NOTES</span></span>

## <span data-ttu-id="918cb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="918cb-132">RELATED LINKS</span></span>
