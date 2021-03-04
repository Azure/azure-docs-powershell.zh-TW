---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 465c4b366990bb69d437fbdbe51fe2c5f4316758
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906178"
---
# <span data-ttu-id="c541f-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="c541f-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="c541f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c541f-102">SYNOPSIS</span></span>
<span data-ttu-id="c541f-103">建立函數應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="c541f-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="c541f-104">語法</span><span class="sxs-lookup"><span data-stu-id="c541f-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c541f-105">描述</span><span class="sxs-lookup"><span data-stu-id="c541f-105">DESCRIPTION</span></span>
<span data-ttu-id="c541f-106">建立函數應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="c541f-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="c541f-107">例子</span><span class="sxs-lookup"><span data-stu-id="c541f-107">EXAMPLES</span></span>

### <span data-ttu-id="c541f-108">範例 1：在西歐使用 out out 功能建立 Windows Premium 應用程式方案，最多 10 個實例。</span><span class="sxs-lookup"><span data-stu-id="c541f-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="c541f-109">此命令在西歐建立 Windows 進位版應用程式方案，其外發功能最多 10 個實例。</span><span class="sxs-lookup"><span data-stu-id="c541f-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="c541f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c541f-110">PARAMETERS</span></span>

### <span data-ttu-id="c541f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c541f-111">-AsJob</span></span>
<span data-ttu-id="c541f-112">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="c541f-112">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c541f-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-114">-位置</span><span class="sxs-lookup"><span data-stu-id="c541f-114">-Location</span></span>
<span data-ttu-id="c541f-115">消費方案的位置。</span><span class="sxs-lookup"><span data-stu-id="c541f-115">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c541f-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="c541f-117">應用程式服務方案的員工人數上限。</span><span class="sxs-lookup"><span data-stu-id="c541f-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c541f-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="c541f-119">應用程式服務方案的最小工作人員人數。</span><span class="sxs-lookup"><span data-stu-id="c541f-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c541f-120">-Name</span></span>
<span data-ttu-id="c541f-121">應用程式服務方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="c541f-121">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c541f-122">-NoWait</span></span>
<span data-ttu-id="c541f-123">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="c541f-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c541f-124">-ResourceGroupName</span></span>
<span data-ttu-id="c541f-125">資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c541f-125">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c541f-126">-Sku</span></span>
<span data-ttu-id="c541f-127">方案 SKU。</span><span class="sxs-lookup"><span data-stu-id="c541f-127">The plan sku.</span></span>
<span data-ttu-id="c541f-128">有效的輸入為：EP1、EP2、EP3</span><span class="sxs-lookup"><span data-stu-id="c541f-128">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c541f-129">-SubscriptionId</span></span>
<span data-ttu-id="c541f-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c541f-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-131">-標記</span><span class="sxs-lookup"><span data-stu-id="c541f-131">-Tag</span></span>
<span data-ttu-id="c541f-132">資源標記。</span><span class="sxs-lookup"><span data-stu-id="c541f-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="c541f-133">-WorkerType</span></span>
<span data-ttu-id="c541f-134">計畫的員工類型。</span><span class="sxs-lookup"><span data-stu-id="c541f-134">The worker type for the plan.</span></span>
<span data-ttu-id="c541f-135">有效的輸入為：Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="c541f-135">Valid inputs are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c541f-136">-Confirm</span></span>
<span data-ttu-id="c541f-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c541f-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c541f-138">-WhatIf</span></span>
<span data-ttu-id="c541f-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c541f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c541f-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c541f-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c541f-141">CommonParameters</span></span>
<span data-ttu-id="c541f-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c541f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c541f-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c541f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c541f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c541f-144">INPUTS</span></span>

## <span data-ttu-id="c541f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c541f-145">OUTPUTS</span></span>

### <span data-ttu-id="c541f-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c541f-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="c541f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c541f-147">NOTES</span></span>

<span data-ttu-id="c541f-148">別名</span><span class="sxs-lookup"><span data-stu-id="c541f-148">ALIASES</span></span>

## <span data-ttu-id="c541f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c541f-149">RELATED LINKS</span></span>

