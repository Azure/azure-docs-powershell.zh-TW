---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449543"
---
# <span data-ttu-id="5aff0-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="5aff0-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="5aff0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5aff0-102">SYNOPSIS</span></span>
<span data-ttu-id="5aff0-103">移除 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="5aff0-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="5aff0-104">句法</span><span class="sxs-lookup"><span data-stu-id="5aff0-104">SYNTAX</span></span>

### <span data-ttu-id="5aff0-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5aff0-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aff0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aff0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aff0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aff0-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aff0-108">說明</span><span class="sxs-lookup"><span data-stu-id="5aff0-108">DESCRIPTION</span></span>
<span data-ttu-id="5aff0-109">在指定的 ResourceGroup 中移除具有指定名稱的 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="5aff0-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="5aff0-110">示例</span><span class="sxs-lookup"><span data-stu-id="5aff0-110">EXAMPLES</span></span>

### <span data-ttu-id="5aff0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5aff0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="5aff0-112">已刪除 ResourceGroup rg 中帳戶名稱 dbname 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="5aff0-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="5aff0-113">參數</span><span class="sxs-lookup"><span data-stu-id="5aff0-113">PARAMETERS</span></span>

### <span data-ttu-id="5aff0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aff0-114">-AsJob</span></span>
<span data-ttu-id="5aff0-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5aff0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5aff0-116">-確認</span><span class="sxs-lookup"><span data-stu-id="5aff0-116">-Confirm</span></span>
<span data-ttu-id="5aff0-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5aff0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aff0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aff0-118">-DefaultProfile</span></span>
<span data-ttu-id="5aff0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5aff0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aff0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aff0-120">-InputObject</span></span>
<span data-ttu-id="5aff0-121">資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5aff0-121">The Database Account object</span></span>

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

### <span data-ttu-id="5aff0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5aff0-122">-Name</span></span>
<span data-ttu-id="5aff0-123">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5aff0-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5aff0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5aff0-124">-PassThru</span></span>
<span data-ttu-id="5aff0-125">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="5aff0-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5aff0-126">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5aff0-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5aff0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aff0-127">-ResourceGroupName</span></span>
<span data-ttu-id="5aff0-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5aff0-128">Name of resource group.</span></span>

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

### <span data-ttu-id="5aff0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aff0-129">-ResourceId</span></span>
<span data-ttu-id="5aff0-130">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="5aff0-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="5aff0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aff0-131">-WhatIf</span></span>
<span data-ttu-id="5aff0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5aff0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aff0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5aff0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aff0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aff0-134">CommonParameters</span></span>
<span data-ttu-id="5aff0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5aff0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aff0-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5aff0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aff0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5aff0-137">INPUTS</span></span>

### <span data-ttu-id="5aff0-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5aff0-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5aff0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5aff0-139">OUTPUTS</span></span>

### <span data-ttu-id="5aff0-140">System.void</span><span class="sxs-lookup"><span data-stu-id="5aff0-140">System.Void</span></span>

## <span data-ttu-id="5aff0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5aff0-141">NOTES</span></span>

## <span data-ttu-id="5aff0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5aff0-142">RELATED LINKS</span></span>
