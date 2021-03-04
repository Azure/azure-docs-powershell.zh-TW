---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 3123d0fa188e0e9a4c419ceaa567969fc3a2f8b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908177"
---
# <span data-ttu-id="90d1e-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90d1e-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="90d1e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="90d1e-103">備份金鑰庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="90d1e-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="90d1e-104">語法</span><span class="sxs-lookup"><span data-stu-id="90d1e-104">SYNTAX</span></span>

### <span data-ttu-id="90d1e-105">ByKeyName (預設) </span><span class="sxs-lookup"><span data-stu-id="90d1e-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d1e-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="90d1e-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d1e-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="90d1e-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d1e-108">描述</span><span class="sxs-lookup"><span data-stu-id="90d1e-108">DESCRIPTION</span></span>
<span data-ttu-id="90d1e-109">**Backup-AzKeyVaultKey** Cmdlet 會下載金鑰並儲存于檔案中，以備份金鑰保存庫中的指定金鑰。</span><span class="sxs-lookup"><span data-stu-id="90d1e-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="90d1e-110">如果金鑰有多個版本，備份會包含所有版本。</span><span class="sxs-lookup"><span data-stu-id="90d1e-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="90d1e-111">由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="90d1e-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="90d1e-112">您可以將備份金鑰還原到訂閱中任何備份的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="90d1e-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="90d1e-113">使用此 Cmdlet 的一般原因如下：</span><span class="sxs-lookup"><span data-stu-id="90d1e-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="90d1e-114">您想要代管金鑰的一份副本，以便擁有離線副本，以防您不小心在金鑰保存庫中刪除金鑰。</span><span class="sxs-lookup"><span data-stu-id="90d1e-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="90d1e-115">您使用 Key Vault 建立金鑰，而現在想要將金鑰複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用該金鑰。</span><span class="sxs-lookup"><span data-stu-id="90d1e-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="90d1e-116">使用 **Backup-AzKeyVaultKey** Cmdlet 以加密格式來取回金鑰，然後使用 Restore-AzKeyVaultKey Cmdlet，並指定第二個地區的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="90d1e-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="90d1e-117">例子</span><span class="sxs-lookup"><span data-stu-id="90d1e-117">EXAMPLES</span></span>

### <span data-ttu-id="90d1e-118">範例 1：使用自動產生的檔案名備份金鑰</span><span class="sxs-lookup"><span data-stu-id="90d1e-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="90d1e-119">此命令會從名為 MyKeyVault 的金鑰保存庫中，從名為 MyKeyVault 的金鑰中，將該金鑰的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="90d1e-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="90d1e-120">範例 2：將金鑰備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="90d1e-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="90d1e-121">此命令會從名稱為 MyKeyVault 的金鑰保存庫中，從名為 MyKeyVault 的金鑰中，將該金鑰的備份儲存到名為 Backup.blob 的檔案。</span><span class="sxs-lookup"><span data-stu-id="90d1e-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="90d1e-122">範例 3：將先前所取的金鑰備份到指定的檔案名，覆寫目標檔案而不提示。</span><span class="sxs-lookup"><span data-stu-id="90d1e-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="90d1e-123">此命令會建立名為 $key 的金鑰備份。名稱為 $key。保存庫名稱為名為 Backup.blob 的檔案，如果檔案已存在，會以無提示方式覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="90d1e-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="90d1e-124">參數</span><span class="sxs-lookup"><span data-stu-id="90d1e-124">PARAMETERS</span></span>

### <span data-ttu-id="90d1e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d1e-125">-DefaultProfile</span></span>
<span data-ttu-id="90d1e-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="90d1e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90d1e-127">-強制</span><span class="sxs-lookup"><span data-stu-id="90d1e-127">-Force</span></span>
<span data-ttu-id="90d1e-128">覆寫已存在的檔案</span><span class="sxs-lookup"><span data-stu-id="90d1e-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="90d1e-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="90d1e-129">-HsmName</span></span>
<span data-ttu-id="90d1e-130">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="90d1e-130">HSM name.</span></span> <span data-ttu-id="90d1e-131">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="90d1e-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="90d1e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90d1e-132">-InputObject</span></span>
<span data-ttu-id="90d1e-133">要備份的金鑰組合，從呼叫的取回輸出中輸入。</span><span class="sxs-lookup"><span data-stu-id="90d1e-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="90d1e-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="90d1e-134">-Name</span></span>
<span data-ttu-id="90d1e-135">指定要備份的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="90d1e-135">Specifies the name of the key to back up.</span></span>

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

### <span data-ttu-id="90d1e-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="90d1e-136">-OutputFile</span></span>
<span data-ttu-id="90d1e-137">指定儲存備份 Blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="90d1e-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="90d1e-138">如果您未指定此參數，此 Cmdlet 會產生您的檔案名。</span><span class="sxs-lookup"><span data-stu-id="90d1e-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="90d1e-139">如果您指定現有輸出檔案的名稱，作業將不會完成，並返回備份檔案已存在的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="90d1e-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="90d1e-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="90d1e-140">-VaultName</span></span>
<span data-ttu-id="90d1e-141">指定包含要備份之金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="90d1e-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="90d1e-142">-確認</span><span class="sxs-lookup"><span data-stu-id="90d1e-142">-Confirm</span></span>
<span data-ttu-id="90d1e-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90d1e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d1e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d1e-144">-WhatIf</span></span>
<span data-ttu-id="90d1e-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90d1e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d1e-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90d1e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d1e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d1e-147">CommonParameters</span></span>
<span data-ttu-id="90d1e-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90d1e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d1e-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90d1e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d1e-150">輸入</span><span class="sxs-lookup"><span data-stu-id="90d1e-150">INPUTS</span></span>

### <span data-ttu-id="90d1e-151">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="90d1e-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="90d1e-152">輸出</span><span class="sxs-lookup"><span data-stu-id="90d1e-152">OUTPUTS</span></span>

### <span data-ttu-id="90d1e-153">System.String</span><span class="sxs-lookup"><span data-stu-id="90d1e-153">System.String</span></span>

## <span data-ttu-id="90d1e-154">筆記</span><span class="sxs-lookup"><span data-stu-id="90d1e-154">NOTES</span></span>

## <span data-ttu-id="90d1e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="90d1e-155">RELATED LINKS</span></span>

[<span data-ttu-id="90d1e-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90d1e-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="90d1e-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90d1e-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="90d1e-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90d1e-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="90d1e-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90d1e-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

