---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: b21d265d507c1ff508c5db68094a65b54257931a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907302"
---
# <span data-ttu-id="9b447-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9b447-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="9b447-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b447-102">SYNOPSIS</span></span>
<span data-ttu-id="9b447-103">將指定的 RBAC 角色指派給指定範圍中的指定主體。</span><span class="sxs-lookup"><span data-stu-id="9b447-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="9b447-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b447-104">SYNTAX</span></span>

### <span data-ttu-id="9b447-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9b447-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b447-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b447-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b447-116">描述</span><span class="sxs-lookup"><span data-stu-id="9b447-116">DESCRIPTION</span></span>
<span data-ttu-id="9b447-117">使用 New-AzRoleAssignment 命令來授予存取權。</span><span class="sxs-lookup"><span data-stu-id="9b447-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="9b447-118">Access 是在正確的範圍中指派適當的 RBAC 角色給他們，以授予存取權。</span><span class="sxs-lookup"><span data-stu-id="9b447-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="9b447-119">若要授予整個訂閱的存取權，請指派訂閱範圍中的角色。</span><span class="sxs-lookup"><span data-stu-id="9b447-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="9b447-120">若要授予訂閱中特定資源群組的存取權，請指派資源群組範圍中的角色。</span><span class="sxs-lookup"><span data-stu-id="9b447-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="9b447-121">必須指定作業的主體。</span><span class="sxs-lookup"><span data-stu-id="9b447-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="9b447-122">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="9b447-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="9b447-123">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="9b447-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="9b447-124">若要指定 Azure AD 應用程式，請使用 ApplicationId 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="9b447-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="9b447-125">指派的角色必須使用 RoleDefinitionName 參數指定。</span><span class="sxs-lookup"><span data-stu-id="9b447-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="9b447-126">您可以指定授予存取權的範圍。</span><span class="sxs-lookup"><span data-stu-id="9b447-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="9b447-127">它會預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b447-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="9b447-128">工作分派的範圍可以使用下列其中一個參數組合 a 來指定。</span><span class="sxs-lookup"><span data-stu-id="9b447-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="9b447-129">範圍 - 這是從 /subscriptions/b 開始完整範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="9b447-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="9b447-130">ResourceGroupName - 以授予指定資源群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="9b447-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="9b447-131">C。</span><span class="sxs-lookup"><span data-stu-id="9b447-131">c.</span></span>
<span data-ttu-id="9b447-132">ResourceName、ResourceType、ResourceGroupName 和 (選擇) ParentResource - 以指定資源群組中的特定資源以授予存取權。</span><span class="sxs-lookup"><span data-stu-id="9b447-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="9b447-133">例子</span><span class="sxs-lookup"><span data-stu-id="9b447-133">EXAMPLES</span></span>

### <span data-ttu-id="9b447-134">範例 1</span><span class="sxs-lookup"><span data-stu-id="9b447-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="9b447-135">將讀取者角色存取權授予資源群組範圍中的使用者，而角色指派可供委派使用</span><span class="sxs-lookup"><span data-stu-id="9b447-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="9b447-136">範例 2</span><span class="sxs-lookup"><span data-stu-id="9b447-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="9b447-137">將存取權授予安全性群組</span><span class="sxs-lookup"><span data-stu-id="9b447-137">Grant access to a security group</span></span>

### <span data-ttu-id="9b447-138">範例 3</span><span class="sxs-lookup"><span data-stu-id="9b447-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="9b447-139">將存取權授予位於資源 (網站) </span><span class="sxs-lookup"><span data-stu-id="9b447-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="9b447-140">範例 4</span><span class="sxs-lookup"><span data-stu-id="9b447-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="9b447-141">將存取權授予巢 (子網) </span><span class="sxs-lookup"><span data-stu-id="9b447-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="9b447-142">範例 5</span><span class="sxs-lookup"><span data-stu-id="9b447-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="9b447-143">將讀取者存取權授予服務主體</span><span class="sxs-lookup"><span data-stu-id="9b447-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="9b447-144">參數</span><span class="sxs-lookup"><span data-stu-id="9b447-144">PARAMETERS</span></span>

