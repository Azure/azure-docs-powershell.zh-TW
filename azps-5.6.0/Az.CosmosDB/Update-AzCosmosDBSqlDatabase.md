---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1bfb0ec8392c0ddcce20db839f1817688e8feb7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908222"
---
# <span data-ttu-id="83a56-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="83a56-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="83a56-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83a56-102">SYNOPSIS</span></span>
<span data-ttu-id="83a56-103">更新一些更新的一些 Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="83a56-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="83a56-104">讀取現有的資料庫，以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="83a56-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="83a56-105">語法</span><span class="sxs-lookup"><span data-stu-id="83a56-105">SYNTAX</span></span>

### <span data-ttu-id="83a56-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="83a56-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83a56-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a56-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83a56-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a56-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83a56-109">描述</span><span class="sxs-lookup"><span data-stu-id="83a56-109">DESCRIPTION</span></span>
<span data-ttu-id="83a56-110">更新一些更新的一些 Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="83a56-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="83a56-111">讀取現有的資料庫，以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="83a56-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="83a56-112">例子</span><span class="sxs-lookup"><span data-stu-id="83a56-112">EXAMPLES</span></span>

### <span data-ttu-id="83a56-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="83a56-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="83a56-114">參數</span><span class="sxs-lookup"><span data-stu-id="83a56-114">PARAMETERS</span></span>

### <span data-ttu-id="83a56-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="83a56-115">-AccountName</span></span>
<span data-ttu-id="83a56-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a56-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="83a56-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="83a56-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="83a56-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="83a56-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="83a56-119">-確認</span><span class="sxs-lookup"><span data-stu-id="83a56-119">-Confirm</span></span>
<span data-ttu-id="83a56-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="83a56-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83a56-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a56-121">-DefaultProfile</span></span>
<span data-ttu-id="83a56-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83a56-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83a56-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83a56-123">-InputObject</span></span>
<span data-ttu-id="83a56-124">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="83a56-124">Sql Database object.</span></span>

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

### <span data-ttu-id="83a56-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="83a56-125">-Name</span></span>
<span data-ttu-id="83a56-126">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="83a56-126">Database name.</span></span>

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

### <span data-ttu-id="83a56-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="83a56-127">-ParentObject</span></span>
<span data-ttu-id="83a56-128">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="83a56-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="83a56-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a56-129">-ResourceGroupName</span></span>
<span data-ttu-id="83a56-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a56-130">Name of resource group.</span></span>

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

### <span data-ttu-id="83a56-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="83a56-131">-Throughput</span></span>
<span data-ttu-id="83a56-132">SQL 資料庫的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="83a56-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="83a56-133">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="83a56-133">Default value is 400.</span></span>

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

### <span data-ttu-id="83a56-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83a56-134">-WhatIf</span></span>
<span data-ttu-id="83a56-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83a56-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83a56-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83a56-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83a56-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a56-137">CommonParameters</span></span>
<span data-ttu-id="83a56-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83a56-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a56-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83a56-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a56-140">輸入</span><span class="sxs-lookup"><span data-stu-id="83a56-140">INPUTS</span></span>

### <span data-ttu-id="83a56-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="83a56-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="83a56-142">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="83a56-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="83a56-143">輸出</span><span class="sxs-lookup"><span data-stu-id="83a56-143">OUTPUTS</span></span>

### <span data-ttu-id="83a56-144">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="83a56-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="83a56-145">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="83a56-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="83a56-146">筆記</span><span class="sxs-lookup"><span data-stu-id="83a56-146">NOTES</span></span>

## <span data-ttu-id="83a56-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="83a56-147">RELATED LINKS</span></span>
