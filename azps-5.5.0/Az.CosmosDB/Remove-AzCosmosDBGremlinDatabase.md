---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138483"
---
# <span data-ttu-id="b8136-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b8136-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b8136-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8136-102">SYNOPSIS</span></span>
<span data-ttu-id="b8136-103">刪除 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b8136-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b8136-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8136-104">SYNTAX</span></span>

### <span data-ttu-id="b8136-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8136-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8136-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8136-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8136-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8136-107">DESCRIPTION</span></span>
<span data-ttu-id="b8136-108">**AzCosmosDBGremlinDatabase** Cmdlet 會刪除 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b8136-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b8136-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8136-109">EXAMPLES</span></span>

### <span data-ttu-id="b8136-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b8136-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="b8136-111">如果刪除成功，則此 Cmdlet 會) 傳回類型為 bool (的物件。</span><span class="sxs-lookup"><span data-stu-id="b8136-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="b8136-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8136-112">PARAMETERS</span></span>

### <span data-ttu-id="b8136-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b8136-113">-AccountName</span></span>
<span data-ttu-id="b8136-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8136-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b8136-115">-確認</span><span class="sxs-lookup"><span data-stu-id="b8136-115">-Confirm</span></span>
<span data-ttu-id="b8136-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8136-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8136-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8136-117">-DefaultProfile</span></span>
<span data-ttu-id="b8136-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8136-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8136-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8136-119">-InputObject</span></span>
<span data-ttu-id="b8136-120">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="b8136-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8136-121">-Name</span></span>
<span data-ttu-id="b8136-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b8136-122">Database name.</span></span>

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

### <span data-ttu-id="b8136-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8136-123">-PassThru</span></span>
<span data-ttu-id="b8136-124">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="b8136-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b8136-125">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8136-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b8136-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8136-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8136-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8136-127">Name of resource group.</span></span>

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

### <span data-ttu-id="b8136-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8136-128">-WhatIf</span></span>
<span data-ttu-id="b8136-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8136-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8136-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8136-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8136-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8136-131">CommonParameters</span></span>
<span data-ttu-id="b8136-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8136-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8136-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8136-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8136-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b8136-134">INPUTS</span></span>

### <span data-ttu-id="b8136-135">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b8136-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b8136-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b8136-136">OUTPUTS</span></span>

### <span data-ttu-id="b8136-137">System.void</span><span class="sxs-lookup"><span data-stu-id="b8136-137">System.Void</span></span>

### <span data-ttu-id="b8136-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b8136-138">System.Boolean</span></span>

## <span data-ttu-id="b8136-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b8136-139">NOTES</span></span>

## <span data-ttu-id="b8136-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8136-140">RELATED LINKS</span></span>
