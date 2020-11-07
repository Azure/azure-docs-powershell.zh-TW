---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625679"
---
# <span data-ttu-id="38bf0-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38bf0-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="38bf0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="38bf0-103">修改資源群組。</span><span class="sxs-lookup"><span data-stu-id="38bf0-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38bf0-104">句法</span><span class="sxs-lookup"><span data-stu-id="38bf0-104">SYNTAX</span></span>

### <span data-ttu-id="38bf0-105">根據名稱列出 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="38bf0-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="38bf0-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="38bf0-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38bf0-107">根據 [識別碼] 列出 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="38bf0-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38bf0-108">說明</span><span class="sxs-lookup"><span data-stu-id="38bf0-108">DESCRIPTION</span></span>
<span data-ttu-id="38bf0-109">**AzureRmResourceGroup** Cmdlet 會修改資源群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="38bf0-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="38bf0-110">您可以使用此 Cmdlet 來新增、變更或刪除套用至資源群組的 Azure 標記。</span><span class="sxs-lookup"><span data-stu-id="38bf0-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="38bf0-111">指定 *Name* 參數來識別 [資源] 群組，以及要修改標籤的 *標記* 參數。</span><span class="sxs-lookup"><span data-stu-id="38bf0-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="38bf0-112">您無法使用這個 Cmdlet 來變更資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38bf0-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="38bf0-113">示例</span><span class="sxs-lookup"><span data-stu-id="38bf0-113">EXAMPLES</span></span>

### <span data-ttu-id="38bf0-114">範例1：將標籤套用至資源群組</span><span class="sxs-lookup"><span data-stu-id="38bf0-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="38bf0-115">這個命令會將部門標籤的值套用至沒有現有標籤的資源群組。</span><span class="sxs-lookup"><span data-stu-id="38bf0-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="38bf0-116">範例2：新增標籤至資源群組</span><span class="sxs-lookup"><span data-stu-id="38bf0-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="38bf0-117">這個範例會將狀態標記加上已核准的值，並將 [FY2016] 標籤新增至含有現有標記的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="38bf0-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="38bf0-118">因為您指定的標記會取代現有的標記，所以您必須將現有的標記包含在新的標記集合中，否則您就會遺失它們。</span><span class="sxs-lookup"><span data-stu-id="38bf0-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="38bf0-119">第一個命令會取得 ContosoRG 資源群組，並使用點方法來取得其 Tags 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="38bf0-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="38bf0-120">該命令會將標記儲存在 $Tags 變數中。</span><span class="sxs-lookup"><span data-stu-id="38bf0-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="38bf0-121">第二個命令會取得 $Tags 變數中的標記。</span><span class="sxs-lookup"><span data-stu-id="38bf0-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="38bf0-122">第三個命令使用 + = 指派運算子，將 Status 及 FY2016 標籤新增至 $Tags 變數中的標記陣列。</span><span class="sxs-lookup"><span data-stu-id="38bf0-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="38bf0-123">第四個命令使用 **AzureRmResourceGroup 設定** 的 *Tag* 參數，將 $Tags 變數中的標籤套用至 ContosoRG 資源群組。</span><span class="sxs-lookup"><span data-stu-id="38bf0-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="38bf0-124">第五個命令會取得套用至 ContosoRG 資源群組的所有標記。</span><span class="sxs-lookup"><span data-stu-id="38bf0-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="38bf0-125">[輸出] 會顯示 [資源] 群組具有 [部門] 標記，以及兩個新的標籤： [狀態] 和 [FY2015]。</span><span class="sxs-lookup"><span data-stu-id="38bf0-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="38bf0-126">範例3：刪除資源群組的所有標籤</span><span class="sxs-lookup"><span data-stu-id="38bf0-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="38bf0-127">這個命令會將 *Tag* 參數指定為空白的雜湊資料表值，以刪除 ContosoRG 資源群組中的所有標記。</span><span class="sxs-lookup"><span data-stu-id="38bf0-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="38bf0-128">參數</span><span class="sxs-lookup"><span data-stu-id="38bf0-128">PARAMETERS</span></span>

### <span data-ttu-id="38bf0-129">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38bf0-129">-ApiVersion</span></span>
<span data-ttu-id="38bf0-130">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="38bf0-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="38bf0-131">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="38bf0-131">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="38bf0-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="38bf0-132">-Id</span></span>
<span data-ttu-id="38bf0-133">指定要修改之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38bf0-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bf0-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="38bf0-134">-Name</span></span>
<span data-ttu-id="38bf0-135">指定要修改之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38bf0-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38bf0-136">-預先</span><span class="sxs-lookup"><span data-stu-id="38bf0-136">-Pre</span></span>
<span data-ttu-id="38bf0-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="38bf0-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="38bf0-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="38bf0-138">-Tag</span></span>
<span data-ttu-id="38bf0-139">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="38bf0-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="38bf0-140">例如：</span><span class="sxs-lookup"><span data-stu-id="38bf0-140">For example:</span></span>

<span data-ttu-id="38bf0-141">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="38bf0-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="38bf0-142">標記是您可以建立並套用至資源和資源群組的名稱-值對。</span><span class="sxs-lookup"><span data-stu-id="38bf0-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="38bf0-143">在您指派標籤至資源和群組之後，您可以使用 Get-AzureRmResource 和 Get-AzureRmResourceGroup 的 *tag* 參數，依標記名稱或名稱和值來搜尋資源和群組。</span><span class="sxs-lookup"><span data-stu-id="38bf0-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="38bf0-144">您可以使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="38bf0-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="38bf0-145">若要新增或變更標記，您必須取代資源群組的標記集合。</span><span class="sxs-lookup"><span data-stu-id="38bf0-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="38bf0-146">若要刪除標籤，請輸入目前已套用至資源群組的所有標籤的雜湊資料表（從 **AzureRmResourceGroup** ，除了您要刪除的標記之外）。</span><span class="sxs-lookup"><span data-stu-id="38bf0-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="38bf0-147">若要刪除資源群組中的所有標記，請指定空的雜湊資料表： `@{}` 。</span><span class="sxs-lookup"><span data-stu-id="38bf0-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="38bf0-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bf0-148">-DefaultProfile</span></span>
<span data-ttu-id="38bf0-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38bf0-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38bf0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bf0-150">CommonParameters</span></span>
<span data-ttu-id="38bf0-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38bf0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bf0-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38bf0-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bf0-153">輸入</span><span class="sxs-lookup"><span data-stu-id="38bf0-153">INPUTS</span></span>

### <span data-ttu-id="38bf0-154">所有</span><span class="sxs-lookup"><span data-stu-id="38bf0-154">None</span></span>

## <span data-ttu-id="38bf0-155">輸出</span><span class="sxs-lookup"><span data-stu-id="38bf0-155">OUTPUTS</span></span>

### <span data-ttu-id="38bf0-156">PSResourceGroup 中的 .Resources。</span><span class="sxs-lookup"><span data-stu-id="38bf0-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="38bf0-157">筆記</span><span class="sxs-lookup"><span data-stu-id="38bf0-157">NOTES</span></span>

## <span data-ttu-id="38bf0-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="38bf0-158">RELATED LINKS</span></span>

[<span data-ttu-id="38bf0-159">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="38bf0-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="38bf0-160">AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38bf0-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="38bf0-161">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38bf0-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="38bf0-162">移除-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38bf0-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
