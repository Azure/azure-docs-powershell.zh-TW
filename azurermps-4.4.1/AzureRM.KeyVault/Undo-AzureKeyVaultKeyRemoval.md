---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455736"
---
# <span data-ttu-id="5a920-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="5a920-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="5a920-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a920-102">SYNOPSIS</span></span>
<span data-ttu-id="5a920-103">將 [金鑰 vault] 中的已刪除金鑰復原為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="5a920-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a920-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a920-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a920-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a920-105">DESCRIPTION</span></span>
<span data-ttu-id="5a920-106">**Undo AzureKeyVaultKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="5a920-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="5a920-107">復原的金鑰將是作用中的，而且可用於所有正常按鍵作業。</span><span class="sxs-lookup"><span data-stu-id="5a920-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="5a920-108">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="5a920-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="5a920-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a920-109">EXAMPLES</span></span>

### <span data-ttu-id="5a920-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5a920-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="5a920-111">這個命令會將先前刪除的金鑰 ' MyKey ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a920-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="5a920-112">參數</span><span class="sxs-lookup"><span data-stu-id="5a920-112">PARAMETERS</span></span>

### <span data-ttu-id="5a920-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a920-113">-Name</span></span>
<span data-ttu-id="5a920-114">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="5a920-114">Key name.</span></span>
<span data-ttu-id="5a920-115">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5a920-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a920-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a920-116">-VaultName</span></span>
<span data-ttu-id="5a920-117">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5a920-117">Vault name.</span></span>
<span data-ttu-id="5a920-118">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5a920-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a920-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5a920-119">-Confirm</span></span>
<span data-ttu-id="5a920-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a920-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a920-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a920-121">-WhatIf</span></span>
<span data-ttu-id="5a920-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a920-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a920-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a920-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a920-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a920-124">-DefaultProfile</span></span>
<span data-ttu-id="5a920-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a920-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a920-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a920-126">CommonParameters</span></span>
<span data-ttu-id="5a920-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a920-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a920-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a920-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a920-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5a920-129">INPUTS</span></span>

### <span data-ttu-id="5a920-130">System.object</span><span class="sxs-lookup"><span data-stu-id="5a920-130">System.String</span></span>

## <span data-ttu-id="5a920-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5a920-131">OUTPUTS</span></span>

### <span data-ttu-id="5a920-132">KeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="5a920-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="5a920-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5a920-133">NOTES</span></span>

## <span data-ttu-id="5a920-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a920-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a920-135">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a920-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="5a920-136">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a920-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="5a920-137">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a920-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

