---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128511"
---
# <span data-ttu-id="2ae08-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="2ae08-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="2ae08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ae08-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae08-103">取得 Cassandra 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="2ae08-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="2ae08-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ae08-104">SYNTAX</span></span>

### <span data-ttu-id="2ae08-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2ae08-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae08-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ae08-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ae08-107">說明</span><span class="sxs-lookup"><span data-stu-id="2ae08-107">DESCRIPTION</span></span>
<span data-ttu-id="2ae08-108">**AzCosmosDBCassandraTableThroughput** Cmdlet 會取得對應至指定 Keyspace 的輸送量物件。</span><span class="sxs-lookup"><span data-stu-id="2ae08-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="2ae08-109">示例</span><span class="sxs-lookup"><span data-stu-id="2ae08-109">EXAMPLES</span></span>

### <span data-ttu-id="2ae08-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2ae08-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="2ae08-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ae08-111">PARAMETERS</span></span>

### <span data-ttu-id="2ae08-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ae08-112">-AccountName</span></span>
<span data-ttu-id="2ae08-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ae08-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ae08-114">-確認</span><span class="sxs-lookup"><span data-stu-id="2ae08-114">-Confirm</span></span>
<span data-ttu-id="2ae08-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ae08-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae08-116">-DefaultProfile</span></span>
<span data-ttu-id="2ae08-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ae08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ae08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ae08-118">-InputObject</span></span>
<span data-ttu-id="2ae08-119">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="2ae08-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="2ae08-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="2ae08-120">-KeyspaceName</span></span>
<span data-ttu-id="2ae08-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2ae08-121">Database name.</span></span>

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

### <span data-ttu-id="2ae08-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ae08-122">-Name</span></span>
<span data-ttu-id="2ae08-123">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="2ae08-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="2ae08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae08-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ae08-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ae08-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2ae08-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae08-126">-WhatIf</span></span>
<span data-ttu-id="2ae08-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ae08-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae08-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ae08-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae08-129">CommonParameters</span></span>
<span data-ttu-id="2ae08-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ae08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae08-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ae08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae08-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2ae08-132">INPUTS</span></span>

### <span data-ttu-id="2ae08-133">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2ae08-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="2ae08-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2ae08-134">OUTPUTS</span></span>

### <span data-ttu-id="2ae08-135">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2ae08-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2ae08-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2ae08-136">NOTES</span></span>

## <span data-ttu-id="2ae08-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ae08-137">RELATED LINKS</span></span>
