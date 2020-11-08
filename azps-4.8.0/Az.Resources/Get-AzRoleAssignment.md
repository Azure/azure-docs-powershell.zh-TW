---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127377"
---
# <span data-ttu-id="40f23-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="40f23-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="40f23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40f23-102">SYNOPSIS</span></span>
<span data-ttu-id="40f23-103">列出指定範圍內的 Azure RBAC 角色分派。</span><span class="sxs-lookup"><span data-stu-id="40f23-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="40f23-104">根據預設，它會列出所選 Azure 訂閱中的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="40f23-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="40f23-105">使用個別的參數，將作業清單指派給特定的使用者，或列出特定資源群組或資源上的作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="40f23-106">句法</span><span class="sxs-lookup"><span data-stu-id="40f23-106">SYNTAX</span></span>

### <span data-ttu-id="40f23-107">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="40f23-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f23-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f23-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40f23-124">說明</span><span class="sxs-lookup"><span data-stu-id="40f23-124">DESCRIPTION</span></span>
<span data-ttu-id="40f23-125">使用 [Get-AzRoleAssignment] 命令來列出在某個範圍內有效的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="40f23-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="40f23-126">如果沒有任何參數，這個命令會傳回在訂閱下所做的所有角色分派。</span><span class="sxs-lookup"><span data-stu-id="40f23-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="40f23-127">您可以使用 [主要]、[角色] 和 [範圍] 的篩選參數來篩選此清單。</span><span class="sxs-lookup"><span data-stu-id="40f23-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="40f23-128">必須指定作業的主語。</span><span class="sxs-lookup"><span data-stu-id="40f23-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="40f23-129">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="40f23-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="40f23-130">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="40f23-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="40f23-131">若要指定 Azure AD 應用程式，請使用 ServicePrincipalName 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="40f23-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="40f23-132">所指派的角色，必須使用 RoleDefinitionName 參數加以指定。</span><span class="sxs-lookup"><span data-stu-id="40f23-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="40f23-133">您可以指定授權存取的範圍。</span><span class="sxs-lookup"><span data-stu-id="40f23-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="40f23-134">預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="40f23-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="40f23-135">您可以使用下列其中一個參數組合來指定作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="40f23-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="40f23-136">範圍-這是從/subscriptions/開始的完整限定範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="40f23-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="40f23-137">這將會篩選在該特定範圍中有效的作業，亦即在該範圍和上方的所有作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="40f23-138">乙.</span><span class="sxs-lookup"><span data-stu-id="40f23-138">b.</span></span>
<span data-ttu-id="40f23-139">ResourceGroupName-訂閱下任何資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40f23-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="40f23-140">這將會在指定的資源群組 c 中篩選作業生效。</span><span class="sxs-lookup"><span data-stu-id="40f23-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="40f23-141">[資源 ResourceGroupName]、[ResourceType]、[] 和 [ (] （選擇性）) ParentResource-識別訂閱下的特定資源，並且會篩選該資源範圍中的作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="40f23-142">若要判斷特定使用者在訂閱中所擁有的存取權，請使用 ExpandPrincipalGroups 開關。</span><span class="sxs-lookup"><span data-stu-id="40f23-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="40f23-143">這會列出指派給該使用者的所有角色，以及該使用者所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="40f23-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="40f23-144">您也可以使用 IncludeClassicAdministrators 開關來顯示 [訂閱管理員] 和 [共同管理員]。</span><span class="sxs-lookup"><span data-stu-id="40f23-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="40f23-145">示例</span><span class="sxs-lookup"><span data-stu-id="40f23-145">EXAMPLES</span></span>

### <span data-ttu-id="40f23-146">範例1</span><span class="sxs-lookup"><span data-stu-id="40f23-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="40f23-147">列出訂閱中的所有角色指派</span><span class="sxs-lookup"><span data-stu-id="40f23-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="40f23-148">範例2</span><span class="sxs-lookup"><span data-stu-id="40f23-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="40f23-149">在 testRG 範圍或上方，取得對使用者所做的所有角色指派 john.doe@contoso.com ，以及該成員的群組。</span><span class="sxs-lookup"><span data-stu-id="40f23-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="40f23-150">範例3</span><span class="sxs-lookup"><span data-stu-id="40f23-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="40f23-151">取得指定服務主體的所有角色指派</span><span class="sxs-lookup"><span data-stu-id="40f23-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="40f23-152">範例4</span><span class="sxs-lookup"><span data-stu-id="40f23-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="40f23-153">取得「site1」網站範圍的角色分派。</span><span class="sxs-lookup"><span data-stu-id="40f23-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="40f23-154">參數</span><span class="sxs-lookup"><span data-stu-id="40f23-154">PARAMETERS</span></span>

