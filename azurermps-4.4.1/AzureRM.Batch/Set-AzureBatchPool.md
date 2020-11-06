---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450860"
---
# Set-AzureBatchPool

## 摘要
更新文件庫的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchPool** Cmdlet 會更新 Azure Batch 服務中的 pool 屬性。
使用 Get-AzureBatchPool Cmdlet 來取得 **PSCloudPool** 物件。
修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。

## 示例

### 範例1：更新文件庫
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

第一個命令會使用 **AzureBatchPool** 來取得池子，然後將它儲存在 $Pool 變數中。

接下來的三個命令會修改 $Pool 物件上的「開始」任務規格。

最後一個命令會更新批次服務，以符合 $Pool 中的本機物件。

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

### -Pool
指定此 Cmdlet 更新批次服務的 **PSCloudPool** 。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
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

### PSCloudPool
形參 "Pool" 接受管線中 "PSCloudPool" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureBatchPool](./Get-AzureBatchPool.md)

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[新-AzureBatchPool](./New-AzureBatchPool.md)

[移除-AzureBatchPool](./Remove-AzureBatchPool.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


