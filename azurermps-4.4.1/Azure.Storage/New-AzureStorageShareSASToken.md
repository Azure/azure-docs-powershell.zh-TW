---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 84f280bf5e3297796bb8b56e5a5d42e513b79e79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446906"
---
# New-AzureStorageShareSASToken

## 摘要
產生 Azure 儲存空間共用的共用存取簽名權杖。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## 說明
**新的-AzureStorageShareSASToken** Cmdlet 會針對 Azure 儲存空間共用產生共用存取簽名權杖。

## 示例

### 範例1：為共用產生共用存取簽名權杖
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

這個命令會建立名為 ContosoShare 的共用存取簽名權杖。

### 範例2：使用管線產生多個共用存取簽名權杖
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

這個命令會取得符合前置詞測試的所有儲存空間共用。
命令會使用管線運算子將它們傳遞至目前的 Cmdlet。
目前的 Cmdlet 會為具有指定許可權的每個儲存空間共用建立共用存取權杖。

### 範例3：產生使用共用存取原則的共用存取簽名權杖
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

這個命令會為擁有名為 ContosoPolicy03 原則之名為 ContosoShare 的儲存空間共用建立共用存取簽名權杖。

## 參數

### -內容
指定 Azure 儲存區內容。
若要取得內容，請使用 New-AzureStorageContext Cmdlet。

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

### -許可權
指定權杖中的許可權，以存取共用中的共用和檔案。

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -原則
指定共用的儲存存取原則。

```yaml
Type: String
Parameter Sets: SasPolicy
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
Parameter Sets: (All)
Aliases: N, Name

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

### 字串

參數「共用名稱」接受來自管線的 "String" 類型的值

## 輸出

### System.object

## 筆記
* 關鍵字：常見、azure、services、data、storage、blob、queue、table

## 相關連結

[AzureStorageShare](./Get-AzureStorageShare.md)

[新-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
