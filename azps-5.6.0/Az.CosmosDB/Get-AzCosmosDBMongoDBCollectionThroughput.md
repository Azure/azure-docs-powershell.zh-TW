---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 8c27df120b17805a72e7ed50497448a8f3f58461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916575"
---
# <span data-ttu-id="dd11f-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="dd11f-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="dd11f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd11f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd11f-103">獲得 MongoDB 集合的集中的集中處理量屬性。</span><span class="sxs-lookup"><span data-stu-id="dd11f-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="dd11f-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd11f-104">SYNTAX</span></span>

### <span data-ttu-id="dd11f-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dd11f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd11f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd11f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd11f-107">描述</span><span class="sxs-lookup"><span data-stu-id="dd11f-107">DESCRIPTION</span></span>
<span data-ttu-id="dd11f-108">**Get-AzCosmosDBMongoDBCollectionThroughput Cmdlet** 會取得 MongoDB 集合的輸送量屬性。</span><span class="sxs-lookup"><span data-stu-id="dd11f-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="dd11f-109">例子</span><span class="sxs-lookup"><span data-stu-id="dd11f-109">EXAMPLES</span></span>

### <span data-ttu-id="dd11f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="dd11f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="dd11f-111">參數</span><span class="sxs-lookup"><span data-stu-id="dd11f-111">PARAMETERS</span></span>

### <span data-ttu-id="dd11f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd11f-112">-AccountName</span></span>
<span data-ttu-id="dd11f-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd11f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dd11f-114">-確認</span><span class="sxs-lookup"><span data-stu-id="dd11f-114">-Confirm</span></span>
<span data-ttu-id="dd11f-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dd11f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd11f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd11f-116">-DatabaseName</span></span>
<span data-ttu-id="dd11f-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="dd11f-117">Database name.</span></span>

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

### <span data-ttu-id="dd11f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd11f-118">-DefaultProfile</span></span>
<span data-ttu-id="dd11f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd11f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd11f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd11f-120">-InputObject</span></span>
<span data-ttu-id="dd11f-121">如果提供的話，Cmdlet 會以對應的輸送量值來返回集合。</span><span class="sxs-lookup"><span data-stu-id="dd11f-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="dd11f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd11f-122">-Name</span></span>
<span data-ttu-id="dd11f-123">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="dd11f-123">Collection name.</span></span>

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

### <span data-ttu-id="dd11f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd11f-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd11f-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd11f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="dd11f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd11f-126">-WhatIf</span></span>
<span data-ttu-id="dd11f-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd11f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd11f-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd11f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd11f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd11f-129">CommonParameters</span></span>
<span data-ttu-id="dd11f-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd11f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd11f-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd11f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd11f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="dd11f-132">INPUTS</span></span>

### <span data-ttu-id="dd11f-133">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="dd11f-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="dd11f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dd11f-134">OUTPUTS</span></span>

### <span data-ttu-id="dd11f-135">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dd11f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dd11f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dd11f-136">NOTES</span></span>

## <span data-ttu-id="dd11f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd11f-137">RELATED LINKS</span></span>
