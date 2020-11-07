---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7af5afeac742bf9d256ac16470af0169170eb1e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799910"
---
# <span data-ttu-id="ad35f-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad35f-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="ad35f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad35f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad35f-103">在金鑰保存庫中建立金鑰或將金鑰匯入到金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad35f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad35f-104">SYNTAX</span></span>

### <span data-ttu-id="ad35f-105">建立 (預設) </span><span class="sxs-lookup"><span data-stu-id="ad35f-105">Create (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad35f-106">Import</span><span class="sxs-lookup"><span data-stu-id="ad35f-106">Import</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad35f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad35f-107">DESCRIPTION</span></span>
<span data-ttu-id="ad35f-108">AzureKeyVaultKey Cmdlet 會在 Azure 金鑰保存庫中的金鑰保存庫中建立金鑰，或 **將** 金鑰匯入到金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-108">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="ad35f-109">使用這個 Cmdlet，使用下列任何一種方法來新增金鑰：</span><span class="sxs-lookup"><span data-stu-id="ad35f-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="ad35f-110">在硬體安全模組中建立金鑰， (在主要 Vault 服務中的 HSM) 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="ad35f-111">在金鑰 Vault 服務的軟體中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="ad35f-112">從您自己的硬體安全模組將金鑰匯入到主要 Vault 服務中 (HSM) 至 Hsm。</span><span class="sxs-lookup"><span data-stu-id="ad35f-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="ad35f-113">從您電腦上的 .pfx 檔案匯入金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="ad35f-114">從您電腦上的 .pfx 檔案將金鑰匯入到 [主要 Vault] 服務中 (Hsm) 的硬體安全模組。</span><span class="sxs-lookup"><span data-stu-id="ad35f-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="ad35f-115">針對這些作業中的任何一個，您可以提供重要屬性或接受預設設定。</span><span class="sxs-lookup"><span data-stu-id="ad35f-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="ad35f-116">如果您在金鑰保存庫中建立或匯入與現有金鑰同名的金鑰，則會使用您為新金鑰指定的值來更新原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="ad35f-117">您可以使用該版本金鑰的版本特定 URI 來存取先前的值。</span><span class="sxs-lookup"><span data-stu-id="ad35f-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="ad35f-118">若要瞭解主要版本與 URI 結構，請參閱主要保存庫 REST API 檔中的 [ [關於金鑰 andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) ]。</span><span class="sxs-lookup"><span data-stu-id="ad35f-118">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="ad35f-119">注意：若要從您自己的硬體安全模組匯入金鑰，您必須先使用 Azure Key Vault BYOK 工具集，以) BYOK 副檔名 (的檔案來產生 BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="ad35f-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="ad35f-120">如需詳細資訊，請參閱 [如何為 Azure 金鑰電子倉庫產生及轉移 HSM-Protected 金鑰](https://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="ad35f-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="ad35f-121">最佳做法是使用 Backup-AzureKeyVaultKey Cmdlet，在建立或更新金鑰後進行備份。</span><span class="sxs-lookup"><span data-stu-id="ad35f-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="ad35f-122">沒有取消刪除功能，因此如果您不小心刪除或刪除您的金鑰，然後改變主意，除非您有可以還原的備份，否則金鑰是無法復原的。</span><span class="sxs-lookup"><span data-stu-id="ad35f-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="ad35f-123">示例</span><span class="sxs-lookup"><span data-stu-id="ad35f-123">EXAMPLES</span></span>

### <span data-ttu-id="ad35f-124">範例1：建立索引鍵</span><span class="sxs-lookup"><span data-stu-id="ad35f-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="ad35f-125">這個命令會在名為 Contoso 的主要保存庫中，建立名為 ITSoftware 的軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="ad35f-126">範例2：建立受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="ad35f-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="ad35f-127">這個命令會在名為 Contoso 的金鑰保存庫中建立受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="ad35f-128">範例3：使用非預設值建立金鑰</span><span class="sxs-lookup"><span data-stu-id="ad35f-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="ad35f-129">第一個命令會儲存在 $KeyOperations 變數中解密和驗證的值。</span><span class="sxs-lookup"><span data-stu-id="ad35f-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="ad35f-130">第二個命令會建立一個 **DateTime** 物件（在 UTC 中定義），方法是使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad35f-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ad35f-131">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="ad35f-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="ad35f-132">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="ad35f-133">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="ad35f-134">第三個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="ad35f-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ad35f-135">該物件會指定目前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="ad35f-135">That object specifies current UTC time.</span></span> <span data-ttu-id="ad35f-136">該命令會將該日期儲存在 $NotBefore 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="ad35f-137">最後一個命令會建立一個名為 ITHsmNonDefault 的索引鍵，該金鑰是受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="ad35f-138">此命令會指定儲存 $KeyOperations 所允許的按鍵作業值。</span><span class="sxs-lookup"><span data-stu-id="ad35f-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="ad35f-139">此命令會指定在前一個命令中建立的 *Expires* 及 *NotBefore* 參數的時間，以及高嚴重性及嚴重度的標記。</span><span class="sxs-lookup"><span data-stu-id="ad35f-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="ad35f-140">新的索引鍵是停用的。</span><span class="sxs-lookup"><span data-stu-id="ad35f-140">The new key is disabled.</span></span> <span data-ttu-id="ad35f-141">您可以使用 **AzureKeyVaultKey** Cmdlet 來啟用它。</span><span class="sxs-lookup"><span data-stu-id="ad35f-141">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="ad35f-142">範例4：匯入受 HSM 保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="ad35f-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="ad35f-143">這個命令會從 *KeyFilePath* 參數指定的位置匯入名為 ITByok 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="ad35f-144">匯入金鑰是受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="ad35f-145">若要匯入您自己的硬體安全模組中的金鑰，您必須先使用 Azure 金鑰保存庫 BYOK 工具集，以) BYOK 副檔名 (的檔案來產生 BYOK 套件。</span><span class="sxs-lookup"><span data-stu-id="ad35f-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="ad35f-146">如需詳細資訊，請參閱 [如何為 Azure 金鑰電子倉庫產生及轉移 HSM-Protected 金鑰](https://go.microsoft.com/fwlink/?LinkId=522252)。</span><span class="sxs-lookup"><span data-stu-id="ad35f-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="ad35f-147">範例5：匯入軟體保護的金鑰</span><span class="sxs-lookup"><span data-stu-id="ad35f-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="ad35f-148">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="ad35f-149">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="ad35f-150">第二個命令會在 Contoso 金鑰保存庫中建立軟體密碼。</span><span class="sxs-lookup"><span data-stu-id="ad35f-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="ad35f-151">命令會指定儲存在 $Password 的索引鍵和密碼的位置。</span><span class="sxs-lookup"><span data-stu-id="ad35f-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="ad35f-152">範例6：匯入金鑰並指派屬性</span><span class="sxs-lookup"><span data-stu-id="ad35f-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="ad35f-153">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="ad35f-154">第二個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件，然後將該物件儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad35f-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="ad35f-155">第三個命令會建立 $tags 變數，以設定高嚴重性及它的標記。</span><span class="sxs-lookup"><span data-stu-id="ad35f-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="ad35f-156">最終的命令會將金鑰從指定的位置匯入為 HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="ad35f-157">此命令會指定儲存在 $Password 中的 $Expires 和密碼儲存的到期時間，並套用 $tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="ad35f-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="ad35f-158">參數</span><span class="sxs-lookup"><span data-stu-id="ad35f-158">PARAMETERS</span></span>

### <span data-ttu-id="ad35f-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad35f-159">-DefaultProfile</span></span>
<span data-ttu-id="ad35f-160">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ad35f-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-161">-目的地</span><span class="sxs-lookup"><span data-stu-id="ad35f-161">-Destination</span></span>
<span data-ttu-id="ad35f-162">指定是否要在金鑰保存庫服務中，將金鑰新增為軟體保護金鑰或受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="ad35f-163">有效值為： HSM 和軟體。</span><span class="sxs-lookup"><span data-stu-id="ad35f-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="ad35f-164">注意：若要使用 HSM 作為目的地，您必須擁有支援 Hsm 的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="ad35f-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="ad35f-165">如需有關 Azure 金鑰保存庫之服務層級和功能的詳細資訊，請參閱 [Azure 金鑰保存庫定價網站](https://go.microsoft.com/fwlink/?linkid=512521)。</span><span class="sxs-lookup"><span data-stu-id="ad35f-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="ad35f-166">當您建立新的金鑰時，這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ad35f-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="ad35f-167">如果您使用 *KeyFilePath* 參數匯入金鑰，則此參數為 optional （選用）：</span><span class="sxs-lookup"><span data-stu-id="ad35f-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="ad35f-168">如果您沒有指定此參數，且這個 Cmdlet 會匯入副檔名為 byok 的金鑰，它會將該金鑰匯入為受 HSM 保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="ad35f-169">Cmdlet 無法將該金鑰匯入為軟體保護的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="ad35f-170">如果您沒有指定此參數，且這個 Cmdlet 會匯入副檔名為 .pfx 的金鑰，它會將金鑰匯入為軟體保護金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-171">-停用</span><span class="sxs-lookup"><span data-stu-id="ad35f-171">-Disable</span></span>
<span data-ttu-id="ad35f-172">表示您要新增的金鑰已設定為 [已停用] 的初始狀態。</span><span class="sxs-lookup"><span data-stu-id="ad35f-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="ad35f-173">任何使用金鑰的嘗試都將失敗。</span><span class="sxs-lookup"><span data-stu-id="ad35f-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="ad35f-174">如果您正在預載入您想要稍後啟用的金鑰，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="ad35f-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-175">-到期</span><span class="sxs-lookup"><span data-stu-id="ad35f-175">-Expires</span></span>
<span data-ttu-id="ad35f-176">指定此 Cmdlet 所新增之金鑰的到期時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="ad35f-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="ad35f-177">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="ad35f-178">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad35f-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ad35f-179">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="ad35f-180">如果您沒有指定此參數，金鑰就不會過期。</span><span class="sxs-lookup"><span data-stu-id="ad35f-180">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="ad35f-181">-KeyFilePassword</span></span>
<span data-ttu-id="ad35f-182">指定匯入檔案的密碼做為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="ad35f-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="ad35f-183">若要取得 **SecureString** 物件，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad35f-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="ad35f-184">如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="ad35f-185">您必須指定此密碼才能匯入副檔名為 .pfx 的檔案。</span><span class="sxs-lookup"><span data-stu-id="ad35f-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="ad35f-186">-KeyFilePath</span></span>
<span data-ttu-id="ad35f-187">指定本機檔案的路徑，該檔案內含這個 Cmdlet 所匯入的重要材料。</span><span class="sxs-lookup"><span data-stu-id="ad35f-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="ad35f-188">有效的檔案名副檔名為 byok 和 .pfx。</span><span class="sxs-lookup"><span data-stu-id="ad35f-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="ad35f-189">如果檔案是 byok 檔案，則在匯入之後，金鑰會自動受 Hsm 保護，而且您無法覆寫此預設值。</span><span class="sxs-lookup"><span data-stu-id="ad35f-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="ad35f-190">如果檔案是 .pfx 檔案，則在匯入之後，該金鑰會自動受到軟體的保護。</span><span class="sxs-lookup"><span data-stu-id="ad35f-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="ad35f-191">若要覆寫此預設值，請將 *Destination* 參數設定為 hsm，讓金鑰受 HSM 保護。</span><span class="sxs-lookup"><span data-stu-id="ad35f-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="ad35f-192">當您指定此參數時， *Destination* 參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ad35f-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="ad35f-193">-KeyOps</span></span>
<span data-ttu-id="ad35f-194">指定可使用這個 Cmdlet 所新增之金鑰來執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="ad35f-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="ad35f-195">如果您沒有指定此參數，則可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="ad35f-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="ad35f-196">此參數可接受的值是由 [JSON Web 金鑰 (JWK) 規格](https://go.microsoft.com/fwlink/?LinkID=613300)所定義的以逗號分隔的主要動作清單：</span><span class="sxs-lookup"><span data-stu-id="ad35f-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="ad35f-197">進行</span><span class="sxs-lookup"><span data-stu-id="ad35f-197">Encrypt</span></span>
- <span data-ttu-id="ad35f-198">對</span><span class="sxs-lookup"><span data-stu-id="ad35f-198">Decrypt</span></span>
- <span data-ttu-id="ad35f-199">浮</span><span class="sxs-lookup"><span data-stu-id="ad35f-199">Wrap</span></span>
- <span data-ttu-id="ad35f-200">解</span><span class="sxs-lookup"><span data-stu-id="ad35f-200">Unwrap</span></span>
- <span data-ttu-id="ad35f-201">母音</span><span class="sxs-lookup"><span data-stu-id="ad35f-201">Sign</span></span>
- <span data-ttu-id="ad35f-202">是否</span><span class="sxs-lookup"><span data-stu-id="ad35f-202">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-203">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad35f-203">-Name</span></span>
<span data-ttu-id="ad35f-204">指定要新增到 [主要電子倉庫] 的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="ad35f-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="ad35f-205">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="ad35f-206">名稱必須是1到63個字元的字串，長度只包含0-9、a-z、A-z，並 (破折號) 符號。</span><span class="sxs-lookup"><span data-stu-id="ad35f-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ad35f-207">-NotBefore</span></span>
<span data-ttu-id="ad35f-208">指定時間（作為 **DateTime** 物件），在此之後就不能使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ad35f-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="ad35f-209">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="ad35f-209">This parameter uses UTC.</span></span> <span data-ttu-id="ad35f-210">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad35f-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ad35f-211">如果您沒有指定此參數，就可以立即使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad35f-211">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-212">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad35f-212">-Tag</span></span>
<span data-ttu-id="ad35f-213">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ad35f-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ad35f-214">例如：</span><span class="sxs-lookup"><span data-stu-id="ad35f-214">For example:</span></span>

<span data-ttu-id="ad35f-215">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ad35f-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ad35f-216">-VaultName</span></span>
<span data-ttu-id="ad35f-217">指定此 Cmdlet 要在其中新增金鑰的主要保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad35f-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="ad35f-218">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ad35f-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-219">-確認</span><span class="sxs-lookup"><span data-stu-id="ad35f-219">-Confirm</span></span>
<span data-ttu-id="ad35f-220">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad35f-220">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad35f-221">-WhatIf</span></span>
<span data-ttu-id="ad35f-222">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad35f-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad35f-223">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad35f-223">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad35f-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad35f-224">CommonParameters</span></span>
<span data-ttu-id="ad35f-225">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad35f-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad35f-226">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad35f-226">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad35f-227">輸入</span><span class="sxs-lookup"><span data-stu-id="ad35f-227">INPUTS</span></span>

## <span data-ttu-id="ad35f-228">輸出</span><span class="sxs-lookup"><span data-stu-id="ad35f-228">OUTPUTS</span></span>

### <span data-ttu-id="ad35f-229">KeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ad35f-229">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="ad35f-230">筆記</span><span class="sxs-lookup"><span data-stu-id="ad35f-230">NOTES</span></span>

## <span data-ttu-id="ad35f-231">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad35f-231">RELATED LINKS</span></span>

[<span data-ttu-id="ad35f-232">備份-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad35f-232">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="ad35f-233">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad35f-233">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="ad35f-234">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad35f-234">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="ad35f-235">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="ad35f-235">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
