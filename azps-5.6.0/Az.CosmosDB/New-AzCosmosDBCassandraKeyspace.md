---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 9e06e6eaaea72b0fab9b3333291b29bdc09469d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905597"
---
# <span data-ttu-id="56ba4-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="56ba4-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="56ba4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="56ba4-103">建立新一個一格的花式鍵盤鍵格。</span><span class="sxs-lookup"><span data-stu-id="56ba4-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="56ba4-104">語法</span><span class="sxs-lookup"><span data-stu-id="56ba4-104">SYNTAX</span></span>

### <span data-ttu-id="56ba4-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="56ba4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56ba4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56ba4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56ba4-107">描述</span><span class="sxs-lookup"><span data-stu-id="56ba4-107">DESCRIPTION</span></span>
<span data-ttu-id="56ba4-108">建立新一個一格的花式鍵盤鍵格。</span><span class="sxs-lookup"><span data-stu-id="56ba4-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="56ba4-109">例子</span><span class="sxs-lookup"><span data-stu-id="56ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="56ba4-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="56ba4-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="56ba4-111">參數</span><span class="sxs-lookup"><span data-stu-id="56ba4-111">PARAMETERS</span></span>

### <span data-ttu-id="56ba4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56ba4-112">-AccountName</span></span>
<span data-ttu-id="56ba4-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="56ba4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="56ba4-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="56ba4-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="56ba4-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="56ba4-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="56ba4-116">-確認</span><span class="sxs-lookup"><span data-stu-id="56ba4-116">-Confirm</span></span>
<span data-ttu-id="56ba4-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56ba4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ba4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ba4-118">-DefaultProfile</span></span>
<span data-ttu-id="56ba4-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56ba4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ba4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="56ba4-120">-Name</span></span>
<span data-ttu-id="56ba4-121">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="56ba4-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="56ba4-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="56ba4-122">-ParentObject</span></span>
<span data-ttu-id="56ba4-123">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="56ba4-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="56ba4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ba4-124">-ResourceGroupName</span></span>
<span data-ttu-id="56ba4-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56ba4-125">Name of resource group.</span></span>

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

### <span data-ttu-id="56ba4-126">-輸送量</span><span class="sxs-lookup"><span data-stu-id="56ba4-126">-Throughput</span></span>
<span data-ttu-id="56ba4-127">Cassandra Keyspace (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="56ba4-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="56ba4-128">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="56ba4-128">Default value is 400.</span></span>

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

### <span data-ttu-id="56ba4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ba4-129">-WhatIf</span></span>
<span data-ttu-id="56ba4-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56ba4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ba4-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56ba4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ba4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ba4-132">CommonParameters</span></span>
<span data-ttu-id="56ba4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56ba4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ba4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56ba4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ba4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="56ba4-135">INPUTS</span></span>

### <span data-ttu-id="56ba4-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="56ba4-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="56ba4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="56ba4-137">OUTPUTS</span></span>

### <span data-ttu-id="56ba4-138">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="56ba4-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="56ba4-139">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="56ba4-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="56ba4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="56ba4-140">NOTES</span></span>

## <span data-ttu-id="56ba4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="56ba4-141">RELATED LINKS</span></span>
