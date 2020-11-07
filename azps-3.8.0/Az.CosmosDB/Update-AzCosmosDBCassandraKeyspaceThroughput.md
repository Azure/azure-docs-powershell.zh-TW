---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 0c104573fe0ecfb710f37c9c2fe898a6777f49e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956484"
---
# <span data-ttu-id="c238b-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="c238b-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="c238b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c238b-102">SYNOPSIS</span></span>
<span data-ttu-id="c238b-103">更新 CosmosDB Cassandra Keyspace 的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="c238b-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c238b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c238b-104">SYNTAX</span></span>

### <span data-ttu-id="c238b-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c238b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c238b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c238b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c238b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c238b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c238b-108">示例</span><span class="sxs-lookup"><span data-stu-id="c238b-108">EXAMPLES</span></span>

### <span data-ttu-id="c238b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="c238b-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="c238b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c238b-110">PARAMETERS</span></span>

### <span data-ttu-id="c238b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c238b-111">-AccountName</span></span>
<span data-ttu-id="c238b-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c238b-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c238b-113">-確認</span><span class="sxs-lookup"><span data-stu-id="c238b-113">-Confirm</span></span>
<span data-ttu-id="c238b-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c238b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c238b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c238b-115">-DefaultProfile</span></span>
<span data-ttu-id="c238b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c238b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c238b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c238b-117">-InputObject</span></span>
<span data-ttu-id="c238b-118">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="c238b-118">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c238b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c238b-119">-Name</span></span>
<span data-ttu-id="c238b-120">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="c238b-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c238b-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c238b-121">-ParentObject</span></span>
<span data-ttu-id="c238b-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="c238b-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c238b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c238b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c238b-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c238b-124">Name of resource group.</span></span>

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

### <span data-ttu-id="c238b-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="c238b-125">-Throughput</span></span>
<span data-ttu-id="c238b-126">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="c238b-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="c238b-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="c238b-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c238b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c238b-128">-WhatIf</span></span>
<span data-ttu-id="c238b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c238b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c238b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c238b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c238b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c238b-131">CommonParameters</span></span>
<span data-ttu-id="c238b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c238b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c238b-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c238b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c238b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c238b-134">INPUTS</span></span>

### <span data-ttu-id="c238b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c238b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c238b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c238b-136">OUTPUTS</span></span>

### <span data-ttu-id="c238b-137">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="c238b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c238b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c238b-138">NOTES</span></span>

## <span data-ttu-id="c238b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c238b-139">RELATED LINKS</span></span>
