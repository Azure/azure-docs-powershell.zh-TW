---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: cd9700a633f1a9c09c5fafd060d318b35eaeaabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455896"
---
# <span data-ttu-id="ff06a-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ff06a-101">New-AzureRmTag</span></span>

## <span data-ttu-id="ff06a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff06a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff06a-103">建立預先定義的 Azure 標記，或將值新增到現有的標籤。</span><span class="sxs-lookup"><span data-stu-id="ff06a-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff06a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff06a-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff06a-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff06a-105">DESCRIPTION</span></span>
<span data-ttu-id="ff06a-106">**AzureRmTag** Cmdlet 會建立具有選擇性預先定義值的預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="ff06a-107">您也可以使用它將其他值新增到現有的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="ff06a-108">若要建立預先定義的標記，請輸入唯一的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="ff06a-109">若要將值新增到現有的預先定義標記，請指定現有標記的名稱和新值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="ff06a-110">這個 Cmdlet 會傳回一個物件，該物件代表新的或修改過的標記及其值，以及已套用的資源數。</span><span class="sxs-lookup"><span data-stu-id="ff06a-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="ff06a-111">AzureRmTag 是 [Azure Tags] 模組的一部分，可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="ff06a-112">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="ff06a-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="ff06a-113">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="ff06a-114">若要將預先定義的標記套用至資源或資源群組，請使用 New-AzureRmTag Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="ff06a-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="ff06a-115">若要搜尋具有指定標記名稱或名稱和值的資源群組，請使用 Get-AzureRMResourceGroup Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="ff06a-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ff06a-116">每個標記都有一個名稱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-116">Every tag has a name.</span></span>
<span data-ttu-id="ff06a-117">這些值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ff06a-117">The values are optional.</span></span>
<span data-ttu-id="ff06a-118">預先定義的 Azure 標記可以有多個值，但是當您將標籤套用至資源或資源群組時，會套用標籤名稱，且只套用其其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="ff06a-119">例如，您可以建立預先定義的部門標記，其中包含每個部門的值，例如財務、人力資源及 IT。</span><span class="sxs-lookup"><span data-stu-id="ff06a-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="ff06a-120">當您將部門標記套用至資源時，只會套用一個預先定義的值（例如 [財務]）。</span><span class="sxs-lookup"><span data-stu-id="ff06a-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="ff06a-121">示例</span><span class="sxs-lookup"><span data-stu-id="ff06a-121">EXAMPLES</span></span>

### <span data-ttu-id="ff06a-122">範例1：建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="ff06a-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   FY2015
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="ff06a-123">這個命令會建立名為 FY2015 的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="ff06a-124">此標記沒有值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-124">This tag has no values.</span></span>
<span data-ttu-id="ff06a-125">您可以將沒有值的標籤套用至資源或資源群組，或使用 [ **新-AzureRmTag** ]，將值新增到標籤。</span><span class="sxs-lookup"><span data-stu-id="ff06a-125">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="ff06a-126">您也可以在將標籤套用至 [資源] 或 [資源] 群組時，指定一個值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="ff06a-127">範例2：使用值建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="ff06a-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="ff06a-128">這個命令會建立名為「含財務價值」的「部門」的預先定義標籤。</span><span class="sxs-lookup"><span data-stu-id="ff06a-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="ff06a-129">範例3：將值新增至預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="ff06a-129">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="ff06a-130">這些命令會建立名為「具有兩個值的部門」的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="ff06a-131">如果標籤名稱存在， **新的 AzureRmTag** 會將值新增到現有的標籤，而不是建立新的標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-131">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="ff06a-132">範例4：使用預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="ff06a-132">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="ff06a-133">這個範例中的命令會建立並使用預先定義的標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="ff06a-134">參數</span><span class="sxs-lookup"><span data-stu-id="ff06a-134">PARAMETERS</span></span>

### <span data-ttu-id="ff06a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff06a-135">-DefaultProfile</span></span>
<span data-ttu-id="ff06a-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff06a-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff06a-137">-Name</span></span>
<span data-ttu-id="ff06a-138">指定標記名稱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-138">Specifies the tag name.</span></span>
<span data-ttu-id="ff06a-139">若要建立新的預先定義標記，請輸入唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="ff06a-140">若要將值新增至現有的標籤，請輸入現有標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="ff06a-141">如果現有預先定義的標記具有指定的名稱， **新的 AzureRmTag** 會將指定的值（如果有的話）加到具有該名稱的標籤，而不是建立新的標記。</span><span class="sxs-lookup"><span data-stu-id="ff06a-141">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="ff06a-142">-值</span><span class="sxs-lookup"><span data-stu-id="ff06a-142">-Value</span></span>
<span data-ttu-id="ff06a-143">指定標記值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-143">Specifies a tag value.</span></span>
<span data-ttu-id="ff06a-144">預先定義的標記可以有多個值，但您只能在每個命令中輸入一個值。</span><span class="sxs-lookup"><span data-stu-id="ff06a-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="ff06a-145">這個參數是選擇性的，因為標記可以有沒有值的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff06a-145">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff06a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff06a-146">CommonParameters</span></span>
<span data-ttu-id="ff06a-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff06a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff06a-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff06a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff06a-149">輸入</span><span class="sxs-lookup"><span data-stu-id="ff06a-149">INPUTS</span></span>

### <span data-ttu-id="ff06a-150">System.object</span><span class="sxs-lookup"><span data-stu-id="ff06a-150">System.String</span></span>

## <span data-ttu-id="ff06a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="ff06a-151">OUTPUTS</span></span>

### <span data-ttu-id="ff06a-152">PSTag 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="ff06a-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="ff06a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="ff06a-153">NOTES</span></span>

## <span data-ttu-id="ff06a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff06a-154">RELATED LINKS</span></span>

[<span data-ttu-id="ff06a-155">AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ff06a-155">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="ff06a-156">移除-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ff06a-156">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


