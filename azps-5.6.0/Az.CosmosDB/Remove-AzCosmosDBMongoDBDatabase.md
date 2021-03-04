---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: aa5934de20812a8f8a5ebf76c4b23e01cb59d2b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913249"
---
# <span data-ttu-id="63b37-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="63b37-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="63b37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63b37-102">SYNOPSIS</span></span>
<span data-ttu-id="63b37-103">刪除一個代斯DB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="63b37-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="63b37-104">語法</span><span class="sxs-lookup"><span data-stu-id="63b37-104">SYNTAX</span></span>

### <span data-ttu-id="63b37-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63b37-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63b37-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63b37-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63b37-107">描述</span><span class="sxs-lookup"><span data-stu-id="63b37-107">DESCRIPTION</span></span>
<span data-ttu-id="63b37-108">**Remove-AzCosmosDBMongoDBDatabase** Cmdlet 會刪除一個OsosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="63b37-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="63b37-109">例子</span><span class="sxs-lookup"><span data-stu-id="63b37-109">EXAMPLES</span></span>

### <span data-ttu-id="63b37-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="63b37-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="63b37-111">當傳遞 -PassThru 時，cmd (let 會傳回類型布林值的物件) 如果刪除成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="63b37-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="63b37-112">參數</span><span class="sxs-lookup"><span data-stu-id="63b37-112">PARAMETERS</span></span>

### <span data-ttu-id="63b37-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63b37-113">-AccountName</span></span>
<span data-ttu-id="63b37-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="63b37-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="63b37-115">-確認</span><span class="sxs-lookup"><span data-stu-id="63b37-115">-Confirm</span></span>
<span data-ttu-id="63b37-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63b37-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63b37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63b37-117">-DefaultProfile</span></span>
<span data-ttu-id="63b37-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63b37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63b37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63b37-119">-InputObject</span></span>
<span data-ttu-id="63b37-120">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="63b37-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63b37-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="63b37-121">-Name</span></span>
<span data-ttu-id="63b37-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="63b37-122">Database name.</span></span>

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

### <span data-ttu-id="63b37-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63b37-123">-PassThru</span></span>
<span data-ttu-id="63b37-124">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="63b37-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="63b37-125">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="63b37-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="63b37-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63b37-126">-ResourceGroupName</span></span>
<span data-ttu-id="63b37-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="63b37-127">Name of resource group.</span></span>

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

### <span data-ttu-id="63b37-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63b37-128">-WhatIf</span></span>
<span data-ttu-id="63b37-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63b37-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63b37-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63b37-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63b37-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63b37-131">CommonParameters</span></span>
<span data-ttu-id="63b37-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63b37-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63b37-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63b37-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63b37-134">輸入</span><span class="sxs-lookup"><span data-stu-id="63b37-134">INPUTS</span></span>

### <span data-ttu-id="63b37-135">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="63b37-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="63b37-136">輸出</span><span class="sxs-lookup"><span data-stu-id="63b37-136">OUTPUTS</span></span>

### <span data-ttu-id="63b37-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="63b37-137">System.Void</span></span>

### <span data-ttu-id="63b37-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63b37-138">System.Boolean</span></span>

## <span data-ttu-id="63b37-139">筆記</span><span class="sxs-lookup"><span data-stu-id="63b37-139">NOTES</span></span>

## <span data-ttu-id="63b37-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="63b37-140">RELATED LINKS</span></span>
