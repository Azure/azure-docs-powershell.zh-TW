---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138487"
---
# <span data-ttu-id="8d0da-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="8d0da-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="8d0da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d0da-102">SYNOPSIS</span></span>
<span data-ttu-id="8d0da-103">建立新的範本規格。</span><span class="sxs-lookup"><span data-stu-id="8d0da-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="8d0da-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d0da-104">SYNTAX</span></span>

### <span data-ttu-id="8d0da-105">FromJsonStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8d0da-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d0da-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d0da-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d0da-107">說明</span><span class="sxs-lookup"><span data-stu-id="8d0da-107">DESCRIPTION</span></span>
<span data-ttu-id="8d0da-108">使用指定的 ARM 範本內容建立新的範本規格版本。</span><span class="sxs-lookup"><span data-stu-id="8d0da-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="8d0da-109">內容可能是來自原始 JSON 字串， (使用 **FromJsonStringParameterSet** 參數集) 或從指定的 json 檔案（ (使用 **FromJsonFileParameterSet** 參數集) ）。</span><span class="sxs-lookup"><span data-stu-id="8d0da-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="8d0da-110">如果根範本規格還不存在，則會與範本規格版本建立。</span><span class="sxs-lookup"><span data-stu-id="8d0da-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="8d0da-111">如果已存在具有指定名稱的範本規格，則會在 (任何其他現有版本保留) 中，更新指定的版本。</span><span class="sxs-lookup"><span data-stu-id="8d0da-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="8d0da-112">示例</span><span class="sxs-lookup"><span data-stu-id="8d0da-112">EXAMPLES</span></span>

### <span data-ttu-id="8d0da-113">範例1：</span><span class="sxs-lookup"><span data-stu-id="8d0da-113">Example 1:</span></span>
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

<span data-ttu-id="8d0da-114">在名為 "myTemplateSpec" 的範本規範中，建立新的範本規格版本 "v 1.0"。</span><span class="sxs-lookup"><span data-stu-id="8d0da-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="8d0da-115">指定的版本將 $templateJson 為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="8d0da-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="8d0da-116">**注意：** 這個範例中的 ARM 範本是不含實際資源的 [非 op]。</span><span class="sxs-lookup"><span data-stu-id="8d0da-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="8d0da-117">範例2：</span><span class="sxs-lookup"><span data-stu-id="8d0da-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="8d0da-118">在名為 "myTemplateSpec" 的範本規範中，建立新的範本規格版本 "v 2.0"。</span><span class="sxs-lookup"><span data-stu-id="8d0da-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="8d0da-119">指定的版本會將本機檔案 "myTemplateContent.js的內容] 做為版本的 ARM 範本內容。</span><span class="sxs-lookup"><span data-stu-id="8d0da-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="8d0da-120">參數</span><span class="sxs-lookup"><span data-stu-id="8d0da-120">PARAMETERS</span></span>

### <span data-ttu-id="8d0da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d0da-121">-DefaultProfile</span></span>
<span data-ttu-id="8d0da-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d0da-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d0da-123">-描述</span><span class="sxs-lookup"><span data-stu-id="8d0da-123">-Description</span></span>
<span data-ttu-id="8d0da-124">範本規格的描述。</span><span class="sxs-lookup"><span data-stu-id="8d0da-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="8d0da-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8d0da-125">-DisplayName</span></span>
<span data-ttu-id="8d0da-126">範本規格的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8d0da-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="8d0da-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8d0da-127">-Force</span></span>
<span data-ttu-id="8d0da-128">覆寫現有版本時不要求確認。</span><span class="sxs-lookup"><span data-stu-id="8d0da-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="8d0da-129">-位置</span><span class="sxs-lookup"><span data-stu-id="8d0da-129">-Location</span></span>
<span data-ttu-id="8d0da-130">範本規格的位置。只有在範本規格尚不存在時才需要。</span><span class="sxs-lookup"><span data-stu-id="8d0da-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="8d0da-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d0da-131">-Name</span></span>
<span data-ttu-id="8d0da-132">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d0da-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="8d0da-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d0da-133">-ResourceGroupName</span></span>
<span data-ttu-id="8d0da-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d0da-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d0da-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8d0da-135">-TemplateFile</span></span>
<span data-ttu-id="8d0da-136">本機 Azure 資源管理器範本 JSON 檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="8d0da-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="8d0da-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="8d0da-137">-TemplateJson</span></span>
<span data-ttu-id="8d0da-138">Azure 資源管理器範本 JSON。</span><span class="sxs-lookup"><span data-stu-id="8d0da-138">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="8d0da-139">-版本</span><span class="sxs-lookup"><span data-stu-id="8d0da-139">-Version</span></span>
<span data-ttu-id="8d0da-140">範本規格的版本。</span><span class="sxs-lookup"><span data-stu-id="8d0da-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="8d0da-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="8d0da-141">-VersionDescription</span></span>
<span data-ttu-id="8d0da-142">版本的描述。</span><span class="sxs-lookup"><span data-stu-id="8d0da-142">The description of the version.</span></span>

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

### <span data-ttu-id="8d0da-143">-確認</span><span class="sxs-lookup"><span data-stu-id="8d0da-143">-Confirm</span></span>
<span data-ttu-id="8d0da-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d0da-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d0da-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d0da-145">-WhatIf</span></span>
<span data-ttu-id="8d0da-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d0da-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d0da-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d0da-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d0da-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0da-148">CommonParameters</span></span>
<span data-ttu-id="8d0da-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d0da-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0da-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d0da-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0da-151">輸入</span><span class="sxs-lookup"><span data-stu-id="8d0da-151">INPUTS</span></span>

### <span data-ttu-id="8d0da-152">System.object</span><span class="sxs-lookup"><span data-stu-id="8d0da-152">System.String</span></span>

## <span data-ttu-id="8d0da-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8d0da-153">OUTPUTS</span></span>

### <span data-ttu-id="8d0da-154">PSTemplateSpec 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="8d0da-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="8d0da-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8d0da-155">NOTES</span></span>

## <span data-ttu-id="8d0da-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d0da-156">RELATED LINKS</span></span>
