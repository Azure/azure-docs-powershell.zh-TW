---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625646"
---
# <span data-ttu-id="793e9-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="793e9-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="793e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="793e9-102">SYNOPSIS</span></span>
<span data-ttu-id="793e9-103">刪除預先定義的 Azure 標記或值。</span><span class="sxs-lookup"><span data-stu-id="793e9-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="793e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="793e9-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="793e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="793e9-105">DESCRIPTION</span></span>
<span data-ttu-id="793e9-106">**AzureRmTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標記和值。</span><span class="sxs-lookup"><span data-stu-id="793e9-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="793e9-107">若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="793e9-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="793e9-108">根據預設， **移除-AzureRmTag** 會刪除指定的標記及其所有值。您無法刪除目前已套用至資源或資源群組的標記或值。</span><span class="sxs-lookup"><span data-stu-id="793e9-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="793e9-109">在使用 **Remove-AzureRmTag** 之前，請使用 Set-AzureRMResourceGroup Cmdlet 的 *tag* 參數來刪除 [資源] 或 [資源] 群組中的標籤或值。</span><span class="sxs-lookup"><span data-stu-id="793e9-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="793e9-110">AzureRmTag 是其中一部分的 Azure Tags 模組可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="793e9-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="793e9-111">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="793e9-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="793e9-112">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="793e9-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="793e9-113">如果訂閱包含任何預先定義的標記，您就無法將未定義的標籤或值套用到訂閱中的任何資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="793e9-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="793e9-114">示例</span><span class="sxs-lookup"><span data-stu-id="793e9-114">EXAMPLES</span></span>

### <span data-ttu-id="793e9-115">範例1：刪除預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="793e9-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="793e9-116">這個命令會刪除名為「部門」及其所有資源的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="793e9-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="793e9-117">如果已將標記套用至任何資源或資源群組，則命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="793e9-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="793e9-118">範例2：從預先定義的標記中刪除值</span><span class="sxs-lookup"><span data-stu-id="793e9-118">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="793e9-119">這個命令會從預先定義的 [部門] 標記刪除 HumanResources 值。</span><span class="sxs-lookup"><span data-stu-id="793e9-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="793e9-120">它不會刪除標記。</span><span class="sxs-lookup"><span data-stu-id="793e9-120">It does not delete the tag.</span></span>
<span data-ttu-id="793e9-121">如果該值已套用至任何資源或資源群組，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="793e9-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="793e9-122">參數</span><span class="sxs-lookup"><span data-stu-id="793e9-122">PARAMETERS</span></span>

### <span data-ttu-id="793e9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="793e9-123">-Name</span></span>
<span data-ttu-id="793e9-124">指定要刪除的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="793e9-124">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="793e9-125">根據預設， **移除-AzureRmTag** 會移除指定的標記及其所有值。</span><span class="sxs-lookup"><span data-stu-id="793e9-125">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="793e9-126">若要刪除選取的值，但不刪除標記，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="793e9-126">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="793e9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="793e9-127">-PassThru</span></span>
<span data-ttu-id="793e9-128">傳回代表已刪除的標籤或含有已刪除之值的結果標記的物件。</span><span class="sxs-lookup"><span data-stu-id="793e9-128">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="793e9-129">-值</span><span class="sxs-lookup"><span data-stu-id="793e9-129">-Value</span></span>
<span data-ttu-id="793e9-130">從預先定義的標記中刪除指定的值，但不會刪除標籤。</span><span class="sxs-lookup"><span data-stu-id="793e9-130">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="793e9-131">-確認</span><span class="sxs-lookup"><span data-stu-id="793e9-131">-Confirm</span></span>
<span data-ttu-id="793e9-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="793e9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793e9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793e9-133">-WhatIf</span></span>
<span data-ttu-id="793e9-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="793e9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="793e9-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="793e9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793e9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793e9-136">-DefaultProfile</span></span>
<span data-ttu-id="793e9-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="793e9-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="793e9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793e9-138">CommonParameters</span></span>
<span data-ttu-id="793e9-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="793e9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793e9-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="793e9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793e9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="793e9-141">INPUTS</span></span>

### <span data-ttu-id="793e9-142">所有</span><span class="sxs-lookup"><span data-stu-id="793e9-142">None</span></span>

## <span data-ttu-id="793e9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="793e9-143">OUTPUTS</span></span>

### <span data-ttu-id="793e9-144">[無] 或 [PSTag]。</span><span class="sxs-lookup"><span data-stu-id="793e9-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="793e9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="793e9-145">NOTES</span></span>

## <span data-ttu-id="793e9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="793e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="793e9-147">AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="793e9-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="793e9-148">新-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="793e9-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


