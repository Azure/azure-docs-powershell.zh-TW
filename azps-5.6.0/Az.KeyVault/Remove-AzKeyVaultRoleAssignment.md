---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: f93adbf99667c2854557e71af8091012ea82bb74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917721"
---
# <span data-ttu-id="fcd83-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fcd83-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="fcd83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fcd83-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd83-103">移除指派給特定範圍中特定角色之指定主體的角色指派。</span><span class="sxs-lookup"><span data-stu-id="fcd83-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="fcd83-104">語法</span><span class="sxs-lookup"><span data-stu-id="fcd83-104">SYNTAX</span></span>

### <span data-ttu-id="fcd83-105">DefinitionNameSignInName (預設) </span><span class="sxs-lookup"><span data-stu-id="fcd83-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd83-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="fcd83-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd83-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="fcd83-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd83-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="fcd83-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd83-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="fcd83-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd83-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="fcd83-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd83-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcd83-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd83-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="fcd83-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd83-113">描述</span><span class="sxs-lookup"><span data-stu-id="fcd83-113">DESCRIPTION</span></span>
<span data-ttu-id="fcd83-114">使用 `Remove-AzKeyVaultRoleAssignment` Cmdlet 在給定範圍和給定角色中撤銷任何主體的存取權。</span><span class="sxs-lookup"><span data-stu-id="fcd83-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="fcd83-115">工作分派的物件，即必須指定主體。</span><span class="sxs-lookup"><span data-stu-id="fcd83-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="fcd83-116">主體可以是使用者 (使用 SignInName 或 ObjectId 參數來識別使用者) ，安全性群組 (會使用 ObjectId 參數來識別群組) 或服務主體 (使用 ApplicationId 或 ObjectId 參數來識別 ServicePrincipal。</span><span class="sxs-lookup"><span data-stu-id="fcd83-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="fcd83-117">必須使用 RoleDefinitionName 或 RoleDefinitionId 參數指定指派給主體的角色。</span><span class="sxs-lookup"><span data-stu-id="fcd83-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="fcd83-118">例子</span><span class="sxs-lookup"><span data-stu-id="fcd83-118">EXAMPLES</span></span>

### <span data-ttu-id="fcd83-119">範例 1</span><span class="sxs-lookup"><span data-stu-id="fcd83-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="fcd83-120">此範例在 "/keys" 範圍中撤銷 "" 的「受管理 HSM 策略系統管理員 user1@microsoft.com 」角色。</span><span class="sxs-lookup"><span data-stu-id="fcd83-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="fcd83-121">範例 2</span><span class="sxs-lookup"><span data-stu-id="fcd83-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="fcd83-122">此範例在所有範圍中撤銷 user1@microsoft.com "" 的所有角色。</span><span class="sxs-lookup"><span data-stu-id="fcd83-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="fcd83-123">參數</span><span class="sxs-lookup"><span data-stu-id="fcd83-123">PARAMETERS</span></span>

### <span data-ttu-id="fcd83-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fcd83-124">-ApplicationId</span></span>
<span data-ttu-id="fcd83-125">應用程式 SPN。</span><span class="sxs-lookup"><span data-stu-id="fcd83-125">The app SPN.</span></span>

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

### <span data-ttu-id="fcd83-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd83-126">-DefaultProfile</span></span>
<span data-ttu-id="fcd83-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcd83-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd83-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fcd83-128">-HsmName</span></span>
<span data-ttu-id="fcd83-129">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd83-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="fcd83-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcd83-130">-InputObject</span></span>
<span data-ttu-id="fcd83-131">角色指派物件。</span><span class="sxs-lookup"><span data-stu-id="fcd83-131">Role assignment object.</span></span>

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

### <span data-ttu-id="fcd83-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fcd83-132">-ObjectId</span></span>
<span data-ttu-id="fcd83-133">使用者或群組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcd83-133">The user or group object id.</span></span>

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

### <span data-ttu-id="fcd83-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcd83-134">-PassThru</span></span>
<span data-ttu-id="fcd83-135">還原 HSM 時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="fcd83-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="fcd83-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fcd83-136">-RoleAssignmentName</span></span>
<span data-ttu-id="fcd83-137">角色指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd83-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="fcd83-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fcd83-138">-RoleDefinitionId</span></span>
<span data-ttu-id="fcd83-139">指派主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcd83-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="fcd83-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fcd83-140">-RoleDefinitionName</span></span>
<span data-ttu-id="fcd83-141">要指派主體的 RBAC 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd83-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="fcd83-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="fcd83-142">-Scope</span></span>
<span data-ttu-id="fcd83-143">角色指派或定義適用的範圍，例如'/'或'/key'或'/key/{keyName}'。</span><span class="sxs-lookup"><span data-stu-id="fcd83-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="fcd83-144">省略時，會使用 '/'。</span><span class="sxs-lookup"><span data-stu-id="fcd83-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="fcd83-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="fcd83-145">-SignInName</span></span>
<span data-ttu-id="fcd83-146">使用者 SignInName。</span><span class="sxs-lookup"><span data-stu-id="fcd83-146">The user SignInName.</span></span>

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

### <span data-ttu-id="fcd83-147">-確認</span><span class="sxs-lookup"><span data-stu-id="fcd83-147">-Confirm</span></span>
<span data-ttu-id="fcd83-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fcd83-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcd83-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd83-149">-WhatIf</span></span>
<span data-ttu-id="fcd83-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcd83-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcd83-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcd83-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcd83-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd83-152">CommonParameters</span></span>
<span data-ttu-id="fcd83-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fcd83-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd83-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcd83-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd83-155">輸入</span><span class="sxs-lookup"><span data-stu-id="fcd83-155">INPUTS</span></span>

### <span data-ttu-id="fcd83-156">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fcd83-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="fcd83-157">輸出</span><span class="sxs-lookup"><span data-stu-id="fcd83-157">OUTPUTS</span></span>

### <span data-ttu-id="fcd83-158">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fcd83-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="fcd83-159">筆記</span><span class="sxs-lookup"><span data-stu-id="fcd83-159">NOTES</span></span>

## <span data-ttu-id="fcd83-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcd83-160">RELATED LINKS</span></span>
