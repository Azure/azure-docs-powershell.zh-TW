---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133099"
---
# <span data-ttu-id="dfcfb-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dfcfb-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="dfcfb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcfb-103">取得或列出受管理 HSM 的角色指派。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="dfcfb-104">使用個別的參數，將作業清單指派給特定的使用者或角色定義。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="dfcfb-105">句法</span><span class="sxs-lookup"><span data-stu-id="dfcfb-105">SYNTAX</span></span>

### <span data-ttu-id="dfcfb-106"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="dfcfb-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfcfb-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="dfcfb-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfcfb-108">說明</span><span class="sxs-lookup"><span data-stu-id="dfcfb-108">DESCRIPTION</span></span>
<span data-ttu-id="dfcfb-109">使用 `Get-AzKeyVaultRoleAssignment` 命令來列出所有在範圍中有效的角色指派。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="dfcfb-110">如果沒有任何參數，這個命令會傳回受管理的 HSM 下所做的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="dfcfb-111">您可以使用 [主要]、[角色] 和 [範圍] 的篩選參數來篩選此清單。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="dfcfb-112">必須指定作業的主語。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="dfcfb-113">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="dfcfb-114">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="dfcfb-115">若要指定 Azure AD 應用程式，請使用 ApplicationId 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="dfcfb-116">所指派的角色，必須使用 RoleDefinitionName 或 RoleDefinitionId 參數加以指定。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="dfcfb-117">您可以指定授權存取的範圍。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="dfcfb-118">預設值為 "/"。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-118">It defaults to "/".</span></span>

## <span data-ttu-id="dfcfb-119">示例</span><span class="sxs-lookup"><span data-stu-id="dfcfb-119">EXAMPLES</span></span>

### <span data-ttu-id="dfcfb-120">範例1</span><span class="sxs-lookup"><span data-stu-id="dfcfb-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="dfcfb-121">這個範例會列出所有作用域上「myHsm」的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="dfcfb-122">範例2</span><span class="sxs-lookup"><span data-stu-id="dfcfb-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="dfcfb-123">這個範例會列出「/keys」作用域上「myHsm」的所有角色指派，並依使用者登入名稱篩選結果。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="dfcfb-124">參數</span><span class="sxs-lookup"><span data-stu-id="dfcfb-124">PARAMETERS</span></span>

### <span data-ttu-id="dfcfb-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dfcfb-125">-ApplicationId</span></span>
<span data-ttu-id="dfcfb-126">應用程式 SPN。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcfb-127">-DefaultProfile</span></span>
<span data-ttu-id="dfcfb-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfcfb-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="dfcfb-129">-HsmName</span></span>
<span data-ttu-id="dfcfb-130">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dfcfb-131">-ObjectId</span></span>
<span data-ttu-id="dfcfb-132">[使用者] 或 [群組] 物件 id。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="dfcfb-133">-RoleAssignmentName</span></span>
<span data-ttu-id="dfcfb-134">角色指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dfcfb-135">-RoleDefinitionId</span></span>
<span data-ttu-id="dfcfb-136">指派主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="dfcfb-137">-RoleDefinitionName</span></span>
<span data-ttu-id="dfcfb-138">要指派主體的 RBAC 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-139">-範圍</span><span class="sxs-lookup"><span data-stu-id="dfcfb-139">-Scope</span></span>
<span data-ttu-id="dfcfb-140">角色指派或定義適用的範圍，例如，"/" 或 "/keys" 或 "/keys/{keyName}"。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="dfcfb-141">省略時使用 "/"。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-141">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="dfcfb-142">-SignInName</span></span>
<span data-ttu-id="dfcfb-143">[使用者 SignInName]。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcfb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcfb-144">CommonParameters</span></span>
<span data-ttu-id="dfcfb-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcfb-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcfb-147">輸入</span><span class="sxs-lookup"><span data-stu-id="dfcfb-147">INPUTS</span></span>

### <span data-ttu-id="dfcfb-148">所有</span><span class="sxs-lookup"><span data-stu-id="dfcfb-148">None</span></span>

## <span data-ttu-id="dfcfb-149">輸出</span><span class="sxs-lookup"><span data-stu-id="dfcfb-149">OUTPUTS</span></span>

### <span data-ttu-id="dfcfb-150">PSKeyVaultRoleAssignment 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="dfcfb-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="dfcfb-151">筆記</span><span class="sxs-lookup"><span data-stu-id="dfcfb-151">NOTES</span></span>

## <span data-ttu-id="dfcfb-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfcfb-152">RELATED LINKS</span></span>
