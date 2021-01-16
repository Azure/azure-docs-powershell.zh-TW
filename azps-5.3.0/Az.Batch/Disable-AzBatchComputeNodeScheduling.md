---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447055"
---
# Disable-AzBatchComputeNodeScheduling

## 摘要
停用指定計算節點上的任務排程。

## 句法

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

## 說明
**Disable AzBatchComputeNodeScheduling** Cmdlet 會在指定的計算節點上停用工作排程。
計算節點是專用於特定應用程式工作負載的 Azure 虛擬機器。
當您在 [計算] 節點上停用任務排程時，您也可以決定如何處理目前在節點任務佇列中的工作。
**停用-AzBatchComputeNodeScheduling** 可讓您執行下列動作： 
- 終止工作並將其放回作業佇列中。
這樣可將這些工作重新安排在另一個計算節點上。 
- 終止工作並將其從作業佇列中移除。
以這種方式停止的工作不會重新排定日程。 
- 等待目前執行的所有工作完成，然後在 [計算] 節點上停用 [任務排程]。 
- 等待所有執行中的工作完成，並將所有資料保持期到期，然後在 [計算] 節點上停用 [任務排程]。

## 示例

### 範例1：停用計算節點上的任務排程
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

這些命令會在 compute 節點 tvm-1783593343_34-20151117t222514z 上停用 [任務排程]。
若要這樣做，範例中的第一個命令會針對批次帳戶 contosobatchaccount 建立帳戶金鑰的物件參考。
這個物件參照會儲存在名為 $coNtext 的變數中。
然後，第二個命令會使用這個物件參照和 **Disable AzBatchComputeNodeScheduling** Cmdlet 來連線至 [pool myPool]，並在節點 tvm 上停用 [任務排程]-1783593343_34-20151117t222514z。
因為未包含 *DisableComputeNodeSchedulingOptions* 參數，所以任何目前在計算節點上執行的工作都會重新排隊。

### 範例2：在池中的所有計算節點上停用任務排程
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

這些命令會在批次池中 Pool06 的所有電腦節點上停用 [任務排程]。
若要執行這項工作，範例中的第一個命令會建立一個物件參考，以取得批次帳戶 contosobatchaccount 的帳戶金鑰。
這個物件參照會儲存在名為 $coNtext 的變數中。
接著，這個範例中的第二個命令會使用這個物件參考，並 **取得 AzBatchComputeNode** ，以傳回在 Pool06 中找到的所有計算節點集合。
然後，該集合會輸送成管道，然後 **Disable AzBatchComputeNodeScheduling** Cmdlet，即可在集合中的每個計算節點上停用任務排程。
因為未包含 *DisableComputeNodeSchedulingOptions* 參數，所以任何目前在計算節點上執行的工作都會重新排隊。

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
指定任務排程停用之計算節點的物件參照。
這個物件參照是使用 Get-AzBatchComputeNode Cmdlet 建立，並將傳回的計算節點物件儲存在變數中。

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

### -DisableSchedulingOption
指定此 Cmdlet 處理正在停用排程之電腦節點上執行的任何工作的方式。
此參數可接受的值為：
- Requeue.
任務會立即停止並傳回作業佇列。
這可讓任務在另一個計算節點上重新排定。
這是預設值。 
- 終結.
工作會立即停止並從作業佇列中移除。
將不會重新安排這些工作。 
- TaskCompletion.
在計算節點上停用任務排程前，目前執行中的工作將能完成。
此節點上將不會排程任何新工作。 
- RetainedData.
在計算節點上停用任務排程前，目前執行中的工作將能完成，且資料保留期間將能到期。
此節點上將不會排程任何新工作。

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

### -識別碼
指定 [任務排程] 停用的計算節點識別碼。

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
指定包含已停用任務排程之計算節點的批次池的識別碼。
如果您使用 *PoolId* 參數，請勿在相同的命令中使用 *ComputeNode* 參數。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### Microsoft.Azure.Commands.Batch。PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### System.void

## 筆記

## 相關連結

[AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


