---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958125"
---
# <span data-ttu-id="79d91-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="79d91-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="79d91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79d91-102">SYNOPSIS</span></span>
<span data-ttu-id="79d91-103">更新 CosmosDB Gremlin 圖形的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="79d91-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="79d91-104">句法</span><span class="sxs-lookup"><span data-stu-id="79d91-104">SYNTAX</span></span>

### <span data-ttu-id="79d91-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79d91-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79d91-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79d91-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79d91-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79d91-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79d91-108">示例</span><span class="sxs-lookup"><span data-stu-id="79d91-108">EXAMPLES</span></span>

### <span data-ttu-id="79d91-109">範例1</span><span class="sxs-lookup"><span data-stu-id="79d91-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="79d91-110">參數</span><span class="sxs-lookup"><span data-stu-id="79d91-110">PARAMETERS</span></span>

### <span data-ttu-id="79d91-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79d91-111">-AccountName</span></span>
<span data-ttu-id="79d91-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="79d91-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79d91-113">-確認</span><span class="sxs-lookup"><span data-stu-id="79d91-113">-Confirm</span></span>
<span data-ttu-id="79d91-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79d91-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79d91-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79d91-115">-DatabaseName</span></span>
<span data-ttu-id="79d91-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="79d91-116">Database name.</span></span>

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

### <span data-ttu-id="79d91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d91-117">-DefaultProfile</span></span>
<span data-ttu-id="79d91-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79d91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79d91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79d91-119">-InputObject</span></span>
<span data-ttu-id="79d91-120">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="79d91-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="79d91-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="79d91-121">-Name</span></span>
<span data-ttu-id="79d91-122">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="79d91-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="79d91-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79d91-123">-ParentObject</span></span>
<span data-ttu-id="79d91-124">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="79d91-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="79d91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d91-125">-ResourceGroupName</span></span>
<span data-ttu-id="79d91-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79d91-126">Name of resource group.</span></span>

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

### <span data-ttu-id="79d91-127">-輸送量</span><span class="sxs-lookup"><span data-stu-id="79d91-127">-Throughput</span></span>
<span data-ttu-id="79d91-128">Gremlin 圖的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="79d91-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="79d91-129">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="79d91-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d91-130">-WhatIf</span></span>
<span data-ttu-id="79d91-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79d91-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79d91-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79d91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79d91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d91-133">CommonParameters</span></span>
<span data-ttu-id="79d91-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79d91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d91-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79d91-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d91-136">輸入</span><span class="sxs-lookup"><span data-stu-id="79d91-136">INPUTS</span></span>

### <span data-ttu-id="79d91-137">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="79d91-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="79d91-138">輸出</span><span class="sxs-lookup"><span data-stu-id="79d91-138">OUTPUTS</span></span>

### <span data-ttu-id="79d91-139">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="79d91-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79d91-140">筆記</span><span class="sxs-lookup"><span data-stu-id="79d91-140">NOTES</span></span>

## <span data-ttu-id="79d91-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="79d91-141">RELATED LINKS</span></span>
