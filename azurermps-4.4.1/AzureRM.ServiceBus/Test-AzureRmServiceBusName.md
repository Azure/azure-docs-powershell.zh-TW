---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625671"
---
# Test-AzureRmServiceBusName

## 摘要
檢查指定命名空間名稱的可用性

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## 說明
**Test AzureRmServiceBusName** Cmdlet 會檢查命名空間名稱的可用性

## 示例

### 範例1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### 範例2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### 範例3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

傳回命名空間名稱的可用性狀態

## 參數

### -命名空間
已將命名空間名稱。

```yaml
Type: String
Parameter Sets: (All)
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

### -命名空間
 System.object

## 輸出

### [CheckNameAvailabilityResultAttributes，0.1.0.0，Version =，Culture = 中性，PublicKeyToken = null）]。））。

### 範例1
NameAvailable 原因訊息
------------- ------ -------
         True   None

### 範例2
NameAvailable 原因訊息
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### 範例3
NameAvailable 原因訊息
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## 筆記

## 相關連結
