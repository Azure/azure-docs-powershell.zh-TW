---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453508"
---
# Get-AzureRmMetric

## 摘要
取得資源的度量值。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 預設模式中 Get-AzureRmMetric Cmdlet 的參數
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 完整參數集模式中 Get-AzureRmMetric Cmdlet 的參數
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmMetric** Cmdlet 會取得指定資源的規格值。

## 示例

### 範例1：使用摘要輸出取得量度
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

這個命令會取得含1分鐘時間細微性之 website3 的公制值。

### 範例2：取得詳細輸出的規格
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

這個命令會取得含1分鐘時間細微性之 website3 的公制值。
輸出是詳細的。

### 範例3：取得指定指標的詳細輸出
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

這個命令會針對要求規格取得詳細的輸出。

## 參數

### -DetailedOutput
表示此 Cmdlet 會顯示詳細的輸出。
根據預設，輸出是匯總的。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
指定當地時間的查詢結束時間。
預設為目前時間。

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricNames
指定度量單位名稱的陣列。

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
指定度量的資源識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
指定當地時間查詢的開始時間。
預設為目前的當地時間減去1小時。

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeGrain
以 hh： mm： ss 格式指定公制的時間細微性，以 Timespan.zero 物件為 **TimeSpan** 。

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AggregationType
Quer 的聚合類型

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### PSMetric [] 的 OutputClasses []

## 筆記

## 相關連結

[AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)


