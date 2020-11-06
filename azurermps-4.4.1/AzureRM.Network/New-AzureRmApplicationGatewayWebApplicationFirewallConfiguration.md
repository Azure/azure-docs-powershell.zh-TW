---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 281a4a0d935d73777f7fdd693f3d32982b2da47a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448846"
---
# New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration

## 摘要
建立應用程式閘道的 WAF 配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會建立 web 應用程式防火牆 (WAF Azure 應用程式閘道的) 設定。

## 示例

### 範例1：建立應用程式閘道的 web 應用程式防火牆設定
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

第一個命令會針對名為「要求-942-應用程式-SQLI」的規則群組建立新的已停用規則群組設定，並停用規則942130與規則942140。
第二個命令會針對名為「要求 921--通訊協定-PROTOCOL」的規則群組，建立另一個停用的規則群組設定。 不會明確傳遞任何規則，因此規則群組的所有規則都將停用。
最後一個命令接著會建立 WAF 設定，並停用防火牆規則，$disabledRuleGroup 1 和 $disabledRuleGroup 2 中已設定。 新的 WAF 設定會儲存在 $firewallConfig 變數中。

## 參數

### -DisabledRuleGroups
已停用的規則群組。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -啟用
指出是否已啟用 WAF。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallMode
指定 web 應用程式防火牆模式。
此參數可接受的值為：

- 偵測
- 防護

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleSetType
Web 應用程式防火牆規則集的類型。 此參數可接受的值為： 

- OWASP

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleSetVersion
規則集類型的版本。
此參數可接受的值為： 

- 3.0
- 2.2.9

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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

### PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]

## 筆記

## 相關連結

[AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


