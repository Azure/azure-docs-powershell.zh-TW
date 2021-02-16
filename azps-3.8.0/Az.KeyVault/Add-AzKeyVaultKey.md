---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 3d0f7267d1dbe899de0e0414c52a395985f09bfd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412532"
---
# <span data-ttu-id="0c577-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c577-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="0c577-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c577-102">SYNOPSIS</span></span>
<span data-ttu-id="0c577-103">在金鑰庫中建立金鑰，或將金鑰導入到金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="0c577-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="0c577-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c577-104">SYNTAX</span></span>

### <span data-ttu-id="0c577-105">InteractiveCreate (預設) </span><span class="sxs-lookup"><span data-stu-id="0c577-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c577-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="0c577-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c577-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="0c577-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c577-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="0c577-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c577-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="0c577-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c577-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="0c577-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c577-111">描述</span><span class="sxs-lookup"><span data-stu-id="0c577-111">DESCRIPTION</span></span>
<span data-ttu-id="0c577-112">**Add-AzKeyVaultKey** Cmdlet 在 Azure 金鑰庫的金鑰庫中建立金鑰，或將金鑰導入金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="0c577-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="0c577-113">使用此 Cmdlet 使用下列任一方法新增金鑰：</span><span class="sxs-lookup"><span data-stu-id="0c577-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="0c577-114">在金鑰庫服務中的 HSM (中) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="0c577-115">在 Key Vault 服務的軟體中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="0c577-116">從您自己的硬體安全性模組將金鑰 (HSM) 金鑰庫服務中的 HSMS。</span><span class="sxs-lookup"><span data-stu-id="0c577-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="0c577-117">從您電腦的 .pfx 檔案中輸入金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="0c577-118">將您電腦的 .pfx 檔案中的金鑰， (金鑰保存庫服務) HSMS 中的硬體安全性模組。</span><span class="sxs-lookup"><span data-stu-id="0c577-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="0c577-119">針對任何這些作業，您可以提供重要屬性或接受預設設定。</span><span class="sxs-lookup"><span data-stu-id="0c577-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="0c577-120">如果您建立或導入的金鑰與金鑰庫中現有金鑰的名稱相同，原始金鑰會以您為新金鑰指定的值更新。</span><span class="sxs-lookup"><span data-stu-id="0c577-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="0c577-121">您可以使用該金鑰版本的特定 URI 存取先前的值。</span><span class="sxs-lookup"><span data-stu-id="0c577-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="0c577-122">若要瞭解金鑰版本和 URI 結構，請參閱[](http://go.microsoft.com/fwlink/?linkid=518560)Key Vault REST API 檔中關於金鑰和秘訣的資訊。</span><span class="sxs-lookup"><span data-stu-id="0c577-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="0c577-123">注意：若要從您自己的硬體安全性模組中導入金鑰，您必須先使用 Azure Key Vault BYOK 工具集產生具有 .byok 副檔名 (的 BYOK 套件) 檔案。</span><span class="sxs-lookup"><span data-stu-id="0c577-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="0c577-124">詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="0c577-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="0c577-125">最佳做法是在建立或更新金鑰之後，使用 Backup-AzKeyVaultKey備份。</span><span class="sxs-lookup"><span data-stu-id="0c577-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="0c577-126">沒有任何取消刪除的功能，因此如果您不小心刪除或刪除金鑰，然後改變心意，除非有可還原的備份，否則無法復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="0c577-127">例子</span><span class="sxs-lookup"><span data-stu-id="0c577-127">EXAMPLES</span></span>

