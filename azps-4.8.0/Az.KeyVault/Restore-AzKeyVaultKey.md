---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127660"
---
# <span data-ttu-id="60e0b-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60e0b-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="60e0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="60e0b-103">從備份金鑰在金鑰保存庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="60e0b-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="60e0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="60e0b-104">SYNTAX</span></span>

### <span data-ttu-id="60e0b-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="60e0b-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60e0b-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="60e0b-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e0b-108">說明</span><span class="sxs-lookup"><span data-stu-id="60e0b-108">DESCRIPTION</span></span>
<span data-ttu-id="60e0b-109">**Restore-AzKeyVaultKey** Cmdlet 會在指定的金鑰保存庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="60e0b-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="60e0b-110">此金鑰是輸入檔案中備份金鑰的複本，且與原始金鑰的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="60e0b-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="60e0b-111">如果主要電子倉庫已有相同名稱的金鑰，這個 Cmdlet 會失敗，而不會覆寫原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="60e0b-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="60e0b-112">如果備份包含多個版本的金鑰，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="60e0b-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="60e0b-113">您還原金鑰的主要電子倉庫，可能會與您備份金鑰的主要保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="60e0b-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="60e0b-114">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="60e0b-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="60e0b-115">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="60e0b-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="60e0b-116">示例</span><span class="sxs-lookup"><span data-stu-id="60e0b-116">EXAMPLES</span></span>

### <span data-ttu-id="60e0b-117">範例1：還原備份金鑰</span><span class="sxs-lookup"><span data-stu-id="60e0b-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="60e0b-118">這個命令會從名為 MyKeyVault 的金鑰保存庫中，將包含其所有版本之備份檔案的金鑰（包括其所有版本）還原。</span><span class="sxs-lookup"><span data-stu-id="60e0b-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="60e0b-119">參數</span><span class="sxs-lookup"><span data-stu-id="60e0b-119">PARAMETERS</span></span>

### <span data-ttu-id="60e0b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e0b-120">-DefaultProfile</span></span>
<span data-ttu-id="60e0b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="60e0b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60e0b-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="60e0b-122">-InputFile</span></span>
<span data-ttu-id="60e0b-123">指定包含要還原之金鑰備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="60e0b-123">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e0b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60e0b-124">-InputObject</span></span>
<span data-ttu-id="60e0b-125">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="60e0b-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60e0b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60e0b-126">-ResourceId</span></span>
<span data-ttu-id="60e0b-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="60e0b-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e0b-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="60e0b-128">-VaultName</span></span>
<span data-ttu-id="60e0b-129">指定要還原金鑰的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="60e0b-129">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e0b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="60e0b-130">-Confirm</span></span>
<span data-ttu-id="60e0b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60e0b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e0b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e0b-132">-WhatIf</span></span>
<span data-ttu-id="60e0b-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60e0b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e0b-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60e0b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e0b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e0b-135">CommonParameters</span></span>
<span data-ttu-id="60e0b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60e0b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e0b-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60e0b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e0b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="60e0b-138">INPUTS</span></span>

### <span data-ttu-id="60e0b-139">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="60e0b-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="60e0b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="60e0b-140">System.String</span></span>

## <span data-ttu-id="60e0b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="60e0b-141">OUTPUTS</span></span>

### <span data-ttu-id="60e0b-142">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="60e0b-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="60e0b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="60e0b-143">NOTES</span></span>

## <span data-ttu-id="60e0b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="60e0b-144">RELATED LINKS</span></span>

[<span data-ttu-id="60e0b-145">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60e0b-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="60e0b-146">備份-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60e0b-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="60e0b-147">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60e0b-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="60e0b-148">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60e0b-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

