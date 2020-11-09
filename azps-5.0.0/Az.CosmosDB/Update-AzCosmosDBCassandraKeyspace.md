---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285435"
---
# <span data-ttu-id="573ff-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="573ff-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="573ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="573ff-102">SYNOPSIS</span></span>
<span data-ttu-id="573ff-103">更新 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="573ff-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="573ff-104">讀取現有的 Keyspace，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="573ff-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="573ff-105">句法</span><span class="sxs-lookup"><span data-stu-id="573ff-105">SYNTAX</span></span>

### <span data-ttu-id="573ff-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="573ff-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="573ff-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="573ff-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="573ff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="573ff-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="573ff-109">說明</span><span class="sxs-lookup"><span data-stu-id="573ff-109">DESCRIPTION</span></span>
<span data-ttu-id="573ff-110">更新 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="573ff-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="573ff-111">讀取現有的 Keyspace，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="573ff-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="573ff-112">示例</span><span class="sxs-lookup"><span data-stu-id="573ff-112">EXAMPLES</span></span>

### <span data-ttu-id="573ff-113">範例1</span><span class="sxs-lookup"><span data-stu-id="573ff-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="573ff-114">參數</span><span class="sxs-lookup"><span data-stu-id="573ff-114">PARAMETERS</span></span>

### <span data-ttu-id="573ff-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="573ff-115">-AccountName</span></span>
<span data-ttu-id="573ff-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="573ff-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="573ff-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="573ff-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="573ff-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="573ff-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="573ff-119">-確認</span><span class="sxs-lookup"><span data-stu-id="573ff-119">-Confirm</span></span>
<span data-ttu-id="573ff-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="573ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573ff-121">-DefaultProfile</span></span>
<span data-ttu-id="573ff-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="573ff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573ff-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="573ff-123">-InputObject</span></span>
<span data-ttu-id="573ff-124">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="573ff-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="573ff-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="573ff-125">-Name</span></span>
<span data-ttu-id="573ff-126">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="573ff-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="573ff-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="573ff-127">-ParentObject</span></span>
<span data-ttu-id="573ff-128">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="573ff-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="573ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="573ff-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="573ff-130">Name of resource group.</span></span>

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

### <span data-ttu-id="573ff-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="573ff-131">-Throughput</span></span>
<span data-ttu-id="573ff-132">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="573ff-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="573ff-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="573ff-133">Default value is 400.</span></span>

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

### <span data-ttu-id="573ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573ff-134">-WhatIf</span></span>
<span data-ttu-id="573ff-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="573ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573ff-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="573ff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573ff-137">CommonParameters</span></span>
<span data-ttu-id="573ff-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="573ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573ff-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="573ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573ff-140">輸入</span><span class="sxs-lookup"><span data-stu-id="573ff-140">INPUTS</span></span>

### <span data-ttu-id="573ff-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="573ff-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="573ff-142">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="573ff-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="573ff-143">輸出</span><span class="sxs-lookup"><span data-stu-id="573ff-143">OUTPUTS</span></span>

### <span data-ttu-id="573ff-144">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="573ff-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="573ff-145">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="573ff-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="573ff-146">筆記</span><span class="sxs-lookup"><span data-stu-id="573ff-146">NOTES</span></span>

## <span data-ttu-id="573ff-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="573ff-147">RELATED LINKS</span></span>
