---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 9de4cc6572a20dc9ec241c6f93cb035162b914f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916937"
---
# <span data-ttu-id="577b2-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="577b2-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="577b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="577b2-102">SYNOPSIS</span></span>
<span data-ttu-id="577b2-103">將金鑰庫中已刪除的金鑰復原為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="577b2-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="577b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="577b2-104">SYNTAX</span></span>

### <span data-ttu-id="577b2-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="577b2-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="577b2-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="577b2-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="577b2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="577b2-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="577b2-108">描述</span><span class="sxs-lookup"><span data-stu-id="577b2-108">DESCRIPTION</span></span>
<span data-ttu-id="577b2-109">**Undo-AzKeyVaultKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="577b2-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="577b2-110">復原的金鑰將會為使用中，而且可用於所有一般金鑰作業。</span><span class="sxs-lookup"><span data-stu-id="577b2-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="577b2-111">來電者必須擁有復原許可權，才能執行此作業。</span><span class="sxs-lookup"><span data-stu-id="577b2-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="577b2-112">例子</span><span class="sxs-lookup"><span data-stu-id="577b2-112">EXAMPLES</span></span>

### <span data-ttu-id="577b2-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="577b2-113">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="577b2-114">此命令將會將先前刪除的金鑰 "MyKey" 復原為使用中且可用狀態。</span><span class="sxs-lookup"><span data-stu-id="577b2-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="577b2-115">參數</span><span class="sxs-lookup"><span data-stu-id="577b2-115">PARAMETERS</span></span>

### <span data-ttu-id="577b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577b2-116">-DefaultProfile</span></span>
<span data-ttu-id="577b2-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="577b2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="577b2-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="577b2-118">-HsmName</span></span>
<span data-ttu-id="577b2-119">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="577b2-119">HSM name.</span></span> <span data-ttu-id="577b2-120">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="577b2-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577b2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="577b2-121">-InputObject</span></span>
<span data-ttu-id="577b2-122">已刪除的金鑰組象</span><span class="sxs-lookup"><span data-stu-id="577b2-122">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577b2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="577b2-123">-Name</span></span>
<span data-ttu-id="577b2-124">金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="577b2-124">Key name.</span></span>
<span data-ttu-id="577b2-125">Cmdlet 會從儲存庫名稱、目前選取的環境和金鑰名稱建構金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="577b2-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577b2-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="577b2-126">-VaultName</span></span>
<span data-ttu-id="577b2-127">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="577b2-127">Vault name.</span></span>
<span data-ttu-id="577b2-128">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="577b2-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577b2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="577b2-129">-Confirm</span></span>
<span data-ttu-id="577b2-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="577b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577b2-131">-WhatIf</span></span>
<span data-ttu-id="577b2-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="577b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577b2-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="577b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577b2-134">CommonParameters</span></span>
<span data-ttu-id="577b2-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="577b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577b2-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="577b2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577b2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="577b2-137">INPUTS</span></span>

### <span data-ttu-id="577b2-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="577b2-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="577b2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="577b2-139">OUTPUTS</span></span>

### <span data-ttu-id="577b2-140">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="577b2-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="577b2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="577b2-141">NOTES</span></span>

## <span data-ttu-id="577b2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="577b2-142">RELATED LINKS</span></span>

[<span data-ttu-id="577b2-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="577b2-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="577b2-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="577b2-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="577b2-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="577b2-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

