---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: c3988727e8afd54dddea9719c348222c41f47503
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449545"
---
# <span data-ttu-id="b869e-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b869e-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="b869e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b869e-102">SYNOPSIS</span></span>
<span data-ttu-id="b869e-103">在指定的範圍內，將指定的 RBAC 角色指派給指定的主體。</span><span class="sxs-lookup"><span data-stu-id="b869e-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b869e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b869e-104">SYNTAX</span></span>

### <span data-ttu-id="b869e-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b869e-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b869e-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b869e-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b869e-116">說明</span><span class="sxs-lookup"><span data-stu-id="b869e-116">DESCRIPTION</span></span>
<span data-ttu-id="b869e-117">使用 New-AzureRMRoleAssignment 命令來授與存取權。</span><span class="sxs-lookup"><span data-stu-id="b869e-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="b869e-118">您可以在適當的範圍內指派適當的 RBAC 角色來取得存取權。</span><span class="sxs-lookup"><span data-stu-id="b869e-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="b869e-119">若要授與整個訂閱的存取權，請在訂閱範圍指派一個角色。</span><span class="sxs-lookup"><span data-stu-id="b869e-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="b869e-120">若要在訂閱中授與特定資源群組的存取權，請在資源群組範圍中指派一個角色。</span><span class="sxs-lookup"><span data-stu-id="b869e-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="b869e-121">必須指定作業的主語。</span><span class="sxs-lookup"><span data-stu-id="b869e-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="b869e-122">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="b869e-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="b869e-123">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="b869e-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="b869e-124">若要指定 Azure AD 應用程式，請使用 ServicePrincipalName 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="b869e-124">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="b869e-125">所指派的角色，必須使用 RoleDefinitionName 參數加以指定。</span><span class="sxs-lookup"><span data-stu-id="b869e-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="b869e-126">您可以指定授權存取的範圍。</span><span class="sxs-lookup"><span data-stu-id="b869e-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="b869e-127">預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b869e-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="b869e-128">您可以使用下列其中一個參數組合來指定作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="b869e-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="b869e-129">範圍-這是從/subscriptions/b 開始的完整範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="b869e-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="b869e-130">ResourceGroupName-以授與指定資源群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="b869e-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="b869e-131">c-clip.</span><span class="sxs-lookup"><span data-stu-id="b869e-131">c.</span></span>
<span data-ttu-id="b869e-132">[資源 ResourceGroupName]、[ResourceType]、[] 和 [ (] （ParentResource）) ）指定資源群組中要授與存取權的特定資源。</span><span class="sxs-lookup"><span data-stu-id="b869e-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="b869e-133">示例</span><span class="sxs-lookup"><span data-stu-id="b869e-133">EXAMPLES</span></span>

