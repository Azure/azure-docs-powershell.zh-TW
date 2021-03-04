---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909826"
---
# <span data-ttu-id="35369-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="35369-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="35369-102">簡介</span><span class="sxs-lookup"><span data-stu-id="35369-102">SYNOPSIS</span></span>
<span data-ttu-id="35369-103">獲得 ThroughputsDB 的輸送量 。。</span><span class="sxs-lookup"><span data-stu-id="35369-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="35369-104">語法</span><span class="sxs-lookup"><span data-stu-id="35369-104">SYNTAX</span></span>

### <span data-ttu-id="35369-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="35369-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35369-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35369-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35369-107">描述</span><span class="sxs-lookup"><span data-stu-id="35369-107">DESCRIPTION</span></span>
<span data-ttu-id="35369-108">**Get-AzCosmosDBGremlinGraphThroughput** Cmdlet 會取得一個一個一次管理圖形的輸送量。</span><span class="sxs-lookup"><span data-stu-id="35369-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="35369-109">例子</span><span class="sxs-lookup"><span data-stu-id="35369-109">EXAMPLES</span></span>

### <span data-ttu-id="35369-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="35369-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="35369-111">參數</span><span class="sxs-lookup"><span data-stu-id="35369-111">PARAMETERS</span></span>

### <span data-ttu-id="35369-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="35369-112">-AccountName</span></span>
<span data-ttu-id="35369-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="35369-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="35369-114">-確認</span><span class="sxs-lookup"><span data-stu-id="35369-114">-Confirm</span></span>
<span data-ttu-id="35369-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="35369-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35369-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35369-116">-DatabaseName</span></span>
<span data-ttu-id="35369-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="35369-117">Database name.</span></span>

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

### <span data-ttu-id="35369-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35369-118">-DefaultProfile</span></span>
<span data-ttu-id="35369-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="35369-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35369-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35369-120">-InputObject</span></span>
<span data-ttu-id="35369-121">億萬繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="35369-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35369-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="35369-122">-Name</span></span>
<span data-ttu-id="35369-123">百分百圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="35369-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="35369-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35369-124">-ResourceGroupName</span></span>
<span data-ttu-id="35369-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35369-125">Name of resource group.</span></span>

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

### <span data-ttu-id="35369-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35369-126">-WhatIf</span></span>
<span data-ttu-id="35369-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35369-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35369-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35369-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35369-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35369-129">CommonParameters</span></span>
<span data-ttu-id="35369-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="35369-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35369-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35369-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35369-132">輸入</span><span class="sxs-lookup"><span data-stu-id="35369-132">INPUTS</span></span>

### <span data-ttu-id="35369-133">Microsoft.Azure.Commands.AzsDB.models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="35369-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="35369-134">輸出</span><span class="sxs-lookup"><span data-stu-id="35369-134">OUTPUTS</span></span>

### <span data-ttu-id="35369-135">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="35369-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="35369-136">筆記</span><span class="sxs-lookup"><span data-stu-id="35369-136">NOTES</span></span>

## <span data-ttu-id="35369-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="35369-137">RELATED LINKS</span></span>
