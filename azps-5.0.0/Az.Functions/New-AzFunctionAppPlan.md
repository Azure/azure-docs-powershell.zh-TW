---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136866"
---
# <span data-ttu-id="0d595-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="0d595-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="0d595-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d595-102">SYNOPSIS</span></span>
<span data-ttu-id="0d595-103">建立函數 app 服務方案。</span><span class="sxs-lookup"><span data-stu-id="0d595-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="0d595-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d595-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d595-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d595-105">DESCRIPTION</span></span>
<span data-ttu-id="0d595-106">建立函數 app 服務方案。</span><span class="sxs-lookup"><span data-stu-id="0d595-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="0d595-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d595-107">EXAMPLES</span></span>

### <span data-ttu-id="0d595-108">範例1：在西歐建立 Windows premium 應用程式方案，並提供最多10個實例的突髮式功能。</span><span class="sxs-lookup"><span data-stu-id="0d595-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="0d595-109">這個命令會在西歐建立 Windows premium 應用程式方案，最多可達10個實例。</span><span class="sxs-lookup"><span data-stu-id="0d595-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="0d595-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d595-110">PARAMETERS</span></span>

### <span data-ttu-id="0d595-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d595-111">-AsJob</span></span>
<span data-ttu-id="0d595-112">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="0d595-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="0d595-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d595-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="0d595-114">-位置</span><span class="sxs-lookup"><span data-stu-id="0d595-114">-Location</span></span>
<span data-ttu-id="0d595-115">消耗量方案的位置。</span><span class="sxs-lookup"><span data-stu-id="0d595-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="0d595-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0d595-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="0d595-117">App 服務方案的工作人數上限。</span><span class="sxs-lookup"><span data-stu-id="0d595-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="0d595-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0d595-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="0d595-119">App 服務方案的工作人數最小值。</span><span class="sxs-lookup"><span data-stu-id="0d595-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="0d595-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d595-120">-Name</span></span>
<span data-ttu-id="0d595-121">App 服務方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d595-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="0d595-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0d595-122">-NoWait</span></span>
<span data-ttu-id="0d595-123">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="0d595-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0d595-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d595-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d595-125">資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d595-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="0d595-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="0d595-126">-Sku</span></span>
<span data-ttu-id="0d595-127">方案 sku。</span><span class="sxs-lookup"><span data-stu-id="0d595-127">The plan sku.</span></span>
<span data-ttu-id="0d595-128">有效的輸入為： EP1、EP2、EP3</span><span class="sxs-lookup"><span data-stu-id="0d595-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="0d595-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d595-129">-SubscriptionId</span></span>
<span data-ttu-id="0d595-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0d595-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="0d595-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d595-131">-Tag</span></span>
<span data-ttu-id="0d595-132">資源標記。</span><span class="sxs-lookup"><span data-stu-id="0d595-132">Resource tags.</span></span>

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

### <span data-ttu-id="0d595-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="0d595-133">-WorkerType</span></span>
<span data-ttu-id="0d595-134">方案的工作人員類型。</span><span class="sxs-lookup"><span data-stu-id="0d595-134">The worker type for the plan.</span></span>
<span data-ttu-id="0d595-135">有效的輸入為： Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="0d595-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="0d595-136">-確認</span><span class="sxs-lookup"><span data-stu-id="0d595-136">-Confirm</span></span>
<span data-ttu-id="0d595-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d595-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d595-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d595-138">-WhatIf</span></span>
<span data-ttu-id="0d595-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d595-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d595-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d595-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d595-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d595-141">CommonParameters</span></span>
<span data-ttu-id="0d595-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d595-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d595-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d595-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d595-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0d595-144">INPUTS</span></span>

## <span data-ttu-id="0d595-145">輸出</span><span class="sxs-lookup"><span data-stu-id="0d595-145">OUTPUTS</span></span>

### <span data-ttu-id="0d595-146">IAppServicePlan 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="0d595-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0d595-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0d595-147">NOTES</span></span>

<span data-ttu-id="0d595-148">別名</span><span class="sxs-lookup"><span data-stu-id="0d595-148">ALIASES</span></span>

## <span data-ttu-id="0d595-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d595-149">RELATED LINKS</span></span>
