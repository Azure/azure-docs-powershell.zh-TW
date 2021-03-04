---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: b5f80abac4c114ab60dcb130f229265c4aafd78f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906869"
---
# <span data-ttu-id="84019-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="84019-101">New-AzTag</span></span>

## <span data-ttu-id="84019-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84019-102">SYNOPSIS</span></span>
<span data-ttu-id="84019-103">建立預先定義的 Azure 標記，或將值加到現有的標記|在資源或訂閱上建立或更新整組標記。</span><span class="sxs-lookup"><span data-stu-id="84019-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="84019-104">語法</span><span class="sxs-lookup"><span data-stu-id="84019-104">SYNTAX</span></span>

### <span data-ttu-id="84019-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="84019-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84019-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84019-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="84019-107">描述</span><span class="sxs-lookup"><span data-stu-id="84019-107">DESCRIPTION</span></span>

<span data-ttu-id="84019-108">**CreatePredefinedTagSet：New-AzTag** Cmdlet 會建立預先定義的 Azure 標籤，以及選擇性的預先定義值。 </span><span class="sxs-lookup"><span data-stu-id="84019-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="84019-109">您也可以使用它，將其他值新增到現有的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="84019-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="84019-110">若要建立預先定義的標記，請輸入唯一的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="84019-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="84019-111">若要新增值至現有的預先定義標記，請指定現有標記的名稱及新值。</span><span class="sxs-lookup"><span data-stu-id="84019-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="84019-112">此 Cmdlet 會以其值及已使用的資源數目，來代表新的或修改過標記的物件。</span><span class="sxs-lookup"><span data-stu-id="84019-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="84019-113">**New-AzTag** 屬於 Azure 標記模組的一部分，可協助管理預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="84019-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="84019-114">Azure 標記是一組名稱值，可用於將 Azure 資源和資源群組分類，例如按部門或成本中心分類，或追蹤資源與群組的附注或批註。</span><span class="sxs-lookup"><span data-stu-id="84019-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="84019-115">您可以在單一步驟中定義並應用標記，但預先定義的標記讓您為訂閱中的標記建立標準、一致、可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="84019-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="84019-116">若要將預先定義的標籤適用于資源或資源群組，請使用Cmdlet New-AzTag標記參數。</span><span class="sxs-lookup"><span data-stu-id="84019-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="84019-117">若要搜尋具有指定標籤名稱或名稱和值的資源群組，請使用 Get-AzResourceGroup  Cmdlet 的 Tag 參數。</span><span class="sxs-lookup"><span data-stu-id="84019-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="84019-118">每個標記都有一個名稱。</span><span class="sxs-lookup"><span data-stu-id="84019-118">Every tag has a name.</span></span>
<span data-ttu-id="84019-119">這些值為選擇性。</span><span class="sxs-lookup"><span data-stu-id="84019-119">The values are optional.</span></span>
<span data-ttu-id="84019-120">預先定義的 Azure 標記可以有多個值，但當您將標記適用于資源或資源群組時，您只會將標記名稱及其中一個值進行設定。</span><span class="sxs-lookup"><span data-stu-id="84019-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="84019-121">例如，您可以針對每個部門建立預先定義的部門標記，例如財務、人力資源和 IT。</span><span class="sxs-lookup"><span data-stu-id="84019-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="84019-122">當您將部門標記適用于資源時，您只會使用一個預先定義的值，例如財務。</span><span class="sxs-lookup"><span data-stu-id="84019-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="84019-123">**CreateByResourceIdParameterSet：\*\*\*\*具有 ResourceId** 的 **New-AzTag** Cmdlet 會建立或更新資源或訂閱上的整組標籤。</span><span class="sxs-lookup"><span data-stu-id="84019-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="84019-124">這項作業允許在指定的資源或訂閱上新增或取代整組標記。</span><span class="sxs-lookup"><span data-stu-id="84019-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="84019-125">指定實體最多可以有 50 個標記。</span><span class="sxs-lookup"><span data-stu-id="84019-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="84019-126">例子</span><span class="sxs-lookup"><span data-stu-id="84019-126">EXAMPLES</span></span>

