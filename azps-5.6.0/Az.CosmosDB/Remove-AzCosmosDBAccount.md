---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: 64d6f0bd604e8074d593f20a572768b54ced8a59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904118"
---
# <span data-ttu-id="36ff0-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="36ff0-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="36ff0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="36ff0-103">移除一個科克斯DB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="36ff0-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="36ff0-104">語法</span><span class="sxs-lookup"><span data-stu-id="36ff0-104">SYNTAX</span></span>

### <span data-ttu-id="36ff0-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="36ff0-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ff0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36ff0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ff0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36ff0-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ff0-108">描述</span><span class="sxs-lookup"><span data-stu-id="36ff0-108">DESCRIPTION</span></span>
<span data-ttu-id="36ff0-109">移除指定 ResourceGroup 中具有指定名稱的一個部科資料庫帳戶。</span><span class="sxs-lookup"><span data-stu-id="36ff0-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="36ff0-110">例子</span><span class="sxs-lookup"><span data-stu-id="36ff0-110">EXAMPLES</span></span>

### <span data-ttu-id="36ff0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="36ff0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="36ff0-112">在 ResourceGroup rg 中具有帳戶名稱 dbname 的帳戶會被刪除。</span><span class="sxs-lookup"><span data-stu-id="36ff0-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="36ff0-113">參數</span><span class="sxs-lookup"><span data-stu-id="36ff0-113">PARAMETERS</span></span>

### <span data-ttu-id="36ff0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36ff0-114">-AsJob</span></span>
<span data-ttu-id="36ff0-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36ff0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36ff0-116">-確認</span><span class="sxs-lookup"><span data-stu-id="36ff0-116">-Confirm</span></span>
<span data-ttu-id="36ff0-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="36ff0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ff0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ff0-118">-DefaultProfile</span></span>
<span data-ttu-id="36ff0-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36ff0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ff0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36ff0-120">-InputObject</span></span>
<span data-ttu-id="36ff0-121">資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="36ff0-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36ff0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="36ff0-122">-Name</span></span>
<span data-ttu-id="36ff0-123">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="36ff0-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36ff0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36ff0-124">-PassThru</span></span>
<span data-ttu-id="36ff0-125">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="36ff0-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="36ff0-126">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="36ff0-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="36ff0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ff0-127">-ResourceGroupName</span></span>
<span data-ttu-id="36ff0-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36ff0-128">Name of resource group.</span></span>

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

### <span data-ttu-id="36ff0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36ff0-129">-ResourceId</span></span>
<span data-ttu-id="36ff0-130">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="36ff0-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ff0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ff0-131">-WhatIf</span></span>
<span data-ttu-id="36ff0-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36ff0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ff0-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36ff0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ff0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ff0-134">CommonParameters</span></span>
<span data-ttu-id="36ff0-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36ff0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ff0-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36ff0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ff0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="36ff0-137">INPUTS</span></span>

### <span data-ttu-id="36ff0-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="36ff0-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="36ff0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="36ff0-139">OUTPUTS</span></span>

### <span data-ttu-id="36ff0-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="36ff0-140">System.Void</span></span>

## <span data-ttu-id="36ff0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="36ff0-141">NOTES</span></span>

## <span data-ttu-id="36ff0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="36ff0-142">RELATED LINKS</span></span>
