---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 6bd60ced20e9c5b8ce9c3be01d419af55281aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902953"
---
# <span data-ttu-id="a70e2-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a70e2-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a70e2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a70e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a70e2-103">更新現有承諾計畫資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="a70e2-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="a70e2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a70e2-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70e2-105">描述</span><span class="sxs-lookup"><span data-stu-id="a70e2-105">DESCRIPTION</span></span>
<span data-ttu-id="a70e2-106">更新現有的承諾計畫資源。</span><span class="sxs-lookup"><span data-stu-id="a70e2-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="a70e2-107">請注意，承諾計畫大部分的屬性都是可更新的，而且無法修改。</span><span class="sxs-lookup"><span data-stu-id="a70e2-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="a70e2-108">可修改的屬性包括 SKU (允許您將承諾計畫從一個 SKU 遷移到另一個) 標記。</span><span class="sxs-lookup"><span data-stu-id="a70e2-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="a70e2-109">例子</span><span class="sxs-lookup"><span data-stu-id="a70e2-109">EXAMPLES</span></span>

### <span data-ttu-id="a70e2-110">範例 1：更新承諾計畫</span><span class="sxs-lookup"><span data-stu-id="a70e2-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="a70e2-111">參數</span><span class="sxs-lookup"><span data-stu-id="a70e2-111">PARAMETERS</span></span>

### <span data-ttu-id="a70e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70e2-112">-DefaultProfile</span></span>
<span data-ttu-id="a70e2-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a70e2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a70e2-114">-強制</span><span class="sxs-lookup"><span data-stu-id="a70e2-114">-Force</span></span>
<span data-ttu-id="a70e2-115">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="a70e2-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a70e2-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a70e2-116">-Name</span></span>
<span data-ttu-id="a70e2-117">Azure ML 承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a70e2-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a70e2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70e2-118">-ResourceGroupName</span></span>
<span data-ttu-id="a70e2-119">Azure ML 承諾計畫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a70e2-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a70e2-120">-Sku以</span><span class="sxs-lookup"><span data-stu-id="a70e2-120">-SkuCapacity</span></span>
<span data-ttu-id="a70e2-121">更新 Azure ML 承諾計畫時所使用 SKU 的容量。</span><span class="sxs-lookup"><span data-stu-id="a70e2-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a70e2-122">-SKUName</span><span class="sxs-lookup"><span data-stu-id="a70e2-122">-SkuName</span></span>
<span data-ttu-id="a70e2-123">更新 Azure ML 承諾計畫時要使用的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="a70e2-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a70e2-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a70e2-124">-SkuTier</span></span>
<span data-ttu-id="a70e2-125">更新 Azure ML 承諾計畫時要使用的 SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="a70e2-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a70e2-126">-標記</span><span class="sxs-lookup"><span data-stu-id="a70e2-126">-Tag</span></span>
<span data-ttu-id="a70e2-127">承諾計畫資源的標記。</span><span class="sxs-lookup"><span data-stu-id="a70e2-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="a70e2-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a70e2-128">-Confirm</span></span>
<span data-ttu-id="a70e2-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a70e2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70e2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70e2-130">-WhatIf</span></span>
<span data-ttu-id="a70e2-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a70e2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a70e2-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a70e2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a70e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70e2-133">CommonParameters</span></span>
<span data-ttu-id="a70e2-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a70e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70e2-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a70e2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70e2-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a70e2-136">INPUTS</span></span>

### <span data-ttu-id="a70e2-137">沒有</span><span class="sxs-lookup"><span data-stu-id="a70e2-137">None</span></span>

## <span data-ttu-id="a70e2-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a70e2-138">OUTPUTS</span></span>

### <span data-ttu-id="a70e2-139">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a70e2-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a70e2-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a70e2-140">NOTES</span></span>
<span data-ttu-id="a70e2-141">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="a70e2-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a70e2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a70e2-142">RELATED LINKS</span></span>
