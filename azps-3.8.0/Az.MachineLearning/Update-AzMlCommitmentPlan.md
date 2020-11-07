---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965672"
---
# <span data-ttu-id="32df0-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="32df0-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="32df0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32df0-102">SYNOPSIS</span></span>
<span data-ttu-id="32df0-103">更新現有 [提交方案] 資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="32df0-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="32df0-104">句法</span><span class="sxs-lookup"><span data-stu-id="32df0-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32df0-105">說明</span><span class="sxs-lookup"><span data-stu-id="32df0-105">DESCRIPTION</span></span>
<span data-ttu-id="32df0-106">更新現有的 [承諾計畫] 資源。</span><span class="sxs-lookup"><span data-stu-id="32df0-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="32df0-107">請注意，「承諾方案」的大部分屬性都是不可變的，而且無法修改。</span><span class="sxs-lookup"><span data-stu-id="32df0-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="32df0-108">可修改的內容包括 Sku (，讓您可以將承諾方案從一個 SKU 遷移到另一個) 與標記。</span><span class="sxs-lookup"><span data-stu-id="32df0-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="32df0-109">示例</span><span class="sxs-lookup"><span data-stu-id="32df0-109">EXAMPLES</span></span>

### <span data-ttu-id="32df0-110">範例1：更新承諾方案</span><span class="sxs-lookup"><span data-stu-id="32df0-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="32df0-111">參數</span><span class="sxs-lookup"><span data-stu-id="32df0-111">PARAMETERS</span></span>

### <span data-ttu-id="32df0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32df0-112">-DefaultProfile</span></span>
<span data-ttu-id="32df0-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="32df0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32df0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="32df0-114">-Force</span></span>
<span data-ttu-id="32df0-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="32df0-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="32df0-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="32df0-116">-Name</span></span>
<span data-ttu-id="32df0-117">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="32df0-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="32df0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32df0-118">-ResourceGroupName</span></span>
<span data-ttu-id="32df0-119">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32df0-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="32df0-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="32df0-120">-SkuCapacity</span></span>
<span data-ttu-id="32df0-121">更新 Azure ML 提交方案時所使用之 SKU 的容量。</span><span class="sxs-lookup"><span data-stu-id="32df0-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="32df0-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="32df0-122">-SkuName</span></span>
<span data-ttu-id="32df0-123">更新 Azure ML 提交方案時要使用之 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="32df0-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="32df0-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="32df0-124">-SkuTier</span></span>
<span data-ttu-id="32df0-125">更新 Azure ML 提交方案時要使用的 SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="32df0-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="32df0-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="32df0-126">-Tag</span></span>
<span data-ttu-id="32df0-127">[提交方案] 資源的標記。</span><span class="sxs-lookup"><span data-stu-id="32df0-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32df0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="32df0-128">-Confirm</span></span>
<span data-ttu-id="32df0-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32df0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32df0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32df0-130">-WhatIf</span></span>
<span data-ttu-id="32df0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32df0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32df0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32df0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32df0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32df0-133">CommonParameters</span></span>
<span data-ttu-id="32df0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32df0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32df0-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32df0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32df0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="32df0-136">INPUTS</span></span>

### <span data-ttu-id="32df0-137">所有</span><span class="sxs-lookup"><span data-stu-id="32df0-137">None</span></span>

## <span data-ttu-id="32df0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="32df0-138">OUTPUTS</span></span>

### <span data-ttu-id="32df0-139">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="32df0-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="32df0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="32df0-140">NOTES</span></span>
<span data-ttu-id="32df0-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="32df0-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="32df0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="32df0-142">RELATED LINKS</span></span>
