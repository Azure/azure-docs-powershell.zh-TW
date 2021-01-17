---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449531"
---
# <span data-ttu-id="4b35d-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="4b35d-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="4b35d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b35d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b35d-103">刪除 CosmosDB 資料表。</span><span class="sxs-lookup"><span data-stu-id="4b35d-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="4b35d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b35d-104">SYNTAX</span></span>

### <span data-ttu-id="4b35d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b35d-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b35d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b35d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b35d-107">說明</span><span class="sxs-lookup"><span data-stu-id="4b35d-107">DESCRIPTION</span></span>
<span data-ttu-id="4b35d-108">**AzCosmosDBTable** Cmdlet 會刪除 CosmosDB 資料表。</span><span class="sxs-lookup"><span data-stu-id="4b35d-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="4b35d-109">示例</span><span class="sxs-lookup"><span data-stu-id="4b35d-109">EXAMPLES</span></span>

### <span data-ttu-id="4b35d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4b35d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="4b35d-111">如果刪除成功，則此 Cmdlet 會) 傳回類型為 bool (的物件。</span><span class="sxs-lookup"><span data-stu-id="4b35d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="4b35d-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b35d-112">PARAMETERS</span></span>

### <span data-ttu-id="4b35d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4b35d-113">-AccountName</span></span>
<span data-ttu-id="4b35d-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b35d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4b35d-115">-確認</span><span class="sxs-lookup"><span data-stu-id="4b35d-115">-Confirm</span></span>
<span data-ttu-id="4b35d-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b35d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b35d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b35d-117">-DefaultProfile</span></span>
<span data-ttu-id="4b35d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b35d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b35d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b35d-119">-InputObject</span></span>
<span data-ttu-id="4b35d-120">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="4b35d-120">Sql Database object.</span></span>

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

### <span data-ttu-id="4b35d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b35d-121">-Name</span></span>
<span data-ttu-id="4b35d-122">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b35d-122">Name of the Table.</span></span>

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

### <span data-ttu-id="4b35d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b35d-123">-PassThru</span></span>
<span data-ttu-id="4b35d-124">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="4b35d-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4b35d-125">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b35d-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4b35d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b35d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b35d-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b35d-127">Name of resource group.</span></span>

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

### <span data-ttu-id="4b35d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b35d-128">-WhatIf</span></span>
<span data-ttu-id="4b35d-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b35d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b35d-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b35d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b35d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b35d-131">CommonParameters</span></span>
<span data-ttu-id="4b35d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b35d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b35d-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4b35d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b35d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4b35d-134">INPUTS</span></span>

### <span data-ttu-id="4b35d-135">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="4b35d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="4b35d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4b35d-136">OUTPUTS</span></span>

### <span data-ttu-id="4b35d-137">System.void</span><span class="sxs-lookup"><span data-stu-id="4b35d-137">System.Void</span></span>

### <span data-ttu-id="4b35d-138">System.object</span><span class="sxs-lookup"><span data-stu-id="4b35d-138">System.Boolean</span></span>

## <span data-ttu-id="4b35d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4b35d-139">NOTES</span></span>

## <span data-ttu-id="4b35d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b35d-140">RELATED LINKS</span></span>
