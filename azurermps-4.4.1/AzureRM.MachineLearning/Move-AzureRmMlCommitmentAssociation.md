---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456544"
---
# <span data-ttu-id="dd995-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="dd995-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="dd995-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd995-102">SYNOPSIS</span></span>
<span data-ttu-id="dd995-103">將承諾關聯從一個承諾方案移至另一個。</span><span class="sxs-lookup"><span data-stu-id="dd995-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd995-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd995-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd995-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd995-105">DESCRIPTION</span></span>
<span data-ttu-id="dd995-106">將承諾關聯資源從其父項承諾方案移至另一個承諾計畫。</span><span class="sxs-lookup"><span data-stu-id="dd995-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="dd995-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd995-107">EXAMPLES</span></span>

### <span data-ttu-id="dd995-108">--------------------------範例1：移動承諾關聯--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd995-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="dd995-109">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd995-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="dd995-110">參數</span><span class="sxs-lookup"><span data-stu-id="dd995-110">PARAMETERS</span></span>

### <span data-ttu-id="dd995-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="dd995-111">-CommitmentPlanName</span></span>
<span data-ttu-id="dd995-112">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd995-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd995-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="dd995-113">-DestinationPlanId</span></span>
<span data-ttu-id="dd995-114">目的地 Azure ML 提交方案的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd995-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dd995-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd995-115">-Name</span></span>
<span data-ttu-id="dd995-116">Azure ML 承諾協會的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd995-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="dd995-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd995-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd995-118">Azure ML 承諾協會之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd995-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="dd995-119">-確認</span><span class="sxs-lookup"><span data-stu-id="dd995-119">-Confirm</span></span>
<span data-ttu-id="dd995-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd995-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd995-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd995-121">-WhatIf</span></span>
<span data-ttu-id="dd995-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd995-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd995-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd995-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd995-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd995-124">-DefaultProfile</span></span>
<span data-ttu-id="dd995-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd995-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd995-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd995-126">CommonParameters</span></span>
<span data-ttu-id="dd995-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd995-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd995-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd995-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd995-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dd995-129">INPUTS</span></span>

## <span data-ttu-id="dd995-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dd995-130">OUTPUTS</span></span>

### <span data-ttu-id="dd995-131">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="dd995-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="dd995-132">CommitmentPlan []. MachineLearning [CommitmentPlans]</span><span class="sxs-lookup"><span data-stu-id="dd995-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="dd995-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dd995-133">NOTES</span></span>
<span data-ttu-id="dd995-134">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="dd995-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dd995-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd995-135">RELATED LINKS</span></span>

