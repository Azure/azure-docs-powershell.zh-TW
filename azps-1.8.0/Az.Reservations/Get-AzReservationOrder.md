---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 3db5c7bf9665498236c3d0dacf05107926ed45eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620925"
---
# Get-AzReservationOrder

## 摘要
獲取 `ReservationOrder`

## 句法

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
`ReservationOrder`使用者在目前租使用者中可存取的所有 s 的清單。 如果已設定 ReservationOrderId 參數，請取得該特定 ReservationOrder。

## 示例

### 範例1
```
PS C:\> Get-AzReservationOrder
```

列出 `ReservationOrder` 使用者在目前租使用者中可存取的所有內容

### 範例2
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

取得 `ReservationOrder` 指定的 ReservationOrderId

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservationOrderId
使用者想要查看的特定 ReservationOrder 識別碼

```yaml
Type: System.Guid
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

### PSReservationOrderPage 中的 [命令]。

### PSReservationOrder 中的 [命令]。

## 筆記

## 相關連結
