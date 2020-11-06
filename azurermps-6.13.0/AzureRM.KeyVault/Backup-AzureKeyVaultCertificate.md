---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446990"
---
# <span data-ttu-id="03b87-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="03b87-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="03b87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03b87-102">SYNOPSIS</span></span>
<span data-ttu-id="03b87-103">在金鑰保存庫中備份憑證。</span><span class="sxs-lookup"><span data-stu-id="03b87-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03b87-104">句法</span><span class="sxs-lookup"><span data-stu-id="03b87-104">SYNTAX</span></span>

### <span data-ttu-id="03b87-105">ByCertificateName (預設) </span><span class="sxs-lookup"><span data-stu-id="03b87-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b87-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="03b87-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b87-107">說明</span><span class="sxs-lookup"><span data-stu-id="03b87-107">DESCRIPTION</span></span>
<span data-ttu-id="03b87-108">**AzureKeyVaultCertificate** Cmdlet 會透過下載並儲存在檔案中，以備份金鑰儲存庫中指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="03b87-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="03b87-109">如果憑證有多個版本，則備份中會包含其所有版本。</span><span class="sxs-lookup"><span data-stu-id="03b87-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="03b87-110">因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。</span><span class="sxs-lookup"><span data-stu-id="03b87-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="03b87-111">只要電子倉庫位於同一個 Azure 地理位置，您就可以將已備份的憑證還原到其備份之訂閱中的任何重要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="03b87-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="03b87-112">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="03b87-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="03b87-113">您想要保留憑證的離線複本，以防您不小心刪除電子倉庫中的原始版本。</span><span class="sxs-lookup"><span data-stu-id="03b87-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="03b87-114">您是使用金鑰保存庫建立憑證，現在想要將物件克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。</span><span class="sxs-lookup"><span data-stu-id="03b87-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="03b87-115">使用 **AzureKeyVaultCertificate** Cmdlet，以加密格式來檢索憑證，然後使用 **Restore-AzureKeyVaultCertificate** Cmdlet，並在第二個區域中指定一個金鑰保險存儲區。</span><span class="sxs-lookup"><span data-stu-id="03b87-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="03b87-116">示例</span><span class="sxs-lookup"><span data-stu-id="03b87-116">EXAMPLES</span></span>

### <span data-ttu-id="03b87-117">範例1：使用自動產生的檔案名備份憑證</span><span class="sxs-lookup"><span data-stu-id="03b87-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="03b87-118">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyCert 的憑證，並將該憑證的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="03b87-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="03b87-119">範例2：將憑證備份到指定的檔案名</span><span class="sxs-lookup"><span data-stu-id="03b87-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="03b87-120">這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyCert 的憑證，並將該憑證的備份儲存到名為 [Backup.] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="03b87-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="03b87-121">範例3：將先前檢索的憑證備份到指定的檔案名，不需提示即覆寫目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="03b87-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="03b87-122">這個命令會建立名為 $cert 的憑證備份。名為 $cert 的保存庫中的名稱。VaultName 到名為 Backup 的檔案，如果檔案已存在，則會以無訊息方式覆蓋該檔案。</span><span class="sxs-lookup"><span data-stu-id="03b87-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="03b87-123">參數</span><span class="sxs-lookup"><span data-stu-id="03b87-123">PARAMETERS</span></span>

### <span data-ttu-id="03b87-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b87-124">-DefaultProfile</span></span>
<span data-ttu-id="03b87-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03b87-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b87-126">-Force</span><span class="sxs-lookup"><span data-stu-id="03b87-126">-Force</span></span>
<span data-ttu-id="03b87-127">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="03b87-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="03b87-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03b87-128">-InputObject</span></span>
<span data-ttu-id="03b87-129">要備份的機密，從檢索呼叫的輸出中流水線。</span><span class="sxs-lookup"><span data-stu-id="03b87-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="03b87-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="03b87-130">-Name</span></span>
<span data-ttu-id="03b87-131">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="03b87-131">Secret name.</span></span>
<span data-ttu-id="03b87-132">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="03b87-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="03b87-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="03b87-133">-OutputFile</span></span>
<span data-ttu-id="03b87-134">輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="03b87-134">Output file.</span></span>
<span data-ttu-id="03b87-135">儲存憑證備份的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="03b87-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="03b87-136">如果未指定，將會產生預設檔案名。</span><span class="sxs-lookup"><span data-stu-id="03b87-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="03b87-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="03b87-137">-VaultName</span></span>
<span data-ttu-id="03b87-138">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="03b87-138">Vault name.</span></span>
<span data-ttu-id="03b87-139">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="03b87-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="03b87-140">-確認</span><span class="sxs-lookup"><span data-stu-id="03b87-140">-Confirm</span></span>
<span data-ttu-id="03b87-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03b87-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b87-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b87-142">-WhatIf</span></span>
<span data-ttu-id="03b87-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03b87-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b87-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03b87-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b87-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b87-145">CommonParameters</span></span>
<span data-ttu-id="03b87-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03b87-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b87-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03b87-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b87-148">輸入</span><span class="sxs-lookup"><span data-stu-id="03b87-148">INPUTS</span></span>

### <span data-ttu-id="03b87-149">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="03b87-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="03b87-150">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="03b87-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="03b87-151">輸出</span><span class="sxs-lookup"><span data-stu-id="03b87-151">OUTPUTS</span></span>

### <span data-ttu-id="03b87-152">System.object</span><span class="sxs-lookup"><span data-stu-id="03b87-152">System.String</span></span>

## <span data-ttu-id="03b87-153">筆記</span><span class="sxs-lookup"><span data-stu-id="03b87-153">NOTES</span></span>

## <span data-ttu-id="03b87-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="03b87-154">RELATED LINKS</span></span>
