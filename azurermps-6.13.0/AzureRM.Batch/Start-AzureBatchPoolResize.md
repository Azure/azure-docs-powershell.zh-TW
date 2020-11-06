---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: c635061ac19b0fcc9543222da176324f84bea3a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450280"
---
# Start-AzureBatchPoolResize

## 摘要
開始調整池子的大小。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchPoolResize** Cmdlet 會在池中啟動 Azure Batch 調整大小作業。

## 示例

### 範例1：將池大小調整成12個節點
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

這個命令會在具有識別碼 ContosoPool06 的池中啟動調整大小作業。
操作的目標是12個專用的計算節點。
使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

### 範例2：使用解除配置選項調整池子的大小
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

這個 Cmdlet 會將一個池大小調整為五個專用的計算節點。
命令會使用 Get-AzureBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。
透過使用管線運算子，命令會將該 pool 物件傳遞到目前的 Cmdlet。
命令會在該文檔池中啟動調整大小作業。
目標是五個專用的計算節點。
此命令指定一個小時的超時時間。
命令會指定 [終止] 的解除配置選項。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。
如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。 若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。 使用共用金鑰驗證時，預設會使用主要便捷鍵。 若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。

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

### -ComputeNodeDeallocationOption
指定此 Cmdlet 啟動之大小調整作業的解除配置選項。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -識別碼
指定此 Cmdlet 調整大小的池 ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResizeTimeout
指定調整大小作業的超時週期。
如果此時間池未達到目標大小，則會停止調整大小操作。

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDedicatedComputeNodes
目標專用計算節點的數目。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetLowPriorityComputeNodes
目標低優先順序計算節點的數目。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext
參數： BatchCoNtext (ByValue) 

## 輸出

### System.void

## 筆記

## 相關連結

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[AzureBatchPool](./Get-AzureBatchPool.md)

[停止 AzureBatchPoolResize](./Stop-AzureBatchPoolResize.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


