---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904425"
---
# <span data-ttu-id="7acae-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7acae-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="7acae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7acae-102">SYNOPSIS</span></span>
<span data-ttu-id="7acae-103">備份金鑰庫中的機密。</span><span class="sxs-lookup"><span data-stu-id="7acae-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="7acae-104">語法</span><span class="sxs-lookup"><span data-stu-id="7acae-104">SYNTAX</span></span>

### <span data-ttu-id="7acae-105">BySecretName (預設) </span><span class="sxs-lookup"><span data-stu-id="7acae-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7acae-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="7acae-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7acae-107">描述</span><span class="sxs-lookup"><span data-stu-id="7acae-107">DESCRIPTION</span></span>
<span data-ttu-id="7acae-108">**Backup-AzKeyVaultSecret** Cmdlet 可下載並儲存于檔案中，以備份金鑰保存庫中的指定機密。</span><span class="sxs-lookup"><span data-stu-id="7acae-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="7acae-109">如果有多個版本的金鑰，所有版本會包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="7acae-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="7acae-110">由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="7acae-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="7acae-111">您可以將備份的機密還原到訂閱中任何備份的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="7acae-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="7acae-112">使用此 Cmdlet 的一般原因如下：</span><span class="sxs-lookup"><span data-stu-id="7acae-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="7acae-113">您想要代管您金鑰的一份副本，這樣一來，萬一您不小心在金鑰保存庫中刪除您的密碼，就擁有一份離線副本。</span><span class="sxs-lookup"><span data-stu-id="7acae-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="7acae-114">您新增了金鑰庫的機密，而現在想要將金鑰複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用它。</span><span class="sxs-lookup"><span data-stu-id="7acae-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="7acae-115">使用 Backup-AzKeyVaultSecret Cmdlet 以加密格式來取回密碼，然後使用 Restore-AzKeyVaultSecret Cmdlet，並指定第二個地區的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="7acae-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="7acae-116"> (請注意，區域必須屬於相同的地理位置.) </span><span class="sxs-lookup"><span data-stu-id="7acae-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="7acae-117">例子</span><span class="sxs-lookup"><span data-stu-id="7acae-117">EXAMPLES</span></span>

### <span data-ttu-id="7acae-118">範例 1：使用自動產生的檔案名備份機密</span><span class="sxs-lookup"><span data-stu-id="7acae-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="7acae-119">此命令會從名為 MyKeyVault 的金鑰保存庫中，取取名為 MySecret 的機密，並儲存該機密的備份至自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="7acae-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="7acae-120">範例 2：備份指定檔案名的機密，覆寫現有檔案而不提示</span><span class="sxs-lookup"><span data-stu-id="7acae-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="7acae-121">此命令會從名稱為 MyKeyVault 的金鑰保存庫取取名為 MySecret 的機密，並儲存該機密的備份至名為 Backup.blob 的檔案。</span><span class="sxs-lookup"><span data-stu-id="7acae-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="7acae-122">範例 3：備份先前取至指定檔案名的機密</span><span class="sxs-lookup"><span data-stu-id="7acae-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="7acae-123">此命令會使用$secret保存庫名稱和名稱來取回機密，並儲存其備份到名為 Backup.blob 的檔案。</span><span class="sxs-lookup"><span data-stu-id="7acae-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="7acae-124">參數</span><span class="sxs-lookup"><span data-stu-id="7acae-124">PARAMETERS</span></span>

### <span data-ttu-id="7acae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acae-125">-DefaultProfile</span></span>
<span data-ttu-id="7acae-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7acae-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7acae-127">-強制</span><span class="sxs-lookup"><span data-stu-id="7acae-127">-Force</span></span>
<span data-ttu-id="7acae-128">提示您確認，然後再覆寫輸出檔案 ，如果有。</span><span class="sxs-lookup"><span data-stu-id="7acae-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acae-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7acae-129">-InputObject</span></span>
<span data-ttu-id="7acae-130">要備份的機密，從呼叫的取回輸出中輸入。</span><span class="sxs-lookup"><span data-stu-id="7acae-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7acae-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="7acae-131">-Name</span></span>
<span data-ttu-id="7acae-132">指定要備份的機密名稱。</span><span class="sxs-lookup"><span data-stu-id="7acae-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acae-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7acae-133">-OutputFile</span></span>
<span data-ttu-id="7acae-134">指定儲存備份 Blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="7acae-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="7acae-135">如果您未指定此參數，此 Cmdlet 會產生您的檔案名。</span><span class="sxs-lookup"><span data-stu-id="7acae-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="7acae-136">如果您指定現有輸出檔案的名稱，作業將不會完成，並返回備份檔案已存在的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7acae-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acae-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7acae-137">-VaultName</span></span>
<span data-ttu-id="7acae-138">指定包含要備份之機密之金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7acae-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acae-139">-確認</span><span class="sxs-lookup"><span data-stu-id="7acae-139">-Confirm</span></span>
<span data-ttu-id="7acae-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7acae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7acae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7acae-141">-WhatIf</span></span>
<span data-ttu-id="7acae-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7acae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7acae-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7acae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7acae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acae-144">CommonParameters</span></span>
<span data-ttu-id="7acae-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7acae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acae-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7acae-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acae-147">輸入</span><span class="sxs-lookup"><span data-stu-id="7acae-147">INPUTS</span></span>

### <span data-ttu-id="7acae-148">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7acae-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="7acae-149">輸出</span><span class="sxs-lookup"><span data-stu-id="7acae-149">OUTPUTS</span></span>

### <span data-ttu-id="7acae-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7acae-150">System.String</span></span>

## <span data-ttu-id="7acae-151">筆記</span><span class="sxs-lookup"><span data-stu-id="7acae-151">NOTES</span></span>

## <span data-ttu-id="7acae-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="7acae-152">RELATED LINKS</span></span>

[<span data-ttu-id="7acae-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7acae-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="7acae-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7acae-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="7acae-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7acae-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="7acae-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7acae-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

