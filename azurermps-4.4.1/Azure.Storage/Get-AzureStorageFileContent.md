---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a04a035e0fedfa4bca00eceda1dcf8dba0680c0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452655"
---
# Get-AzureStorageFileContent

## 摘要
下載檔案的內容。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 共用名稱 (預設) 
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 共用
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 空目錄
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 檔案
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzureStorageFileContent** Cmdlet 會下載檔案的內容，然後將檔案儲存到您指定的目的地。
這個 Cmdlet 不會傳回檔案的內容。

## 示例

### 範例1：從資料夾下載檔案
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

這個命令會將資料夾 ContosoWorkingFolder 中名為 CurrentDataFile 的檔案從 [檔案共用] ContosoShare06 下載到 [目前] 資料夾。

### 範例2：下載 [範例檔案共用] 下的檔案
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

這個範例會下載 [範例檔案共用] 下的檔案

## 參數

### -CheckMd5
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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

### -ClientTimeoutPerRequest
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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

### -目的地
指定目的地路徑。
這個 Cmdlet 會將檔案內容下載到此參數指定的位置。

如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directory
將資料夾指定為 **CloudFileDirectory** 物件。
這個 Cmdlet 會取得此參數指定之資料夾中檔案的內容。
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

### 檔案
將檔案指定為 **CloudFile** 物件。
這個 Cmdlet 會取得此參數指定的檔案。
若要取得 **CloudFile** 物件，請使用 Get-AzureStorageFile Cmdlet。

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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

### -PassThru
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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

### -Path
指定檔案的路徑。
這個 Cmdlet 會取得此參數所指定之檔案的內容。
如果檔案不存在，這個 Cmdlet 會傳回錯誤。

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。
如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。
如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。

如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。

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
這個 Cmdlet 會下載此參數指定的共用中檔案的內容。
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
這個 Cmdlet 會下載此參數指定的共用中檔案的內容。

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

### IStorageCoNtext

參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值

### CloudFileDirectory

形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值

### CloudFile

形參 "File" 接受管線中 "CloudFile" 類型的值

### CloudFileShare

形參 "Share" 接受管線中 "CloudFileShare" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


