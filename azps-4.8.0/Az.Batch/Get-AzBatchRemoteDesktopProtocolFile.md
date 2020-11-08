---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128555"
---
# Get-AzBatchRemoteDesktopProtocolFile

## 摘要
從計算節點取得 RDP 檔案。

## 句法

### Id_Path (預設) 
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Id_Stream
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzBatchRemoteDesktopProtocolFile** Cmdlet 會從計算節點取得遠端桌面通訊協定 (RDP) 檔案，並將它儲存為檔案或使用者提供的資料流程。

## 示例

### 範例1：從指定的計算節點取得 RDP 檔案並儲存檔案
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

這個命令會從具有 ID Pool06 的 ComputeNode01 中的 [計算] 節點取得 RDP 檔案。
該命令會將 .rdp 檔案另存為 C:\PowerShell\MyComputeNode.rdp。
使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。

### 範例2：從計算節點取得 RDP 檔案，並使用管線儲存檔案
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

這個命令會在擁有 ID Pool06 的池中取得 ID 為 ComputeNode02 的 compute 節點。
命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。
目前的 Cmdlet 會從 [計算] 節點取得 rpd 檔案，然後將內容另存為名為 C:\PowerShell\MyComputeNode02.rdp. 的檔案。

### 範例3：從指定的計算節點取得 RDP 檔案，並將它引導至資料流程
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。
第二個命令會從計算節點中取得一個 .rdp 檔案，並在擁有 ID Pool06 的池中包含 ID ComputeNode03。
命令會將檔案內容定向至 $Stream 中的資料流程。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。
如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。 若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。 使用共用金鑰驗證時，預設會使用主要便捷鍵。 若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。

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

### -ComputeNode
將 .rdp 檔案指向的計算節點指定為 **PSComputeNode** 物件。
若要取得計算節點物件，請使用 Get-AzBatchComputeNode Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
指定 .rdp 檔案指向的計算節點 ID。

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
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
指定此 Cmdlet 儲存 .rdp 檔案的檔路徑。

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
指定此 Cmdlet 將 RDP 資料導向到哪個資料流程。
這個 Cmdlet 不會關閉或倒帶此資料流程。

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
指定包含 [計算] 節點（這個 Cmdlet 取得 .rdp 檔案）的池 ID。

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### Microsoft.Azure.Commands.Batch。PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### System.void

## 筆記

## 相關連結

[AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Azure 批次 Cmdlet](/powershell/module/Az.Batch/)
