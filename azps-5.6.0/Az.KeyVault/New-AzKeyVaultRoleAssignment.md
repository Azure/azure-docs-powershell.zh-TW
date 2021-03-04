---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ae55bf782f627c17cd73cbb075fd9f0d36ae6081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914773"
---
# <span data-ttu-id="42303-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="42303-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="42303-102">簡介</span><span class="sxs-lookup"><span data-stu-id="42303-102">SYNOPSIS</span></span>
<span data-ttu-id="42303-103">將指定的 RBAC 角色指派給指定範圍中的指定主體。</span><span class="sxs-lookup"><span data-stu-id="42303-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="42303-104">語法</span><span class="sxs-lookup"><span data-stu-id="42303-104">SYNTAX</span></span>

### <span data-ttu-id="42303-105">DefinitionNameSignInName (預設) </span><span class="sxs-lookup"><span data-stu-id="42303-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42303-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="42303-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42303-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="42303-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42303-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="42303-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42303-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="42303-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42303-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="42303-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42303-111">描述</span><span class="sxs-lookup"><span data-stu-id="42303-111">DESCRIPTION</span></span>
<span data-ttu-id="42303-112">使用命令 `New-AzKeyVaultRoleAssignment` 來授予存取權。</span><span class="sxs-lookup"><span data-stu-id="42303-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="42303-113">Access 是在正確的範圍中指派適當的 RBAC 角色給他們，以授予存取權。</span><span class="sxs-lookup"><span data-stu-id="42303-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="42303-114">必須指定作業的主體。</span><span class="sxs-lookup"><span data-stu-id="42303-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="42303-115">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="42303-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="42303-116">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="42303-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="42303-117">若要指定 Azure AD 應用程式，請使用 ApplicationId 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="42303-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="42303-118">指派的角色必須使用 RoleDefinitionName pr RoleDefinitionId 參數指定。</span><span class="sxs-lookup"><span data-stu-id="42303-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="42303-119">您可以指定授予存取權的範圍。</span><span class="sxs-lookup"><span data-stu-id="42303-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="42303-120">它會預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="42303-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="42303-121">例子</span><span class="sxs-lookup"><span data-stu-id="42303-121">EXAMPLES</span></span>

### <span data-ttu-id="42303-122">範例 1</span><span class="sxs-lookup"><span data-stu-id="42303-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="42303-123">此範例將角色「受管理的 HSM 策略管理員」指派給使用者」在 user1@microsoft.com 最上方的範圍。</span><span class="sxs-lookup"><span data-stu-id="42303-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="42303-124">參數</span><span class="sxs-lookup"><span data-stu-id="42303-124">PARAMETERS</span></span>

### <span data-ttu-id="42303-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="42303-125">-ApplicationId</span></span>
<span data-ttu-id="42303-126">應用程式 SPN。</span><span class="sxs-lookup"><span data-stu-id="42303-126">The app SPN.</span></span>

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

### <span data-ttu-id="42303-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42303-127">-DefaultProfile</span></span>
<span data-ttu-id="42303-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="42303-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42303-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="42303-129">-HsmName</span></span>
<span data-ttu-id="42303-130">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="42303-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="42303-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="42303-131">-ObjectId</span></span>
<span data-ttu-id="42303-132">使用者或群組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="42303-132">The user or group object id.</span></span>

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

### <span data-ttu-id="42303-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="42303-133">-RoleDefinitionId</span></span>
<span data-ttu-id="42303-134">指派主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="42303-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="42303-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="42303-135">-RoleDefinitionName</span></span>
<span data-ttu-id="42303-136">要指派主體的 RBAC 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="42303-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="42303-137">-範圍</span><span class="sxs-lookup"><span data-stu-id="42303-137">-Scope</span></span>
<span data-ttu-id="42303-138">角色指派或定義適用的範圍，例如'/'或'/key'或'/key/{keyName}'。</span><span class="sxs-lookup"><span data-stu-id="42303-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="42303-139">省略時，會使用 '/'。</span><span class="sxs-lookup"><span data-stu-id="42303-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="42303-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="42303-140">-SignInName</span></span>
<span data-ttu-id="42303-141">使用者 SignInName。</span><span class="sxs-lookup"><span data-stu-id="42303-141">The user SignInName.</span></span>

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

### <span data-ttu-id="42303-142">-確認</span><span class="sxs-lookup"><span data-stu-id="42303-142">-Confirm</span></span>
<span data-ttu-id="42303-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="42303-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42303-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42303-144">-WhatIf</span></span>
<span data-ttu-id="42303-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42303-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42303-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42303-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42303-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42303-147">CommonParameters</span></span>
<span data-ttu-id="42303-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="42303-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42303-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42303-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42303-150">輸入</span><span class="sxs-lookup"><span data-stu-id="42303-150">INPUTS</span></span>

### <span data-ttu-id="42303-151">沒有</span><span class="sxs-lookup"><span data-stu-id="42303-151">None</span></span>

## <span data-ttu-id="42303-152">輸出</span><span class="sxs-lookup"><span data-stu-id="42303-152">OUTPUTS</span></span>

### <span data-ttu-id="42303-153">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="42303-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="42303-154">筆記</span><span class="sxs-lookup"><span data-stu-id="42303-154">NOTES</span></span>

## <span data-ttu-id="42303-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="42303-155">RELATED LINKS</span></span>
