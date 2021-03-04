---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 56f5279b1d3645717a29e392fd45599344515a29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908530"
---
# <span data-ttu-id="13d55-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="13d55-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="13d55-102">簡介</span><span class="sxs-lookup"><span data-stu-id="13d55-102">SYNOPSIS</span></span>
<span data-ttu-id="13d55-103">從備份的機密建立金鑰庫中的機密。</span><span class="sxs-lookup"><span data-stu-id="13d55-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="13d55-104">語法</span><span class="sxs-lookup"><span data-stu-id="13d55-104">SYNTAX</span></span>

### <span data-ttu-id="13d55-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="13d55-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d55-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13d55-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d55-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13d55-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13d55-108">描述</span><span class="sxs-lookup"><span data-stu-id="13d55-108">DESCRIPTION</span></span>
<span data-ttu-id="13d55-109">**Restore-AzKeyVaultSecret** Cmdlet 會建立指定金鑰庫中的機密。</span><span class="sxs-lookup"><span data-stu-id="13d55-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="13d55-110">此秘訣是輸入檔案中備份機密的複本，其名稱與原始密碼相同。</span><span class="sxs-lookup"><span data-stu-id="13d55-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="13d55-111">如果金鑰庫已經有相同名稱的機密，此 Cmdlet 會失敗，而不會覆寫原始的機密。</span><span class="sxs-lookup"><span data-stu-id="13d55-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="13d55-112">如果備份包含多個版本的機密，所有版本會還原。</span><span class="sxs-lookup"><span data-stu-id="13d55-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="13d55-113">您還原機密的金鑰庫可能會與備份該機密的金鑰庫不同。</span><span class="sxs-lookup"><span data-stu-id="13d55-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="13d55-114">不過，金鑰庫必須使用相同的訂閱，而且位於位於相同地理位置的 Azure (例如北美地區) 。</span><span class="sxs-lookup"><span data-stu-id="13d55-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="13d55-115">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) Azure 區域與地理位置的相互比對。</span><span class="sxs-lookup"><span data-stu-id="13d55-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="13d55-116">例子</span><span class="sxs-lookup"><span data-stu-id="13d55-116">EXAMPLES</span></span>

### <span data-ttu-id="13d55-117">範例 1：還原備份機密</span><span class="sxs-lookup"><span data-stu-id="13d55-117">Example 1: Restore a backed-up secret</span></span>
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

<span data-ttu-id="13d55-118">此命令會從名為 Backup.blob 的備份檔案還原為名為 contoso 的金鑰保存庫，包括其所有版本。</span><span class="sxs-lookup"><span data-stu-id="13d55-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="13d55-119">參數</span><span class="sxs-lookup"><span data-stu-id="13d55-119">PARAMETERS</span></span>

### <span data-ttu-id="13d55-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d55-120">-DefaultProfile</span></span>
<span data-ttu-id="13d55-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="13d55-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13d55-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="13d55-122">-InputFile</span></span>
<span data-ttu-id="13d55-123">指定包含要還原之機密備份的輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="13d55-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="13d55-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13d55-124">-InputObject</span></span>
<span data-ttu-id="13d55-125">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="13d55-125">KeyVault object</span></span>

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

### <span data-ttu-id="13d55-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d55-126">-ResourceId</span></span>
<span data-ttu-id="13d55-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13d55-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="13d55-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="13d55-128">-VaultName</span></span>
<span data-ttu-id="13d55-129">指定要還原機密的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="13d55-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="13d55-130">-確認</span><span class="sxs-lookup"><span data-stu-id="13d55-130">-Confirm</span></span>
<span data-ttu-id="13d55-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="13d55-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13d55-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d55-132">-WhatIf</span></span>
<span data-ttu-id="13d55-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13d55-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13d55-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13d55-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13d55-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d55-135">CommonParameters</span></span>
<span data-ttu-id="13d55-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="13d55-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d55-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13d55-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d55-138">輸入</span><span class="sxs-lookup"><span data-stu-id="13d55-138">INPUTS</span></span>

### <span data-ttu-id="13d55-139">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="13d55-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="13d55-140">System.String</span><span class="sxs-lookup"><span data-stu-id="13d55-140">System.String</span></span>

## <span data-ttu-id="13d55-141">輸出</span><span class="sxs-lookup"><span data-stu-id="13d55-141">OUTPUTS</span></span>

### <span data-ttu-id="13d55-142">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="13d55-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="13d55-143">筆記</span><span class="sxs-lookup"><span data-stu-id="13d55-143">NOTES</span></span>

## <span data-ttu-id="13d55-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="13d55-144">RELATED LINKS</span></span>

[<span data-ttu-id="13d55-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="13d55-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="13d55-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="13d55-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="13d55-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="13d55-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="13d55-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="13d55-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

