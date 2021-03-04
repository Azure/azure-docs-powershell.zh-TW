---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913258"
---
# Enable-AzBatchComputeNodeScheduling

## 簡介
啟用指定計算節點上的任務排程。

## 語法

### 識別碼 (預設) 
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Enable-AzBatchComputeNodeScheduling** Cmdlet 可啟用指定計算節點上的任務排程。
計算節點是專屬於特定應用程式工作負載的 Azure 虛擬機器。

## 例子

### 範例 1：啟用計算節點上的任務排程
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

這些命令可啟用計算節點 tvm-1783593343_34-20151117t222514z 上的任務排程。
若要這麼做，範例中的第一個命令會建立一個物件參照，其中包含批次帳戶 contosobatchaccount的帳戶金鑰。
此物件參照會儲存在名為 $coNtext 的$coNtext。
接著，第二個命令會使用此物件參照和 **Enable-AzBatchComputeNodeScheduling** Cmdlet 來連接到 myPool 的資料庫，並啟用 tvm-1783593343_34-20151117t222514z 上的任務排程。

### 範例 2：啟用資料集中計算節點上的任務排程
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

這些命令可啟用在集區集區 06 中所有計算節點上的任務排程。
若要執行這項工作，範例中的第一個命令會建立一個物件參照，其中包含批次帳戶 contosobatchaccount的帳戶金鑰。
此物件參照會儲存在名為 $coNtext 的$coNtext。
接著，範例中的第二個命令會使用此物件參照和 **Get-AzBatchComputeNode，** 以返回 Pool06 中找到的所有計算節點集合。
該集合接著會傳輸至 **Enable-AzBatchComputeNodeScheduling** Cmdlet，這可讓集合中的每個計算節點上的任務排程。

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
指定啟用任務排程之計算節點的物件參照。
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

### -Id
指定啟用任務排程的計算節點識別碼。

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
指定包含啟用任務排程之計算節點的批次集區識別碼。

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

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


