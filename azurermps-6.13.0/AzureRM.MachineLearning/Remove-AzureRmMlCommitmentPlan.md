---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d14baa5382d5d9ffeeac8efd863a17cbad279865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453719"
---
# <span data-ttu-id="ec36e-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ec36e-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ec36e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec36e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec36e-103">刪除承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="ec36e-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec36e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec36e-104">SYNTAX</span></span>

### <span data-ttu-id="ec36e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec36e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec36e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ec36e-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec36e-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec36e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec36e-108">刪除 Azure 機器學習承諾方案。</span><span class="sxs-lookup"><span data-stu-id="ec36e-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="ec36e-109">請注意，必須刪除具有承諾關聯性的承諾方案。</span><span class="sxs-lookup"><span data-stu-id="ec36e-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="ec36e-110">承諾關聯只能透過其目標資源來刪除。</span><span class="sxs-lookup"><span data-stu-id="ec36e-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="ec36e-111">例如，如果您刪除 Azure 機器學習 web 服務，則會刪除將 web 服務與承諾方案相關聯的承諾關聯。</span><span class="sxs-lookup"><span data-stu-id="ec36e-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="ec36e-112">示例</span><span class="sxs-lookup"><span data-stu-id="ec36e-112">EXAMPLES</span></span>

### <span data-ttu-id="ec36e-113">範例1：刪除承諾方案</span><span class="sxs-lookup"><span data-stu-id="ec36e-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="ec36e-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec36e-114">PARAMETERS</span></span>

### <span data-ttu-id="ec36e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec36e-115">-DefaultProfile</span></span>
<span data-ttu-id="ec36e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ec36e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec36e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ec36e-117">-Force</span></span>
<span data-ttu-id="ec36e-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ec36e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ec36e-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ec36e-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="ec36e-120">機器學習 web 服務物件。</span><span class="sxs-lookup"><span data-stu-id="ec36e-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="ec36e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec36e-121">-Name</span></span>
<span data-ttu-id="ec36e-122">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec36e-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ec36e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec36e-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec36e-124">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec36e-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ec36e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ec36e-125">-Confirm</span></span>
<span data-ttu-id="ec36e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec36e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec36e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec36e-127">-WhatIf</span></span>
<span data-ttu-id="ec36e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec36e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec36e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec36e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec36e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec36e-130">CommonParameters</span></span>
<span data-ttu-id="ec36e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec36e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec36e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec36e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec36e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ec36e-133">INPUTS</span></span>

### <span data-ttu-id="ec36e-134">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="ec36e-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="ec36e-135">參數： MlCommitmentPlan (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ec36e-135">Parameters: MlCommitmentPlan (ByValue)</span></span>

## <span data-ttu-id="ec36e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ec36e-136">OUTPUTS</span></span>

### <span data-ttu-id="ec36e-137">System.void</span><span class="sxs-lookup"><span data-stu-id="ec36e-137">System.Void</span></span>

## <span data-ttu-id="ec36e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ec36e-138">NOTES</span></span>
<span data-ttu-id="ec36e-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="ec36e-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ec36e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec36e-140">RELATED LINKS</span></span>
