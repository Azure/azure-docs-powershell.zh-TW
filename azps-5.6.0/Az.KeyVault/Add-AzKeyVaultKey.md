---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b853e688330eda17f037381fc5105626e16d93fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902570"
---
# <span data-ttu-id="4a6bb-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="4a6bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4a6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6bb-103">在金鑰庫中建立金鑰，或將金鑰導入到金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="4a6bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="4a6bb-104">SYNTAX</span></span>

### <span data-ttu-id="4a6bb-105">InteractiveCreate (預設) </span><span class="sxs-lookup"><span data-stu-id="4a6bb-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="4a6bb-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="4a6bb-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="4a6bb-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="4a6bb-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="4a6bb-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="4a6bb-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="4a6bb-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="4a6bb-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="4a6bb-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="4a6bb-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6bb-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="4a6bb-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a6bb-117">描述</span><span class="sxs-lookup"><span data-stu-id="4a6bb-117">DESCRIPTION</span></span>
<span data-ttu-id="4a6bb-118">**Add-AzKeyVaultKey** Cmdlet 在 Azure 金鑰庫的金鑰庫中建立金鑰，或將金鑰導入金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="4a6bb-119">使用此 Cmdlet 使用下列任一方法新增金鑰：</span><span class="sxs-lookup"><span data-stu-id="4a6bb-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="4a6bb-120">在金鑰庫服務中的 HSM (中) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="4a6bb-121">在 Key Vault 服務的軟體中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="4a6bb-122">從您自己的硬體安全性模組將金鑰 (HSM) 金鑰庫服務中的 HSMS。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="4a6bb-123">從您電腦的 .pfx 檔案中輸入金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="4a6bb-124">將您電腦的 .pfx 檔案中的金鑰， (金鑰保存庫服務) HSMS 中的硬體安全性模組。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="4a6bb-125">針對任何這些作業，您可以提供重要屬性或接受預設設定。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="4a6bb-126">如果您建立或導入的金鑰與金鑰庫中現有金鑰的名稱相同，原始金鑰會以您為新金鑰指定的值更新。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="4a6bb-127">您可以使用該金鑰版本的特定 URI 存取先前的值。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="4a6bb-128">若要瞭解金鑰版本和 URI 結構，請參閱[](http://go.microsoft.com/fwlink/?linkid=518560)Key Vault REST API 檔中關於金鑰和秘訣的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="4a6bb-129">注意：若要從您自己的硬體安全性模組中輸入金鑰，您必須先使用 Azure Key Vault BYOK 工具集 (產生副檔名為 .byok 的檔案) BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="4a6bb-130">詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="4a6bb-131">最佳做法是在建立或更新金鑰之後，使用 Backup-AzKeyVaultKey備份。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="4a6bb-132">沒有取消刪除的功能，因此如果您不小心刪除或刪除金鑰，然後改變心意，除非您有可還原的備份，否則無法復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="4a6bb-133">例子</span><span class="sxs-lookup"><span data-stu-id="4a6bb-133">EXAMPLES</span></span>

### <span data-ttu-id="4a6bb-134">範例 1：建立金鑰</span><span class="sxs-lookup"><span data-stu-id="4a6bb-134">Example 1: Create a key</span></span>
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

