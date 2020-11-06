---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452084"
---
# Get-AzureRmReservationHistory

## 摘要
取得 `Reservation` 修訂歷程記錄。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### [命令列 (預設) 
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### PipeObject
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## 說明
所有修訂版本的清單 `Reservation` 。

## 示例

### 範例1
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

取得特定保留的修訂歷程記錄

## 參數

### 預留
S 的管道物件參數 `Reservation`

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReservationId
`Reservation`要顯示其記錄的 ReservationId

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrderId
ReservationOrderId `ReservationOrder` 包含 `Reservation`

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object
PSReservation 中的 [命令]。

## 輸出

### PSReservationPage 中的 [命令]。

## 筆記

## 相關連結

