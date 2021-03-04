---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 7e216a6d2751ddd24e7d948cb6cca036c2a9b336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907941"
---
# <span data-ttu-id="fd2b3-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fd2b3-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="fd2b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2b3-103">建立 Synapse Analyticss 角色指派。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fd2b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd2b3-104">SYNTAX</span></span>

### <span data-ttu-id="fd2b3-105">NewByWorkspaceNameAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fd2b3-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2b3-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd2b3-113">描述</span><span class="sxs-lookup"><span data-stu-id="fd2b3-113">DESCRIPTION</span></span>
<span data-ttu-id="fd2b3-114">**New-AzSynapseRoleAssignment Cmdlet** 會建立 Azure Synapse Analytics 角色指派。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fd2b3-115">例子</span><span class="sxs-lookup"><span data-stu-id="fd2b3-115">EXAMPLES</span></span>

### <span data-ttu-id="fd2b3-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="fd2b3-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="fd2b3-117">此命令會指派 ContosoRole 給主體名稱為 ContosoName 的使用者。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="fd2b3-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="fd2b3-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="fd2b3-119">此命令會指派 ContosoRole 給使用者，其主體名稱為 ContosoName 透過管線。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="fd2b3-120">參數</span><span class="sxs-lookup"><span data-stu-id="fd2b3-120">PARAMETERS</span></span>

### <span data-ttu-id="fd2b3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd2b3-121">-AsJob</span></span>
<span data-ttu-id="fd2b3-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fd2b3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd2b3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2b3-123">-DefaultProfile</span></span>
<span data-ttu-id="fd2b3-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd2b3-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fd2b3-125">-ObjectId</span></span>
<span data-ttu-id="fd2b3-126">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fd2b3-127">-RoleDefinitionId</span></span>
<span data-ttu-id="fd2b3-128">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fd2b3-129">-RoleDefinitionName</span></span>
<span data-ttu-id="fd2b3-130">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd2b3-131">-ServicePrincipalName</span></span>
<span data-ttu-id="fd2b3-132">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="fd2b3-133">-SignInName</span></span>
<span data-ttu-id="fd2b3-134">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd2b3-135">-WorkspaceName</span></span>
<span data-ttu-id="fd2b3-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fd2b3-137">-WorkspaceObject</span></span>
<span data-ttu-id="fd2b3-138">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2b3-139">-確認</span><span class="sxs-lookup"><span data-stu-id="fd2b3-139">-Confirm</span></span>
<span data-ttu-id="fd2b3-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2b3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2b3-141">-WhatIf</span></span>
<span data-ttu-id="fd2b3-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd2b3-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2b3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2b3-144">CommonParameters</span></span>
<span data-ttu-id="fd2b3-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd2b3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2b3-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd2b3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2b3-147">輸入</span><span class="sxs-lookup"><span data-stu-id="fd2b3-147">INPUTS</span></span>

### <span data-ttu-id="fd2b3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd2b3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fd2b3-149">輸出</span><span class="sxs-lookup"><span data-stu-id="fd2b3-149">OUTPUTS</span></span>

### <span data-ttu-id="fd2b3-150">Microsoft.Azure.Commands.Synapse.models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="fd2b3-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="fd2b3-151">筆記</span><span class="sxs-lookup"><span data-stu-id="fd2b3-151">NOTES</span></span>

## <span data-ttu-id="fd2b3-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd2b3-152">RELATED LINKS</span></span>
