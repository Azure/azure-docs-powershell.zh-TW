---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285419"
---
# <span data-ttu-id="7cb74-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="7cb74-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="7cb74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cb74-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb74-103">更新 CosmosDB Gremlin 圖形的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="7cb74-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="7cb74-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cb74-104">SYNTAX</span></span>

### <span data-ttu-id="7cb74-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7cb74-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb74-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb74-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb74-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb74-108">說明</span><span class="sxs-lookup"><span data-stu-id="7cb74-108">DESCRIPTION</span></span>
<span data-ttu-id="7cb74-109">更新 CosmosDB Gremlin 圖形的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="7cb74-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="7cb74-110">示例</span><span class="sxs-lookup"><span data-stu-id="7cb74-110">EXAMPLES</span></span>

### <span data-ttu-id="7cb74-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7cb74-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="7cb74-112">參數</span><span class="sxs-lookup"><span data-stu-id="7cb74-112">PARAMETERS</span></span>

### <span data-ttu-id="7cb74-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7cb74-113">-AccountName</span></span>
<span data-ttu-id="7cb74-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb74-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7cb74-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7cb74-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7cb74-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="7cb74-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7cb74-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7cb74-117">-Confirm</span></span>
<span data-ttu-id="7cb74-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7cb74-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb74-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7cb74-119">-DatabaseName</span></span>
<span data-ttu-id="7cb74-120">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb74-120">Database name.</span></span>

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

### <span data-ttu-id="7cb74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb74-121">-DefaultProfile</span></span>
<span data-ttu-id="7cb74-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cb74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb74-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb74-123">-InputObject</span></span>
<span data-ttu-id="7cb74-124">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="7cb74-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="7cb74-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7cb74-125">-Name</span></span>
<span data-ttu-id="7cb74-126">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb74-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="7cb74-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7cb74-127">-ParentObject</span></span>
<span data-ttu-id="7cb74-128">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="7cb74-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="7cb74-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb74-129">-ResourceGroupName</span></span>
<span data-ttu-id="7cb74-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb74-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7cb74-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="7cb74-131">-Throughput</span></span>
<span data-ttu-id="7cb74-132">Gremlin 圖的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="7cb74-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="7cb74-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="7cb74-133">Default value is 400.</span></span>

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

### <span data-ttu-id="7cb74-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb74-134">-WhatIf</span></span>
<span data-ttu-id="7cb74-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cb74-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb74-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cb74-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb74-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb74-137">CommonParameters</span></span>
<span data-ttu-id="7cb74-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cb74-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb74-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7cb74-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb74-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7cb74-140">INPUTS</span></span>

### <span data-ttu-id="7cb74-141">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7cb74-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="7cb74-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7cb74-142">OUTPUTS</span></span>

### <span data-ttu-id="7cb74-143">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7cb74-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7cb74-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7cb74-144">NOTES</span></span>

## <span data-ttu-id="7cb74-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cb74-145">RELATED LINKS</span></span>
