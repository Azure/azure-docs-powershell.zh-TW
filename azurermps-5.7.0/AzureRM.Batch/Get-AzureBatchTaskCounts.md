---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446511"
---
# Get-AzureBatchTaskCounts

## 摘要
取得指定工作的任務計數。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 標識號
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### ParentObject
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## 說明
**AzureBatchTaskCounts** Cmdlet 會取得批次作業的 Azure Batch 任務計數。
使用 *JobId* 參數或 *作業* 參數指定作業。
[任務計數]：依活動、執行或已完成的任務狀態，以及成功或失敗的任務計數，提供任務的計數。 準備狀態中的工作會計算為正在執行。 如果 validationStatus 是 unvalidated，則批次服務無法針對清單任務 API 中所報告的任務狀態檢查狀態計數。 如果工作包含200000以上的任務，可能會 unvalidated validationStatus。

## 示例

### 範例1：依識別碼取得任務計數
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

這個命令會取得工作 Job01 的任務計數。
使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

## 參數

### -BatchCoNtext
與批次服務互動時要使用的 BatchAccountCoNtext 實例。
如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。
若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。
使用共用金鑰驗證時，預設會使用主要便捷鍵。
若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。

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

### -工作
指定包含此 Cmdlet 所取得之任務的工作。
若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。

```yaml
Type: PSCloudJob
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
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## 輸入

### System.object
Microsoft.Azure.Commands.Batch。PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountCoNtext


## 輸出

### Microsoft.Azure.Commands.Batch。PSTaskCounts


## 筆記

## 相關連結

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[AzureBatchJob](./Get-AzureBatchJob.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)
