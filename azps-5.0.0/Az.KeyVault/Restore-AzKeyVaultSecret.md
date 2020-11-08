---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136728"
---
# <span data-ttu-id="003e1-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="003e1-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="003e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="003e1-102">SYNOPSIS</span></span>
<span data-ttu-id="003e1-103">從備份的機密在金鑰保存庫中建立秘密。</span><span class="sxs-lookup"><span data-stu-id="003e1-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="003e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="003e1-104">SYNTAX</span></span>

### <span data-ttu-id="003e1-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="003e1-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="003e1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="003e1-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="003e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="003e1-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003e1-108">說明</span><span class="sxs-lookup"><span data-stu-id="003e1-108">DESCRIPTION</span></span>
<span data-ttu-id="003e1-109">**Restore-AzKeyVaultSecret** Cmdlet 會在指定的金鑰保存庫中建立一個秘密。</span><span class="sxs-lookup"><span data-stu-id="003e1-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="003e1-110">這個秘密是輸入檔案中的備份密碼複本，且與原始密碼的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="003e1-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="003e1-111">如果主要電子倉庫已有相同名稱的機密，這個 Cmdlet 會失敗，而不會覆寫原始的密碼。</span><span class="sxs-lookup"><span data-stu-id="003e1-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="003e1-112">如果備份包含多個版本的密碼，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="003e1-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="003e1-113">您將密碼還原到哪個金鑰保存庫，可能與您在其中備份密碼的金鑰保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="003e1-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="003e1-114">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="003e1-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="003e1-115">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="003e1-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="003e1-116">示例</span><span class="sxs-lookup"><span data-stu-id="003e1-116">EXAMPLES</span></span>

### <span data-ttu-id="003e1-117">範例1：還原備份的機密</span><span class="sxs-lookup"><span data-stu-id="003e1-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="003e1-118">這個命令會從名為 [contoso] 的金鑰保存庫中，將包含其所有版本的備份檔案還原為一個秘密，包括其所有版本。</span><span class="sxs-lookup"><span data-stu-id="003e1-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="003e1-119">參數</span><span class="sxs-lookup"><span data-stu-id="003e1-119">PARAMETERS</span></span>

### <span data-ttu-id="003e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003e1-120">-DefaultProfile</span></span>
<span data-ttu-id="003e1-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="003e1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="003e1-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="003e1-122">-InputFile</span></span>
<span data-ttu-id="003e1-123">指定包含要還原之密碼備份的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="003e1-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="003e1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="003e1-124">-InputObject</span></span>
<span data-ttu-id="003e1-125">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="003e1-125">KeyVault object</span></span>

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

### <span data-ttu-id="003e1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="003e1-126">-ResourceId</span></span>
<span data-ttu-id="003e1-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="003e1-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="003e1-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="003e1-128">-VaultName</span></span>
<span data-ttu-id="003e1-129">指定要將密碼還原到哪個主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="003e1-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="003e1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="003e1-130">-Confirm</span></span>
<span data-ttu-id="003e1-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="003e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003e1-132">-WhatIf</span></span>
<span data-ttu-id="003e1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="003e1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003e1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="003e1-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003e1-135">CommonParameters</span></span>
<span data-ttu-id="003e1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="003e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003e1-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="003e1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003e1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="003e1-138">INPUTS</span></span>

### <span data-ttu-id="003e1-139">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="003e1-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="003e1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="003e1-140">System.String</span></span>

## <span data-ttu-id="003e1-141">輸出</span><span class="sxs-lookup"><span data-stu-id="003e1-141">OUTPUTS</span></span>

### <span data-ttu-id="003e1-142">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="003e1-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="003e1-143">筆記</span><span class="sxs-lookup"><span data-stu-id="003e1-143">NOTES</span></span>

## <span data-ttu-id="003e1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="003e1-144">RELATED LINKS</span></span>

[<span data-ttu-id="003e1-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="003e1-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="003e1-146">備份-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="003e1-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="003e1-147">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="003e1-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="003e1-148">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="003e1-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

