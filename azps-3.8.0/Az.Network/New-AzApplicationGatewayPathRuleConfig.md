---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f06dbac5e7c7a67acc38c5357351905fab0ed141
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402553"
---
# New-AzApplicationGatewayPathRuleConfig

## 簡介
建立應用程式閘道路徑規則。

## 語法

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。
此 Cmdlet 所建立的規則可以新增到 URL 路徑地圖設定設定集合，然後指派給閘道。
路徑圖設定設定用於應用程式閘道負載平衡。

## 例子

### 範例 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

這些命令會建立新的應用程式閘道路徑規則，然後使用 **Add-AzApplicationGatewayUrlPathMapConfig** Cmdlet 將規則指派給應用程式閘道。
若要這麼做，第一個命令會建立閘道 ContosoApplicationGateway 的物件參照。
此物件參照會儲存在名為 $Gateway 的變數中。
接下來兩個命令會建立後端位址集區及後端 HTTP 設定物件;這些物件 (儲存在$AddressPool$HttpSettings) ，才能建立路徑規則物件。
第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。
第五個命令使用 **Add-AzApplicationGatewayUrlPathMapConfig，** 將設定設定和這些設定中包含的新路徑規則新增到 ContosoApplicationGateway。

### 範例 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

這些命令會建立路徑規則，名稱為"base"、Path as "/base"、後端AddressPool as $AddressPool、後端HttpSettings as $HttpSettings 和 FirewallPolicy as $firewallPolicy.ngs，以及這些設定中包含的新路徑規則至 ContosoApplicationGateway。

## 參數

### -後端AddressPool
指定要新增到閘道路徑規則設定設定之後端位址集區設定集合的物件參照。
您可以使用類似以下的 Cmdlet New-AzApplicationGatewayBackendAddressPool建立此物件參照： `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 到位址區段。
請注意，IP 位址會以引號括住，並且使用逗號分隔。
結果變數 $AddressPool，然後可以用來做為 *DefaultBackendAddressPool* 參數的參數值。
後端位址資料庫代表後端伺服器的 IP 位址。
這些 IP 位址應屬於虛擬網路子網，或應為公用 IP 位址。
如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendAddressPoolId* 參數。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -後端AddressPoolId
指定可以新加入閘道路徑規則設定設定的現有後端位址集區識別碼。
您可以使用 Cmdlet 來Get-AzApplicationGatewayBackendAddressPool位址。
在您擁有識別碼之後，就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。
例如：-DefaultBackendAddressPoolId"/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10 /resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/後端AddressPools/ContosoAddressPool" 後端位址資料庫代表後端伺服器的 IP 位址。
這些 IP 位址應屬於虛擬網路子網，或應為公用 IP 位址。

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -後端HttpSettings
指定要新加入閘道路徑規則設定設定之後端 HTTP 設定集合的物件參照。
您可以使用類似以下的 New-AzApplicationGatewayBackendHttpSettings Cmdlet 和語法來建立此物件參照：$HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "HTTP" -CookieBasedAffinity "Disabled" 產生的變數， $HttpSettings，然後可以用來做為 *DefaultBackendAddressPool* 參數的參數值：-DefaultBackendHttpSettings $HttpSettings 後端 HTTP 設定會為後端資料庫設定埠、通訊協定和 Cookie 型關聯等屬性。
如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendHttpSettingsId* 參數。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -後端HttpSettingsId
指定可以新加入閘道路徑規則設定設定的現有後端 HTTP 設定集合識別碼。
HTTP 設定 ID 可以使用 Cmdlet Get-AzApplicationGatewayBackendHttpSettings回。
在您擁有識別碼之後，就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。
例如：-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/後端HttpSettingsCollection/ContosoHttpSettings" 後端 HTTP 設定設定屬性，例如埠， 協定，以及後端資料庫的 Cookie 型關聯。
如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendHttpSettings* 參數。

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
指定頂層防火牆政策的物件參照。 您可以使用 Cmdlet 建立New-AzApplicationGatewayWebApplicationFirewallPolicy參照。
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 使用上述命令建立防火牆原則，可以在路徑規則層級中參考。 上方命令會建立預設原則設定及受管理規則。
使用者可以指定 PolicySettings、ManagedRules，而不使用預設值，New-AzApplicationGatewayFirewallPolicySettings和New-AzApplicationGatewayFirewallPolicyManagedRules設定。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
指定現有頂層 Web 應用程式防火牆資源的識別碼。
防火牆策略的 ID 可以使用 Get-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet。 當我們有識別碼之後，您可以使用 *FirewallPolicyId* 參數，而不是 *FirewallPolicy* 參數。
例如：-FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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
指定此 Cmdlet 建立的路徑規則組組名稱。

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

### -路徑
指定一或多個應用程式閘道路徑規則。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
應用程式閘道 RedirectConfiguration

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
應用程式閘道 RedirectConfiguration 的識別碼

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSet
應用程式閘道 RewriteRuleSet

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
應用程式閘道 RewriteRuleSet 的識別碼

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPathRule

## 筆記

## 相關連結

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)


[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


