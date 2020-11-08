---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969639"
---
# <span data-ttu-id="1917f-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="1917f-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="1917f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1917f-102">SYNOPSIS</span></span>
<span data-ttu-id="1917f-103">將承諾關聯從一個承諾方案移至另一個。</span><span class="sxs-lookup"><span data-stu-id="1917f-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="1917f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1917f-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1917f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1917f-105">DESCRIPTION</span></span>
<span data-ttu-id="1917f-106">將承諾關聯資源從其父項承諾方案移至另一個承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="1917f-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="1917f-107">示例</span><span class="sxs-lookup"><span data-stu-id="1917f-107">EXAMPLES</span></span>

### <span data-ttu-id="1917f-108">範例1：移動承諾關聯</span><span class="sxs-lookup"><span data-stu-id="1917f-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="1917f-109">參數</span><span class="sxs-lookup"><span data-stu-id="1917f-109">PARAMETERS</span></span>

### <span data-ttu-id="1917f-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="1917f-110">-CommitmentPlanName</span></span>
<span data-ttu-id="1917f-111">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="1917f-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="1917f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1917f-112">-DefaultProfile</span></span>
<span data-ttu-id="1917f-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1917f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1917f-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="1917f-114">-DestinationPlanId</span></span>
<span data-ttu-id="1917f-115">目的地 Azure ML 提交方案的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1917f-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="1917f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1917f-116">-Name</span></span>
<span data-ttu-id="1917f-117">Azure ML 承諾協會的名稱。</span><span class="sxs-lookup"><span data-stu-id="1917f-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="1917f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1917f-118">-ResourceGroupName</span></span>
<span data-ttu-id="1917f-119">Azure ML 承諾協會之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1917f-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="1917f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="1917f-120">-Confirm</span></span>
<span data-ttu-id="1917f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1917f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1917f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1917f-122">-WhatIf</span></span>
<span data-ttu-id="1917f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1917f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1917f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1917f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1917f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1917f-125">CommonParameters</span></span>
<span data-ttu-id="1917f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1917f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1917f-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1917f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1917f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1917f-128">INPUTS</span></span>

### <span data-ttu-id="1917f-129">所有</span><span class="sxs-lookup"><span data-stu-id="1917f-129">None</span></span>

## <span data-ttu-id="1917f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1917f-130">OUTPUTS</span></span>

### <span data-ttu-id="1917f-131">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="1917f-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="1917f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1917f-132">NOTES</span></span>
<span data-ttu-id="1917f-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="1917f-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1917f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1917f-134">RELATED LINKS</span></span>
