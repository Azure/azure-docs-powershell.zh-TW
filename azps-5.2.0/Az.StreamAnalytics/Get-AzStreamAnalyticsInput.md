---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 1f83eaf8ff358c211dbe8b83cfb99d986e56c1ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283283"
---
# Get-AzStreamAnalyticsInput

## 摘要
取得串流分析作業輸入。

## 句法

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzStreamAnalyticsInput** Cmdlet 會列出資料流程分析作業中定義的所有輸入，或取得特定輸入的相關資訊。

## 示例

### 範例1：取得作業中定義之輸入的相關資訊
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

這個命令會傳回有關作業 StreamingJob 上所定義之所有輸入的資訊。

### 範例2：取得作業中定義之特定輸入的相關資訊
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

這個命令會傳回在作業 StreamingJob 上定義之名為 EntryStream 的輸入資訊。

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
指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。

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
指定要檢索之 Azure 串流分析輸入的名稱。

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
指定 Azure 串流分析輸入所屬之資源群組的名稱。

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

## 輸出

### PSInput 中的 StreamAnalytics。

## 筆記

## 相關連結

[新-AzStreamAnalyticsInput](./New-AzStreamAnalyticsInput.md)

[移除-AzStreamAnalyticsInput](./Remove-AzStreamAnalyticsInput.md)

[Test-AzStreamAnalyticsInput](./Test-AzStreamAnalyticsInput.md)


