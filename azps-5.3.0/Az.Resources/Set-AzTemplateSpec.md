---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435385"
---
# <span data-ttu-id="5c479-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="5c479-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="5c479-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c479-102">SYNOPSIS</span></span>
<span data-ttu-id="5c479-103">修改範本規格。</span><span class="sxs-lookup"><span data-stu-id="5c479-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="5c479-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c479-104">SYNTAX</span></span>

### <span data-ttu-id="5c479-105">FromJsonStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5c479-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c479-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c479-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c479-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c479-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c479-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c479-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c479-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c479-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c479-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c479-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c479-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c479-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c479-112">說明</span><span class="sxs-lookup"><span data-stu-id="5c479-112">DESCRIPTION</span></span>
<span data-ttu-id="5c479-113">修改 Templace 規格。如果指定名稱與/或特定版本的範本規格尚不存在，則會建立。</span><span class="sxs-lookup"><span data-stu-id="5c479-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="5c479-114">在修改範本規格版本的 ARM 範本內容時，內容可能是來自原始的 JSON 字串， (使用 **UpdateVersionByNameFromJsonParameterSet** 參數集) 或從指定的 json 檔案（ (使用 **UpdateVersionByNameFromJsonFileParameterSet** 參數集) ）。</span><span class="sxs-lookup"><span data-stu-id="5c479-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="5c479-115">示例</span><span class="sxs-lookup"><span data-stu-id="5c479-115">EXAMPLES</span></span>

### <span data-ttu-id="5c479-116">範例1：</span><span class="sxs-lookup"><span data-stu-id="5c479-116">Example 1:</span></span>
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

<span data-ttu-id="5c479-117">修改名為 "myTemplateSpec" 的範本規格 "v 1.0" 版本。</span><span class="sxs-lookup"><span data-stu-id="5c479-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="5c479-118">指定的版本將 $templateJson 為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="5c479-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="5c479-119">如果根範本規格與/或版本還不存在，就會建立它們。</span><span class="sxs-lookup"><span data-stu-id="5c479-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="5c479-120">**筆記**</span><span class="sxs-lookup"><span data-stu-id="5c479-120">**Notes:**</span></span> 

* <span data-ttu-id="5c479-121">這個範例中的 ARM 範本是不含實際資源的 [非 op]。</span><span class="sxs-lookup"><span data-stu-id="5c479-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="5c479-122">只有範本規格不存在時，才需要位置</span><span class="sxs-lookup"><span data-stu-id="5c479-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="5c479-123">範例2：</span><span class="sxs-lookup"><span data-stu-id="5c479-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="5c479-124">修改名為 "myTemplateSpec" 的範本規格 "v 2.0" 版本。</span><span class="sxs-lookup"><span data-stu-id="5c479-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="5c479-125">指定的版本會將本機檔案 "myTemplateContent.js的內容] 做為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="5c479-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="5c479-126">如果根範本規格與/或版本還不存在，就會建立它們。</span><span class="sxs-lookup"><span data-stu-id="5c479-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="5c479-127">**注意：** 只有範本規格不存在時，才需要位置</span><span class="sxs-lookup"><span data-stu-id="5c479-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="5c479-128">範例3：</span><span class="sxs-lookup"><span data-stu-id="5c479-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="5c479-129">修改資源群組 "myRG" 中名為 "myTemplateSpec" 的範本規格的描述。</span><span class="sxs-lookup"><span data-stu-id="5c479-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="5c479-130">如果範本規格還不存在，則會建立。</span><span class="sxs-lookup"><span data-stu-id="5c479-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="5c479-131">**注意：** 只有範本規格不存在時，才需要位置</span><span class="sxs-lookup"><span data-stu-id="5c479-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="5c479-132">參數</span><span class="sxs-lookup"><span data-stu-id="5c479-132">PARAMETERS</span></span>

### <span data-ttu-id="5c479-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c479-133">-DefaultProfile</span></span>
<span data-ttu-id="5c479-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c479-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c479-135">-描述</span><span class="sxs-lookup"><span data-stu-id="5c479-135">-Description</span></span>
<span data-ttu-id="5c479-136">範本規格的描述。</span><span class="sxs-lookup"><span data-stu-id="5c479-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="5c479-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5c479-137">-DisplayName</span></span>
<span data-ttu-id="5c479-138">範本規格的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5c479-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="5c479-139">-位置</span><span class="sxs-lookup"><span data-stu-id="5c479-139">-Location</span></span>
<span data-ttu-id="5c479-140">範本規格的位置。只有在範本規格尚不存在時才需要。</span><span class="sxs-lookup"><span data-stu-id="5c479-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="5c479-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c479-141">-Name</span></span>
<span data-ttu-id="5c479-142">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c479-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="5c479-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c479-143">-ResourceGroupName</span></span>
<span data-ttu-id="5c479-144">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c479-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c479-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c479-145">-ResourceId</span></span>
<span data-ttu-id="5c479-146">範本規格的完全限定資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="5c479-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="5c479-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c479-147">-Tag</span></span>
<span data-ttu-id="5c479-148">範本規格與/或版本的標記雜湊</span><span class="sxs-lookup"><span data-stu-id="5c479-148">Hashtable of tags for the template spec and/or version</span></span>

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

### <span data-ttu-id="5c479-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5c479-149">-TemplateFile</span></span>
<span data-ttu-id="5c479-150">本機 Azure 資源管理器範本 JSON 檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5c479-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="5c479-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="5c479-151">-TemplateJson</span></span>
<span data-ttu-id="5c479-152">Azure 資源管理器範本 JSON。</span><span class="sxs-lookup"><span data-stu-id="5c479-152">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="5c479-153">-版本</span><span class="sxs-lookup"><span data-stu-id="5c479-153">-Version</span></span>
<span data-ttu-id="5c479-154">範本規格的版本。</span><span class="sxs-lookup"><span data-stu-id="5c479-154">The version of the template spec.</span></span>

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

### <span data-ttu-id="5c479-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="5c479-155">-VersionDescription</span></span>
<span data-ttu-id="5c479-156">版本的描述。</span><span class="sxs-lookup"><span data-stu-id="5c479-156">The description of the version.</span></span>

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

### <span data-ttu-id="5c479-157">-確認</span><span class="sxs-lookup"><span data-stu-id="5c479-157">-Confirm</span></span>
<span data-ttu-id="5c479-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c479-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c479-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c479-159">-WhatIf</span></span>
<span data-ttu-id="5c479-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c479-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c479-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c479-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c479-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c479-162">CommonParameters</span></span>
<span data-ttu-id="5c479-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c479-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c479-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c479-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c479-165">輸入</span><span class="sxs-lookup"><span data-stu-id="5c479-165">INPUTS</span></span>

### <span data-ttu-id="5c479-166">System.object</span><span class="sxs-lookup"><span data-stu-id="5c479-166">System.String</span></span>

## <span data-ttu-id="5c479-167">輸出</span><span class="sxs-lookup"><span data-stu-id="5c479-167">OUTPUTS</span></span>

### <span data-ttu-id="5c479-168">PSTemplateSpec 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="5c479-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="5c479-169">筆記</span><span class="sxs-lookup"><span data-stu-id="5c479-169">NOTES</span></span>

## <span data-ttu-id="5c479-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c479-170">RELATED LINKS</span></span>
