---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136539"
---
# <span data-ttu-id="cb19e-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="cb19e-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="cb19e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb19e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb19e-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="cb19e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="cb19e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb19e-104">SYNTAX</span></span>

### <span data-ttu-id="cb19e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cb19e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb19e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb19e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb19e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb19e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb19e-108">說明</span><span class="sxs-lookup"><span data-stu-id="cb19e-108">DESCRIPTION</span></span>
<span data-ttu-id="cb19e-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="cb19e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="cb19e-110">示例</span><span class="sxs-lookup"><span data-stu-id="cb19e-110">EXAMPLES</span></span>

### <span data-ttu-id="cb19e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cb19e-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="cb19e-112">參數</span><span class="sxs-lookup"><span data-stu-id="cb19e-112">PARAMETERS</span></span>

### <span data-ttu-id="cb19e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb19e-113">-AccountName</span></span>
<span data-ttu-id="cb19e-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb19e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cb19e-115">-確認</span><span class="sxs-lookup"><span data-stu-id="cb19e-115">-Confirm</span></span>
<span data-ttu-id="cb19e-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb19e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb19e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb19e-117">-DefaultProfile</span></span>
<span data-ttu-id="cb19e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb19e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb19e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb19e-119">-InputObject</span></span>
<span data-ttu-id="cb19e-120">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="cb19e-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="cb19e-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="cb19e-121">-KeyspaceName</span></span>
<span data-ttu-id="cb19e-122">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="cb19e-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="cb19e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb19e-123">-Name</span></span>
<span data-ttu-id="cb19e-124">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="cb19e-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="cb19e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cb19e-125">-ParentObject</span></span>
<span data-ttu-id="cb19e-126">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="cb19e-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="cb19e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb19e-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb19e-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb19e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="cb19e-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="cb19e-129">-ThroughputType</span></span>
<span data-ttu-id="cb19e-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="cb19e-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="cb19e-131">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="cb19e-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="cb19e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb19e-132">-WhatIf</span></span>
<span data-ttu-id="cb19e-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb19e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb19e-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb19e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb19e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb19e-135">CommonParameters</span></span>
<span data-ttu-id="cb19e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb19e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb19e-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb19e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb19e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cb19e-138">INPUTS</span></span>

### <span data-ttu-id="cb19e-139">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="cb19e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="cb19e-140">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="cb19e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="cb19e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cb19e-141">OUTPUTS</span></span>

### <span data-ttu-id="cb19e-142">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="cb19e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cb19e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cb19e-143">NOTES</span></span>

## <span data-ttu-id="cb19e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb19e-144">RELATED LINKS</span></span>
