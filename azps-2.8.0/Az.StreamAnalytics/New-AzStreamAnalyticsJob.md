---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: b50141c37c55d55f8fd8e823f09fefad49a55543
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793117"
---
# New-AzStreamAnalyticsJob

## 摘要
建立或更新資料流程分析作業。

## 句法

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的 AzStreamAnalyticsJob** Cmdlet 會在 Azure 中建立新的資料流程分析作業，或更新現有指定作業的定義。
您可以在中指定作業名稱。JSON 檔案或命令列上。
如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。
如果您指定的作業名稱已經存在，但沒有指定 *Force* 參數，則 Cmdlet 會詢問是否要取代現有的作業。
如果您指定 *Force* 參數並指定現有的作業名稱，作業定義將會不經確認就加以取代。

## 示例

### 範例1：建立工作
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

這個命令會從 JobDefinition.js的定義建立作業。
如果已定義作業定義檔中具有指定名稱的現有作業，則 Cmdlet 會詢問是否要取代該作業。

### 範例2：取代作業定義
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

這個命令會取代 StreamingJob 的作業定義而不需確認。

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

### 檔案
指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 串流分析作業的 JSON 標記法。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要建立之 Azure 串流分析作業的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資料流程分析作業應該屬於的資源群組的名稱。

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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSJob 中的 StreamAnalytics。

## 筆記

## 相關連結

[AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[移除-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[開始-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[停止 AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)

[停止 AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


