---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: 3baaa7296ab0fdd2c1dcab606b2896b11e5773f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445704"
---
# Set-AzureBatchJob

## 摘要
更新批次作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchJob** Cmdlet 會更新 Azure Batch 作業。
使用 Get-AzureBatchJob Cmdlet 來取得 **PSCloudJob** 物件。
修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。

## 示例

### 範例1：更新作業
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

第一個命令會使用 **AzureBatchJob** 來取得池子，然後將它儲存在 $Job 變數中。
第二個命令會修改 $Job 物件的優先順序規格。
最後一個命令會更新批次服務，以符合 $Job 中的本機物件。

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

### -工作
指定此 Cmdlet 更新批次服務的 **PSCloudJob** 。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### Microsoft.Azure.Commands.Batch。PSCloudJob
參數：作業 (ByValue) 

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext
參數： BatchCoNtext (ByValue) 

## 輸出

### System.void

## 筆記

## 相關連結

[Disable-AzureBatchJob](./Disable-AzureBatchJob.md)

[Enable-AzureBatchJob](./Enable-AzureBatchJob.md)

[AzureBatchJob](./Get-AzureBatchJob.md)

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[新-AzureBatchJob](./New-AzureBatchJob.md)

[移除-AzureBatchJob](./Remove-AzureBatchJob.md)

[停止 AzureBatchJob](./Stop-AzureBatchJob.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


