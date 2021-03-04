---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 65b1cbaebdf4118b5e22a7d1f9672273281ba55b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912433"
---
# <span data-ttu-id="28860-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="28860-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="28860-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28860-102">SYNOPSIS</span></span>
<span data-ttu-id="28860-103">請使用此功能將自動縮放輸送量遷移到手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="28860-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="28860-104">語法</span><span class="sxs-lookup"><span data-stu-id="28860-104">SYNTAX</span></span>

### <span data-ttu-id="28860-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28860-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28860-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28860-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28860-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28860-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28860-108">描述</span><span class="sxs-lookup"><span data-stu-id="28860-108">DESCRIPTION</span></span>
<span data-ttu-id="28860-109">ThroughpyteType 參數會定義要遷移到的輸送量。</span><span class="sxs-lookup"><span data-stu-id="28860-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="28860-110">例子</span><span class="sxs-lookup"><span data-stu-id="28860-110">EXAMPLES</span></span>

### <span data-ttu-id="28860-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="28860-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="28860-112">參數</span><span class="sxs-lookup"><span data-stu-id="28860-112">PARAMETERS</span></span>

### <span data-ttu-id="28860-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28860-113">-AccountName</span></span>
<span data-ttu-id="28860-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="28860-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="28860-115">-確認</span><span class="sxs-lookup"><span data-stu-id="28860-115">-Confirm</span></span>
<span data-ttu-id="28860-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28860-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28860-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28860-117">-DefaultProfile</span></span>
<span data-ttu-id="28860-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28860-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28860-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28860-119">-InputObject</span></span>
<span data-ttu-id="28860-120">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="28860-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28860-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="28860-121">-KeyspaceName</span></span>
<span data-ttu-id="28860-122">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="28860-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="28860-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="28860-123">-Name</span></span>
<span data-ttu-id="28860-124">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="28860-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="28860-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="28860-125">-ParentObject</span></span>
<span data-ttu-id="28860-126">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="28860-126">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28860-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28860-127">-ResourceGroupName</span></span>
<span data-ttu-id="28860-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28860-128">Name of resource group.</span></span>

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

### <span data-ttu-id="28860-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="28860-129">-ThroughputType</span></span>
<span data-ttu-id="28860-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="28860-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="28860-131">可能的值有：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="28860-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="28860-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28860-132">-WhatIf</span></span>
<span data-ttu-id="28860-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28860-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28860-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28860-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28860-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28860-135">CommonParameters</span></span>
<span data-ttu-id="28860-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28860-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28860-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28860-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28860-138">輸入</span><span class="sxs-lookup"><span data-stu-id="28860-138">INPUTS</span></span>

### <span data-ttu-id="28860-139">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="28860-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="28860-140">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="28860-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="28860-141">輸出</span><span class="sxs-lookup"><span data-stu-id="28860-141">OUTPUTS</span></span>

### <span data-ttu-id="28860-142">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="28860-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="28860-143">筆記</span><span class="sxs-lookup"><span data-stu-id="28860-143">NOTES</span></span>

## <span data-ttu-id="28860-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="28860-144">RELATED LINKS</span></span>