### <span data-ttu-id="b869e-134">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b869e-134">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader
```

<span data-ttu-id="b869e-135">授與讀者角色存取資源群組作用中的使用者</span><span class="sxs-lookup"><span data-stu-id="b869e-135">Grant Reader role access to a user at a resource group scope</span></span>

### <span data-ttu-id="b869e-136">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b869e-136">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="b869e-137">授與安全群組的存取權</span><span class="sxs-lookup"><span data-stu-id="b869e-137">Grant access to a security group</span></span>

### <span data-ttu-id="b869e-138">--------------------------範例 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="b869e-138">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="b869e-139">在資源 (網站上授與使用者的存取權) </span><span class="sxs-lookup"><span data-stu-id="b869e-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="b869e-140">--------------------------範例 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="b869e-140">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="b869e-141">在嵌套資源 (子網上) ，授與群組的存取權</span><span class="sxs-lookup"><span data-stu-id="b869e-141">Grant access to a group at a nested resource (subnet)</span></span>

## <span data-ttu-id="b869e-142">參數</span><span class="sxs-lookup"><span data-stu-id="b869e-142">PARAMETERS</span></span>

### <span data-ttu-id="b869e-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b869e-143">-ObjectId</span></span>
<span data-ttu-id="b869e-144">使用者、群組或服務主體的 Azure AD Objectid。</span><span class="sxs-lookup"><span data-stu-id="b869e-144">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b869e-145">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b869e-145">-ParentResource</span></span>
<span data-ttu-id="b869e-146">層次結構中的父資源， (使用資源使用不足的) 參數指定的資源。</span><span class="sxs-lookup"><span data-stu-id="b869e-146">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="b869e-147">只能與 ResourceGroupName、ResourceType 和資源類型參數搭配使用，以以相對 URI 的形式來構造階層範圍，以識別資源。</span><span class="sxs-lookup"><span data-stu-id="b869e-147">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b869e-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b869e-148">-ResourceGroupName</span></span>
<span data-ttu-id="b869e-149">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b869e-149">The resource group name.</span></span>
<span data-ttu-id="b869e-150">建立可在指定資源群組中生效的作業。</span><span class="sxs-lookup"><span data-stu-id="b869e-150">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="b869e-151">與資源中心、ResourceType 和 (（可選擇) ParentResource 參數）搭配使用時，命令會以相對 URI 的形式來構造階層範圍，以識別資源。</span><span class="sxs-lookup"><span data-stu-id="b869e-151">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b869e-152">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="b869e-152">-ResourceName</span></span>
<span data-ttu-id="b869e-153">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b869e-153">The resource name.</span></span>
<span data-ttu-id="b869e-154">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="b869e-154">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="b869e-155">只能與 ResourceGroupName、ResourceType 及 (（選擇性）) ParentResource 參數，以以相對 URI 的形式來構造階層範圍，以識別資源。</span><span class="sxs-lookup"><span data-stu-id="b869e-155">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b869e-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b869e-156">-ResourceType</span></span>
<span data-ttu-id="b869e-157">資源類型。</span><span class="sxs-lookup"><span data-stu-id="b869e-157">The resource type.</span></span>
<span data-ttu-id="b869e-158">例如，. Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="b869e-158">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="b869e-159">只能與 ResourceGroupName、CoNtext.resourcename 和 (搭配使用，) ParentResource 參數，以以相對 URI 的形式來構造階層範圍，以識別資源。</span><span class="sxs-lookup"><span data-stu-id="b869e-159">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="b869e-160">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b869e-160">-RoleDefinitionId</span></span>
<span data-ttu-id="b869e-161">需要指派給主體的 RBAC 角色 Id。</span><span class="sxs-lookup"><span data-stu-id="b869e-161">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="b869e-162">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b869e-162">-RoleDefinitionName</span></span>
<span data-ttu-id="b869e-163">需要指派給 principal （例如讀者、參與者、虛擬網路管理員等）的 RBAC 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="b869e-163">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b869e-164">-範圍</span><span class="sxs-lookup"><span data-stu-id="b869e-164">-Scope</span></span>
<span data-ttu-id="b869e-165">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="b869e-165">The Scope of the role assignment.</span></span>
<span data-ttu-id="b869e-166">相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="b869e-166">In the format of relative URI.</span></span>
<span data-ttu-id="b869e-167">例如，"/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG"。</span><span class="sxs-lookup"><span data-stu-id="b869e-167">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="b869e-168">如果未指定，將會在訂閱層級建立角色指派。</span><span class="sxs-lookup"><span data-stu-id="b869e-168">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="b869e-169">如果已指定，它應該以 "/subscriptions/{id}" 為開頭。</span><span class="sxs-lookup"><span data-stu-id="b869e-169">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b869e-170">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b869e-170">-ServicePrincipalName</span></span>
<span data-ttu-id="b869e-171">Azure AD 應用程式的 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b869e-171">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b869e-172">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b869e-172">-SignInName</span></span>
<span data-ttu-id="b869e-173">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="b869e-173">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="b869e-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b869e-174">-DefaultProfile</span></span>
<span data-ttu-id="b869e-175">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b869e-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b869e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b869e-176">CommonParameters</span></span>
<span data-ttu-id="b869e-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b869e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b869e-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b869e-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b869e-179">輸入</span><span class="sxs-lookup"><span data-stu-id="b869e-179">INPUTS</span></span>

## <span data-ttu-id="b869e-180">輸出</span><span class="sxs-lookup"><span data-stu-id="b869e-180">OUTPUTS</span></span>

### <span data-ttu-id="b869e-181">PSRoleAssignment 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="b869e-181">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="b869e-182">筆記</span><span class="sxs-lookup"><span data-stu-id="b869e-182">NOTES</span></span>
<span data-ttu-id="b869e-183">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="b869e-183">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b869e-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="b869e-184">RELATED LINKS</span></span>

[<span data-ttu-id="b869e-185">AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b869e-185">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="b869e-186">移除-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b869e-186">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="b869e-187">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b869e-187">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
