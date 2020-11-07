---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624300"
---
# <span data-ttu-id="98ec5-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98ec5-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="98ec5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="98ec5-103">從備份金鑰在金鑰保存庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="98ec5-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98ec5-104">句法</span><span class="sxs-lookup"><span data-stu-id="98ec5-104">SYNTAX</span></span>

### <span data-ttu-id="98ec5-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="98ec5-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ec5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98ec5-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ec5-107">說明</span><span class="sxs-lookup"><span data-stu-id="98ec5-107">DESCRIPTION</span></span>
<span data-ttu-id="98ec5-108">**Restore-AzureKeyVaultKey** Cmdlet 會在指定的金鑰保存庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="98ec5-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="98ec5-109">此金鑰是輸入檔案中備份金鑰的複本，且與原始金鑰的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="98ec5-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="98ec5-110">如果主要電子倉庫已有相同名稱的金鑰，這個 Cmdlet 會失敗，而不會覆寫原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="98ec5-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="98ec5-111">如果備份包含多個版本的金鑰，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="98ec5-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="98ec5-112">您還原金鑰的主要電子倉庫，可能會與您備份金鑰的主要保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="98ec5-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="98ec5-113">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="98ec5-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="98ec5-114">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="98ec5-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="98ec5-115">示例</span><span class="sxs-lookup"><span data-stu-id="98ec5-115">EXAMPLES</span></span>

### <span data-ttu-id="98ec5-116">範例1：還原備份金鑰</span><span class="sxs-lookup"><span data-stu-id="98ec5-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="98ec5-117">這個命令會從名為 MyKeyVault 的金鑰保存庫中，將包含其所有版本之備份檔案的金鑰（包括其所有版本）還原。</span><span class="sxs-lookup"><span data-stu-id="98ec5-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="98ec5-118">參數</span><span class="sxs-lookup"><span data-stu-id="98ec5-118">PARAMETERS</span></span>

### <span data-ttu-id="98ec5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ec5-119">-DefaultProfile</span></span>
<span data-ttu-id="98ec5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="98ec5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98ec5-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="98ec5-121">-InputFile</span></span>
<span data-ttu-id="98ec5-122">指定包含要還原之金鑰備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="98ec5-122">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="98ec5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98ec5-123">-InputObject</span></span>
<span data-ttu-id="98ec5-124">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="98ec5-124">KeyVault object</span></span>

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

### <span data-ttu-id="98ec5-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="98ec5-125">-VaultName</span></span>
<span data-ttu-id="98ec5-126">指定要還原金鑰的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="98ec5-126">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="98ec5-127">-確認</span><span class="sxs-lookup"><span data-stu-id="98ec5-127">-Confirm</span></span>
<span data-ttu-id="98ec5-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98ec5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ec5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ec5-129">-WhatIf</span></span>
<span data-ttu-id="98ec5-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98ec5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ec5-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98ec5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ec5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ec5-132">CommonParameters</span></span>
<span data-ttu-id="98ec5-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98ec5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ec5-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98ec5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ec5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="98ec5-135">INPUTS</span></span>

### <span data-ttu-id="98ec5-136">所有</span><span class="sxs-lookup"><span data-stu-id="98ec5-136">None</span></span>
<span data-ttu-id="98ec5-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="98ec5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98ec5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="98ec5-138">OUTPUTS</span></span>

### <span data-ttu-id="98ec5-139">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="98ec5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="98ec5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="98ec5-140">NOTES</span></span>

## <span data-ttu-id="98ec5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="98ec5-141">RELATED LINKS</span></span>

[<span data-ttu-id="98ec5-142">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98ec5-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="98ec5-143">備份-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98ec5-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="98ec5-144">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98ec5-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="98ec5-145">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98ec5-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

