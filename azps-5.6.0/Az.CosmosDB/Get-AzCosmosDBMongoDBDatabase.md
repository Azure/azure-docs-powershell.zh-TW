---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912901"
---
# <span data-ttu-id="9c139-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="9c139-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="9c139-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c139-102">SYNOPSIS</span></span>
<span data-ttu-id="9c139-103">獲得代斯DB MongoDB 資料庫</span><span class="sxs-lookup"><span data-stu-id="9c139-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="9c139-104">語法</span><span class="sxs-lookup"><span data-stu-id="9c139-104">SYNTAX</span></span>

### <span data-ttu-id="9c139-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9c139-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c139-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c139-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c139-107">描述</span><span class="sxs-lookup"><span data-stu-id="9c139-107">DESCRIPTION</span></span>
<span data-ttu-id="9c139-108">**Get-AzCosmosDBMongoDBDatabase** Cmdlet 會取得一個OsosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="9c139-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="9c139-109">例子</span><span class="sxs-lookup"><span data-stu-id="9c139-109">EXAMPLES</span></span>

### <span data-ttu-id="9c139-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="9c139-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="9c139-111">資源物件包含_rid、_ts、_etag屬性。</span><span class="sxs-lookup"><span data-stu-id="9c139-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="9c139-112">參數</span><span class="sxs-lookup"><span data-stu-id="9c139-112">PARAMETERS</span></span>

### <span data-ttu-id="9c139-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c139-113">-AccountName</span></span>
<span data-ttu-id="9c139-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c139-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9c139-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c139-115">-DefaultProfile</span></span>
<span data-ttu-id="9c139-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c139-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c139-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c139-117">-Name</span></span>
<span data-ttu-id="9c139-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9c139-118">Database name.</span></span>

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

### <span data-ttu-id="9c139-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9c139-119">-ParentObject</span></span>
<span data-ttu-id="9c139-120">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9c139-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c139-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c139-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c139-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c139-122">Name of resource group.</span></span>

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

### <span data-ttu-id="9c139-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c139-123">CommonParameters</span></span>
<span data-ttu-id="9c139-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c139-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c139-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c139-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c139-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9c139-126">INPUTS</span></span>

### <span data-ttu-id="9c139-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9c139-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9c139-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9c139-128">OUTPUTS</span></span>

### <span data-ttu-id="9c139-129">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9c139-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="9c139-130">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9c139-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9c139-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9c139-131">NOTES</span></span>

## <span data-ttu-id="9c139-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c139-132">RELATED LINKS</span></span>
