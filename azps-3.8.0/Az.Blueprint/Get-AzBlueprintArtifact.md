---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: d8541285cb8cef0565a06715910ff5b8cc8cc392
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796809"
---
# <span data-ttu-id="988e5-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="988e5-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="988e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="988e5-102">SYNOPSIS</span></span>
<span data-ttu-id="988e5-103">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="988e5-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="988e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="988e5-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="988e5-105">DESCRIPTION</span></span>
<span data-ttu-id="988e5-106">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="988e5-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="988e5-107">如果沒有指定藍圖定義版本，就會檢索草稿版本。</span><span class="sxs-lookup"><span data-stu-id="988e5-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="988e5-108">在沒有草稿版本的情況下，會傳回最新發佈的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="988e5-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="988e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="988e5-109">EXAMPLES</span></span>

### <span data-ttu-id="988e5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="988e5-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="988e5-111">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="988e5-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="988e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="988e5-112">PARAMETERS</span></span>

### <span data-ttu-id="988e5-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="988e5-113">-ArtifactFile</span></span>
<span data-ttu-id="988e5-114">在磁片上 JSON 格式的專案檔案位置。</span><span class="sxs-lookup"><span data-stu-id="988e5-114">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="988e5-115">-藍圖</span><span class="sxs-lookup"><span data-stu-id="988e5-115">-Blueprint</span></span>
<span data-ttu-id="988e5-116">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="988e5-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="988e5-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="988e5-117">-BlueprintVersion</span></span>
<span data-ttu-id="988e5-118">取得工件的藍圖版本。</span><span class="sxs-lookup"><span data-stu-id="988e5-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988e5-119">-DefaultProfile</span></span>
<span data-ttu-id="988e5-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="988e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988e5-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="988e5-121">-DependsOn</span></span>
<span data-ttu-id="988e5-122">建立目前的專案之前需要建立之專案名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="988e5-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="988e5-123">-描述</span><span class="sxs-lookup"><span data-stu-id="988e5-123">-Description</span></span>
<span data-ttu-id="988e5-124">專案的描述。</span><span class="sxs-lookup"><span data-stu-id="988e5-124">Description of the artifact.</span></span>

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

### <span data-ttu-id="988e5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="988e5-125">-Name</span></span>
<span data-ttu-id="988e5-126">專案名稱</span><span class="sxs-lookup"><span data-stu-id="988e5-126">Name of the artifact</span></span>

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

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="988e5-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="988e5-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="988e5-128">原則定義的定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="988e5-128">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="988e5-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="988e5-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="988e5-130">要傳遞給原則定義專案的參數雜湊散數。</span><span class="sxs-lookup"><span data-stu-id="988e5-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="988e5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988e5-131">-ResourceGroupName</span></span>
<span data-ttu-id="988e5-132">專案要位於其中的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="988e5-132">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="988e5-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="988e5-133">-RoleDefinitionId</span></span>
<span data-ttu-id="988e5-134">角色定義清單</span><span class="sxs-lookup"><span data-stu-id="988e5-134">List of role definition</span></span>

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

### <span data-ttu-id="988e5-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="988e5-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="988e5-136">角色定義主體識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="988e5-136">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="988e5-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="988e5-137">-TemplateFile</span></span>
<span data-ttu-id="988e5-138">ARM 範本檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="988e5-138">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="988e5-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="988e5-139">-TemplateParameterFile</span></span>
<span data-ttu-id="988e5-140">ARM 範本參數檔案在磁片上的位置。</span><span class="sxs-lookup"><span data-stu-id="988e5-140">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="988e5-141">-類型</span><span class="sxs-lookup"><span data-stu-id="988e5-141">-Type</span></span>
<span data-ttu-id="988e5-142">專案的類型。</span><span class="sxs-lookup"><span data-stu-id="988e5-142">Type of the artifact.</span></span>
<span data-ttu-id="988e5-143">支援3種類型： RoleAssignmentArtifact、PolicyAssignmentArtifact、TemplateArtifact。</span><span class="sxs-lookup"><span data-stu-id="988e5-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="988e5-144">-確認</span><span class="sxs-lookup"><span data-stu-id="988e5-144">-Confirm</span></span>
<span data-ttu-id="988e5-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="988e5-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988e5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988e5-146">-WhatIf</span></span>
<span data-ttu-id="988e5-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="988e5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988e5-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="988e5-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988e5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988e5-149">CommonParameters</span></span>
<span data-ttu-id="988e5-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="988e5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="988e5-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="988e5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988e5-152">輸入</span><span class="sxs-lookup"><span data-stu-id="988e5-152">INPUTS</span></span>

### <span data-ttu-id="988e5-153">System.object</span><span class="sxs-lookup"><span data-stu-id="988e5-153">System.String</span></span>

### <span data-ttu-id="988e5-154">PSArtifactKind 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="988e5-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="988e5-155">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="988e5-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="988e5-156">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="988e5-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="988e5-157">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="988e5-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="988e5-158">System.object []</span><span class="sxs-lookup"><span data-stu-id="988e5-158">System.String[]</span></span>

## <span data-ttu-id="988e5-159">輸出</span><span class="sxs-lookup"><span data-stu-id="988e5-159">OUTPUTS</span></span>

### <span data-ttu-id="988e5-160">PSBlueprintAssignment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="988e5-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="988e5-161">筆記</span><span class="sxs-lookup"><span data-stu-id="988e5-161">NOTES</span></span>

## <span data-ttu-id="988e5-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="988e5-162">RELATED LINKS</span></span>
