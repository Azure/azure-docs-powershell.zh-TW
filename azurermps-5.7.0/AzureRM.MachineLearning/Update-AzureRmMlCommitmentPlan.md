---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 0cda9ee6f6a93a43234835104130ea39782f36d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449331"
---
# <span data-ttu-id="c1b3c-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c1b3c-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="c1b3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b3c-103">更新現有 [提交方案] 資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1b3c-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b3c-106">更新現有的 [承諾計畫] 資源。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="c1b3c-107">請注意，「承諾方案」的大部分屬性都是不可變的，而且無法修改。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="c1b3c-108">可修改的內容包括 Sku (，讓您可以將承諾方案從一個 SKU 遷移到另一個) 與標記。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="c1b3c-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1b3c-109">EXAMPLES</span></span>

### <span data-ttu-id="c1b3c-110">範例1：更新承諾方案</span><span class="sxs-lookup"><span data-stu-id="c1b3c-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="c1b3c-111">參數</span><span class="sxs-lookup"><span data-stu-id="c1b3c-111">PARAMETERS</span></span>

### <span data-ttu-id="c1b3c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b3c-112">-DefaultProfile</span></span>
<span data-ttu-id="c1b3c-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c1b3c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c1b3c-114">-Force</span></span>
<span data-ttu-id="c1b3c-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1b3c-116">-Name</span></span>
<span data-ttu-id="c1b3c-117">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b3c-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1b3c-119">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c1b3c-120">-SkuCapacity</span></span>
<span data-ttu-id="c1b3c-121">更新 Azure ML 提交方案時所使用之 SKU 的容量。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c1b3c-122">-SkuName</span></span>
<span data-ttu-id="c1b3c-123">更新 Azure ML 提交方案時要使用之 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c1b3c-124">-SkuTier</span></span>
<span data-ttu-id="c1b3c-125">更新 Azure ML 提交方案時要使用的 SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1b3c-126">-Tag</span></span>
<span data-ttu-id="c1b3c-127">[提交方案] 資源的標記。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c1b3c-128">-Confirm</span></span>
<span data-ttu-id="c1b3c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b3c-130">-WhatIf</span></span>
<span data-ttu-id="c1b3c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1b3c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b3c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b3c-133">CommonParameters</span></span>
<span data-ttu-id="c1b3c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b3c-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b3c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c1b3c-136">INPUTS</span></span>

### <span data-ttu-id="c1b3c-137">所有</span><span class="sxs-lookup"><span data-stu-id="c1b3c-137">None</span></span>
<span data-ttu-id="c1b3c-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c1b3c-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1b3c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c1b3c-139">OUTPUTS</span></span>

### <span data-ttu-id="c1b3c-140">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="c1b3c-140">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="c1b3c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c1b3c-141">NOTES</span></span>
<span data-ttu-id="c1b3c-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="c1b3c-142">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c1b3c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1b3c-143">RELATED LINKS</span></span>
