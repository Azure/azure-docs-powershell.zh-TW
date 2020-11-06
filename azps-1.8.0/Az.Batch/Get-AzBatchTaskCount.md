---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 51e9053737b95113144d5421492f64623b425ff6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623315"
---
# Get-AzBatchTaskCount

## 摘要
取得指定工作的任務計數。

## 句法

### 標識號
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzBatchTaskCount** Cmdlet 會取得批次作業的 Azure Batch 任務計數。
使用 *JobId* 參數或 *作業* 參數指定作業。
[任務計數]：依活動、執行或已完成的任務狀態，以及成功或失敗的任務計數，提供任務的計數。 準備狀態中的工作會計算為正在執行。 如果 validationStatus 是 unvalidated，則批次服務無法針對清單任務 API 中所報告的任務狀態檢查狀態計數。 如果工作包含200000以上的任務，可能會 unvalidated validationStatus。

## 示例

### 範例1：依識別碼取得任務計數
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

這個命令會取得工作 Job01 的任務計數。
使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

## 參數

### -BatchCoNtext
與批次服務互動時要使用的 BatchAccountCoNtext 實例。
如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。
若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。
使用共用金鑰驗證時，預設會使用主要便捷鍵。
若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。

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

### -工作
指定包含此 Cmdlet 所取得之任務的工作。
若要取得 **PSCloudJob** 物件，請使用 Get-AzBatchJob Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -作業 Id
要取得其任務計數的作業識別碼。

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### Microsoft.Azure.Commands.Batch。PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### Microsoft.Azure.Commands.Batch。PSTaskCounts

## 筆記

## 相關連結

[AzBatchAccountKeys](./Get-AzBatchAccountKey.md)

[AzBatchJob](./Get-AzBatchJob.md)

[Azure 批次 Cmdlet](/powershell/module/az.batch)
