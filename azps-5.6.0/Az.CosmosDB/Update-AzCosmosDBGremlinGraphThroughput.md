---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: c5d7bc79185639c4ec79ab14d7ed2f6201dcedb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908253"
---
# <span data-ttu-id="5c9d3-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="5c9d3-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="5c9d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9d3-103">更新一個一格的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5c9d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c9d3-104">SYNTAX</span></span>

### <span data-ttu-id="5c9d3-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5c9d3-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c9d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9d3-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c9d3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9d3-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c9d3-108">描述</span><span class="sxs-lookup"><span data-stu-id="5c9d3-108">DESCRIPTION</span></span>
<span data-ttu-id="5c9d3-109">更新一個一格的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5c9d3-110">例子</span><span class="sxs-lookup"><span data-stu-id="5c9d3-110">EXAMPLES</span></span>

### <span data-ttu-id="5c9d3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5c9d3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="5c9d3-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c9d3-112">PARAMETERS</span></span>

### <span data-ttu-id="5c9d3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c9d3-113">-AccountName</span></span>
<span data-ttu-id="5c9d3-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5c9d3-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5c9d3-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5c9d3-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5c9d3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="5c9d3-117">-Confirm</span></span>
<span data-ttu-id="5c9d3-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c9d3-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c9d3-119">-DatabaseName</span></span>
<span data-ttu-id="5c9d3-120">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-120">Database name.</span></span>

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

### <span data-ttu-id="5c9d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9d3-121">-DefaultProfile</span></span>
<span data-ttu-id="5c9d3-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c9d3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c9d3-123">-InputObject</span></span>
<span data-ttu-id="5c9d3-124">資料表資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5c9d3-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c9d3-125">-Name</span></span>
<span data-ttu-id="5c9d3-126">百分百圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5c9d3-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5c9d3-127">-ParentObject</span></span>
<span data-ttu-id="5c9d3-128">資料表資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5c9d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="5c9d3-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5c9d3-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="5c9d3-131">-Throughput</span></span>
<span data-ttu-id="5c9d3-132">在 Ru/s (中，) 。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="5c9d3-133">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-133">Default value is 400.</span></span>

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

### <span data-ttu-id="5c9d3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c9d3-134">-WhatIf</span></span>
<span data-ttu-id="5c9d3-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c9d3-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c9d3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9d3-137">CommonParameters</span></span>
<span data-ttu-id="5c9d3-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c9d3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9d3-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c9d3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9d3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5c9d3-140">INPUTS</span></span>

### <span data-ttu-id="5c9d3-141">Microsoft.Azure.Commands.AzsDB.models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5c9d3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5c9d3-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5c9d3-142">OUTPUTS</span></span>

### <span data-ttu-id="5c9d3-143">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5c9d3-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5c9d3-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5c9d3-144">NOTES</span></span>

## <span data-ttu-id="5c9d3-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c9d3-145">RELATED LINKS</span></span>
