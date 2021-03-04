---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8195179599d98fbc3fd8954361ba142706460886
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916985"
---
# <span data-ttu-id="ce30e-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce30e-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="ce30e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce30e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce30e-103">建立新一個管理資料庫。</span><span class="sxs-lookup"><span data-stu-id="ce30e-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ce30e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce30e-104">SYNTAX</span></span>

### <span data-ttu-id="ce30e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ce30e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce30e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce30e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce30e-107">描述</span><span class="sxs-lookup"><span data-stu-id="ce30e-107">DESCRIPTION</span></span>
<span data-ttu-id="ce30e-108">建立新一個管理資料庫。</span><span class="sxs-lookup"><span data-stu-id="ce30e-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ce30e-109">例子</span><span class="sxs-lookup"><span data-stu-id="ce30e-109">EXAMPLES</span></span>

### <span data-ttu-id="ce30e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ce30e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="ce30e-111">參數</span><span class="sxs-lookup"><span data-stu-id="ce30e-111">PARAMETERS</span></span>

### <span data-ttu-id="ce30e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ce30e-112">-AccountName</span></span>
<span data-ttu-id="ce30e-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce30e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ce30e-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ce30e-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ce30e-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="ce30e-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ce30e-116">-確認</span><span class="sxs-lookup"><span data-stu-id="ce30e-116">-Confirm</span></span>
<span data-ttu-id="ce30e-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ce30e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce30e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce30e-118">-DefaultProfile</span></span>
<span data-ttu-id="ce30e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce30e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce30e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce30e-120">-Name</span></span>
<span data-ttu-id="ce30e-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ce30e-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce30e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ce30e-122">-ParentObject</span></span>
<span data-ttu-id="ce30e-123">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ce30e-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ce30e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce30e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce30e-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce30e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="ce30e-126">-輸送量</span><span class="sxs-lookup"><span data-stu-id="ce30e-126">-Throughput</span></span>
<span data-ttu-id="ce30e-127">SQL 資料庫的輸送量 (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="ce30e-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="ce30e-128">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="ce30e-128">Default value is 400.</span></span>

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

### <span data-ttu-id="ce30e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce30e-129">-WhatIf</span></span>
<span data-ttu-id="ce30e-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce30e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce30e-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce30e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce30e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce30e-132">CommonParameters</span></span>
<span data-ttu-id="ce30e-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce30e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce30e-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce30e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce30e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ce30e-135">INPUTS</span></span>

### <span data-ttu-id="ce30e-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ce30e-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ce30e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ce30e-137">OUTPUTS</span></span>

### <span data-ttu-id="ce30e-138">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ce30e-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ce30e-139">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ce30e-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ce30e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ce30e-140">NOTES</span></span>

## <span data-ttu-id="ce30e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce30e-141">RELATED LINKS</span></span>
