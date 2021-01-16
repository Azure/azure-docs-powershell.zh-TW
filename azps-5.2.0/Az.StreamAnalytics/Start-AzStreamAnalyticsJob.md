---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283231"
---
# Start-AzStreamAnalyticsJob

## 摘要
啟動資料流程分析作業。

## 句法

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzStreamAnalyticsJob** Cmdlet 會在 Azure 中非同步部署和啟動資料流程分析作業。

## 示例

### 範例1：啟動資料流程分析作業
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

這個命令會啟動作業 StreamingJob，並指定輸出事件資料流程應該在 timestamp 2014-03T01：00Z 啟動。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
 - LastOutputEventTime-這個值表示輸出事件資料流程的起點應該從最後一個事件輸出時間開始。
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]

## 輸出

### System.object

## 筆記

## 相關連結

[AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[新-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[移除-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[停止 AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


