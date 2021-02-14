---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143295"
---
# <span data-ttu-id="e6c31-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6c31-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="e6c31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6c31-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c31-103">建立新的 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e6c31-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="e6c31-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6c31-104">SYNTAX</span></span>

### <span data-ttu-id="e6c31-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e6c31-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6c31-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6c31-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c31-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6c31-107">DESCRIPTION</span></span>
<span data-ttu-id="e6c31-108">建立新的 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e6c31-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="e6c31-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6c31-109">EXAMPLES</span></span>

### <span data-ttu-id="e6c31-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e6c31-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="e6c31-111">參數</span><span class="sxs-lookup"><span data-stu-id="e6c31-111">PARAMETERS</span></span>

### <span data-ttu-id="e6c31-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e6c31-112">-AccountName</span></span>
<span data-ttu-id="e6c31-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c31-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e6c31-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e6c31-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e6c31-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="e6c31-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e6c31-116">-確認</span><span class="sxs-lookup"><span data-stu-id="e6c31-116">-Confirm</span></span>
<span data-ttu-id="e6c31-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6c31-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6c31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c31-118">-DefaultProfile</span></span>
<span data-ttu-id="e6c31-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6c31-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c31-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6c31-120">-Name</span></span>
<span data-ttu-id="e6c31-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c31-121">Database name.</span></span>

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

### <span data-ttu-id="e6c31-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e6c31-122">-ParentObject</span></span>
<span data-ttu-id="e6c31-123">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e6c31-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e6c31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c31-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6c31-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c31-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e6c31-126">-輸送量</span><span class="sxs-lookup"><span data-stu-id="e6c31-126">-Throughput</span></span>
<span data-ttu-id="e6c31-127">SQL database 的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="e6c31-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="e6c31-128">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="e6c31-128">Default value is 400.</span></span>

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

### <span data-ttu-id="e6c31-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6c31-129">-WhatIf</span></span>
<span data-ttu-id="e6c31-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6c31-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6c31-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6c31-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6c31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c31-132">CommonParameters</span></span>
<span data-ttu-id="e6c31-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6c31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c31-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e6c31-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c31-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e6c31-135">INPUTS</span></span>

### <span data-ttu-id="e6c31-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e6c31-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e6c31-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e6c31-137">OUTPUTS</span></span>

### <span data-ttu-id="e6c31-138">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e6c31-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e6c31-139">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e6c31-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e6c31-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e6c31-140">NOTES</span></span>

## <span data-ttu-id="e6c31-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6c31-141">RELATED LINKS</span></span>
