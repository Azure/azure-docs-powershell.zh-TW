---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: d2c153cf0ae2f5cffbf47656d3ae64a531cb780b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413790"
---
# <span data-ttu-id="b32bc-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="b32bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b32bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b32bc-103">在金鑰庫中建立金鑰，或將金鑰導入到金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="b32bc-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="b32bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="b32bc-104">SYNTAX</span></span>

### <span data-ttu-id="b32bc-105">InteractiveCreate (預設) </span><span class="sxs-lookup"><span data-stu-id="b32bc-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32bc-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="b32bc-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32bc-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="b32bc-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32bc-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="b32bc-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32bc-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="b32bc-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32bc-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="b32bc-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32bc-111">描述</span><span class="sxs-lookup"><span data-stu-id="b32bc-111">DESCRIPTION</span></span>
<span data-ttu-id="b32bc-112">**Add-AzKeyVaultKey** Cmdlet 在 Azure 金鑰庫的金鑰庫中建立金鑰，或將金鑰導入金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="b32bc-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="b32bc-113">使用此 Cmdlet 使用下列任一方法新增金鑰：</span><span class="sxs-lookup"><span data-stu-id="b32bc-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="b32bc-114">在金鑰庫服務 (HSM) 中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="b32bc-115">在 Key Vault 服務的軟體中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="b32bc-116">從您自己的硬體安全性模組將金鑰 (HSM) 金鑰庫服務中的 HSMS。</span><span class="sxs-lookup"><span data-stu-id="b32bc-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="b32bc-117">從您電腦的 .pfx 檔案中輸入金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="b32bc-118">將您電腦的 .pfx 檔案中的金鑰， (金鑰保存庫服務) HSMS 中的硬體安全性模組。</span><span class="sxs-lookup"><span data-stu-id="b32bc-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="b32bc-119">針對這些作業，您可以提供重要屬性或接受預設設定。</span><span class="sxs-lookup"><span data-stu-id="b32bc-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="b32bc-120">如果您建立或導入的金鑰與金鑰庫中現有金鑰的名稱相同，原始金鑰會以您為新金鑰指定的值更新。</span><span class="sxs-lookup"><span data-stu-id="b32bc-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="b32bc-121">您可以使用該金鑰版本的特定 URI 存取先前的值。</span><span class="sxs-lookup"><span data-stu-id="b32bc-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="b32bc-122">若要瞭解金鑰版本和 URI 結構，請參閱[](http://go.microsoft.com/fwlink/?linkid=518560)Key Vault REST API 檔中有關金鑰和秘訣的資訊。</span><span class="sxs-lookup"><span data-stu-id="b32bc-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="b32bc-123">注意：若要從您自己的硬體安全性模組中導入金鑰，您必須先使用 Azure Key Vault BYOK 工具集產生具有 .byok 副檔名 (的 BYOK 套件) 檔案。</span><span class="sxs-lookup"><span data-stu-id="b32bc-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="b32bc-124">詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="b32bc-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="b32bc-125">最佳做法是在建立或更新金鑰之後，使用 Backup-AzKeyVaultKey備份。</span><span class="sxs-lookup"><span data-stu-id="b32bc-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="b32bc-126">沒有任何取消刪除的功能，因此如果您不小心刪除或刪除金鑰，然後改變心意，除非有可還原的備份，否則無法復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="b32bc-127">例子</span><span class="sxs-lookup"><span data-stu-id="b32bc-127">EXAMPLES</span></span>

