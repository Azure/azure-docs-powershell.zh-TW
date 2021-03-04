---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: 019ff5b50eb366947f82004d60ae38888532ac10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902013"
---
# <span data-ttu-id="f14a6-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="f14a6-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="f14a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f14a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f14a6-103">將承諾關聯從一個承諾計畫移至另一個承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="f14a6-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="f14a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="f14a6-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f14a6-105">描述</span><span class="sxs-lookup"><span data-stu-id="f14a6-105">DESCRIPTION</span></span>
<span data-ttu-id="f14a6-106">將承諾關聯資源從其父承諾計畫移至另一個承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="f14a6-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="f14a6-107">例子</span><span class="sxs-lookup"><span data-stu-id="f14a6-107">EXAMPLES</span></span>

### <span data-ttu-id="f14a6-108">範例 1：移動承諾關聯</span><span class="sxs-lookup"><span data-stu-id="f14a6-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="f14a6-109">參數</span><span class="sxs-lookup"><span data-stu-id="f14a6-109">PARAMETERS</span></span>

### <span data-ttu-id="f14a6-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="f14a6-110">-CommitmentPlanName</span></span>
<span data-ttu-id="f14a6-111">Azure ML 承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f14a6-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f14a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14a6-112">-DefaultProfile</span></span>
<span data-ttu-id="f14a6-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f14a6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f14a6-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="f14a6-114">-DestinationPlanId</span></span>
<span data-ttu-id="f14a6-115">目的地 Azure ML 承諾計畫的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f14a6-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f14a6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f14a6-116">-Name</span></span>
<span data-ttu-id="f14a6-117">Azure ML 承諾關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="f14a6-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="f14a6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14a6-118">-ResourceGroupName</span></span>
<span data-ttu-id="f14a6-119">Azure ML 承諾關聯之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f14a6-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="f14a6-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f14a6-120">-Confirm</span></span>
<span data-ttu-id="f14a6-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f14a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f14a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14a6-122">-WhatIf</span></span>
<span data-ttu-id="f14a6-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f14a6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f14a6-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f14a6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f14a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14a6-125">CommonParameters</span></span>
<span data-ttu-id="f14a6-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f14a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14a6-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f14a6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14a6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f14a6-128">INPUTS</span></span>

### <span data-ttu-id="f14a6-129">沒有</span><span class="sxs-lookup"><span data-stu-id="f14a6-129">None</span></span>

## <span data-ttu-id="f14a6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f14a6-130">OUTPUTS</span></span>

### <span data-ttu-id="f14a6-131">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f14a6-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f14a6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f14a6-132">NOTES</span></span>
<span data-ttu-id="f14a6-133">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="f14a6-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f14a6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f14a6-134">RELATED LINKS</span></span>
