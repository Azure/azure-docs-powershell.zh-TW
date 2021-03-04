---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: b65443b2fc8d8b97b4b0598e0bfbb3afb9d1b925
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914149"
---
# <span data-ttu-id="76dc4-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="76dc4-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="76dc4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="76dc4-103">建立新一個管理中心Db 的一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="76dc4-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="76dc4-104">語法</span><span class="sxs-lookup"><span data-stu-id="76dc4-104">SYNTAX</span></span>

### <span data-ttu-id="76dc4-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="76dc4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76dc4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76dc4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76dc4-107">描述</span><span class="sxs-lookup"><span data-stu-id="76dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="76dc4-108">建立新一個管理中心Db 的一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="76dc4-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="76dc4-109">例子</span><span class="sxs-lookup"><span data-stu-id="76dc4-109">EXAMPLES</span></span>

### <span data-ttu-id="76dc4-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="76dc4-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="76dc4-111">參數</span><span class="sxs-lookup"><span data-stu-id="76dc4-111">PARAMETERS</span></span>

### <span data-ttu-id="76dc4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76dc4-112">-AccountName</span></span>
<span data-ttu-id="76dc4-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="76dc4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="76dc4-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="76dc4-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="76dc4-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="76dc4-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dc4-116">-確認</span><span class="sxs-lookup"><span data-stu-id="76dc4-116">-Confirm</span></span>
<span data-ttu-id="76dc4-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76dc4-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dc4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76dc4-118">-DefaultProfile</span></span>
<span data-ttu-id="76dc4-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76dc4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76dc4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="76dc4-120">-Name</span></span>
<span data-ttu-id="76dc4-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="76dc4-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dc4-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="76dc4-122">-ParentObject</span></span>
<span data-ttu-id="76dc4-123">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="76dc4-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="76dc4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76dc4-124">-ResourceGroupName</span></span>
<span data-ttu-id="76dc4-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76dc4-125">Name of resource group.</span></span>

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

### <span data-ttu-id="76dc4-126">-輸送量</span><span class="sxs-lookup"><span data-stu-id="76dc4-126">-Throughput</span></span>
<span data-ttu-id="76dc4-127">在 Ru/s (中，) 。</span><span class="sxs-lookup"><span data-stu-id="76dc4-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="76dc4-128">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="76dc4-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dc4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76dc4-129">-WhatIf</span></span>
<span data-ttu-id="76dc4-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76dc4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76dc4-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76dc4-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76dc4-132">CommonParameters</span></span>
<span data-ttu-id="76dc4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76dc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76dc4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76dc4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76dc4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="76dc4-135">INPUTS</span></span>

### <span data-ttu-id="76dc4-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="76dc4-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="76dc4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="76dc4-137">OUTPUTS</span></span>

### <span data-ttu-id="76dc4-138">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="76dc4-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="76dc4-139">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="76dc4-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="76dc4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="76dc4-140">NOTES</span></span>

## <span data-ttu-id="76dc4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="76dc4-141">RELATED LINKS</span></span>
