---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 66ca19099d4562da3add57411a16be1a0573ea02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908246"
---
# <span data-ttu-id="7b2e7-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="7b2e7-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="7b2e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2e7-103">更新一個集中的一個管理資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7b2e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b2e7-104">SYNTAX</span></span>

### <span data-ttu-id="7b2e7-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7b2e7-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b2e7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b2e7-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b2e7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b2e7-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b2e7-108">描述</span><span class="sxs-lookup"><span data-stu-id="7b2e7-108">DESCRIPTION</span></span>
<span data-ttu-id="7b2e7-109">更新一個集中的一個管理資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7b2e7-110">例子</span><span class="sxs-lookup"><span data-stu-id="7b2e7-110">EXAMPLES</span></span>

### <span data-ttu-id="7b2e7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7b2e7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="7b2e7-112">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="7b2e7-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="7b2e7-113">參數</span><span class="sxs-lookup"><span data-stu-id="7b2e7-113">PARAMETERS</span></span>

### <span data-ttu-id="7b2e7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7b2e7-114">-AccountName</span></span>
<span data-ttu-id="7b2e7-115">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7b2e7-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7b2e7-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7b2e7-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7b2e7-118">-確認</span><span class="sxs-lookup"><span data-stu-id="7b2e7-118">-Confirm</span></span>
<span data-ttu-id="7b2e7-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b2e7-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7b2e7-120">-DatabaseName</span></span>
<span data-ttu-id="7b2e7-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-121">Database name.</span></span>

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

### <span data-ttu-id="7b2e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2e7-122">-DefaultProfile</span></span>
<span data-ttu-id="7b2e7-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b2e7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b2e7-124">-InputObject</span></span>
<span data-ttu-id="7b2e7-125">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="7b2e7-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b2e7-126">-Name</span></span>
<span data-ttu-id="7b2e7-127">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-127">Collection name.</span></span>

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

### <span data-ttu-id="7b2e7-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7b2e7-128">-ParentObject</span></span>
<span data-ttu-id="7b2e7-129">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="7b2e7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2e7-130">-ResourceGroupName</span></span>
<span data-ttu-id="7b2e7-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-131">Name of resource group.</span></span>

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

### <span data-ttu-id="7b2e7-132">-輸送量</span><span class="sxs-lookup"><span data-stu-id="7b2e7-132">-Throughput</span></span>
<span data-ttu-id="7b2e7-133">SQL 容器的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7b2e7-134">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-134">Default value is 400.</span></span>

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

### <span data-ttu-id="7b2e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b2e7-135">-WhatIf</span></span>
<span data-ttu-id="7b2e7-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b2e7-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b2e7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2e7-138">CommonParameters</span></span>
<span data-ttu-id="7b2e7-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b2e7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2e7-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b2e7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2e7-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7b2e7-141">INPUTS</span></span>

### <span data-ttu-id="7b2e7-142">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7b2e7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7b2e7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7b2e7-143">OUTPUTS</span></span>

### <span data-ttu-id="7b2e7-144">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7b2e7-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7b2e7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7b2e7-145">NOTES</span></span>

## <span data-ttu-id="7b2e7-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b2e7-146">RELATED LINKS</span></span>
