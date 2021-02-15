---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142169"
---
# New-AzFirewallApplicationRuleCollection

## 摘要
建立防火牆應用程式規則的集合。

## 句法

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzFirewallApplicationRuleCollection** Cmdlet 會建立防火牆應用程式規則的集合。

## 示例

### 範例1：使用單一規則建立集合
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

這個範例會使用一條規則建立集合。 會允許符合 $rule 1 中所識別之條件的所有流量。
第一個規則是針對埠443上的所有 HTTPS 流量（10.0.0.0）。 如果有具有較高優先順序的另一個應用程式規則集合 (較小的數位) ，這也會與 $rule 1 中所識別的流量相符，而具有較高優先順序的 rule 集合的動作將會生效。 

### 範例2：在規則集合中加入規則
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

這個範例會建立一個含有一個規則的新應用程式規則集合，然後使用規則集合物件上的方法 AddRule，將第二個規則新增到規則集合。 指定規則集合中的每個規則名稱必須具有唯一的名稱，且不區分大小寫。

### 範例3：從規則集合取得規則
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

這個範例會建立一個含有一個規則的新應用程式規則集合，然後依名稱取得規則，並在規則集合物件上呼叫方法 GetRuleByName。 方法 GetRuleByName 的規則名稱不區分大小寫。

### 範例4：從規則集合中移除規則
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

這個範例會建立具有兩個規則的新應用程式規則集合，然後在規則集合物件上呼叫方法 RemoveRuleByName，移除規則集合中的第一個規則。 方法 RemoveRuleByName 的規則名稱不區分大小寫。

## 參數

### -ActionType
規則集合的動作

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
指定此應用程式規則的名稱。 該名稱在規則集合內必須是唯一的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -優先順序
指定此規則的優先順序。 [優先順序] 是介於100和65000之間的數位。 數值越小，優先順序就越大。

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -規則
指定要在此集合下組成群組的規則清單。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSAzureFirewallApplicationRuleCollection 中的 [.]

## 筆記

## 相關連結

[新-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[新-AzFirewall](./New-AzFirewall.md)

[AzFirewall](./Get-AzFirewall.md)
