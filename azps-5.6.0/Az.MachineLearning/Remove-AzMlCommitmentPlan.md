---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 287db082c5cbe842b0a92b124870effb77068912
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904061"
---
# <span data-ttu-id="933fd-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="933fd-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="933fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="933fd-102">SYNOPSIS</span></span>
<span data-ttu-id="933fd-103">刪除承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="933fd-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="933fd-104">語法</span><span class="sxs-lookup"><span data-stu-id="933fd-104">SYNTAX</span></span>

### <span data-ttu-id="933fd-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="933fd-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="933fd-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="933fd-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933fd-107">描述</span><span class="sxs-lookup"><span data-stu-id="933fd-107">DESCRIPTION</span></span>
<span data-ttu-id="933fd-108">刪除 Azure 機器學習承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="933fd-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="933fd-109">請注意，具有承諾關聯的承諾計畫無法刪除。</span><span class="sxs-lookup"><span data-stu-id="933fd-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="933fd-110">承諾關聯只能由目標資源刪除。</span><span class="sxs-lookup"><span data-stu-id="933fd-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="933fd-111">例如，如果您刪除 Azure 機器學習 Web 服務，也會刪除將 Web 服務與承諾計畫建立關聯的承諾關聯。</span><span class="sxs-lookup"><span data-stu-id="933fd-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="933fd-112">例子</span><span class="sxs-lookup"><span data-stu-id="933fd-112">EXAMPLES</span></span>

### <span data-ttu-id="933fd-113">範例 1：刪除承諾計畫</span><span class="sxs-lookup"><span data-stu-id="933fd-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="933fd-114">參數</span><span class="sxs-lookup"><span data-stu-id="933fd-114">PARAMETERS</span></span>

### <span data-ttu-id="933fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933fd-115">-DefaultProfile</span></span>
<span data-ttu-id="933fd-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="933fd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="933fd-117">-強制</span><span class="sxs-lookup"><span data-stu-id="933fd-117">-Force</span></span>
<span data-ttu-id="933fd-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="933fd-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="933fd-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="933fd-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="933fd-120">機器學習 Web 服務物件。</span><span class="sxs-lookup"><span data-stu-id="933fd-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="933fd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="933fd-121">-Name</span></span>
<span data-ttu-id="933fd-122">Azure ML 承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="933fd-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="933fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="933fd-124">Azure ML 承諾計畫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="933fd-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="933fd-125">-確認</span><span class="sxs-lookup"><span data-stu-id="933fd-125">-Confirm</span></span>
<span data-ttu-id="933fd-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="933fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933fd-127">-WhatIf</span></span>
<span data-ttu-id="933fd-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="933fd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="933fd-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="933fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933fd-130">CommonParameters</span></span>
<span data-ttu-id="933fd-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="933fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933fd-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="933fd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933fd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="933fd-133">INPUTS</span></span>

### <span data-ttu-id="933fd-134">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="933fd-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="933fd-135">輸出</span><span class="sxs-lookup"><span data-stu-id="933fd-135">OUTPUTS</span></span>

### <span data-ttu-id="933fd-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="933fd-136">System.Void</span></span>

## <span data-ttu-id="933fd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="933fd-137">NOTES</span></span>
<span data-ttu-id="933fd-138">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="933fd-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="933fd-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="933fd-139">RELATED LINKS</span></span>
