---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 4fc0c28293484b2f3791145591576d4110ac2974
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911721"
---
# <span data-ttu-id="e844d-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e844d-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="e844d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e844d-102">SYNOPSIS</span></span>
<span data-ttu-id="e844d-103">請使用此功能將自動縮放輸送量遷移到手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="e844d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e844d-104">語法</span><span class="sxs-lookup"><span data-stu-id="e844d-104">SYNTAX</span></span>

### <span data-ttu-id="e844d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e844d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e844d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e844d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e844d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e844d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e844d-108">描述</span><span class="sxs-lookup"><span data-stu-id="e844d-108">DESCRIPTION</span></span>
<span data-ttu-id="e844d-109">ThroughpyteType 參數會定義要遷移到的輸送量。</span><span class="sxs-lookup"><span data-stu-id="e844d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e844d-110">例子</span><span class="sxs-lookup"><span data-stu-id="e844d-110">EXAMPLES</span></span>

### <span data-ttu-id="e844d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e844d-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="e844d-112">參數</span><span class="sxs-lookup"><span data-stu-id="e844d-112">PARAMETERS</span></span>

### <span data-ttu-id="e844d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e844d-113">-AccountName</span></span>
<span data-ttu-id="e844d-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e844d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e844d-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e844d-115">-Confirm</span></span>
<span data-ttu-id="e844d-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e844d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e844d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e844d-117">-DatabaseName</span></span>
<span data-ttu-id="e844d-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e844d-118">Database name.</span></span>

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

### <span data-ttu-id="e844d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e844d-119">-DefaultProfile</span></span>
<span data-ttu-id="e844d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e844d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e844d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e844d-121">-InputObject</span></span>
<span data-ttu-id="e844d-122">億萬繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="e844d-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e844d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e844d-123">-Name</span></span>
<span data-ttu-id="e844d-124">百分百圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="e844d-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="e844d-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e844d-125">-ParentObject</span></span>
<span data-ttu-id="e844d-126">資料表資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="e844d-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="e844d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e844d-127">-ResourceGroupName</span></span>
<span data-ttu-id="e844d-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e844d-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e844d-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e844d-129">-ThroughputType</span></span>
<span data-ttu-id="e844d-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="e844d-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="e844d-131">可能的值有：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="e844d-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e844d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e844d-132">-WhatIf</span></span>
<span data-ttu-id="e844d-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e844d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e844d-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e844d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e844d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e844d-135">CommonParameters</span></span>
<span data-ttu-id="e844d-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e844d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e844d-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e844d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e844d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e844d-138">INPUTS</span></span>

### <span data-ttu-id="e844d-139">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e844d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e844d-140">Microsoft.Azure.Commands.AzsDB.models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="e844d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="e844d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e844d-141">OUTPUTS</span></span>

### <span data-ttu-id="e844d-142">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e844d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e844d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e844d-143">NOTES</span></span>

## <span data-ttu-id="e844d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e844d-144">RELATED LINKS</span></span>
