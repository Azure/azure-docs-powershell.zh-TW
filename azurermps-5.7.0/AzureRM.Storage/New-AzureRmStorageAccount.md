---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453972"
---
# New-AzureRmStorageAccount

## 摘要
建立儲存空間帳戶。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**新的-AzureRmStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。

## 示例

### 範例1：建立儲存空間帳戶
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

這個命令會為 [資源] 群組名稱 MyResourceGroup 建立儲存空間帳戶。

### 範例2：建立使用儲存服務加密的 Blob 儲存空間帳戶
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

這個命令會建立使用熱存取類型的 Blob 儲存空間帳戶。
帳戶已啟用 Blob 服務的儲存服務加密。

### 範例3：建立可在 Blob 和檔案服務上啟用儲存服務加密的儲存空間帳戶，並為 Azure KeyVault 產生並指派身分識別。
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

這個命令會建立可在 Blob 和檔案服務上啟用儲存服務加密的儲存空間帳戶。  它也會產生並指派可用於透過 Azure KeyVault 管理帳戶金鑰的身分識別。

## 參數

### -AccessTier
指定此 Cmdlet 所建立之儲存空間帳戶的存取層。
此參數可接受的值為： [熱] 和 [超酷]。

如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。

如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。

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
指定儲存空間帳戶之自訂網域的名稱。
預設值為 [儲存]。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
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
Position: 8
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

### 類型
指定這個 Cmdlet 所建立的儲存空間帳戶類型。
此參數可接受的值為：

- 容量.
支援 Blob、表格、佇列、檔案和磁片儲存的一般用途儲存空間帳戶。

- BlobStorage.
僅支援以 Blob 儲存的 blob 儲存空間帳戶。


預設值為 [儲存]。

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

### -位置
指定要建立的儲存空間帳戶位置。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要建立的儲存空間帳戶名稱。

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
指定要新增儲存空間帳戶之資源群組的名稱。

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
指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。
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

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。

如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
指示是否要啟用間接 CName 驗證。

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
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

[移除-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
