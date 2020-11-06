---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448582"
---
# Get-AzureRmReservationCatalog

## 摘要
取得可用保留的目錄

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## 說明
取得適用于指定 Azure 訂閱之保留實例購買的地區和 sku。

## 示例

### 範例1
```
PS C:\> Get-AzureRmReservationCatalog
```

取得預設訂閱的目錄

### 範例2
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

取得指定訂閱的目錄

## 參數

### -SubscriptionId
訂閱的識別碼

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### [System.object]。清單 ' 1 [PSCatalog，#........ = 1.0.0.0，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]

## 筆記

## 相關連結

