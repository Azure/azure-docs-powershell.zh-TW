---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912322"
---
# <span data-ttu-id="f0a51-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="f0a51-101">Get-AzTag</span></span>

## <span data-ttu-id="f0a51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a51-103">預先定義 Azure 標記|在資源或訂閱上獲得整組標記。</span><span class="sxs-lookup"><span data-stu-id="f0a51-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="f0a51-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0a51-104">SYNTAX</span></span>

### <span data-ttu-id="f0a51-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0a51-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0a51-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0a51-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a51-107">描述</span><span class="sxs-lookup"><span data-stu-id="f0a51-107">DESCRIPTION</span></span>

<span data-ttu-id="f0a51-108">**GetPredefinedTagSet：Get-AzTag** Cmdlet 會取得訂閱中預先定義的 Azure 標籤。 </span><span class="sxs-lookup"><span data-stu-id="f0a51-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="f0a51-109">此 Cmdlet 會返回標籤的基本資訊，或標籤及其值的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f0a51-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="f0a51-110">所有輸出物件都包含 Count 屬性，代表已將標記和值所使用之資源和資源群組的數量。</span><span class="sxs-lookup"><span data-stu-id="f0a51-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="f0a51-111">**Get-AzTag** 是其中一部分的 Azure 標記模組可協助管理預先定義的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="f0a51-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="f0a51-112">Azure 標記是一組名稱值，可用於將 Azure 資源和資源群組分類，例如按部門或成本中心分類，或追蹤資源與群組的附注或批註。</span><span class="sxs-lookup"><span data-stu-id="f0a51-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="f0a51-113">您可以在單一步驟中定義並應用標記，但預先定義的標記讓您為訂閱中的標記建立標準、一致、可預測的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="f0a51-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="f0a51-114">若要建立預先定義的標籤，請使用 New-AzTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0a51-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="f0a51-115">若要將預先定義的標籤適用于資源群組，請使用Cmdlet New-AzTag標記參數。</span><span class="sxs-lookup"><span data-stu-id="f0a51-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="f0a51-116">若要搜尋資源群組中的特定標籤名稱或名稱與值，請使用Get-AzResourceGroup Cmdlet 的 Tag 參數。</span><span class="sxs-lookup"><span data-stu-id="f0a51-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="f0a51-117">**GetByResourceIdParameterSet：\*\*\*\*具有 ResourceId** 的 **Get-AzTag** Cmdlet 會取得資源或訂閱上的整組標籤。</span><span class="sxs-lookup"><span data-stu-id="f0a51-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="f0a51-118">例子</span><span class="sxs-lookup"><span data-stu-id="f0a51-118">EXAMPLES</span></span>

### <span data-ttu-id="f0a51-119">範例 1：取得所有預先定義的標記</span><span class="sxs-lookup"><span data-stu-id="f0a51-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="f0a51-120">此命令會獲得訂閱中所有預先定義的標記。</span><span class="sxs-lookup"><span data-stu-id="f0a51-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="f0a51-121">Count 屬性會顯示該標記已對訂閱中的資源和資源群組所使用次數。</span><span class="sxs-lookup"><span data-stu-id="f0a51-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="f0a51-122">範例 2：按名稱取得標記</span><span class="sxs-lookup"><span data-stu-id="f0a51-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="f0a51-123">此命令會獲得部門標記及其值的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f0a51-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="f0a51-124">Count 屬性會顯示標記及其每個值已對訂閱中的資源和資源群組所使用次數。</span><span class="sxs-lookup"><span data-stu-id="f0a51-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="f0a51-125">範例 3：取得所有標記的值</span><span class="sxs-lookup"><span data-stu-id="f0a51-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

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

<span data-ttu-id="f0a51-126">此命令使用 *詳細參數* 取得訂閱中所有預先定義之標記的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f0a51-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="f0a51-127">使用 *詳細* 參數相當於針對每個標記使用 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="f0a51-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="f0a51-128">範例 4：取得訂閱上的整組標記</span><span class="sxs-lookup"><span data-stu-id="f0a51-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="f0a51-129">此命令會使用 {subId} 在訂閱上獲得整組標記。</span><span class="sxs-lookup"><span data-stu-id="f0a51-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="f0a51-130">範例 5：取得資源上的整組標記</span><span class="sxs-lookup"><span data-stu-id="f0a51-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="f0a51-131">此命令會使用 {resourceId} 在資源上獲得整組標記。</span><span class="sxs-lookup"><span data-stu-id="f0a51-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="f0a51-132">參數</span><span class="sxs-lookup"><span data-stu-id="f0a51-132">PARAMETERS</span></span>

### <span data-ttu-id="f0a51-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a51-133">-DefaultProfile</span></span>
<span data-ttu-id="f0a51-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0a51-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0a51-135">-詳細資料</span><span class="sxs-lookup"><span data-stu-id="f0a51-135">-Detailed</span></span>
<span data-ttu-id="f0a51-136">表示此作業會將有關標記值的資訊新加到輸出中。</span><span class="sxs-lookup"><span data-stu-id="f0a51-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a51-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0a51-137">-Name</span></span>
<span data-ttu-id="f0a51-138">預先定義的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="f0a51-138">Name of the predefined tag.</span></span>
<span data-ttu-id="f0a51-139">根據預設 **，Get-AzTag** 會取得訂閱中所有預先定義之標記的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="f0a51-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="f0a51-140">當您指定 *Name* 參數時， *詳細參數* 沒有作用。</span><span class="sxs-lookup"><span data-stu-id="f0a51-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a51-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0a51-141">-ResourceId</span></span>
<span data-ttu-id="f0a51-142">標記實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0a51-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="f0a51-143">系統可能會標記資源、資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0a51-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a51-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a51-144">CommonParameters</span></span>
<span data-ttu-id="f0a51-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0a51-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a51-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0a51-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a51-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f0a51-147">INPUTS</span></span>

### <span data-ttu-id="f0a51-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a51-148">System.String</span></span>

### <span data-ttu-id="f0a51-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0a51-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0a51-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f0a51-150">OUTPUTS</span></span>

### <span data-ttu-id="f0a51-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag |Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="f0a51-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="f0a51-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f0a51-152">NOTES</span></span>

## <span data-ttu-id="f0a51-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0a51-153">RELATED LINKS</span></span>

[<span data-ttu-id="f0a51-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="f0a51-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="f0a51-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="f0a51-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="f0a51-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="f0a51-156">Update-AzTag</span></span>](./Update-AzTag.md)
