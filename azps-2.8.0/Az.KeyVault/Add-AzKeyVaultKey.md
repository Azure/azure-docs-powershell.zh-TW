---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: f7447725e63634642f285b6a796a2b59b4d1d301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612165"
---
# <span data-ttu-id="1e458-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e458-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="1e458-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e458-102">SYNOPSIS</span></span>
<span data-ttu-id="1e458-103">在金鑰保存庫中建立金鑰或將金鑰匯入到金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="1e458-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="1e458-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e458-104">SYNTAX</span></span>

### <span data-ttu-id="1e458-105">InteractiveCreate (預設) </span><span class="sxs-lookup"><span data-stu-id="1e458-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e458-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="1e458-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e458-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="1e458-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e458-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="1e458-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e458-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="1e458-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e458-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="1e458-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e458-111">說明</span><span class="sxs-lookup"><span data-stu-id="1e458-111">DESCRIPTION</span></span>
<span data-ttu-id="1e458-112">AzKeyVaultKey Cmdlet 會在 Azure 金鑰保存庫中的金鑰保存庫中建立金鑰，或 **將** 金鑰匯入到金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="1e458-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="1e458-113">使用這個 Cmdlet，使用下列任何一種方法來新增金鑰：</span><span class="sxs-lookup"><span data-stu-id="1e458-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="1e458-114">在硬體安全模組中建立金鑰， (在主要 Vault 服務中的 HSM) 。</span><span class="sxs-lookup"><span data-stu-id="1e458-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="1e458-115">在金鑰 Vault 服務的軟體中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="1e458-116">從您自己的硬體安全模組將金鑰匯入到主要 Vault 服務中 (HSM) 至 Hsm。</span><span class="sxs-lookup"><span data-stu-id="1e458-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="1e458-117">從您電腦上的 .pfx 檔案匯入金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="1e458-118">從您電腦上的 .pfx 檔案將金鑰匯入到 [主要 Vault] 服務中 (Hsm) 的硬體安全模組。</span><span class="sxs-lookup"><span data-stu-id="1e458-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="1e458-119">針對這些作業中的任何一個，您可以提供重要屬性或接受預設設定。</span><span class="sxs-lookup"><span data-stu-id="1e458-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="1e458-120">如果您在金鑰保存庫中建立或匯入與現有金鑰同名的金鑰，則會使用您為新金鑰指定的值來更新原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="1e458-121">您可以使用該版本金鑰的版本特定 URI 來存取先前的值。</span><span class="sxs-lookup"><span data-stu-id="1e458-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="1e458-122">若要瞭解主要版本與 URI 結構，請參閱主要保存庫 REST API 檔中的 [金鑰與密碼](https://go.microsoft.com/fwlink/?linkid=518560) 。</span><span class="sxs-lookup"><span data-stu-id="1e458-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="1e458-123">注意：若要從您自己的硬體安全模組匯入金鑰，您必須先使用 Azure Key Vault BYOK 工具集，以) BYOK 副檔名 (的檔案來產生 BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="1e458-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="1e458-124">如需詳細資訊，請參閱 [如何為 Azure 金鑰電子倉庫產生及轉移 HSM-Protected 金鑰](https://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="1e458-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="1e458-125">最佳做法是使用 Backup-AzKeyVaultKey Cmdlet，在建立或更新金鑰後進行備份。</span><span class="sxs-lookup"><span data-stu-id="1e458-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="1e458-126">沒有取消刪除功能，因此如果您不小心刪除或刪除您的金鑰，然後改變主意，除非您有可以還原的備份，否則金鑰是無法復原的。</span><span class="sxs-lookup"><span data-stu-id="1e458-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="1e458-127">示例</span><span class="sxs-lookup"><span data-stu-id="1e458-127">EXAMPLES</span></span>

### <span data-ttu-id="1e458-128">範例1：建立索引鍵</span><span class="sxs-lookup"><span data-stu-id="1e458-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e458-129">這個命令會在名為 Contoso 的主要保存庫中，建立名為 ITSoftware 的軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e458-130">範例2：建立受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="1e458-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e458-131">這個命令會在名為 Contoso 的金鑰保存庫中建立受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e458-132">範例3：使用非預設值建立金鑰</span><span class="sxs-lookup"><span data-stu-id="1e458-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="1e458-133">第一個命令會儲存在 $KeyOperations 變數中解密和驗證的值。</span><span class="sxs-lookup"><span data-stu-id="1e458-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="1e458-134">第二個命令會建立一個 **DateTime** 物件（在 UTC 中定義），方法是使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e458-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="1e458-135">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="1e458-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="1e458-136">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e458-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="1e458-137">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="1e458-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1e458-138">第三個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="1e458-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e458-139">該物件會指定目前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="1e458-139">That object specifies current UTC time.</span></span> <span data-ttu-id="1e458-140">該命令會將該日期儲存在 $NotBefore 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e458-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="1e458-141">最後一個命令會建立一個名為 ITHsmNonDefault 的索引鍵，該金鑰是受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="1e458-142">此命令會指定儲存 $KeyOperations 所允許的按鍵作業值。</span><span class="sxs-lookup"><span data-stu-id="1e458-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="1e458-143">此命令會指定在前一個命令中建立的 *Expires* 及 *NotBefore* 參數的時間，以及高嚴重性及嚴重度的標記。</span><span class="sxs-lookup"><span data-stu-id="1e458-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="1e458-144">新的索引鍵是停用的。</span><span class="sxs-lookup"><span data-stu-id="1e458-144">The new key is disabled.</span></span> <span data-ttu-id="1e458-145">您可以使用 **AzKeyVaultKey** Cmdlet 來啟用它。</span><span class="sxs-lookup"><span data-stu-id="1e458-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="1e458-146">範例4：匯入受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="1e458-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e458-147">這個命令會從 *KeyFilePath* 參數指定的位置匯入名為 ITByok 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="1e458-148">匯入金鑰是受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="1e458-149">若要匯入您自己的硬體安全模組中的金鑰，您必須先使用 Azure 金鑰保存庫 BYOK 工具集，以) BYOK 副檔名 (的檔案來產生 BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="1e458-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="1e458-150">如需詳細資訊，請參閱 [如何為 Azure 金鑰電子倉庫產生及轉移 HSM-Protected 金鑰](https://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="1e458-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="1e458-151">範例5：匯入軟體保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="1e458-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e458-152">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e458-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="1e458-153">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="1e458-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1e458-154">第二個命令會在 Contoso 金鑰保存庫中建立軟體密碼。</span><span class="sxs-lookup"><span data-stu-id="1e458-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="1e458-155">命令會指定儲存在 $Password 的索引鍵和密碼的位置。</span><span class="sxs-lookup"><span data-stu-id="1e458-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="1e458-156">範例6：匯入金鑰並指派屬性</span><span class="sxs-lookup"><span data-stu-id="1e458-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="1e458-157">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e458-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="1e458-158">第二個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件，然後將該物件儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e458-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="1e458-159">第三個命令會建立 $tags 變數，以設定高嚴重性及它的標記。</span><span class="sxs-lookup"><span data-stu-id="1e458-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="1e458-160">最終的命令會將金鑰從指定的位置匯入為 HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="1e458-161">此命令會指定儲存在 $Password 中的 $Expires 和密碼儲存的到期時間，並套用 $tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="1e458-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="1e458-162">參數</span><span class="sxs-lookup"><span data-stu-id="1e458-162">PARAMETERS</span></span>

### <span data-ttu-id="1e458-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e458-163">-DefaultProfile</span></span>
<span data-ttu-id="1e458-164">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e458-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e458-165">-目的地</span><span class="sxs-lookup"><span data-stu-id="1e458-165">-Destination</span></span>
<span data-ttu-id="1e458-166">指定是否要在金鑰保存庫服務中，將金鑰新增為軟體保護金鑰或受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="1e458-167">有效值為： HSM 和軟體。</span><span class="sxs-lookup"><span data-stu-id="1e458-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="1e458-168">注意：若要使用 HSM 作為目的地，您必須擁有支援 Hsm 的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="1e458-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="1e458-169">如需有關 Azure 金鑰保存庫之服務層級和功能的詳細資訊，請參閱 [Azure 金鑰保存庫定價網站](https://go.microsoft.com/fwlink/?linkid=512521)。</span><span class="sxs-lookup"><span data-stu-id="1e458-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="1e458-170">當您建立新的金鑰時，這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="1e458-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="1e458-171">如果您使用 *KeyFilePath* 參數匯入金鑰，則此參數為 optional （選用）：</span><span class="sxs-lookup"><span data-stu-id="1e458-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="1e458-172">如果您沒有指定此參數，且這個 Cmdlet 會匯入副檔名為 byok 的金鑰，它會將該金鑰匯入為受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="1e458-173">Cmdlet 無法將該金鑰匯入為軟體保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="1e458-174">如果您沒有指定此參數，且這個 Cmdlet 會匯入副檔名為 .pfx 的金鑰，它會將金鑰匯入為軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-175">-停用</span><span class="sxs-lookup"><span data-stu-id="1e458-175">-Disable</span></span>
<span data-ttu-id="1e458-176">表示您要新增的金鑰已設定為 [已停用] 的初始狀態。</span><span class="sxs-lookup"><span data-stu-id="1e458-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="1e458-177">任何使用金鑰的嘗試都將失敗。</span><span class="sxs-lookup"><span data-stu-id="1e458-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="1e458-178">如果您正在預載入您想要稍後啟用的金鑰，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="1e458-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="1e458-179">-到期</span><span class="sxs-lookup"><span data-stu-id="1e458-179">-Expires</span></span>
<span data-ttu-id="1e458-180">指定此 Cmdlet 所新增之金鑰的到期時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="1e458-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="1e458-181">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="1e458-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1e458-182">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e458-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e458-183">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="1e458-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="1e458-184">如果您沒有指定此參數，金鑰就不會過期。</span><span class="sxs-lookup"><span data-stu-id="1e458-184">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e458-185">-InputObject</span></span>
<span data-ttu-id="1e458-186">Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="1e458-186">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="1e458-187">-KeyFilePassword</span></span>
<span data-ttu-id="1e458-188">指定匯入檔案的密碼做為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="1e458-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="1e458-189">若要取得 **SecureString** 物件，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e458-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="1e458-190">如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="1e458-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="1e458-191">您必須指定此密碼才能匯入副檔名為 .pfx 的檔案。</span><span class="sxs-lookup"><span data-stu-id="1e458-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="1e458-192">-KeyFilePath</span></span>
<span data-ttu-id="1e458-193">指定本機檔案的路徑，該檔案內含這個 Cmdlet 所匯入的重要材料。</span><span class="sxs-lookup"><span data-stu-id="1e458-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="1e458-194">有效的檔案名副檔名為 byok 和 .pfx。</span><span class="sxs-lookup"><span data-stu-id="1e458-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="1e458-195">如果檔案是 byok 檔案，則在匯入之後，金鑰會自動受 Hsm 保護，而且您無法覆寫此預設值。</span><span class="sxs-lookup"><span data-stu-id="1e458-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="1e458-196">如果檔案是 .pfx 檔案，則在匯入之後，該金鑰會自動受到軟體的保護。</span><span class="sxs-lookup"><span data-stu-id="1e458-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="1e458-197">若要覆寫此預設值，請將 *Destination* 參數設定為 hsm，讓金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="1e458-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="1e458-198">當您指定此參數時， *Destination* 參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1e458-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="1e458-199">-KeyOps</span></span>
<span data-ttu-id="1e458-200">指定可使用這個 Cmdlet 所新增之金鑰來執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="1e458-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="1e458-201">如果您沒有指定此參數，則可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="1e458-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="1e458-202">此參數可接受的值是由 [JSON Web 金鑰 (JWK) 規格](https://go.microsoft.com/fwlink/?LinkID=613300)所定義的以逗號分隔的主要動作清單：</span><span class="sxs-lookup"><span data-stu-id="1e458-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="1e458-203">進行</span><span class="sxs-lookup"><span data-stu-id="1e458-203">Encrypt</span></span>
- <span data-ttu-id="1e458-204">對</span><span class="sxs-lookup"><span data-stu-id="1e458-204">Decrypt</span></span>
- <span data-ttu-id="1e458-205">浮</span><span class="sxs-lookup"><span data-stu-id="1e458-205">Wrap</span></span>
- <span data-ttu-id="1e458-206">解</span><span class="sxs-lookup"><span data-stu-id="1e458-206">Unwrap</span></span>
- <span data-ttu-id="1e458-207">母音</span><span class="sxs-lookup"><span data-stu-id="1e458-207">Sign</span></span>
- <span data-ttu-id="1e458-208">是否</span><span class="sxs-lookup"><span data-stu-id="1e458-208">Verify</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-209">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e458-209">-Name</span></span>
<span data-ttu-id="1e458-210">指定要新增到 [主要電子倉庫] 的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="1e458-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="1e458-211">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="1e458-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="1e458-212">名稱必須是1到63個字元的字串，長度只包含0-9、a-z、A-z，並 (破折號) 符號。</span><span class="sxs-lookup"><span data-stu-id="1e458-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1e458-213">-NotBefore</span></span>
<span data-ttu-id="1e458-214">指定時間（作為 **DateTime** 物件），在此之後就不能使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1e458-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="1e458-215">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="1e458-215">This parameter uses UTC.</span></span> <span data-ttu-id="1e458-216">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e458-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e458-217">如果您沒有指定此參數，就可以立即使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e458-217">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e458-218">-ResourceId</span></span>
<span data-ttu-id="1e458-219">保存庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e458-219">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-220">-大小</span><span class="sxs-lookup"><span data-stu-id="1e458-220">-Size</span></span>
<span data-ttu-id="1e458-221">RSA 金鑰大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="1e458-221">RSA key size, in bits.</span></span> <span data-ttu-id="1e458-222">如果未指定，服務將會提供安全的預設值。</span><span class="sxs-lookup"><span data-stu-id="1e458-222">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e458-223">-Tag</span></span>
<span data-ttu-id="1e458-224">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="1e458-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e458-225">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1e458-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e458-226">-VaultName</span></span>
<span data-ttu-id="1e458-227">指定此 Cmdlet 要在其中新增金鑰的主要保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e458-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="1e458-228">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1e458-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e458-229">-確認</span><span class="sxs-lookup"><span data-stu-id="1e458-229">-Confirm</span></span>
<span data-ttu-id="1e458-230">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e458-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e458-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e458-231">-WhatIf</span></span>
<span data-ttu-id="1e458-232">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e458-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e458-233">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e458-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e458-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e458-234">CommonParameters</span></span>
<span data-ttu-id="1e458-235">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e458-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e458-236">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e458-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e458-237">輸入</span><span class="sxs-lookup"><span data-stu-id="1e458-237">INPUTS</span></span>

### <span data-ttu-id="1e458-238">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="1e458-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1e458-239">System.object</span><span class="sxs-lookup"><span data-stu-id="1e458-239">System.String</span></span>

## <span data-ttu-id="1e458-240">輸出</span><span class="sxs-lookup"><span data-stu-id="1e458-240">OUTPUTS</span></span>

### <span data-ttu-id="1e458-241">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="1e458-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1e458-242">筆記</span><span class="sxs-lookup"><span data-stu-id="1e458-242">NOTES</span></span>

## <span data-ttu-id="1e458-243">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e458-243">RELATED LINKS</span></span>

[<span data-ttu-id="1e458-244">備份-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e458-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="1e458-245">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e458-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="1e458-246">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e458-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1e458-247">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="1e458-247">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
