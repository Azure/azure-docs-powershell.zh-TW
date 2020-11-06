---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446232"
---
# <span data-ttu-id="7e8c8-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="7e8c8-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="7e8c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8c8-103">將 [金鑰 vault] 中的已刪除金鑰復原為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e8c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e8c8-104">SYNTAX</span></span>

### <span data-ttu-id="7e8c8-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="7e8c8-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e8c8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7e8c8-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e8c8-107">說明</span><span class="sxs-lookup"><span data-stu-id="7e8c8-107">DESCRIPTION</span></span>
<span data-ttu-id="7e8c8-108">**Undo AzureKeyVaultKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="7e8c8-109">復原的金鑰將是作用中的，而且可用於所有正常按鍵作業。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="7e8c8-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="7e8c8-111">示例</span><span class="sxs-lookup"><span data-stu-id="7e8c8-111">EXAMPLES</span></span>

### <span data-ttu-id="7e8c8-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7e8c8-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="7e8c8-113">這個命令會將先前刪除的金鑰 ' MyKey ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="7e8c8-114">參數</span><span class="sxs-lookup"><span data-stu-id="7e8c8-114">PARAMETERS</span></span>

### <span data-ttu-id="7e8c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8c8-115">-DefaultProfile</span></span>
<span data-ttu-id="7e8c8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7e8c8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8c8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e8c8-117">-InputObject</span></span>
<span data-ttu-id="7e8c8-118">已刪除的主要物件</span><span class="sxs-lookup"><span data-stu-id="7e8c8-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8c8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e8c8-119">-Name</span></span>
<span data-ttu-id="7e8c8-120">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-120">Key name.</span></span>
<span data-ttu-id="7e8c8-121">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8c8-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7e8c8-122">-VaultName</span></span>
<span data-ttu-id="7e8c8-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-123">Vault name.</span></span>
<span data-ttu-id="7e8c8-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8c8-125">-確認</span><span class="sxs-lookup"><span data-stu-id="7e8c8-125">-Confirm</span></span>
<span data-ttu-id="7e8c8-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8c8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e8c8-127">-WhatIf</span></span>
<span data-ttu-id="7e8c8-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e8c8-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8c8-130">CommonParameters</span></span>
<span data-ttu-id="7e8c8-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8c8-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8c8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7e8c8-133">INPUTS</span></span>

### <span data-ttu-id="7e8c8-134">System.object</span><span class="sxs-lookup"><span data-stu-id="7e8c8-134">System.String</span></span>

## <span data-ttu-id="7e8c8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7e8c8-135">OUTPUTS</span></span>

### <span data-ttu-id="7e8c8-136">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="7e8c8-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="7e8c8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7e8c8-137">NOTES</span></span>

## <span data-ttu-id="7e8c8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e8c8-138">RELATED LINKS</span></span>

[<span data-ttu-id="7e8c8-139">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e8c8-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="7e8c8-140">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e8c8-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="7e8c8-141">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e8c8-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

