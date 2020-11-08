---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965565"
---
# <span data-ttu-id="b6024-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="b6024-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="b6024-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6024-102">SYNOPSIS</span></span>
<span data-ttu-id="b6024-103">取得 MongoDB 集合的 CosmosDB 輸送量屬性。</span><span class="sxs-lookup"><span data-stu-id="b6024-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="b6024-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6024-104">SYNTAX</span></span>

### <span data-ttu-id="b6024-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b6024-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6024-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6024-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6024-107">說明</span><span class="sxs-lookup"><span data-stu-id="b6024-107">DESCRIPTION</span></span>
<span data-ttu-id="b6024-108">**AzCosmosDBMongoDBCollectionThroughput** Cmdlet 會取得 MongoDB 集合的輸送量屬性。</span><span class="sxs-lookup"><span data-stu-id="b6024-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="b6024-109">示例</span><span class="sxs-lookup"><span data-stu-id="b6024-109">EXAMPLES</span></span>

### <span data-ttu-id="b6024-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b6024-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="b6024-111">參數</span><span class="sxs-lookup"><span data-stu-id="b6024-111">PARAMETERS</span></span>

### <span data-ttu-id="b6024-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6024-112">-AccountName</span></span>
<span data-ttu-id="b6024-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6024-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b6024-114">-確認</span><span class="sxs-lookup"><span data-stu-id="b6024-114">-Confirm</span></span>
<span data-ttu-id="b6024-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6024-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6024-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6024-116">-DatabaseName</span></span>
<span data-ttu-id="b6024-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b6024-117">Database name.</span></span>

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

### <span data-ttu-id="b6024-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6024-118">-DefaultProfile</span></span>
<span data-ttu-id="b6024-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6024-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6024-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6024-120">-InputObject</span></span>
<span data-ttu-id="b6024-121">如果提供此選項，則 Cmdlet 會傳回具有對應的輸送量值的集合。</span><span class="sxs-lookup"><span data-stu-id="b6024-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6024-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6024-122">-Name</span></span>
<span data-ttu-id="b6024-123">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="b6024-123">Collection name.</span></span>

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

### <span data-ttu-id="b6024-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6024-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6024-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6024-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b6024-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6024-126">-WhatIf</span></span>
<span data-ttu-id="b6024-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6024-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6024-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6024-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6024-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6024-129">CommonParameters</span></span>
<span data-ttu-id="b6024-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6024-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6024-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6024-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6024-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b6024-132">INPUTS</span></span>

### <span data-ttu-id="b6024-133">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b6024-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="b6024-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b6024-134">OUTPUTS</span></span>

### <span data-ttu-id="b6024-135">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b6024-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b6024-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b6024-136">NOTES</span></span>

## <span data-ttu-id="b6024-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6024-137">RELATED LINKS</span></span>