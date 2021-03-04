---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913334"
---
# <span data-ttu-id="d470f-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d470f-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="d470f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d470f-102">SYNOPSIS</span></span>
<span data-ttu-id="d470f-103">修改資源群組。</span><span class="sxs-lookup"><span data-stu-id="d470f-103">Modifies a resource group.</span></span>

## <span data-ttu-id="d470f-104">語法</span><span class="sxs-lookup"><span data-stu-id="d470f-104">SYNTAX</span></span>

### <span data-ttu-id="d470f-105">SetByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="d470f-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d470f-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d470f-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d470f-107">描述</span><span class="sxs-lookup"><span data-stu-id="d470f-107">DESCRIPTION</span></span>
<span data-ttu-id="d470f-108">**Set-AzResourceGroup** Cmdlet 會修改資源群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="d470f-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="d470f-109">您可以使用此 Cmdlet 來新增、變更或刪除已適用于資源群組的 Azure 標籤。</span><span class="sxs-lookup"><span data-stu-id="d470f-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="d470f-110">指定 *名稱* 參數以識別資源群組，並指定 *Tag* 參數來修改標記。</span><span class="sxs-lookup"><span data-stu-id="d470f-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="d470f-111">您無法使用此 Cmdlet 變更資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d470f-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="d470f-112">例子</span><span class="sxs-lookup"><span data-stu-id="d470f-112">EXAMPLES</span></span>

### <span data-ttu-id="d470f-113">範例 1：將標記適用于資源群組</span><span class="sxs-lookup"><span data-stu-id="d470f-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="d470f-114">此命令會將具有 IT 值的部門標記，適用于沒有現有標記的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d470f-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="d470f-115">範例 2：新增標記至資源群組</span><span class="sxs-lookup"><span data-stu-id="d470f-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="d470f-116">此範例會將具有已核准值的狀態標記和 FY2016 標記新增到具有現有標記的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d470f-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="d470f-117">由於您指定的標記會取代現有的標記，因此您必須將現有的標記納入新標記集合中，否則將會失去這些標記。</span><span class="sxs-lookup"><span data-stu-id="d470f-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="d470f-118">第一個命令會取得 ContosoRG 資源群組，並使用點方法取得其 Tags 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d470f-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="d470f-119">該命令會儲存變數中的$Tags標記。</span><span class="sxs-lookup"><span data-stu-id="d470f-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="d470f-120">第二個命令會獲得該變數$Tags標記。</span><span class="sxs-lookup"><span data-stu-id="d470f-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="d470f-121">第三個命令使用 += 工作分派運算子，將狀態和 FY2016 標記新加到變數中的$Tags陣列。</span><span class="sxs-lookup"><span data-stu-id="d470f-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="d470f-122">第四個命令使用 **Set-AzResourceGroup** 的 *Tag* 參數，將 $Tags 變數中的標籤套用至 ContosoRG 資源群組。</span><span class="sxs-lookup"><span data-stu-id="d470f-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="d470f-123">第五個命令會套用至 ContosoRG 資源群組的所有標籤。</span><span class="sxs-lookup"><span data-stu-id="d470f-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="d470f-124">輸出顯示資源群組有部門標記和兩個新標記：狀態和 FY2015。</span><span class="sxs-lookup"><span data-stu-id="d470f-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="d470f-125">範例 3：刪除資源群組的所有標記</span><span class="sxs-lookup"><span data-stu-id="d470f-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="d470f-126">此命令會指定具有空白雜湊表格值的 *Tag* 參數，以刪除 ContosoRG 資源群組的所有標籤。</span><span class="sxs-lookup"><span data-stu-id="d470f-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="d470f-127">參數</span><span class="sxs-lookup"><span data-stu-id="d470f-127">PARAMETERS</span></span>

### <span data-ttu-id="d470f-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d470f-128">-ApiVersion</span></span>
<span data-ttu-id="d470f-129">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d470f-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d470f-130">您可以指定與預設版本不同的版本。</span><span class="sxs-lookup"><span data-stu-id="d470f-130">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d470f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d470f-131">-DefaultProfile</span></span>
<span data-ttu-id="d470f-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d470f-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d470f-133">-Id</span><span class="sxs-lookup"><span data-stu-id="d470f-133">-Id</span></span>
<span data-ttu-id="d470f-134">指定要修改的資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="d470f-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d470f-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="d470f-135">-Name</span></span>
<span data-ttu-id="d470f-136">指定要修改的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d470f-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d470f-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="d470f-137">-Pre</span></span>
<span data-ttu-id="d470f-138">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d470f-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d470f-139">-標記</span><span class="sxs-lookup"><span data-stu-id="d470f-139">-Tag</span></span>
<span data-ttu-id="d470f-140">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="d470f-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d470f-141">例如：@{key0="value0";key1=$null;key2="value2"} 標記是一組名稱值，您可以建立並適用于資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="d470f-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="d470f-142">將標記指派給資源和群組後，您可以使用 Get-AzResource 和Get-AzResourceGroup 標記參數，根據標記名稱或名稱和值來搜尋資源和群組。</span><span class="sxs-lookup"><span data-stu-id="d470f-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="d470f-143">您可以使用標記來分類資源，例如按照部門或成本中心，或追蹤資源的附注或批註。</span><span class="sxs-lookup"><span data-stu-id="d470f-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="d470f-144">若要新增或變更標記，您必須取代資源群組的標記集合。</span><span class="sxs-lookup"><span data-stu-id="d470f-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="d470f-145">若要刪除標記，請從 **Get-AzResourceGroup** 輸入包含目前所有已適用于資源群組之標記的雜湊表格，但您想要刪除的標記除外。</span><span class="sxs-lookup"><span data-stu-id="d470f-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="d470f-146">若要刪除資源群組的所有標記，請指定空白雜湊表 `@{}` ：。</span><span class="sxs-lookup"><span data-stu-id="d470f-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d470f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d470f-147">CommonParameters</span></span>
<span data-ttu-id="d470f-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d470f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d470f-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d470f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d470f-150">輸入</span><span class="sxs-lookup"><span data-stu-id="d470f-150">INPUTS</span></span>

### <span data-ttu-id="d470f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d470f-151">System.String</span></span>

### <span data-ttu-id="d470f-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d470f-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d470f-153">輸出</span><span class="sxs-lookup"><span data-stu-id="d470f-153">OUTPUTS</span></span>

### <span data-ttu-id="d470f-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d470f-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="d470f-155">筆記</span><span class="sxs-lookup"><span data-stu-id="d470f-155">NOTES</span></span>

## <span data-ttu-id="d470f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="d470f-156">RELATED LINKS</span></span>

[<span data-ttu-id="d470f-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="d470f-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="d470f-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d470f-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="d470f-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d470f-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="d470f-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d470f-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
