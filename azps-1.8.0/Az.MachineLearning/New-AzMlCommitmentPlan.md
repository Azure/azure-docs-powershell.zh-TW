---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: b6edd4d40b3d976cfe93ca013fb9719d4ed69e9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786949"
---
# <span data-ttu-id="88d37-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="88d37-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="88d37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88d37-102">SYNOPSIS</span></span>
<span data-ttu-id="88d37-103">建立新的承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="88d37-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="88d37-104">句法</span><span class="sxs-lookup"><span data-stu-id="88d37-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d37-105">說明</span><span class="sxs-lookup"><span data-stu-id="88d37-105">DESCRIPTION</span></span>
<span data-ttu-id="88d37-106">在現有的資源群組中建立 Azure 機器學習承諾方案。</span><span class="sxs-lookup"><span data-stu-id="88d37-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="88d37-107">如果資源群組中存在具有相同名稱的承諾方案，該通話就會做為更新作業，而現有的承諾方案會覆寫。</span><span class="sxs-lookup"><span data-stu-id="88d37-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="88d37-108">示例</span><span class="sxs-lookup"><span data-stu-id="88d37-108">EXAMPLES</span></span>

### <span data-ttu-id="88d37-109">範例1：建立新的承約方案</span><span class="sxs-lookup"><span data-stu-id="88d37-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="88d37-110">在「MyResourceGroup」群組和美國中南部地區，建立名為「MyCommitmentPlanName」的新 Azure 機器學習承諾方案。</span><span class="sxs-lookup"><span data-stu-id="88d37-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="88d37-111">在這個範例中，使用 SKU DevTest/標準，這表示承諾方案提供的資源將由 DevTest/標準的限制來 definied。</span><span class="sxs-lookup"><span data-stu-id="88d37-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="88d37-112">這個範例中的 SkuCapacity 為1，表示計畫的成本將是 DevTest 的成本，而方案包含的資源將會是 DevTest 提供的資源。</span><span class="sxs-lookup"><span data-stu-id="88d37-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="88d37-113">參數</span><span class="sxs-lookup"><span data-stu-id="88d37-113">PARAMETERS</span></span>

### <span data-ttu-id="88d37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d37-114">-DefaultProfile</span></span>
<span data-ttu-id="88d37-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="88d37-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88d37-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88d37-116">-Force</span></span>
<span data-ttu-id="88d37-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="88d37-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="88d37-118">-位置</span><span class="sxs-lookup"><span data-stu-id="88d37-118">-Location</span></span>
<span data-ttu-id="88d37-119">Azure ML 提交方案的位置。</span><span class="sxs-lookup"><span data-stu-id="88d37-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="88d37-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="88d37-120">-Name</span></span>
<span data-ttu-id="88d37-121">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="88d37-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="88d37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d37-122">-ResourceGroupName</span></span>
<span data-ttu-id="88d37-123">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88d37-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="88d37-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="88d37-124">-SkuCapacity</span></span>
<span data-ttu-id="88d37-125">提供 Azure ML 提交方案時要使用的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="88d37-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="88d37-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="88d37-126">-SkuName</span></span>
<span data-ttu-id="88d37-127">提供 Azure ML 提交方案時要使用之 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="88d37-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="88d37-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="88d37-128">-SkuTier</span></span>
<span data-ttu-id="88d37-129">提供 Azure ML 提交方案時要使用的 SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="88d37-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="88d37-130">-確認</span><span class="sxs-lookup"><span data-stu-id="88d37-130">-Confirm</span></span>
<span data-ttu-id="88d37-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88d37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d37-132">-WhatIf</span></span>
<span data-ttu-id="88d37-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88d37-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d37-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88d37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d37-135">CommonParameters</span></span>
<span data-ttu-id="88d37-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88d37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d37-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88d37-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d37-138">輸入</span><span class="sxs-lookup"><span data-stu-id="88d37-138">INPUTS</span></span>

### <span data-ttu-id="88d37-139">所有</span><span class="sxs-lookup"><span data-stu-id="88d37-139">None</span></span>

## <span data-ttu-id="88d37-140">輸出</span><span class="sxs-lookup"><span data-stu-id="88d37-140">OUTPUTS</span></span>

### <span data-ttu-id="88d37-141">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="88d37-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="88d37-142">筆記</span><span class="sxs-lookup"><span data-stu-id="88d37-142">NOTES</span></span>
<span data-ttu-id="88d37-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="88d37-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="88d37-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="88d37-144">RELATED LINKS</span></span>
