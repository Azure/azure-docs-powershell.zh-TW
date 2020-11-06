---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451748"
---
# Stop-AzureBatchTask

## 摘要
停止批次任務。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 標識號
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchTask** Cmdlet 會停止 Azure Batch 工作。

## 示例

### 範例1：依識別碼刪除批次任務
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

這個命令會停止在具有 ID 作業的作業下具有識別碼 Task23 的工作-000001。
命令會提示您進行確認。
使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

### 範例2：使用管線停止批次工作
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

這個命令會透過使用 Get-AzureBatchTask Cmdlet 來取得作業中具有 id 作業000001之識別碼 Task26 的批次任務。
透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。
命令會停止該任務。

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
指定此 Cmdlet 停止的任務識別碼。

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -作業 Id
指定包含該任務的作業識別碼。

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

### -任務
指定此 Cmdlet 停止的工作。
若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### BatchAccountCoNtext
形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值

### PSCloudTask
形參 "Task" 接受管線中 "PSCloudTask" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureBatchTask](./Get-AzureBatchTask.md)

[新-AzureBatchTask](./New-AzureBatchTask.md)

[移除-AzureBatchTask](./Remove-AzureBatchTask.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


