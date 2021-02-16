---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131742"
---
# <span data-ttu-id="47347-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="47347-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="47347-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47347-102">SYNOPSIS</span></span>
<span data-ttu-id="47347-103">將 [金鑰 vault] 中的已刪除金鑰復原為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="47347-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="47347-104">句法</span><span class="sxs-lookup"><span data-stu-id="47347-104">SYNTAX</span></span>

### <span data-ttu-id="47347-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="47347-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47347-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="47347-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47347-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="47347-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47347-108">說明</span><span class="sxs-lookup"><span data-stu-id="47347-108">DESCRIPTION</span></span>
<span data-ttu-id="47347-109">**Undo AzKeyVaultKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="47347-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="47347-110">復原的金鑰將是作用中的，而且可用於所有正常按鍵作業。</span><span class="sxs-lookup"><span data-stu-id="47347-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="47347-111">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="47347-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="47347-112">示例</span><span class="sxs-lookup"><span data-stu-id="47347-112">EXAMPLES</span></span>

### <span data-ttu-id="47347-113">範例1</span><span class="sxs-lookup"><span data-stu-id="47347-113">Example 1</span></span>
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

<span data-ttu-id="47347-114">這個命令會將先前刪除的金鑰 ' MyKey ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="47347-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="47347-115">參數</span><span class="sxs-lookup"><span data-stu-id="47347-115">PARAMETERS</span></span>

### <span data-ttu-id="47347-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47347-116">-DefaultProfile</span></span>
<span data-ttu-id="47347-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="47347-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47347-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="47347-118">-HsmName</span></span>
<span data-ttu-id="47347-119">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="47347-119">HSM name.</span></span> <span data-ttu-id="47347-120">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="47347-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="47347-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47347-121">-InputObject</span></span>
<span data-ttu-id="47347-122">已刪除的主要物件</span><span class="sxs-lookup"><span data-stu-id="47347-122">Deleted key object</span></span>

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

### <span data-ttu-id="47347-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="47347-123">-Name</span></span>
<span data-ttu-id="47347-124">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="47347-124">Key name.</span></span>
<span data-ttu-id="47347-125">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="47347-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="47347-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="47347-126">-VaultName</span></span>
<span data-ttu-id="47347-127">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="47347-127">Vault name.</span></span>
<span data-ttu-id="47347-128">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="47347-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="47347-129">-確認</span><span class="sxs-lookup"><span data-stu-id="47347-129">-Confirm</span></span>
<span data-ttu-id="47347-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47347-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47347-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47347-131">-WhatIf</span></span>
<span data-ttu-id="47347-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47347-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47347-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47347-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47347-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47347-134">CommonParameters</span></span>
<span data-ttu-id="47347-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47347-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47347-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47347-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47347-137">輸入</span><span class="sxs-lookup"><span data-stu-id="47347-137">INPUTS</span></span>

### <span data-ttu-id="47347-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="47347-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="47347-139">輸出</span><span class="sxs-lookup"><span data-stu-id="47347-139">OUTPUTS</span></span>

### <span data-ttu-id="47347-140">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="47347-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="47347-141">筆記</span><span class="sxs-lookup"><span data-stu-id="47347-141">NOTES</span></span>

## <span data-ttu-id="47347-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="47347-142">RELATED LINKS</span></span>

[<span data-ttu-id="47347-143">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47347-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="47347-144">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47347-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="47347-145">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47347-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

