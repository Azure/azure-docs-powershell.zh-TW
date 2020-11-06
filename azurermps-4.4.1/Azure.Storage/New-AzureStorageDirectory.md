---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: c039546504e51e6ba121402ae32025ef49294294
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457372"
---
# New-AzureStorageDirectory

## 摘要
建立目錄。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 共用名稱 (預設) 
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### 共用
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### 空目錄
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 說明
**新的-AzureStorageDirectory** Cmdlet 會建立目錄。
這個 Cmdlet 會傳回 **CloudFileDirectory** 物件。

## 示例

### 範例1：在檔案共用中建立資料夾
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

這個命令會在檔案共用中建立名為 ContosoWorkingFolder 的資料夾（名為 ContosoShare06）。

### 範例2：在檔案共用物件中指定的檔案共用中建立資料夾
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

這個命令會使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。

## 參數

### -ClientTimeoutPerRequest
指定一個服務要求的用戶端超時間隔（以秒為單位）。
如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。
如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
指定最大併發網路通話數。
您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。
指定的值是絕對計數，不會乘以核心計數。
這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。
預設值為10。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -內容
指定 Azure 儲存區內容。
若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Directory
將資料夾指定為 **CloudFileDirectory** 物件。
這個 Cmdlet 會在此參數指定的位置中建立資料夾。
若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。
您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
指定資料夾的路徑。
這個 Cmdlet 會為這個 Cmdlet 所指定的路徑建立一個資料夾。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求中伺服器部分的超時時間長度。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -共用
指定 **CloudFileShare** 物件。
這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。
若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。
此物件包含儲存內容。
如果您指定此參數，請勿指定 *CoNtext* 參數。

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -共用名稱
指定檔案共用的名稱。
這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### IStorageCoNtext

參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值

### CloudFileDirectory

形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值

### 字串

形參 "Path" 接受來自管線的 "String" 類型的值

### CloudFileShare

形參 "Share" 接受管線中 "CloudFileShare" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureStorageFile](./Get-AzureStorageFile.md)

[AzureStorageShare](./Get-AzureStorageShare.md)

[新-AzureStorageCoNtext](./New-AzureStorageContext.md)

[新-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[移除-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)
