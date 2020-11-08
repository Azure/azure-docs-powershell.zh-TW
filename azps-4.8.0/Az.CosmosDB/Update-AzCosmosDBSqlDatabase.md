---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128794"
---
# <span data-ttu-id="e9763-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9763-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="e9763-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9763-102">SYNOPSIS</span></span>
<span data-ttu-id="e9763-103">更新 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9763-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="e9763-104">透過讀取現有的資料庫來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="e9763-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="e9763-105">句法</span><span class="sxs-lookup"><span data-stu-id="e9763-105">SYNTAX</span></span>

### <span data-ttu-id="e9763-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9763-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9763-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9763-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9763-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9763-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9763-109">說明</span><span class="sxs-lookup"><span data-stu-id="e9763-109">DESCRIPTION</span></span>
<span data-ttu-id="e9763-110">更新 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9763-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="e9763-111">透過讀取現有的資料庫來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="e9763-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="e9763-112">示例</span><span class="sxs-lookup"><span data-stu-id="e9763-112">EXAMPLES</span></span>

### <span data-ttu-id="e9763-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e9763-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="e9763-114">參數</span><span class="sxs-lookup"><span data-stu-id="e9763-114">PARAMETERS</span></span>

### <span data-ttu-id="e9763-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9763-115">-AccountName</span></span>
<span data-ttu-id="e9763-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9763-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e9763-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e9763-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e9763-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="e9763-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e9763-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e9763-119">-Confirm</span></span>
<span data-ttu-id="e9763-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9763-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9763-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9763-121">-DefaultProfile</span></span>
<span data-ttu-id="e9763-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9763-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9763-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9763-123">-InputObject</span></span>
<span data-ttu-id="e9763-124">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="e9763-124">Sql Database object.</span></span>

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

### <span data-ttu-id="e9763-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9763-125">-Name</span></span>
<span data-ttu-id="e9763-126">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e9763-126">Database name.</span></span>

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

### <span data-ttu-id="e9763-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e9763-127">-ParentObject</span></span>
<span data-ttu-id="e9763-128">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e9763-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e9763-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9763-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9763-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9763-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e9763-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="e9763-131">-Throughput</span></span>
<span data-ttu-id="e9763-132">SQL database 的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="e9763-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="e9763-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="e9763-133">Default value is 400.</span></span>

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

### <span data-ttu-id="e9763-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9763-134">-WhatIf</span></span>
<span data-ttu-id="e9763-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9763-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9763-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9763-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9763-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9763-137">CommonParameters</span></span>
<span data-ttu-id="e9763-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9763-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9763-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9763-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9763-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e9763-140">INPUTS</span></span>

### <span data-ttu-id="e9763-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e9763-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="e9763-142">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e9763-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="e9763-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e9763-143">OUTPUTS</span></span>

### <span data-ttu-id="e9763-144">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e9763-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e9763-145">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e9763-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e9763-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e9763-146">NOTES</span></span>

## <span data-ttu-id="e9763-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9763-147">RELATED LINKS</span></span>