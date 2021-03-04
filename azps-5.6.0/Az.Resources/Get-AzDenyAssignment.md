---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: d54d6ff9ed26b76d3c36ab47cf04024dcdf11281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903085"
---
# <span data-ttu-id="ed429-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="ed429-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="ed429-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed429-102">SYNOPSIS</span></span>
<span data-ttu-id="ed429-103">列出 Azure RBAC 拒絕指定範圍中的指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="ed429-104">根據預設，它會列出所選 Azure 訂閱中所有拒絕的指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="ed429-105">使用各自的參數列出拒絕指派給特定使用者，或列出特定資源群組或資源的拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="ed429-106">語法</span><span class="sxs-lookup"><span data-stu-id="ed429-106">SYNTAX</span></span>

### <span data-ttu-id="ed429-107">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ed429-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed429-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed429-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed429-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed429-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed429-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed429-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed429-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed429-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed429-125">描述</span><span class="sxs-lookup"><span data-stu-id="ed429-125">DESCRIPTION</span></span>
<span data-ttu-id="ed429-126">使用 Get-AzDenyAssignment 命令列出範圍中有效的所有拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="ed429-127">若沒有任何參數，此命令會返回訂閱下進行的所有拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="ed429-128">此清單可以使用主體的篩選參數進行篩選，拒絕工作分派名稱和範圍。</span><span class="sxs-lookup"><span data-stu-id="ed429-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="ed429-129">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="ed429-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="ed429-130">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="ed429-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="ed429-131">若要指定 Azure AD 應用程式，請使用 ServicePrincipalName 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="ed429-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="ed429-132">您可以指定拒絕存取的範圍。</span><span class="sxs-lookup"><span data-stu-id="ed429-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="ed429-133">它會預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed429-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="ed429-134">您可以使用下列其中一個參數組合 a 來指定拒絕指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="ed429-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="ed429-135">範圍 - 這是從 /subscriptions/開始的所有完整範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="ed429-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="ed429-136">這會篩選有效于該特定範圍中的拒絕指派，也就是說，所有拒絕該範圍及以上範圍的工作分派。</span><span class="sxs-lookup"><span data-stu-id="ed429-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="ed429-137">B。</span><span class="sxs-lookup"><span data-stu-id="ed429-137">b.</span></span>
<span data-ttu-id="ed429-138">ResourceGroupName - 訂閱下任何資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed429-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="ed429-139">這會篩選指定資源群組中有效的工作分派，也就是說，所有拒絕該範圍及以上範圍的指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="ed429-140">C。</span><span class="sxs-lookup"><span data-stu-id="ed429-140">c.</span></span>
<span data-ttu-id="ed429-141">ResourceName、ResourceType、ResourceGroupName 和 (選) ParentResource - 識別訂閱下的特定資源，並篩選該資源範圍中有效的拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="ed429-142">若要判斷訂閱中特定使用者的存取遭到拒絕，請使用 ExpandPrincipalGroups 切換。</span><span class="sxs-lookup"><span data-stu-id="ed429-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="ed429-143">這會列出指派給使用者的所有拒絕指派，以及該使用者所組成群組的所有拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="ed429-144">例子</span><span class="sxs-lookup"><span data-stu-id="ed429-144">EXAMPLES</span></span>

### <span data-ttu-id="ed429-145">範例 1</span><span class="sxs-lookup"><span data-stu-id="ed429-145">Example 1</span></span>

<span data-ttu-id="ed429-146">列出訂閱中所有拒絕的指派</span><span class="sxs-lookup"><span data-stu-id="ed429-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="ed429-147">範例 2</span><span class="sxs-lookup"><span data-stu-id="ed429-147">Example 2</span></span>

<span data-ttu-id="ed429-148">在範圍測試RG 及以上範圍內取得 john.doe@contoso.com 使用者的所有拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="ed429-149">範例 3</span><span class="sxs-lookup"><span data-stu-id="ed429-149">Example 3</span></span>

<span data-ttu-id="ed429-150">獲得指定服務主體的所有拒絕指派</span><span class="sxs-lookup"><span data-stu-id="ed429-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="ed429-151">範例 4</span><span class="sxs-lookup"><span data-stu-id="ed429-151">Example 4</span></span>

<span data-ttu-id="ed429-152">在 'site1' 網站範圍中收到拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

## <span data-ttu-id="ed429-153">參數</span><span class="sxs-lookup"><span data-stu-id="ed429-153">PARAMETERS</span></span>

