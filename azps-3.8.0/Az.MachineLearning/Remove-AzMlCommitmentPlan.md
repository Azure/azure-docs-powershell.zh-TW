---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965677"
---
# <span data-ttu-id="a566c-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a566c-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a566c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a566c-102">SYNOPSIS</span></span>
<span data-ttu-id="a566c-103">刪除承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="a566c-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="a566c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a566c-104">SYNTAX</span></span>

### <span data-ttu-id="a566c-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a566c-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a566c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a566c-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a566c-107">說明</span><span class="sxs-lookup"><span data-stu-id="a566c-107">DESCRIPTION</span></span>
<span data-ttu-id="a566c-108">刪除 Azure 機器學習承諾方案。</span><span class="sxs-lookup"><span data-stu-id="a566c-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="a566c-109">請注意，必須刪除具有承諾關聯性的承諾方案。</span><span class="sxs-lookup"><span data-stu-id="a566c-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="a566c-110">承諾關聯只能透過其目標資源來刪除。</span><span class="sxs-lookup"><span data-stu-id="a566c-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="a566c-111">例如，如果您刪除 Azure 機器學習 web 服務，則會刪除將 web 服務與承諾方案相關聯的承諾關聯。</span><span class="sxs-lookup"><span data-stu-id="a566c-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="a566c-112">示例</span><span class="sxs-lookup"><span data-stu-id="a566c-112">EXAMPLES</span></span>

### <span data-ttu-id="a566c-113">範例1：刪除承諾方案</span><span class="sxs-lookup"><span data-stu-id="a566c-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="a566c-114">參數</span><span class="sxs-lookup"><span data-stu-id="a566c-114">PARAMETERS</span></span>

### <span data-ttu-id="a566c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a566c-115">-DefaultProfile</span></span>
<span data-ttu-id="a566c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a566c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a566c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a566c-117">-Force</span></span>
<span data-ttu-id="a566c-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a566c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a566c-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a566c-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="a566c-120">機器學習 web 服務物件。</span><span class="sxs-lookup"><span data-stu-id="a566c-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a566c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a566c-121">-Name</span></span>
<span data-ttu-id="a566c-122">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a566c-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a566c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a566c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a566c-124">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a566c-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a566c-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a566c-125">-Confirm</span></span>
<span data-ttu-id="a566c-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a566c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a566c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a566c-127">-WhatIf</span></span>
<span data-ttu-id="a566c-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a566c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a566c-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a566c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a566c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a566c-130">CommonParameters</span></span>
<span data-ttu-id="a566c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a566c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a566c-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a566c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a566c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a566c-133">INPUTS</span></span>

### <span data-ttu-id="a566c-134">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="a566c-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a566c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a566c-135">OUTPUTS</span></span>

### <span data-ttu-id="a566c-136">System.void</span><span class="sxs-lookup"><span data-stu-id="a566c-136">System.Void</span></span>

## <span data-ttu-id="a566c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a566c-137">NOTES</span></span>
<span data-ttu-id="a566c-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="a566c-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a566c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a566c-139">RELATED LINKS</span></span>
