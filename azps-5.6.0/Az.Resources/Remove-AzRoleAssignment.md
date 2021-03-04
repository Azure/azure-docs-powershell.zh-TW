---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d941e5cc3bf4a3f2363aa8369a7f5b0518ba2e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915905"
---
# <span data-ttu-id="61cee-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61cee-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="61cee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61cee-102">SYNOPSIS</span></span>
<span data-ttu-id="61cee-103">移除指派給特定範圍中特定角色之指定主體的角色指派。</span><span class="sxs-lookup"><span data-stu-id="61cee-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="61cee-104">語法</span><span class="sxs-lookup"><span data-stu-id="61cee-104">SYNTAX</span></span>

### <span data-ttu-id="61cee-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61cee-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cee-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cee-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61cee-117">描述</span><span class="sxs-lookup"><span data-stu-id="61cee-117">DESCRIPTION</span></span>
<span data-ttu-id="61cee-118">使用 Remove-AzRoleAssignment命令小命令，以在給定範圍和所給予的角色中撤銷任何主體的存取權。</span><span class="sxs-lookup"><span data-stu-id="61cee-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="61cee-119">工作分派的物件，即必須指定主體。</span><span class="sxs-lookup"><span data-stu-id="61cee-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="61cee-120">主體可以是使用者 (使用 SignInName 或 ObjectId 參數來識別使用者) ，安全性群組 (會使用 ObjectId 參數來識別群組) 或服務主體 (使用 ServicePrincipalName 或 ObjectId 參數來識別 ServicePrincipal。</span><span class="sxs-lookup"><span data-stu-id="61cee-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="61cee-121">必須使用 RoleDefinitionName 參數指定指派給主體的角色。</span><span class="sxs-lookup"><span data-stu-id="61cee-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="61cee-122">您可以指定指派的範圍，如果未指定，會預設為訂閱範圍，即會嘗試刪除訂閱範圍中指定主體和角色的指派。</span><span class="sxs-lookup"><span data-stu-id="61cee-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="61cee-123">您可以使用下列其中一個參數來指定工作分派的範圍。</span><span class="sxs-lookup"><span data-stu-id="61cee-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="61cee-124">a。</span><span class="sxs-lookup"><span data-stu-id="61cee-124">a.</span></span>
<span data-ttu-id="61cee-125">範圍 - 這是從 /subscriptions/b 開始完整範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="61cee-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="61cee-126">ResourceGroupName - 訂閱下任何資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61cee-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="61cee-127">C。</span><span class="sxs-lookup"><span data-stu-id="61cee-127">c.</span></span>
<span data-ttu-id="61cee-128">ResourceName、ResourceType、ResourceGroupName 和 (選) ParentResource - 識別訂閱下的特定資源。</span><span class="sxs-lookup"><span data-stu-id="61cee-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="61cee-129">例子</span><span class="sxs-lookup"><span data-stu-id="61cee-129">EXAMPLES</span></span>

### <span data-ttu-id="61cee-130">範例 1</span><span class="sxs-lookup"><span data-stu-id="61cee-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="61cee-131">移除在 rg1 資源組範圍中指派給讀取者 john.doe@contoso.com 角色的角色指派。</span><span class="sxs-lookup"><span data-stu-id="61cee-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="61cee-132">範例 2</span><span class="sxs-lookup"><span data-stu-id="61cee-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="61cee-133">移除指派給 ObjectId 識別並指派給讀取者角色之群組主體的角色指派。</span><span class="sxs-lookup"><span data-stu-id="61cee-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="61cee-134">預設會使用目前的訂閱做為範圍，以尋找要刪除的指派。</span><span class="sxs-lookup"><span data-stu-id="61cee-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="61cee-135">範例 3</span><span class="sxs-lookup"><span data-stu-id="61cee-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="61cee-136">移除從命令小命令中抓取的第一Get-AzRoleAssignment物件。</span><span class="sxs-lookup"><span data-stu-id="61cee-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="61cee-137">參數</span><span class="sxs-lookup"><span data-stu-id="61cee-137">PARAMETERS</span></span>

### <span data-ttu-id="61cee-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61cee-138">-DefaultProfile</span></span>
<span data-ttu-id="61cee-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="61cee-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61cee-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61cee-140">-InputObject</span></span>
<span data-ttu-id="61cee-141">角色指派物件。</span><span class="sxs-lookup"><span data-stu-id="61cee-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="61cee-142">-ObjectId</span></span>
<span data-ttu-id="61cee-143">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="61cee-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="61cee-144">-ParentResource</span></span>
<span data-ttu-id="61cee-145">階層中的父資源 (ResourceName 參數指定之資源的) ，如果有。</span><span class="sxs-lookup"><span data-stu-id="61cee-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="61cee-146">必須與 ResourceGroupName、ResourceType 和 ResourceName 參數一起使用，以識別資源的相對 URI 形式建構階層式範圍。</span><span class="sxs-lookup"><span data-stu-id="61cee-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61cee-147">-PassThru</span></span>
<span data-ttu-id="61cee-148">如果指定，會顯示已刪除的角色指派</span><span class="sxs-lookup"><span data-stu-id="61cee-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="61cee-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61cee-149">-ResourceGroupName</span></span>
<span data-ttu-id="61cee-150">角色指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="61cee-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="61cee-151">嘗試刪除指定資源群組範圍中的工作分派。</span><span class="sxs-lookup"><span data-stu-id="61cee-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="61cee-152">當與 ResourceName、ResourceType 和 (選擇性地) ParentResource 參數一起使用時，該命令會以可識別資源的相對 URI 形式建構階層式範圍。</span><span class="sxs-lookup"><span data-stu-id="61cee-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="61cee-153">-ResourceName</span></span>
<span data-ttu-id="61cee-154">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="61cee-154">The resource name.</span></span>
<span data-ttu-id="61cee-155">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="61cee-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="61cee-156">您必須與 ResourceGroupName、ResourceType 和 (選擇性地) ParentResource 參數一起使用，以相對 URI 形式建構階層式範圍，以識別資源並刪除該範圍中的工作分派。</span><span class="sxs-lookup"><span data-stu-id="61cee-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="61cee-157">-ResourceType</span></span>
<span data-ttu-id="61cee-158">資源類型。</span><span class="sxs-lookup"><span data-stu-id="61cee-158">The resource type.</span></span>
<span data-ttu-id="61cee-159">例如，Microsoft.Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="61cee-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="61cee-160">您必須與 ResourceGroupName、ResourceName 和 (選擇性地) ParentResource 參數一起使用，以相對 URI 形式建構階層式範圍，以識別資源並刪除該資源範圍中的工作分派。</span><span class="sxs-lookup"><span data-stu-id="61cee-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="61cee-161">-RoleDefinitionId</span></span>
<span data-ttu-id="61cee-162">需要刪除工作分派之 RBAC 角色的識別碼。</span><span class="sxs-lookup"><span data-stu-id="61cee-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="61cee-163">-RoleDefinitionName</span></span>
<span data-ttu-id="61cee-164">需要刪除作業的 RBAC 角色名稱，例如讀取者、參與者、虛擬網路管理員等。</span><span class="sxs-lookup"><span data-stu-id="61cee-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-165">-範圍</span><span class="sxs-lookup"><span data-stu-id="61cee-165">-Scope</span></span>
<span data-ttu-id="61cee-166">要刪除的角色指派範圍。</span><span class="sxs-lookup"><span data-stu-id="61cee-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="61cee-167">以相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="61cee-167">In the format of relative URI.</span></span>
<span data-ttu-id="61cee-168">例如"/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG"。</span><span class="sxs-lookup"><span data-stu-id="61cee-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="61cee-169">如果未指定，將會嘗試刪除訂閱層級的角色。</span><span class="sxs-lookup"><span data-stu-id="61cee-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="61cee-170">如果指定，應該從"/subscriptions/{id}"開始。</span><span class="sxs-lookup"><span data-stu-id="61cee-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="61cee-171">-ServicePrincipalName</span></span>
<span data-ttu-id="61cee-172">Azure AD 應用程式的 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="61cee-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="61cee-173">-SignInName</span></span>
<span data-ttu-id="61cee-174">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="61cee-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61cee-175">-確認</span><span class="sxs-lookup"><span data-stu-id="61cee-175">-Confirm</span></span>
<span data-ttu-id="61cee-176">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61cee-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61cee-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61cee-177">-WhatIf</span></span>
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

### <span data-ttu-id="61cee-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61cee-178">CommonParameters</span></span>
<span data-ttu-id="61cee-179">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61cee-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61cee-180">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61cee-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61cee-181">輸入</span><span class="sxs-lookup"><span data-stu-id="61cee-181">INPUTS</span></span>

### <span data-ttu-id="61cee-182">System.String</span><span class="sxs-lookup"><span data-stu-id="61cee-182">System.String</span></span>

### <span data-ttu-id="61cee-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="61cee-183">System.Guid</span></span>

### <span data-ttu-id="61cee-184">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61cee-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="61cee-185">輸出</span><span class="sxs-lookup"><span data-stu-id="61cee-185">OUTPUTS</span></span>

### <span data-ttu-id="61cee-186">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61cee-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="61cee-187">筆記</span><span class="sxs-lookup"><span data-stu-id="61cee-187">NOTES</span></span>
<span data-ttu-id="61cee-188">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="61cee-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="61cee-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="61cee-189">RELATED LINKS</span></span>

[<span data-ttu-id="61cee-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61cee-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="61cee-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61cee-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="61cee-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61cee-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

