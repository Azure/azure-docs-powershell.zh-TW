---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452300"
---
# New-AzureRmAnalysisServicesFirewallRule

## 摘要
建立新的 Analysis Services 防火牆規則

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## 說明
New-AzureRmAnalysisServicesFirewallRule 會建立新的防火牆規則物件。

## 示例

### 範例1
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

建立名為 rule1 且起始範圍為0.0.0.0 且結束範圍255.255.255.255 的防火牆規則

## 參數

### -FirewallRuleName
防火牆規則的名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RangeStart
防火牆規則的範圍開始

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RangeEnd
防火牆規則的範圍結束

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 輸入

## 輸出

### AzureAnalysisServicesFirewallRule 中的 AnalysisServices。

## 相關連結

[新-AzureRmAnalysisServicesFirewallConfig](./New-AzureRmAnalysisServicesFirewallConfig.md)
