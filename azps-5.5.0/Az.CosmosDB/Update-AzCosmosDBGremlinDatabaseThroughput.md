---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138474"
---
# <span data-ttu-id="694d7-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="694d7-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="694d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="694d7-102">SYNOPSIS</span></span>
<span data-ttu-id="694d7-103">更新 CosmosDB Gremlin 資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="694d7-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="694d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="694d7-104">SYNTAX</span></span>

### <span data-ttu-id="694d7-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="694d7-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="694d7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="694d7-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="694d7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="694d7-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="694d7-108">說明</span><span class="sxs-lookup"><span data-stu-id="694d7-108">DESCRIPTION</span></span>
<span data-ttu-id="694d7-109">更新 CosmosDB Gremlin 資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="694d7-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="694d7-110">示例</span><span class="sxs-lookup"><span data-stu-id="694d7-110">EXAMPLES</span></span>

### <span data-ttu-id="694d7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="694d7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="694d7-112">參數</span><span class="sxs-lookup"><span data-stu-id="694d7-112">PARAMETERS</span></span>

### <span data-ttu-id="694d7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="694d7-113">-AccountName</span></span>
<span data-ttu-id="694d7-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="694d7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="694d7-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="694d7-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="694d7-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="694d7-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="694d7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="694d7-117">-Confirm</span></span>
<span data-ttu-id="694d7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="694d7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="694d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694d7-119">-DefaultProfile</span></span>
<span data-ttu-id="694d7-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="694d7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="694d7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="694d7-121">-InputObject</span></span>
<span data-ttu-id="694d7-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="694d7-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="694d7-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="694d7-123">-Name</span></span>
<span data-ttu-id="694d7-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="694d7-124">Database name.</span></span>

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

### <span data-ttu-id="694d7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="694d7-125">-ParentObject</span></span>
<span data-ttu-id="694d7-126">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="694d7-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="694d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="694d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="694d7-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="694d7-128">Name of resource group.</span></span>

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

### <span data-ttu-id="694d7-129">-輸送量</span><span class="sxs-lookup"><span data-stu-id="694d7-129">-Throughput</span></span>
<span data-ttu-id="694d7-130">Gremlin 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="694d7-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="694d7-131">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="694d7-131">Default value is 400.</span></span>

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

### <span data-ttu-id="694d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694d7-132">-WhatIf</span></span>
<span data-ttu-id="694d7-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="694d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="694d7-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="694d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="694d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694d7-135">CommonParameters</span></span>
<span data-ttu-id="694d7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="694d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694d7-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="694d7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694d7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="694d7-138">INPUTS</span></span>

### <span data-ttu-id="694d7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="694d7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="694d7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="694d7-140">OUTPUTS</span></span>

### <span data-ttu-id="694d7-141">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="694d7-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="694d7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="694d7-142">NOTES</span></span>

## <span data-ttu-id="694d7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="694d7-143">RELATED LINKS</span></span>