### <span data-ttu-id="ed429-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed429-154">-DefaultProfile</span></span>
<span data-ttu-id="ed429-155">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ed429-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed429-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ed429-156">-DenyAssignmentName</span></span>
<span data-ttu-id="ed429-157">拒絕作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed429-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed429-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="ed429-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="ed429-159">如果指定，會返回直接指派給使用者和使用者為成員之群組的拒絕指派， (指派) 。</span><span class="sxs-lookup"><span data-stu-id="ed429-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="ed429-160">僅支援使用者主體。</span><span class="sxs-lookup"><span data-stu-id="ed429-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="ed429-161">-Id</span><span class="sxs-lookup"><span data-stu-id="ed429-161">-Id</span></span>
<span data-ttu-id="ed429-162">拒絕作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed429-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed429-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ed429-163">-ObjectId</span></span>
<span data-ttu-id="ed429-164">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="ed429-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="ed429-165">篩選所有對指定主體的拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed429-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="ed429-166">-ParentResource</span></span>
<span data-ttu-id="ed429-167">使用 ResourceName 參數指定之資源階層中的父資源。</span><span class="sxs-lookup"><span data-stu-id="ed429-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="ed429-168">必須與 ResourceGroupName、ResourceType 和 ResourceName 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="ed429-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="ed429-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed429-169">-ResourceGroupName</span></span>
<span data-ttu-id="ed429-170">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ed429-170">The resource group name.</span></span>
<span data-ttu-id="ed429-171">清單拒絕在指定的資源群組中有效的工作分派。</span><span class="sxs-lookup"><span data-stu-id="ed429-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="ed429-172">與 ResourceName、ResourceType 和 ParentResource 參數一起使用時，命令會列出對資源群組內資源有效拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="ed429-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ed429-173">-ResourceName</span></span>
<span data-ttu-id="ed429-174">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ed429-174">The resource name.</span></span>
<span data-ttu-id="ed429-175">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="ed429-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="ed429-176">必須和 ResourceGroupName、ResourceType 和 (ParentResource 參數) 使用。</span><span class="sxs-lookup"><span data-stu-id="ed429-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="ed429-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ed429-177">-ResourceType</span></span>
<span data-ttu-id="ed429-178">資源類型。</span><span class="sxs-lookup"><span data-stu-id="ed429-178">The resource type.</span></span>
<span data-ttu-id="ed429-179">例如，Microsoft.Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="ed429-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="ed429-180">必須配合 ResourceGroupName、ResourceName 和 (ParentResource 參數) 使用。</span><span class="sxs-lookup"><span data-stu-id="ed429-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="ed429-181">-範圍</span><span class="sxs-lookup"><span data-stu-id="ed429-181">-Scope</span></span>
<span data-ttu-id="ed429-182">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="ed429-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="ed429-183">以相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="ed429-183">In the format of relative URI.</span></span>
<span data-ttu-id="ed429-184">例如/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG。</span><span class="sxs-lookup"><span data-stu-id="ed429-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="ed429-185">它必須以"/subscriptions/{id}"開始。</span><span class="sxs-lookup"><span data-stu-id="ed429-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="ed429-186">該命令會篩選所有有效于該範圍中的拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="ed429-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed429-187">-ServicePrincipalName</span></span>
<span data-ttu-id="ed429-188">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="ed429-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="ed429-189">篩選對指定的 Azure AD 應用程式進行的所有拒絕指派。</span><span class="sxs-lookup"><span data-stu-id="ed429-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="ed429-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="ed429-190">-SignInName</span></span>
<span data-ttu-id="ed429-191">使用者的電子郵件地址或使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="ed429-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="ed429-192">篩選所有拒絕指派給指定的使用者。</span><span class="sxs-lookup"><span data-stu-id="ed429-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="ed429-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed429-193">CommonParameters</span></span>
<span data-ttu-id="ed429-194">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed429-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed429-195">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed429-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed429-196">輸入</span><span class="sxs-lookup"><span data-stu-id="ed429-196">INPUTS</span></span>

### <span data-ttu-id="ed429-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ed429-197">System.Guid</span></span>

### <span data-ttu-id="ed429-198">System.String</span><span class="sxs-lookup"><span data-stu-id="ed429-198">System.String</span></span>

## <span data-ttu-id="ed429-199">輸出</span><span class="sxs-lookup"><span data-stu-id="ed429-199">OUTPUTS</span></span>

### <span data-ttu-id="ed429-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="ed429-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="ed429-201">筆記</span><span class="sxs-lookup"><span data-stu-id="ed429-201">NOTES</span></span>
<span data-ttu-id="ed429-202">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="ed429-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ed429-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed429-203">RELATED LINKS</span></span>
