---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791298"
---
# <span data-ttu-id="9beec-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="9beec-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="9beec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9beec-102">SYNOPSIS</span></span>
<span data-ttu-id="9beec-103">列出指定範圍內的 Azure RBAC 拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="9beec-104">根據預設，會列出所選 Azure 訂閱中的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="9beec-105">使用個別的參數，將 [拒絕作業] 指派給特定的使用者，或列出特定資源群組或資源上的 [拒絕作業]。</span><span class="sxs-lookup"><span data-stu-id="9beec-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="9beec-106">句法</span><span class="sxs-lookup"><span data-stu-id="9beec-106">SYNTAX</span></span>

### <span data-ttu-id="9beec-107">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9beec-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-108">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-110">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-111">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-112">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-113">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beec-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="9beec-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9beec-125">說明</span><span class="sxs-lookup"><span data-stu-id="9beec-125">DESCRIPTION</span></span>
<span data-ttu-id="9beec-126">使用 Get-AzDenyAssignment 命令來列出所有在範圍中都有效的拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="9beec-127">如果沒有任何參數，這個命令會傳回在訂閱下所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="9beec-128">您可以使用 [本金] 的篩選參數、[拒絕作業名稱和範圍] 來篩選這個清單。</span><span class="sxs-lookup"><span data-stu-id="9beec-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="9beec-129">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="9beec-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="9beec-130">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="9beec-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="9beec-131">若要指定 Azure AD 應用程式，請使用 ServicePrincipalName 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="9beec-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="9beec-132">可能會指定存取權遭到拒絕的範圍。</span><span class="sxs-lookup"><span data-stu-id="9beec-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="9beec-133">預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9beec-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="9beec-134">可使用下列其中一個參數組合來指定拒絕作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="9beec-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="9beec-135">範圍-這是從/subscriptions/subscriptionId 開始的完整限定 \< 範圍 \> 。</span><span class="sxs-lookup"><span data-stu-id="9beec-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="9beec-136">這將會篩選在該特定範圍中有效的拒絕作業，亦即，在該範圍及上述全部拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="9beec-137">乙.</span><span class="sxs-lookup"><span data-stu-id="9beec-137">b.</span></span>
<span data-ttu-id="9beec-138">ResourceGroupName-訂閱下任何資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9beec-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="9beec-139">這將會在指定的資源群組上篩選指派，亦即在該範圍及更上方的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="9beec-140">c-clip.</span><span class="sxs-lookup"><span data-stu-id="9beec-140">c.</span></span>
<span data-ttu-id="9beec-141">[資源 ResourceGroupName]、[ResourceType]、[] 和 [ (] （選擇性）) ParentResource-識別訂閱下的特定資源，並且將在該資源範圍內篩選拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="9beec-142">若要判斷對訂閱中的特定使用者所拒絕的存取權，請使用 ExpandPrincipalGroups 開關。</span><span class="sxs-lookup"><span data-stu-id="9beec-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="9beec-143">這會列出指派給該使用者的所有拒絕作業，以及該使用者所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="9beec-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="9beec-144">示例</span><span class="sxs-lookup"><span data-stu-id="9beec-144">EXAMPLES</span></span>

### <span data-ttu-id="9beec-145">範例1</span><span class="sxs-lookup"><span data-stu-id="9beec-145">Example 1</span></span>

<span data-ttu-id="9beec-146">列出訂閱中的所有拒絕作業</span><span class="sxs-lookup"><span data-stu-id="9beec-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="9beec-147">範例2</span><span class="sxs-lookup"><span data-stu-id="9beec-147">Example 2</span></span>

<span data-ttu-id="9beec-148">取得在範圍 testRG 及更新版本中對使用者所做的全部拒絕作業 john.doe@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="9beec-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="9beec-149">範例3</span><span class="sxs-lookup"><span data-stu-id="9beec-149">Example 3</span></span>

<span data-ttu-id="9beec-150">取得指定服務主體的全部拒絕作業</span><span class="sxs-lookup"><span data-stu-id="9beec-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="9beec-151">範例4</span><span class="sxs-lookup"><span data-stu-id="9beec-151">Example 4</span></span>

<span data-ttu-id="9beec-152">取得「site1」網站範圍的拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="9beec-153">參數</span><span class="sxs-lookup"><span data-stu-id="9beec-153">PARAMETERS</span></span>

