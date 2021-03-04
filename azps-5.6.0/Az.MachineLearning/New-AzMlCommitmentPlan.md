---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: f5386f3c971159f2a33353efeb380164447ee295
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907102"
---
# <span data-ttu-id="a0d98-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a0d98-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a0d98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a0d98-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d98-103">建立新的承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="a0d98-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="a0d98-104">語法</span><span class="sxs-lookup"><span data-stu-id="a0d98-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d98-105">描述</span><span class="sxs-lookup"><span data-stu-id="a0d98-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d98-106">在現有的資源群組中建立 Azure 機器學習承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="a0d98-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="a0d98-107">如果資源群組中已存在相同名稱的承諾計畫，則呼叫會做為更新作業，並覆蓋現有的承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="a0d98-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="a0d98-108">例子</span><span class="sxs-lookup"><span data-stu-id="a0d98-108">EXAMPLES</span></span>

### <span data-ttu-id="a0d98-109">範例 1：建立新承諾計畫</span><span class="sxs-lookup"><span data-stu-id="a0d98-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="a0d98-110">在「MyResourceGroup」群組中，以及美國中南部地區，建立名為「MyCommitmentPlanName」的新 Azure 機器學習承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="a0d98-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="a0d98-111">在此範例中，使用 SKU DevTest/Standard，表示承諾計畫提供的資源會以 DevTest/Standard 的限制定義。</span><span class="sxs-lookup"><span data-stu-id="a0d98-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="a0d98-112">此範例中的 Sku只為 1，表示規劃成本是 DevTest 成本的 1 倍，而計畫包含的資源是 DevTest 提供的 1 倍。</span><span class="sxs-lookup"><span data-stu-id="a0d98-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="a0d98-113">參數</span><span class="sxs-lookup"><span data-stu-id="a0d98-113">PARAMETERS</span></span>

### <span data-ttu-id="a0d98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d98-114">-DefaultProfile</span></span>
<span data-ttu-id="a0d98-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a0d98-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d98-116">-強制</span><span class="sxs-lookup"><span data-stu-id="a0d98-116">-Force</span></span>
<span data-ttu-id="a0d98-117">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="a0d98-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0d98-118">-位置</span><span class="sxs-lookup"><span data-stu-id="a0d98-118">-Location</span></span>
<span data-ttu-id="a0d98-119">Azure ML 承諾計畫的位置。</span><span class="sxs-lookup"><span data-stu-id="a0d98-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a0d98-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0d98-120">-Name</span></span>
<span data-ttu-id="a0d98-121">Azure ML 承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0d98-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a0d98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d98-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0d98-123">Azure ML 承諾計畫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a0d98-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a0d98-124">-Sku以</span><span class="sxs-lookup"><span data-stu-id="a0d98-124">-SkuCapacity</span></span>
<span data-ttu-id="a0d98-125">在提供 Azure ML 承諾計畫時所使用 SKU 的容量。</span><span class="sxs-lookup"><span data-stu-id="a0d98-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d98-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="a0d98-126">-SkuName</span></span>
<span data-ttu-id="a0d98-127">用於提供 Azure ML 承諾計畫之 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0d98-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a0d98-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a0d98-128">-SkuTier</span></span>
<span data-ttu-id="a0d98-129">在配置 Azure ML 承諾計畫時所使用之 SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="a0d98-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a0d98-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a0d98-130">-Confirm</span></span>
<span data-ttu-id="a0d98-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a0d98-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d98-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d98-132">-WhatIf</span></span>
<span data-ttu-id="a0d98-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0d98-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d98-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0d98-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d98-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d98-135">CommonParameters</span></span>
<span data-ttu-id="a0d98-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a0d98-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d98-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a0d98-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d98-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a0d98-138">INPUTS</span></span>

### <span data-ttu-id="a0d98-139">沒有</span><span class="sxs-lookup"><span data-stu-id="a0d98-139">None</span></span>

## <span data-ttu-id="a0d98-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a0d98-140">OUTPUTS</span></span>

### <span data-ttu-id="a0d98-141">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a0d98-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a0d98-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a0d98-142">NOTES</span></span>
<span data-ttu-id="a0d98-143">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="a0d98-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a0d98-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0d98-144">RELATED LINKS</span></span>