<span data-ttu-id="4a6bb-135">此命令在名為 Contoso 的金鑰庫中，建立一個名為 ITSoftware 的軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="4a6bb-136">範例 2：建立受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="4a6bb-136">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="4a6bb-137">此命令在名為 Contoso 的金鑰庫中建立受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="4a6bb-138">範例 3：建立具有非預設值的金鑰</span><span class="sxs-lookup"><span data-stu-id="4a6bb-138">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="4a6bb-139">第一個命令會儲存值解密，並在$KeyOperations驗證。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="4a6bb-140">第二個命令會使用 **Get-Date** Cmdlet 建立以 UTC 定義的 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="4a6bb-141">該物件會指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="4a6bb-142">命令會儲存該日期至$Expires變數。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="4a6bb-143">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="4a6bb-144">第三個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4a6bb-145">該物件會指定目前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-145">That object specifies current UTC time.</span></span> <span data-ttu-id="4a6bb-146">命令會儲存該日期至$NotBefore變數。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="4a6bb-147">最後一個命令會建立名為 ITOnnonDefault 的金鑰，該金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="4a6bb-148">該命令會指定儲存于其中之允許之金鑰作業$KeyOperations。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="4a6bb-149">命令會指定在先前命令中建立之 *到期* 和 *NotBefore* 參數的時間，以及高嚴重性和 IT 的標記。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="4a6bb-150">新金鑰已停用。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-150">The new key is disabled.</span></span> <span data-ttu-id="4a6bb-151">您可以使用 **Set-AzKeyVaultKey** Cmdlet 來啟用。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="4a6bb-152">範例 4：匯出受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="4a6bb-152">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="4a6bb-153">此命令會從 KeyFilePath 參數指定的位置，將 *名為 ITByok* 的金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="4a6bb-154">所輸入的金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="4a6bb-155">若要從您自己的硬體安全性模組中輸入金鑰，您必須先使用 Azure Key Vault BYOK 工具集 (以 .byok 副檔名) 的檔案產生 BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="4a6bb-156">詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="4a6bb-157">範例 5：匯出軟體保護金鑰</span><span class="sxs-lookup"><span data-stu-id="4a6bb-157">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="4a6bb-158">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="4a6bb-159">如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="4a6bb-160">第二個命令在 Contoso 金鑰保存庫中建立軟體密碼。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="4a6bb-161">命令會指定金鑰的位置，以及儲存在$Password。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="4a6bb-162">範例 6：輸入金鑰並指派屬性</span><span class="sxs-lookup"><span data-stu-id="4a6bb-162">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="4a6bb-163">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="4a6bb-164">第二個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件，然後將該物件儲存在$Expires變數中。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="4a6bb-165">第三個命令會建立$tags變數，以設定高嚴重性和 IT 的標記。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="4a6bb-166">最後一個命令會從指定位置將金鑰輸入為 HSM 鍵。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="4a6bb-167">命令會指定儲存在 $Expires 中的到期日和密碼$Password，並適用儲存在 $tags 中的標記。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="4a6bb-168">範例 7：產生 KEY Exchange 金鑰 (KEK) for "bring your own key" (BYOK) 功能</span><span class="sxs-lookup"><span data-stu-id="4a6bb-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="4a6bb-169">產生稱為 KEY Exchange (KEY Exchange 鍵 (KEK) ) 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="4a6bb-170">KEK 必須是只包含導入金鑰作業的 RSA-HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="4a6bb-171">只有 Key Vault Premium SKU 支援 RSA-HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="4a6bb-172">如需詳細資料，請參閱 https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="4a6bb-172">For more details please refer to https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="4a6bb-173">參數</span><span class="sxs-lookup"><span data-stu-id="4a6bb-173">PARAMETERS</span></span>

