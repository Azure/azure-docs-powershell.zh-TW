---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447571"
---
# Set-AzureRmStorageAccount

## 摘要
修改儲存空間帳戶。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### StorageEncryption (預設) 
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### KeyvaultEncryption
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmStorageAccount** Cmdlet 會修改 Azure 儲存空間帳戶。
您可以使用此 Cmdlet 來修改帳戶類型、更新客戶網域，或在儲存空間帳戶上設定標籤。

## 示例

### 範例1：設定儲存帳戶類型
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

這個命令會將儲存帳戶類型設定為 [Standard_RAGRS]。

### 範例2：針對儲存帳戶設定自訂網域
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

這個命令會針對儲存空間帳戶設定自訂網域。

### 範例3：在 Blob 和檔案服務上啟用加密
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

這個命令會在 Blob 和檔案上啟用儲存空間帳戶的儲存服務加密。

### 範例4：設定存取層的值
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

該命令會將 [存取層] 值設定為 [冷卻]。

### 範例4：設定自訂網域和標籤
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

該命令會將 [存取層] 值設定為 [冷卻]。

### 範例5：使用 Keyvault 在 Blob 服務上啟用加密
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

這個命令會在 Blob 上以新建立的 Keyvault 啟用儲存服務加密。

### 範例6：停用 KeySource 設定為 "Microsoft. Storage" 的檔案服務加密
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

這個命令會在 KeySource 設定為 "Microsoft. Storage" 的檔案服務上停用加密

## 參數

### -AccessTier
指定此 Cmdlet 修改之儲存空間帳戶的存取層。
此參數可接受的值為： [熱] 和 [超酷]。

如果您變更了存取層，可能會導致額外的費用。
如需詳細資訊，請參閱 Azure Blob 儲存體：熱及冷卻儲存層 https://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482) 。
如果儲存空間帳戶的類型是 [儲存空間]，請勿指定此參數。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。

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

### -CustomDomainName
指定自訂網域的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableEncryptionService
指示此 Cmdlet 是否停用儲存服務上的儲存服務加密。
支援 azure Blob 和 Azure 檔案服務。

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
指示此 Cmdlet 是否在儲存服務上啟用儲存服務加密。
支援 azure Blob 和 Azure 檔案服務。

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
指出儲存空間帳戶是否只啟用 HTTPs 流量。

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
如果您變更了存取層，可能會導致額外的費用。
如需詳細資訊，請參閱 Azure Blob 儲存體：熱及冷卻儲存層 https://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482) 。
如果儲存空間帳戶的類型是 [儲存空間]，請勿指定此參數。

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

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyName
儲存帳戶加密 keySource KeyVault KeyName

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyvaultEncryption
是否將儲存帳戶加密 KeySource 設定為 Keyvault。
如果您指定 KeyName、KeyVersion 和 KeyvaultUri，儲存帳戶加密 keySource 也會設定為 Microsoft。 Keyvault 天氣此參數已設定。
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultUri
儲存帳戶加密 keySource KeyVault KeyVaultUri

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVersion
儲存帳戶加密 keySource KeyVault KeyVersion

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要修改的儲存空間帳戶名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要修改儲存空間帳戶之資源群組的名稱。

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

### -SkuName
指定儲存空間帳戶的 SKU 名稱。
此參數可接受的值為：

- Standard_LRS]。
本機冗余儲存空間。
- Standard_ZRS]。
區域冗余儲存空間。
- Standard_GRS]。
地域冗余儲存空間。
- Standard_RAGRS]。
讀取 access 地域冗余儲存空間。
- Premium_LRS]。
[特優] 本機-冗余儲存空間。

您無法將 Standard_ZRS 和 Premium_LRS 類型變更為其他帳戶類型。
您無法將其他帳戶類型變更為 [Standard_ZRS] 或 [Premium_LRS]。

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEncryption
是否將儲存帳戶加密 KeySource 到 Microsoft. 儲存。

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
如果您為 New-AzureRmStorageAccount Cmdlet 的 *Kind* 參數指定了 BlobStorage 值，您必須指定 *AccessTier* 參數的值。

如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubDomain
指示是否要啟用間接 CName 驗證。

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[新-AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[移除-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)
