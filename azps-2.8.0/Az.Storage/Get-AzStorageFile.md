---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 5d73923dd3de630673d9228461397ec1789bd268
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792965"
---
# Get-AzStorageFile

## 摘要
列出路徑的目錄和檔案。

## 句法

### 共用名稱 (預設) 
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### 共用
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### 空目錄
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## 說明
**AzStorageFile** Cmdlet 會列出您指定的共用或目錄的目錄和檔案。
指定 *path* 參數，以取得指定路徑中目錄或檔案的實例。
這個 Cmdlet 會傳回 **AzureStorageFile** 和 **AzureStorageDirectory** 物件。
您可以使用 **IsDirectory** 屬性來區分資料夾與檔案。

## 示例

### 範例1：列出共用中的目錄
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

這個命令只會列出 [共用] ContosoShare06 中的目錄。
它會先使用管線運算子來檢索檔案和目錄，並將它們傳到 **where** 運算子，然後捨棄類型不是 "CloudFileDirectory" 的任何物件。

### 範例2：列出檔案目錄
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

這個命令會在 [共用 ContosoShare06] 底下的 [目錄 ContosoWorkingFolder] 中列出檔案和資料夾。
它會先取得目錄實例，然後將它的管道加入 **AzStorageFile** Cmdlet，以列出該目錄。

## 參數

### -ClientTimeoutPerRequest
指定一個服務要求的用戶端超時間隔（以秒為單位）。
如果上一個呼叫在指定的間隔時間內失敗，這個 Cmdlet 會將要求重試。
如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。

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
指定最大併發網路通話數。
您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。
指定的值是絕對計數，不會乘以核心計數。
這個參數可協助減輕低頻寬環境中的網路連線問題，例如 100 kb/秒。
預設值為10。

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
指定 Azure 儲存區內容。
若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。

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
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -Directory
將資料夾指定為 **CloudFileDirectory** 物件。
這個 Cmdlet 會取得此參數指定的資料夾。
若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。
您也可以使用 **AzStorageFile** Cmdlet 來取得目錄。

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
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
如果您省略 *Path* 參數， **AzStorageFile** 會列出指定檔案共用或目錄中的目錄和檔案。
如果您包含 *Path* 參數，則 **AzStorageFile** 會傳回指定路徑中目錄或檔案的實例。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求的服務端超時間隔（以秒為單位）。
如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。

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
這個 Cmdlet 會從此參數指定的檔案共用取得檔案或目錄。
若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。
此物件包含儲存內容。
如果您指定此參數，請勿指定 *CoNtext* 參數。

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
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
這個 Cmdlet 會從此參數指定的檔案共用取得檔案或目錄。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### CloudFileShare （即 Azure）

### CloudFileDirectory （即 Azure）

### IStorageCoNtext 中的 [Common.]

## 輸出

### CloudFile （即 Azure）

## 筆記

## 相關連結

[AzStorageFileContent](./Get-AzStorageFileContent.md)

[新-AzStorageDirectory](./New-AzStorageDirectory.md)

[移除-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[移除-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


