---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449106"
---
# <span data-ttu-id="8115a-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8115a-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="8115a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8115a-102">SYNOPSIS</span></span>
<span data-ttu-id="8115a-103">備份金鑰保存庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="8115a-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="8115a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8115a-104">SYNTAX</span></span>

### <span data-ttu-id="8115a-105">ByKeyName (預設) </span><span class="sxs-lookup"><span data-stu-id="8115a-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8115a-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="8115a-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8115a-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="8115a-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8115a-108">說明</span><span class="sxs-lookup"><span data-stu-id="8115a-108">DESCRIPTION</span></span>
<span data-ttu-id="8115a-109">**AzKeyVaultKey** Cmdlet 會在金鑰保存庫中備份指定的金鑰，方法是下載並儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="8115a-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="8115a-110">如果有多個版本的金鑰，所有版本都包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="8115a-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="8115a-111">因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="8115a-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="8115a-112">您可以將備份的金鑰還原到其備份之訂閱中的任何重要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8115a-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="8115a-113">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="8115a-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="8115a-114">您想要保管金鑰複本，以便您在金鑰保存庫中不小心刪除金鑰時擁有離線複本。</span><span class="sxs-lookup"><span data-stu-id="8115a-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="8115a-115">您是使用 [主要電子倉庫] 建立金鑰，現在想要將該金鑰克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。</span><span class="sxs-lookup"><span data-stu-id="8115a-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="8115a-116">使用 **AzKeyVaultKey** Cmdlet 以加密格式來檢索金鑰，然後使用 Restore-AzKeyVaultKey Cmdlet，並在第二個區域中指定金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="8115a-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="8115a-117">示例</span><span class="sxs-lookup"><span data-stu-id="8115a-117">EXAMPLES</span></span>

### <span data-ttu-id="8115a-118">範例1：使用自動產生的檔案名備份金鑰</span><span class="sxs-lookup"><span data-stu-id="8115a-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="8115a-119">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyKey 的金鑰，並將該金鑰的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="8115a-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="8115a-120">範例2：將金鑰備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="8115a-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="8115a-121">這個命令會從 key vaultnamed MyKeyVault 中檢索名為 MyKey 的金鑰，並將該金鑰的備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="8115a-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="8115a-122">範例3：將先前檢索的金鑰備份到指定的檔案名，不需提示即覆寫目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="8115a-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="8115a-123">這個命令會建立名為 $key 之金鑰的備份。名為 $key 的保存庫中的名稱。VaultName 到名為 Backup 的檔案，如果檔案已存在，則會以無訊息方式覆蓋該檔案。</span><span class="sxs-lookup"><span data-stu-id="8115a-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="8115a-124">參數</span><span class="sxs-lookup"><span data-stu-id="8115a-124">PARAMETERS</span></span>

### <span data-ttu-id="8115a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8115a-125">-DefaultProfile</span></span>
<span data-ttu-id="8115a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8115a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8115a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8115a-127">-Force</span></span>
<span data-ttu-id="8115a-128">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="8115a-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="8115a-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="8115a-129">-HsmName</span></span>
<span data-ttu-id="8115a-130">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="8115a-130">HSM name.</span></span> <span data-ttu-id="8115a-131">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8115a-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8115a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8115a-132">-InputObject</span></span>
<span data-ttu-id="8115a-133">要備份的主要捆綁，從檢索呼叫的輸出中流水線。</span><span class="sxs-lookup"><span data-stu-id="8115a-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="8115a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="8115a-134">-Name</span></span>
<span data-ttu-id="8115a-135">指定要備份的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="8115a-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8115a-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="8115a-136">-OutputFile</span></span>
<span data-ttu-id="8115a-137">指定儲存備份 blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="8115a-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="8115a-138">如果您沒有指定此參數，這個 Cmdlet 會為您產生檔案名。</span><span class="sxs-lookup"><span data-stu-id="8115a-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="8115a-139">如果您指定現有輸出檔案的名稱，該作業將無法完成，而且會傳回備份檔案已經存在的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="8115a-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="8115a-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8115a-140">-VaultName</span></span>
<span data-ttu-id="8115a-141">指定包含要備份之金鑰之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8115a-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="8115a-142">-確認</span><span class="sxs-lookup"><span data-stu-id="8115a-142">-Confirm</span></span>
<span data-ttu-id="8115a-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8115a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8115a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8115a-144">-WhatIf</span></span>
<span data-ttu-id="8115a-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8115a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8115a-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8115a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8115a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8115a-147">CommonParameters</span></span>
<span data-ttu-id="8115a-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8115a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8115a-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8115a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8115a-150">輸入</span><span class="sxs-lookup"><span data-stu-id="8115a-150">INPUTS</span></span>

### <span data-ttu-id="8115a-151">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8115a-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="8115a-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8115a-152">OUTPUTS</span></span>

### <span data-ttu-id="8115a-153">System.object</span><span class="sxs-lookup"><span data-stu-id="8115a-153">System.String</span></span>

## <span data-ttu-id="8115a-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8115a-154">NOTES</span></span>

## <span data-ttu-id="8115a-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8115a-155">RELATED LINKS</span></span>

[<span data-ttu-id="8115a-156">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8115a-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="8115a-157">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8115a-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="8115a-158">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8115a-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="8115a-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8115a-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

