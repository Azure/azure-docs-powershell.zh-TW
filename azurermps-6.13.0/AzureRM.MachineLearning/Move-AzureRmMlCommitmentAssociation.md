---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 25a77e0e34e741273618ab4c434168b796595737
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449764"
---
# <span data-ttu-id="7bab9-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="7bab9-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="7bab9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bab9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bab9-103">將承諾關聯從一個承諾方案移至另一個。</span><span class="sxs-lookup"><span data-stu-id="7bab9-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bab9-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bab9-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bab9-105">說明</span><span class="sxs-lookup"><span data-stu-id="7bab9-105">DESCRIPTION</span></span>
<span data-ttu-id="7bab9-106">將承諾關聯資源從其父項承諾方案移至另一個承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="7bab9-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="7bab9-107">示例</span><span class="sxs-lookup"><span data-stu-id="7bab9-107">EXAMPLES</span></span>

### <span data-ttu-id="7bab9-108">範例1：移動承諾關聯</span><span class="sxs-lookup"><span data-stu-id="7bab9-108">Example 1: Move a commitment association</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="7bab9-109">參數</span><span class="sxs-lookup"><span data-stu-id="7bab9-109">PARAMETERS</span></span>

### <span data-ttu-id="7bab9-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="7bab9-110">-CommitmentPlanName</span></span>
<span data-ttu-id="7bab9-111">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bab9-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7bab9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bab9-112">-DefaultProfile</span></span>
<span data-ttu-id="7bab9-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7bab9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bab9-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="7bab9-114">-DestinationPlanId</span></span>
<span data-ttu-id="7bab9-115">目的地 Azure ML 提交方案的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bab9-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7bab9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bab9-116">-Name</span></span>
<span data-ttu-id="7bab9-117">Azure ML 承諾協會的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bab9-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7bab9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bab9-118">-ResourceGroupName</span></span>
<span data-ttu-id="7bab9-119">Azure ML 承諾協會之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bab9-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7bab9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="7bab9-120">-Confirm</span></span>
<span data-ttu-id="7bab9-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bab9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bab9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bab9-122">-WhatIf</span></span>
<span data-ttu-id="7bab9-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bab9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bab9-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bab9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bab9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bab9-125">CommonParameters</span></span>
<span data-ttu-id="7bab9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bab9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bab9-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7bab9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bab9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7bab9-128">INPUTS</span></span>

### <span data-ttu-id="7bab9-129">所有</span><span class="sxs-lookup"><span data-stu-id="7bab9-129">None</span></span>

## <span data-ttu-id="7bab9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7bab9-130">OUTPUTS</span></span>

### <span data-ttu-id="7bab9-131">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="7bab9-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7bab9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7bab9-132">NOTES</span></span>
<span data-ttu-id="7bab9-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="7bab9-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7bab9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bab9-134">RELATED LINKS</span></span>