### <span data-ttu-id="40f23-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f23-155">-DefaultProfile</span></span>
<span data-ttu-id="40f23-156">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40f23-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40f23-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="40f23-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="40f23-158">如果已指定，會傳回直接指派給使用者的角色，以及使用者是其成員的群組 (可傳遞) 。</span><span class="sxs-lookup"><span data-stu-id="40f23-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="40f23-159">僅支援使用者主體。</span><span class="sxs-lookup"><span data-stu-id="40f23-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="40f23-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="40f23-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="40f23-161">如果已指定，也會列出 [訂閱傳統管理員] (共同管理員、服務管理員等。 ) 角色指派。</span><span class="sxs-lookup"><span data-stu-id="40f23-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="40f23-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="40f23-162">-ObjectId</span></span>
<span data-ttu-id="40f23-163">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="40f23-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="40f23-164">篩選對指定本金所做的所有作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="40f23-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="40f23-165">-ParentResource</span></span>
<span data-ttu-id="40f23-166">使用 [資源數] 參數指定之資源階層中的父資源。</span><span class="sxs-lookup"><span data-stu-id="40f23-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="40f23-167">必須與 ResourceGroupName、ResourceType 和 CoNtext.resourcename 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="40f23-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="40f23-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f23-168">-ResourceGroupName</span></span>
<span data-ttu-id="40f23-169">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40f23-169">The resource group name.</span></span>
<span data-ttu-id="40f23-170">列出在指定資源群組中有效的角色指派。</span><span class="sxs-lookup"><span data-stu-id="40f23-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="40f23-171">當與 [資源清單]、[ResourceType] 和 [ParentResource] 參數搭配使用時，命令會列出工作指派在資源群組中的實際資源。</span><span class="sxs-lookup"><span data-stu-id="40f23-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="40f23-172">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="40f23-172">-ResourceName</span></span>
<span data-ttu-id="40f23-173">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="40f23-173">The resource name.</span></span>
<span data-ttu-id="40f23-174">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="40f23-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="40f23-175">必須與 ResourceGroupName、ResourceType 及 (（選擇性）) ParentResource 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="40f23-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="40f23-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="40f23-176">-ResourceType</span></span>
<span data-ttu-id="40f23-177">資源類型。</span><span class="sxs-lookup"><span data-stu-id="40f23-177">The resource type.</span></span>
<span data-ttu-id="40f23-178">例如，. Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="40f23-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="40f23-179">必須與 ResourceGroupName、和 (（選擇性) ParentResource 參數）搭配使用。</span><span class="sxs-lookup"><span data-stu-id="40f23-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="40f23-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="40f23-180">-RoleDefinitionId</span></span>
<span data-ttu-id="40f23-181">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="40f23-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="40f23-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="40f23-182">-RoleDefinitionName</span></span>
<span data-ttu-id="40f23-183">指派給 principal （例如讀者、參與者、虛擬網路管理員等）的角色。</span><span class="sxs-lookup"><span data-stu-id="40f23-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="40f23-184">-範圍</span><span class="sxs-lookup"><span data-stu-id="40f23-184">-Scope</span></span>
<span data-ttu-id="40f23-185">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="40f23-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="40f23-186">相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="40f23-186">In the format of relative URI.</span></span>
<span data-ttu-id="40f23-187">例如/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG。</span><span class="sxs-lookup"><span data-stu-id="40f23-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="40f23-188">其開頭必須是 "/subscriptions/{id}"。</span><span class="sxs-lookup"><span data-stu-id="40f23-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="40f23-189">此命令會篩選在該範圍內有效的所有作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="40f23-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="40f23-190">-ServicePrincipalName</span></span>
<span data-ttu-id="40f23-191">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="40f23-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="40f23-192">篩選對指定 Azure AD 應用程式所做的所有作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="40f23-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="40f23-193">-SignInName</span></span>
<span data-ttu-id="40f23-194">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="40f23-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="40f23-195">篩選對指定使用者所做的所有作業。</span><span class="sxs-lookup"><span data-stu-id="40f23-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="40f23-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f23-196">CommonParameters</span></span>
<span data-ttu-id="40f23-197">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40f23-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f23-198">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="40f23-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f23-199">輸入</span><span class="sxs-lookup"><span data-stu-id="40f23-199">INPUTS</span></span>

### <span data-ttu-id="40f23-200">System.object</span><span class="sxs-lookup"><span data-stu-id="40f23-200">System.String</span></span>

### <span data-ttu-id="40f23-201">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="40f23-201">System.Guid</span></span>

## <span data-ttu-id="40f23-202">輸出</span><span class="sxs-lookup"><span data-stu-id="40f23-202">OUTPUTS</span></span>

### <span data-ttu-id="40f23-203">PSRoleAssignment 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="40f23-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="40f23-204">筆記</span><span class="sxs-lookup"><span data-stu-id="40f23-204">NOTES</span></span>
<span data-ttu-id="40f23-205">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="40f23-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="40f23-206">相關連結</span><span class="sxs-lookup"><span data-stu-id="40f23-206">RELATED LINKS</span></span>

[<span data-ttu-id="40f23-207">新-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="40f23-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="40f23-208">移除-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="40f23-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="40f23-209">AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="40f23-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

