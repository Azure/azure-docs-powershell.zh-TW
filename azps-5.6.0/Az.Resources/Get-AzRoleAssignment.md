---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: dd59b49ad4002d38cd9a49506cb1723b5ac1e426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913726"
---
# <span data-ttu-id="dbbd1-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbbd1-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="dbbd1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbbd1-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbd1-103">列出指定範圍中的 Azure RBAC 角色指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="dbbd1-104">根據預設，它會列出所選 Azure 訂閱中所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="dbbd1-105">使用各自的參數列出指派給特定使用者，或列出特定資源群組或資源的指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="dbbd1-106">語法</span><span class="sxs-lookup"><span data-stu-id="dbbd1-106">SYNTAX</span></span>

### <span data-ttu-id="dbbd1-107">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbbd1-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbd1-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbd1-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbbd1-124">描述</span><span class="sxs-lookup"><span data-stu-id="dbbd1-124">DESCRIPTION</span></span>
<span data-ttu-id="dbbd1-125">使用 Get-AzRoleAssignment 命令列出範圍中有效的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="dbbd1-126">若沒有任何參數，此命令會返回訂閱下進行的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="dbbd1-127">此清單可以使用主體、角色和範圍的篩選參數進行篩選。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="dbbd1-128">必須指定作業的主體。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="dbbd1-129">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="dbbd1-130">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="dbbd1-131">若要指定 Azure AD 應用程式，請使用 ServicePrincipalName 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="dbbd1-132">指派的角色必須使用 RoleDefinitionName 參數指定。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="dbbd1-133">您可以指定授予存取權的範圍。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="dbbd1-134">它會預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="dbbd1-135">工作分派的範圍可以使用下列其中一個參數組合 a 來指定。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="dbbd1-136">範圍 - 這是從 /subscriptions/開始的所有完整範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="dbbd1-137">這會篩選有效于該特定範圍的工作分派，即該範圍及以上範圍的所有工作分派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="dbbd1-138">B。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-138">b.</span></span>
<span data-ttu-id="dbbd1-139">ResourceGroupName - 訂閱下任何資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="dbbd1-140">這會篩選指定資源群組 c 的有效工作分派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="dbbd1-141">ResourceName、ResourceType、ResourceGroupName 和 (選) ParentResource - 識別訂閱下的特定資源，並篩選該資源範圍中有效的工作分派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="dbbd1-142">若要判斷特定使用者在訂閱中擁有哪些存取權，請使用 ExpandPrincipalGroups 切換。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="dbbd1-143">這會列出指派給使用者的所有角色，以及使用者所組成群組的所有角色。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="dbbd1-144">使用 IncludeClassicAdministrators 切換來同時顯示訂閱系統管理員和共同管理員。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="dbbd1-145">例子</span><span class="sxs-lookup"><span data-stu-id="dbbd1-145">EXAMPLES</span></span>

### <span data-ttu-id="dbbd1-146">範例 1</span><span class="sxs-lookup"><span data-stu-id="dbbd1-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="dbbd1-147">列出訂閱中所有角色指派</span><span class="sxs-lookup"><span data-stu-id="dbbd1-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="dbbd1-148">範例 2</span><span class="sxs-lookup"><span data-stu-id="dbbd1-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="dbbd1-149">取得在 testRG 範圍或以上範圍內指派給使用者的所有角色，以及其為成員 john.doe@contoso.com 群組。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="dbbd1-150">範例 3</span><span class="sxs-lookup"><span data-stu-id="dbbd1-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="dbbd1-151">獲得指定服務主體的所有角色指派</span><span class="sxs-lookup"><span data-stu-id="dbbd1-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="dbbd1-152">範例 4</span><span class="sxs-lookup"><span data-stu-id="dbbd1-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="dbbd1-153">在網站 1 網站範圍中獲得角色指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="dbbd1-154">參數</span><span class="sxs-lookup"><span data-stu-id="dbbd1-154">PARAMETERS</span></span>

