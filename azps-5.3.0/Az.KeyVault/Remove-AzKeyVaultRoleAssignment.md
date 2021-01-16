---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439328"
---
# <span data-ttu-id="b9815-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b9815-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b9815-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9815-102">SYNOPSIS</span></span>
<span data-ttu-id="b9815-103">移除指派給特定作用域中特定角色之指定原則的角色指派。</span><span class="sxs-lookup"><span data-stu-id="b9815-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="b9815-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9815-104">SYNTAX</span></span>

### <span data-ttu-id="b9815-105">DefinitionNameSignInName (預設) </span><span class="sxs-lookup"><span data-stu-id="b9815-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9815-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="b9815-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9815-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="b9815-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9815-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="b9815-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9815-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="b9815-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9815-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="b9815-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9815-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9815-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9815-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9815-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9815-113">說明</span><span class="sxs-lookup"><span data-stu-id="b9815-113">DESCRIPTION</span></span>
<span data-ttu-id="b9815-114">使用 `Remove-AzKeyVaultRoleAssignment` Cmdlet 撤銷對指定範圍和指定角色的任何主體的存取權。</span><span class="sxs-lookup"><span data-stu-id="b9815-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="b9815-115">作業的物件（亦即必須指定 principal）。</span><span class="sxs-lookup"><span data-stu-id="b9815-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="b9815-116">主體可以是使用者 (使用 SignInName 或 ObjectId 參數來識別使用者) 、安全性群組 (使用 ObjectId 參數來識別群組) 或服務主體 (使用 ApplicationId 或 ObjectId 參數來識別 ServicePrincipal。</span><span class="sxs-lookup"><span data-stu-id="b9815-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="b9815-117">承擔者所指派的角色，必須使用 RoleDefinitionName 或 RoleDefinitionId 參數加以指定。</span><span class="sxs-lookup"><span data-stu-id="b9815-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="b9815-118">示例</span><span class="sxs-lookup"><span data-stu-id="b9815-118">EXAMPLES</span></span>

### <span data-ttu-id="b9815-119">範例1</span><span class="sxs-lookup"><span data-stu-id="b9815-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="b9815-120">這個範例會 user1@microsoft.com 在 "/keys" 範圍撤銷「受管理的 HSM 原則系統管理員」角色。</span><span class="sxs-lookup"><span data-stu-id="b9815-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="b9815-121">範例2</span><span class="sxs-lookup"><span data-stu-id="b9815-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="b9815-122">這個範例會撤銷所有作用中 "" 的所有角色 user1@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="b9815-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="b9815-123">參數</span><span class="sxs-lookup"><span data-stu-id="b9815-123">PARAMETERS</span></span>

### <span data-ttu-id="b9815-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b9815-124">-ApplicationId</span></span>
<span data-ttu-id="b9815-125">應用程式 SPN。</span><span class="sxs-lookup"><span data-stu-id="b9815-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9815-126">-DefaultProfile</span></span>
<span data-ttu-id="b9815-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9815-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9815-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b9815-128">-HsmName</span></span>
<span data-ttu-id="b9815-129">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9815-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9815-130">-InputObject</span></span>
<span data-ttu-id="b9815-131">角色指派物件。</span><span class="sxs-lookup"><span data-stu-id="b9815-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b9815-132">-ObjectId</span></span>
<span data-ttu-id="b9815-133">[使用者] 或 [群組] 物件 id。</span><span class="sxs-lookup"><span data-stu-id="b9815-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9815-134">-PassThru</span></span>
<span data-ttu-id="b9815-135">還原 HSM 時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="b9815-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="b9815-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b9815-136">-RoleAssignmentName</span></span>
<span data-ttu-id="b9815-137">角色指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9815-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b9815-138">-RoleDefinitionId</span></span>
<span data-ttu-id="b9815-139">指派主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9815-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b9815-140">-RoleDefinitionName</span></span>
<span data-ttu-id="b9815-141">要指派主體的 RBAC 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="b9815-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="b9815-142">-Scope</span></span>
<span data-ttu-id="b9815-143">角色指派或定義適用的範圍，例如，"/" 或 "/keys" 或 "/keys/{keyName}"。</span><span class="sxs-lookup"><span data-stu-id="b9815-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="b9815-144">省略時使用 "/"。</span><span class="sxs-lookup"><span data-stu-id="b9815-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="b9815-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b9815-145">-SignInName</span></span>
<span data-ttu-id="b9815-146">[使用者 SignInName]。</span><span class="sxs-lookup"><span data-stu-id="b9815-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9815-147">-確認</span><span class="sxs-lookup"><span data-stu-id="b9815-147">-Confirm</span></span>
<span data-ttu-id="b9815-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9815-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9815-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9815-149">-WhatIf</span></span>
<span data-ttu-id="b9815-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9815-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9815-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9815-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9815-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9815-152">CommonParameters</span></span>
<span data-ttu-id="b9815-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9815-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9815-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9815-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9815-155">輸入</span><span class="sxs-lookup"><span data-stu-id="b9815-155">INPUTS</span></span>

### <span data-ttu-id="b9815-156">PSKeyVaultRoleAssignment 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b9815-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b9815-157">輸出</span><span class="sxs-lookup"><span data-stu-id="b9815-157">OUTPUTS</span></span>

### <span data-ttu-id="b9815-158">PSKeyVaultRoleAssignment 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b9815-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b9815-159">筆記</span><span class="sxs-lookup"><span data-stu-id="b9815-159">NOTES</span></span>

## <span data-ttu-id="b9815-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9815-160">RELATED LINKS</span></span>
