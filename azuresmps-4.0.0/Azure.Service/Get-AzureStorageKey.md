---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966994"
---
# Get-AzureStorageKey

## 摘要
傳回 Azure 儲存空間帳戶的主要和次要儲存空間帳戶金鑰。

## 句法

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureStorageKey** Cmdlet 會傳回具有 Azure 儲存空間帳戶名稱的物件、主要帳戶金鑰，以及指定之 Azure 儲存空間帳戶的次要帳戶金鑰做為屬性。

## 示例

### 範例1：取得包含主要和次要儲存空間金鑰的物件
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

這個命令會透過 ContosoStore01 儲存空間帳戶的主要和次要儲存空間來取得物件。

### 範例2：取得主要儲存空間帳戶金鑰並將它儲存在變數中
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

這個命令會將 ContosoStore01 儲存空間帳戶的 [主要儲存空間] 帳戶金鑰放在 $ContosoStoreKey 變數中。

## 參數

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

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
指定儲存空間帳戶名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記
* 若要取得 Node.js 的協助，請使用 `help node-dev` 命令。 如需 PHP 延伸的說明，請使用 `help php-dev` 命令。

## 相關連結

[AzureStorageAccount](./Get-AzureStorageAccount.md)

[新-AzureStorageAccount](./New-AzureStorageAccount.md)

[新-AzureStorageKey](./New-AzureStorageKey.md)

[移除-AzureStorageAccount](./Remove-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