### <span data-ttu-id="b32bc-128">範例 1：建立金鑰</span><span class="sxs-lookup"><span data-stu-id="b32bc-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="b32bc-129">此命令在名為 Contoso 的金鑰庫中，建立一個名為 ITSoftware 的軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="b32bc-130">範例 2：建立受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="b32bc-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="b32bc-131">此命令在名為 Contoso 的金鑰庫中建立受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="b32bc-132">範例 3：建立具有非預設值的金鑰</span><span class="sxs-lookup"><span data-stu-id="b32bc-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="b32bc-133">第一個命令會儲存值解密，並在$KeyOperations驗證。</span><span class="sxs-lookup"><span data-stu-id="b32bc-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="b32bc-134">第二個命令會使用 **Get-Date** Cmdlet 建立以 UTC 定義的 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="b32bc-135">該物件會指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="b32bc-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="b32bc-136">命令會儲存該日期至$Expires變數。</span><span class="sxs-lookup"><span data-stu-id="b32bc-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="b32bc-137">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b32bc-138">第三個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b32bc-139">該物件會指定目前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="b32bc-139">That object specifies current UTC time.</span></span> <span data-ttu-id="b32bc-140">命令會儲存該日期至$NotBefore變數。</span><span class="sxs-lookup"><span data-stu-id="b32bc-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="b32bc-141">最後一個命令會建立名為 ITHMNonDefault 的金鑰，該金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="b32bc-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="b32bc-142">該命令會指定儲存于其中之允許之金鑰作業$KeyOperations。</span><span class="sxs-lookup"><span data-stu-id="b32bc-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="b32bc-143">命令會指定在先前命令中建立之 *到期* 和 *NotBefore* 參數的時間，以及高嚴重性和 IT 的標記。</span><span class="sxs-lookup"><span data-stu-id="b32bc-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="b32bc-144">新金鑰已停用。</span><span class="sxs-lookup"><span data-stu-id="b32bc-144">The new key is disabled.</span></span> <span data-ttu-id="b32bc-145">您可以使用 **Set-AzKeyVaultKey** Cmdlet 來啟用。</span><span class="sxs-lookup"><span data-stu-id="b32bc-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="b32bc-146">範例 4：匯出受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="b32bc-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="b32bc-147">此命令會從 KeyFilePath 參數指定的位置，將 *名為 ITByok* 的金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="b32bc-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="b32bc-148">所導入的金鑰是受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="b32bc-149">若要從您自己的硬體安全性模組中輸入金鑰，您必須先使用 Azure Key Vault BYOK 工具集 (產生副檔名為 .byok 的檔案) BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="b32bc-150">詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="b32bc-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="b32bc-151">範例 5：匯出軟體保護金鑰</span><span class="sxs-lookup"><span data-stu-id="b32bc-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="b32bc-152">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="b32bc-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="b32bc-153">如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="b32bc-154">第二個命令在 Contoso 金鑰保存庫中建立軟體密碼。</span><span class="sxs-lookup"><span data-stu-id="b32bc-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="b32bc-155">命令會指定金鑰的位置，以及儲存在 $Password。</span><span class="sxs-lookup"><span data-stu-id="b32bc-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="b32bc-156">範例 6：輸入金鑰並指派屬性</span><span class="sxs-lookup"><span data-stu-id="b32bc-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="b32bc-157">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="b32bc-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="b32bc-158">第二個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件，然後將該物件儲存在$Expires變數中。</span><span class="sxs-lookup"><span data-stu-id="b32bc-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="b32bc-159">第三個命令會建立$tags變數，以設定高嚴重性和 IT 的標記。</span><span class="sxs-lookup"><span data-stu-id="b32bc-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="b32bc-160">最後一個命令會從指定位置將金鑰輸入為 HSM 鍵。</span><span class="sxs-lookup"><span data-stu-id="b32bc-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="b32bc-161">命令會指定儲存在 $Expires 中的到期日和密碼$Password，並適用儲存在 $tags 中的標記。</span><span class="sxs-lookup"><span data-stu-id="b32bc-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="b32bc-162">範例 7：產生 KEY Exchange 金鑰 (KEK) FOR "bring your own key" (BYOK) 功能</span><span class="sxs-lookup"><span data-stu-id="b32bc-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="b32bc-163">產生稱為 KEY Exchange (KEY Exchange 鍵 (KEK) ) 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="b32bc-164">KEK 必須是只包含導入金鑰作業的 RSA-HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="b32bc-165">只有 Key Vault Premium SKU 支援 RSA-HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="b32bc-166">如需詳細資料，請參閱 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="b32bc-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="b32bc-167">參數</span><span class="sxs-lookup"><span data-stu-id="b32bc-167">PARAMETERS</span></span>

