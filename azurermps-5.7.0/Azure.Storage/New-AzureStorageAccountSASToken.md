---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452319"
---
# New-AzureStorageAccountSASToken

## 摘要
建立帳戶層級 SAS 權杖。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## 說明
**新的-AzureStorageSASToken** Cmdlet 會針對 Azure 儲存空間帳戶 (SAS) 權杖建立帳戶層級的共用存取簽章。

您可以使用 SAS 權杖委派多個服務的許可權，或委派無法搭配物件層級 SAS 權杖使用之服務的許可權。

## 示例

### 範例1：使用完整許可權建立帳戶層級 SAS 標記
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

這個命令會建立具有完整許可權的帳戶層級 SAS 權杖。

### 範例2：針對 IP 位址範圍建立帳戶層級 SAS 標記
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

這個命令會針對來自指定 IP 位址範圍的 HTTPS 式要求建立帳戶層級 SAS 權杖。

## 參數

### -內容
指定 Azure 儲存區內容。
您可以使用 New-AzureStorageContext Cmdlet 來取得 **AzureStorageCoNtext** 物件。

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
指定共用存取簽名失效的時間。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。
範圍包括在內。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -許可權
指定儲存空間帳戶的許可權。
許可權只有符合指定的資源類型時才是有效的。
如需可接受許可權值的詳細資訊，請參閱建立帳戶 SAShttps://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
指定以帳戶 SA 發出的要求所允許的通訊協定。
此參數可接受的值為：

- HttpsOnly
- HttpsOrHttp

預設值為 HttpsOrHttp。

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
指定可用於 SAS 權杖的資源類型。
此參數可接受的值為：

- 所有
- Services
- 包裝箱
- 面向

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -服務
指定服務。
此參數可接受的值為：

- 所有
- Blob
- 檔案
- 序列
- 張

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
指定時間（以 **DateTime** 物件表示），SAS 就會生效。
若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### IStorageCoNtext

參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值

## 輸出

### System.object

## 筆記

## 相關連結

[新-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[新-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[新-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[新-AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[新-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[新-AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


