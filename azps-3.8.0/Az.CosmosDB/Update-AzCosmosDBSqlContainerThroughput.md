---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958127"
---
# <span data-ttu-id="99249-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="99249-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="99249-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99249-102">SYNOPSIS</span></span>
<span data-ttu-id="99249-103">更新 CosmosDB Sql 容器的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="99249-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="99249-104">句法</span><span class="sxs-lookup"><span data-stu-id="99249-104">SYNTAX</span></span>

### <span data-ttu-id="99249-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="99249-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99249-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99249-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99249-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99249-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99249-108">示例</span><span class="sxs-lookup"><span data-stu-id="99249-108">EXAMPLES</span></span>

### <span data-ttu-id="99249-109">範例1</span><span class="sxs-lookup"><span data-stu-id="99249-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="99249-110">參數</span><span class="sxs-lookup"><span data-stu-id="99249-110">PARAMETERS</span></span>

### <span data-ttu-id="99249-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="99249-111">-AccountName</span></span>
<span data-ttu-id="99249-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="99249-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99249-113">-確認</span><span class="sxs-lookup"><span data-stu-id="99249-113">-Confirm</span></span>
<span data-ttu-id="99249-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99249-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99249-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99249-115">-DatabaseName</span></span>
<span data-ttu-id="99249-116">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="99249-116">Database name.</span></span>

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

### <span data-ttu-id="99249-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99249-117">-DefaultProfile</span></span>
<span data-ttu-id="99249-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99249-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99249-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99249-119">-InputObject</span></span>
<span data-ttu-id="99249-120">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="99249-120">Sql Database object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99249-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="99249-121">-Name</span></span>
<span data-ttu-id="99249-122">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="99249-122">Container name.</span></span>

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

### <span data-ttu-id="99249-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="99249-123">-ParentObject</span></span>
<span data-ttu-id="99249-124">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="99249-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99249-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99249-125">-ResourceGroupName</span></span>
<span data-ttu-id="99249-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99249-126">Name of resource group.</span></span>

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

### <span data-ttu-id="99249-127">-輸送量</span><span class="sxs-lookup"><span data-stu-id="99249-127">-Throughput</span></span>
<span data-ttu-id="99249-128">SQL 容器的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="99249-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="99249-129">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="99249-129">Default value is 400.</span></span>

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

### <span data-ttu-id="99249-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99249-130">-WhatIf</span></span>
<span data-ttu-id="99249-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99249-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99249-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99249-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99249-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99249-133">CommonParameters</span></span>
<span data-ttu-id="99249-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99249-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99249-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="99249-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99249-136">輸入</span><span class="sxs-lookup"><span data-stu-id="99249-136">INPUTS</span></span>

### <span data-ttu-id="99249-137">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="99249-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="99249-138">輸出</span><span class="sxs-lookup"><span data-stu-id="99249-138">OUTPUTS</span></span>

### <span data-ttu-id="99249-139">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="99249-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="99249-140">筆記</span><span class="sxs-lookup"><span data-stu-id="99249-140">NOTES</span></span>

## <span data-ttu-id="99249-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="99249-141">RELATED LINKS</span></span>
