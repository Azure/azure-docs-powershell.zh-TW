---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 201e341ce05b22597f05601d7d269d2eb27c2358
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908778"
---
# <span data-ttu-id="882a6-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="882a6-101">Remove-AzTag</span></span>

## <span data-ttu-id="882a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="882a6-102">SYNOPSIS</span></span>
<span data-ttu-id="882a6-103">刪除預先定義的 Azure 標記或|刪除資源或訂閱上的整組標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="882a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="882a6-104">SYNTAX</span></span>

### <span data-ttu-id="882a6-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="882a6-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="882a6-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="882a6-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="882a6-107">描述</span><span class="sxs-lookup"><span data-stu-id="882a6-107">DESCRIPTION</span></span>

<span data-ttu-id="882a6-108">**RemovePredefinedTagSet：Remove-AzTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標籤和值。 </span><span class="sxs-lookup"><span data-stu-id="882a6-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="882a6-109">若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="882a6-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="882a6-110">根據預設 **，Remove-AzTag** 會刪除指定的標記及其所有值。您無法刪除目前適用于資源或資源群組的標記或值。</span><span class="sxs-lookup"><span data-stu-id="882a6-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="882a6-111">使用 **Remove-AzTag** 之前，請使用 Set-AzResourceGroup Cmdlet 的 Tag 參數，從資源或資源群組中刪除標籤或值。</span><span class="sxs-lookup"><span data-stu-id="882a6-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="882a6-112">**Remove-AzTag** 是其中一部分的 Azure 標記模組，可協助管理預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="882a6-113">Azure 標記是一組名稱值，可用於將 Azure 資源和資源群組分類，例如按部門或成本中心分類，或追蹤資源與群組的附注或批註。</span><span class="sxs-lookup"><span data-stu-id="882a6-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="882a6-114">您可以在單一步驟中定義並應用標記，但預先定義的標記讓您為訂閱中的標記建立標準、一致、可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="882a6-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="882a6-115">**RemoveByResourceIdParameterSet：\*\*\*\*具有 ResourceId** 的 **Remove-AzTag** Cmdlet 會刪除資源或訂閱上的整組標籤。</span><span class="sxs-lookup"><span data-stu-id="882a6-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="882a6-116">例子</span><span class="sxs-lookup"><span data-stu-id="882a6-116">EXAMPLES</span></span>

### <span data-ttu-id="882a6-117">範例 1：刪除預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="882a6-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="882a6-118">此命令會刪除名為 Department 的預先定義標記及其所有值。</span><span class="sxs-lookup"><span data-stu-id="882a6-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="882a6-119">如果標記已適用于任何資源或資源群組，則命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="882a6-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="882a6-120">範例 2：從預先定義的標記刪除值</span><span class="sxs-lookup"><span data-stu-id="882a6-120">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="882a6-121">此命令會從預先定義的 Department 標記中刪除 HumanResources 值。</span><span class="sxs-lookup"><span data-stu-id="882a6-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="882a6-122">不會刪除標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-122">It does not delete the tag.</span></span>
<span data-ttu-id="882a6-123">如果該值已適用于任何資源或資源群組，則命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="882a6-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="882a6-124">範例 3：刪除訂閱上的整組標記</span><span class="sxs-lookup"><span data-stu-id="882a6-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="882a6-125">此命令會刪除訂閱上的 {subId} 整組標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="882a6-126">如果未在 "-PassThru" 中傳遞，不會傳回已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="882a6-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="882a6-127">範例 4：刪除資源上的整組標記</span><span class="sxs-lookup"><span data-stu-id="882a6-127">Example 4: Deletes the entire set of tags on a resource</span></span>

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

<span data-ttu-id="882a6-128">此命令會使用 {resourceId} 刪除資源上的整組標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="882a6-129">傳回傳遞 "-PassThru" 時已刪除的 oject。</span><span class="sxs-lookup"><span data-stu-id="882a6-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="882a6-130">參數</span><span class="sxs-lookup"><span data-stu-id="882a6-130">PARAMETERS</span></span>

### <span data-ttu-id="882a6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882a6-131">-DefaultProfile</span></span>
<span data-ttu-id="882a6-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="882a6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="882a6-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="882a6-133">-Name</span></span>
<span data-ttu-id="882a6-134">指定要移除的預先定義標記名稱。</span><span class="sxs-lookup"><span data-stu-id="882a6-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="882a6-135">根據預設 **，Remove-AzTag** 會移除指定的標記及其所有值。</span><span class="sxs-lookup"><span data-stu-id="882a6-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="882a6-136">若要刪除選取的值，但不要刪除標記，請使用 *Value* 參數。</span><span class="sxs-lookup"><span data-stu-id="882a6-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="882a6-137">-值</span><span class="sxs-lookup"><span data-stu-id="882a6-137">-Value</span></span>
<span data-ttu-id="882a6-138">刪除預先定義的標記中的指定值，但不刪除標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="882a6-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="882a6-139">-ResourceId</span></span>
<span data-ttu-id="882a6-140">標記實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="882a6-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="882a6-141">系統可能會標記資源、資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="882a6-141">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="882a6-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="882a6-142">-PassThru</span></span>
<span data-ttu-id="882a6-143">會返回代表已刪除標記的物件，或具有已刪除值的結果標記。</span><span class="sxs-lookup"><span data-stu-id="882a6-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="882a6-144">-確認</span><span class="sxs-lookup"><span data-stu-id="882a6-144">-Confirm</span></span>
<span data-ttu-id="882a6-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="882a6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="882a6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="882a6-146">-WhatIf</span></span>
<span data-ttu-id="882a6-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="882a6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="882a6-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="882a6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="882a6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882a6-149">CommonParameters</span></span>
<span data-ttu-id="882a6-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="882a6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882a6-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="882a6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882a6-152">輸入</span><span class="sxs-lookup"><span data-stu-id="882a6-152">INPUTS</span></span>

### <span data-ttu-id="882a6-153">System.String</span><span class="sxs-lookup"><span data-stu-id="882a6-153">System.String</span></span>

### <span data-ttu-id="882a6-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="882a6-154">System.String[]</span></span>

### <span data-ttu-id="882a6-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="882a6-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="882a6-156">輸出</span><span class="sxs-lookup"><span data-stu-id="882a6-156">OUTPUTS</span></span>

### <span data-ttu-id="882a6-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag |Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="882a6-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="882a6-158">筆記</span><span class="sxs-lookup"><span data-stu-id="882a6-158">NOTES</span></span>

## <span data-ttu-id="882a6-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="882a6-159">RELATED LINKS</span></span>

[<span data-ttu-id="882a6-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="882a6-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="882a6-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="882a6-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="882a6-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="882a6-162">Update-AzTag</span></span>](./Update-AzTag.md)