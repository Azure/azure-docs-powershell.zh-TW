---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 5e34e0b1ba9e9ab24c0cb47de636ceecec9751f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793234"
---
# Get-AzStreamAnalyticsFunction

## 摘要
取得資料流程分析作業中的函數。

## 句法

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzStreamAnalyticsFunction** Cmdlet 會取得 Azure 資料流程分析作業中定義的函數清單，或特定函數的相關資訊。

## 示例

### 範例1：取得所有串流分析函數
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

這個命令會取得在名為 StreamJob22 的作業中定義的函數。

### 範例2：取得特定的資料流程分析函式函數
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

這個命令會在名為 StreamJob22 的作業上，取得名為 ScoreTweet 定義之函數的相關資訊。

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

### -JobName
指定函數所歸屬之串流分析作業的名稱。
這個 Cmdlet 會取得此參數指定作業的功能。

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

### -名稱
指定此 Cmdlet 取得的資料流程分析函數的名稱。

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

### -ResourceGroupName
指定串流分析函數所歸屬之資源群組的名稱。
這個 Cmdlet 會取得此參數指定之群組的函數。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSFunction 中的 StreamAnalytics。

## 筆記

## 相關連結

[新-AzStreamAnalyticsFunction](./New-AzStreamAnalyticsFunction.md)

[移除-AzStreamAnalyticsFunction](./Remove-AzStreamAnalyticsFunction.md)

[Test-AzStreamAnalyticsFunction](./Test-AzStreamAnalyticsFunction.md)


