---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911950"
---
# <span data-ttu-id="e1bab-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1bab-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e1bab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1bab-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bab-103">備份 KeyVault 管理的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e1bab-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="e1bab-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1bab-104">SYNTAX</span></span>

### <span data-ttu-id="e1bab-105">ByStorageAccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="e1bab-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bab-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1bab-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1bab-107">描述</span><span class="sxs-lookup"><span data-stu-id="e1bab-107">DESCRIPTION</span></span>
<span data-ttu-id="e1bab-108">**Backup-AzKeyVaultManagedStorageAccount** Cmdlet 可下載並儲存于檔案中，以備份金鑰保存庫中指定的受管理儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="e1bab-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="e1bab-109">由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="e1bab-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="e1bab-110">只要保存庫位於相同的 Azure 地理位置，您即可以將備份的儲存空間帳戶還原到訂閱中任何備份的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="e1bab-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="e1bab-111">使用此 Cmdlet 的一般原因如下：</span><span class="sxs-lookup"><span data-stu-id="e1bab-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="e1bab-112">您想要保留儲存空間帳戶的離線副本，以防您不小心從保存庫刪除原始檔案。</span><span class="sxs-lookup"><span data-stu-id="e1bab-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="e1bab-113">您使用 Key Vault 建立受管理的儲存帳戶，而現在想要將物件複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用它。</span><span class="sxs-lookup"><span data-stu-id="e1bab-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="e1bab-114">使用 **Backup-AzKeyVaultManagedStorageAccount** Cmdlet 以加密格式來取回受管理的儲存帳戶，然後使用 **Restore-AzKeyVaultManagedStorageAccount** Cmdlet，並指定第二個地區的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="e1bab-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="e1bab-115">例子</span><span class="sxs-lookup"><span data-stu-id="e1bab-115">EXAMPLES</span></span>

### <span data-ttu-id="e1bab-116">範例 1：使用自動產生的檔案名備份受管理的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="e1bab-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="e1bab-117">此命令會從名為 MyKeyVault 的金鑰保存庫中，從名為 MyMSAK 的受管理儲存帳戶，並儲存該受管理儲存帳戶的備份至自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="e1bab-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="e1bab-118">範例 2：將受管理的儲存空間帳戶備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="e1bab-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="e1bab-119">此命令會從名為 MyKeyVault 的金鑰保存庫中，從名為 MyMSAK 的受管理儲存帳戶，並儲存該受管理儲存帳戶的備份至名為 Backup.blob 的檔案。</span><span class="sxs-lookup"><span data-stu-id="e1bab-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="e1bab-120">範例 3：將先前取回的受管理的儲存空間帳戶備份到指定的檔案名，覆寫目標檔案而不提示。</span><span class="sxs-lookup"><span data-stu-id="e1bab-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="e1bab-121">此命令會建立名為 $msak 的受管理儲存帳戶$msak。名稱為 $msak。保存庫名稱為名為 Backup.blob 的檔案，如果檔案已存在，會以無提示方式覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="e1bab-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="e1bab-122">參數</span><span class="sxs-lookup"><span data-stu-id="e1bab-122">PARAMETERS</span></span>

### <span data-ttu-id="e1bab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bab-123">-DefaultProfile</span></span>
<span data-ttu-id="e1bab-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1bab-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bab-125">-強制</span><span class="sxs-lookup"><span data-stu-id="e1bab-125">-Force</span></span>
<span data-ttu-id="e1bab-126">覆寫已存在的檔案</span><span class="sxs-lookup"><span data-stu-id="e1bab-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="e1bab-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1bab-127">-InputObject</span></span>
<span data-ttu-id="e1bab-128">要備份的儲存空間帳戶套件，從呼叫的取回輸出中輸入。</span><span class="sxs-lookup"><span data-stu-id="e1bab-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bab-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1bab-129">-Name</span></span>
<span data-ttu-id="e1bab-130">機密名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bab-130">Secret name.</span></span>
<span data-ttu-id="e1bab-131">Cmdlet 會從儲存庫名稱、目前選取的環境和機密名稱建構一個機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e1bab-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bab-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e1bab-132">-OutputFile</span></span>
<span data-ttu-id="e1bab-133">輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="e1bab-133">Output file.</span></span>
<span data-ttu-id="e1bab-134">儲存儲存帳戶備份的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="e1bab-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="e1bab-135">如果未指定，將會產生預設檔案名。</span><span class="sxs-lookup"><span data-stu-id="e1bab-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="e1bab-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e1bab-136">-VaultName</span></span>
<span data-ttu-id="e1bab-137">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bab-137">Vault name.</span></span>
<span data-ttu-id="e1bab-138">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e1bab-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bab-139">-確認</span><span class="sxs-lookup"><span data-stu-id="e1bab-139">-Confirm</span></span>
<span data-ttu-id="e1bab-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e1bab-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1bab-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1bab-141">-WhatIf</span></span>
<span data-ttu-id="e1bab-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1bab-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1bab-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1bab-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1bab-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bab-144">CommonParameters</span></span>
<span data-ttu-id="e1bab-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1bab-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bab-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1bab-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bab-147">輸入</span><span class="sxs-lookup"><span data-stu-id="e1bab-147">INPUTS</span></span>

### <span data-ttu-id="e1bab-148">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e1bab-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e1bab-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e1bab-149">OUTPUTS</span></span>

### <span data-ttu-id="e1bab-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e1bab-150">System.String</span></span>

## <span data-ttu-id="e1bab-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e1bab-151">NOTES</span></span>

## <span data-ttu-id="e1bab-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1bab-152">RELATED LINKS</span></span>
