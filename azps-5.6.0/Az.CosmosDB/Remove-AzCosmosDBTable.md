---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ff294af7e4305facd3265d96151c97b82ff9c052
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916770"
---
# <span data-ttu-id="e177a-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="e177a-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="e177a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e177a-102">SYNOPSIS</span></span>
<span data-ttu-id="e177a-103">刪除一個花邊DB 表格。</span><span class="sxs-lookup"><span data-stu-id="e177a-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="e177a-104">語法</span><span class="sxs-lookup"><span data-stu-id="e177a-104">SYNTAX</span></span>

### <span data-ttu-id="e177a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e177a-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e177a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e177a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e177a-107">描述</span><span class="sxs-lookup"><span data-stu-id="e177a-107">DESCRIPTION</span></span>
<span data-ttu-id="e177a-108">**Remove-AzCosmosDBTable** Cmdlet 會刪除一個以一個資料表表示的一個資料表。</span><span class="sxs-lookup"><span data-stu-id="e177a-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="e177a-109">例子</span><span class="sxs-lookup"><span data-stu-id="e177a-109">EXAMPLES</span></span>

### <span data-ttu-id="e177a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e177a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="e177a-111">當傳遞 -PassThru 時，cmd (let 會傳回類型布林值的物件) 如果刪除成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e177a-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="e177a-112">參數</span><span class="sxs-lookup"><span data-stu-id="e177a-112">PARAMETERS</span></span>

### <span data-ttu-id="e177a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e177a-113">-AccountName</span></span>
<span data-ttu-id="e177a-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e177a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e177a-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e177a-115">-Confirm</span></span>
<span data-ttu-id="e177a-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e177a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e177a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e177a-117">-DefaultProfile</span></span>
<span data-ttu-id="e177a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e177a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e177a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e177a-119">-InputObject</span></span>
<span data-ttu-id="e177a-120">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="e177a-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e177a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e177a-121">-Name</span></span>
<span data-ttu-id="e177a-122">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="e177a-122">Name of the Table.</span></span>

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

### <span data-ttu-id="e177a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e177a-123">-PassThru</span></span>
<span data-ttu-id="e177a-124">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="e177a-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e177a-125">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="e177a-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e177a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e177a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e177a-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e177a-127">Name of resource group.</span></span>

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

### <span data-ttu-id="e177a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e177a-128">-WhatIf</span></span>
<span data-ttu-id="e177a-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e177a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e177a-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e177a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e177a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e177a-131">CommonParameters</span></span>
<span data-ttu-id="e177a-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e177a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e177a-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e177a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e177a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e177a-134">INPUTS</span></span>

### <span data-ttu-id="e177a-135">Microsoft.Azure.Commands.AzsDB.models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="e177a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="e177a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e177a-136">OUTPUTS</span></span>

### <span data-ttu-id="e177a-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="e177a-137">System.Void</span></span>

### <span data-ttu-id="e177a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e177a-138">System.Boolean</span></span>

## <span data-ttu-id="e177a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e177a-139">NOTES</span></span>

## <span data-ttu-id="e177a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e177a-140">RELATED LINKS</span></span>
