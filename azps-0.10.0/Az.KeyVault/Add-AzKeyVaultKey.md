---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795562"
---
# Add-AzKeyVaultKey

## 摘要
在金鑰保存庫中建立金鑰或將金鑰匯入到金鑰保存庫中。

## 句法

### 建立 (預設) 
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Import
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
AzKeyVaultKey Cmdlet 會在 Azure 金鑰保存庫中的金鑰保存庫中建立金鑰，或 **將** 金鑰匯入到金鑰保存庫中。
使用這個 Cmdlet，使用下列任何一種方法來新增金鑰：

- 在硬體安全模組中建立金鑰， (在主要 Vault 服務中的 HSM) 。
- 在金鑰 Vault 服務的軟體中建立金鑰。
- 從您自己的硬體安全模組將金鑰匯入到主要 Vault 服務中 (HSM) 至 Hsm。
- 從您電腦上的 .pfx 檔案匯入金鑰。
- 從您電腦上的 .pfx 檔案將金鑰匯入到 [主要 Vault] 服務中 (Hsm) 的硬體安全模組。

針對這些作業中的任何一個，您可以提供重要屬性或接受預設設定。

如果您在金鑰保存庫中建立或匯入與現有金鑰同名的金鑰，則會使用您為新金鑰指定的值來更新原始金鑰。 您可以使用該版本金鑰的版本特定 URI 來存取先前的值。 若要瞭解主要版本與 URI 結構，請參閱主要保存庫 REST API 檔中的 [ [關於金鑰 andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) ]。

