---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799849"
---
# <span data-ttu-id="76351-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76351-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="76351-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76351-102">SYNOPSIS</span></span>
<span data-ttu-id="76351-103">從備份的機密在金鑰保存庫中建立秘密。</span><span class="sxs-lookup"><span data-stu-id="76351-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76351-104">句法</span><span class="sxs-lookup"><span data-stu-id="76351-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76351-105">說明</span><span class="sxs-lookup"><span data-stu-id="76351-105">DESCRIPTION</span></span>
<span data-ttu-id="76351-106">**Restore-AzureKeyVaultSecret** Cmdlet 會在指定的金鑰保存庫中建立一個秘密。</span><span class="sxs-lookup"><span data-stu-id="76351-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="76351-107">這個秘密是輸入檔案中的備份密碼複本，且與原始密碼的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="76351-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="76351-108">如果主要電子倉庫已有相同名稱的機密，這個 Cmdlet 會失敗，而不會覆寫原始的密碼。</span><span class="sxs-lookup"><span data-stu-id="76351-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="76351-109">如果備份包含多個版本的密碼，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="76351-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="76351-110">您將密碼還原到哪個金鑰保存庫，可能與您在其中備份密碼的金鑰保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="76351-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="76351-111">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="76351-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="76351-112">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="76351-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="76351-113">示例</span><span class="sxs-lookup"><span data-stu-id="76351-113">EXAMPLES</span></span>

### <span data-ttu-id="76351-114">範例1：還原備份的機密</span><span class="sxs-lookup"><span data-stu-id="76351-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="76351-115">這個命令會從名為 MyKeyVault 的金鑰保存庫中，將包含所有版本的備份檔案還原為一個秘密，包括其所有版本。</span><span class="sxs-lookup"><span data-stu-id="76351-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="76351-116">參數</span><span class="sxs-lookup"><span data-stu-id="76351-116">PARAMETERS</span></span>

### <span data-ttu-id="76351-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76351-117">-DefaultProfile</span></span>
<span data-ttu-id="76351-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="76351-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76351-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="76351-119">-InputFile</span></span>
<span data-ttu-id="76351-120">指定包含要還原之密碼備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="76351-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76351-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="76351-121">-VaultName</span></span>
<span data-ttu-id="76351-122">指定要將密碼還原到哪個主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="76351-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="76351-123">-確認</span><span class="sxs-lookup"><span data-stu-id="76351-123">-Confirm</span></span>
<span data-ttu-id="76351-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76351-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76351-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76351-125">-WhatIf</span></span>
<span data-ttu-id="76351-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76351-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76351-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76351-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76351-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76351-128">CommonParameters</span></span>
<span data-ttu-id="76351-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76351-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76351-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76351-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76351-131">輸入</span><span class="sxs-lookup"><span data-stu-id="76351-131">INPUTS</span></span>

## <span data-ttu-id="76351-132">輸出</span><span class="sxs-lookup"><span data-stu-id="76351-132">OUTPUTS</span></span>

### <span data-ttu-id="76351-133">KeyVault （密碼）。</span><span class="sxs-lookup"><span data-stu-id="76351-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="76351-134">筆記</span><span class="sxs-lookup"><span data-stu-id="76351-134">NOTES</span></span>

## <span data-ttu-id="76351-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="76351-135">RELATED LINKS</span></span>

[<span data-ttu-id="76351-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76351-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="76351-137">備份-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76351-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="76351-138">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76351-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="76351-139">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76351-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

