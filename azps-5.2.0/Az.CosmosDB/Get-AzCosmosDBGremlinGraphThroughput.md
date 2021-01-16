---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276127"
---
# <span data-ttu-id="3be4f-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="3be4f-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="3be4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3be4f-102">SYNOPSIS</span></span>
<span data-ttu-id="3be4f-103">取得 CosmosDB Gremlin 圖形的輸送量。</span><span class="sxs-lookup"><span data-stu-id="3be4f-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="3be4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3be4f-104">SYNTAX</span></span>

### <span data-ttu-id="3be4f-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3be4f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be4f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3be4f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be4f-107">說明</span><span class="sxs-lookup"><span data-stu-id="3be4f-107">DESCRIPTION</span></span>
<span data-ttu-id="3be4f-108">**AzCosmosDBGremlinGraphThroughput** Cmdlet 會取得 CosmosDB Gremlin 圖形的輸送量。</span><span class="sxs-lookup"><span data-stu-id="3be4f-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="3be4f-109">示例</span><span class="sxs-lookup"><span data-stu-id="3be4f-109">EXAMPLES</span></span>

### <span data-ttu-id="3be4f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3be4f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="3be4f-111">參數</span><span class="sxs-lookup"><span data-stu-id="3be4f-111">PARAMETERS</span></span>

### <span data-ttu-id="3be4f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3be4f-112">-AccountName</span></span>
<span data-ttu-id="3be4f-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3be4f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3be4f-114">-確認</span><span class="sxs-lookup"><span data-stu-id="3be4f-114">-Confirm</span></span>
<span data-ttu-id="3be4f-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3be4f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be4f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3be4f-116">-DatabaseName</span></span>
<span data-ttu-id="3be4f-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3be4f-117">Database name.</span></span>

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

### <span data-ttu-id="3be4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be4f-118">-DefaultProfile</span></span>
<span data-ttu-id="3be4f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3be4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3be4f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3be4f-120">-InputObject</span></span>
<span data-ttu-id="3be4f-121">Gremlin Graph 物件。</span><span class="sxs-lookup"><span data-stu-id="3be4f-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="3be4f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3be4f-122">-Name</span></span>
<span data-ttu-id="3be4f-123">Gremlin 圖名稱。</span><span class="sxs-lookup"><span data-stu-id="3be4f-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="3be4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3be4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3be4f-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3be4f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3be4f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be4f-126">-WhatIf</span></span>
<span data-ttu-id="3be4f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3be4f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be4f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3be4f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be4f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be4f-129">CommonParameters</span></span>
<span data-ttu-id="3be4f-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3be4f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be4f-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3be4f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be4f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3be4f-132">INPUTS</span></span>

### <span data-ttu-id="3be4f-133">PSGremlinGraphGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3be4f-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="3be4f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3be4f-134">OUTPUTS</span></span>

### <span data-ttu-id="3be4f-135">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3be4f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3be4f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3be4f-136">NOTES</span></span>

## <span data-ttu-id="3be4f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3be4f-137">RELATED LINKS</span></span>
