---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285543"
---
# <span data-ttu-id="7ffae-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="7ffae-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="7ffae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ffae-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffae-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="7ffae-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="7ffae-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ffae-104">SYNTAX</span></span>

### <span data-ttu-id="7ffae-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7ffae-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ffae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ffae-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ffae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ffae-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ffae-108">說明</span><span class="sxs-lookup"><span data-stu-id="7ffae-108">DESCRIPTION</span></span>
<span data-ttu-id="7ffae-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="7ffae-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="7ffae-110">示例</span><span class="sxs-lookup"><span data-stu-id="7ffae-110">EXAMPLES</span></span>

### <span data-ttu-id="7ffae-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7ffae-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="7ffae-112">參數</span><span class="sxs-lookup"><span data-stu-id="7ffae-112">PARAMETERS</span></span>

### <span data-ttu-id="7ffae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ffae-113">-AccountName</span></span>
<span data-ttu-id="7ffae-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ffae-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7ffae-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7ffae-115">-Confirm</span></span>
<span data-ttu-id="7ffae-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7ffae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ffae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffae-117">-DefaultProfile</span></span>
<span data-ttu-id="7ffae-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ffae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ffae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ffae-119">-InputObject</span></span>
<span data-ttu-id="7ffae-120">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="7ffae-120">Sql Database object.</span></span>

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

### <span data-ttu-id="7ffae-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ffae-121">-Name</span></span>
<span data-ttu-id="7ffae-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7ffae-122">Database name.</span></span>

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

### <span data-ttu-id="7ffae-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7ffae-123">-ParentObject</span></span>
<span data-ttu-id="7ffae-124">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="7ffae-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7ffae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffae-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ffae-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ffae-126">Name of resource group.</span></span>

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

### <span data-ttu-id="7ffae-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="7ffae-127">-ThroughputType</span></span>
<span data-ttu-id="7ffae-128">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="7ffae-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="7ffae-129">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="7ffae-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="7ffae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ffae-130">-WhatIf</span></span>
<span data-ttu-id="7ffae-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ffae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ffae-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ffae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ffae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffae-133">CommonParameters</span></span>
<span data-ttu-id="7ffae-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ffae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffae-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ffae-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffae-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7ffae-136">INPUTS</span></span>

### <span data-ttu-id="7ffae-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="7ffae-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="7ffae-138">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7ffae-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="7ffae-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7ffae-139">OUTPUTS</span></span>

### <span data-ttu-id="7ffae-140">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7ffae-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7ffae-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7ffae-141">NOTES</span></span>

## <span data-ttu-id="7ffae-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ffae-142">RELATED LINKS</span></span>
