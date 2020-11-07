---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957055"
---
# New-AzAlertRuleWebhook

## 摘要
建立警示規則 webhook。

## 句法

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzAlertRuleWebhook** Cmdlet 會建立一個警報規則 webhook。

## 示例

### 範例1：建立警示規則 webhook
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

這個命令會透過只指定服務 URI 來建立警示規則 webhook。

### 範例2：使用一個屬性建立 webhook
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

這個命令會針對具有一個屬性的 Contoso.com 建立一個警示規則 webhook，然後將它儲存在 $Actual 變數中。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -屬性
指定 [@ (property1 = ' value1 ",.... ) 格式的屬性清單。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceUri
指定服務 URI。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

## 輸出

### RuleWebhookAction 中的 [管理模型]。

## 筆記

## 相關連結

[附加 AzLogAlertRule](./Add-AzLogAlertRule.md)

[附加 AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[附加 AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[新-AzAlertRuleEmail](./New-AzAlertRuleEmail.md)

[新-AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


