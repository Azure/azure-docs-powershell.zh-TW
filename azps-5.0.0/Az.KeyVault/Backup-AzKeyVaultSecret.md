---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136767"
---
# <span data-ttu-id="5a867-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a867-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="5a867-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a867-102">SYNOPSIS</span></span>
<span data-ttu-id="5a867-103">在金鑰保存庫中備份密碼。</span><span class="sxs-lookup"><span data-stu-id="5a867-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="5a867-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a867-104">SYNTAX</span></span>

### <span data-ttu-id="5a867-105">BySecretName (預設) </span><span class="sxs-lookup"><span data-stu-id="5a867-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a867-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="5a867-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a867-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a867-107">DESCRIPTION</span></span>
<span data-ttu-id="5a867-108">**AzKeyVaultSecret** Cmdlet 會透過下載並儲存在一個檔案中，以在金鑰儲存庫中備份指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="5a867-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="5a867-109">如果有多個版本的密碼，所有版本都包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="5a867-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="5a867-110">因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="5a867-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="5a867-111">您可以將備份的密碼還原到其備份之訂閱中的任何重要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="5a867-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="5a867-112">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="5a867-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="5a867-113">您想要保管您的機密複本，以便您在金鑰保存庫中不小心刪除您的機密時擁有離線複本。</span><span class="sxs-lookup"><span data-stu-id="5a867-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="5a867-114">您已將密碼新增到金鑰保存庫，現在想要將該秘密克隆至不同的 Azure 區域，以便您可以從分散式應用程式的所有實例中使用。</span><span class="sxs-lookup"><span data-stu-id="5a867-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="5a867-115">使用 Backup-AzKeyVaultSecret Cmdlet 以加密格式來檢索機密，然後使用 Restore-AzKeyVaultSecret Cmdlet，並在第二個區域中指定金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="5a867-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="5a867-116"> (請注意，地區必須屬於相同的地理位置。 ) </span><span class="sxs-lookup"><span data-stu-id="5a867-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="5a867-117">示例</span><span class="sxs-lookup"><span data-stu-id="5a867-117">EXAMPLES</span></span>

### <span data-ttu-id="5a867-118">範例1：使用自動產生的檔案名備份密碼</span><span class="sxs-lookup"><span data-stu-id="5a867-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="5a867-119">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MySecret 的密碼，並將該密碼的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="5a867-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="5a867-120">範例2：將機密備份到指定的檔案名，覆寫現有檔案而不提示</span><span class="sxs-lookup"><span data-stu-id="5a867-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="5a867-121">這個命令會從 [金鑰 vaultnamed MyKeyVault] 中檢索名為 MySecret 的密碼，並將該密碼的備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="5a867-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="5a867-122">範例3：備份先前檢索到指定檔案名的密碼</span><span class="sxs-lookup"><span data-stu-id="5a867-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="5a867-123">這個命令會使用 $secret 物件的電子倉庫名稱和名稱來檢索機密，並將其備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="5a867-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="5a867-124">參數</span><span class="sxs-lookup"><span data-stu-id="5a867-124">PARAMETERS</span></span>

### <span data-ttu-id="5a867-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a867-125">-DefaultProfile</span></span>
<span data-ttu-id="5a867-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5a867-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a867-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5a867-127">-Force</span></span>
<span data-ttu-id="5a867-128">會在您覆寫輸出檔案（如果有的話）時提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a867-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

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

### <span data-ttu-id="5a867-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a867-129">-InputObject</span></span>
<span data-ttu-id="5a867-130">要備份的機密，從檢索呼叫的輸出中流水線。</span><span class="sxs-lookup"><span data-stu-id="5a867-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="5a867-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a867-131">-Name</span></span>
<span data-ttu-id="5a867-132">指定要備份之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a867-132">Specifies the name of the secret to back up.</span></span>

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

### <span data-ttu-id="5a867-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5a867-133">-OutputFile</span></span>
<span data-ttu-id="5a867-134">指定儲存備份 blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="5a867-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="5a867-135">如果您沒有指定此參數，這個 Cmdlet 會為您產生檔案名。</span><span class="sxs-lookup"><span data-stu-id="5a867-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="5a867-136">如果您指定現有輸出檔案的名稱，該作業將無法完成，而且會傳回備份檔案已經存在的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5a867-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="5a867-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a867-137">-VaultName</span></span>
<span data-ttu-id="5a867-138">指定包含要備份之密碼之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a867-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

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

### <span data-ttu-id="5a867-139">-確認</span><span class="sxs-lookup"><span data-stu-id="5a867-139">-Confirm</span></span>
<span data-ttu-id="5a867-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a867-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a867-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a867-141">-WhatIf</span></span>
<span data-ttu-id="5a867-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a867-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a867-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a867-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a867-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a867-144">CommonParameters</span></span>
<span data-ttu-id="5a867-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a867-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a867-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a867-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a867-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5a867-147">INPUTS</span></span>

### <span data-ttu-id="5a867-148">PSKeyVaultSecretIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="5a867-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="5a867-149">輸出</span><span class="sxs-lookup"><span data-stu-id="5a867-149">OUTPUTS</span></span>

### <span data-ttu-id="5a867-150">System.object</span><span class="sxs-lookup"><span data-stu-id="5a867-150">System.String</span></span>

## <span data-ttu-id="5a867-151">筆記</span><span class="sxs-lookup"><span data-stu-id="5a867-151">NOTES</span></span>

## <span data-ttu-id="5a867-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a867-152">RELATED LINKS</span></span>

[<span data-ttu-id="5a867-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a867-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="5a867-154">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a867-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="5a867-155">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a867-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="5a867-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a867-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

