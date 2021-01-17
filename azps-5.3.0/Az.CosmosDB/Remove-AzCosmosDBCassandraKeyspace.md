---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446031"
---
# <span data-ttu-id="235d6-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="235d6-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="235d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="235d6-102">SYNOPSIS</span></span>
<span data-ttu-id="235d6-103">刪除 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="235d6-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="235d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="235d6-104">SYNTAX</span></span>

### <span data-ttu-id="235d6-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="235d6-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235d6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="235d6-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235d6-107">說明</span><span class="sxs-lookup"><span data-stu-id="235d6-107">DESCRIPTION</span></span>
<span data-ttu-id="235d6-108">AzCosmosDBCassandraKeyspace Cmdlet 會刪除現有 **的** CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="235d6-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="235d6-109">示例</span><span class="sxs-lookup"><span data-stu-id="235d6-109">EXAMPLES</span></span>

### <span data-ttu-id="235d6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="235d6-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="235d6-111">在傳遞時，Cmdlet 會傳回類型為 bool (的物件) 如果刪除成功，則為 true。</span><span class="sxs-lookup"><span data-stu-id="235d6-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="235d6-112">參數</span><span class="sxs-lookup"><span data-stu-id="235d6-112">PARAMETERS</span></span>

### <span data-ttu-id="235d6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="235d6-113">-AccountName</span></span>
<span data-ttu-id="235d6-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="235d6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="235d6-115">-確認</span><span class="sxs-lookup"><span data-stu-id="235d6-115">-Confirm</span></span>
<span data-ttu-id="235d6-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235d6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235d6-117">-DefaultProfile</span></span>
<span data-ttu-id="235d6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="235d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="235d6-119">-InputObject</span></span>
<span data-ttu-id="235d6-120">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="235d6-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="235d6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="235d6-121">-Name</span></span>
<span data-ttu-id="235d6-122">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="235d6-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="235d6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="235d6-123">-PassThru</span></span>
<span data-ttu-id="235d6-124">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="235d6-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="235d6-125">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="235d6-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="235d6-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="235d6-127">Name of resource group.</span></span>

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

### <span data-ttu-id="235d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235d6-128">-WhatIf</span></span>
<span data-ttu-id="235d6-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="235d6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235d6-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="235d6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235d6-131">CommonParameters</span></span>
<span data-ttu-id="235d6-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="235d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235d6-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="235d6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235d6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="235d6-134">INPUTS</span></span>

### <span data-ttu-id="235d6-135">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="235d6-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="235d6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="235d6-136">OUTPUTS</span></span>

### <span data-ttu-id="235d6-137">System.void</span><span class="sxs-lookup"><span data-stu-id="235d6-137">System.Void</span></span>

### <span data-ttu-id="235d6-138">System.object</span><span class="sxs-lookup"><span data-stu-id="235d6-138">System.Boolean</span></span>

## <span data-ttu-id="235d6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="235d6-139">NOTES</span></span>

## <span data-ttu-id="235d6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="235d6-140">RELATED LINKS</span></span>
