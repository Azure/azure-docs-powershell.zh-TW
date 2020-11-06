---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: d8ce1ec138decb5769aebba431db2accd671f100
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451752"
---
# Stop-AzureBatchPoolResize

## 摘要
停止調整池大小的操作。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchPoolResize** Cmdlet 會在池中停止 Azure 批次調整大小操作。

## 示例

### 範例1：停止調整池子的大小
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

這個命令會在具有識別碼 ContosoPool06 的池中停止調整大小操作。
使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

### 範例2：使用管線停止調整池的大小
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

這個命令會使用管線運算子停止調整池的大小。
命令會使用 Get-AzureBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。
命令會將該 pool 物件傳遞到目前的 Cmdlet。
該命令會停止該池子上的調整大小作業。

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
指定此 Cmdlet 停止調整大小操作的池 ID。

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

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[AzureBatchPool](./Get-AzureBatchPool.md)

[開始-AzureBatchPoolResize](./Start-AzureBatchPoolResize.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


