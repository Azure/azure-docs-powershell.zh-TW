---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800942"
---
# <span data-ttu-id="bf2cf-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="bf2cf-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="bf2cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="bf2cf-103">將 [金鑰 vault] 中的已刪除金鑰復原為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf2cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf2cf-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf2cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="bf2cf-106">**Undo AzureKeyVaultKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="bf2cf-107">復原的金鑰將是作用中的，而且可用於所有正常按鍵作業。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="bf2cf-108">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="bf2cf-109">示例</span><span class="sxs-lookup"><span data-stu-id="bf2cf-109">EXAMPLES</span></span>

### <span data-ttu-id="bf2cf-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bf2cf-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="bf2cf-111">這個命令會將先前刪除的金鑰 ' MyKey ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="bf2cf-112">參數</span><span class="sxs-lookup"><span data-stu-id="bf2cf-112">PARAMETERS</span></span>

### <span data-ttu-id="bf2cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf2cf-113">-DefaultProfile</span></span>
<span data-ttu-id="bf2cf-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bf2cf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf2cf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf2cf-115">-Name</span></span>
<span data-ttu-id="bf2cf-116">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-116">Key name.</span></span>
<span data-ttu-id="bf2cf-117">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf2cf-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bf2cf-118">-VaultName</span></span>
<span data-ttu-id="bf2cf-119">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-119">Vault name.</span></span>
<span data-ttu-id="bf2cf-120">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf2cf-121">-確認</span><span class="sxs-lookup"><span data-stu-id="bf2cf-121">-Confirm</span></span>
<span data-ttu-id="bf2cf-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf2cf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf2cf-123">-WhatIf</span></span>
<span data-ttu-id="bf2cf-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf2cf-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf2cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf2cf-126">CommonParameters</span></span>
<span data-ttu-id="bf2cf-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf2cf-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf2cf-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bf2cf-129">INPUTS</span></span>

### <span data-ttu-id="bf2cf-130">System.object</span><span class="sxs-lookup"><span data-stu-id="bf2cf-130">System.String</span></span>

## <span data-ttu-id="bf2cf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bf2cf-131">OUTPUTS</span></span>

### <span data-ttu-id="bf2cf-132">KeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="bf2cf-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="bf2cf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bf2cf-133">NOTES</span></span>

## <span data-ttu-id="bf2cf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf2cf-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf2cf-135">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf2cf-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="bf2cf-136">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf2cf-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="bf2cf-137">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf2cf-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

