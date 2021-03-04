---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912913"
---
# Disable-AzBatchComputeNodeScheduling

## 簡介
停用指定計算節點上的任務排程。

## 語法

### 識別碼 (預設) 
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Disable-AzBatchComputeNodeScheduling** Cmdlet 會停用指定計算節點上的任務排程。
計算節點是專屬於特定應用程式工作負載的 Azure 虛擬機器。
當您停用計算節點上的任務排程時，您也可以選擇決定對節點工作佇列中目前的工作執行什麼處理。
**Disable-AzBatchComputeNodeScheduling** 可讓您執行下列操作： 
- 終止工作並放回工作佇列。
這可讓這些任務在另一個計算節點上重新排期。 
- 終止工作，並從工作佇列移除工作。
以這種方式停止的工作將不會重新排期。 
- 等待目前執行的所有工作完成，然後停用計算節點上的任務排程。 
- 等待所有執行中的工作完成，所有資料保留期間到期，然後停用計算節點上的任務排程。

## 例子

### 範例 1：停用計算節點上的任務排程
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

這些命令會停用計算節點 tvm-1783593343_34-20151117t222514z 上的任務排程。
若要這麼做，範例中的第一個命令會建立批次帳戶 contosobatchaccount 帳戶金鑰的物件參照。
此物件參照會儲存在名為 $coNtext 的$coNtext。
接著，第二個命令會使用此物件參照和 **Disable-AzBatchComputeNodeScheduling** Cmdlet 連線到 myPool 資料庫，並停用節點 tvm-1783593343_34-20151117t222514z 上的任務排程。
由於 *DisableComputeNodeSchedulingOptions* 參數並未包含任何目前在計算節點上執行的工作，因此將會重新叫用。

### 範例 2：停用資料集中所有計算節點上的任務排程
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

這些命令會停用批次處理集區集區 06 中所有電腦節點上的任務排程。
若要執行這項工作，範例中的第一個命令會建立批次帳戶 contosobatchaccount 帳戶金鑰的物件參照。
此物件參照會儲存在名為 $coNtext 的$coNtext。
接著，範例中的第二個命令會使用此物件參照和 **Get-AzBatchComputeNode，** 以返回 Pool06 中找到的所有計算節點集合。
然後，該集合會傳輸至 **Disable-AzBatchComputeNodeScheduling** Cmdlet，以停用集合中每個計算節點上的任務排程。
由於 *DisableComputeNodeSchedulingOptions* 參數並未包含任何目前在計算節點上執行的工作，因此將會重新叫用。

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

### -ComputeNode
指定停用任務排程之計算節點的物件參照。
此物件參照是使用 Get-AzBatchComputeNode Cmdlet，並儲存于變數中所返回的計算節點物件所建立。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -停用SchedulingOption
指定此 Cmdlet 如何處理正在停用排程的電腦節點上執行的任何工作。
此參數可接受的值為：
- 重新叫出。
工作會立即停止，並返回工作佇列。
這可讓任務重新排在另一個計算節點上。
這是預設值。 
- 終止。
工作會立即停止，並且從工作佇列移除。
這些工作將不會重新排期。 
- 任務完成。
在計算節點上停用任務排程之前，目前執行的工作將能夠完成。
此節點上不會排程任何新工作。 
- RetainedData。
目前執行的工作將能夠完成，而資料保留期間在計算節點上停用任務排程之前，也會過期。
此節點上不會排程任何新工作。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
指定停用任務排程的計算節點識別碼。

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
指定包含已停用任務排程之計算節點的批次集區識別碼。
如果您使用 *PoolId* 參數，請勿在同一個命令中使用 *ComputeNode* 參數。

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Batch。Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### System.Void

## 筆記

## 相關連結

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


