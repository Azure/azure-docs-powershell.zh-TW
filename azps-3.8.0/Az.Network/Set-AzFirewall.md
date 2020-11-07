---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 36ba29104fbc9e87ae2776504dc48bed8a5b9ffa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957273"
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

### 4：解除配置並指派防火牆
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
這個範例會檢索防火牆、解除防火牆的釋放並儲存防火牆。 解除配置命令會移除執行中的服務，但會保留防火牆的設定。 若要在雲端反射的變更，必須呼叫 Set-AzFirewall。
如果使用者想要再次啟動服務，請在防火牆上呼叫 Allocate 方法。
新的 VNet 和公用 IP 必須與防火牆在相同的資源群組中。 同樣地，若要在雲端中反映變更，必須呼叫 Set-AzFirewall。

### 5：使用強制隧道案例的管理公用 IP 位址進行配置
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
這個範例會將防火牆與管理公用 IP 位址和子網結合在一起，以進行強制隧道案例的配置。 VNet 必須包含一個名為 "AzureFirewallManagementSubnet" 的子網。

### 6：將公用 IP 位址新增至 Azure 防火牆
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

在這個範例中，公用 IP 位址 "azFwPublicIp1" 已附加到防火牆。

### 7：從 Azure 防火牆移除公用 IP 位址
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

在這個範例中，公用 IP 位址「azFwPublicIp1」已從防火牆中分離。

### 8：變更 Azure 防火牆上的管理公用 IP 位址
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

在這個範例中，防火牆的管理公用 IP 位址會變更為 "AzFwMgmtPublicIp2"


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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSAzureFirewall 中的 [.]

## 輸出

### PSAzureFirewall 中的 [.]

## 筆記

## 相關連結

[AzFirewall](./Get-AzFirewall.md)

[新-AzFirewall](./New-AzFirewall.md)

[移除-AzFirewall](./Remove-AzFirewall.md)
