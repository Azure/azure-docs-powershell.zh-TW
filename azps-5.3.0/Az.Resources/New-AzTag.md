---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435426"
---
# <span data-ttu-id="22448-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="22448-101">New-AzTag</span></span>

## <span data-ttu-id="22448-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22448-102">SYNOPSIS</span></span>
<span data-ttu-id="22448-103">建立預先定義的 Azure 標記，或將值新增至現有的標記 |在資源或訂閱上建立或更新一組完整的標記。</span><span class="sxs-lookup"><span data-stu-id="22448-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="22448-104">句法</span><span class="sxs-lookup"><span data-stu-id="22448-104">SYNTAX</span></span>

### <span data-ttu-id="22448-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="22448-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22448-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22448-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="22448-107">說明</span><span class="sxs-lookup"><span data-stu-id="22448-107">DESCRIPTION</span></span>

<span data-ttu-id="22448-108">**CreatePredefinedTagSet**： **AzTag** Cmdlet 會建立具有選擇性預先定義值的預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="22448-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="22448-109">您也可以使用它將其他值新增到現有的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="22448-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="22448-110">若要建立預先定義的標記，請輸入唯一的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="22448-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="22448-111">若要將值新增到現有的預先定義標記，請指定現有標記的名稱和新值。</span><span class="sxs-lookup"><span data-stu-id="22448-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="22448-112">這個 Cmdlet 會傳回一個物件，該物件代表新的或修改過的標記及其值，以及已套用的資源數。</span><span class="sxs-lookup"><span data-stu-id="22448-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="22448-113">AzTag 是 [Azure Tags] 模組的一部分，可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="22448-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="22448-114">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="22448-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="22448-115">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="22448-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="22448-116">若要將預先定義的標記套用至資源或資源群組，請使用 New-AzTag Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="22448-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="22448-117">若要搜尋具有指定標記名稱或名稱和值的資源群組，請使用 Get-AzResourceGroup Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="22448-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="22448-118">每個標記都有一個名稱。</span><span class="sxs-lookup"><span data-stu-id="22448-118">Every tag has a name.</span></span>
<span data-ttu-id="22448-119">這些值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="22448-119">The values are optional.</span></span>
<span data-ttu-id="22448-120">預先定義的 Azure 標記可以有多個值，但是當您將標籤套用至資源或資源群組時，會套用標籤名稱，且只套用其其中一個值。</span><span class="sxs-lookup"><span data-stu-id="22448-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="22448-121">例如，您可以建立預先定義的部門標記，其中包含每個部門的值，例如財務、人力資源及 IT。</span><span class="sxs-lookup"><span data-stu-id="22448-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="22448-122">當您將部門標記套用至資源時，只會套用一個預先定義的值（例如 [財務]）。</span><span class="sxs-lookup"><span data-stu-id="22448-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="22448-123">**CreateByResourceIdParameterSet**： AzTag Cmdlet （含 **ResourceId** **）** 會在資源或訂閱上建立或更新整個標記組。</span><span class="sxs-lookup"><span data-stu-id="22448-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="22448-124">這個作業可讓您在指定的資源或訂閱上新增或取代整個標記組。</span><span class="sxs-lookup"><span data-stu-id="22448-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="22448-125">指定的實體最多可以有50個標籤。</span><span class="sxs-lookup"><span data-stu-id="22448-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="22448-126">示例</span><span class="sxs-lookup"><span data-stu-id="22448-126">EXAMPLES</span></span>

