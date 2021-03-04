---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 48a700f29a80b03df0fd4fc2d858dcb1c1c57f76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909466"
---
# <span data-ttu-id="75dc1-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="75dc1-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="75dc1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="75dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="75dc1-103">修改範本規格。</span><span class="sxs-lookup"><span data-stu-id="75dc1-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="75dc1-104">語法</span><span class="sxs-lookup"><span data-stu-id="75dc1-104">SYNTAX</span></span>

### <span data-ttu-id="75dc1-105">FromJsonStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="75dc1-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75dc1-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dc1-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dc1-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dc1-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dc1-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dc1-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dc1-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dc1-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dc1-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dc1-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dc1-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dc1-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75dc1-112">描述</span><span class="sxs-lookup"><span data-stu-id="75dc1-112">DESCRIPTION</span></span>
<span data-ttu-id="75dc1-113">修改 Templace 規格。如果指定名稱和/或特定版本的範本規格不存在，將會建立範本規格。</span><span class="sxs-lookup"><span data-stu-id="75dc1-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="75dc1-114">修改範本規格版本的 ARM 範本內容時，內容可能來自原始 JSON 字串 (使用 **UpdateVersionByNameFromJsonParameterSet** 參數集) 或來自指定的 JSON 檔案 (使用 **UpdateVersionByNameFromJsonFileParameterSet** 參數集) 。</span><span class="sxs-lookup"><span data-stu-id="75dc1-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="75dc1-115">例子</span><span class="sxs-lookup"><span data-stu-id="75dc1-115">EXAMPLES</span></span>

### <span data-ttu-id="75dc1-116">範例 1：</span><span class="sxs-lookup"><span data-stu-id="75dc1-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="75dc1-117">修改名為"myTemplateSpec"的範本規格版本"v1.0"。</span><span class="sxs-lookup"><span data-stu-id="75dc1-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="75dc1-118">指定的版本會$templateJson做為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="75dc1-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="75dc1-119">如果根範本規格和/或版本不存在，將會建立它們。</span><span class="sxs-lookup"><span data-stu-id="75dc1-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="75dc1-120">**筆記：**</span><span class="sxs-lookup"><span data-stu-id="75dc1-120">**Notes:**</span></span> 

* <span data-ttu-id="75dc1-121">範例中的 ARM 範本沒有作用，因為它不包含實際資源。</span><span class="sxs-lookup"><span data-stu-id="75dc1-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="75dc1-122">只有當範本規格不存在時，才需要位置</span><span class="sxs-lookup"><span data-stu-id="75dc1-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="75dc1-123">範例 2：</span><span class="sxs-lookup"><span data-stu-id="75dc1-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="75dc1-124">修改名為"myTemplateSpec"的範本規格版本"v2.0"。</span><span class="sxs-lookup"><span data-stu-id="75dc1-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="75dc1-125">指定的版本將具有來自本地檔案「myTemplateContent.js」的內容做為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="75dc1-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="75dc1-126">如果根範本規格和/或版本不存在，將會建立它們。</span><span class="sxs-lookup"><span data-stu-id="75dc1-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="75dc1-127">**注意：** 只有當範本規格不存在時，才需要位置</span><span class="sxs-lookup"><span data-stu-id="75dc1-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="75dc1-128">範例 3：</span><span class="sxs-lookup"><span data-stu-id="75dc1-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="75dc1-129">修改資源群組 "myRG" 中名為 "myTemplateSpec" 的範本規格描述。</span><span class="sxs-lookup"><span data-stu-id="75dc1-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="75dc1-130">如果範本規格不存在，將會建立範本規格。</span><span class="sxs-lookup"><span data-stu-id="75dc1-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="75dc1-131">**注意：** 只有當範本規格不存在時，才需要位置</span><span class="sxs-lookup"><span data-stu-id="75dc1-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="75dc1-132">參數</span><span class="sxs-lookup"><span data-stu-id="75dc1-132">PARAMETERS</span></span>

### <span data-ttu-id="75dc1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dc1-133">-DefaultProfile</span></span>
<span data-ttu-id="75dc1-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="75dc1-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75dc1-135">-描述</span><span class="sxs-lookup"><span data-stu-id="75dc1-135">-Description</span></span>
<span data-ttu-id="75dc1-136">範本規格的描述。</span><span class="sxs-lookup"><span data-stu-id="75dc1-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75dc1-137">-DisplayName</span></span>
<span data-ttu-id="75dc1-138">範本規格的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="75dc1-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-139">-位置</span><span class="sxs-lookup"><span data-stu-id="75dc1-139">-Location</span></span>
<span data-ttu-id="75dc1-140">範本規格的位置。只有在範本規格不存在時才需要。</span><span class="sxs-lookup"><span data-stu-id="75dc1-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="75dc1-141">-Name</span></span>
<span data-ttu-id="75dc1-142">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="75dc1-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75dc1-143">-ResourceGroupName</span></span>
<span data-ttu-id="75dc1-144">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75dc1-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75dc1-145">-ResourceId</span></span>
<span data-ttu-id="75dc1-146">範本規格的完全合格的資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="75dc1-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-147">-標記</span><span class="sxs-lookup"><span data-stu-id="75dc1-147">-Tag</span></span>
<span data-ttu-id="75dc1-148">範本規格和/或版本的標記雜湊表</span><span class="sxs-lookup"><span data-stu-id="75dc1-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="75dc1-149">-TemplateFile</span></span>
<span data-ttu-id="75dc1-150">本地 Azure Resource Manager 範本 JSON 檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="75dc1-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="75dc1-151">-TemplateJson</span></span>
<span data-ttu-id="75dc1-152">Azure Resource Manager 範本 JSON。</span><span class="sxs-lookup"><span data-stu-id="75dc1-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-153">-版本</span><span class="sxs-lookup"><span data-stu-id="75dc1-153">-Version</span></span>
<span data-ttu-id="75dc1-154">範本規格的版本。</span><span class="sxs-lookup"><span data-stu-id="75dc1-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="75dc1-155">-VersionDescription</span></span>
<span data-ttu-id="75dc1-156">版本的描述。</span><span class="sxs-lookup"><span data-stu-id="75dc1-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-157">-確認</span><span class="sxs-lookup"><span data-stu-id="75dc1-157">-Confirm</span></span>
<span data-ttu-id="75dc1-158">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="75dc1-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75dc1-159">-WhatIf</span></span>
<span data-ttu-id="75dc1-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75dc1-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75dc1-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75dc1-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dc1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dc1-162">CommonParameters</span></span>
<span data-ttu-id="75dc1-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="75dc1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dc1-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75dc1-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dc1-165">輸入</span><span class="sxs-lookup"><span data-stu-id="75dc1-165">INPUTS</span></span>

### <span data-ttu-id="75dc1-166">System.String</span><span class="sxs-lookup"><span data-stu-id="75dc1-166">System.String</span></span>

## <span data-ttu-id="75dc1-167">輸出</span><span class="sxs-lookup"><span data-stu-id="75dc1-167">OUTPUTS</span></span>

### <span data-ttu-id="75dc1-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="75dc1-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="75dc1-169">筆記</span><span class="sxs-lookup"><span data-stu-id="75dc1-169">NOTES</span></span>

## <span data-ttu-id="75dc1-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="75dc1-170">RELATED LINKS</span></span>
