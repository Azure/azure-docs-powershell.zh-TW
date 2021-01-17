---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449532"
---
# <span data-ttu-id="b7eb9-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="b7eb9-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="b7eb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="b7eb9-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="b7eb9-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="b7eb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7eb9-104">SYNTAX</span></span>

### <span data-ttu-id="b7eb9-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b7eb9-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7eb9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7eb9-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7eb9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7eb9-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7eb9-108">說明</span><span class="sxs-lookup"><span data-stu-id="b7eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="b7eb9-109">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="b7eb9-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="b7eb9-110">示例</span><span class="sxs-lookup"><span data-stu-id="b7eb9-110">EXAMPLES</span></span>

### <span data-ttu-id="b7eb9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b7eb9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="b7eb9-112">FailoverPolicies 更新為 FailoverPriority 1 的 region1，region2 為 FailoverPriority 2，region3 為 FailoverPriority 3。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="b7eb9-113">參數</span><span class="sxs-lookup"><span data-stu-id="b7eb9-113">PARAMETERS</span></span>

### <span data-ttu-id="b7eb9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7eb9-114">-AsJob</span></span>
<span data-ttu-id="b7eb9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7eb9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7eb9-116">-確認</span><span class="sxs-lookup"><span data-stu-id="b7eb9-116">-Confirm</span></span>
<span data-ttu-id="b7eb9-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7eb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7eb9-118">-DefaultProfile</span></span>
<span data-ttu-id="b7eb9-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7eb9-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b7eb9-120">-FailoverPolicy</span></span>
<span data-ttu-id="b7eb9-121">具有地區名稱的字串陣列，依容錯移轉優先順序排序。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="b7eb9-122">例如 eastus、westus</span><span class="sxs-lookup"><span data-stu-id="b7eb9-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7eb9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7eb9-123">-InputObject</span></span>
<span data-ttu-id="b7eb9-124">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="b7eb9-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b7eb9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7eb9-125">-Name</span></span>
<span data-ttu-id="b7eb9-126">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b7eb9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7eb9-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7eb9-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b7eb9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7eb9-129">-ResourceId</span></span>
<span data-ttu-id="b7eb9-130">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b7eb9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7eb9-131">-WhatIf</span></span>
<span data-ttu-id="b7eb9-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7eb9-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7eb9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7eb9-134">CommonParameters</span></span>
<span data-ttu-id="b7eb9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7eb9-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b7eb9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7eb9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b7eb9-137">INPUTS</span></span>

### <span data-ttu-id="b7eb9-138">所有</span><span class="sxs-lookup"><span data-stu-id="b7eb9-138">None</span></span>

## <span data-ttu-id="b7eb9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b7eb9-139">OUTPUTS</span></span>

### <span data-ttu-id="b7eb9-140">System.void</span><span class="sxs-lookup"><span data-stu-id="b7eb9-140">System.Void</span></span>

## <span data-ttu-id="b7eb9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b7eb9-141">NOTES</span></span>

## <span data-ttu-id="b7eb9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7eb9-142">RELATED LINKS</span></span>
