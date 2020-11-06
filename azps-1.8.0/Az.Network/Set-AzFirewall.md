---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621460"
---
# Set-AzFirewall

## 摘要
儲存已修改的防火牆。

## 句法

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzFirewall** Cmdlet 會更新 Azure 防火牆。

## 示例

### 1：更新防火牆應用程式規則集合的優先順序
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

此範例更新現有的 Azure 防火牆規則集合的優先順序。
假設資源群組 "rg" 中的 Azure 防火牆「AzureFirewall」包含名為「ruleCollectionName」的應用程式規則集合，則上述命令將會變更該規則集合的優先順序，之後就會更新 Azure 防火牆。 如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。

### 2：建立 Azure 防火牆並稍後設定應用程式規則集合
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

在這個範例中，首先會建立不含任何應用程式規則集合的防火牆。 接著會建立應用程式規則和應用程式規則集合，然後在記憶體中修改 Firewall 物件，而不會影響雲端的實際設定。 若要在雲端反射的變更，必須呼叫 Set-AzFirewall。

### 3：更新 Microsoft Azure 防火牆的 [Intel 作業] 模式
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

這個範例會更新資源群組 "rg" 中的 Azure 防火牆 "AzureFirewall" 的威脅 Intel 作業模式。
如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。

## 參數

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

### -AzureFirewall
AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSAzureFirewall 中的 [.]

## 輸出

### PSAzureFirewall 中的 [.]

## 筆記

## 相關連結

[AzFirewall](./Get-AzFirewall.md)

[新-AzFirewall](./New-AzFirewall.md)

[移除-AzFirewall](./Remove-AzFirewall.md)