### <span data-ttu-id="0c577-128">範例 1：建立金鑰</span><span class="sxs-lookup"><span data-stu-id="0c577-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="0c577-129">此命令在名為 Contoso 的金鑰庫中，建立一個名為 ITSoftware 的軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="0c577-130">範例 2：建立受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="0c577-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="0c577-131">此命令在名為 Contoso 的金鑰庫中建立受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="0c577-132">範例 3：建立具有非預設值的金鑰</span><span class="sxs-lookup"><span data-stu-id="0c577-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="0c577-133">第一個命令會儲存值解密，並在$KeyOperations驗證。</span><span class="sxs-lookup"><span data-stu-id="0c577-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="0c577-134">第二個命令會使用 **Get-Date** Cmdlet 建立以 UTC 定義的 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c577-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0c577-135">該物件會指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="0c577-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="0c577-136">命令會儲存該日期至$Expires變數。</span><span class="sxs-lookup"><span data-stu-id="0c577-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="0c577-137">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="0c577-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0c577-138">第三個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c577-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0c577-139">該物件會指定目前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="0c577-139">That object specifies current UTC time.</span></span> <span data-ttu-id="0c577-140">命令會儲存該日期至$NotBefore變數。</span><span class="sxs-lookup"><span data-stu-id="0c577-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="0c577-141">最後一個命令會建立名為 ITHMNonDefault 的金鑰，該金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="0c577-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="0c577-142">該命令會指定儲存于其中之允許之金鑰作業$KeyOperations。</span><span class="sxs-lookup"><span data-stu-id="0c577-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="0c577-143">命令會指定在先前命令中建立之 *到期* 和 *NotBefore* 參數的時間，以及高嚴重性和 IT 的標記。</span><span class="sxs-lookup"><span data-stu-id="0c577-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="0c577-144">新金鑰已停用。</span><span class="sxs-lookup"><span data-stu-id="0c577-144">The new key is disabled.</span></span> <span data-ttu-id="0c577-145">您可以使用 **Set-AzKeyVaultKey** Cmdlet 來啟用。</span><span class="sxs-lookup"><span data-stu-id="0c577-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="0c577-146">範例 4：匯出受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="0c577-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="0c577-147">此命令會從 KeyFilePath 參數指定的位置，將 *名為 ITByok* 的金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="0c577-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="0c577-148">所輸入的金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="0c577-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="0c577-149">若要從您自己的硬體安全性模組中輸入金鑰，您必須先使用 Azure Key Vault BYOK 工具集 (產生副檔名為 .byok 的檔案) BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="0c577-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="0c577-150">詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="0c577-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="0c577-151">範例 5：匯出軟體保護金鑰</span><span class="sxs-lookup"><span data-stu-id="0c577-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="0c577-152">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c577-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="0c577-153">如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="0c577-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="0c577-154">第二個命令在 Contoso 金鑰保存庫中建立軟體密碼。</span><span class="sxs-lookup"><span data-stu-id="0c577-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="0c577-155">命令會指定金鑰的位置，以及儲存在 $Password。</span><span class="sxs-lookup"><span data-stu-id="0c577-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="0c577-156">範例 6：輸入金鑰並指派屬性</span><span class="sxs-lookup"><span data-stu-id="0c577-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="0c577-157">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c577-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="0c577-158">第二個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件，然後將該物件儲存在$Expires變數中。</span><span class="sxs-lookup"><span data-stu-id="0c577-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="0c577-159">第三個命令會建立$tags變數，以設定高嚴重性和 IT 的標記。</span><span class="sxs-lookup"><span data-stu-id="0c577-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="0c577-160">最後一個命令會從指定位置將金鑰輸入為 HSM 鍵。</span><span class="sxs-lookup"><span data-stu-id="0c577-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="0c577-161">命令會指定儲存在 $Expires 中的到期日和密碼$Password，並適用儲存在 $tags 中的標記。</span><span class="sxs-lookup"><span data-stu-id="0c577-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="0c577-162">參數</span><span class="sxs-lookup"><span data-stu-id="0c577-162">PARAMETERS</span></span>