### <span data-ttu-id="22448-127">範例1：建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="22448-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="22448-128">這個命令會建立名為 FY2015 的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="22448-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="22448-129">此標記沒有值。</span><span class="sxs-lookup"><span data-stu-id="22448-129">This tag has no values.</span></span>
<span data-ttu-id="22448-130">您可以將沒有值的標籤套用至資源或資源群組，或使用 [ **新-AzTag** ]，將值新增到標籤。</span><span class="sxs-lookup"><span data-stu-id="22448-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="22448-131">您也可以在將標籤套用至 [資源] 或 [資源] 群組時，指定一個值。</span><span class="sxs-lookup"><span data-stu-id="22448-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="22448-132">範例2：使用值建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="22448-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="22448-133">這個命令會建立名為「含財務價值」的「部門」的預先定義標籤。</span><span class="sxs-lookup"><span data-stu-id="22448-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="22448-134">範例3：將值新增至預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="22448-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="22448-135">這些命令會建立名為「具有兩個值的部門」的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="22448-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="22448-136">如果標籤名稱存在， **新的 AzTag** 會將值新增到現有的標籤，而不是建立新的標記。</span><span class="sxs-lookup"><span data-stu-id="22448-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="22448-137">範例4：使用預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="22448-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="22448-138">這個範例中的命令會建立並使用預先定義的標記。</span><span class="sxs-lookup"><span data-stu-id="22448-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="22448-139">範例5：建立或更新訂閱上的整個標記集</span><span class="sxs-lookup"><span data-stu-id="22448-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="22448-140">這個命令會在您的訂閱中使用 {subId} 建立或更新整個標記組。</span><span class="sxs-lookup"><span data-stu-id="22448-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="22448-141">範例6：建立或更新資源的整個標記集</span><span class="sxs-lookup"><span data-stu-id="22448-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="22448-142">這個命令會使用 {resourceId} 在資源上建立或更新整個標記組。</span><span class="sxs-lookup"><span data-stu-id="22448-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="22448-143">參數</span><span class="sxs-lookup"><span data-stu-id="22448-143">PARAMETERS</span></span>

### <span data-ttu-id="22448-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22448-144">-DefaultProfile</span></span>
<span data-ttu-id="22448-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22448-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22448-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="22448-146">-Name</span></span>
<span data-ttu-id="22448-147">指定預先定義的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="22448-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="22448-148">若要建立新的預先定義標記，請輸入唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="22448-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="22448-149">若要將值新增至現有的標籤，請輸入現有標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="22448-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="22448-150">如果現有預先定義的標記具有指定的名稱， **新的 AzTag** 會將指定的值（如果有的話）加到具有該名稱的標籤，而不是建立新的標記。</span><span class="sxs-lookup"><span data-stu-id="22448-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22448-151">-值</span><span class="sxs-lookup"><span data-stu-id="22448-151">-Value</span></span>
<span data-ttu-id="22448-152">指定預先定義的標記值。</span><span class="sxs-lookup"><span data-stu-id="22448-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="22448-153">預先定義的標記可以有多個值，但您只能在每個命令中輸入一個值。</span><span class="sxs-lookup"><span data-stu-id="22448-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="22448-154">這個參數是選擇性的，因為標記可以有沒有值的名稱。</span><span class="sxs-lookup"><span data-stu-id="22448-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22448-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22448-155">-ResourceId</span></span>
<span data-ttu-id="22448-156">要加上標籤的實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="22448-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="22448-157">資源、資源群組或訂閱可能會加上標籤。</span><span class="sxs-lookup"><span data-stu-id="22448-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22448-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="22448-158">-Tag</span></span>
<span data-ttu-id="22448-159">要放在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="22448-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22448-160">-確認</span><span class="sxs-lookup"><span data-stu-id="22448-160">-Confirm</span></span>
<span data-ttu-id="22448-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22448-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22448-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22448-162">-WhatIf</span></span>
<span data-ttu-id="22448-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22448-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22448-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22448-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22448-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22448-165">CommonParameters</span></span>
<span data-ttu-id="22448-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22448-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22448-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22448-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22448-168">輸入</span><span class="sxs-lookup"><span data-stu-id="22448-168">INPUTS</span></span>

### <span data-ttu-id="22448-169">System.object</span><span class="sxs-lookup"><span data-stu-id="22448-169">System.String</span></span>

### <span data-ttu-id="22448-170">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22448-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22448-171">輸出</span><span class="sxs-lookup"><span data-stu-id="22448-171">OUTPUTS</span></span>

### <span data-ttu-id="22448-172">[PSTag |] （通用）命令。[PSTagResource] 命令。</span><span class="sxs-lookup"><span data-stu-id="22448-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="22448-173">筆記</span><span class="sxs-lookup"><span data-stu-id="22448-173">NOTES</span></span>

## <span data-ttu-id="22448-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="22448-174">RELATED LINKS</span></span>

[<span data-ttu-id="22448-175">AzTag</span><span class="sxs-lookup"><span data-stu-id="22448-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="22448-176">移除-AzTag</span><span class="sxs-lookup"><span data-stu-id="22448-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="22448-177">更新-AzTag</span><span class="sxs-lookup"><span data-stu-id="22448-177">Update-AzTag</span></span>](./Update-AzTag.md)