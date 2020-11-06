---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448579"
---
# Split-AzureRmReservation

## 摘要
分割 a `Reservation` 。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### [命令列 (預設) 
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PipeObject
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
`Reservation`以指定的數量分配分割 a 到兩個 `Reservation` 。

## 示例

### 範例1
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

將指定的 `Reservation` 數量分割成兩 `Reservation` 秒，並將相對應的數量分割

## 參數

### 數量
兩個 s 之 [數量] 欄位的逗號分隔整數 `Reservation`

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 預留
的 Pipe 物件參數 `Reservation`

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
`Reservation`要分割的識別碼

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

### -ReservationOrderId
`ReservationOrder`包含 `Reservation` 要分割之使用者的識別碼

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

### PSReservation 中的 [命令]。

## 輸出

### [System.object]。清單 ' 1 [PSReservation，#........ = 1.0.0.0，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]

## 筆記

## 相關連結

