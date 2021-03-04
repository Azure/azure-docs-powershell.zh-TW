---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 7de4753d47ff2a285da6a9d3d60e0f95fcbf6e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914818"
---
# <span data-ttu-id="74547-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="74547-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="74547-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74547-102">SYNOPSIS</span></span>
<span data-ttu-id="74547-103">取得或列出受管理 HSM 的角色指派。</span><span class="sxs-lookup"><span data-stu-id="74547-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="74547-104">使用各自的參數列出指派給特定使用者或角色定義。</span><span class="sxs-lookup"><span data-stu-id="74547-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="74547-105">語法</span><span class="sxs-lookup"><span data-stu-id="74547-105">SYNTAX</span></span>

### <span data-ttu-id="74547-106">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="74547-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74547-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="74547-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74547-108">描述</span><span class="sxs-lookup"><span data-stu-id="74547-108">DESCRIPTION</span></span>
<span data-ttu-id="74547-109">使用命令 `Get-AzKeyVaultRoleAssignment` 列出在範圍中有效的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="74547-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="74547-110">若沒有任何參數，此命令會返回受管理 HSM 下進行的所有角色指派。</span><span class="sxs-lookup"><span data-stu-id="74547-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="74547-111">此清單可以使用主體、角色和範圍的篩選參數進行篩選。</span><span class="sxs-lookup"><span data-stu-id="74547-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="74547-112">必須指定作業的主體。</span><span class="sxs-lookup"><span data-stu-id="74547-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="74547-113">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="74547-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="74547-114">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="74547-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="74547-115">若要指定 Azure AD 應用程式，請使用 ApplicationId 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="74547-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="74547-116">指派的角色必須使用 RoleDefinitionName 或 RoleDefinitionId 參數指定。</span><span class="sxs-lookup"><span data-stu-id="74547-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="74547-117">您可以指定授予存取權的範圍。</span><span class="sxs-lookup"><span data-stu-id="74547-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="74547-118">它預設為 "/"。</span><span class="sxs-lookup"><span data-stu-id="74547-118">It defaults to "/".</span></span>

## <span data-ttu-id="74547-119">例子</span><span class="sxs-lookup"><span data-stu-id="74547-119">EXAMPLES</span></span>

### <span data-ttu-id="74547-120">範例 1</span><span class="sxs-lookup"><span data-stu-id="74547-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="74547-121">此範例會列出所有範圍中所有 「my進一步」的角色指派。</span><span class="sxs-lookup"><span data-stu-id="74547-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="74547-122">範例 2</span><span class="sxs-lookup"><span data-stu-id="74547-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="74547-123">此範例會列出 「/keys」範圍中「my進一步」的所有角色指派，並按使用者登錄名稱篩選結果。</span><span class="sxs-lookup"><span data-stu-id="74547-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="74547-124">參數</span><span class="sxs-lookup"><span data-stu-id="74547-124">PARAMETERS</span></span>

### <span data-ttu-id="74547-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="74547-125">-ApplicationId</span></span>
<span data-ttu-id="74547-126">應用程式 SPN。</span><span class="sxs-lookup"><span data-stu-id="74547-126">The app SPN.</span></span>

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

### <span data-ttu-id="74547-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74547-127">-DefaultProfile</span></span>
<span data-ttu-id="74547-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74547-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74547-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="74547-129">-HsmName</span></span>
<span data-ttu-id="74547-130">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="74547-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="74547-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="74547-131">-ObjectId</span></span>
<span data-ttu-id="74547-132">使用者或群組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="74547-132">The user or group object id.</span></span>

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

### <span data-ttu-id="74547-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="74547-133">-RoleAssignmentName</span></span>
<span data-ttu-id="74547-134">角色指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="74547-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="74547-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="74547-135">-RoleDefinitionId</span></span>
<span data-ttu-id="74547-136">指派主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="74547-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="74547-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="74547-137">-RoleDefinitionName</span></span>
<span data-ttu-id="74547-138">要指派主體的 RBAC 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="74547-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="74547-139">-範圍</span><span class="sxs-lookup"><span data-stu-id="74547-139">-Scope</span></span>
<span data-ttu-id="74547-140">角色指派或定義適用的範圍，例如'/'或'/key'或'/key/{keyName}'。</span><span class="sxs-lookup"><span data-stu-id="74547-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="74547-141">省略時，會使用 '/'。</span><span class="sxs-lookup"><span data-stu-id="74547-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="74547-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="74547-142">-SignInName</span></span>
<span data-ttu-id="74547-143">使用者 SignInName。</span><span class="sxs-lookup"><span data-stu-id="74547-143">The user SignInName.</span></span>

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

### <span data-ttu-id="74547-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74547-144">CommonParameters</span></span>
<span data-ttu-id="74547-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74547-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74547-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74547-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74547-147">輸入</span><span class="sxs-lookup"><span data-stu-id="74547-147">INPUTS</span></span>

### <span data-ttu-id="74547-148">沒有</span><span class="sxs-lookup"><span data-stu-id="74547-148">None</span></span>

## <span data-ttu-id="74547-149">輸出</span><span class="sxs-lookup"><span data-stu-id="74547-149">OUTPUTS</span></span>

### <span data-ttu-id="74547-150">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="74547-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="74547-151">筆記</span><span class="sxs-lookup"><span data-stu-id="74547-151">NOTES</span></span>

## <span data-ttu-id="74547-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="74547-152">RELATED LINKS</span></span>
