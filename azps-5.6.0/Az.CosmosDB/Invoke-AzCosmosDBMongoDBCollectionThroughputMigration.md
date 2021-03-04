---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 230fb5f43bceda32489ac632cb995eb5e4adac25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906941"
---
# <span data-ttu-id="bd461-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="bd461-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="bd461-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd461-102">SYNOPSIS</span></span>
<span data-ttu-id="bd461-103">請使用此功能將自動縮放輸送量遷移到手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="bd461-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="bd461-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd461-104">SYNTAX</span></span>

### <span data-ttu-id="bd461-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd461-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd461-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd461-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd461-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd461-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd461-108">描述</span><span class="sxs-lookup"><span data-stu-id="bd461-108">DESCRIPTION</span></span>
<span data-ttu-id="bd461-109">ThroughpyteType 參數會定義要遷移到的輸送量。</span><span class="sxs-lookup"><span data-stu-id="bd461-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="bd461-110">例子</span><span class="sxs-lookup"><span data-stu-id="bd461-110">EXAMPLES</span></span>

### <span data-ttu-id="bd461-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bd461-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="bd461-112">參數</span><span class="sxs-lookup"><span data-stu-id="bd461-112">PARAMETERS</span></span>

### <span data-ttu-id="bd461-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd461-113">-AccountName</span></span>
<span data-ttu-id="bd461-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd461-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bd461-115">-確認</span><span class="sxs-lookup"><span data-stu-id="bd461-115">-Confirm</span></span>
<span data-ttu-id="bd461-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bd461-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd461-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd461-117">-DatabaseName</span></span>
<span data-ttu-id="bd461-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="bd461-118">Database name.</span></span>

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

### <span data-ttu-id="bd461-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd461-119">-DefaultProfile</span></span>
<span data-ttu-id="bd461-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd461-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd461-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd461-121">-InputObject</span></span>
<span data-ttu-id="bd461-122">Mongo Collection 物件。</span><span class="sxs-lookup"><span data-stu-id="bd461-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd461-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd461-123">-Name</span></span>
<span data-ttu-id="bd461-124">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="bd461-124">Collection name.</span></span>

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

### <span data-ttu-id="bd461-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd461-125">-ParentObject</span></span>
<span data-ttu-id="bd461-126">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="bd461-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="bd461-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd461-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd461-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd461-128">Name of resource group.</span></span>

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

### <span data-ttu-id="bd461-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="bd461-129">-ThroughputType</span></span>
<span data-ttu-id="bd461-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="bd461-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="bd461-131">可能的值有：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="bd461-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="bd461-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd461-132">-WhatIf</span></span>
<span data-ttu-id="bd461-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd461-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd461-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd461-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd461-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd461-135">CommonParameters</span></span>
<span data-ttu-id="bd461-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd461-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd461-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd461-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd461-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bd461-138">INPUTS</span></span>

### <span data-ttu-id="bd461-139">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bd461-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="bd461-140">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="bd461-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="bd461-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bd461-141">OUTPUTS</span></span>

### <span data-ttu-id="bd461-142">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bd461-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bd461-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bd461-143">NOTES</span></span>

## <span data-ttu-id="bd461-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd461-144">RELATED LINKS</span></span>