### <span data-ttu-id="0c577-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c577-163">-DefaultProfile</span></span>
<span data-ttu-id="0c577-164">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0c577-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c577-165">-目的地</span><span class="sxs-lookup"><span data-stu-id="0c577-165">-Destination</span></span>
<span data-ttu-id="0c577-166">指定是否要在 Key Vault 服務中將金鑰新增為受軟體保護的金鑰或 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="0c577-167">有效的值為：HSM 和 Software。</span><span class="sxs-lookup"><span data-stu-id="0c577-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="0c577-168">注意：若要使用 HSM 做為目的地，您必須有支援 HSMS 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="0c577-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="0c577-169">有關 Azure 金鑰庫的服務層級和功能的詳細資訊，請參閱 [Azure 金鑰庫定價網站](http://go.microsoft.com/fwlink/?linkid=512521)。</span><span class="sxs-lookup"><span data-stu-id="0c577-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="0c577-170">當您建立新金鑰時，需要此參數。</span><span class="sxs-lookup"><span data-stu-id="0c577-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="0c577-171">如果您使用 *KeyFilePath* 參數來輸入金鑰，此參數為選擇性：</span><span class="sxs-lookup"><span data-stu-id="0c577-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="0c577-172">如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .byok 的金鑰，它會將該金鑰以 HSM 保護的金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="0c577-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="0c577-173">Cmdlet 無法將該金鑰以軟體保護金鑰進行導入。</span><span class="sxs-lookup"><span data-stu-id="0c577-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="0c577-174">如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .pfx 的金鑰，它會將金鑰以軟體保護金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="0c577-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="0c577-175">-停用</span><span class="sxs-lookup"><span data-stu-id="0c577-175">-Disable</span></span>
<span data-ttu-id="0c577-176">表示您新增的金鑰已設定為初始停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0c577-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="0c577-177">任何使用金鑰的嘗試都會失敗。</span><span class="sxs-lookup"><span data-stu-id="0c577-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="0c577-178">如果您要預先載入要稍後啟用的金鑰，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="0c577-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="0c577-179">-到期</span><span class="sxs-lookup"><span data-stu-id="0c577-179">-Expires</span></span>
<span data-ttu-id="0c577-180">指定此 Cmdlet 新增之金鑰的到期日 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c577-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="0c577-181">此參數使用 Utc (協調) 。</span><span class="sxs-lookup"><span data-stu-id="0c577-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0c577-182">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c577-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0c577-183">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="0c577-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="0c577-184">如果您未指定此參數，金鑰不會過期。</span><span class="sxs-lookup"><span data-stu-id="0c577-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="0c577-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c577-185">-InputObject</span></span>
<span data-ttu-id="0c577-186">Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="0c577-186">Vault object.</span></span>

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

### <span data-ttu-id="0c577-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="0c577-187">-KeyFilePassword</span></span>
<span data-ttu-id="0c577-188">將所輸入檔案的密碼指定為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c577-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="0c577-189">若要取得 **SecureString 物件** ，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c577-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="0c577-190">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="0c577-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="0c577-191">您必須指定此密碼，才能使用 .pfx 副檔名來輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="0c577-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="0c577-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="0c577-192">-KeyFilePath</span></span>
<span data-ttu-id="0c577-193">指定包含此 Cmdlet 所導入之重要資料之本地檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0c577-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="0c577-194">有效的副檔名為 .byok 和 .pfx。</span><span class="sxs-lookup"><span data-stu-id="0c577-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="0c577-195">如果檔案是 .byok 檔案，則金鑰會在進行匯出後自動受到 HSMS 保護，而且您無法覆蓋此預設值。</span><span class="sxs-lookup"><span data-stu-id="0c577-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="0c577-196">如果檔案是 .pfx 檔案，則金鑰會在匯出後自動受到軟體保護。</span><span class="sxs-lookup"><span data-stu-id="0c577-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="0c577-197">若要覆蓋此預設值，將 *Destination* 參數設定為 HSM，讓金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="0c577-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="0c577-198">當您指定此參數時 *，Destination* 參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="0c577-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="0c577-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="0c577-199">-KeyOps</span></span>
<span data-ttu-id="0c577-200">指定可以使用此 Cmdlet 新增的金鑰執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="0c577-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="0c577-201">如果您未指定此參數，可以執行所有操作。</span><span class="sxs-lookup"><span data-stu-id="0c577-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="0c577-202">此參數可接受的值是 JSON Web Key ([JWK](http://go.microsoft.com/fwlink/?LinkID=613300)) 定義之金鑰作業的逗號分隔清單：</span><span class="sxs-lookup"><span data-stu-id="0c577-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="0c577-203">加密</span><span class="sxs-lookup"><span data-stu-id="0c577-203">Encrypt</span></span>
- <span data-ttu-id="0c577-204">解密</span><span class="sxs-lookup"><span data-stu-id="0c577-204">Decrypt</span></span>
- <span data-ttu-id="0c577-205">包裝</span><span class="sxs-lookup"><span data-stu-id="0c577-205">Wrap</span></span>
- <span data-ttu-id="0c577-206">打開</span><span class="sxs-lookup"><span data-stu-id="0c577-206">Unwrap</span></span>
- <span data-ttu-id="0c577-207">標誌</span><span class="sxs-lookup"><span data-stu-id="0c577-207">Sign</span></span>
- <span data-ttu-id="0c577-208">驗證</span><span class="sxs-lookup"><span data-stu-id="0c577-208">Verify</span></span>

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

### <span data-ttu-id="0c577-209">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c577-209">-Name</span></span>
<span data-ttu-id="0c577-210">指定要新加到金鑰庫的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="0c577-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="0c577-211">此 Cmdlet 會依據此參數指定的名稱、金鑰庫名稱，以及您目前的環境，建構金鑰的完全限定功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="0c577-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="0c577-212">名稱必須是長度為 1 到 63 個字元的字串，只包含 0-9、a-z、A-Z 和 - (破折號) 。</span><span class="sxs-lookup"><span data-stu-id="0c577-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="0c577-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0c577-213">-NotBefore</span></span>
<span data-ttu-id="0c577-214">指定無法使用金鑰的時間 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c577-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="0c577-215">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="0c577-215">This parameter uses UTC.</span></span> <span data-ttu-id="0c577-216">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c577-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0c577-217">如果您未指定此參數，可以立即使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c577-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="0c577-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c577-218">-ResourceId</span></span>
<span data-ttu-id="0c577-219">Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c577-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="0c577-220">-大小</span><span class="sxs-lookup"><span data-stu-id="0c577-220">-Size</span></span>
<span data-ttu-id="0c577-221">以位為單位的 RSA 金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="0c577-221">RSA key size, in bits.</span></span> <span data-ttu-id="0c577-222">如果未指定，服務會提供安全預設值。</span><span class="sxs-lookup"><span data-stu-id="0c577-222">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="0c577-223">-標記</span><span class="sxs-lookup"><span data-stu-id="0c577-223">-Tag</span></span>
<span data-ttu-id="0c577-224">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="0c577-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c577-225">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0c577-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0c577-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0c577-226">-VaultName</span></span>
<span data-ttu-id="0c577-227">指定此 Cmdlet 新增該金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0c577-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="0c577-228">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0c577-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0c577-229">-確認</span><span class="sxs-lookup"><span data-stu-id="0c577-229">-Confirm</span></span>
<span data-ttu-id="0c577-230">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0c577-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c577-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c577-231">-WhatIf</span></span>
<span data-ttu-id="0c577-232">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c577-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c577-233">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c577-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c577-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c577-234">CommonParameters</span></span>
<span data-ttu-id="0c577-235">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c577-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c577-236">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c577-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c577-237">輸入</span><span class="sxs-lookup"><span data-stu-id="0c577-237">INPUTS</span></span>

### <span data-ttu-id="0c577-238">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0c577-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0c577-239">System.String</span><span class="sxs-lookup"><span data-stu-id="0c577-239">System.String</span></span>

## <span data-ttu-id="0c577-240">輸出</span><span class="sxs-lookup"><span data-stu-id="0c577-240">OUTPUTS</span></span>

### <span data-ttu-id="0c577-241">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c577-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="0c577-242">筆記</span><span class="sxs-lookup"><span data-stu-id="0c577-242">NOTES</span></span>

## <span data-ttu-id="0c577-243">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c577-243">RELATED LINKS</span></span>

[<span data-ttu-id="0c577-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c577-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="0c577-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c577-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="0c577-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c577-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

