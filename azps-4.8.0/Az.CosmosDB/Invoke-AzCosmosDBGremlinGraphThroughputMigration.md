---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136537"
---
# <span data-ttu-id="e30c1-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e30c1-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="e30c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e30c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e30c1-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="e30c1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e30c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e30c1-104">SYNTAX</span></span>

### <span data-ttu-id="e30c1-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e30c1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e30c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e30c1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e30c1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e30c1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30c1-108">說明</span><span class="sxs-lookup"><span data-stu-id="e30c1-108">DESCRIPTION</span></span>
<span data-ttu-id="e30c1-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="e30c1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e30c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="e30c1-110">EXAMPLES</span></span>

### <span data-ttu-id="e30c1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e30c1-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="e30c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="e30c1-112">PARAMETERS</span></span>

### <span data-ttu-id="e30c1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e30c1-113">-AccountName</span></span>
<span data-ttu-id="e30c1-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e30c1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e30c1-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e30c1-115">-Confirm</span></span>
<span data-ttu-id="e30c1-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e30c1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e30c1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e30c1-117">-DatabaseName</span></span>
<span data-ttu-id="e30c1-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e30c1-118">Database name.</span></span>

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

### <span data-ttu-id="e30c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30c1-119">-DefaultProfile</span></span>
<span data-ttu-id="e30c1-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e30c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e30c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e30c1-121">-InputObject</span></span>
<span data-ttu-id="e30c1-122">Gremlin Graph 物件。</span><span class="sxs-lookup"><span data-stu-id="e30c1-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="e30c1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e30c1-123">-Name</span></span>
<span data-ttu-id="e30c1-124">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="e30c1-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="e30c1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e30c1-125">-ParentObject</span></span>
<span data-ttu-id="e30c1-126">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="e30c1-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="e30c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e30c1-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e30c1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e30c1-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e30c1-129">-ThroughputType</span></span>
<span data-ttu-id="e30c1-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="e30c1-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="e30c1-131">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="e30c1-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e30c1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30c1-132">-WhatIf</span></span>
<span data-ttu-id="e30c1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e30c1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e30c1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e30c1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e30c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30c1-135">CommonParameters</span></span>
<span data-ttu-id="e30c1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e30c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30c1-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e30c1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30c1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e30c1-138">INPUTS</span></span>

### <span data-ttu-id="e30c1-139">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e30c1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e30c1-140">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e30c1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="e30c1-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e30c1-141">OUTPUTS</span></span>

### <span data-ttu-id="e30c1-142">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e30c1-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e30c1-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e30c1-143">NOTES</span></span>

## <span data-ttu-id="e30c1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e30c1-144">RELATED LINKS</span></span>