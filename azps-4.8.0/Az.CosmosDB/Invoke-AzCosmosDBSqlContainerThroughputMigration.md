---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136077"
---
# <span data-ttu-id="4d129-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="4d129-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="4d129-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d129-102">SYNOPSIS</span></span>
<span data-ttu-id="4d129-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="4d129-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="4d129-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d129-104">SYNTAX</span></span>

### <span data-ttu-id="4d129-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4d129-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d129-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d129-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d129-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d129-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d129-108">說明</span><span class="sxs-lookup"><span data-stu-id="4d129-108">DESCRIPTION</span></span>
<span data-ttu-id="4d129-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="4d129-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="4d129-110">示例</span><span class="sxs-lookup"><span data-stu-id="4d129-110">EXAMPLES</span></span>

### <span data-ttu-id="4d129-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4d129-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="4d129-112">參數</span><span class="sxs-lookup"><span data-stu-id="4d129-112">PARAMETERS</span></span>

### <span data-ttu-id="4d129-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d129-113">-AccountName</span></span>
<span data-ttu-id="4d129-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d129-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d129-115">-確認</span><span class="sxs-lookup"><span data-stu-id="4d129-115">-Confirm</span></span>
<span data-ttu-id="4d129-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d129-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d129-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d129-117">-DatabaseName</span></span>
<span data-ttu-id="4d129-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4d129-118">Database name.</span></span>

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

### <span data-ttu-id="4d129-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d129-119">-DefaultProfile</span></span>
<span data-ttu-id="4d129-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d129-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d129-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d129-121">-InputObject</span></span>
<span data-ttu-id="4d129-122">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="4d129-122">Sql Container object.</span></span>

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

### <span data-ttu-id="4d129-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d129-123">-Name</span></span>
<span data-ttu-id="4d129-124">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="4d129-124">Container name.</span></span>

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

### <span data-ttu-id="4d129-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d129-125">-ParentObject</span></span>
<span data-ttu-id="4d129-126">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="4d129-126">Sql Database object.</span></span>

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

### <span data-ttu-id="4d129-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d129-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d129-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d129-128">Name of resource group.</span></span>

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

### <span data-ttu-id="4d129-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="4d129-129">-ThroughputType</span></span>
<span data-ttu-id="4d129-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="4d129-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="4d129-131">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="4d129-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="4d129-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d129-132">-WhatIf</span></span>
<span data-ttu-id="4d129-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d129-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d129-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d129-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d129-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d129-135">CommonParameters</span></span>
<span data-ttu-id="4d129-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d129-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d129-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4d129-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d129-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4d129-138">INPUTS</span></span>

### <span data-ttu-id="4d129-139">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="4d129-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="4d129-140">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="4d129-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="4d129-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4d129-141">OUTPUTS</span></span>

### <span data-ttu-id="4d129-142">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="4d129-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4d129-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4d129-143">NOTES</span></span>

## <span data-ttu-id="4d129-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d129-144">RELATED LINKS</span></span>