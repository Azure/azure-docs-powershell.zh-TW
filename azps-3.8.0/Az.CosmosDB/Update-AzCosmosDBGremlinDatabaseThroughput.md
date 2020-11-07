---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 75ea7849424d8587f4eb4151bde63f31ea35676f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799278"
---
# <span data-ttu-id="98d97-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="98d97-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="98d97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98d97-102">SYNOPSIS</span></span>
<span data-ttu-id="98d97-103">更新 CosmosDB Gremlin 資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="98d97-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="98d97-104">句法</span><span class="sxs-lookup"><span data-stu-id="98d97-104">SYNTAX</span></span>

### <span data-ttu-id="98d97-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="98d97-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98d97-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98d97-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98d97-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98d97-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98d97-108">示例</span><span class="sxs-lookup"><span data-stu-id="98d97-108">EXAMPLES</span></span>

### <span data-ttu-id="98d97-109">範例1</span><span class="sxs-lookup"><span data-stu-id="98d97-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="98d97-110">參數</span><span class="sxs-lookup"><span data-stu-id="98d97-110">PARAMETERS</span></span>

### <span data-ttu-id="98d97-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98d97-111">-AccountName</span></span>
<span data-ttu-id="98d97-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="98d97-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="98d97-113">-確認</span><span class="sxs-lookup"><span data-stu-id="98d97-113">-Confirm</span></span>
<span data-ttu-id="98d97-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98d97-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d97-115">-DefaultProfile</span></span>
<span data-ttu-id="98d97-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98d97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98d97-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98d97-117">-InputObject</span></span>
<span data-ttu-id="98d97-118">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="98d97-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="98d97-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="98d97-119">-Name</span></span>
<span data-ttu-id="98d97-120">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="98d97-120">Database name.</span></span>

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

### <span data-ttu-id="98d97-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="98d97-121">-ParentObject</span></span>
<span data-ttu-id="98d97-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="98d97-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98d97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d97-123">-ResourceGroupName</span></span>
<span data-ttu-id="98d97-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98d97-124">Name of resource group.</span></span>

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

### <span data-ttu-id="98d97-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="98d97-125">-Throughput</span></span>
<span data-ttu-id="98d97-126">Gremlin 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="98d97-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="98d97-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="98d97-127">Default value is 400.</span></span>

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

### <span data-ttu-id="98d97-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d97-128">-WhatIf</span></span>
<span data-ttu-id="98d97-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98d97-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98d97-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98d97-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d97-131">CommonParameters</span></span>
<span data-ttu-id="98d97-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98d97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d97-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98d97-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d97-134">輸入</span><span class="sxs-lookup"><span data-stu-id="98d97-134">INPUTS</span></span>

### <span data-ttu-id="98d97-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="98d97-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="98d97-136">輸出</span><span class="sxs-lookup"><span data-stu-id="98d97-136">OUTPUTS</span></span>

### <span data-ttu-id="98d97-137">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="98d97-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="98d97-138">筆記</span><span class="sxs-lookup"><span data-stu-id="98d97-138">NOTES</span></span>

## <span data-ttu-id="98d97-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="98d97-139">RELATED LINKS</span></span>
