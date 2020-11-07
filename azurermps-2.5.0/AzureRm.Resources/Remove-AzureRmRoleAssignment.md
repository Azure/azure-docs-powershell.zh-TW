---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
ms.openlocfilehash: adf6147db102ee834f7e12e19409a95734fae7e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802185"
---
# <span data-ttu-id="d4a2e-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d4a2e-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="d4a2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a2e-103">移除指派給特定作用域中特定角色之指定原則的角色指派。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4a2e-104">SYNTAX</span></span>

### <span data-ttu-id="d4a2e-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d4a2e-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a2e-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a2e-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a2e-117">說明</span><span class="sxs-lookup"><span data-stu-id="d4a2e-117">DESCRIPTION</span></span>
<span data-ttu-id="d4a2e-118">使用 Remove-AzureRmRoleAssignment commandlet 撤銷對指定作用中的任何原則，以及指定角色的存取權。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="d4a2e-119">作業的物件（亦即必須指定 principal）。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="d4a2e-120">主體可以是使用者 (使用 SignInName 或 ObjectId 參數來識別使用者) 、安全性群組 (使用 ObjectId 參數來識別群組) 或服務主體 (使用 ServicePrincipalName 或 ObjectId 參數來識別 ServicePrincipal。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="d4a2e-121">承擔者所指派的角色，必須使用 RoleDefinitionName 參數加以指定。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="d4a2e-122">您可以指定指派的範圍，如果未指定，則預設為 [訂閱範圍]，亦即，該作業將會嘗試在訂閱範圍中刪除指派給指定的主體和角色。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="d4a2e-123">您可以使用下列其中一個參數指定作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="d4a2e-124">是.</span><span class="sxs-lookup"><span data-stu-id="d4a2e-124">a.</span></span>
<span data-ttu-id="d4a2e-125">範圍-這是從/subscriptions/b 開始的完整範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="d4a2e-126">ResourceGroupName-訂閱下任何資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="d4a2e-127">c-clip.</span><span class="sxs-lookup"><span data-stu-id="d4a2e-127">c.</span></span>
<span data-ttu-id="d4a2e-128">[資源 ResourceGroupName]、[ResourceType]、[] 和 [ (]) （ParentResource）會在訂閱下識別特定資源。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="d4a2e-129">示例</span><span class="sxs-lookup"><span data-stu-id="d4a2e-129">EXAMPLES</span></span>

### <span data-ttu-id="d4a2e-130">範例1</span><span class="sxs-lookup"><span data-stu-id="d4a2e-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="d4a2e-131">移除 john.doe@contoso.com 指派給 rg1 resourcegroup 範圍之 Reader 角色的人員的角色指派。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="d4a2e-132">範例2</span><span class="sxs-lookup"><span data-stu-id="d4a2e-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="d4a2e-133">移除由 ObjectId 所標識的群組主要角色指派，並指派給讀者角色。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="d4a2e-134">預設為使用目前的訂閱作為範圍，以尋找要刪除的作業。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="d4a2e-135">範例3</span><span class="sxs-lookup"><span data-stu-id="d4a2e-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="d4a2e-136">移除從 Get-AzureRmRoleAssignment commandlet 回遷的第一個角色指派物件。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="d4a2e-137">參數</span><span class="sxs-lookup"><span data-stu-id="d4a2e-137">PARAMETERS</span></span>

### <span data-ttu-id="d4a2e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a2e-138">-DefaultProfile</span></span>
<span data-ttu-id="d4a2e-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d4a2e-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a2e-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4a2e-140">-InputObject</span></span>
<span data-ttu-id="d4a2e-141">角色指派物件。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="d4a2e-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d4a2e-142">-ObjectId</span></span>
<span data-ttu-id="d4a2e-143">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a2e-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="d4a2e-144">-ParentResource</span></span>
<span data-ttu-id="d4a2e-145">階層中的父項資源，使用資源使用不足的參數) （如果有的話），在層次結構中 (。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="d4a2e-146">必須與 ResourceGroupName、ResourceType 和資源類型參數搭配使用，以以相對 URI 的形式來構造階層範圍，以識別資源。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="d4a2e-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4a2e-147">-PassThru</span></span>
<span data-ttu-id="d4a2e-148">如果已指定，則會顯示刪除的角色指派</span><span class="sxs-lookup"><span data-stu-id="d4a2e-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="d4a2e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a2e-149">-ResourceGroupName</span></span>
<span data-ttu-id="d4a2e-150">指派角色的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="d4a2e-151">嘗試刪除指定資源群組範圍中的作業。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="d4a2e-152">與資源中心、ResourceType 和 (（可選擇) ParentResource 參數）搭配使用時，命令會以相對 URI 的形式來構造階層範圍，以識別資源。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="d4a2e-153">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="d4a2e-153">-ResourceName</span></span>
<span data-ttu-id="d4a2e-154">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-154">The resource name.</span></span>
<span data-ttu-id="d4a2e-155">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="d4a2e-156">必須與 ResourceGroupName、ResourceType 和 (（選擇性) ParentResource 參數）搭配使用，以在相對 URI 的形式中構造階層範圍，識別該資源並刪除該範圍中的作業。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="d4a2e-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d4a2e-157">-ResourceType</span></span>
<span data-ttu-id="d4a2e-158">資源類型。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-158">The resource type.</span></span>
<span data-ttu-id="d4a2e-159">例如，. Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="d4a2e-160">必須與 ResourceGroupName、資源類型和 (搭配使用，也可以) ParentResource 參數來構造相對 URI 形式的階層範圍，以識別該資源並刪除該資源範圍中的作業。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="d4a2e-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d4a2e-161">-RoleDefinitionId</span></span>
<span data-ttu-id="d4a2e-162">需要刪除工作分派之 RBAC 角色的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="d4a2e-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d4a2e-163">-RoleDefinitionName</span></span>
<span data-ttu-id="d4a2e-164">需要刪除工作分派的 RBAC 角色名稱，亦即讀取器、參與者、虛擬網路管理員等等。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="d4a2e-165">-範圍</span><span class="sxs-lookup"><span data-stu-id="d4a2e-165">-Scope</span></span>
<span data-ttu-id="d4a2e-166">要刪除之角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="d4a2e-167">相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-167">In the format of relative URI.</span></span>
<span data-ttu-id="d4a2e-168">例如，"/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG"。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="d4a2e-169">如果未指定，將會嘗試刪除訂閱層級的角色。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="d4a2e-170">如果已指定，它應該以 "/subscriptions/{id}" 為開頭。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="d4a2e-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4a2e-171">-ServicePrincipalName</span></span>
<span data-ttu-id="d4a2e-172">Azure AD 應用程式的 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4a2e-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="d4a2e-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d4a2e-173">-SignInName</span></span>
<span data-ttu-id="d4a2e-174">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="d4a2e-175">-確認</span><span class="sxs-lookup"><span data-stu-id="d4a2e-175">-Confirm</span></span>
<span data-ttu-id="d4a2e-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a2e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a2e-177">-WhatIf</span></span>
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

### <span data-ttu-id="d4a2e-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a2e-178">CommonParameters</span></span>
<span data-ttu-id="d4a2e-179">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a2e-180">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4a2e-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a2e-181">輸入</span><span class="sxs-lookup"><span data-stu-id="d4a2e-181">INPUTS</span></span>

### <span data-ttu-id="d4a2e-182">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="d4a2e-182">System.Guid</span></span>

### <span data-ttu-id="d4a2e-183">System.object</span><span class="sxs-lookup"><span data-stu-id="d4a2e-183">System.String</span></span>

### <span data-ttu-id="d4a2e-184">PSRoleAssignment 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="d4a2e-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>
<span data-ttu-id="d4a2e-185">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d4a2e-185">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d4a2e-186">輸出</span><span class="sxs-lookup"><span data-stu-id="d4a2e-186">OUTPUTS</span></span>

### <span data-ttu-id="d4a2e-187">PSRoleAssignment 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="d4a2e-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="d4a2e-188">筆記</span><span class="sxs-lookup"><span data-stu-id="d4a2e-188">NOTES</span></span>
<span data-ttu-id="d4a2e-189">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="d4a2e-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d4a2e-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4a2e-190">RELATED LINKS</span></span>

[<span data-ttu-id="d4a2e-191">新-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d4a2e-191">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="d4a2e-192">AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d4a2e-192">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="d4a2e-193">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d4a2e-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

