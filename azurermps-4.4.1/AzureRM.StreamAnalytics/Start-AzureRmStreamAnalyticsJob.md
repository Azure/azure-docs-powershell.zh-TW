---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b012704eebfa9d2c2a868679450cd0231667f585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626583"
---
# Start-AzureRmStreamAnalyticsJob

## 摘要
啟動資料流程分析作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmStreamAnalyticsJob** Cmdlet 會在 Azure 中非同步部署和啟動資料流程分析作業。

## 示例

### 範例1：啟動資料流程分析作業
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

這個命令會啟動作業 StreamingJob，並指定輸出事件資料流程應該在 timestamp 2014-03T01：00Z 啟動。

## 參數

### -名稱
指定要啟動之 Azure 串流分析作業的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartMode
指定作業的開始模式。
有效值為： 

- JobStartTime-這個值表示輸出事件資料流程的起始點應該在作業啟動時開始。
- CustomTime-此值表示輸出事件資料流程的起始點應從在 *OutputStartTime* 參數中指定的自訂時間開始。 
 --LastOutputEventTime-此值表示輸出事件資料流程的起始點應該從最後一個事件輸出時間開始。

如果屬性不存在，則預設值為 JobStartTime。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
指定輸出開始時間。
這個值是一個 ISO-8601 格式化的時間戳記，可指出輸出事件資料流程的起點，或 $Null 來指示每當資料流程作業啟動時，都會開始進行輸出事件資料流程。
如果 *OutputStartMode* 設定為 CustomTime，則這個屬性必須有值。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資料流程分析作業所屬之資源群組的名稱。

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

### System.object

## 筆記

## 相關連結

[AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[新-AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[移除-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[停止 AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


