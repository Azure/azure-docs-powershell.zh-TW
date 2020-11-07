---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795544"
---
# <span data-ttu-id="f21f7-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f21f7-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="f21f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f21f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f21f7-103">從備份金鑰在金鑰保存庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="f21f7-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="f21f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="f21f7-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f21f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="f21f7-105">DESCRIPTION</span></span>
<span data-ttu-id="f21f7-106">**Restore-AzKeyVaultKey** Cmdlet 會在指定的金鑰保存庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="f21f7-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="f21f7-107">此金鑰是輸入檔案中備份金鑰的複本，且與原始金鑰的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="f21f7-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="f21f7-108">如果主要電子倉庫已有相同名稱的金鑰，這個 Cmdlet 會失敗，而不會覆寫原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="f21f7-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="f21f7-109">如果備份包含多個版本的金鑰，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="f21f7-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="f21f7-110">您還原金鑰的主要電子倉庫，可能會與您備份金鑰的主要保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="f21f7-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="f21f7-111">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="f21f7-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="f21f7-112">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="f21f7-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="f21f7-113">示例</span><span class="sxs-lookup"><span data-stu-id="f21f7-113">EXAMPLES</span></span>

### <span data-ttu-id="f21f7-114">範例1：還原備份金鑰</span><span class="sxs-lookup"><span data-stu-id="f21f7-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="f21f7-115">這個命令會從名為 MyKeyVault 的金鑰保存庫中，將包含其所有版本之備份檔案的金鑰（包括其所有版本）還原。</span><span class="sxs-lookup"><span data-stu-id="f21f7-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="f21f7-116">參數</span><span class="sxs-lookup"><span data-stu-id="f21f7-116">PARAMETERS</span></span>

### <span data-ttu-id="f21f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21f7-117">-DefaultProfile</span></span>
<span data-ttu-id="f21f7-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f21f7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f21f7-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f21f7-119">-InputFile</span></span>
<span data-ttu-id="f21f7-120">指定包含要還原之金鑰備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="f21f7-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="f21f7-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f21f7-121">-VaultName</span></span>
<span data-ttu-id="f21f7-122">指定要還原金鑰的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f21f7-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="f21f7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f21f7-123">-Confirm</span></span>
<span data-ttu-id="f21f7-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f21f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f21f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f21f7-125">-WhatIf</span></span>
<span data-ttu-id="f21f7-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f21f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f21f7-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f21f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f21f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21f7-128">CommonParameters</span></span>
<span data-ttu-id="f21f7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f21f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21f7-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f21f7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21f7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f21f7-131">INPUTS</span></span>

### <span data-ttu-id="f21f7-132">所有</span><span class="sxs-lookup"><span data-stu-id="f21f7-132">None</span></span>
<span data-ttu-id="f21f7-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f21f7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f21f7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f21f7-134">OUTPUTS</span></span>

### <span data-ttu-id="f21f7-135">KeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f21f7-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="f21f7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f21f7-136">NOTES</span></span>

## <span data-ttu-id="f21f7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f21f7-137">RELATED LINKS</span></span>

[<span data-ttu-id="f21f7-138">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f21f7-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="f21f7-139">備份-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f21f7-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="f21f7-140">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f21f7-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="f21f7-141">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f21f7-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

