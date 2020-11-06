---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448578"
---
# Merge-AzureRmReservation

## 摘要
合併兩個 `Reservation` s。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### [命令列 (預設) 
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### PipeObject
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
將指定 `Reservation` 的 s 合併至新的 `Reservation` 。 要合併的兩個 `Reservation` 都必須有相同的屬性。

## 示例

### 範例1
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

將兩個指定的 `Reservation` s 合併成一個 `Reservation`

## 參數

### 預留
要合併的兩個 ReservationIds 的逗號分隔字串

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReservationId
`ReservationOrder`包含兩個 s 的 ReservationOrderId `Reservation`

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservationOrderId
{{Fill ReservationOrderId 說明}}

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSReservation [] 的 []

## 輸出

### [System.object]。清單 ' 1 [PSReservation，#........ = 1.0.0.0，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]

## 筆記

## 相關連結

