---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 28f4550ac850b7bcc5bab4c90ec510128a8e2ab0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971045"
---
# <span data-ttu-id="38784-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="38784-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="38784-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38784-102">SYNOPSIS</span></span>
<span data-ttu-id="38784-103">備份金鑰保存庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="38784-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="38784-104">句法</span><span class="sxs-lookup"><span data-stu-id="38784-104">SYNTAX</span></span>

### <span data-ttu-id="38784-105">ByKeyName (預設) </span><span class="sxs-lookup"><span data-stu-id="38784-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38784-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="38784-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38784-107">說明</span><span class="sxs-lookup"><span data-stu-id="38784-107">DESCRIPTION</span></span>
<span data-ttu-id="38784-108">**AzKeyVaultKey** Cmdlet 會在金鑰保存庫中備份指定的金鑰，方法是下載並儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="38784-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="38784-109">如果有多個版本的金鑰，所有版本都包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="38784-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="38784-110">因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="38784-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="38784-111">您可以將備份的金鑰還原到其備份之訂閱中的任何重要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="38784-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="38784-112">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="38784-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="38784-113">您想要保管金鑰複本，以便您在金鑰保存庫中不小心刪除金鑰時擁有離線複本。</span><span class="sxs-lookup"><span data-stu-id="38784-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="38784-114">您是使用 [主要電子倉庫] 建立金鑰，現在想要將該金鑰克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。</span><span class="sxs-lookup"><span data-stu-id="38784-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="38784-115">使用 **AzKeyVaultKey** Cmdlet 以加密格式來檢索金鑰，然後使用 Restore-AzKeyVaultKey Cmdlet，並在第二個區域中指定金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="38784-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="38784-116">示例</span><span class="sxs-lookup"><span data-stu-id="38784-116">EXAMPLES</span></span>

### <span data-ttu-id="38784-117">範例1：使用自動產生的檔案名備份金鑰</span><span class="sxs-lookup"><span data-stu-id="38784-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="38784-118">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyKey 的金鑰，並將該金鑰的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="38784-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="38784-119">範例2：將金鑰備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="38784-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="38784-120">這個命令會從 key vaultnamed MyKeyVault 中檢索名為 MyKey 的金鑰，並將該金鑰的備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="38784-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="38784-121">範例3：將先前檢索的金鑰備份到指定的檔案名，不需提示即覆寫目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="38784-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="38784-122">這個命令會建立名為 $key 之金鑰的備份。名為 $key 的保存庫中的名稱。VaultName 到名為 Backup 的檔案，如果檔案已存在，則會以無訊息方式覆蓋該檔案。</span><span class="sxs-lookup"><span data-stu-id="38784-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="38784-123">參數</span><span class="sxs-lookup"><span data-stu-id="38784-123">PARAMETERS</span></span>

### <span data-ttu-id="38784-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38784-124">-DefaultProfile</span></span>
<span data-ttu-id="38784-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="38784-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38784-126">-Force</span><span class="sxs-lookup"><span data-stu-id="38784-126">-Force</span></span>
<span data-ttu-id="38784-127">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="38784-127">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38784-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38784-128">-InputObject</span></span>
<span data-ttu-id="38784-129">要備份的主要捆綁，從檢索呼叫的輸出中流水線。</span><span class="sxs-lookup"><span data-stu-id="38784-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38784-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="38784-130">-Name</span></span>
<span data-ttu-id="38784-131">指定要備份的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="38784-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38784-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="38784-132">-OutputFile</span></span>
<span data-ttu-id="38784-133">指定儲存備份 blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="38784-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="38784-134">如果您沒有指定此參數，這個 Cmdlet 會為您產生檔案名。</span><span class="sxs-lookup"><span data-stu-id="38784-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="38784-135">如果您指定現有輸出檔案的名稱，該作業將無法完成，而且會傳回備份檔案已經存在的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="38784-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="38784-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="38784-136">-VaultName</span></span>
<span data-ttu-id="38784-137">指定包含要備份之金鑰之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="38784-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38784-138">-確認</span><span class="sxs-lookup"><span data-stu-id="38784-138">-Confirm</span></span>
<span data-ttu-id="38784-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38784-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38784-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38784-140">-WhatIf</span></span>
<span data-ttu-id="38784-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38784-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38784-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38784-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38784-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38784-143">CommonParameters</span></span>
<span data-ttu-id="38784-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38784-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38784-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38784-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38784-146">輸入</span><span class="sxs-lookup"><span data-stu-id="38784-146">INPUTS</span></span>

### <span data-ttu-id="38784-147">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="38784-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="38784-148">輸出</span><span class="sxs-lookup"><span data-stu-id="38784-148">OUTPUTS</span></span>

### <span data-ttu-id="38784-149">System.object</span><span class="sxs-lookup"><span data-stu-id="38784-149">System.String</span></span>

## <span data-ttu-id="38784-150">筆記</span><span class="sxs-lookup"><span data-stu-id="38784-150">NOTES</span></span>

## <span data-ttu-id="38784-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="38784-151">RELATED LINKS</span></span>

[<span data-ttu-id="38784-152">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="38784-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="38784-153">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="38784-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="38784-154">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="38784-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="38784-155">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="38784-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

