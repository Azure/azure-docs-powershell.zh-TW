---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450233"
---
# New-AzureRmFirewallNetworkRuleCollection

## 摘要
建立網路規則的 Azure 防火牆網路集合。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmFirewallNetworkRuleCollection** Cmdlet 會建立防火牆網路規則的集合。

## 示例

### 1：使用兩個規則建立網路集合
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

這個範例會建立集合，以允許符合兩個規則中任一種的流量。
第一個規則是適用于所有的 UDP 流量。
第二個規則是從10.0.0.0 至60.1.5.0：4040的 TCP 流量。
如果有具有較高優先順序的另一個網路規則集合 (較小的數位) ，也就是與 $rule 1 或 $rule 2 中所識別的流量相符，具有較高優先順序的 rule 集合的動作將會生效。 

### 2：在規則集合中加入規則
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

這個範例會建立一個含有一個規則的新網路規則集合，然後使用規則集合物件上的方法 AddRule，將第二個規則新增到規則集合。 指定規則集合中的每個規則名稱必須具有唯一的名稱，且不區分大小寫。

### 3：從規則集合取得規則
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

這個範例會建立一個含有一條規則的新網路規則集合，然後依名稱取得規則，並在規則集合物件上呼叫方法 GetRuleByName。 方法 GetRuleByName 的規則名稱不區分大小寫。

### 4：移除規則集合中的規則
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

這個範例會建立具有兩個規則的新網路規則集合，然後在規則集合物件上呼叫方法 RemoveRuleByName，移除規則集合中的第一個規則。 方法 RemoveRuleByName 的規則名稱不區分大小寫。

## 參數

### -ActionType
指定要針對此規則的流量相符之情況採取的動作。 已接受的動作為「允許」或「拒絕」。

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此網路規則集合的名稱。 該名稱在所有網路規則集合中都必須是唯一的。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -優先順序
指定此規則集合的優先順序。 [優先順序] 是介於100和65000之間的數位。 數值越小，優先順序越高。

```yaml
Type: UInt32
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
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
Type: SwitchParameter
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
Type: SwitchParameter
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

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSFirewallNetworkRuleCollection 中的 [.]

## 筆記

## 相關連結

[新-AzureRmFirewallNetworkRule](./New-AzureRmFirewallNetworkRule.md)

[新-AzureRmFirewall](./New-AzureRmFirewall.md)

[AzureRmFirewall](./Get-AzureRmFirewall.md)
