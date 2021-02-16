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
# Add-AzKeyVaultKey

## 簡介
在金鑰庫中建立金鑰，或將金鑰導入到金鑰庫。

## 語法

### InteractiveCreate (預設) 
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Add-AzKeyVaultKey** Cmdlet 在 Azure 金鑰庫的金鑰庫中建立金鑰，或將金鑰導入金鑰庫。
使用此 Cmdlet 使用下列任一方法新增金鑰：
- 在金鑰庫服務 (HSM) 中建立金鑰。
- 在 Key Vault 服務的軟體中建立金鑰。
- 從您自己的硬體安全性模組將金鑰 (HSM) 金鑰庫服務中的 HSMS。
- 從您電腦的 .pfx 檔案中輸入金鑰。
- 將您電腦的 .pfx 檔案中的金鑰， (金鑰保存庫服務) HSMS 中的硬體安全性模組。
針對這些作業，您可以提供重要屬性或接受預設設定。
如果您建立或導入的金鑰與金鑰庫中現有金鑰的名稱相同，原始金鑰會以您為新金鑰指定的值更新。 您可以使用該金鑰版本的特定 URI 存取先前的值。 若要瞭解金鑰版本和 URI 結構，請參閱[](http://go.microsoft.com/fwlink/?linkid=518560)Key Vault REST API 檔中有關金鑰和秘訣的資訊。
注意：若要從您自己的硬體安全性模組中導入金鑰，您必須先使用 Azure Key Vault BYOK 工具集產生具有 .byok 副檔名 (的 BYOK 套件) 檔案。 詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。
最佳做法是在建立或更新金鑰之後，使用 Backup-AzKeyVaultKey備份。 沒有任何取消刪除的功能，因此如果您不小心刪除或刪除金鑰，然後改變心意，除非有可還原的備份，否則無法復原金鑰。

## 例子

### 範例 1：建立金鑰
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

此命令在名為 Contoso 的金鑰庫中，建立一個名為 ITSoftware 的軟體保護金鑰。

### 範例 2：建立受 HSM 保護的金鑰
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

此命令在名為 Contoso 的金鑰庫中建立受 HSM 保護的金鑰。

### 範例 3：建立具有非預設值的金鑰
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

第一個命令會儲存值解密，並在$KeyOperations驗證。
第二個命令會使用 **Get-Date** Cmdlet 建立以 UTC 定義的 **DateTime** 物件。
該物件會指定未來兩年的時間。 命令會儲存該日期至$Expires變數。 如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。
第三個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件。 該物件會指定目前的 UTC 時間。 命令會儲存該日期至$NotBefore變數。
最後一個命令會建立名為 ITHMNonDefault 的金鑰，該金鑰受 HSM 保護。 該命令會指定儲存于其中之允許之金鑰作業$KeyOperations。 命令會指定在先前命令中建立之 *到期* 和 *NotBefore* 參數的時間，以及高嚴重性和 IT 的標記。 新金鑰已停用。 您可以使用 **Set-AzKeyVaultKey** Cmdlet 來啟用。

### 範例 4：匯出受 HSM 保護的金鑰
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

此命令會從 KeyFilePath 參數指定的位置，將 *名為 ITByok* 的金鑰導入。 所導入的金鑰是受 HSM 保護的金鑰。
若要從您自己的硬體安全性模組中輸入金鑰，您必須先使用 Azure Key Vault BYOK 工具集 (產生副檔名為 .byok 的檔案) BYOK 套件。
詳細資訊請參閱如何產生及傳輸 [Azure HSM-Protected金鑰庫的金鑰](http://go.microsoft.com/fwlink/?LinkId=522252)。

### 範例 5：匯出軟體保護金鑰
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

第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。 如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。
第二個命令在 Contoso 金鑰保存庫中建立軟體密碼。 命令會指定金鑰的位置，以及儲存在 $Password。

### 範例 6：輸入金鑰並指派屬性
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

第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Password 變數中。
第二個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件，然後將該物件儲存在$Expires變數中。
第三個命令會建立$tags變數，以設定高嚴重性和 IT 的標記。
最後一個命令會從指定位置將金鑰輸入為 HSM 鍵。 命令會指定儲存在 $Expires 中的到期日和密碼$Password，並適用儲存在 $tags 中的標記。

### 範例 7：產生 KEY Exchange 金鑰 (KEK) FOR "bring your own key" (BYOK) 功能

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

產生稱為 KEY Exchange (KEY Exchange 鍵 (KEK) ) 。 KEK 必須是只包含導入金鑰作業的 RSA-HSM 金鑰。 只有 Key Vault Premium SKU 支援 RSA-HSM 金鑰。
如需詳細資料，請參閱 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -目的地
指定是否要在 Key Vault 服務中將金鑰新增為受軟體保護的金鑰或 HSM 保護的金鑰。
有效的值為：HSM 和 Software。
注意：若要使用 HSM 做為目的地，您必須有支援 HSMS 的金鑰庫。 有關 Azure 金鑰庫的服務層級和功能的詳細資訊，請參閱 [Azure 金鑰庫定價網站](http://go.microsoft.com/fwlink/?linkid=512521)。
當您建立新金鑰時，需要此參數。 如果您使用 *KeyFilePath* 參數來輸入金鑰，此參數為選擇性：
- 如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .byok 的金鑰，它會以 HSM 保護金鑰來輸入該金鑰。 Cmdlet 無法將該金鑰以軟體保護金鑰進行導入。
- 如果您未指定此參數，且此 Cmdlet 會輸入副檔名為 .pfx 的金鑰，它會將金鑰以軟體保護金鑰導入。

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

### -停用
表示您新增的金鑰已設定為初始停用狀態。 任何使用金鑰的嘗試都會失敗。 如果您要預先載入要稍後啟用的金鑰，請使用此參數。

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

### -到期
指定此 Cmdlet 新增之金鑰的到期日 ，做為 **DateTime** 物件。 此參數使用 Utc (協調) 。 若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。 如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。 如果您未指定此參數，金鑰不會過期。

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

### -InputObject
Vault 物件。

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

### -KeyFilePassword
將所輸入檔案的密碼指定為 **SecureString** 物件。 若要取得 **SecureString 物件** ，請使用 **ConvertTo-SecureString** Cmdlet。 如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。 您必須指定此密碼，才能使用 .pfx 副檔名來輸入檔案。

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

### -KeyFilePath
指定包含此 Cmdlet 所導入之重要資料之本地檔案的路徑。
有效的副檔名為 .byok 和 .pfx。
- 如果檔案是 .byok 檔案，則金鑰會在進行匯出後自動受到 HSMS 保護，而且您無法覆蓋此預設值。
- 如果檔案是 .pfx 檔案，則金鑰會在匯出後自動受到軟體保護。 若要覆蓋此預設值，將 *Destination* 參數設定為 HSM，讓金鑰受 HSM 保護。
當您指定此參數時 *，Destination* 參數為選擇性。

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

### -KeyOps
指定可以使用此 Cmdlet 新增的金鑰執行的作業陣列。
如果您未指定此參數，可以執行所有作業。
此參數可接受的值是 JSON Web Key ([JWK](http://go.microsoft.com/fwlink/?LinkID=613300)) 定義之金鑰作業的逗號分隔清單：
- 加密
- 解密
- wrapKey
- unwrapKey
- 標誌
- 驗證
- 僅 (KEK 的匯出資料，請參閱範例 7) 

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

### -名稱
指定要新加到金鑰庫的金鑰名稱。 此 Cmdlet 會依據此參數指定的名稱、金鑰庫名稱，以及您目前的環境，建構金鑰的完全限定功能變數名稱 (FQDN) 。 名稱必須是長度為 1 到 63 個字元的字串，只包含 0-9、a-z、A-Z 和 - (破折號) 。

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

### -NotBefore
指定無法使用金鑰的時間 ，做為 **DateTime** 物件。 此參數使用 UTC。 若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。 如果您未指定此參數，可以立即使用金鑰。

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

### -ResourceId
Vault 資源識別碼。

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

### -大小
以位為單位的 RSA 金鑰大小。 如果未指定，服務會提供安全預設值。

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

### -標記
以雜湊表格形式建立索引鍵值組。 例如：@{key0="value0";key1=$null;key2="value2"}

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

### -VaultName
指定此 Cmdlet 新增該金鑰的金鑰庫名稱。 此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。

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

### -確認
執行 Cmdlet 之前，系統會提示您確認。

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

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.KeyVault.models.PSKeyVault

### System.String

## 輸出

### Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey

## 筆記

## 相關連結

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

