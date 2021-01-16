---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284995"
---
# Get-AzBatchJobStatistic

## 摘要
取得批次帳戶的作業摘要統計資料。

## 句法

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzBatchJobStatistic** Cmdlet 會取得 Azure Batch 帳戶中所有作業的存留期摘要統計資料。
統計資料會匯總到帳戶中存在的所有工作，從帳戶建立到統計的最後一次更新時間。

## 示例

### 範例1：取得所有作業的摘要統計資料
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

第一個命令會使用 **AzBatchAccountKey** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。
該命令會將這個物件參照儲存在 $CoNtext 變數中。
第二個命令會取得所有作業的摘要統計資料。
此命令會使用第一個命令的 $CoNtext 值。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### Microsoft.Azure.Commands.Batch。PSJobStatistics

## 筆記

## 相關連結

[AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[AzBatchPoolStatistic](./Get-AzBatchPoolStatistic.md)

[AzBatchPoolUsageMetrics](./Get-AzBatchPoolUsageMetric.md)
