---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136053"
---
# <span data-ttu-id="33465-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="33465-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="33465-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33465-102">SYNOPSIS</span></span>
<span data-ttu-id="33465-103">更新 CosmosDB Sql 資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="33465-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="33465-104">句法</span><span class="sxs-lookup"><span data-stu-id="33465-104">SYNTAX</span></span>

### <span data-ttu-id="33465-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="33465-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33465-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33465-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33465-108">說明</span><span class="sxs-lookup"><span data-stu-id="33465-108">DESCRIPTION</span></span>
<span data-ttu-id="33465-109">更新 CosmosDB Sql 資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="33465-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="33465-110">示例</span><span class="sxs-lookup"><span data-stu-id="33465-110">EXAMPLES</span></span>

### <span data-ttu-id="33465-111">範例1</span><span class="sxs-lookup"><span data-stu-id="33465-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="33465-112">參數</span><span class="sxs-lookup"><span data-stu-id="33465-112">PARAMETERS</span></span>

### <span data-ttu-id="33465-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33465-113">-AccountName</span></span>
<span data-ttu-id="33465-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="33465-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="33465-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="33465-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="33465-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="33465-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="33465-117">-確認</span><span class="sxs-lookup"><span data-stu-id="33465-117">-Confirm</span></span>
<span data-ttu-id="33465-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33465-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33465-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33465-119">-DefaultProfile</span></span>
<span data-ttu-id="33465-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33465-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33465-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33465-121">-InputObject</span></span>
<span data-ttu-id="33465-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="33465-122">CosmosDB Account object</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33465-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="33465-123">-Name</span></span>
<span data-ttu-id="33465-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="33465-124">Database name.</span></span>

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

### <span data-ttu-id="33465-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="33465-125">-ParentObject</span></span>
<span data-ttu-id="33465-126">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="33465-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="33465-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33465-127">-ResourceGroupName</span></span>
<span data-ttu-id="33465-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33465-128">Name of resource group.</span></span>

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

### <span data-ttu-id="33465-129">-輸送量</span><span class="sxs-lookup"><span data-stu-id="33465-129">-Throughput</span></span>
<span data-ttu-id="33465-130">SQL database 的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="33465-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="33465-131">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="33465-131">Default value is 400.</span></span>

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

### <span data-ttu-id="33465-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33465-132">-WhatIf</span></span>
<span data-ttu-id="33465-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33465-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33465-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33465-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33465-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33465-135">CommonParameters</span></span>
<span data-ttu-id="33465-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33465-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33465-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="33465-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33465-138">輸入</span><span class="sxs-lookup"><span data-stu-id="33465-138">INPUTS</span></span>

### <span data-ttu-id="33465-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="33465-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="33465-140">輸出</span><span class="sxs-lookup"><span data-stu-id="33465-140">OUTPUTS</span></span>

### <span data-ttu-id="33465-141">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="33465-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="33465-142">筆記</span><span class="sxs-lookup"><span data-stu-id="33465-142">NOTES</span></span>

## <span data-ttu-id="33465-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="33465-143">RELATED LINKS</span></span>