---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 5ee859811ce791f57fc8c4fa08d2584b28bef1dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956938"
---
# <span data-ttu-id="a3f5b-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a3f5b-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="a3f5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f5b-103">建立新的專案，並將它儲存在藍圖定義中。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="a3f5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3f5b-104">SYNTAX</span></span>

### <span data-ttu-id="a3f5b-105">CreateTemplateArtifact (預設) </span><span class="sxs-lookup"><span data-stu-id="a3f5b-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f5b-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="a3f5b-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f5b-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a3f5b-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f5b-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="a3f5b-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f5b-109">說明</span><span class="sxs-lookup"><span data-stu-id="a3f5b-109">DESCRIPTION</span></span>
<span data-ttu-id="a3f5b-110">建立新的專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-110">Create a new artifact.</span></span> <span data-ttu-id="a3f5b-111">有兩種方式可以建立專案：您可以透過專案 JSON 做為輸入檔案，或提供專案的內聯參數。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="a3f5b-112">雖然 JSON 方法不需要提供內嵌參數方法的專案類型，但需要使用者提供專案到類型參數的類型。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="a3f5b-113">示例</span><span class="sxs-lookup"><span data-stu-id="a3f5b-113">EXAMPLES</span></span>

### <span data-ttu-id="a3f5b-114">範例1</span><span class="sxs-lookup"><span data-stu-id="a3f5b-114">Example 1</span></span>
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

<span data-ttu-id="a3f5b-115">透過專案 JSON 檔案建立新的專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="a3f5b-116">範例2</span><span class="sxs-lookup"><span data-stu-id="a3f5b-116">Example 2</span></span>
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

<span data-ttu-id="a3f5b-117">透過內聯參數建立新的專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-117">Create a new artifact through inline parameters.</span></span>


### <span data-ttu-id="a3f5b-118">範例3</span><span class="sxs-lookup"><span data-stu-id="a3f5b-118">Example 3</span></span>
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

<span data-ttu-id="a3f5b-119">透過 ARM 範本檔案建立新的專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="a3f5b-120">參數</span><span class="sxs-lookup"><span data-stu-id="a3f5b-120">PARAMETERS</span></span>

### <span data-ttu-id="a3f5b-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="a3f5b-121">-ArtifactFile</span></span>
<span data-ttu-id="a3f5b-122">在磁片上 JSON 格式的專案檔案位置。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-123">-藍圖</span><span class="sxs-lookup"><span data-stu-id="a3f5b-123">-Blueprint</span></span>
<span data-ttu-id="a3f5b-124">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f5b-125">-DefaultProfile</span></span>
<span data-ttu-id="a3f5b-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="a3f5b-127">-DependsOn</span></span>
<span data-ttu-id="a3f5b-128">建立目前的專案之前需要建立之專案名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-129">-描述</span><span class="sxs-lookup"><span data-stu-id="a3f5b-129">-Description</span></span>
<span data-ttu-id="a3f5b-130">專案的描述。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-130">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3f5b-131">-Name</span></span>
<span data-ttu-id="a3f5b-132">專案名稱</span><span class="sxs-lookup"><span data-stu-id="a3f5b-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a3f5b-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="a3f5b-134">原則定義的定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-134">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="a3f5b-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="a3f5b-136">要傳遞給原則定義專案的參數雜湊散數。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f5b-137">-ResourceGroupName</span></span>
<span data-ttu-id="a3f5b-138">專案要位於其中的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a3f5b-139">-RoleDefinitionId</span></span>
<span data-ttu-id="a3f5b-140">角色定義清單</span><span class="sxs-lookup"><span data-stu-id="a3f5b-140">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a3f5b-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="a3f5b-142">角色定義主體識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-142">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a3f5b-143">-TemplateFile</span></span>
<span data-ttu-id="a3f5b-144">ARM 範本檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a3f5b-145">-TemplateParameterFile</span></span>
<span data-ttu-id="a3f5b-146">ARM 範本參數檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-147">-類型</span><span class="sxs-lookup"><span data-stu-id="a3f5b-147">-Type</span></span>
<span data-ttu-id="a3f5b-148">專案的類型。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-148">Type of the artifact.</span></span>
<span data-ttu-id="a3f5b-149">支援3種類型： RoleAssignmentArtifact、PolicyAssignmentArtifact、TemplateArtifact。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f5b-150">CommonParameters</span></span>
<span data-ttu-id="a3f5b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3f5b-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f5b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="a3f5b-153">INPUTS</span></span>

### <span data-ttu-id="a3f5b-154">System.object</span><span class="sxs-lookup"><span data-stu-id="a3f5b-154">System.String</span></span>

### <span data-ttu-id="a3f5b-155">PSArtifactKind 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3f5b-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="a3f5b-156">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3f5b-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a3f5b-157">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a3f5b-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a3f5b-158">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3f5b-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a3f5b-159">System.object []</span><span class="sxs-lookup"><span data-stu-id="a3f5b-159">System.String[]</span></span>

## <span data-ttu-id="a3f5b-160">輸出</span><span class="sxs-lookup"><span data-stu-id="a3f5b-160">OUTPUTS</span></span>

### <span data-ttu-id="a3f5b-161">[Azure. 管理] 藍圖</span><span class="sxs-lookup"><span data-stu-id="a3f5b-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="a3f5b-162">筆記</span><span class="sxs-lookup"><span data-stu-id="a3f5b-162">NOTES</span></span>

## <span data-ttu-id="a3f5b-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3f5b-163">RELATED LINKS</span></span>
