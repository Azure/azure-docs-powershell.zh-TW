---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: 2171f99da156d86161773b039edeb884dee7a7e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906826"
---
# <span data-ttu-id="b03af-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b03af-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="b03af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b03af-102">SYNOPSIS</span></span>
<span data-ttu-id="b03af-103">獲得 Synapse Analyticss 角色指派。</span><span class="sxs-lookup"><span data-stu-id="b03af-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="b03af-104">語法</span><span class="sxs-lookup"><span data-stu-id="b03af-104">SYNTAX</span></span>

### <span data-ttu-id="b03af-105">GetByWorkspaceNameAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b03af-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03af-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03af-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b03af-115">描述</span><span class="sxs-lookup"><span data-stu-id="b03af-115">DESCRIPTION</span></span>
<span data-ttu-id="b03af-116">**Get-AzSynapseRoleAssignment Cmdlet** 會取得 Azure Synapse Analytics 角色指派。</span><span class="sxs-lookup"><span data-stu-id="b03af-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="b03af-117">如果您未指定角色定義或使用者主體名稱，此 Cmdlet 會獲得所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="b03af-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="b03af-118">例子</span><span class="sxs-lookup"><span data-stu-id="b03af-118">EXAMPLES</span></span>

### <span data-ttu-id="b03af-119">範例 1</span><span class="sxs-lookup"><span data-stu-id="b03af-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b03af-120">此命令會獲得工作區下的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="b03af-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="b03af-121">範例 2</span><span class="sxs-lookup"><span data-stu-id="b03af-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="b03af-122">此命令會獲得工作區 ContosoWorkspace 下所有角色指派與角色名稱 ContosoRole。</span><span class="sxs-lookup"><span data-stu-id="b03af-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="b03af-123">範例 3</span><span class="sxs-lookup"><span data-stu-id="b03af-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="b03af-124">此命令在工作區 ContosoWorkspace 下獲得角色指派，其角色名稱為 ContosoRole 和使用者主體名稱 ContosoName。</span><span class="sxs-lookup"><span data-stu-id="b03af-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="b03af-125">範例 4</span><span class="sxs-lookup"><span data-stu-id="b03af-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="b03af-126">此命令會透過管線在工作區下獲得所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="b03af-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="b03af-127">參數</span><span class="sxs-lookup"><span data-stu-id="b03af-127">PARAMETERS</span></span>

### <span data-ttu-id="b03af-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03af-128">-DefaultProfile</span></span>
<span data-ttu-id="b03af-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b03af-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03af-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b03af-130">-ObjectId</span></span>
<span data-ttu-id="b03af-131">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="b03af-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="b03af-132">-RoleAssignmentId</span></span>
<span data-ttu-id="b03af-133">角色指派的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b03af-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b03af-134">-RoleDefinitionId</span></span>
<span data-ttu-id="b03af-135">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="b03af-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b03af-136">-RoleDefinitionName</span></span>
<span data-ttu-id="b03af-137">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="b03af-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b03af-138">-ServicePrincipalName</span></span>
<span data-ttu-id="b03af-139">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="b03af-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b03af-140">-SignInName</span></span>
<span data-ttu-id="b03af-141">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="b03af-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b03af-142">-WorkspaceName</span></span>
<span data-ttu-id="b03af-143">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b03af-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b03af-144">-WorkspaceObject</span></span>
<span data-ttu-id="b03af-145">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b03af-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b03af-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03af-146">CommonParameters</span></span>
<span data-ttu-id="b03af-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b03af-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03af-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b03af-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03af-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b03af-149">INPUTS</span></span>

### <span data-ttu-id="b03af-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b03af-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b03af-151">輸出</span><span class="sxs-lookup"><span data-stu-id="b03af-151">OUTPUTS</span></span>

### <span data-ttu-id="b03af-152">Microsoft.Azure.Commands.Synapse.models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="b03af-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="b03af-153">筆記</span><span class="sxs-lookup"><span data-stu-id="b03af-153">NOTES</span></span>

## <span data-ttu-id="b03af-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b03af-154">RELATED LINKS</span></span>
