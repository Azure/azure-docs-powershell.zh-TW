---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7e4558d0ff48f2750ed3ac825b2358b5cad437ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916594"
---
# <span data-ttu-id="53430-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="53430-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="53430-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53430-102">SYNOPSIS</span></span>
<span data-ttu-id="53430-103">更新藍圖定義中的專案。</span><span class="sxs-lookup"><span data-stu-id="53430-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="53430-104">語法</span><span class="sxs-lookup"><span data-stu-id="53430-104">SYNTAX</span></span>

### <span data-ttu-id="53430-105">UpdateTemplateArtifact (預設) </span><span class="sxs-lookup"><span data-stu-id="53430-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53430-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="53430-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53430-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="53430-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53430-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="53430-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53430-109">描述</span><span class="sxs-lookup"><span data-stu-id="53430-109">DESCRIPTION</span></span>
<span data-ttu-id="53430-110">更新產品。</span><span class="sxs-lookup"><span data-stu-id="53430-110">Update an artifact.</span></span> <span data-ttu-id="53430-111">有兩種方法可以更新產品：透過專案 JSON 做為輸入檔案，或透過為產品提供內嵌參數。</span><span class="sxs-lookup"><span data-stu-id="53430-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="53430-112">雖然 JSON 方法不需要提供內嵌參數方法的瑕品類型，但使用者必須透過 -Type 參數提供產品類型。</span><span class="sxs-lookup"><span data-stu-id="53430-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="53430-113">例子</span><span class="sxs-lookup"><span data-stu-id="53430-113">EXAMPLES</span></span>

### <span data-ttu-id="53430-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="53430-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="53430-115">透過專案 JSON 檔案更新產品。</span><span class="sxs-lookup"><span data-stu-id="53430-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="53430-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="53430-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="53430-117">透過內嵌參數更新專案。</span><span class="sxs-lookup"><span data-stu-id="53430-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="53430-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="53430-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="53430-119">透過 ARM 範本檔案更新專案。</span><span class="sxs-lookup"><span data-stu-id="53430-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="53430-120">參數</span><span class="sxs-lookup"><span data-stu-id="53430-120">PARAMETERS</span></span>

### <span data-ttu-id="53430-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="53430-121">-ArtifactFile</span></span>
<span data-ttu-id="53430-122">在磁片上以 JSON 格式顯示之專案檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="53430-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-123">-藍圖</span><span class="sxs-lookup"><span data-stu-id="53430-123">-Blueprint</span></span>
<span data-ttu-id="53430-124">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="53430-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53430-125">-DefaultProfile</span></span>
<span data-ttu-id="53430-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53430-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53430-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="53430-127">-DependsOn</span></span>
<span data-ttu-id="53430-128">建立目前的產品之前，需要建立的專案名稱清單。</span><span class="sxs-lookup"><span data-stu-id="53430-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-129">-描述</span><span class="sxs-lookup"><span data-stu-id="53430-129">-Description</span></span>
<span data-ttu-id="53430-130">產品描述。</span><span class="sxs-lookup"><span data-stu-id="53430-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="53430-131">-Name</span></span>
<span data-ttu-id="53430-132">產品名稱</span><span class="sxs-lookup"><span data-stu-id="53430-132">Name of the artifact</span></span>

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

### <span data-ttu-id="53430-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="53430-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="53430-134">策略定義的定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="53430-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="53430-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="53430-136">要傳遞至策略定義專案的參數雜湊表。</span><span class="sxs-lookup"><span data-stu-id="53430-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53430-137">-ResourceGroupName</span></span>
<span data-ttu-id="53430-138">專案要位於下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="53430-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="53430-139">-RoleDefinitionId</span></span>
<span data-ttu-id="53430-140">角色定義清單</span><span class="sxs-lookup"><span data-stu-id="53430-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="53430-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="53430-142">角色定義主體識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="53430-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="53430-143">-TemplateFile</span></span>
<span data-ttu-id="53430-144">ARM 範本檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="53430-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="53430-145">-TemplateParameterFile</span></span>
<span data-ttu-id="53430-146">ARM 範本參數檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="53430-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-147">-類型</span><span class="sxs-lookup"><span data-stu-id="53430-147">-Type</span></span>
<span data-ttu-id="53430-148">產品類型。</span><span class="sxs-lookup"><span data-stu-id="53430-148">Type of the artifact.</span></span>
<span data-ttu-id="53430-149">支援 3 種類型：RoleAssignmentArtifact、PolicyAssignmentArtifact、TemplateArtifact。</span><span class="sxs-lookup"><span data-stu-id="53430-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53430-150">-確認</span><span class="sxs-lookup"><span data-stu-id="53430-150">-Confirm</span></span>
<span data-ttu-id="53430-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="53430-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53430-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53430-152">-WhatIf</span></span>
<span data-ttu-id="53430-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53430-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53430-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53430-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53430-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53430-155">CommonParameters</span></span>
<span data-ttu-id="53430-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53430-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53430-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53430-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53430-158">輸入</span><span class="sxs-lookup"><span data-stu-id="53430-158">INPUTS</span></span>

### <span data-ttu-id="53430-159">System.String</span><span class="sxs-lookup"><span data-stu-id="53430-159">System.String</span></span>

### <span data-ttu-id="53430-160">Microsoft.Azure.Commands.藍圖.models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="53430-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="53430-161">Microsoft.Azure.Commands.藍圖.models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="53430-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="53430-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="53430-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="53430-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53430-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="53430-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53430-164">System.String[]</span></span>

## <span data-ttu-id="53430-165">輸出</span><span class="sxs-lookup"><span data-stu-id="53430-165">OUTPUTS</span></span>

### <span data-ttu-id="53430-166">Microsoft.Azure.management.藍圖.models.Artifact</span><span class="sxs-lookup"><span data-stu-id="53430-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="53430-167">筆記</span><span class="sxs-lookup"><span data-stu-id="53430-167">NOTES</span></span>

## <span data-ttu-id="53430-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="53430-168">RELATED LINKS</span></span>
