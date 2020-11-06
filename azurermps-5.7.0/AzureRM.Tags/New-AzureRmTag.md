---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452963"
---
# <span data-ttu-id="cdf85-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="cdf85-101">New-AzureRmTag</span></span>

## <span data-ttu-id="cdf85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdf85-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf85-103">建立預先定義的 Azure 標記，或將值新增到現有的標籤。</span><span class="sxs-lookup"><span data-stu-id="cdf85-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdf85-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdf85-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdf85-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdf85-105">DESCRIPTION</span></span>
<span data-ttu-id="cdf85-106">**AzureRmTag** Cmdlet 會建立具有選擇性預先定義值的預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="cdf85-107">您也可以使用它將其他值新增到現有的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="cdf85-108">若要建立預先定義的標記，請輸入唯一的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="cdf85-109">若要將值新增到現有的預先定義標記，請指定現有標記的名稱和新值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="cdf85-110">這個 Cmdlet 會傳回一個物件，該物件代表新的或修改過的標記及其值，以及已套用的資源數。</span><span class="sxs-lookup"><span data-stu-id="cdf85-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="cdf85-111">AzureRmTag 是 [Azure Tags] 模組的一部分，可協助您管理預先定義 **的** Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="cdf85-112">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="cdf85-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="cdf85-113">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="cdf85-114">如果訂閱包含任何預先定義的標記，您就無法將未定義的標籤或值套用到訂閱中的任何資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="cdf85-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="cdf85-115">若要將預先定義的標記套用至資源或資源群組，請使用 New-AzureRmTag Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="cdf85-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="cdf85-116">若要搜尋具有指定標記名稱或名稱和值的資源群組，請使用 Get-AzureRMResourceGroup Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="cdf85-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="cdf85-117">每個標記都有一個名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-117">Every tag has a name.</span></span>
<span data-ttu-id="cdf85-118">這些值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="cdf85-118">The values are optional.</span></span>
<span data-ttu-id="cdf85-119">預先定義的 Azure 標記可以有多個值，但是當您將標籤套用至資源或資源群組時，會套用標籤名稱，且只套用其其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="cdf85-120">例如，您可以建立預先定義的部門標記，其中包含每個部門的值，例如財務、人力資源及 IT。</span><span class="sxs-lookup"><span data-stu-id="cdf85-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="cdf85-121">當您將部門標記套用至資源時，只會套用一個預先定義的值（例如 [財務]）。</span><span class="sxs-lookup"><span data-stu-id="cdf85-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="cdf85-122">示例</span><span class="sxs-lookup"><span data-stu-id="cdf85-122">EXAMPLES</span></span>

### <span data-ttu-id="cdf85-123">範例1：建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="cdf85-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="cdf85-124">這個命令會建立名為 FY2015 的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="cdf85-125">此標記沒有值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-125">This tag has no values.</span></span>
<span data-ttu-id="cdf85-126">您可以將沒有值的標籤套用至資源或資源群組，或使用 [ **新-AzureRmTag** ]，將值新增到標籤。</span><span class="sxs-lookup"><span data-stu-id="cdf85-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="cdf85-127">您也可以在將標籤套用至 [資源] 或 [資源] 群組時，指定一個值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="cdf85-128">範例2：使用值建立預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="cdf85-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="cdf85-129">這個命令會建立名為「含財務價值」的「部門」的預先定義標籤。</span><span class="sxs-lookup"><span data-stu-id="cdf85-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="cdf85-130">範例3：將值新增至預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="cdf85-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="cdf85-131">這些命令會建立名為「具有兩個值的部門」的預先定義標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="cdf85-132">如果標籤名稱存在， **新的 AzureRmTag** 會將值新增到現有的標籤，而不是建立新的標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="cdf85-133">範例4：使用預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="cdf85-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="cdf85-134">這個範例中的命令會建立並使用預先定義的標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="cdf85-135">參數</span><span class="sxs-lookup"><span data-stu-id="cdf85-135">PARAMETERS</span></span>

### <span data-ttu-id="cdf85-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf85-136">-DefaultProfile</span></span>
<span data-ttu-id="cdf85-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdf85-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdf85-138">-Name</span></span>
<span data-ttu-id="cdf85-139">指定標記名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-139">Specifies the tag name.</span></span>
<span data-ttu-id="cdf85-140">若要建立新的預先定義標記，請輸入唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-140">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="cdf85-141">若要將值新增至現有的標籤，請輸入現有標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-141">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="cdf85-142">如果現有預先定義的標記具有指定的名稱， **新的 AzureRmTag** 會將指定的值（如果有的話）加到具有該名稱的標籤，而不是建立新的標記。</span><span class="sxs-lookup"><span data-stu-id="cdf85-142">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="cdf85-143">-值</span><span class="sxs-lookup"><span data-stu-id="cdf85-143">-Value</span></span>
<span data-ttu-id="cdf85-144">指定標記值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-144">Specifies a tag value.</span></span>
<span data-ttu-id="cdf85-145">預先定義的標記可以有多個值，但您只能在每個命令中輸入一個值。</span><span class="sxs-lookup"><span data-stu-id="cdf85-145">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="cdf85-146">這個參數是選擇性的，因為標記可以有沒有值的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf85-146">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf85-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf85-147">CommonParameters</span></span>
<span data-ttu-id="cdf85-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdf85-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf85-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cdf85-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf85-150">輸入</span><span class="sxs-lookup"><span data-stu-id="cdf85-150">INPUTS</span></span>

### <span data-ttu-id="cdf85-151">所有</span><span class="sxs-lookup"><span data-stu-id="cdf85-151">None</span></span>

## <span data-ttu-id="cdf85-152">輸出</span><span class="sxs-lookup"><span data-stu-id="cdf85-152">OUTPUTS</span></span>

### <span data-ttu-id="cdf85-153">[PSTag] 命令。</span><span class="sxs-lookup"><span data-stu-id="cdf85-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="cdf85-154">筆記</span><span class="sxs-lookup"><span data-stu-id="cdf85-154">NOTES</span></span>

## <span data-ttu-id="cdf85-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdf85-155">RELATED LINKS</span></span>

[<span data-ttu-id="cdf85-156">AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="cdf85-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="cdf85-157">移除-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="cdf85-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


