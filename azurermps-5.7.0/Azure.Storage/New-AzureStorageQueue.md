---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449446"
---
# New-AzureStorageQueue

## 摘要
建立儲存佇列。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 說明
**新的-AzureStorageQueue** Cmdlet 會在 Azure 中建立儲存佇列。

## 示例

### 範例1：建立 Azure 儲存空間佇列
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

這個範例會建立名為 queueabc 的儲存佇列。

### 範例2：建立多個 azure 存儲佇列
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

這個範例會建立多個儲存佇列。
它會使用 .NET 字串類別的 Split 方法，然後傳送管線上的名稱。

## 參數

### -內容
指定 Azure 儲存區內容。
您可以使用 New-AzureStorageContext Cmdlet 來建立它。

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -名稱
指定佇列的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### IStorageCoNtext

參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值

### 字串

形參 "Name" 接受管線中類型 "String" 的值

## 輸出

### AzureStorageQueue WindowsAzure. ResourceModel。

## 筆記

## 相關連結

[AzureStorageQueue](./Get-AzureStorageQueue.md)

[移除-AzureStorageQueue](./Remove-AzureStorageQueue.md)


