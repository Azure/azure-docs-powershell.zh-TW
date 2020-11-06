---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450708"
---
# Get-AzureBatchNodeFileContent

## 摘要
取得批節點檔案。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### Task_Id_Path
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchNodeFileContent** Cmdlet 會取得 Azure Batch-節點檔案，並將它儲存為檔案或資料流程。

## 示例

### 範例1：取得與任務相關聯的批節點檔案，並儲存檔案
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

這個命令會取得名為 StdOut.txt 的節點檔案，並將它儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。
StdOut.txt 節點檔案與具有 ID Job01 之作業的識別碼 Task01 相關聯。
使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

### 範例2：取得批節點檔案，並使用管線將它儲存到指定的檔案路徑
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

這個命令會透過使用 Get-AzureBatchNodeFile Cmdlet 來取得名為 StdErr.txt 的節點檔案。
命令會使用管線運算子，將該檔案傳遞至目前的 Cmdlet。
目前的 Cmdlet 會將該檔案儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。
StdOut.txt 節點檔案與具有 ID Job02 之作業的識別碼 Task02 相關聯。

### 範例3：取得與任務相關聯的批節點檔案，並將它引導至資料流程
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。

第二個命令會從具有 ID Job03 之作業的識別碼 Task11 的任務中，取得名為 StdOut.txt 的節點檔案。
命令會將檔案內容定向至 $Stream 中的資料流程。

### 範例4：從計算節點取得節點檔案並儲存
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

這個命令會在擁有 ID Pool01 的池中，從 ComputeNode01 ID 為的 compute 節點中取得 Startup\StdOut.txt 節點檔案。
該命令會將檔案儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。

### 範例5：從計算節點取得節點檔案，然後使用管線儲存該檔
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

此命令會從 ComputeNode01 ID 為的計算節點中，使用 Get-AzureBatchNodeFile 來取得節點檔案 Startup\StdOut.txt。
Compute 節點位於 ID 為 Pool01 的池中。
命令會將該節點檔案傳遞至目前的 Cmdlet。
該 Cmdlet 會將檔案儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。

### 範例6：從計算節點取得節點檔案，並將它引導至資料流程
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。

第二個命令會從具有 ID Pool01 的 ComputeNode01 中的計算節點，取得名為 StdOut.txt 的節點檔案。
命令會將檔案內容定向至 $Stream 中的資料流程。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。
如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。 若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。 使用共用金鑰驗證時，預設會使用主要便捷鍵。 若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
要下載之位元組範圍的結尾。
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
要下載的位元組範圍起始。
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
指定包含此 Cmdlet 傳回之節點檔案之計算節點的識別碼。

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPath
指定此 Cmdlet 儲存節點檔案的檔路徑。

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
指定此 Cmdlet 寫入節點檔內容的資料流程。
這個 Cmdlet 不會關閉或倒帶此資料流程。

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
指定此 Cmdlet 取得的檔案，做為 **PSNodeFile** 物件。
若要取得節點檔物件，請使用 Get-AzureBatchNodeFile Cmdlet。

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -作業 Id
指定包含目標任務之作業的識別碼。

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
要下載之節點檔案的路徑。

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
指定包含此 Cmdlet 所取得之節點檔案之 [計算] 節點的池 ID。

```yaml
Type: String
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
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### BatchAccountCoNtext
形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值

### PSNodeFile
形參 "InputObject" 接受管線中 "PSNodeFile" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


