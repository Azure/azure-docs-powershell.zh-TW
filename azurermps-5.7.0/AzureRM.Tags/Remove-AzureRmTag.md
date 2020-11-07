---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: f51411c4683a79283ad5e0a73554f6db3ce7e52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623446"
---
# <span data-ttu-id="87f0a-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="87f0a-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="87f0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="87f0a-103">刪除預先定義的 Azure 標記或值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87f0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="87f0a-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87f0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="87f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="87f0a-106">**AzureRmTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標記和值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="87f0a-107">若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="87f0a-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="87f0a-108">根據預設， **移除-AzureRmTag** 會刪除指定的標記及其所有值。您無法刪除目前已套用至資源或資源群組的標記或值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="87f0a-109">在使用 **Remove-AzureRmTag** 之前，請使用 Set-AzureRMResourceGroup Cmdlet 的 *tag* 參數來刪除 [資源] 或 [資源] 群組中的標籤或值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="87f0a-110">AzureRmTag 是其中一部分的 Azure Tags 模組可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="87f0a-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="87f0a-111">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="87f0a-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="87f0a-112">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="87f0a-113">如果訂閱包含任何預先定義的標記，您就無法將未定義的標籤或值套用到訂閱中的任何資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="87f0a-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="87f0a-114">示例</span><span class="sxs-lookup"><span data-stu-id="87f0a-114">EXAMPLES</span></span>

### <span data-ttu-id="87f0a-115">範例1：刪除預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="87f0a-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="87f0a-116">這個命令會刪除名為「部門」及其所有資源的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="87f0a-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="87f0a-117">如果已將標記套用至任何資源或資源群組，則命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="87f0a-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="87f0a-118">範例2：從預先定義的標記中刪除值</span><span class="sxs-lookup"><span data-stu-id="87f0a-118">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="87f0a-119">這個命令會從預先定義的 [部門] 標記刪除 HumanResources 值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="87f0a-120">它不會刪除標記。</span><span class="sxs-lookup"><span data-stu-id="87f0a-120">It does not delete the tag.</span></span>
<span data-ttu-id="87f0a-121">如果該值已套用至任何資源或資源群組，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="87f0a-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="87f0a-122">參數</span><span class="sxs-lookup"><span data-stu-id="87f0a-122">PARAMETERS</span></span>

### <span data-ttu-id="87f0a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f0a-123">-DefaultProfile</span></span>
<span data-ttu-id="87f0a-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87f0a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f0a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="87f0a-125">-Name</span></span>
<span data-ttu-id="87f0a-126">指定要刪除的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="87f0a-126">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="87f0a-127">根據預設， **移除-AzureRmTag** 會移除指定的標記及其所有值。</span><span class="sxs-lookup"><span data-stu-id="87f0a-127">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="87f0a-128">若要刪除選取的值，但不刪除標記，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="87f0a-128">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f0a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87f0a-129">-PassThru</span></span>
<span data-ttu-id="87f0a-130">傳回代表已刪除的標籤或含有已刪除之值的結果標記的物件。</span><span class="sxs-lookup"><span data-stu-id="87f0a-130">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f0a-131">-值</span><span class="sxs-lookup"><span data-stu-id="87f0a-131">-Value</span></span>
<span data-ttu-id="87f0a-132">從預先定義的標記中刪除指定的值，但不會刪除標籤。</span><span class="sxs-lookup"><span data-stu-id="87f0a-132">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f0a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="87f0a-133">-Confirm</span></span>
<span data-ttu-id="87f0a-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87f0a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f0a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87f0a-135">-WhatIf</span></span>
<span data-ttu-id="87f0a-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87f0a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87f0a-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87f0a-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f0a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f0a-138">CommonParameters</span></span>
<span data-ttu-id="87f0a-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87f0a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f0a-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87f0a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f0a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="87f0a-141">INPUTS</span></span>

### <span data-ttu-id="87f0a-142">所有</span><span class="sxs-lookup"><span data-stu-id="87f0a-142">None</span></span>

## <span data-ttu-id="87f0a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="87f0a-143">OUTPUTS</span></span>

### <span data-ttu-id="87f0a-144">[無] 或 [PSTag]。</span><span class="sxs-lookup"><span data-stu-id="87f0a-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="87f0a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="87f0a-145">NOTES</span></span>

## <span data-ttu-id="87f0a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="87f0a-146">RELATED LINKS</span></span>

[<span data-ttu-id="87f0a-147">AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="87f0a-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="87f0a-148">新-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="87f0a-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


