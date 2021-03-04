---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 5790d217a63b7c2ef3aa7011d5f8a708df1dfbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909786"
---
# Get-AzBatchNodeFileContent

## 簡介
獲得批次處理節點檔案。

## 語法

### Task_Id_Path
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-AzBatchNodeFileContent** Cmdlet 會取得 Azure Batch-節點檔案，並另存為檔案或串流。

## 例子

### 範例 1：取得與工作相關聯的批次處理節點檔案並儲存該檔案
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

此命令會獲得名為 StdOut.txt 的節點檔案，並E:\PowerShell\StdOut.txt到本地電腦的檔案路徑。
StdOut.txt節點檔案與具有識別碼 Job01 的工作具有識別碼工作01 的工作相關聯。
使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。

### 範例 2：取得批次節點檔案，然後使用管線將其儲存到指定的檔案路徑
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

此命令會使用 Cmdlet StdErr.txt名為 Get-AzBatchNodeFile檔案。
該命令會使用管線運算子，將檔案傳遞至目前的 Cmdlet。
目前的 Cmdlet 會將該檔案E:\PowerShell\StdOut.txt本地電腦的檔案路徑。
StdOut.txt節點檔案與具有識別碼 Job02 的工作具有識別碼工作02 的工作相關聯。

### 範例 3：取得與工作相關聯的批次處理節點檔案，並引導它至串流
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。
第二個命令會從具有識別碼 Job03 的工作StdOut.txt識別碼工作 11 的工作中，獲得名稱為 StdOut.txt 的節點檔案。
命令會以命令將檔案內容引導至 $Stream。

### 範例 4：從計算節點取得節點檔案並儲存
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

此命令會從具有識別碼Startup\StdOut.txt 01 之資料集中具有 ID ComputeNode01 的計算節點中，獲得節點檔案。
該命令會將檔案E:\PowerShell\StdOut.txt本地電腦的檔案路徑。

### 範例 5：從計算節點取得節點檔案，然後使用管線儲存
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

此命令會使用具有 ID ComputeNode01 之Startup\StdOut.txt計算節點Get-AzBatchNodeFile的節點檔案。
計算節點位於具有 ID Pool01 的集中。
該命令會將該節點檔案傳遞至目前的 Cmdlet。
該 Cmdlet 會將檔案E:\PowerShell\StdOut.txt本地電腦的檔案路徑。

### 範例 6：從計算節點取得節點檔案，並引導它至串流
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。
第二個命令會從具有 ID pool01 之StdOut.txt識別碼 ComputeNode01 的計算節點中，獲得名為 StdOut.txt 的節點檔案。
命令會以命令將檔案內容引導至 $Stream。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。
如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。 若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。 使用共用金鑰驗證時，預設會使用主便捷鍵。 若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
要下載的位元組範圍結尾。

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
要下載的位元組範圍的開始。

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
指定包含此 Cmdlet 所返回之節點檔案的計算節點識別碼。

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -DestinationPath
指定此 Cmdlet 將節點檔案另存的檔案路徑。

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
指定此 Cmdlet 寫入節點檔案內容的資料流程。
此 Cmdlet 不會關閉或倒帶此串流。

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
指定此 Cmdlet 以 **PSNodeFile** 物件獲得之檔案。
若要取得節點檔案物件，請使用 Get-AzBatchNodeFile Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
指定包含目標工作的工作的識別碼。

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -路徑
要下載的節點檔案路徑。

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
指定包含包含此 Cmdlet 所獲取之節點檔案之計算節點的集區識別碼。

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskId
指定任務的識別碼。

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### Microsoft.Azure.Commands.Batch。Models.PSNodeFile

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### System.Void

## 筆記

## 相關連結

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchNodeFile](./Get-AzBatchNodeFile.md)

[Azure Batch Cmdlet](/powershell/module/Az.Batch/)
