---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448820"
---
# Get-AzureRmStreamAnalyticsFunction

## 摘要
取得資料流程分析作業中的函數。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmStreamAnalyticsFunction** Cmdlet 會取得 Azure 資料流程分析作業中定義的函數清單，或特定函數的相關資訊。

## 示例

### 範例1：取得所有串流分析函數
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

這個命令會取得在名為 StreamJob22 的作業中定義的函數。

### 範例2：取得特定的資料流程分析函式函數
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

這個命令會在名為 StreamJob22 的作業上，取得名為 ScoreTweet 定義之函數的相關資訊。

## 參數

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

### [PSFunction]、[StreamAnalytics]、[StreamAnalytics]、[]、[]、[]、[StreamAnalytics. PSFunction]

## 筆記

## 相關連結

[新-AzureRmStreamAnalyticsFunction](./New-AzureRmStreamAnalyticsFunction.md)

[移除-AzureRmStreamAnalyticsFunction](./Remove-AzureRmStreamAnalyticsFunction.md)

[Test-AzureRmStreamAnalyticsFunction](./Test-AzureRmStreamAnalyticsFunction.md)


