---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129285"
---
# <span data-ttu-id="e9c00-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9c00-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="e9c00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9c00-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c00-103">修改資源群組。</span><span class="sxs-lookup"><span data-stu-id="e9c00-103">Modifies a resource group.</span></span>

## <span data-ttu-id="e9c00-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9c00-104">SYNTAX</span></span>

### <span data-ttu-id="e9c00-105">SetByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="e9c00-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9c00-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e9c00-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9c00-107">說明</span><span class="sxs-lookup"><span data-stu-id="e9c00-107">DESCRIPTION</span></span>
<span data-ttu-id="e9c00-108">**AzResourceGroup** Cmdlet 會修改資源群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9c00-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="e9c00-109">您可以使用此 Cmdlet 來新增、變更或刪除套用至資源群組的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="e9c00-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="e9c00-110">指定 *Name* 參數來識別 [資源] 群組，以及要修改標籤的 *標記* 參數。</span><span class="sxs-lookup"><span data-stu-id="e9c00-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="e9c00-111">您無法使用這個 Cmdlet 來變更資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c00-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="e9c00-112">示例</span><span class="sxs-lookup"><span data-stu-id="e9c00-112">EXAMPLES</span></span>

### <span data-ttu-id="e9c00-113">範例1：將標籤套用至資源群組</span><span class="sxs-lookup"><span data-stu-id="e9c00-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="e9c00-114">這個命令會將部門標籤的值套用至沒有現有標籤的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e9c00-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="e9c00-115">範例2：新增標籤至資源群組</span><span class="sxs-lookup"><span data-stu-id="e9c00-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="e9c00-116">這個範例會將狀態標記加上已核准的值，並將 [FY2016] 標籤新增至含有現有標記的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="e9c00-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="e9c00-117">因為您指定的標記會取代現有的標記，所以您必須將現有的標記包含在新的標記集合中，否則您就會遺失它們。</span><span class="sxs-lookup"><span data-stu-id="e9c00-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="e9c00-118">第一個命令會取得 ContosoRG 資源群組，並使用點方法來取得其 Tags 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e9c00-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="e9c00-119">該命令會將標記儲存在 $Tags 變數中。</span><span class="sxs-lookup"><span data-stu-id="e9c00-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="e9c00-120">第二個命令會取得 $Tags 變數中的標記。</span><span class="sxs-lookup"><span data-stu-id="e9c00-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="e9c00-121">第三個命令使用 + = 指派運算子，將 Status 及 FY2016 標籤新增至 $Tags 變數中的標記陣列。</span><span class="sxs-lookup"><span data-stu-id="e9c00-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="e9c00-122">第四個命令使用 **AzResourceGroup 設定** 的 *Tag* 參數，將 $Tags 變數中的標籤套用至 ContosoRG 資源群組。</span><span class="sxs-lookup"><span data-stu-id="e9c00-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="e9c00-123">第五個命令會取得套用至 ContosoRG 資源群組的所有標記。</span><span class="sxs-lookup"><span data-stu-id="e9c00-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="e9c00-124">[輸出] 會顯示 [資源] 群組具有 [部門] 標記，以及兩個新的標籤： [狀態] 和 [FY2015]。</span><span class="sxs-lookup"><span data-stu-id="e9c00-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="e9c00-125">範例3：刪除資源群組的所有標籤</span><span class="sxs-lookup"><span data-stu-id="e9c00-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="e9c00-126">這個命令會將 *Tag* 參數指定為空白的雜湊資料表值，以刪除 ContosoRG 資源群組中的所有標記。</span><span class="sxs-lookup"><span data-stu-id="e9c00-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="e9c00-127">參數</span><span class="sxs-lookup"><span data-stu-id="e9c00-127">PARAMETERS</span></span>

### <span data-ttu-id="e9c00-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e9c00-128">-ApiVersion</span></span>
<span data-ttu-id="e9c00-129">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e9c00-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e9c00-130">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="e9c00-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e9c00-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c00-131">-DefaultProfile</span></span>
<span data-ttu-id="e9c00-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e9c00-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9c00-133">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e9c00-133">-Id</span></span>
<span data-ttu-id="e9c00-134">指定要修改之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9c00-134">Specifies the ID of the resource group to modify.</span></span>

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

### <span data-ttu-id="e9c00-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9c00-135">-Name</span></span>
<span data-ttu-id="e9c00-136">指定要修改之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c00-136">Specifies the name of the resource group to modify.</span></span>

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

### <span data-ttu-id="e9c00-137">-預先</span><span class="sxs-lookup"><span data-stu-id="e9c00-137">-Pre</span></span>
<span data-ttu-id="e9c00-138">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e9c00-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e9c00-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9c00-139">-Tag</span></span>
<span data-ttu-id="e9c00-140">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e9c00-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9c00-141">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"} 標記是您可以建立並套用至資源和資源群組的名稱值對。</span><span class="sxs-lookup"><span data-stu-id="e9c00-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="e9c00-142">在您指派標籤至資源和群組之後，您可以使用 Get-AzResource 和 Get-AzResourceGroup 的 *tag* 參數，依標記名稱或名稱和值來搜尋資源和群組。</span><span class="sxs-lookup"><span data-stu-id="e9c00-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="e9c00-143">您可以使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="e9c00-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="e9c00-144">若要新增或變更標記，您必須取代資源群組的標記集合。</span><span class="sxs-lookup"><span data-stu-id="e9c00-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="e9c00-145">若要刪除標籤，請輸入目前已套用至資源群組的所有標籤的雜湊資料表（從 **AzResourceGroup** ，除了您要刪除的標記之外）。</span><span class="sxs-lookup"><span data-stu-id="e9c00-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="e9c00-146">若要刪除資源群組中的所有標記，請指定空的雜湊資料表： `@{}` 。</span><span class="sxs-lookup"><span data-stu-id="e9c00-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="e9c00-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c00-147">CommonParameters</span></span>
<span data-ttu-id="e9c00-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9c00-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c00-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9c00-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c00-150">輸入</span><span class="sxs-lookup"><span data-stu-id="e9c00-150">INPUTS</span></span>

### <span data-ttu-id="e9c00-151">System.object</span><span class="sxs-lookup"><span data-stu-id="e9c00-151">System.String</span></span>

### <span data-ttu-id="e9c00-152">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9c00-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9c00-153">輸出</span><span class="sxs-lookup"><span data-stu-id="e9c00-153">OUTPUTS</span></span>

### <span data-ttu-id="e9c00-154">PSResourceGroup 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="e9c00-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="e9c00-155">筆記</span><span class="sxs-lookup"><span data-stu-id="e9c00-155">NOTES</span></span>

## <span data-ttu-id="e9c00-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9c00-156">RELATED LINKS</span></span>

[<span data-ttu-id="e9c00-157">AzResource</span><span class="sxs-lookup"><span data-stu-id="e9c00-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="e9c00-158">AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9c00-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="e9c00-159">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9c00-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="e9c00-160">移除-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9c00-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
