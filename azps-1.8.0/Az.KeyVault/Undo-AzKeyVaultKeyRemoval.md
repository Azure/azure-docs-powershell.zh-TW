---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: ff4682a7c97f721dac9fb53f375c2a96f4bb33b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787274"
---
# <span data-ttu-id="f67cf-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f67cf-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="f67cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f67cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f67cf-103">將 [金鑰 vault] 中的已刪除金鑰復原為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="f67cf-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="f67cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="f67cf-104">SYNTAX</span></span>

### <span data-ttu-id="f67cf-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f67cf-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f67cf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f67cf-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f67cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="f67cf-107">DESCRIPTION</span></span>
<span data-ttu-id="f67cf-108">**Undo AzKeyVaultKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f67cf-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="f67cf-109">復原的金鑰將是作用中的，而且可用於所有正常按鍵作業。</span><span class="sxs-lookup"><span data-stu-id="f67cf-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="f67cf-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="f67cf-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f67cf-111">示例</span><span class="sxs-lookup"><span data-stu-id="f67cf-111">EXAMPLES</span></span>

### <span data-ttu-id="f67cf-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f67cf-112">Example 1</span></span>
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

<span data-ttu-id="f67cf-113">這個命令會將先前刪除的金鑰 ' MyKey ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="f67cf-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f67cf-114">參數</span><span class="sxs-lookup"><span data-stu-id="f67cf-114">PARAMETERS</span></span>

### <span data-ttu-id="f67cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67cf-115">-DefaultProfile</span></span>
<span data-ttu-id="f67cf-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f67cf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f67cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f67cf-117">-InputObject</span></span>
<span data-ttu-id="f67cf-118">已刪除的主要物件</span><span class="sxs-lookup"><span data-stu-id="f67cf-118">Deleted key object</span></span>

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

### <span data-ttu-id="f67cf-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f67cf-119">-Name</span></span>
<span data-ttu-id="f67cf-120">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="f67cf-120">Key name.</span></span>
<span data-ttu-id="f67cf-121">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f67cf-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f67cf-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f67cf-122">-VaultName</span></span>
<span data-ttu-id="f67cf-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f67cf-123">Vault name.</span></span>
<span data-ttu-id="f67cf-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f67cf-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f67cf-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f67cf-125">-Confirm</span></span>
<span data-ttu-id="f67cf-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f67cf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f67cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f67cf-127">-WhatIf</span></span>
<span data-ttu-id="f67cf-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f67cf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f67cf-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f67cf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f67cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67cf-130">CommonParameters</span></span>
<span data-ttu-id="f67cf-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f67cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67cf-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f67cf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67cf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f67cf-133">INPUTS</span></span>

### <span data-ttu-id="f67cf-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f67cf-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="f67cf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f67cf-135">OUTPUTS</span></span>

### <span data-ttu-id="f67cf-136">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f67cf-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f67cf-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f67cf-137">NOTES</span></span>

## <span data-ttu-id="f67cf-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f67cf-138">RELATED LINKS</span></span>

[<span data-ttu-id="f67cf-139">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f67cf-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="f67cf-140">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f67cf-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="f67cf-141">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f67cf-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

