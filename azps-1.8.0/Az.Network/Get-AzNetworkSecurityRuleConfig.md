---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: f861c1589d6f35c9650f0c20800b577e1724d66b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621982"
---
# Get-AzNetworkSecurityRuleConfig

## 摘要
取得網路安全性群組的網路安全規則配置。

## 句法

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzNetworkSecurityRuleConfig** Cmdlet 會取得 Azure 網路安全性群組的網路安全規則配置。

## 示例

### 1：檢索網路安全規則 config
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

這個命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure network security 群組中，檢索名為 "AllowInternetOutBound" 的預設規則。

### 2：只使用名稱來檢索網路安全規則配置
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

這個命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure 網路安全性群組中，檢索名為 "rdp-tcp 規則" 的使用者定義規則

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

### -DefaultRules
指示此 Cmdlet 是否會取得使用者建立的規則設定或預設規則設定。

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

### -名稱
指定要取得的網路安全規則配置名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
指定包含要取得之網路安全性規則配置的 **NetworkSecurityGroup** 物件。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSNetworkSecurityGroup 中的 [.]

## 輸出

### PSSecurityRule 中的 [.]

## 筆記

## 相關連結

[附加 AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[新-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[移除-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


