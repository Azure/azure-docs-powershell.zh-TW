---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446888"
---
# New-AzBatchResourceFile

## 摘要
建立供使用的資源檔 `New-AzBatchTask` 。

## 句法

### HttpUrl (預設) 
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

## 說明
建立供使用的資源檔 `New-AzBatchTask` 。

## 示例

### 範例1：從指向單一檔案的 HTTP URL 建立資源檔
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

建立 `PSResourceFile` 參考 HTTP url。

### 範例2：從 Azure 儲存體容器 URL 建立資源檔
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

建立 `PSResourceFile` 參照 Azure 儲存體容器 URL。 容器中的所有檔案將會下載到指定的資料夾中。

### 範例3：從自動儲存空間容器名稱建立資源檔
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

建立對 `PSResourceFile` 自動儲存空間容器名稱的參照。 容器中的所有檔案將會下載到指定的資料夾中。

## 參數

### -AutoStorageContainerName
[自動儲存空間] 帳戶中的儲存容器名稱。

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
取得從 Azure 儲存空間容器下載 blob 時所要使用的 blob 前置詞。
只有其名稱以指定的首碼開頭的 blob 才會下載。
此前置詞可以是部分的檔案名或子目錄。
如果未指定前置詞，將會下載容器中的所有檔案。

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
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -低
取得八進位格式的檔案許可權模式屬性。
這個屬性只有在資源檔案下載到 Linux 節點時才適用。
如果沒有為 Linux 節點指定此屬性，則預設值為0770。

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
要將檔案下載到哪個計算節點上 (s) 的位置，相對於任務的工作目錄。 如果指定了 HttpUrl 參數，則需要 FilePath，並說明檔案將下載到哪個路徑，包括檔案名。 否則，如果指定 AutoStorageContainerName 或 StorageContainerUrl 參數，則 FilePath 是選擇性的，也就是下載檔案的目錄。 在使用 FilePath 做為目錄的情況下，任何已與輸入資料相關聯的目錄結構，都會保留完整並附加到指定的 FilePath 目錄中。 指定的相對路徑無法從工作的工作目錄中中斷 (例如使用 "...") ]。

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

### -HttpUrl
要下載之檔案的 URL。
如果 URL 是 Azure Blob 儲存空間，就必須使用匿名存取才能閱讀;也就是說，在下載 blob 時，批次服務不會顯示任何認證。
您可以透過兩種方式取得 Azure 儲存區中的 blob URL：包含共用存取簽章 (SAS) 授予對 blob 的讀取權限，或將 blob 或其容器的 ACL 設定為允許公用存取。

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
Azure Blob 儲存空間中的 blob 容器 URL。
這個 URL 必須是可讀取的，且可以使用匿名存取 listable。也就是說，當您從容器下載 blob 時，批服務不會顯示任何認證。
在 Azure 儲存體中，有兩種方式可取得容器的 URL：包含共用存取簽章 (SAS) 授予容器的讀取權限，或設定容器的 ACL 以允許公用存取。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### Microsoft.Azure.Commands.Batch。PSResourceFile

## 筆記

## 相關連結

[新-AzBatchTask](./New-AzBatchTask.md)