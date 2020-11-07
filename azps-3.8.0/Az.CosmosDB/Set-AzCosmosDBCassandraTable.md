---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965885"
---
# <span data-ttu-id="d0a7d-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="d0a7d-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="d0a7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a7d-103">設定 [CosmosDB Cassandra] 資料表。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="d0a7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0a7d-104">SYNTAX</span></span>

### <span data-ttu-id="d0a7d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d0a7d-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0a7d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0a7d-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a7d-107">說明</span><span class="sxs-lookup"><span data-stu-id="d0a7d-107">DESCRIPTION</span></span>
<span data-ttu-id="d0a7d-108">**AzCosmosDBCassandraTable** Cmdlet 會設定 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d0a7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="d0a7d-109">EXAMPLES</span></span>

### <span data-ttu-id="d0a7d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d0a7d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="d0a7d-111">資源物件包含 _rid、_ts、_etag、DefaultTtl 與架構屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="d0a7d-112">參數</span><span class="sxs-lookup"><span data-stu-id="d0a7d-112">PARAMETERS</span></span>

### <span data-ttu-id="d0a7d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0a7d-113">-AccountName</span></span>
<span data-ttu-id="d0a7d-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0a7d-115">-確認</span><span class="sxs-lookup"><span data-stu-id="d0a7d-115">-Confirm</span></span>
<span data-ttu-id="d0a7d-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a7d-117">-DefaultProfile</span></span>
<span data-ttu-id="d0a7d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a7d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0a7d-119">-InputObject</span></span>
<span data-ttu-id="d0a7d-120">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="d0a7d-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="d0a7d-121">-KeyspaceName</span></span>
<span data-ttu-id="d0a7d-122">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d0a7d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0a7d-123">-Name</span></span>
<span data-ttu-id="d0a7d-124">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="d0a7d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a7d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0a7d-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d0a7d-127">-架構</span><span class="sxs-lookup"><span data-stu-id="d0a7d-127">-Schema</span></span>
<span data-ttu-id="d0a7d-128">PSCassandraSchema 物件。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="d0a7d-129">使用 New-AzCosmosDBCassandraSchema 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a7d-130">-輸送量</span><span class="sxs-lookup"><span data-stu-id="d0a7d-130">-Throughput</span></span>
<span data-ttu-id="d0a7d-131">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="d0a7d-132">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-132">Default value is 400.</span></span>

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

### <span data-ttu-id="d0a7d-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d0a7d-133">-TtlInSeconds</span></span>
<span data-ttu-id="d0a7d-134">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="d0a7d-135">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d0a7d-136">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d0a7d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a7d-137">-WhatIf</span></span>
<span data-ttu-id="d0a7d-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a7d-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a7d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a7d-140">CommonParameters</span></span>
<span data-ttu-id="d0a7d-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a7d-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a7d-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d0a7d-143">INPUTS</span></span>

### <span data-ttu-id="d0a7d-144">PSCassandraSchema 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="d0a7d-145">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="d0a7d-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d0a7d-146">OUTPUTS</span></span>

### <span data-ttu-id="d0a7d-147">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d0a7d-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="d0a7d-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d0a7d-148">NOTES</span></span>

## <span data-ttu-id="d0a7d-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0a7d-149">RELATED LINKS</span></span>
