---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136768"
---
# <span data-ttu-id="29885-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="29885-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="29885-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29885-102">SYNOPSIS</span></span>
<span data-ttu-id="29885-103">備份 KeyVault 管理的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="29885-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="29885-104">句法</span><span class="sxs-lookup"><span data-stu-id="29885-104">SYNTAX</span></span>

### <span data-ttu-id="29885-105">ByStorageAccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="29885-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29885-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="29885-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29885-107">說明</span><span class="sxs-lookup"><span data-stu-id="29885-107">DESCRIPTION</span></span>
<span data-ttu-id="29885-108">**AzKeyVaultManagedStorageAccount** Cmdlet 會將指定的受管理儲存空間帳戶下載，並儲存在檔案中，以在金鑰保存庫中備份。</span><span class="sxs-lookup"><span data-stu-id="29885-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="29885-109">因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="29885-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="29885-110">只要電子倉庫位於同一個 Azure 地理位置，您就可以將備份的儲存空間帳戶還原到其備份之訂閱中的任何重要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="29885-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="29885-111">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="29885-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="29885-112">您想要保留儲存空間帳戶的離線複本，以防您不小心從 vault 刪除原始文檔。</span><span class="sxs-lookup"><span data-stu-id="29885-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="29885-113">您使用 [主要電子倉庫] 建立受管理的儲存空間帳戶，現在想要將物件克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。</span><span class="sxs-lookup"><span data-stu-id="29885-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="29885-114">使用 **AzKeyVaultManagedStorageAccount** Cmdlet 以加密格式來檢索受管理的儲存空間帳戶，然後使用 **Restore-AzKeyVaultManagedStorageAccount** Cmdlet，並在第二個區域中指定一個金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="29885-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="29885-115">示例</span><span class="sxs-lookup"><span data-stu-id="29885-115">EXAMPLES</span></span>

### <span data-ttu-id="29885-116">範例1：使用自動產生的檔案名備份受管理的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="29885-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="29885-117">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyMSAK 的受管理儲存空間帳戶，並將該受管理的儲存空間帳戶的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="29885-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="29885-118">範例2：將受管理的儲存空間帳戶備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="29885-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="29885-119">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyMSAK 的受管理儲存空間帳戶，並將該受管理的儲存空間帳戶的備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="29885-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="29885-120">範例3：將先前檢索到的受管理儲存空間帳戶備份到指定的檔案名，不需提示即覆寫目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="29885-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="29885-121">這個命令會建立名為 $msak 的受管理儲存空間帳戶的備份。名為 $msak 的保存庫中的名稱。VaultName 到名為 Backup 的檔案，如果檔案已存在，則會以無訊息方式覆蓋該檔案。</span><span class="sxs-lookup"><span data-stu-id="29885-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="29885-122">參數</span><span class="sxs-lookup"><span data-stu-id="29885-122">PARAMETERS</span></span>

### <span data-ttu-id="29885-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29885-123">-DefaultProfile</span></span>
<span data-ttu-id="29885-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29885-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29885-125">-Force</span><span class="sxs-lookup"><span data-stu-id="29885-125">-Force</span></span>
<span data-ttu-id="29885-126">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="29885-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="29885-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29885-127">-InputObject</span></span>
<span data-ttu-id="29885-128">要備份的儲存帳戶套件，從 [檢索呼叫] 的輸出中進行流水線。</span><span class="sxs-lookup"><span data-stu-id="29885-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="29885-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="29885-129">-Name</span></span>
<span data-ttu-id="29885-130">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="29885-130">Secret name.</span></span>
<span data-ttu-id="29885-131">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="29885-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="29885-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="29885-132">-OutputFile</span></span>
<span data-ttu-id="29885-133">輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="29885-133">Output file.</span></span>
<span data-ttu-id="29885-134">儲存儲存空間帳戶備份的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="29885-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="29885-135">如果未指定，將會產生預設檔案名。</span><span class="sxs-lookup"><span data-stu-id="29885-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="29885-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29885-136">-VaultName</span></span>
<span data-ttu-id="29885-137">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="29885-137">Vault name.</span></span>
<span data-ttu-id="29885-138">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="29885-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="29885-139">-確認</span><span class="sxs-lookup"><span data-stu-id="29885-139">-Confirm</span></span>
<span data-ttu-id="29885-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29885-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29885-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29885-141">-WhatIf</span></span>
<span data-ttu-id="29885-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29885-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29885-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29885-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29885-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29885-144">CommonParameters</span></span>
<span data-ttu-id="29885-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29885-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29885-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29885-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29885-147">輸入</span><span class="sxs-lookup"><span data-stu-id="29885-147">INPUTS</span></span>

### <span data-ttu-id="29885-148">PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="29885-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="29885-149">輸出</span><span class="sxs-lookup"><span data-stu-id="29885-149">OUTPUTS</span></span>

### <span data-ttu-id="29885-150">System.object</span><span class="sxs-lookup"><span data-stu-id="29885-150">System.String</span></span>

## <span data-ttu-id="29885-151">筆記</span><span class="sxs-lookup"><span data-stu-id="29885-151">NOTES</span></span>

## <span data-ttu-id="29885-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="29885-152">RELATED LINKS</span></span>
