---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 82d0d3667371485d079785dbdb2f87eb8284aa94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902637"
---
# <span data-ttu-id="8cca1-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="8cca1-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="8cca1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8cca1-102">SYNOPSIS</span></span>
<span data-ttu-id="8cca1-103">建立新產品，並將其儲存在藍圖定義中。</span><span class="sxs-lookup"><span data-stu-id="8cca1-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="8cca1-104">語法</span><span class="sxs-lookup"><span data-stu-id="8cca1-104">SYNTAX</span></span>

### <span data-ttu-id="8cca1-105">CreateTemplateArtifact (預設) </span><span class="sxs-lookup"><span data-stu-id="8cca1-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cca1-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="8cca1-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cca1-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="8cca1-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cca1-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="8cca1-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cca1-109">描述</span><span class="sxs-lookup"><span data-stu-id="8cca1-109">DESCRIPTION</span></span>
<span data-ttu-id="8cca1-110">建立新產品。</span><span class="sxs-lookup"><span data-stu-id="8cca1-110">Create a new artifact.</span></span> <span data-ttu-id="8cca1-111">有兩種方法可以建立製作品：一種是透過製作 JSON 做為輸入檔案，一種是透過為產品提供內嵌參數。</span><span class="sxs-lookup"><span data-stu-id="8cca1-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="8cca1-112">雖然 JSON 方法不需要提供內嵌參數方法的瑕品類型，但使用者必須透過 -Type 參數提供產品類型。</span><span class="sxs-lookup"><span data-stu-id="8cca1-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="8cca1-113">例子</span><span class="sxs-lookup"><span data-stu-id="8cca1-113">EXAMPLES</span></span>

### <span data-ttu-id="8cca1-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="8cca1-114">Example 1</span></span>
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

<span data-ttu-id="8cca1-115">透過專案 JSON 檔案建立新產品。</span><span class="sxs-lookup"><span data-stu-id="8cca1-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="8cca1-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="8cca1-116">Example 2</span></span>
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

<span data-ttu-id="8cca1-117">透過內嵌參數建立新產品。</span><span class="sxs-lookup"><span data-stu-id="8cca1-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="8cca1-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="8cca1-118">Example 3</span></span>
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

<span data-ttu-id="8cca1-119">透過 ARM 範本檔案建立新產品。</span><span class="sxs-lookup"><span data-stu-id="8cca1-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="8cca1-120">參數</span><span class="sxs-lookup"><span data-stu-id="8cca1-120">PARAMETERS</span></span>

### <span data-ttu-id="8cca1-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="8cca1-121">-ArtifactFile</span></span>
<span data-ttu-id="8cca1-122">在磁片上以 JSON 格式顯示之專案檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="8cca1-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-123">-藍圖</span><span class="sxs-lookup"><span data-stu-id="8cca1-123">-Blueprint</span></span>
<span data-ttu-id="8cca1-124">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="8cca1-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cca1-125">-DefaultProfile</span></span>
<span data-ttu-id="8cca1-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cca1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cca1-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="8cca1-127">-DependsOn</span></span>
<span data-ttu-id="8cca1-128">建立目前的產品之前，需要建立的專案名稱清單。</span><span class="sxs-lookup"><span data-stu-id="8cca1-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-129">-描述</span><span class="sxs-lookup"><span data-stu-id="8cca1-129">-Description</span></span>
<span data-ttu-id="8cca1-130">產品描述。</span><span class="sxs-lookup"><span data-stu-id="8cca1-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="8cca1-131">-Name</span></span>
<span data-ttu-id="8cca1-132">產品名稱</span><span class="sxs-lookup"><span data-stu-id="8cca1-132">Name of the artifact</span></span>

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

### <span data-ttu-id="8cca1-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8cca1-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="8cca1-134">策略定義的定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="8cca1-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="8cca1-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="8cca1-136">要傳遞至策略定義專案的參數雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8cca1-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cca1-137">-ResourceGroupName</span></span>
<span data-ttu-id="8cca1-138">專案要位於下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8cca1-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8cca1-139">-RoleDefinitionId</span></span>
<span data-ttu-id="8cca1-140">角色定義清單</span><span class="sxs-lookup"><span data-stu-id="8cca1-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="8cca1-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="8cca1-142">角色定義主體識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="8cca1-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8cca1-143">-TemplateFile</span></span>
<span data-ttu-id="8cca1-144">ARM 範本檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="8cca1-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8cca1-145">-TemplateParameterFile</span></span>
<span data-ttu-id="8cca1-146">ARM 範本參數檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="8cca1-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-147">-類型</span><span class="sxs-lookup"><span data-stu-id="8cca1-147">-Type</span></span>
<span data-ttu-id="8cca1-148">產品類型。</span><span class="sxs-lookup"><span data-stu-id="8cca1-148">Type of the artifact.</span></span>
<span data-ttu-id="8cca1-149">支援 3 種類型：RoleAssignmentArtifact、PolicyAssignmentArtifact、TemplateArtifact。</span><span class="sxs-lookup"><span data-stu-id="8cca1-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cca1-150">-確認</span><span class="sxs-lookup"><span data-stu-id="8cca1-150">-Confirm</span></span>
<span data-ttu-id="8cca1-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8cca1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cca1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cca1-152">-WhatIf</span></span>
<span data-ttu-id="8cca1-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8cca1-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cca1-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8cca1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cca1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cca1-155">CommonParameters</span></span>
<span data-ttu-id="8cca1-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8cca1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cca1-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cca1-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cca1-158">輸入</span><span class="sxs-lookup"><span data-stu-id="8cca1-158">INPUTS</span></span>

### <span data-ttu-id="8cca1-159">System.String</span><span class="sxs-lookup"><span data-stu-id="8cca1-159">System.String</span></span>

### <span data-ttu-id="8cca1-160">Microsoft.Azure.Commands.藍圖.models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="8cca1-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="8cca1-161">Microsoft.Azure.Commands.藍圖.models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="8cca1-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="8cca1-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8cca1-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8cca1-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8cca1-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8cca1-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8cca1-164">System.String[]</span></span>

## <span data-ttu-id="8cca1-165">輸出</span><span class="sxs-lookup"><span data-stu-id="8cca1-165">OUTPUTS</span></span>

### <span data-ttu-id="8cca1-166">Microsoft.Azure.management.藍圖.models.Artifact</span><span class="sxs-lookup"><span data-stu-id="8cca1-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="8cca1-167">筆記</span><span class="sxs-lookup"><span data-stu-id="8cca1-167">NOTES</span></span>

## <span data-ttu-id="8cca1-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cca1-168">RELATED LINKS</span></span>
