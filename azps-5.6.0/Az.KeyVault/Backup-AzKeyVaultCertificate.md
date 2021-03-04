---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: e4692d9b623ce285a2be50d51a450fd8da39a5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906162"
---
# <span data-ttu-id="3ab96-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3ab96-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3ab96-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ab96-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab96-103">備份金鑰庫中的憑證。</span><span class="sxs-lookup"><span data-stu-id="3ab96-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="3ab96-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ab96-104">SYNTAX</span></span>

### <span data-ttu-id="3ab96-105">ByCertificateName (預設) </span><span class="sxs-lookup"><span data-stu-id="3ab96-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab96-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="3ab96-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab96-107">描述</span><span class="sxs-lookup"><span data-stu-id="3ab96-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab96-108">**Backup-AzKeyVaultCertificate Cmdlet** 會下載並儲存于檔案中，以備份金鑰保存庫中的指定憑證。</span><span class="sxs-lookup"><span data-stu-id="3ab96-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="3ab96-109">如果憑證有多個版本，其所有版本都會包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="3ab96-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="3ab96-110">由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="3ab96-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="3ab96-111">只要該憑證位於相同的 Azure 地理位置，您即可以將備份憑證還原到其備份之訂閱的任何金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="3ab96-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="3ab96-112">使用此 Cmdlet 的一般原因如下：</span><span class="sxs-lookup"><span data-stu-id="3ab96-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="3ab96-113">您想要保留憑證的離線副本，以防您不小心從保存庫刪除原始檔案。</span><span class="sxs-lookup"><span data-stu-id="3ab96-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="3ab96-114">您使用 Key Vault 建立憑證，而現在想要將物件複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用它。</span><span class="sxs-lookup"><span data-stu-id="3ab96-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="3ab96-115">使用 **Backup-AzKeyVaultCertificate** Cmdlet 以加密格式來取回憑證，然後使用 **Restore-AzKeyVaultCertificate** Cmdlet，並指定第二個地區的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="3ab96-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="3ab96-116">例子</span><span class="sxs-lookup"><span data-stu-id="3ab96-116">EXAMPLES</span></span>

### <span data-ttu-id="3ab96-117">範例 1：使用自動產生的檔案名備份憑證</span><span class="sxs-lookup"><span data-stu-id="3ab96-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="3ab96-118">此命令會從名為 MyKeyVault 的金鑰保存庫取取名為 MyCert 的憑證，並儲存該憑證的備份至自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="3ab96-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="3ab96-119">範例 2：將憑證備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="3ab96-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="3ab96-120">此命令會從名為 MyKeyVault 的金鑰保存庫取取名為 MyCert 的憑證，並儲存該憑證的備份至名為 Backup.blob 的檔案。</span><span class="sxs-lookup"><span data-stu-id="3ab96-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="3ab96-121">範例 3：將先前所取的憑證備份到指定的檔案名，覆寫目標檔案而不提示。</span><span class="sxs-lookup"><span data-stu-id="3ab96-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="3ab96-122">此命令會建立名為 $cert 的憑證備份。名稱為 $cert。保存庫名稱為名為 Backup.blob 的檔案，如果檔案已存在，會以無提示方式覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="3ab96-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="3ab96-123">參數</span><span class="sxs-lookup"><span data-stu-id="3ab96-123">PARAMETERS</span></span>

### <span data-ttu-id="3ab96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab96-124">-DefaultProfile</span></span>
<span data-ttu-id="3ab96-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ab96-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab96-126">-強制</span><span class="sxs-lookup"><span data-stu-id="3ab96-126">-Force</span></span>
<span data-ttu-id="3ab96-127">覆寫已存在的檔案</span><span class="sxs-lookup"><span data-stu-id="3ab96-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="3ab96-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ab96-128">-InputObject</span></span>
<span data-ttu-id="3ab96-129">要備份的機密，從呼叫的取回輸出中輸入。</span><span class="sxs-lookup"><span data-stu-id="3ab96-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab96-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ab96-130">-Name</span></span>
<span data-ttu-id="3ab96-131">機密名稱。</span><span class="sxs-lookup"><span data-stu-id="3ab96-131">Secret name.</span></span>
<span data-ttu-id="3ab96-132">Cmdlet 會從儲存庫名稱、目前選取的環境和機密名稱建構一個機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3ab96-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab96-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="3ab96-133">-OutputFile</span></span>
<span data-ttu-id="3ab96-134">輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="3ab96-134">Output file.</span></span>
<span data-ttu-id="3ab96-135">儲存憑證備份的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="3ab96-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="3ab96-136">如果未指定，將會產生預設檔案名。</span><span class="sxs-lookup"><span data-stu-id="3ab96-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="3ab96-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ab96-137">-VaultName</span></span>
<span data-ttu-id="3ab96-138">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3ab96-138">Vault name.</span></span>
<span data-ttu-id="3ab96-139">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3ab96-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab96-140">-確認</span><span class="sxs-lookup"><span data-stu-id="3ab96-140">-Confirm</span></span>
<span data-ttu-id="3ab96-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3ab96-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab96-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab96-142">-WhatIf</span></span>
<span data-ttu-id="3ab96-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ab96-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab96-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ab96-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab96-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab96-145">CommonParameters</span></span>
<span data-ttu-id="3ab96-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ab96-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab96-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ab96-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab96-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3ab96-148">INPUTS</span></span>

### <span data-ttu-id="3ab96-149">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3ab96-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="3ab96-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3ab96-150">OUTPUTS</span></span>

### <span data-ttu-id="3ab96-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3ab96-151">System.String</span></span>

## <span data-ttu-id="3ab96-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3ab96-152">NOTES</span></span>

## <span data-ttu-id="3ab96-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ab96-153">RELATED LINKS</span></span>
