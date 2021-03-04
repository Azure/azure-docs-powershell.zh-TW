---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 4fbc25b919b7fbb3caa972f4e64467dee1df7116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916456"
---
# <span data-ttu-id="7bb77-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7bb77-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="7bb77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7bb77-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb77-103">刪除 Synapse Analyticss 角色指派。</span><span class="sxs-lookup"><span data-stu-id="7bb77-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="7bb77-104">語法</span><span class="sxs-lookup"><span data-stu-id="7bb77-104">SYNTAX</span></span>

### <span data-ttu-id="7bb77-105">RemoveByWorkspaceNameAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7bb77-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb77-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb77-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb77-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb77-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb77-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb77-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb77-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb77-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb77-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb77-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb77-115">描述</span><span class="sxs-lookup"><span data-stu-id="7bb77-115">DESCRIPTION</span></span>
<span data-ttu-id="7bb77-116">**Remove-AzSynapseRoleAssignment Cmdlet** 會永久刪除 Azure Synapse Analytics 角色指派。</span><span class="sxs-lookup"><span data-stu-id="7bb77-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="7bb77-117">例子</span><span class="sxs-lookup"><span data-stu-id="7bb77-117">EXAMPLES</span></span>

### <span data-ttu-id="7bb77-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="7bb77-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="7bb77-119">此命令會刪除具有角色指派識別碼的 Azure Synapse Analytics 角色指派。</span><span class="sxs-lookup"><span data-stu-id="7bb77-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="7bb77-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="7bb77-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="7bb77-121">此命令會刪除具有角色名稱和使用者主體名稱的 Azure Synapse Analytics 角色指派。</span><span class="sxs-lookup"><span data-stu-id="7bb77-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="7bb77-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="7bb77-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="7bb77-123">此命令會刪除 Azure Synapse Analytics 角色指派，以及透過管道指派角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bb77-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="7bb77-124">參數</span><span class="sxs-lookup"><span data-stu-id="7bb77-124">PARAMETERS</span></span>

### <span data-ttu-id="7bb77-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bb77-125">-AsJob</span></span>
<span data-ttu-id="7bb77-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7bb77-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bb77-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb77-127">-DefaultProfile</span></span>
<span data-ttu-id="7bb77-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bb77-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bb77-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7bb77-129">-ObjectId</span></span>
<span data-ttu-id="7bb77-130">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="7bb77-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bb77-131">-PassThru</span></span>
<span data-ttu-id="7bb77-132">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="7bb77-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7bb77-133">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="7bb77-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7bb77-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="7bb77-134">-RoleAssignmentId</span></span>
<span data-ttu-id="7bb77-135">角色指派的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bb77-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7bb77-136">-RoleDefinitionId</span></span>
<span data-ttu-id="7bb77-137">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bb77-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7bb77-138">-RoleDefinitionName</span></span>
<span data-ttu-id="7bb77-139">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="7bb77-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7bb77-140">-ServicePrincipalName</span></span>
<span data-ttu-id="7bb77-141">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="7bb77-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7bb77-142">-SignInName</span></span>
<span data-ttu-id="7bb77-143">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="7bb77-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7bb77-144">-WorkspaceName</span></span>
<span data-ttu-id="7bb77-145">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bb77-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7bb77-146">-WorkspaceObject</span></span>
<span data-ttu-id="7bb77-147">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="7bb77-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb77-148">-確認</span><span class="sxs-lookup"><span data-stu-id="7bb77-148">-Confirm</span></span>
<span data-ttu-id="7bb77-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7bb77-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb77-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb77-150">-WhatIf</span></span>
<span data-ttu-id="7bb77-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bb77-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb77-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bb77-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb77-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb77-153">CommonParameters</span></span>
<span data-ttu-id="7bb77-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7bb77-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb77-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bb77-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb77-156">輸入</span><span class="sxs-lookup"><span data-stu-id="7bb77-156">INPUTS</span></span>

### <span data-ttu-id="7bb77-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7bb77-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7bb77-158">輸出</span><span class="sxs-lookup"><span data-stu-id="7bb77-158">OUTPUTS</span></span>

### <span data-ttu-id="7bb77-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bb77-159">System.Boolean</span></span>

## <span data-ttu-id="7bb77-160">筆記</span><span class="sxs-lookup"><span data-stu-id="7bb77-160">NOTES</span></span>

## <span data-ttu-id="7bb77-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bb77-161">RELATED LINKS</span></span>
