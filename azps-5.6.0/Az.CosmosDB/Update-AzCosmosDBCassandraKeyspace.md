---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 4a9a5595345b44eaf3a3b44d9d9ba1d8895a6376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908285"
---
# <span data-ttu-id="9a2cb-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="9a2cb-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="9a2cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2cb-103">更新一些更新的一些資訊。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="9a2cb-104">讀取現有的 Keyspace 以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="9a2cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a2cb-105">SYNTAX</span></span>

### <span data-ttu-id="9a2cb-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9a2cb-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a2cb-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a2cb-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a2cb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a2cb-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a2cb-109">描述</span><span class="sxs-lookup"><span data-stu-id="9a2cb-109">DESCRIPTION</span></span>
<span data-ttu-id="9a2cb-110">更新一些更新的一些資訊。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="9a2cb-111">讀取現有的 Keyspace 以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="9a2cb-112">例子</span><span class="sxs-lookup"><span data-stu-id="9a2cb-112">EXAMPLES</span></span>

### <span data-ttu-id="9a2cb-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="9a2cb-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="9a2cb-114">參數</span><span class="sxs-lookup"><span data-stu-id="9a2cb-114">PARAMETERS</span></span>

### <span data-ttu-id="9a2cb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a2cb-115">-AccountName</span></span>
<span data-ttu-id="9a2cb-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9a2cb-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9a2cb-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9a2cb-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9a2cb-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9a2cb-119">-Confirm</span></span>
<span data-ttu-id="9a2cb-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a2cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a2cb-121">-DefaultProfile</span></span>
<span data-ttu-id="9a2cb-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a2cb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a2cb-123">-InputObject</span></span>
<span data-ttu-id="9a2cb-124">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9a2cb-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a2cb-125">-Name</span></span>
<span data-ttu-id="9a2cb-126">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="9a2cb-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9a2cb-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a2cb-127">-ParentObject</span></span>
<span data-ttu-id="9a2cb-128">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9a2cb-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9a2cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a2cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a2cb-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-130">Name of resource group.</span></span>

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

### <span data-ttu-id="9a2cb-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="9a2cb-131">-Throughput</span></span>
<span data-ttu-id="9a2cb-132">Cassandra Keyspace (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9a2cb-133">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-133">Default value is 400.</span></span>

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

### <span data-ttu-id="9a2cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a2cb-134">-WhatIf</span></span>
<span data-ttu-id="9a2cb-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a2cb-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a2cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2cb-137">CommonParameters</span></span>
<span data-ttu-id="9a2cb-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2cb-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a2cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2cb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9a2cb-140">INPUTS</span></span>

### <span data-ttu-id="9a2cb-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9a2cb-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="9a2cb-142">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9a2cb-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9a2cb-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9a2cb-143">OUTPUTS</span></span>

### <span data-ttu-id="9a2cb-144">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9a2cb-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="9a2cb-145">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9a2cb-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9a2cb-146">筆記</span><span class="sxs-lookup"><span data-stu-id="9a2cb-146">NOTES</span></span>

## <span data-ttu-id="9a2cb-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a2cb-147">RELATED LINKS</span></span>