### <span data-ttu-id="dbbd1-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbd1-155">-DefaultProfile</span></span>
<span data-ttu-id="dbbd1-156">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="dbbd1-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbbd1-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="dbbd1-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="dbbd1-158">如果指定，會直接將角色指派給使用者以及使用者是其中一個成員的群組， (一) 。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="dbbd1-159">僅支援使用者主體。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="dbbd1-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="dbbd1-161">如果指定，也會列出共同 (系統管理員、服務系統管理員等角色指派) 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dbbd1-162">-ObjectId</span></span>
<span data-ttu-id="dbbd1-163">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="dbbd1-164">篩選對指定主體進行的所有工作分派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="dbbd1-165">-ParentResource</span></span>
<span data-ttu-id="dbbd1-166">使用 ResourceName 參數指定之資源階層中的父資源。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="dbbd1-167">必須與 ResourceGroupName、ResourceType 和 ResourceName 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbbd1-168">-ResourceGroupName</span></span>
<span data-ttu-id="dbbd1-169">資源組名。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-169">The resource group name.</span></span>
<span data-ttu-id="dbbd1-170">列出在指定的資源群組中有效的角色指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="dbbd1-171">當與 ResourceName、ResourceType 和 ParentResource 參數一起使用時，命令會列出資源群組中資源的有效工作分派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dbbd1-172">-ResourceName</span></span>
<span data-ttu-id="dbbd1-173">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-173">The resource name.</span></span>
<span data-ttu-id="dbbd1-174">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="dbbd1-175">必須和 ResourceGroupName、ResourceType 和 (ParentResource 參數) 使用。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dbbd1-176">-ResourceType</span></span>
<span data-ttu-id="dbbd1-177">資源類型。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-177">The resource type.</span></span>
<span data-ttu-id="dbbd1-178">例如，Microsoft.Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="dbbd1-179">必須配合 ResourceGroupName、ResourceName 和 (ParentResource 參數) 使用。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dbbd1-180">-RoleDefinitionId</span></span>
<span data-ttu-id="dbbd1-181">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="dbbd1-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="dbbd1-182">-RoleDefinitionName</span></span>
<span data-ttu-id="dbbd1-183">指派給主體的角色，例如讀取者、參與者、虛擬網路管理員等。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-184">-範圍</span><span class="sxs-lookup"><span data-stu-id="dbbd1-184">-Scope</span></span>
<span data-ttu-id="dbbd1-185">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="dbbd1-186">以相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-186">In the format of relative URI.</span></span>
<span data-ttu-id="dbbd1-187">例如/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="dbbd1-188">它必須以"/subscriptions/{id}"開始。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="dbbd1-189">命令會篩選所有有效于該範圍的工作分派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dbbd1-190">-ServicePrincipalName</span></span>
<span data-ttu-id="dbbd1-191">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="dbbd1-192">篩選對指定的 Azure AD 應用程式進行的所有指派。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="dbbd1-193">-SignInName</span></span>
<span data-ttu-id="dbbd1-194">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="dbbd1-195">篩選所有指派給指定的使用者。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbd1-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbd1-196">CommonParameters</span></span>
<span data-ttu-id="dbbd1-197">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbbd1-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbd1-198">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbbd1-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbd1-199">輸入</span><span class="sxs-lookup"><span data-stu-id="dbbd1-199">INPUTS</span></span>

### <span data-ttu-id="dbbd1-200">System.String</span><span class="sxs-lookup"><span data-stu-id="dbbd1-200">System.String</span></span>

### <span data-ttu-id="dbbd1-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dbbd1-201">System.Guid</span></span>

## <span data-ttu-id="dbbd1-202">輸出</span><span class="sxs-lookup"><span data-stu-id="dbbd1-202">OUTPUTS</span></span>

### <span data-ttu-id="dbbd1-203">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbbd1-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="dbbd1-204">筆記</span><span class="sxs-lookup"><span data-stu-id="dbbd1-204">NOTES</span></span>
<span data-ttu-id="dbbd1-205">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="dbbd1-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dbbd1-206">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbbd1-206">RELATED LINKS</span></span>

[<span data-ttu-id="dbbd1-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbbd1-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="dbbd1-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbbd1-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="dbbd1-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dbbd1-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

