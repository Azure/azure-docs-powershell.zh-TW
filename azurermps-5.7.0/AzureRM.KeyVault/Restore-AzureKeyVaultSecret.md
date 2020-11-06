---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450588"
---
# <span data-ttu-id="b7ef1-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7ef1-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="b7ef1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ef1-103">從備份的機密在金鑰保存庫中建立秘密。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7ef1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7ef1-104">SYNTAX</span></span>

### <span data-ttu-id="b7ef1-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="b7ef1-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ef1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7ef1-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ef1-107">說明</span><span class="sxs-lookup"><span data-stu-id="b7ef1-107">DESCRIPTION</span></span>
<span data-ttu-id="b7ef1-108">**Restore-AzureKeyVaultSecret** Cmdlet 會在指定的金鑰保存庫中建立一個秘密。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="b7ef1-109">這個秘密是輸入檔案中的備份密碼複本，且與原始密碼的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="b7ef1-110">如果主要電子倉庫已有相同名稱的機密，這個 Cmdlet 會失敗，而不會覆寫原始的密碼。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="b7ef1-111">如果備份包含多個版本的密碼，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="b7ef1-112">您將密碼還原到哪個金鑰保存庫，可能與您在其中備份密碼的金鑰保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="b7ef1-113">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b7ef1-114">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b7ef1-115">示例</span><span class="sxs-lookup"><span data-stu-id="b7ef1-115">EXAMPLES</span></span>

### <span data-ttu-id="b7ef1-116">範例1：還原備份的機密</span><span class="sxs-lookup"><span data-stu-id="b7ef1-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="b7ef1-117">這個命令會從名為 MyKeyVault 的金鑰保存庫中，將包含所有版本的備份檔案還原為一個秘密，包括其所有版本。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="b7ef1-118">參數</span><span class="sxs-lookup"><span data-stu-id="b7ef1-118">PARAMETERS</span></span>

### <span data-ttu-id="b7ef1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ef1-119">-DefaultProfile</span></span>
<span data-ttu-id="b7ef1-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b7ef1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7ef1-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b7ef1-121">-InputFile</span></span>
<span data-ttu-id="b7ef1-122">指定包含要還原之密碼備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="b7ef1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ef1-123">-InputObject</span></span>
<span data-ttu-id="b7ef1-124">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="b7ef1-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ef1-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b7ef1-125">-VaultName</span></span>
<span data-ttu-id="b7ef1-126">指定要將密碼還原到哪個主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ef1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b7ef1-127">-Confirm</span></span>
<span data-ttu-id="b7ef1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ef1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ef1-129">-WhatIf</span></span>
<span data-ttu-id="b7ef1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ef1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ef1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ef1-132">CommonParameters</span></span>
<span data-ttu-id="b7ef1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ef1-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ef1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b7ef1-135">INPUTS</span></span>

### <span data-ttu-id="b7ef1-136">所有</span><span class="sxs-lookup"><span data-stu-id="b7ef1-136">None</span></span>
<span data-ttu-id="b7ef1-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7ef1-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b7ef1-138">OUTPUTS</span></span>

### <span data-ttu-id="b7ef1-139">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b7ef1-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b7ef1-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b7ef1-140">NOTES</span></span>

## <span data-ttu-id="b7ef1-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7ef1-141">RELATED LINKS</span></span>

[<span data-ttu-id="b7ef1-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7ef1-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="b7ef1-143">備份-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7ef1-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="b7ef1-144">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7ef1-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="b7ef1-145">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7ef1-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

