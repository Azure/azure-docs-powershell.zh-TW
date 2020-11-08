---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136059"
---
# <span data-ttu-id="c798d-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="c798d-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="c798d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c798d-102">SYNOPSIS</span></span>
<span data-ttu-id="c798d-103">刪除 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="c798d-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="c798d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c798d-104">SYNTAX</span></span>

### <span data-ttu-id="c798d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c798d-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c798d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c798d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c798d-107">說明</span><span class="sxs-lookup"><span data-stu-id="c798d-107">DESCRIPTION</span></span>
<span data-ttu-id="c798d-108">**AzCosmosDBMongoDBCollection** Cmdlet 會刪除 CosmosDB MongoDB 集合。</span><span class="sxs-lookup"><span data-stu-id="c798d-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="c798d-109">示例</span><span class="sxs-lookup"><span data-stu-id="c798d-109">EXAMPLES</span></span>

### <span data-ttu-id="c798d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c798d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="c798d-111">如果刪除成功，則此 Cmdlet 會) 傳回類型為 bool (的物件。</span><span class="sxs-lookup"><span data-stu-id="c798d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="c798d-112">參數</span><span class="sxs-lookup"><span data-stu-id="c798d-112">PARAMETERS</span></span>

### <span data-ttu-id="c798d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c798d-113">-AccountName</span></span>
<span data-ttu-id="c798d-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c798d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c798d-115">-確認</span><span class="sxs-lookup"><span data-stu-id="c798d-115">-Confirm</span></span>
<span data-ttu-id="c798d-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c798d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c798d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c798d-117">-DatabaseName</span></span>
<span data-ttu-id="c798d-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c798d-118">Database name.</span></span>

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

### <span data-ttu-id="c798d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c798d-119">-DefaultProfile</span></span>
<span data-ttu-id="c798d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c798d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c798d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c798d-121">-InputObject</span></span>
<span data-ttu-id="c798d-122">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="c798d-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c798d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c798d-123">-Name</span></span>
<span data-ttu-id="c798d-124">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="c798d-124">Collection name.</span></span>

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

### <span data-ttu-id="c798d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c798d-125">-PassThru</span></span>
<span data-ttu-id="c798d-126">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="c798d-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c798d-127">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c798d-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c798d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c798d-128">-ResourceGroupName</span></span>
<span data-ttu-id="c798d-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c798d-129">Name of resource group.</span></span>

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

### <span data-ttu-id="c798d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c798d-130">-WhatIf</span></span>
<span data-ttu-id="c798d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c798d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c798d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c798d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c798d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c798d-133">CommonParameters</span></span>
<span data-ttu-id="c798d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c798d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c798d-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c798d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c798d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c798d-136">INPUTS</span></span>

### <span data-ttu-id="c798d-137">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="c798d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="c798d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c798d-138">OUTPUTS</span></span>

### <span data-ttu-id="c798d-139">System.void</span><span class="sxs-lookup"><span data-stu-id="c798d-139">System.Void</span></span>

### <span data-ttu-id="c798d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="c798d-140">System.Boolean</span></span>

## <span data-ttu-id="c798d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c798d-141">NOTES</span></span>

## <span data-ttu-id="c798d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c798d-142">RELATED LINKS</span></span>