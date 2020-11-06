---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 5e0766039a9becb65aaec13d08e46f751893b8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451572"
---
# <span data-ttu-id="32bb7-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="32bb7-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="32bb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="32bb7-103">取得預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="32bb7-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32bb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="32bb7-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32bb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="32bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="32bb7-106">**AzureRmTag** Cmdlet 會在您的訂閱中取得預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="32bb7-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="32bb7-107">這個 Cmdlet 會傳回有關標記的基本資訊，或有關標籤及其值的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="32bb7-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="32bb7-108">所有輸出物件都包含 Count 屬性，代表已套用標籤和值的資源和資源群組數。</span><span class="sxs-lookup"><span data-stu-id="32bb7-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>

<span data-ttu-id="32bb7-109">**AzureRMTag** 是的 Azure Tags 模組可協助您管理預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="32bb7-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="32bb7-110">Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="32bb7-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="32bb7-111">您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="32bb7-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="32bb7-112">如果訂閱包含任何預先定義的標記，您就無法將未定義的標籤或值套用到訂閱中的任何資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="32bb7-112">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="32bb7-113">若要建立預先定義的標記，請使用 New-AzureRmTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32bb7-113">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="32bb7-114">若要將預先定義的標記套用至資源群組，請使用 New-AzureRmTag Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="32bb7-114">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="32bb7-115">若要在資源群組中搜尋特定的標籤名稱或名稱與值，請使用 Get-AzureRMResourceGroup Cmdlet 的 *tag* 參數。</span><span class="sxs-lookup"><span data-stu-id="32bb7-115">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="32bb7-116">示例</span><span class="sxs-lookup"><span data-stu-id="32bb7-116">EXAMPLES</span></span>

### <span data-ttu-id="32bb7-117">範例1：取得所有預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="32bb7-117">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="32bb7-118">這個命令會取得訂閱中所有預先定義的標記。</span><span class="sxs-lookup"><span data-stu-id="32bb7-118">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="32bb7-119">Count 屬性顯示標籤已套用到訂閱中資源和資源群組的次數。</span><span class="sxs-lookup"><span data-stu-id="32bb7-119">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="32bb7-120">範例2：透過名稱取得標記</span><span class="sxs-lookup"><span data-stu-id="32bb7-120">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="32bb7-121">這個命令會取得部門標記及其值的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="32bb7-121">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="32bb7-122">Count 屬性會顯示標籤及其每個值已套用到訂閱中資源和資源群組的多少次。</span><span class="sxs-lookup"><span data-stu-id="32bb7-122">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="32bb7-123">範例3：取得所有標記的值</span><span class="sxs-lookup"><span data-stu-id="32bb7-123">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="32bb7-124">這個命令會使用 *詳細* 的參數，以取得訂閱中所有預先定義的標記的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="32bb7-124">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="32bb7-125">使用 *詳細* 的參數，相當於使用每個標記的 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="32bb7-125">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="32bb7-126">參數</span><span class="sxs-lookup"><span data-stu-id="32bb7-126">PARAMETERS</span></span>

### <span data-ttu-id="32bb7-127">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="32bb7-127">-Detailed</span></span>
<span data-ttu-id="32bb7-128">指示此操作會將有關標籤值的資訊新增到輸出。</span><span class="sxs-lookup"><span data-stu-id="32bb7-128">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="32bb7-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="32bb7-129">-Name</span></span>
<span data-ttu-id="32bb7-130">指定要取得的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="32bb7-130">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="32bb7-131">根據預設， **AzureRmTag** 會取得訂閱中所有預先定義的標記的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="32bb7-131">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="32bb7-132">當您指定 *Name* 參數時， *詳細* 的參數就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="32bb7-132">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bb7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bb7-133">-DefaultProfile</span></span>
<span data-ttu-id="32bb7-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32bb7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32bb7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bb7-135">CommonParameters</span></span>
<span data-ttu-id="32bb7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32bb7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bb7-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32bb7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bb7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="32bb7-138">INPUTS</span></span>

### <span data-ttu-id="32bb7-139">所有</span><span class="sxs-lookup"><span data-stu-id="32bb7-139">None</span></span>

## <span data-ttu-id="32bb7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="32bb7-140">OUTPUTS</span></span>

### <span data-ttu-id="32bb7-141">[PSTag]、[.]、[Azure.] 命令. 標記</span><span class="sxs-lookup"><span data-stu-id="32bb7-141">Microsoft.Azure.Commands.Tags.Model.PSTag, Microsoft.Azure.Commands.Tags</span></span>

## <span data-ttu-id="32bb7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="32bb7-142">NOTES</span></span>

## <span data-ttu-id="32bb7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="32bb7-143">RELATED LINKS</span></span>

[<span data-ttu-id="32bb7-144">新-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="32bb7-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="32bb7-145">移除-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="32bb7-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