### <span data-ttu-id="9b447-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="9b447-145">-AllowDelegation</span></span>
<span data-ttu-id="9b447-146">建立角色指派時，委派標標。</span><span class="sxs-lookup"><span data-stu-id="9b447-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9b447-147">-ApplicationId</span></span>
<span data-ttu-id="9b447-148">ServicePrincipal 的應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="9b447-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-149">-條件</span><span class="sxs-lookup"><span data-stu-id="9b447-149">-Condition</span></span>
<span data-ttu-id="9b447-150">要適用于 RoleAssignment 的條件。</span><span class="sxs-lookup"><span data-stu-id="9b447-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="9b447-151">-ConditionVersion</span></span>
<span data-ttu-id="9b447-152">條件的版本。</span><span class="sxs-lookup"><span data-stu-id="9b447-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b447-153">-DefaultProfile</span></span>
<span data-ttu-id="9b447-154">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9b447-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b447-155">-描述</span><span class="sxs-lookup"><span data-stu-id="9b447-155">-Description</span></span>
<span data-ttu-id="9b447-156">角色指派的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="9b447-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9b447-157">-InputFile</span></span>
<span data-ttu-id="9b447-158">角色指派路徑 json</span><span class="sxs-lookup"><span data-stu-id="9b447-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9b447-159">-ObjectId</span></span>
<span data-ttu-id="9b447-160">使用者、群組或服務主體的 Azure AD Objectid。</span><span class="sxs-lookup"><span data-stu-id="9b447-160">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="9b447-161">-ParentResource</span></span>
<span data-ttu-id="9b447-162">階層中的父資源 (ResourceName 參數所指定之資源的) 。</span><span class="sxs-lookup"><span data-stu-id="9b447-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="9b447-163">只能與 ResourceGroupName、ResourceType 和 ResourceName 參數一起使用，以識別資源的相對 URI 形式建構階層式範圍。</span><span class="sxs-lookup"><span data-stu-id="9b447-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="9b447-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b447-164">-ResourceGroupName</span></span>
<span data-ttu-id="9b447-165">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9b447-165">The resource group name.</span></span>
<span data-ttu-id="9b447-166">建立在指定的資源群組中有效的工作分派。</span><span class="sxs-lookup"><span data-stu-id="9b447-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="9b447-167">當與 ResourceName、ResourceType 和 (選擇性地) ParentResource 參數一起使用時，該命令會以可識別資源的相對 URI 形式建構階層式範圍。</span><span class="sxs-lookup"><span data-stu-id="9b447-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9b447-168">-ResourceName</span></span>
<span data-ttu-id="9b447-169">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9b447-169">The resource name.</span></span>
<span data-ttu-id="9b447-170">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="9b447-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="9b447-171">應該只能與 ResourceGroupName、ResourceType 和 (選擇性地使用 parentResource 參數) 以識別資源的相對 URI 形式建構階層式範圍。</span><span class="sxs-lookup"><span data-stu-id="9b447-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="9b447-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9b447-172">-ResourceType</span></span>
<span data-ttu-id="9b447-173">資源類型。</span><span class="sxs-lookup"><span data-stu-id="9b447-173">The resource type.</span></span>
<span data-ttu-id="9b447-174">例如，Microsoft.Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="9b447-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="9b447-175">應該只能與 ResourceGroupName、ResourceName 和 (一起使用) ParentResource 參數，以識別資源的相對 URI 形式建構階層式範圍。</span><span class="sxs-lookup"><span data-stu-id="9b447-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="9b447-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9b447-176">-RoleDefinitionId</span></span>
<span data-ttu-id="9b447-177">需要指派給主體的 RBAC 角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b447-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="9b447-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9b447-178">-RoleDefinitionName</span></span>
<span data-ttu-id="9b447-179">需要指派給主體的 RBAC 角色名稱，例如讀取者、參與者、虛擬網路管理員等。</span><span class="sxs-lookup"><span data-stu-id="9b447-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-180">-範圍</span><span class="sxs-lookup"><span data-stu-id="9b447-180">-Scope</span></span>
<span data-ttu-id="9b447-181">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="9b447-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="9b447-182">以相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="9b447-182">In the format of relative URI.</span></span>
<span data-ttu-id="9b447-183">例如"/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG"。</span><span class="sxs-lookup"><span data-stu-id="9b447-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="9b447-184">如果未指定，就會在訂閱層級建立角色指派。</span><span class="sxs-lookup"><span data-stu-id="9b447-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="9b447-185">如果指定，應該從"/subscriptions/{id}"開始。</span><span class="sxs-lookup"><span data-stu-id="9b447-185">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="9b447-186">-SignInName</span></span>
<span data-ttu-id="9b447-187">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="9b447-187">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b447-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b447-188">CommonParameters</span></span>
<span data-ttu-id="9b447-189">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b447-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b447-190">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b447-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b447-191">輸入</span><span class="sxs-lookup"><span data-stu-id="9b447-191">INPUTS</span></span>

### <span data-ttu-id="9b447-192">System.String</span><span class="sxs-lookup"><span data-stu-id="9b447-192">System.String</span></span>

### <span data-ttu-id="9b447-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9b447-193">System.Guid</span></span>

## <span data-ttu-id="9b447-194">輸出</span><span class="sxs-lookup"><span data-stu-id="9b447-194">OUTPUTS</span></span>

### <span data-ttu-id="9b447-195">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9b447-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="9b447-196">筆記</span><span class="sxs-lookup"><span data-stu-id="9b447-196">NOTES</span></span>
<span data-ttu-id="9b447-197">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="9b447-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9b447-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b447-198">RELATED LINKS</span></span>

[<span data-ttu-id="9b447-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9b447-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="9b447-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9b447-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="9b447-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9b447-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
