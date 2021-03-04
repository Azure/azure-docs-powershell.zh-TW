---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: f8df4d49f0181b7cf8abf2581a522f953f3f2df7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916289"
---
# New-AzBatchResourceFile

## 簡介
建立資源檔案供使用 `New-AzBatchTask` 。

## 語法

### HTTPUrl (預設) 
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
建立資源檔案供使用 `New-AzBatchTask` 。

## 例子

### 範例 1：從指向單一檔案的 HTTP URL 建立資源檔案
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

建立參照 `PSResourceFile` HTTP URL。

### 範例 2：從 Azure 儲存容器 URL 建立資源檔案
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

建立參照 `PSResourceFile` Azure 儲存容器 URL。 容器中的所有檔案都會下載到指定的資料夾。

### 範例 3：從自動儲存容器名稱建立資源檔案
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

建立參照 `PSResourceFile` 自動儲存容器名稱。 容器中的所有檔案都會下載到指定的資料夾。

## 參數

### -AutoStorageContainerName
自動儲存帳戶中的儲存容器名稱。

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
從 Azure 儲存容器下載 Blob 時，使用 Blob 首碼。
只有名稱以指定首碼開頭的 Blob 會下載。
此首碼可以是部分檔案名或子目錄。
如果未指定首碼，將會下載容器中的所有檔案。

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileMode
以八進位格式獲得檔案許可權模式屬性。
只有在資源檔案下載到 Linux 節點時，此屬性才適用。
如果未指定 Linux 節點的此屬性，預設值為 0770。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
計算節點上下載檔案的位置 (工作) 的工作目錄。 如果已指定 HttpUrl 參數，則 FilePath 為必填專案，並說明要下載檔案的路徑，包括檔案名。 否則，如果已指定 AutoStorageContainerName 或 StorageContainerUrl 參數，則 FilePath 為選擇性專案，是下載檔案的目錄。 使用 FilePath 做為目錄時，任何已與輸入資料相關聯的目錄結構都會保留完整，並附加到指定的 FilePath 目錄。 指定的相對路徑無法中斷任務的工作目錄 (例如使用 '.」。) 。

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HTTPUrl
要下載之檔案的 URL。
如果 URL 是 Azure Blob 儲存體，則必須使用匿名存取來讀取 URL;也就是說，批次處理服務不會在下載 Blob 時顯示任何認證。
有兩種方法可以取得 Azure 儲存空間中 Blob 的這類 URL：包含共用存取簽章 (SAS) 以在 Blob 上授予讀取權限，或設定 Blob 的 ACL 或容器以允許公用存取。

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
Azure Blob 儲存體中 Blob 容器的 URL。
此 URL 必須使用匿名存取來可讀取且可列出;也就是說，從容器下載 Blob 時，批次處理服務不會顯示任何認證。
有兩種方法可以取得 Azure 儲存空間中容器的這類 URL：包含共用存取簽章 (SAS) 以在容器上授予讀取權限，或設定容器的 ACL 以允許公用存取。

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Batch。Models.PSResourceFile

## 筆記

## 相關連結

[New-AzBatchTask](./New-AzBatchTask.md)