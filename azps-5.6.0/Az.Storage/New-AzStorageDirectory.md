---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915073"
---
# New-AzStorageDirectory

## 簡介
建立目錄。

## 語法

### ShareName (預設) 
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### 共用
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### 目錄
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## 描述
**New-AzStorageDirectory** Cmdlet 會建立目錄。
此 Cmdlet 會返回 **CloudFileDirectory** 物件。

## 例子

### 範例 1：在檔案共用中建立資料夾
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

此命令在名為 ContosoShare06 的檔案共用中，建立一個名為 ContosoWorkingFolder 的資料夾。

### 範例 2：在檔案共用物件中指定的檔案共用中建立資料夾
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

此命令使用 **Get-AzStorageShare** Cmdlet 取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將檔案共用傳遞至目前的 Cmdlet。
目前的 Cmdlet 在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。

## 參數

### -ClientTimeoutPerRequest
指定一個服務要求用戶端的時間間隔 ，以秒為單位。
如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。
如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
指定同時進行的最大網路通話數。
您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。
指定的值是絕對計數，不會乘以核心計數。
此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。
預設值為 10。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -內容
指定 Azure 儲存內容。
若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -目錄
將資料夾指定為 **CloudFileDirectory** 物件。
此 Cmdlet 會在此參數指定的位置建立資料夾。
若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。
您也可以使用 Get-AzStorageFile取得目錄。

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -路徑
指定資料夾的路徑。
此 Cmdlet 會為此 Cmdlet 指定的路徑建立資料夾。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求的伺服器部分之時間長度。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -共用
指定 **CloudFileShare** 物件。
此 Cmdlet 會在此參數指定的檔案共用中建立資料夾。
若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。
此物件包含儲存內容。
如果您指定此參數，請勿指定 *CoNtext* 參數。

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
指定檔案共用的名稱。
此 Cmdlet 會在此參數指定的檔案共用中建立資料夾。

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.storage.File.CloudFileShare

### Microsoft.Azure.storage.File.CloudFileDirectory

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileDirectory

## 筆記

## 相關連結

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Get-AzStorageShare](./Get-AzStorageShare.md)

[New-AzStorageCoNtext](./New-AzStorageContext.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)
