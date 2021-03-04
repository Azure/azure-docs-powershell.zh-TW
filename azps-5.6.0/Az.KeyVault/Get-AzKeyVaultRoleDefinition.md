---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: b5d5da8c02081437f064fc1d2a6a29a5b772e8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914813"
---
# <span data-ttu-id="690cb-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="690cb-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="690cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="690cb-102">SYNOPSIS</span></span>
<span data-ttu-id="690cb-103">在給定範圍中列出受管理 HSM 的角色定義。</span><span class="sxs-lookup"><span data-stu-id="690cb-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="690cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="690cb-104">SYNTAX</span></span>

### <span data-ttu-id="690cb-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="690cb-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="690cb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="690cb-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="690cb-107">描述</span><span class="sxs-lookup"><span data-stu-id="690cb-107">DESCRIPTION</span></span>
<span data-ttu-id="690cb-108">在給定範圍中列出受管理 HSM 的角色定義。</span><span class="sxs-lookup"><span data-stu-id="690cb-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="690cb-109">例子</span><span class="sxs-lookup"><span data-stu-id="690cb-109">EXAMPLES</span></span>

### <span data-ttu-id="690cb-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="690cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="690cb-111">範例會以「/鍵」範圍列出所有角色。</span><span class="sxs-lookup"><span data-stu-id="690cb-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="690cb-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="690cb-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="690cb-113">此範例會獲得「受管理的 HSM 備份」角色，並檢查其許可權。</span><span class="sxs-lookup"><span data-stu-id="690cb-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="690cb-114">參數</span><span class="sxs-lookup"><span data-stu-id="690cb-114">PARAMETERS</span></span>

### <span data-ttu-id="690cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690cb-115">-DefaultProfile</span></span>
<span data-ttu-id="690cb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="690cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="690cb-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="690cb-117">-HsmName</span></span>
<span data-ttu-id="690cb-118">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="690cb-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="690cb-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="690cb-119">-RoleDefinitionName</span></span>
<span data-ttu-id="690cb-120">要取得的角色定義名稱。</span><span class="sxs-lookup"><span data-stu-id="690cb-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690cb-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="690cb-121">-Scope</span></span>
<span data-ttu-id="690cb-122">角色指派或定義適用的範圍，例如'/'或'/key'或'/key/{keyName}'。</span><span class="sxs-lookup"><span data-stu-id="690cb-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="690cb-123">省略時，會使用 '/'。</span><span class="sxs-lookup"><span data-stu-id="690cb-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="690cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690cb-124">CommonParameters</span></span>
<span data-ttu-id="690cb-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="690cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690cb-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="690cb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690cb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="690cb-127">INPUTS</span></span>

### <span data-ttu-id="690cb-128">沒有</span><span class="sxs-lookup"><span data-stu-id="690cb-128">None</span></span>

## <span data-ttu-id="690cb-129">輸出</span><span class="sxs-lookup"><span data-stu-id="690cb-129">OUTPUTS</span></span>

### <span data-ttu-id="690cb-130">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="690cb-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="690cb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="690cb-131">NOTES</span></span>

## <span data-ttu-id="690cb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="690cb-132">RELATED LINKS</span></span>
