---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795541"
---
# <span data-ttu-id="62f7f-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="62f7f-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="62f7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="62f7f-103">從備份的機密在金鑰保存庫中建立秘密。</span><span class="sxs-lookup"><span data-stu-id="62f7f-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="62f7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="62f7f-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62f7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="62f7f-105">DESCRIPTION</span></span>
<span data-ttu-id="62f7f-106">**Restore-AzKeyVaultSecret** Cmdlet 會在指定的金鑰保存庫中建立一個秘密。</span><span class="sxs-lookup"><span data-stu-id="62f7f-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="62f7f-107">這個秘密是輸入檔案中的備份密碼複本，且與原始密碼的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="62f7f-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="62f7f-108">如果主要電子倉庫已有相同名稱的機密，這個 Cmdlet 會失敗，而不會覆寫原始的密碼。</span><span class="sxs-lookup"><span data-stu-id="62f7f-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="62f7f-109">如果備份包含多個版本的密碼，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="62f7f-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="62f7f-110">您將密碼還原到哪個金鑰保存庫，可能與您在其中備份密碼的金鑰保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="62f7f-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="62f7f-111">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="62f7f-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="62f7f-112">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="62f7f-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="62f7f-113">示例</span><span class="sxs-lookup"><span data-stu-id="62f7f-113">EXAMPLES</span></span>

### <span data-ttu-id="62f7f-114">範例1：還原備份的機密</span><span class="sxs-lookup"><span data-stu-id="62f7f-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="62f7f-115">這個命令會從名為 MyKeyVault 的金鑰保存庫中，將包含所有版本的備份檔案還原為一個秘密，包括其所有版本。</span><span class="sxs-lookup"><span data-stu-id="62f7f-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="62f7f-116">參數</span><span class="sxs-lookup"><span data-stu-id="62f7f-116">PARAMETERS</span></span>

### <span data-ttu-id="62f7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f7f-117">-DefaultProfile</span></span>
<span data-ttu-id="62f7f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="62f7f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f7f-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="62f7f-119">-InputFile</span></span>
<span data-ttu-id="62f7f-120">指定包含要還原之密碼備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="62f7f-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="62f7f-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="62f7f-121">-VaultName</span></span>
<span data-ttu-id="62f7f-122">指定要將密碼還原到哪個主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="62f7f-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="62f7f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="62f7f-123">-Confirm</span></span>
<span data-ttu-id="62f7f-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62f7f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62f7f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f7f-125">-WhatIf</span></span>
<span data-ttu-id="62f7f-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62f7f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f7f-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62f7f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62f7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f7f-128">CommonParameters</span></span>
<span data-ttu-id="62f7f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62f7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f7f-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62f7f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f7f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="62f7f-131">INPUTS</span></span>

### <span data-ttu-id="62f7f-132">所有</span><span class="sxs-lookup"><span data-stu-id="62f7f-132">None</span></span>
<span data-ttu-id="62f7f-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="62f7f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62f7f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="62f7f-134">OUTPUTS</span></span>

### <span data-ttu-id="62f7f-135">KeyVault （密碼）。</span><span class="sxs-lookup"><span data-stu-id="62f7f-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="62f7f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="62f7f-136">NOTES</span></span>

## <span data-ttu-id="62f7f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="62f7f-137">RELATED LINKS</span></span>

[<span data-ttu-id="62f7f-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="62f7f-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="62f7f-139">備份-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="62f7f-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="62f7f-140">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="62f7f-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="62f7f-141">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="62f7f-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