### <span data-ttu-id="84019-127">範例 1：建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="84019-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="84019-128">此命令會建立名為 FY2015 的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="84019-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="84019-129">此標記沒有值。</span><span class="sxs-lookup"><span data-stu-id="84019-129">This tag has no values.</span></span>
<span data-ttu-id="84019-130">您可以將沒有值的標記適用于資源或資源群組，或使用 **New-AzTag** 在標記中新增值。</span><span class="sxs-lookup"><span data-stu-id="84019-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="84019-131">您也可以在將標記適用于資源或資源群組時指定值。</span><span class="sxs-lookup"><span data-stu-id="84019-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="84019-132">範例 2：使用值建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="84019-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="84019-133">此命令會建立名為 Department 的預先定義標記，並包含財務值。</span><span class="sxs-lookup"><span data-stu-id="84019-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="84019-134">範例 3：在預先定義的標記中新增值</span><span class="sxs-lookup"><span data-stu-id="84019-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="84019-135">這些命令會建立一個名為 Department 的預先定義標記，並包含兩個值。</span><span class="sxs-lookup"><span data-stu-id="84019-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="84019-136">如果標記名稱存在 **，New-AzTag** 會新增值至現有標記，而不是建立新標記。</span><span class="sxs-lookup"><span data-stu-id="84019-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="84019-137">範例 4：使用預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="84019-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="84019-138">此範例中的命令會建立並使用預先定義的標記。</span><span class="sxs-lookup"><span data-stu-id="84019-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="84019-139">範例 5：在訂閱上建立或更新整組標記</span><span class="sxs-lookup"><span data-stu-id="84019-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="84019-140">此命令會使用 {subId} 建立或更新訂閱上的整組標記。</span><span class="sxs-lookup"><span data-stu-id="84019-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="84019-141">範例 6：建立或更新資源上的整組標記</span><span class="sxs-lookup"><span data-stu-id="84019-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="84019-142">此命令會使用 {resourceId} 建立或更新資源上的整組標記。</span><span class="sxs-lookup"><span data-stu-id="84019-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="84019-143">參數</span><span class="sxs-lookup"><span data-stu-id="84019-143">PARAMETERS</span></span>

### <span data-ttu-id="84019-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84019-144">-DefaultProfile</span></span>
<span data-ttu-id="84019-145">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84019-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84019-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="84019-146">-Name</span></span>
<span data-ttu-id="84019-147">指定預先定義的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="84019-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="84019-148">若要建立新的預先定義標記，請輸入唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="84019-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="84019-149">若要新增值至現有的標記，請輸入現有標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="84019-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="84019-150">如果現有的預先定義標記有指定的名稱 **，New-AzTag** 會新增指定值至具有該名稱的標記 ，而不是建立新標記。</span><span class="sxs-lookup"><span data-stu-id="84019-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="84019-151">-值</span><span class="sxs-lookup"><span data-stu-id="84019-151">-Value</span></span>
<span data-ttu-id="84019-152">指定預先定義的標記值。</span><span class="sxs-lookup"><span data-stu-id="84019-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="84019-153">預先定義的標記可以有多個值，但您可以在每個命令中只輸入一個值。</span><span class="sxs-lookup"><span data-stu-id="84019-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="84019-154">此參數為選擇性，因為標記的名稱可以沒有值。</span><span class="sxs-lookup"><span data-stu-id="84019-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="84019-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84019-155">-ResourceId</span></span>
<span data-ttu-id="84019-156">要標記之實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="84019-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="84019-157">系統可能會標記資源、資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="84019-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="84019-158">-標記</span><span class="sxs-lookup"><span data-stu-id="84019-158">-Tag</span></span>
<span data-ttu-id="84019-159">要放在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="84019-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="84019-160">-確認</span><span class="sxs-lookup"><span data-stu-id="84019-160">-Confirm</span></span>
<span data-ttu-id="84019-161">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84019-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84019-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84019-162">-WhatIf</span></span>
<span data-ttu-id="84019-163">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84019-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84019-164">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84019-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84019-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84019-165">CommonParameters</span></span>
<span data-ttu-id="84019-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84019-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84019-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84019-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84019-168">輸入</span><span class="sxs-lookup"><span data-stu-id="84019-168">INPUTS</span></span>

### <span data-ttu-id="84019-169">System.String</span><span class="sxs-lookup"><span data-stu-id="84019-169">System.String</span></span>

### <span data-ttu-id="84019-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="84019-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84019-171">輸出</span><span class="sxs-lookup"><span data-stu-id="84019-171">OUTPUTS</span></span>

### <span data-ttu-id="84019-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag |Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="84019-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="84019-173">筆記</span><span class="sxs-lookup"><span data-stu-id="84019-173">NOTES</span></span>

## <span data-ttu-id="84019-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="84019-174">RELATED LINKS</span></span>

[<span data-ttu-id="84019-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="84019-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="84019-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="84019-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="84019-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="84019-177">Update-AzTag</span></span>](./Update-AzTag.md)