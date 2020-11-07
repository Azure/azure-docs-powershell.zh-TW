---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959656"
---
# <span data-ttu-id="69e7c-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="69e7c-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="69e7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="69e7c-103">刪除 CosmosDB Cassandra 表格。</span><span class="sxs-lookup"><span data-stu-id="69e7c-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="69e7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="69e7c-104">SYNTAX</span></span>

### <span data-ttu-id="69e7c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="69e7c-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69e7c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69e7c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69e7c-107">說明</span><span class="sxs-lookup"><span data-stu-id="69e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="69e7c-108">[ **移除-AzCosmosDBCassandraTable** ] 會刪除 CosmosDB Cassandra 資料表。</span><span class="sxs-lookup"><span data-stu-id="69e7c-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="69e7c-109">示例</span><span class="sxs-lookup"><span data-stu-id="69e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="69e7c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="69e7c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="69e7c-111">如果刪除成功，則此 Cmdlet 會) 傳回類型為 bool (的物件。</span><span class="sxs-lookup"><span data-stu-id="69e7c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="69e7c-112">參數</span><span class="sxs-lookup"><span data-stu-id="69e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="69e7c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="69e7c-113">-AccountName</span></span>
<span data-ttu-id="69e7c-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="69e7c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="69e7c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="69e7c-115">-Confirm</span></span>
<span data-ttu-id="69e7c-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69e7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e7c-117">-DefaultProfile</span></span>
<span data-ttu-id="69e7c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69e7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e7c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69e7c-119">-InputObject</span></span>
<span data-ttu-id="69e7c-120">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="69e7c-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="69e7c-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="69e7c-121">-KeyspaceName</span></span>
<span data-ttu-id="69e7c-122">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="69e7c-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="69e7c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="69e7c-123">-Name</span></span>
<span data-ttu-id="69e7c-124">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="69e7c-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="69e7c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69e7c-125">-PassThru</span></span>
<span data-ttu-id="69e7c-126">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="69e7c-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="69e7c-127">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="69e7c-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="69e7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e7c-128">-ResourceGroupName</span></span>
<span data-ttu-id="69e7c-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69e7c-129">Name of resource group.</span></span>

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

### <span data-ttu-id="69e7c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e7c-130">-WhatIf</span></span>
<span data-ttu-id="69e7c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69e7c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e7c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69e7c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e7c-133">CommonParameters</span></span>
<span data-ttu-id="69e7c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69e7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e7c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="69e7c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e7c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="69e7c-136">INPUTS</span></span>

### <span data-ttu-id="69e7c-137">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="69e7c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="69e7c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="69e7c-138">OUTPUTS</span></span>

### <span data-ttu-id="69e7c-139">System.void</span><span class="sxs-lookup"><span data-stu-id="69e7c-139">System.Void</span></span>

### <span data-ttu-id="69e7c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="69e7c-140">System.Boolean</span></span>

## <span data-ttu-id="69e7c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="69e7c-141">NOTES</span></span>

## <span data-ttu-id="69e7c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="69e7c-142">RELATED LINKS</span></span>
