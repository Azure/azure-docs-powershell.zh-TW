---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626605"
---
# <span data-ttu-id="46297-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="46297-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="46297-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46297-102">SYNOPSIS</span></span>
<span data-ttu-id="46297-103">刪除承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="46297-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46297-104">句法</span><span class="sxs-lookup"><span data-stu-id="46297-104">SYNTAX</span></span>

### <span data-ttu-id="46297-105">移除名稱和資源群組指定的 Azure ML 提交方案。</span><span class="sxs-lookup"><span data-stu-id="46297-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46297-106">移除指定為物件的 Azure ML 提交方案。</span><span class="sxs-lookup"><span data-stu-id="46297-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46297-107">說明</span><span class="sxs-lookup"><span data-stu-id="46297-107">DESCRIPTION</span></span>
<span data-ttu-id="46297-108">刪除 Azure 機器學習承諾方案。</span><span class="sxs-lookup"><span data-stu-id="46297-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="46297-109">請注意，必須刪除具有承諾關聯性的承諾方案。</span><span class="sxs-lookup"><span data-stu-id="46297-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="46297-110">承諾關聯只能透過其目標資源來刪除。</span><span class="sxs-lookup"><span data-stu-id="46297-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="46297-111">例如，如果您刪除 Azure 機器學習 web 服務，則會刪除將 web 服務與承諾方案相關聯的承諾關聯。</span><span class="sxs-lookup"><span data-stu-id="46297-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="46297-112">示例</span><span class="sxs-lookup"><span data-stu-id="46297-112">EXAMPLES</span></span>

### <span data-ttu-id="46297-113">--------------------------範例1：刪除承諾方案--------------------------</span><span class="sxs-lookup"><span data-stu-id="46297-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="46297-114">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="46297-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="46297-115">參數</span><span class="sxs-lookup"><span data-stu-id="46297-115">PARAMETERS</span></span>

### <span data-ttu-id="46297-116">-Force</span><span class="sxs-lookup"><span data-stu-id="46297-116">-Force</span></span>
<span data-ttu-id="46297-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="46297-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46297-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="46297-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="46297-119">機器學習 web 服務物件。</span><span class="sxs-lookup"><span data-stu-id="46297-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46297-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="46297-120">-Name</span></span>
<span data-ttu-id="46297-121">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="46297-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46297-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46297-122">-ResourceGroupName</span></span>
<span data-ttu-id="46297-123">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46297-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46297-124">-確認</span><span class="sxs-lookup"><span data-stu-id="46297-124">-Confirm</span></span>
<span data-ttu-id="46297-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46297-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46297-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46297-126">-WhatIf</span></span>
<span data-ttu-id="46297-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46297-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46297-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46297-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46297-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46297-129">-DefaultProfile</span></span>
<span data-ttu-id="46297-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46297-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46297-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46297-131">CommonParameters</span></span>
<span data-ttu-id="46297-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46297-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46297-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46297-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46297-134">輸入</span><span class="sxs-lookup"><span data-stu-id="46297-134">INPUTS</span></span>

### <span data-ttu-id="46297-135">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="46297-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="46297-136">輸出</span><span class="sxs-lookup"><span data-stu-id="46297-136">OUTPUTS</span></span>

### <span data-ttu-id="46297-137">所有</span><span class="sxs-lookup"><span data-stu-id="46297-137">None</span></span>

## <span data-ttu-id="46297-138">筆記</span><span class="sxs-lookup"><span data-stu-id="46297-138">NOTES</span></span>
<span data-ttu-id="46297-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="46297-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="46297-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="46297-140">RELATED LINKS</span></span>

