---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621791"
---
# New-AzFirewall

## 摘要
在資源群組中建立新的防火牆。

## 句法

### 預設 (預設) 
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IpConfigurationParameterValues
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzFirewall** Cmdlet 會建立 Azure 防火牆。

## 示例

### 1：建立附加至虛擬網路的防火牆
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。
因為未指定任何規則，所以防火牆會封鎖所有流量 (預設行為) 。
威脅英特爾也會在預設模式下執行-警示-這表示惡意流量會記錄，但不會遭到拒絕。

### 2：建立可讓所有 HTTPS 流量使用的防火牆
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

這個範例會建立可讓埠443上所有 HTTPS 流量的防火牆。
威脅英特爾將在預設模式下執行-警示-這表示會記錄惡意流量，但不會遭到拒絕。

### 3： DNAT-將流向10.1.2.3：80的流量重新導向至10.2.3.4：8080
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

這個範例會建立一個已將10.1.2.3：80到10.2.3.4：8080威脅的 [所有資料包] 的目標 IP 和埠，將其轉換為此範例中的 [Intel]。

### 4：建立不含規則的防火牆，並在警示模式中與 Intel 威脅
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

這個範例會建立一個防火牆，該防火牆會封鎖 (預設行為的所有通訊，) 且在 [警示] 模式中受到 Intel 執行的威脅。
這表示在此情況下，將其他 (規則用於在此案例中針對惡意流量發出報警記錄-[全部拒絕]) 

### 5：建立可允許埠8080上所有 HTTP 流量的防火牆，但會封鎖由威脅 Intel 所識別的惡意網域
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

這個範例會建立一個防火牆，以允許埠8080上的所有 HTTP 流量，除非受威脅 Intel 認為是惡意的。
在 [拒絕] 模式中執行時，不像是 [警示]，而受威脅威脅的流量則不只是已登入，但也會封鎖。

## 參數

### -ApplicationRuleCollection
指定新防火牆的應用程式規則集合。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
在背景中執行 Cmdlet

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

### -位置
指定防火牆的區域。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所建立之 Azure 防火牆的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NatRuleCollection
AzureFirewallNatRuleCollections 清單

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleCollection
AzureFirewallNetworkRuleCollections 清單

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpName
公用 Ip 名稱。 公用 IP 必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要包含防火牆之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
雜湊資料表形式的索引鍵/值對。 例如：

@ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThreatIntelMode
指定威脅情報的操作模式。 預設模式為 [警示]，而不是 [關閉]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkName
指定將部署防火牆的虛擬網路名稱。 虛擬網路和防火牆必須屬於相同的資源群組。

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
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

### PSAzureFirewallApplicationRuleCollection [] （[]）

### PSAzureFirewallNatRuleCollection [] （[]）

### PSAzureFirewallNetworkRuleCollection [] （[]）

### [System.object] 集合. Hashtable

## 輸出

### PSAzureFirewall 中的 [.]

## 筆記

## 相關連結

[AzFirewall](./Get-AzFirewall.md)

[移除-AzFirewall](./Remove-AzFirewall.md)

[Set-AzFirewall](./Set-AzFirewall.md)

[新-AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[新-AzFirewallNatRuleCollection](./New-AzFirewallNatRuleCollection.md)

[新-AzFirewallNetworkRuleCollection](./New-AzFirewallNetworkRuleCollection.md)
