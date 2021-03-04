---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 21dd30bd60e9b26fc306ed99b31cd3c52d9fdf8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908258"
---
# <span data-ttu-id="16c5e-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="16c5e-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="16c5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="16c5e-103">更新一個更新了一個一流資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="16c5e-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="16c5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="16c5e-104">SYNTAX</span></span>

### <span data-ttu-id="16c5e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="16c5e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c5e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16c5e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c5e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16c5e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c5e-108">描述</span><span class="sxs-lookup"><span data-stu-id="16c5e-108">DESCRIPTION</span></span>
<span data-ttu-id="16c5e-109">更新一個更新了一個一流資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="16c5e-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="16c5e-110">例子</span><span class="sxs-lookup"><span data-stu-id="16c5e-110">EXAMPLES</span></span>

### <span data-ttu-id="16c5e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="16c5e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="16c5e-112">參數</span><span class="sxs-lookup"><span data-stu-id="16c5e-112">PARAMETERS</span></span>

### <span data-ttu-id="16c5e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16c5e-113">-AccountName</span></span>
<span data-ttu-id="16c5e-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="16c5e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="16c5e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="16c5e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="16c5e-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="16c5e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="16c5e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="16c5e-117">-Confirm</span></span>
<span data-ttu-id="16c5e-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="16c5e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c5e-119">-DefaultProfile</span></span>
<span data-ttu-id="16c5e-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16c5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c5e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c5e-121">-InputObject</span></span>
<span data-ttu-id="16c5e-122">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="16c5e-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="16c5e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="16c5e-123">-Name</span></span>
<span data-ttu-id="16c5e-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="16c5e-124">Database name.</span></span>

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

### <span data-ttu-id="16c5e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="16c5e-125">-ParentObject</span></span>
<span data-ttu-id="16c5e-126">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="16c5e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="16c5e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c5e-127">-ResourceGroupName</span></span>
<span data-ttu-id="16c5e-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16c5e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="16c5e-129">-輸送量</span><span class="sxs-lookup"><span data-stu-id="16c5e-129">-Throughput</span></span>
<span data-ttu-id="16c5e-130">在 Ru/s (中，) 。</span><span class="sxs-lookup"><span data-stu-id="16c5e-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="16c5e-131">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="16c5e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="16c5e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c5e-132">-WhatIf</span></span>
<span data-ttu-id="16c5e-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16c5e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c5e-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16c5e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c5e-135">CommonParameters</span></span>
<span data-ttu-id="16c5e-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16c5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c5e-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16c5e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c5e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="16c5e-138">INPUTS</span></span>

### <span data-ttu-id="16c5e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="16c5e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="16c5e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="16c5e-140">OUTPUTS</span></span>

### <span data-ttu-id="16c5e-141">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="16c5e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="16c5e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="16c5e-142">NOTES</span></span>

## <span data-ttu-id="16c5e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="16c5e-143">RELATED LINKS</span></span>
