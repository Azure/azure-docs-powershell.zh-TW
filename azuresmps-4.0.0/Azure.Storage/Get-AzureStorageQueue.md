---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443443"
---
# Get-AzureStorageQueue

## 摘要
列出 [儲存佇列]。

## 句法

### QueueName (預設) 
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 說明
**AzureStorageQueue** Cmdlet 會列出與 Azure 儲存空間帳戶相關聯的儲存佇列。

## 示例

### 範例1：列出所有 Azure 儲存空間佇列
```
PS C:\>Get-AzureStorageQueue
```

這個命令會取得目前儲存空間帳戶的所有儲存佇列清單。

### 範例2：使用萬用字元列出 Azure 儲存空間佇列
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

這個命令使用萬用字元來取得名稱以 queue 開頭的儲存佇列清單。

### 範例3：使用佇列名稱首碼列出 Azure 儲存空間佇列
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

這個範例使用 *Prefix* 參數來取得名稱以 queue 開頭的儲存佇列清單。

## 參數

### -內容
指定 Azure 儲存區內容。
您可以使用 **新的 AzureStorageCoNtext** Cmdlet 來建立它。

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
指定名稱。
如果沒有指定名稱，則 Cmdlet 會取得所有佇列的清單。
如果指定完整或部分名稱，則 Cmdlet 會取得符合名稱模式的所有佇列。

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
指定要取得的佇列名稱中所用的首碼。

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[新-AzureStorageQueue](./New-AzureStorageQueue.md)

[移除-AzureStorageQueue](./Remove-AzureStorageQueue.md)