### <span data-ttu-id="4a6bb-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="4a6bb-174">-CurveName</span></span>
<span data-ttu-id="4a6bb-175">指定省略號曲線密碼法的曲線名稱，當 KeyType 為 EC 時，此值即為有效。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6bb-176">-DefaultProfile</span></span>
<span data-ttu-id="4a6bb-177">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4a6bb-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a6bb-178">-目的地</span><span class="sxs-lookup"><span data-stu-id="4a6bb-178">-Destination</span></span>
<span data-ttu-id="4a6bb-179">指定是否要在 Key Vault 服務中將金鑰新增為受軟體保護的金鑰或 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="4a6bb-180">有效的值為：HSM 和 Software。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="4a6bb-181">注意：若要使用 HSM 做為目的地，您必須有支援 HSMS 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="4a6bb-182">有關 Azure 金鑰庫的服務層級和功能的詳細資訊，請參閱 [Azure 金鑰庫定價網站](http://go.microsoft.com/fwlink/?linkid=512521)。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="4a6bb-183">當您建立新金鑰時，需要此參數。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="4a6bb-184">如果您使用 *KeyFilePath* 參數來輸入金鑰，此參數為選擇性：</span><span class="sxs-lookup"><span data-stu-id="4a6bb-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="4a6bb-185">如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .byok 的金鑰，它會以 HSM 保護金鑰來輸入該金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="4a6bb-186">Cmdlet 無法將該金鑰以軟體保護金鑰進行導入。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="4a6bb-187">如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .pfx 的金鑰，它會將金鑰以軟體保護金鑰導入。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="4a6bb-188">-停用</span><span class="sxs-lookup"><span data-stu-id="4a6bb-188">-Disable</span></span>
<span data-ttu-id="4a6bb-189">表示您新增的金鑰已設定為初始停用狀態。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="4a6bb-190">任何使用金鑰的嘗試都會失敗。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="4a6bb-191">如果您要預先載入要稍後啟用的金鑰，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="4a6bb-192">-到期</span><span class="sxs-lookup"><span data-stu-id="4a6bb-192">-Expires</span></span>
<span data-ttu-id="4a6bb-193">指定此 Cmdlet 新增之金鑰的到期日 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="4a6bb-194">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="4a6bb-195">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4a6bb-196">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="4a6bb-197">如果您未指定此參數，金鑰不會過期。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-197">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="4a6bb-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="4a6bb-198">-HsmName</span></span>
<span data-ttu-id="4a6bb-199">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-199">HSM name.</span></span> <span data-ttu-id="4a6bb-200">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="4a6bb-201">-HsmObject</span></span>
<span data-ttu-id="4a6bb-202">HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6bb-203">-HsmResourceId</span></span>
<span data-ttu-id="4a6bb-204">HSM 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a6bb-205">-InputObject</span></span>
<span data-ttu-id="4a6bb-206">Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-206">Vault object.</span></span>

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

### <span data-ttu-id="4a6bb-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="4a6bb-207">-KeyFilePassword</span></span>
<span data-ttu-id="4a6bb-208">將所輸入檔案的密碼指定為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="4a6bb-209">若要取得 **SecureString 物件** ，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="4a6bb-210">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="4a6bb-211">您必須指定此密碼，才能使用 .pfx 副檔名來輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="4a6bb-212">-KeyFilePath</span></span>
<span data-ttu-id="4a6bb-213">指定包含此 Cmdlet 所導入之重要資料之本地檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="4a6bb-214">有效的副檔名為 .byok 和 .pfx。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="4a6bb-215">如果檔案是 .byok 檔案，該金鑰會在進行匯出後自動受到 HSMS 保護，而且您無法覆蓋此預設值。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="4a6bb-216">如果檔案是 .pfx 檔案，則金鑰會在匯出後自動受到軟體保護。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="4a6bb-217">若要覆蓋此預設值，將 *Destination* 參數設定為 HSM，讓金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="4a6bb-218">當您指定此參數時 *，Destination* 參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="4a6bb-219">-KeyOps</span></span>
<span data-ttu-id="4a6bb-220">指定可以使用此 Cmdlet 新增的金鑰執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="4a6bb-221">如果您未指定此參數，可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="4a6bb-222">此參數可接受的值是 JSON Web Key ([JWK](http://go.microsoft.com/fwlink/?LinkID=613300)) 定義之金鑰作業的逗號分隔清單：</span><span class="sxs-lookup"><span data-stu-id="4a6bb-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="4a6bb-223">加密</span><span class="sxs-lookup"><span data-stu-id="4a6bb-223">encrypt</span></span>
- <span data-ttu-id="4a6bb-224">解密</span><span class="sxs-lookup"><span data-stu-id="4a6bb-224">decrypt</span></span>
- <span data-ttu-id="4a6bb-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-225">wrapKey</span></span>
- <span data-ttu-id="4a6bb-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-226">unwrapKey</span></span>
- <span data-ttu-id="4a6bb-227">標誌</span><span class="sxs-lookup"><span data-stu-id="4a6bb-227">sign</span></span>
- <span data-ttu-id="4a6bb-228">驗證</span><span class="sxs-lookup"><span data-stu-id="4a6bb-228">verify</span></span>
- <span data-ttu-id="4a6bb-229">僅 (KEK 的匯出資料，請參閱範例 7) </span><span class="sxs-lookup"><span data-stu-id="4a6bb-229">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="4a6bb-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4a6bb-230">-KeyType</span></span>
<span data-ttu-id="4a6bb-231">指定此金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-231">Specifies the key type of this key.</span></span> <span data-ttu-id="4a6bb-232">在輸入 BYOK 金鑰時，預設為 "RSA"。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-232">When importing BYOK keys, it defaults to 'RSA'.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-233">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a6bb-233">-Name</span></span>
<span data-ttu-id="4a6bb-234">指定要新加到金鑰庫的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-234">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="4a6bb-235">此 Cmdlet 會依據此參數指定的名稱、金鑰庫名稱，以及您目前的環境，建構金鑰的完全限定功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-235">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="4a6bb-236">名稱必須是長度為 1 到 63 個字元的字串，只包含 0-9、a-z、A-Z 和 - (破折號) 。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-236">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="4a6bb-237">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="4a6bb-237">-NotBefore</span></span>
<span data-ttu-id="4a6bb-238">指定無法使用金鑰的時間 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-238">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="4a6bb-239">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-239">This parameter uses UTC.</span></span> <span data-ttu-id="4a6bb-240">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-240">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4a6bb-241">如果您未指定此參數，可以立即使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-241">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="4a6bb-242">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6bb-242">-ResourceId</span></span>
<span data-ttu-id="4a6bb-243">Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-243">Vault Resource Id.</span></span>

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

### <span data-ttu-id="4a6bb-244">-大小</span><span class="sxs-lookup"><span data-stu-id="4a6bb-244">-Size</span></span>
<span data-ttu-id="4a6bb-245">以位為單位的 RSA 金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-245">RSA key size, in bits.</span></span> <span data-ttu-id="4a6bb-246">如果未指定，服務會提供安全預設值。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-246">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6bb-247">-標記</span><span class="sxs-lookup"><span data-stu-id="4a6bb-247">-Tag</span></span>
<span data-ttu-id="4a6bb-248">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-248">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4a6bb-249">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4a6bb-249">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4a6bb-250">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4a6bb-250">-VaultName</span></span>
<span data-ttu-id="4a6bb-251">指定此 Cmdlet 新增該金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-251">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="4a6bb-252">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-252">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="4a6bb-253">-確認</span><span class="sxs-lookup"><span data-stu-id="4a6bb-253">-Confirm</span></span>
<span data-ttu-id="4a6bb-254">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a6bb-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a6bb-255">-WhatIf</span></span>
<span data-ttu-id="4a6bb-256">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-256">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a6bb-257">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a6bb-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6bb-258">CommonParameters</span></span>
<span data-ttu-id="4a6bb-259">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4a6bb-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6bb-260">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a6bb-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6bb-261">輸入</span><span class="sxs-lookup"><span data-stu-id="4a6bb-261">INPUTS</span></span>

### <span data-ttu-id="4a6bb-262">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4a6bb-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4a6bb-263">System.String</span><span class="sxs-lookup"><span data-stu-id="4a6bb-263">System.String</span></span>

## <span data-ttu-id="4a6bb-264">輸出</span><span class="sxs-lookup"><span data-stu-id="4a6bb-264">OUTPUTS</span></span>

### <span data-ttu-id="4a6bb-265">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="4a6bb-266">筆記</span><span class="sxs-lookup"><span data-stu-id="4a6bb-266">NOTES</span></span>

## <span data-ttu-id="4a6bb-267">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a6bb-267">RELATED LINKS</span></span>

[<span data-ttu-id="4a6bb-268">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-268">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="4a6bb-269">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-269">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="4a6bb-270">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4a6bb-270">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="4a6bb-271">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="4a6bb-271">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