### <span data-ttu-id="b32bc-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32bc-168">-DefaultProfile</span></span>
<span data-ttu-id="b32bc-169">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b32bc-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b32bc-170">-目的地</span><span class="sxs-lookup"><span data-stu-id="b32bc-170">-Destination</span></span>
<span data-ttu-id="b32bc-171">指定是否要在 Key Vault 服務中將金鑰新增為受軟體保護的金鑰或 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="b32bc-172">有效的值為：HSM 和 Software。</span><span class="sxs-lookup"><span data-stu-id="b32bc-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="b32bc-173">注意：若要使用 HSM 做為目的地，您必須有支援 HSMS 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="b32bc-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="b32bc-174">有關 Azure 金鑰庫的服務層級和功能的詳細資訊，請參閱 [Azure 金鑰庫定價網站](http://go.microsoft.com/fwlink/?linkid=512521)。</span><span class="sxs-lookup"><span data-stu-id="b32bc-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="b32bc-175">當您建立新金鑰時，需要此參數。</span><span class="sxs-lookup"><span data-stu-id="b32bc-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="b32bc-176">如果您使用 *KeyFilePath* 參數來輸入金鑰，此參數為選擇性：</span><span class="sxs-lookup"><span data-stu-id="b32bc-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="b32bc-177">如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .byok 的金鑰，它會以 HSM 保護金鑰來輸入該金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="b32bc-178">Cmdlet 無法將該金鑰以軟體保護金鑰進行導入。</span><span class="sxs-lookup"><span data-stu-id="b32bc-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="b32bc-179">如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .pfx 的金鑰，它會將金鑰以軟體保護金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="b32bc-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="b32bc-180">-停用</span><span class="sxs-lookup"><span data-stu-id="b32bc-180">-Disable</span></span>
<span data-ttu-id="b32bc-181">表示您新增的金鑰已設定為初始停用狀態。</span><span class="sxs-lookup"><span data-stu-id="b32bc-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="b32bc-182">任何使用金鑰的嘗試都會失敗。</span><span class="sxs-lookup"><span data-stu-id="b32bc-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="b32bc-183">如果您要預先載入要稍後啟用的金鑰，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="b32bc-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="b32bc-184">-到期</span><span class="sxs-lookup"><span data-stu-id="b32bc-184">-Expires</span></span>
<span data-ttu-id="b32bc-185">指定此 Cmdlet 新增之金鑰的到期日 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="b32bc-186">此參數使用 Utc (協調) 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b32bc-187">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b32bc-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b32bc-188">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="b32bc-189">如果您未指定此參數，金鑰不會過期。</span><span class="sxs-lookup"><span data-stu-id="b32bc-189">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="b32bc-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b32bc-190">-InputObject</span></span>
<span data-ttu-id="b32bc-191">Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-191">Vault object.</span></span>

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

### <span data-ttu-id="b32bc-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="b32bc-192">-KeyFilePassword</span></span>
<span data-ttu-id="b32bc-193">將所輸入檔案的密碼指定為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="b32bc-194">若要取得 **SecureString 物件** ，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b32bc-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="b32bc-195">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="b32bc-196">您必須指定此密碼，才能使用 .pfx 副檔名來輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="b32bc-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="b32bc-197">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="b32bc-197">-KeyFilePath</span></span>
<span data-ttu-id="b32bc-198">指定包含此 Cmdlet 所導入之重要資料之本地檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b32bc-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="b32bc-199">有效的副檔名為 .byok 和 .pfx。</span><span class="sxs-lookup"><span data-stu-id="b32bc-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="b32bc-200">如果檔案是 .byok 檔案，則金鑰會在進行匯出後自動受到 HSMS 保護，而且您無法覆蓋此預設值。</span><span class="sxs-lookup"><span data-stu-id="b32bc-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="b32bc-201">如果檔案是 .pfx 檔案，則金鑰會在匯出後自動受到軟體保護。</span><span class="sxs-lookup"><span data-stu-id="b32bc-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="b32bc-202">若要覆蓋此預設值，將 *Destination* 參數設定為 HSM，讓金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="b32bc-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="b32bc-203">當您指定此參數時 *，Destination* 參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b32bc-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="b32bc-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="b32bc-204">-KeyOps</span></span>
<span data-ttu-id="b32bc-205">指定可以使用此 Cmdlet 新增的金鑰執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="b32bc-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="b32bc-206">如果您未指定此參數，可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="b32bc-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="b32bc-207">此參數可接受的值是 JSON Web Key ([JWK](http://go.microsoft.com/fwlink/?LinkID=613300)) 定義之金鑰作業的逗號分隔清單：</span><span class="sxs-lookup"><span data-stu-id="b32bc-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="b32bc-208">加密</span><span class="sxs-lookup"><span data-stu-id="b32bc-208">encrypt</span></span>
- <span data-ttu-id="b32bc-209">解密</span><span class="sxs-lookup"><span data-stu-id="b32bc-209">decrypt</span></span>
- <span data-ttu-id="b32bc-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-210">wrapKey</span></span>
- <span data-ttu-id="b32bc-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-211">unwrapKey</span></span>
- <span data-ttu-id="b32bc-212">標誌</span><span class="sxs-lookup"><span data-stu-id="b32bc-212">sign</span></span>
- <span data-ttu-id="b32bc-213">驗證</span><span class="sxs-lookup"><span data-stu-id="b32bc-213">verify</span></span>
- <span data-ttu-id="b32bc-214">僅 (KEK 的匯出資料，請參閱範例 7) </span><span class="sxs-lookup"><span data-stu-id="b32bc-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="b32bc-215">-名稱</span><span class="sxs-lookup"><span data-stu-id="b32bc-215">-Name</span></span>
<span data-ttu-id="b32bc-216">指定要新加到金鑰庫的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="b32bc-217">此 Cmdlet 會依據此參數指定的名稱、金鑰庫名稱，以及您目前的環境，建構金鑰的完全限定功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="b32bc-218">名稱必須是長度為 1 到 63 個字元的字串，只包含 0-9、a-z、A-Z 和 - (破折號) 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="b32bc-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b32bc-219">-NotBefore</span></span>
<span data-ttu-id="b32bc-220">指定無法使用金鑰的時間 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b32bc-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="b32bc-221">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="b32bc-221">This parameter uses UTC.</span></span> <span data-ttu-id="b32bc-222">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b32bc-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b32bc-223">如果您未指定此參數，可以立即使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b32bc-223">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="b32bc-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b32bc-224">-ResourceId</span></span>
<span data-ttu-id="b32bc-225">Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b32bc-225">Vault Resource Id.</span></span>

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

### <span data-ttu-id="b32bc-226">-大小</span><span class="sxs-lookup"><span data-stu-id="b32bc-226">-Size</span></span>
<span data-ttu-id="b32bc-227">以位為單位的 RSA 金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="b32bc-227">RSA key size, in bits.</span></span> <span data-ttu-id="b32bc-228">如果未指定，服務會提供安全預設值。</span><span class="sxs-lookup"><span data-stu-id="b32bc-228">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="b32bc-229">-標記</span><span class="sxs-lookup"><span data-stu-id="b32bc-229">-Tag</span></span>
<span data-ttu-id="b32bc-230">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="b32bc-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b32bc-231">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b32bc-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b32bc-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b32bc-232">-VaultName</span></span>
<span data-ttu-id="b32bc-233">指定此 Cmdlet 新增該金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="b32bc-234">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b32bc-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="b32bc-235">-確認</span><span class="sxs-lookup"><span data-stu-id="b32bc-235">-Confirm</span></span>
<span data-ttu-id="b32bc-236">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b32bc-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32bc-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32bc-237">-WhatIf</span></span>
<span data-ttu-id="b32bc-238">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b32bc-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b32bc-239">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b32bc-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32bc-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32bc-240">CommonParameters</span></span>
<span data-ttu-id="b32bc-241">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b32bc-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32bc-242">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b32bc-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32bc-243">輸入</span><span class="sxs-lookup"><span data-stu-id="b32bc-243">INPUTS</span></span>

### <span data-ttu-id="b32bc-244">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b32bc-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b32bc-245">System.String</span><span class="sxs-lookup"><span data-stu-id="b32bc-245">System.String</span></span>

## <span data-ttu-id="b32bc-246">輸出</span><span class="sxs-lookup"><span data-stu-id="b32bc-246">OUTPUTS</span></span>

### <span data-ttu-id="b32bc-247">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b32bc-248">筆記</span><span class="sxs-lookup"><span data-stu-id="b32bc-248">NOTES</span></span>

## <span data-ttu-id="b32bc-249">相關連結</span><span class="sxs-lookup"><span data-stu-id="b32bc-249">RELATED LINKS</span></span>

[<span data-ttu-id="b32bc-250">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="b32bc-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="b32bc-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b32bc-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

