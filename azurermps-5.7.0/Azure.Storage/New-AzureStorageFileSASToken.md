---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: e5e4eaf5fa6808432dfdb04120bf9ef92a98452b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449448"
---
# New-AzureStorageFileSASToken

## 摘要
產生儲存空間的共用存取簽名權杖。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### NameSasPermission
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### NameSasPolicy
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### FileSasPermission
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### FileSasPolicy
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## 說明
**新的-AzureStorageFileSASToken** Cmdlet 會針對 Azure 儲存空間檔產生共用存取簽名權杖。

## 示例

### 範例1：產生具有完整檔案許可權的共用存取簽名權杖
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

這個命令會產生擁有名為 FilePath 之檔案之完整許可權的共用存取簽名權杖。

### 範例2：產生具有時間限制的共用存取簽名權杖
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

第一個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。
該命令會將目前的時間儲存在 $StartTime 變數中。

第二個命令會將兩個小時加到 $StartTime 中的物件，然後將結果儲存在 $EndTime 變數中。
此物件是在未來兩個小時的時間。

第三個命令會產生擁有指定許可權的共用存取簽名權杖。
此權杖會在目前的時間生效。
權杖在 $EndTime 中儲存的時間之前一直保持有效。

## 參數

### -內容
指定 Azure 儲存區內容。
若要取得內容，請使用 New-AzureStorageContext Cmdlet。

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### 檔案
指定 **CloudFile** 物件。
您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FullUri
指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。

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

### -Path
指定檔案相對於儲存區共用的路徑。

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -許可權
指定儲存空間的許可權。

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -原則
指定檔案的儲存存取原則。

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
指定要求所允許的通訊協定。
此參數可接受的值為：
* HttpsOnly
* HttpsOrHttp

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

### -共用名稱
指定儲存空間共用的名稱。

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StartTime
指定共用存取簽章生效的時間。

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

### CloudFile

形參 "File" 接受管線中 "CloudFile" 類型的值

### 字串

形參 "Path" 接受來自管線的 "String" 類型的值

### 字串

參數「共用名稱」接受來自管線的 "String" 類型的值

## 輸出

### System.object

## 筆記

## 相關連結

[新-AzureStorageCoNtext](./New-AzureStorageContext.md)

[新-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)
