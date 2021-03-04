---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: e431e1e9186cdaf0ec722b5a609a3f0a9f186bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907306"
---
# <span data-ttu-id="28dd6-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28dd6-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="28dd6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="28dd6-103">獲得資源群組。</span><span class="sxs-lookup"><span data-stu-id="28dd6-103">Gets resource groups.</span></span>

## <span data-ttu-id="28dd6-104">語法</span><span class="sxs-lookup"><span data-stu-id="28dd6-104">SYNTAX</span></span>

### <span data-ttu-id="28dd6-105">GetByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="28dd6-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28dd6-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="28dd6-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28dd6-107">描述</span><span class="sxs-lookup"><span data-stu-id="28dd6-107">DESCRIPTION</span></span>
<span data-ttu-id="28dd6-108">**Get-AzResourceGroup** Cmdlet 會取得目前訂閱中的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="28dd6-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="28dd6-109">您可以取得所有資源群組，或根據名稱或其他屬性指定資源群組。</span><span class="sxs-lookup"><span data-stu-id="28dd6-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="28dd6-110">根據預設，此 Cmdlet 會獲得目前訂閱的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="28dd6-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="28dd6-111">有關 Azure 資源與 Azure 資源群組的資訊，請參閱 New-AzResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28dd6-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="28dd6-112">例子</span><span class="sxs-lookup"><span data-stu-id="28dd6-112">EXAMPLES</span></span>

### <span data-ttu-id="28dd6-113">範例 1：根據名稱取得資源群組</span><span class="sxs-lookup"><span data-stu-id="28dd6-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="28dd6-114">此命令會獲得您訂閱中名為 EngineerBlog 的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="28dd6-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="28dd6-115">範例 2：取得資源群組的所有標記</span><span class="sxs-lookup"><span data-stu-id="28dd6-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="28dd6-116">此命令會獲得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="28dd6-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="28dd6-117">範例 3：根據標記取得資源群組</span><span class="sxs-lookup"><span data-stu-id="28dd6-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="28dd6-118">範例 4：根據位置顯示資源群組</span><span class="sxs-lookup"><span data-stu-id="28dd6-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="28dd6-119">範例 5：顯示特定位置中所有資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="28dd6-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="28dd6-120">範例 6：顯示名稱以 WebServer 開頭的資源群組</span><span class="sxs-lookup"><span data-stu-id="28dd6-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="28dd6-121">參數</span><span class="sxs-lookup"><span data-stu-id="28dd6-121">PARAMETERS</span></span>

### <span data-ttu-id="28dd6-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="28dd6-122">-ApiVersion</span></span>
<span data-ttu-id="28dd6-123">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="28dd6-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="28dd6-124">您可以指定與預設版本不同的版本。</span><span class="sxs-lookup"><span data-stu-id="28dd6-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="28dd6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28dd6-125">-DefaultProfile</span></span>
<span data-ttu-id="28dd6-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="28dd6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28dd6-127">-Id</span><span class="sxs-lookup"><span data-stu-id="28dd6-127">-Id</span></span>
<span data-ttu-id="28dd6-128">指定要取得的資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="28dd6-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="28dd6-129">不允許萬用字元。</span><span class="sxs-lookup"><span data-stu-id="28dd6-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28dd6-130">-位置</span><span class="sxs-lookup"><span data-stu-id="28dd6-130">-Location</span></span>
<span data-ttu-id="28dd6-131">指定要取得的資源群組位置。</span><span class="sxs-lookup"><span data-stu-id="28dd6-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="28dd6-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="28dd6-132">-Name</span></span>
<span data-ttu-id="28dd6-133">指定要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="28dd6-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="28dd6-134">此參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="28dd6-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="28dd6-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="28dd6-135">-Pre</span></span>
<span data-ttu-id="28dd6-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="28dd6-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="28dd6-137">-標記</span><span class="sxs-lookup"><span data-stu-id="28dd6-137">-Tag</span></span>
<span data-ttu-id="28dd6-138">可篩選資源群組的標記雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28dd6-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28dd6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28dd6-139">CommonParameters</span></span>
<span data-ttu-id="28dd6-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28dd6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28dd6-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28dd6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28dd6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="28dd6-142">INPUTS</span></span>

### <span data-ttu-id="28dd6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="28dd6-143">System.String</span></span>

### <span data-ttu-id="28dd6-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="28dd6-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="28dd6-145">輸出</span><span class="sxs-lookup"><span data-stu-id="28dd6-145">OUTPUTS</span></span>

### <span data-ttu-id="28dd6-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28dd6-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="28dd6-147">筆記</span><span class="sxs-lookup"><span data-stu-id="28dd6-147">NOTES</span></span>

## <span data-ttu-id="28dd6-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="28dd6-148">RELATED LINKS</span></span>

[<span data-ttu-id="28dd6-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28dd6-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="28dd6-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28dd6-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="28dd6-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28dd6-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

