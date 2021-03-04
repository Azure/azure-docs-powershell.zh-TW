---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 2d3555d879d05e1235fb8713e75c9b27fca46b51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916761"
---
# <span data-ttu-id="996c6-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="996c6-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="996c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="996c6-102">SYNOPSIS</span></span>
<span data-ttu-id="996c6-103">{{ 填寫 <a0/a0><a1> </a0>的摘要資料 }}</span><span class="sxs-lookup"><span data-stu-id="996c6-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="996c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="996c6-104">SYNTAX</span></span>

### <span data-ttu-id="996c6-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="996c6-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996c6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="996c6-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996c6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="996c6-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="996c6-108">描述</span><span class="sxs-lookup"><span data-stu-id="996c6-108">DESCRIPTION</span></span>
<span data-ttu-id="996c6-109">{{ 填寫描述 }}</span><span class="sxs-lookup"><span data-stu-id="996c6-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="996c6-110">例子</span><span class="sxs-lookup"><span data-stu-id="996c6-110">EXAMPLES</span></span>

### <span data-ttu-id="996c6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="996c6-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="996c6-112">FailoverPolicies 更新為地區 1 為 FailoverPriority 1，region2 為 FailoverPriority 2，而 region3 為 FailoverPriority 3。</span><span class="sxs-lookup"><span data-stu-id="996c6-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="996c6-113">參數</span><span class="sxs-lookup"><span data-stu-id="996c6-113">PARAMETERS</span></span>

### <span data-ttu-id="996c6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="996c6-114">-AsJob</span></span>
<span data-ttu-id="996c6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="996c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="996c6-116">-確認</span><span class="sxs-lookup"><span data-stu-id="996c6-116">-Confirm</span></span>
<span data-ttu-id="996c6-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="996c6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="996c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996c6-118">-DefaultProfile</span></span>
<span data-ttu-id="996c6-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="996c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="996c6-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="996c6-120">-FailoverPolicy</span></span>
<span data-ttu-id="996c6-121">具有地區名稱的字串陣列，以容錯移轉優先順序排序。</span><span class="sxs-lookup"><span data-stu-id="996c6-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="996c6-122">例如 eastus、westus</span><span class="sxs-lookup"><span data-stu-id="996c6-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="996c6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="996c6-123">-InputObject</span></span>
<span data-ttu-id="996c6-124">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="996c6-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="996c6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="996c6-125">-Name</span></span>
<span data-ttu-id="996c6-126">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="996c6-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="996c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="996c6-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="996c6-128">Name of resource group.</span></span>

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

### <span data-ttu-id="996c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="996c6-129">-ResourceId</span></span>
<span data-ttu-id="996c6-130">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="996c6-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="996c6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="996c6-131">-WhatIf</span></span>
<span data-ttu-id="996c6-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="996c6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="996c6-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="996c6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="996c6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996c6-134">CommonParameters</span></span>
<span data-ttu-id="996c6-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="996c6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996c6-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="996c6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996c6-137">輸入</span><span class="sxs-lookup"><span data-stu-id="996c6-137">INPUTS</span></span>

### <span data-ttu-id="996c6-138">沒有</span><span class="sxs-lookup"><span data-stu-id="996c6-138">None</span></span>

## <span data-ttu-id="996c6-139">輸出</span><span class="sxs-lookup"><span data-stu-id="996c6-139">OUTPUTS</span></span>

### <span data-ttu-id="996c6-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="996c6-140">System.Void</span></span>

## <span data-ttu-id="996c6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="996c6-141">NOTES</span></span>

## <span data-ttu-id="996c6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="996c6-142">RELATED LINKS</span></span>
