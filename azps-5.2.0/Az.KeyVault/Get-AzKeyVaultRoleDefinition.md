---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273472"
---
# <span data-ttu-id="cd134-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cd134-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="cd134-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd134-102">SYNOPSIS</span></span>
<span data-ttu-id="cd134-103">列出指定範圍內的特定受管理 HSM 的角色定義。</span><span class="sxs-lookup"><span data-stu-id="cd134-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="cd134-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd134-104">SYNTAX</span></span>

### <span data-ttu-id="cd134-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="cd134-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd134-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cd134-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd134-107">說明</span><span class="sxs-lookup"><span data-stu-id="cd134-107">DESCRIPTION</span></span>
<span data-ttu-id="cd134-108">列出指定範圍內的特定受管理 HSM 的角色定義。</span><span class="sxs-lookup"><span data-stu-id="cd134-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="cd134-109">示例</span><span class="sxs-lookup"><span data-stu-id="cd134-109">EXAMPLES</span></span>

### <span data-ttu-id="cd134-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cd134-110">Example 1</span></span>
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

<span data-ttu-id="cd134-111">此範例會列出「/keys」作用域中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="cd134-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="cd134-112">範例2</span><span class="sxs-lookup"><span data-stu-id="cd134-112">Example 2</span></span>
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

<span data-ttu-id="cd134-113">這個範例會取得「受管理的 HSM 備份」角色，並檢查它的許可權。</span><span class="sxs-lookup"><span data-stu-id="cd134-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="cd134-114">參數</span><span class="sxs-lookup"><span data-stu-id="cd134-114">PARAMETERS</span></span>

### <span data-ttu-id="cd134-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd134-115">-DefaultProfile</span></span>
<span data-ttu-id="cd134-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd134-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd134-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="cd134-117">-HsmName</span></span>
<span data-ttu-id="cd134-118">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd134-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="cd134-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="cd134-119">-RoleDefinitionName</span></span>
<span data-ttu-id="cd134-120">要取得的角色定義名稱。</span><span class="sxs-lookup"><span data-stu-id="cd134-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="cd134-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="cd134-121">-Scope</span></span>
<span data-ttu-id="cd134-122">角色指派或定義適用的範圍，例如，"/" 或 "/keys" 或 "/keys/{keyName}"。</span><span class="sxs-lookup"><span data-stu-id="cd134-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="cd134-123">省略時使用 "/"。</span><span class="sxs-lookup"><span data-stu-id="cd134-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="cd134-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd134-124">CommonParameters</span></span>
<span data-ttu-id="cd134-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd134-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd134-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cd134-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd134-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cd134-127">INPUTS</span></span>

### <span data-ttu-id="cd134-128">所有</span><span class="sxs-lookup"><span data-stu-id="cd134-128">None</span></span>

## <span data-ttu-id="cd134-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cd134-129">OUTPUTS</span></span>

### <span data-ttu-id="cd134-130">PSKeyVaultRoleDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="cd134-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="cd134-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cd134-131">NOTES</span></span>

## <span data-ttu-id="cd134-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd134-132">RELATED LINKS</span></span>
