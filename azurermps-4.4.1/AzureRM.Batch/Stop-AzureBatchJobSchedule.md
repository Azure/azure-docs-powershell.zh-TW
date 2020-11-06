---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451755"
---
# Stop-AzureBatchJobSchedule

## 摘要
停止批次作業排程。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchJobSchedule** Cmdlet 會停止 Azure 批次作業排程。

## 示例

### 範例1：停止作業排程
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

這個命令會停止具有識別碼 JobSchedule17 的作業排程。
使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。
若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。

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

### -識別碼
指定此 Cmdlet 停止的作業排程 ID。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### BatchAccountCoNtext
形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值

### 字串
形參 "Id" 接受管線中類型 "String" 的值

## 輸出

## 筆記

## 相關連結

[Disable-AzureBatchJobSchedule](./Disable-AzureBatchJobSchedule.md)

[Enable-AzureBatchJobSchedule](./Enable-AzureBatchJobSchedule.md)

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[新-AzureBatchJobSchedule](./New-AzureBatchJobSchedule.md)

[移除-AzureBatchJobSchedule](./Remove-AzureBatchJobSchedule.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


