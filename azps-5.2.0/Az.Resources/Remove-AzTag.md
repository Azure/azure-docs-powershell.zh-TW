---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280996"
---
# <span data-ttu-id="42d3f-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="42d3f-101">Remove-AzTag</span></span>

## <span data-ttu-id="42d3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="42d3f-103">刪除預先定義的 Azure 標記或值 |刪除資源或訂閱上的整個標記組。</span><span class="sxs-lookup"><span data-stu-id="42d3f-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="42d3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="42d3f-104">SYNTAX</span></span>

### <span data-ttu-id="42d3f-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="42d3f-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d3f-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42d3f-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="42d3f-107">說明</span><span class="sxs-lookup"><span data-stu-id="42d3f-107">DESCRIPTION</span></span>

<span data-ttu-id="42d3f-108">**RemovePredefinedTagSet**： **Remove-AzTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標記和值。</span><span class="sxs-lookup"><span data-stu-id="42d3f-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="42d3f-109">若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="42d3f-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="42d3f-110">根據預設， **移除-AzTag** 會刪除指定的標記及其所有值。您無法刪除目前已套用至資源或資源群組的標記或值。</span><span class="sxs-lookup"><span data-stu-id="42d3f-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="42d3f-111">在使用 **Remove-AzTag** 之前，請使用 Set-AzResourceGroup Cmdlet 的 *tag* 參數來刪除 [資源] 或 [資源] 群組中的標籤或值。</span><span class="sxs-lookup"><span data-stu-id="42d3f-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="42d3f-112">AzTag 是其中一部分的 Azure Tags 模組可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="42d3f-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="42d3f-113">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="42d3f-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="42d3f-114">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="42d3f-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="42d3f-115">**RemoveByResourceIdParameterSet**： AzTag Cmdlet （含 **ResourceId** **）** 會刪除資源或訂閱上的整個標記組。</span><span class="sxs-lookup"><span data-stu-id="42d3f-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="42d3f-116">示例</span><span class="sxs-lookup"><span data-stu-id="42d3f-116">EXAMPLES</span></span>

### <span data-ttu-id="42d3f-117">範例1：刪除預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="42d3f-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="42d3f-118">這個命令會刪除名為「部門」及其所有值的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="42d3f-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="42d3f-119">如果已將標記套用至任何資源或資源群組，則命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="42d3f-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="42d3f-120">範例2：從預先定義的標記中刪除值</span><span class="sxs-lookup"><span data-stu-id="42d3f-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="42d3f-121">這個命令會從預先定義的 [部門] 標記刪除 HumanResources 值。</span><span class="sxs-lookup"><span data-stu-id="42d3f-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="42d3f-122">它不會刪除標記。</span><span class="sxs-lookup"><span data-stu-id="42d3f-122">It does not delete the tag.</span></span>
<span data-ttu-id="42d3f-123">如果該值已套用至任何資源或資源群組，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="42d3f-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="42d3f-124">範例3：刪除訂閱上整套的標記</span><span class="sxs-lookup"><span data-stu-id="42d3f-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="42d3f-125">這個命令會使用 {subId} 刪除訂閱上的整個標記組。</span><span class="sxs-lookup"><span data-stu-id="42d3f-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="42d3f-126">如果不是傳入 "-PassThru"，就不會傳回刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="42d3f-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="42d3f-127">範例4：刪除資源的整個標記集</span><span class="sxs-lookup"><span data-stu-id="42d3f-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="42d3f-128">這個命令會在資源上使用 {resourceId} 刪除整個標記組。</span><span class="sxs-lookup"><span data-stu-id="42d3f-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="42d3f-129">傳入 "-PassThru" 時，會傳回已刪除的 oject。</span><span class="sxs-lookup"><span data-stu-id="42d3f-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="42d3f-130">參數</span><span class="sxs-lookup"><span data-stu-id="42d3f-130">PARAMETERS</span></span>

### <span data-ttu-id="42d3f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d3f-131">-DefaultProfile</span></span>
<span data-ttu-id="42d3f-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42d3f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d3f-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="42d3f-133">-Name</span></span>
<span data-ttu-id="42d3f-134">指定要移除的預先定義標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="42d3f-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="42d3f-135">根據預設， **移除-AzTag** 會移除指定的標記及其所有值。</span><span class="sxs-lookup"><span data-stu-id="42d3f-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="42d3f-136">若要刪除選取的值，但不刪除標記，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="42d3f-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d3f-137">-值</span><span class="sxs-lookup"><span data-stu-id="42d3f-137">-Value</span></span>
<span data-ttu-id="42d3f-138">從預先定義的標記中刪除指定的值，但不會刪除標籤。</span><span class="sxs-lookup"><span data-stu-id="42d3f-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d3f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42d3f-139">-ResourceId</span></span>
<span data-ttu-id="42d3f-140">標籤實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="42d3f-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="42d3f-141">資源、資源群組或訂閱可能會加上標籤。</span><span class="sxs-lookup"><span data-stu-id="42d3f-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d3f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42d3f-142">-PassThru</span></span>
<span data-ttu-id="42d3f-143">傳回代表已刪除的標籤或含有已刪除之值的結果標記的物件。</span><span class="sxs-lookup"><span data-stu-id="42d3f-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="42d3f-144">-確認</span><span class="sxs-lookup"><span data-stu-id="42d3f-144">-Confirm</span></span>
<span data-ttu-id="42d3f-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42d3f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d3f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d3f-146">-WhatIf</span></span>
<span data-ttu-id="42d3f-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42d3f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d3f-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42d3f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d3f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d3f-149">CommonParameters</span></span>
<span data-ttu-id="42d3f-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42d3f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d3f-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42d3f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d3f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="42d3f-152">INPUTS</span></span>

### <span data-ttu-id="42d3f-153">System.object</span><span class="sxs-lookup"><span data-stu-id="42d3f-153">System.String</span></span>

### <span data-ttu-id="42d3f-154">System.object []</span><span class="sxs-lookup"><span data-stu-id="42d3f-154">System.String[]</span></span>

### <span data-ttu-id="42d3f-155">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="42d3f-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42d3f-156">輸出</span><span class="sxs-lookup"><span data-stu-id="42d3f-156">OUTPUTS</span></span>

### <span data-ttu-id="42d3f-157">[PSTag |] （通用）命令。[PSTagResource] 命令。</span><span class="sxs-lookup"><span data-stu-id="42d3f-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="42d3f-158">筆記</span><span class="sxs-lookup"><span data-stu-id="42d3f-158">NOTES</span></span>

## <span data-ttu-id="42d3f-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="42d3f-159">RELATED LINKS</span></span>

[<span data-ttu-id="42d3f-160">AzTag</span><span class="sxs-lookup"><span data-stu-id="42d3f-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="42d3f-161">新-AzTag</span><span class="sxs-lookup"><span data-stu-id="42d3f-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="42d3f-162">更新-AzTag</span><span class="sxs-lookup"><span data-stu-id="42d3f-162">Update-AzTag</span></span>](./Update-AzTag.md)