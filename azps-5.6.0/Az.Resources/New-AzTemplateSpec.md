---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 72c668f195024ac88e6d8ed67c08c6db6d0e3445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907534"
---
# <span data-ttu-id="a18d0-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="a18d0-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="a18d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a18d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a18d0-103">建立新範本規格。</span><span class="sxs-lookup"><span data-stu-id="a18d0-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="a18d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="a18d0-104">SYNTAX</span></span>

### <span data-ttu-id="a18d0-105">FromJsonStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a18d0-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a18d0-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18d0-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a18d0-107">描述</span><span class="sxs-lookup"><span data-stu-id="a18d0-107">DESCRIPTION</span></span>
<span data-ttu-id="a18d0-108">使用指定的 ARM 範本內容建立新範本規格版本。</span><span class="sxs-lookup"><span data-stu-id="a18d0-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="a18d0-109">內容可能來自原始 JSON 字串 (使用 **FromJsonStringParameterSet** 參數集) 或來自指定的 JSON 檔案 (使用 **FromJsonFileParameterSet** 參數集) 。</span><span class="sxs-lookup"><span data-stu-id="a18d0-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="a18d0-110">如果根範本規格不存在，將會與範本規格版本一起建立。</span><span class="sxs-lookup"><span data-stu-id="a18d0-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="a18d0-111">如果已有指定名稱的範本規格，該範本規格和指定的版本將會更新 (任何其他現有版本都會保留) 。</span><span class="sxs-lookup"><span data-stu-id="a18d0-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="a18d0-112">例子</span><span class="sxs-lookup"><span data-stu-id="a18d0-112">EXAMPLES</span></span>

### <span data-ttu-id="a18d0-113">範例 1：</span><span class="sxs-lookup"><span data-stu-id="a18d0-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="a18d0-114">在名為 "myTemplateSpec" 的範本規格中，建立新的範本規格版本 "v1.0"。</span><span class="sxs-lookup"><span data-stu-id="a18d0-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="a18d0-115">指定的版本會$templateJson做為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="a18d0-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="a18d0-116">**注意：** 範例中的 ARM 範本沒有作用，因為它不包含實際資源。</span><span class="sxs-lookup"><span data-stu-id="a18d0-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="a18d0-117">範例 2：</span><span class="sxs-lookup"><span data-stu-id="a18d0-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="a18d0-118">在名為 "myTemplateSpec" 的範本規格中，建立新的範本規格版本 "v2.0"。</span><span class="sxs-lookup"><span data-stu-id="a18d0-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="a18d0-119">指定的版本將具有來自本地檔案「myTemplateContent.js」的內容做為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="a18d0-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="a18d0-120">參數</span><span class="sxs-lookup"><span data-stu-id="a18d0-120">PARAMETERS</span></span>

### <span data-ttu-id="a18d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18d0-121">-DefaultProfile</span></span>
<span data-ttu-id="a18d0-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a18d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18d0-123">-描述</span><span class="sxs-lookup"><span data-stu-id="a18d0-123">-Description</span></span>
<span data-ttu-id="a18d0-124">範本規格的描述。</span><span class="sxs-lookup"><span data-stu-id="a18d0-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="a18d0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a18d0-125">-DisplayName</span></span>
<span data-ttu-id="a18d0-126">範本規格的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a18d0-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="a18d0-127">-強制</span><span class="sxs-lookup"><span data-stu-id="a18d0-127">-Force</span></span>
<span data-ttu-id="a18d0-128">覆寫現有版本時，請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="a18d0-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="a18d0-129">-位置</span><span class="sxs-lookup"><span data-stu-id="a18d0-129">-Location</span></span>
<span data-ttu-id="a18d0-130">範本規格的位置。只有在範本規格不存在時才需要。</span><span class="sxs-lookup"><span data-stu-id="a18d0-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="a18d0-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="a18d0-131">-Name</span></span>
<span data-ttu-id="a18d0-132">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="a18d0-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18d0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18d0-133">-ResourceGroupName</span></span>
<span data-ttu-id="a18d0-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a18d0-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="a18d0-135">-標記</span><span class="sxs-lookup"><span data-stu-id="a18d0-135">-Tag</span></span>
<span data-ttu-id="a18d0-136">新範本規格資源的標記雜湊表 () 。</span><span class="sxs-lookup"><span data-stu-id="a18d0-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="a18d0-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a18d0-137">-TemplateFile</span></span>
<span data-ttu-id="a18d0-138">本地 Azure Resource Manager 範本 JSON 檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="a18d0-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18d0-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="a18d0-139">-TemplateJson</span></span>
<span data-ttu-id="a18d0-140">Azure Resource Manager 範本 JSON。</span><span class="sxs-lookup"><span data-stu-id="a18d0-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18d0-141">-版本</span><span class="sxs-lookup"><span data-stu-id="a18d0-141">-Version</span></span>
<span data-ttu-id="a18d0-142">範本規格的版本。</span><span class="sxs-lookup"><span data-stu-id="a18d0-142">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18d0-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="a18d0-143">-VersionDescription</span></span>
<span data-ttu-id="a18d0-144">版本的描述。</span><span class="sxs-lookup"><span data-stu-id="a18d0-144">The description of the version.</span></span>

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

### <span data-ttu-id="a18d0-145">-確認</span><span class="sxs-lookup"><span data-stu-id="a18d0-145">-Confirm</span></span>
<span data-ttu-id="a18d0-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a18d0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a18d0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a18d0-147">-WhatIf</span></span>
<span data-ttu-id="a18d0-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a18d0-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a18d0-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a18d0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a18d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18d0-150">CommonParameters</span></span>
<span data-ttu-id="a18d0-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a18d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18d0-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a18d0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18d0-153">輸入</span><span class="sxs-lookup"><span data-stu-id="a18d0-153">INPUTS</span></span>

### <span data-ttu-id="a18d0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a18d0-154">System.String</span></span>

## <span data-ttu-id="a18d0-155">輸出</span><span class="sxs-lookup"><span data-stu-id="a18d0-155">OUTPUTS</span></span>

### <span data-ttu-id="a18d0-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="a18d0-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="a18d0-157">筆記</span><span class="sxs-lookup"><span data-stu-id="a18d0-157">NOTES</span></span>

## <span data-ttu-id="a18d0-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="a18d0-158">RELATED LINKS</span></span>
