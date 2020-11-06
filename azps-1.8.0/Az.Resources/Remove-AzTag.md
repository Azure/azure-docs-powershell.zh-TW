---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: f9afc10613024d99cfa6b03b260324b3e5d22586
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620771"
---
# <span data-ttu-id="c5ad5-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="c5ad5-101">Remove-AzTag</span></span>

## <span data-ttu-id="c5ad5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ad5-103">刪除預先定義的 Azure 標記或值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="c5ad5-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5ad5-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ad5-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5ad5-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ad5-106">**AzTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標記和值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="c5ad5-107">若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="c5ad5-108">根據預設， **移除-AzTag** 會刪除指定的標記及其所有值。您無法刪除目前已套用至資源或資源群組的標記或值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="c5ad5-109">在使用 **Remove-AzTag** 之前，請使用 Set-AzResourceGroup Cmdlet 的 *tag* 參數來刪除 [資源] 或 [資源] 群組中的標籤或值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="c5ad5-110">AzTag 是其中一部分的 Azure Tags 模組可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="c5ad5-111">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="c5ad5-112">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="c5ad5-113">示例</span><span class="sxs-lookup"><span data-stu-id="c5ad5-113">EXAMPLES</span></span>

### <span data-ttu-id="c5ad5-114">範例1：刪除預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="c5ad5-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="c5ad5-115">這個命令會刪除名為「部門」及其所有資源的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="c5ad5-116">如果已將標記套用至任何資源或資源群組，則命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="c5ad5-117">範例2：從預先定義的標記中刪除值</span><span class="sxs-lookup"><span data-stu-id="c5ad5-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="c5ad5-118">這個命令會從預先定義的 [部門] 標記刪除 HumanResources 值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="c5ad5-119">它不會刪除標記。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-119">It does not delete the tag.</span></span>
<span data-ttu-id="c5ad5-120">如果該值已套用至任何資源或資源群組，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="c5ad5-121">參數</span><span class="sxs-lookup"><span data-stu-id="c5ad5-121">PARAMETERS</span></span>

### <span data-ttu-id="c5ad5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ad5-122">-DefaultProfile</span></span>
<span data-ttu-id="c5ad5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5ad5-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5ad5-124">-Name</span></span>
<span data-ttu-id="c5ad5-125">指定要刪除的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="c5ad5-126">根據預設， **移除-AzTag** 會移除指定的標記及其所有值。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="c5ad5-127">若要刪除選取的值，但不刪除標記，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5ad5-128">-PassThru</span></span>
<span data-ttu-id="c5ad5-129">傳回代表已刪除的標籤或含有已刪除之值的結果標記的物件。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad5-130">-值</span><span class="sxs-lookup"><span data-stu-id="c5ad5-130">-Value</span></span>
<span data-ttu-id="c5ad5-131">從預先定義的標記中刪除指定的值，但不會刪除標籤。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c5ad5-132">-Confirm</span></span>
<span data-ttu-id="c5ad5-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ad5-134">-WhatIf</span></span>
<span data-ttu-id="c5ad5-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5ad5-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ad5-137">CommonParameters</span></span>
<span data-ttu-id="c5ad5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ad5-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ad5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c5ad5-140">INPUTS</span></span>

### <span data-ttu-id="c5ad5-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c5ad5-141">System.String</span></span>

### <span data-ttu-id="c5ad5-142">System.object []</span><span class="sxs-lookup"><span data-stu-id="c5ad5-142">System.String[]</span></span>

### <span data-ttu-id="c5ad5-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="c5ad5-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5ad5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c5ad5-144">OUTPUTS</span></span>

### <span data-ttu-id="c5ad5-145">PSTag 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="c5ad5-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="c5ad5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c5ad5-146">NOTES</span></span>

## <span data-ttu-id="c5ad5-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5ad5-147">RELATED LINKS</span></span>

[<span data-ttu-id="c5ad5-148">AzTag</span><span class="sxs-lookup"><span data-stu-id="c5ad5-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="c5ad5-149">新-AzTag</span><span class="sxs-lookup"><span data-stu-id="c5ad5-149">New-AzTag</span></span>](./New-AzTag.md)

