---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: d860e9f5992cb1bd8df9a3f7f14e51565412284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907898"
---
# <span data-ttu-id="48d9d-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="48d9d-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="48d9d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="48d9d-103">刪除一個科克斯DB 卡薩德拉表格。</span><span class="sxs-lookup"><span data-stu-id="48d9d-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="48d9d-104">語法</span><span class="sxs-lookup"><span data-stu-id="48d9d-104">SYNTAX</span></span>

### <span data-ttu-id="48d9d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="48d9d-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48d9d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48d9d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d9d-107">描述</span><span class="sxs-lookup"><span data-stu-id="48d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="48d9d-108">**Remove-AzCosmosDBCassandraTable** delete a CasssDB Cassandra Table.</span><span class="sxs-lookup"><span data-stu-id="48d9d-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="48d9d-109">例子</span><span class="sxs-lookup"><span data-stu-id="48d9d-109">EXAMPLES</span></span>

### <span data-ttu-id="48d9d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="48d9d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="48d9d-111">當傳遞 -PassThru 時，cmd (let 會傳回類型布林值的物件) 如果刪除成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="48d9d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="48d9d-112">參數</span><span class="sxs-lookup"><span data-stu-id="48d9d-112">PARAMETERS</span></span>

### <span data-ttu-id="48d9d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48d9d-113">-AccountName</span></span>
<span data-ttu-id="48d9d-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="48d9d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="48d9d-115">-確認</span><span class="sxs-lookup"><span data-stu-id="48d9d-115">-Confirm</span></span>
<span data-ttu-id="48d9d-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="48d9d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d9d-117">-DefaultProfile</span></span>
<span data-ttu-id="48d9d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="48d9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d9d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48d9d-119">-InputObject</span></span>
<span data-ttu-id="48d9d-120">Cassandra Table 物件。</span><span class="sxs-lookup"><span data-stu-id="48d9d-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="48d9d-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="48d9d-121">-KeyspaceName</span></span>
<span data-ttu-id="48d9d-122">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="48d9d-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="48d9d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="48d9d-123">-Name</span></span>
<span data-ttu-id="48d9d-124">雅可拉表格名稱。</span><span class="sxs-lookup"><span data-stu-id="48d9d-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="48d9d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48d9d-125">-PassThru</span></span>
<span data-ttu-id="48d9d-126">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="48d9d-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="48d9d-127">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="48d9d-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="48d9d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d9d-128">-ResourceGroupName</span></span>
<span data-ttu-id="48d9d-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48d9d-129">Name of resource group.</span></span>

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

### <span data-ttu-id="48d9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d9d-130">-WhatIf</span></span>
<span data-ttu-id="48d9d-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48d9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48d9d-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48d9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d9d-133">CommonParameters</span></span>
<span data-ttu-id="48d9d-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48d9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d9d-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48d9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d9d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="48d9d-136">INPUTS</span></span>

### <span data-ttu-id="48d9d-137">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="48d9d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="48d9d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="48d9d-138">OUTPUTS</span></span>

### <span data-ttu-id="48d9d-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="48d9d-139">System.Void</span></span>

### <span data-ttu-id="48d9d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48d9d-140">System.Boolean</span></span>

## <span data-ttu-id="48d9d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="48d9d-141">NOTES</span></span>

## <span data-ttu-id="48d9d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="48d9d-142">RELATED LINKS</span></span>
