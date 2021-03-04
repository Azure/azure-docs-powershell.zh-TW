---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 7693d507874dc5ebc4aa7b9c720c3efbe2963c05
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909842"
---
# <span data-ttu-id="2b2a3-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="2b2a3-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="2b2a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2a3-103">獲得卡薩德拉表格的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="2b2a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b2a3-104">SYNTAX</span></span>

### <span data-ttu-id="2b2a3-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2b2a3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b2a3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b2a3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b2a3-107">描述</span><span class="sxs-lookup"><span data-stu-id="2b2a3-107">DESCRIPTION</span></span>
<span data-ttu-id="2b2a3-108">**Get-AzCosmosDBCassandraTableThroughput Cmdlet** 會取得對應至給定 Keyspace 的輸送量物件。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="2b2a3-109">例子</span><span class="sxs-lookup"><span data-stu-id="2b2a3-109">EXAMPLES</span></span>

### <span data-ttu-id="2b2a3-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2b2a3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="2b2a3-111">參數</span><span class="sxs-lookup"><span data-stu-id="2b2a3-111">PARAMETERS</span></span>

### <span data-ttu-id="2b2a3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b2a3-112">-AccountName</span></span>
<span data-ttu-id="2b2a3-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2b2a3-114">-確認</span><span class="sxs-lookup"><span data-stu-id="2b2a3-114">-Confirm</span></span>
<span data-ttu-id="2b2a3-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2a3-116">-DefaultProfile</span></span>
<span data-ttu-id="2b2a3-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b2a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b2a3-118">-InputObject</span></span>
<span data-ttu-id="2b2a3-119">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="2b2a3-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="2b2a3-120">-KeyspaceName</span></span>
<span data-ttu-id="2b2a3-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-121">Database name.</span></span>

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

### <span data-ttu-id="2b2a3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b2a3-122">-Name</span></span>
<span data-ttu-id="2b2a3-123">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="2b2a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b2a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b2a3-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2b2a3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2a3-126">-WhatIf</span></span>
<span data-ttu-id="2b2a3-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b2a3-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2a3-129">CommonParameters</span></span>
<span data-ttu-id="2b2a3-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b2a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2a3-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b2a3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2a3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2b2a3-132">INPUTS</span></span>

### <span data-ttu-id="2b2a3-133">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="2b2a3-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="2b2a3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2b2a3-134">OUTPUTS</span></span>

### <span data-ttu-id="2b2a3-135">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2b2a3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2b2a3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2b2a3-136">NOTES</span></span>

## <span data-ttu-id="2b2a3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b2a3-137">RELATED LINKS</span></span>
