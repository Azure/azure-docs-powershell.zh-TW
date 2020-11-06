---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 540ea984d165a841288d1928192ad0ce035f7eb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449689"
---
# New-AzureRmStreamAnalyticsJob

## 摘要
建立或更新資料流程分析作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的 AzureRmStreamAnalyticsJob** Cmdlet 會在 Azure 中建立新的資料流程分析作業，或更新現有指定作業的定義。
您可以在中指定作業名稱。JSON 檔案或命令列上。
如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。
如果您指定的作業名稱已經存在，但沒有指定 *Force* 參數，則 Cmdlet 會詢問是否要取代現有的作業。
如果您指定 *Force* 參數並指定現有的作業名稱，作業定義將會不經確認就加以取代。

## 示例

### 範例1：建立工作
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

這個命令會從 JobDefinition.js的定義建立作業。
如果已定義作業定義檔中具有指定名稱的現有作業，則 Cmdlet 會詢問是否要取代該作業。

### 範例2：取代作業定義
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

這個命令會取代 StreamingJob 的作業定義而不需確認。

## 參數

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

[AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[移除-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[開始-AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)

[停止 AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)

[停止 AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


