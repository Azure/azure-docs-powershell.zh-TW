---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: b4afffee9f5eced29968b136ec1dc9a07250ab8d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958123"
---
# <span data-ttu-id="11e28-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="11e28-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="11e28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11e28-102">SYNOPSIS</span></span>
<span data-ttu-id="11e28-103">更新 CosmosDB Sql 資料庫的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="11e28-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="11e28-104">句法</span><span class="sxs-lookup"><span data-stu-id="11e28-104">SYNTAX</span></span>

### <span data-ttu-id="11e28-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11e28-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e28-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e28-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e28-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e28-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11e28-108">示例</span><span class="sxs-lookup"><span data-stu-id="11e28-108">EXAMPLES</span></span>

### <span data-ttu-id="11e28-109">範例1</span><span class="sxs-lookup"><span data-stu-id="11e28-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="11e28-110">參數</span><span class="sxs-lookup"><span data-stu-id="11e28-110">PARAMETERS</span></span>

### <span data-ttu-id="11e28-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11e28-111">-AccountName</span></span>
<span data-ttu-id="11e28-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e28-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11e28-113">-確認</span><span class="sxs-lookup"><span data-stu-id="11e28-113">-Confirm</span></span>
<span data-ttu-id="11e28-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11e28-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e28-115">-DefaultProfile</span></span>
<span data-ttu-id="11e28-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11e28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e28-117">-InputObject</span></span>
<span data-ttu-id="11e28-118">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="11e28-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="11e28-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="11e28-119">-Name</span></span>
<span data-ttu-id="11e28-120">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="11e28-120">Database name.</span></span>

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

### <span data-ttu-id="11e28-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="11e28-121">-ParentObject</span></span>
<span data-ttu-id="11e28-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="11e28-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="11e28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e28-123">-ResourceGroupName</span></span>
<span data-ttu-id="11e28-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e28-124">Name of resource group.</span></span>

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

### <span data-ttu-id="11e28-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="11e28-125">-Throughput</span></span>
<span data-ttu-id="11e28-126">SQL database 的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e28-126">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="11e28-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="11e28-127">Default value is 400.</span></span>

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

### <span data-ttu-id="11e28-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e28-128">-WhatIf</span></span>
<span data-ttu-id="11e28-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11e28-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e28-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11e28-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e28-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e28-131">CommonParameters</span></span>
<span data-ttu-id="11e28-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11e28-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e28-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11e28-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e28-134">輸入</span><span class="sxs-lookup"><span data-stu-id="11e28-134">INPUTS</span></span>

### <span data-ttu-id="11e28-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="11e28-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="11e28-136">輸出</span><span class="sxs-lookup"><span data-stu-id="11e28-136">OUTPUTS</span></span>

### <span data-ttu-id="11e28-137">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="11e28-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="11e28-138">筆記</span><span class="sxs-lookup"><span data-stu-id="11e28-138">NOTES</span></span>

## <span data-ttu-id="11e28-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="11e28-139">RELATED LINKS</span></span>
