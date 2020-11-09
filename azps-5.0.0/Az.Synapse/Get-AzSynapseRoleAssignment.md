---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286740"
---
# <span data-ttu-id="305a9-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="305a9-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="305a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="305a9-102">SYNOPSIS</span></span>
<span data-ttu-id="305a9-103">取得 Synapse 分析角色指派。</span><span class="sxs-lookup"><span data-stu-id="305a9-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="305a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="305a9-104">SYNTAX</span></span>

### <span data-ttu-id="305a9-105">GetByWorkspaceNameAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="305a9-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305a9-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="305a9-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="305a9-115">說明</span><span class="sxs-lookup"><span data-stu-id="305a9-115">DESCRIPTION</span></span>
<span data-ttu-id="305a9-116">**AzSynapseRoleAssignment** Cmdlet 會取得 Azure Synapse Analytics 角色分派。</span><span class="sxs-lookup"><span data-stu-id="305a9-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="305a9-117">如果您沒有指定角色定義或使用者主要名稱，此 Cmdlet 會取得所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="305a9-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="305a9-118">示例</span><span class="sxs-lookup"><span data-stu-id="305a9-118">EXAMPLES</span></span>

### <span data-ttu-id="305a9-119">範例1</span><span class="sxs-lookup"><span data-stu-id="305a9-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="305a9-120">這個命令會在工作區中取得所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="305a9-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="305a9-121">範例2</span><span class="sxs-lookup"><span data-stu-id="305a9-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="305a9-122">這個命令會以角色名稱 ContosoRole 來取得 [工作區 ContosoWorkspace] 下的所有角色分派。</span><span class="sxs-lookup"><span data-stu-id="305a9-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="305a9-123">範例3</span><span class="sxs-lookup"><span data-stu-id="305a9-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="305a9-124">這個命令會在 [工作區 ContosoWorkspace] 下以 [角色名稱 ContosoRole] 和 [使用者主要名稱] ContosoName 來取得角色分派。</span><span class="sxs-lookup"><span data-stu-id="305a9-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="305a9-125">範例4</span><span class="sxs-lookup"><span data-stu-id="305a9-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="305a9-126">這個命令會透過管線在工作區下取得所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="305a9-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="305a9-127">參數</span><span class="sxs-lookup"><span data-stu-id="305a9-127">PARAMETERS</span></span>

### <span data-ttu-id="305a9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305a9-128">-DefaultProfile</span></span>
<span data-ttu-id="305a9-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="305a9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="305a9-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="305a9-130">-ObjectId</span></span>
<span data-ttu-id="305a9-131">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="305a9-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="305a9-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="305a9-132">-RoleAssignmentId</span></span>
<span data-ttu-id="305a9-133">角色指派的識別碼。</span><span class="sxs-lookup"><span data-stu-id="305a9-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="305a9-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="305a9-134">-RoleDefinitionId</span></span>
<span data-ttu-id="305a9-135">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="305a9-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="305a9-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="305a9-136">-RoleDefinitionName</span></span>
<span data-ttu-id="305a9-137">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="305a9-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="305a9-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="305a9-138">-ServicePrincipalName</span></span>
<span data-ttu-id="305a9-139">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="305a9-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="305a9-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="305a9-140">-SignInName</span></span>
<span data-ttu-id="305a9-141">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="305a9-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="305a9-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="305a9-142">-WorkspaceName</span></span>
<span data-ttu-id="305a9-143">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="305a9-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="305a9-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="305a9-144">-WorkspaceObject</span></span>
<span data-ttu-id="305a9-145">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="305a9-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="305a9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305a9-146">CommonParameters</span></span>
<span data-ttu-id="305a9-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="305a9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305a9-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="305a9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305a9-149">輸入</span><span class="sxs-lookup"><span data-stu-id="305a9-149">INPUTS</span></span>

### <span data-ttu-id="305a9-150">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="305a9-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="305a9-151">輸出</span><span class="sxs-lookup"><span data-stu-id="305a9-151">OUTPUTS</span></span>

### <span data-ttu-id="305a9-152">PSRoleAssignmentDetails 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="305a9-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="305a9-153">筆記</span><span class="sxs-lookup"><span data-stu-id="305a9-153">NOTES</span></span>

## <span data-ttu-id="305a9-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="305a9-154">RELATED LINKS</span></span>
