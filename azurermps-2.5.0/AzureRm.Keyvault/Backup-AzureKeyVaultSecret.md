---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: cd83d61c64e4111faf7fc6149107e172d0cf0c9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799902"
---
# <span data-ttu-id="2d958-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d958-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="2d958-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d958-102">SYNOPSIS</span></span>
<span data-ttu-id="2d958-103">在金鑰保存庫中備份密碼。</span><span class="sxs-lookup"><span data-stu-id="2d958-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d958-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d958-104">SYNTAX</span></span>

### <span data-ttu-id="2d958-105">BySecretName (預設) </span><span class="sxs-lookup"><span data-stu-id="2d958-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d958-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="2d958-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d958-107">說明</span><span class="sxs-lookup"><span data-stu-id="2d958-107">DESCRIPTION</span></span>
<span data-ttu-id="2d958-108">**AzureKeyVaultSecret** Cmdlet 會透過下載並儲存在一個檔案中，以在金鑰儲存庫中備份指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="2d958-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="2d958-109">如果有多個版本的密碼，所有版本都包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="2d958-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="2d958-110">因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="2d958-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="2d958-111">您可以將備份的密碼還原到其備份之訂閱中的任何重要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="2d958-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="2d958-112">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="2d958-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="2d958-113">您想要保管您的機密複本，以便您在金鑰保存庫中不小心刪除您的機密時擁有離線複本。</span><span class="sxs-lookup"><span data-stu-id="2d958-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="2d958-114">您已將密碼新增到金鑰保存庫，現在想要將該秘密克隆至不同的 Azure 區域，以便您可以從分散式應用程式的所有實例中使用。</span><span class="sxs-lookup"><span data-stu-id="2d958-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="2d958-115">使用 Backup-AzureKeyVaultSecret Cmdlet 以加密格式來檢索機密，然後使用 Restore-AzureKeyVaultSecret Cmdlet，並在第二個區域中指定金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="2d958-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="2d958-116"> (請注意，地區必須屬於相同的地理位置。 ) </span><span class="sxs-lookup"><span data-stu-id="2d958-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="2d958-117">示例</span><span class="sxs-lookup"><span data-stu-id="2d958-117">EXAMPLES</span></span>

### <span data-ttu-id="2d958-118">範例1：使用自動產生的檔案名備份密碼</span><span class="sxs-lookup"><span data-stu-id="2d958-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="2d958-119">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MySecret 的密碼，並將該密碼的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="2d958-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="2d958-120">範例2：將機密備份到指定的檔案名，覆寫現有檔案而不提示</span><span class="sxs-lookup"><span data-stu-id="2d958-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="2d958-121">這個命令會從 [金鑰 vaultnamed MyKeyVault] 中檢索名為 MySecret 的密碼，並將該密碼的備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="2d958-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="2d958-122">範例3：備份先前檢索到指定檔案名的密碼</span><span class="sxs-lookup"><span data-stu-id="2d958-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="2d958-123">這個命令會使用 $secret 物件的電子倉庫名稱和名稱來檢索機密，並將其備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="2d958-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="2d958-124">參數</span><span class="sxs-lookup"><span data-stu-id="2d958-124">PARAMETERS</span></span>

### <span data-ttu-id="2d958-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d958-125">-DefaultProfile</span></span>
<span data-ttu-id="2d958-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2d958-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d958-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2d958-127">-Force</span></span>
<span data-ttu-id="2d958-128">會在您覆寫輸出檔案（如果有的話）時提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d958-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d958-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d958-129">-Name</span></span>
<span data-ttu-id="2d958-130">指定要備份之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d958-130">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d958-131">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="2d958-131">-OutputFile</span></span>
<span data-ttu-id="2d958-132">指定儲存備份 blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="2d958-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="2d958-133">如果您沒有指定此參數，這個 Cmdlet 會為您產生檔案名。</span><span class="sxs-lookup"><span data-stu-id="2d958-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="2d958-134">如果您指定現有輸出檔案的名稱，該作業將無法完成，而且會傳回備份檔案已經存在的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2d958-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d958-135">密碼</span><span class="sxs-lookup"><span data-stu-id="2d958-135">-Secret</span></span>
<span data-ttu-id="2d958-136">指定名稱和保存庫應該用於備份操作的物件。</span><span class="sxs-lookup"><span data-stu-id="2d958-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d958-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2d958-137">-VaultName</span></span>
<span data-ttu-id="2d958-138">指定包含要備份之密碼之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d958-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d958-139">-確認</span><span class="sxs-lookup"><span data-stu-id="2d958-139">-Confirm</span></span>
<span data-ttu-id="2d958-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d958-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d958-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d958-141">-WhatIf</span></span>
<span data-ttu-id="2d958-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d958-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d958-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d958-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d958-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d958-144">CommonParameters</span></span>
<span data-ttu-id="2d958-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d958-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d958-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d958-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d958-147">輸入</span><span class="sxs-lookup"><span data-stu-id="2d958-147">INPUTS</span></span>

## <span data-ttu-id="2d958-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2d958-148">OUTPUTS</span></span>

### <span data-ttu-id="2d958-149">字串</span><span class="sxs-lookup"><span data-stu-id="2d958-149">String</span></span>
<span data-ttu-id="2d958-150">Cmdlet 會傳回包含金鑰備份之輸出檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2d958-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="2d958-151">筆記</span><span class="sxs-lookup"><span data-stu-id="2d958-151">NOTES</span></span>

## <span data-ttu-id="2d958-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d958-152">RELATED LINKS</span></span>

[<span data-ttu-id="2d958-153">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d958-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="2d958-154">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d958-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="2d958-155">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d958-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="2d958-156">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d958-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)
