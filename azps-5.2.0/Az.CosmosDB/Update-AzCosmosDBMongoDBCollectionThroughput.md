---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275024"
---
# <span data-ttu-id="23c79-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="23c79-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="23c79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23c79-102">SYNOPSIS</span></span>
<span data-ttu-id="23c79-103">更新 CosmosDB MongoDB 集合的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="23c79-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="23c79-104">句法</span><span class="sxs-lookup"><span data-stu-id="23c79-104">SYNTAX</span></span>

### <span data-ttu-id="23c79-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="23c79-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23c79-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23c79-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23c79-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23c79-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23c79-108">說明</span><span class="sxs-lookup"><span data-stu-id="23c79-108">DESCRIPTION</span></span>
<span data-ttu-id="23c79-109">更新 CosmosDB MongoDB 集合的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="23c79-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="23c79-110">示例</span><span class="sxs-lookup"><span data-stu-id="23c79-110">EXAMPLES</span></span>

### <span data-ttu-id="23c79-111">範例1</span><span class="sxs-lookup"><span data-stu-id="23c79-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="23c79-112">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="23c79-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="23c79-113">參數</span><span class="sxs-lookup"><span data-stu-id="23c79-113">PARAMETERS</span></span>

### <span data-ttu-id="23c79-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23c79-114">-AccountName</span></span>
<span data-ttu-id="23c79-115">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="23c79-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="23c79-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="23c79-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="23c79-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="23c79-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="23c79-118">-確認</span><span class="sxs-lookup"><span data-stu-id="23c79-118">-Confirm</span></span>
<span data-ttu-id="23c79-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23c79-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23c79-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23c79-120">-DatabaseName</span></span>
<span data-ttu-id="23c79-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="23c79-121">Database name.</span></span>

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

### <span data-ttu-id="23c79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c79-122">-DefaultProfile</span></span>
<span data-ttu-id="23c79-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23c79-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c79-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23c79-124">-InputObject</span></span>
<span data-ttu-id="23c79-125">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="23c79-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="23c79-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="23c79-126">-Name</span></span>
<span data-ttu-id="23c79-127">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="23c79-127">Collection name.</span></span>

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

### <span data-ttu-id="23c79-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="23c79-128">-ParentObject</span></span>
<span data-ttu-id="23c79-129">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="23c79-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="23c79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c79-130">-ResourceGroupName</span></span>
<span data-ttu-id="23c79-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23c79-131">Name of resource group.</span></span>

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

### <span data-ttu-id="23c79-132">-輸送量</span><span class="sxs-lookup"><span data-stu-id="23c79-132">-Throughput</span></span>
<span data-ttu-id="23c79-133">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="23c79-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="23c79-134">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="23c79-134">Default value is 400.</span></span>

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

### <span data-ttu-id="23c79-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23c79-135">-WhatIf</span></span>
<span data-ttu-id="23c79-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23c79-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23c79-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23c79-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23c79-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c79-138">CommonParameters</span></span>
<span data-ttu-id="23c79-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23c79-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c79-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23c79-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c79-141">輸入</span><span class="sxs-lookup"><span data-stu-id="23c79-141">INPUTS</span></span>

### <span data-ttu-id="23c79-142">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="23c79-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="23c79-143">輸出</span><span class="sxs-lookup"><span data-stu-id="23c79-143">OUTPUTS</span></span>

### <span data-ttu-id="23c79-144">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="23c79-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="23c79-145">筆記</span><span class="sxs-lookup"><span data-stu-id="23c79-145">NOTES</span></span>

## <span data-ttu-id="23c79-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="23c79-146">RELATED LINKS</span></span>