### <span data-ttu-id="9beec-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9beec-154">-DefaultProfile</span></span>
<span data-ttu-id="9beec-155">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9beec-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9beec-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="9beec-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="9beec-157">如果已指定，則會傳回直接指派給使用者的拒絕作業，以及使用者是其成員 (可) 的群組。</span><span class="sxs-lookup"><span data-stu-id="9beec-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="9beec-158">僅支援使用者主體。</span><span class="sxs-lookup"><span data-stu-id="9beec-158">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="9beec-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9beec-159">-ObjectId</span></span>
<span data-ttu-id="9beec-160">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="9beec-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="9beec-161">篩選對指定主體所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-161">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9beec-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="9beec-162">-ParentResource</span></span>
<span data-ttu-id="9beec-163">使用 [資源數] 參數指定之資源階層中的父資源。</span><span class="sxs-lookup"><span data-stu-id="9beec-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="9beec-164">必須與 ResourceGroupName、ResourceType 和 CoNtext.resourcename 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9beec-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="9beec-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9beec-165">-ResourceGroupName</span></span>
<span data-ttu-id="9beec-166">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9beec-166">The resource group name.</span></span>
<span data-ttu-id="9beec-167">列出在指定資源群組中生效的 [拒絕作業]。</span><span class="sxs-lookup"><span data-stu-id="9beec-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="9beec-168">當與 [資源清單]、[ResourceType] 和 [ParentResource] 參數搭配使用時，命令會列出 [拒絕作業] 在資源群組中的資源生效。</span><span class="sxs-lookup"><span data-stu-id="9beec-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="9beec-169">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="9beec-169">-ResourceName</span></span>
<span data-ttu-id="9beec-170">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9beec-170">The resource name.</span></span>
<span data-ttu-id="9beec-171">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="9beec-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="9beec-172">必須與 ResourceGroupName、ResourceType 及 (（選擇性）) ParentResource 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9beec-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="9beec-173">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9beec-173">-ResourceType</span></span>
<span data-ttu-id="9beec-174">資源類型。</span><span class="sxs-lookup"><span data-stu-id="9beec-174">The resource type.</span></span>
<span data-ttu-id="9beec-175">例如，. Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="9beec-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="9beec-176">必須與 ResourceGroupName、和 (（選擇性) ParentResource 參數）搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9beec-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="9beec-177">-範圍</span><span class="sxs-lookup"><span data-stu-id="9beec-177">-Scope</span></span>
<span data-ttu-id="9beec-178">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="9beec-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="9beec-179">相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="9beec-179">In the format of relative URI.</span></span>
<span data-ttu-id="9beec-180">例如/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG。</span><span class="sxs-lookup"><span data-stu-id="9beec-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="9beec-181">其開頭必須是 "/subscriptions/{id}"。</span><span class="sxs-lookup"><span data-stu-id="9beec-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="9beec-182">此命令會篩選在該範圍內生效的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-182">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="9beec-183">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9beec-183">-ServicePrincipalName</span></span>
<span data-ttu-id="9beec-184">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="9beec-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="9beec-185">篩選對指定的 Azure AD 應用程式所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="9beec-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="9beec-186">-SignInName</span></span>
<span data-ttu-id="9beec-187">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="9beec-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="9beec-188">篩選對指定使用者所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="9beec-188">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="9beec-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9beec-189">CommonParameters</span></span>
<span data-ttu-id="9beec-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9beec-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9beec-191">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9beec-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9beec-192">輸入</span><span class="sxs-lookup"><span data-stu-id="9beec-192">INPUTS</span></span>

### <span data-ttu-id="9beec-193">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="9beec-193">System.Guid</span></span>

### <span data-ttu-id="9beec-194">System.object</span><span class="sxs-lookup"><span data-stu-id="9beec-194">System.String</span></span>

## <span data-ttu-id="9beec-195">輸出</span><span class="sxs-lookup"><span data-stu-id="9beec-195">OUTPUTS</span></span>

### <span data-ttu-id="9beec-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="9beec-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="9beec-197">筆記</span><span class="sxs-lookup"><span data-stu-id="9beec-197">NOTES</span></span>
<span data-ttu-id="9beec-198">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="9beec-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>