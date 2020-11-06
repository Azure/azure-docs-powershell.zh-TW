---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 8364a3a8b9d88bfd3ce34f2e70f8fcae80e9b612
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452744"
---
# New-AzureRmRedisCacheScheduleEntry

## 摘要
建立排程專案。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmRedisCacheScheduleEntry** Cmdlet 會建立 **PSScheduleEntry** 物件。
Azure Redis Cache 修補程式排程 Cmdlet （例如 New-AzureRmRedisCachePatchSchedule Cmdlet）需要排程專案物件。

## 示例

### 範例1：建立週末的排程專案
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

這個命令會建立一個代表有指定開始時間和視窗之週末排程的 **PSScheduleEntry** 物件。

## 參數

### -DayOfWeek
指定 [排程] 專案在周中的日期。
此參數可接受的值為：
- 生活 
- 版 
- 從 
- 星期二 
- 星期三 
- 星期四 
- 日 
- 星期六 
- 日

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -MaintenanceWindow
指定更新所允許的時間範圍。

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartHourUtc
指定排程開始日的一個小時。

```yaml
Type: System.Int32
Parameter Sets: (All)
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

### System.object

### 系統為 Nullable "1 [[System. Timespan.zero，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

## 輸出

### PSScheduleEntry 中的 RedisCache。

## 筆記
* 關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站

## 相關連結

[AzureRmRedisCachePatchSchedule](./Get-AzureRmRedisCachePatchSchedule.md)

[新-AzureRmRedisCachePatchSchedule](./New-AzureRmRedisCachePatchSchedule.md)

[移除-AzureRmRedisCachePatchSchedule](./Remove-AzureRmRedisCachePatchSchedule.md)