注意：若要從您自己的硬體安全模組匯入金鑰，您必須先使用 Azure Key Vault BYOK 工具集，以) BYOK 副檔名 (的檔案來產生 BYOK 套件。 如需詳細資訊，請參閱 [如何為 Azure 金鑰電子倉庫產生及轉移 HSM-Protected 金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。

最佳做法是使用 Backup-AzKeyVaultKey Cmdlet，在建立或更新金鑰後進行備份。 沒有取消刪除功能，因此如果您不小心刪除或刪除您的金鑰，然後改變主意，除非您有可以還原的備份，否則金鑰是無法復原的。

## 示例

### 範例1：建立索引鍵
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

這個命令會在名為 Contoso 的主要保存庫中，建立名為 ITSoftware 的軟體保護金鑰。

### 範例2：建立受 HSM 保護的金鑰
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

這個命令會在名為 Contoso 的金鑰保存庫中建立受 HSM 保護的金鑰。

### 範例3：使用非預設值建立金鑰
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

第一個命令會儲存在 $KeyOperations 變數中解密和驗證的值。

第二個命令會建立一個 **DateTime** 物件（在 UTC 中定義），方法是使用 [ **取得日期** ] Cmdlet。
該物件指定未來兩年的時間。 該命令會將該日期儲存在 $Expires 變數中。 如需詳細資訊，請輸入 `Get-Help Get-Date` 。

第三個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。 該物件會指定目前的 UTC 時間。 該命令會將該日期儲存在 $NotBefore 變數中。

最後一個命令會建立一個名為 ITHsmNonDefault 的索引鍵，該金鑰是受 HSM 保護的金鑰。 此命令會指定儲存 $KeyOperations 所允許的按鍵作業值。 此命令會指定在前一個命令中建立的 *Expires* 及 *NotBefore* 參數的時間，以及高嚴重性及嚴重度的標記。 新的索引鍵是停用的。 您可以使用 **AzKeyVaultKey** Cmdlet 來啟用它。

### 範例4：匯入受 HSM 保護的金鑰
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

這個命令會從 *KeyFilePath* 參數指定的位置匯入名為 ITByok 的金鑰。 匯入金鑰是受 HSM 保護的金鑰。

若要匯入您自己的硬體安全模組中的金鑰，您必須先使用 Azure 金鑰保存庫 BYOK 工具集，以) BYOK 副檔名 (的檔案來產生 BYOK 套件。
如需詳細資訊，請參閱 [如何為 Azure 金鑰電子倉庫產生及轉移 HSM-Protected 金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。

### 範例5：匯入軟體保護的金鑰
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Password 變數中。 如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。

第二個命令會在 Contoso 金鑰保存庫中建立軟體密碼。 命令會指定儲存在 $Password 的索引鍵和密碼的位置。

### 範例6：匯入金鑰並指派屬性
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Password 變數中。

第二個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件，然後將該物件儲存在 $Expires 變數中。

第三個命令會建立 $tags 變數，以設定高嚴重性及它的標記。

最終的命令會將金鑰從指定的位置匯入為 HSM 金鑰。 此命令會指定儲存在 $Password 中的 $Expires 和密碼儲存的到期時間，並套用 $tags 中儲存的標籤。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -目的地
指定是否要在金鑰保存庫服務中，將金鑰新增為軟體保護金鑰或受 HSM 保護的金鑰。
有效值為： HSM 和軟體。

注意：若要使用 HSM 作為目的地，您必須擁有支援 Hsm 的金鑰保存庫。 如需有關 Azure 金鑰保存庫之服務層級和功能的詳細資訊，請參閱 [Azure 金鑰保存庫定價網站](http://go.microsoft.com/fwlink/?linkid=512521)。

當您建立新的金鑰時，這個參數是必要的。 如果您使用 *KeyFilePath* 參數匯入金鑰，則此參數為 optional （選用）：

- 如果您沒有指定此參數，且這個 Cmdlet 會匯入副檔名為 byok 的金鑰，它會將該金鑰匯入為受 HSM 保護的金鑰。 Cmdlet 無法將該金鑰匯入為軟體保護的金鑰。

- 如果您沒有指定此參數，且這個 Cmdlet 會匯入副檔名為 .pfx 的金鑰，它會將金鑰匯入為軟體保護金鑰。

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

### -停用
表示您要新增的金鑰已設定為 [已停用] 的初始狀態。 任何使用金鑰的嘗試都將失敗。 如果您正在預載入您想要稍後啟用的金鑰，請使用此參數。

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

### -到期
指定此 Cmdlet 所新增之金鑰的到期時間（作為 **DateTime** 物件）。 此參數使用協調通用時間 (UTC) 。 若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。 如需詳細資訊，請輸入 `Get-Help Get-Date` 。 如果您沒有指定此參數，金鑰就不會過期。

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

### -KeyFilePassword
指定匯入檔案的密碼做為 **SecureString** 物件。 若要取得 **SecureString** 物件，請使用 **ConvertTo-SecureString** Cmdlet。 如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。 您必須指定此密碼才能匯入副檔名為 .pfx 的檔案。

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

### -KeyFilePath
指定本機檔案的路徑，該檔案內含這個 Cmdlet 所匯入的重要材料。
有效的檔案名副檔名為 byok 和 .pfx。

- 如果檔案是 byok 檔案，則在匯入之後，金鑰會自動受 Hsm 保護，而且您無法覆寫此預設值。

- 如果檔案是 .pfx 檔案，則在匯入之後，該金鑰會自動受到軟體的保護。 若要覆寫此預設值，請將 *Destination* 參數設定為 hsm，讓金鑰受 HSM 保護。

當您指定此參數時， *Destination* 參數是選擇性的。

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

### -KeyOps
指定可使用這個 Cmdlet 所新增之金鑰來執行的作業陣列。
如果您沒有指定此參數，則可以執行所有作業。

此參數可接受的值是由 [JSON Web 金鑰 (JWK) 規格](http://go.microsoft.com/fwlink/?LinkID=613300)所定義的以逗號分隔的主要動作清單：

- 進行
- 對
- 浮
- 解
- 母音
- 是否

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

### -名稱
指定要新增到 [主要電子倉庫] 的索引鍵名。 這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。 名稱必須是1到63個字元的字串，長度只包含0-9、a-z、A-z，並 (破折號) 符號。

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

### -NotBefore
指定時間（作為 **DateTime** 物件），在此之後就不能使用該索引鍵。 此參數使用 UTC。 若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。 如果您沒有指定此參數，就可以立即使用金鑰。

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

### -Tag
雜湊資料表形式的索引鍵/值對。 例如：

@ {key0 = "value0"; key1 = $null; key2 = "value2"}

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

### -VaultName
指定此 Cmdlet 要在其中新增金鑰的主要保存庫的名稱。 這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。

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

### -確認
在執行 Cmdlet 之前提示您進行確認。

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

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### KeyBundle 中的 KeyVault。

## 筆記

## 相關連結

[備份-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[移除-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
