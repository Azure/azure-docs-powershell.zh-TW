---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447272"
---
# Get-AzureRmReservationOrder

## 摘要
獲取 `ReservationOrder`

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
`ReservationOrder`使用者在目前租使用者中可存取的所有 s 的清單。 如果已設定 ReservationOrderId 參數，請取得該特定 ReservationOrder。

## 示例

### 範例1
```
PS C:\> Get-AzureRmReservationOrder
```

列出 `ReservationOrder` 使用者在目前租使用者中可存取的所有內容

### 範例2
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

取得 `ReservationOrder` 指定的 ReservationOrderId

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
