---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284676"
---
# New-AzApplicationGatewayPathRuleConfig

## 摘要
建立應用程式閘道路徑規則。

## 句法

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

## 說明
**新的-AzApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。
您可以將由此 Cmdlet 建立的規則新增至 URL 路徑對應設定的集合，然後指派給閘道。
路徑對應設定是在應用程式閘道負載平衡中使用。

## 示例

### 範例1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

這些命令會建立新的應用程式閘道路徑規則，然後使用 **AzApplicationGatewayUrlPathMapConfig** Cmdlet 將該規則指派給應用程式閘道。
若要這樣做，第一個命令會建立對閘道 ContosoApplicationGateway 的物件參照。
這個物件參照會儲存在名為 $Gateway 的變數中。
接下來的兩個命令會建立後端位址集區和後端 HTTP 設定物件;這些物件 (儲存在 $AddressPool 變數中，而且需要 $HttpSettings) ，才能建立路徑規則物件。
第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。
第五個命令使用 [ **載入 AzApplicationGatewayUrlPathMapConfig** ]，將配置設定和包含在這些設定中的新路徑規則新增到 ContosoApplicationGateway。

### 範例2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

這些命令會建立名稱為 "base"、路徑為 "/base"、BackendAddressPool 為 $AddressPool 的路徑規則，BackendHttpSettings $HttpSettings 為 [ngs] 和 [$firewallPolicy FirewallPolicy]，將這些設定中所包含的新路徑規則加入 ContosoApplicationGateway。

## 參數

### -BackendAddressPool
指定要新增至 [閘道路徑規則設定] 的後端位址集區設定集合的物件參照。
您可以使用 New-AzApplicationGatewayBackendAddressPool Cmdlet 及如下所示的語法來建立此物件參照： `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 新增到位址集區中。
請注意，IP 位址括在引號中，並以逗號分隔。
產生的變數 $AddressPool，就可以用來做為 *DefaultBackendAddressPool* 參數的參數值。
後端位址集區代表後端伺服器上的 IP 位址。
這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。
如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendAddressPoolId* 參數。

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

### -BackendAddressPoolId
指定可新增至 [閘道路徑規則設定] 的現有後端位址集區 ID。
您可以使用 Get-AzApplicationGatewayBackendAddressPool Cmdlet 傳回位址集區識別碼。
在您擁有 ID 之後，您就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。
例如：-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 後端位址集區代表後端伺服器上的 IP 位址。
這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。

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

### -BackendHttpSettings
指定要新增至 [閘道路徑規則設定] 的後端 HTTP 設定集合的物件參照。
您可以使用 New-AzApplicationGatewayBackendHttpSettings Cmdlet 及如下所示的語法來建立此物件參照： $HttpSettings = New-AzApplicationGatewayBackendHttpSettings 名稱 "ContosoHttpSettings"-Port 80-通訊協定 "Http"-CookieBasedAffinity "Disabled" 所產生的變數（$HttpSettings）隨後可用作 *DefaultBackendAddressPool* 參數的參數值：-DefaultBackendHttpSettings $HttpSettings 後端 Http 設定會針對後端池設定屬性，例如埠、通訊協定和 cookie 的關聯性。
如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettingsId* 參數。

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

### -BackendHttpSettingsId
指定現有後端 HTTP 設定集合的識別碼，該集合可以新增至 [閘道路徑規則] 設定設定。
您可以使用 Get-AzApplicationGatewayBackendHttpSettings Cmdlet 傳回 HTTP 設定 Id。
在您擁有 ID 之後，您就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。
例如：-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 後端 HTTP 設定會為後端池設定屬性，例如埠、通訊協定及 cookie 的關聯性。
如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettings* 參數。

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
指定對頂層防火牆原則的物件參考。 您可以使用 New-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet 來建立物件參考。
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy 名稱 "wafPolicy1"-ResourceGroup "rgName" 使用上述的 commandlet 建立的防火牆原則，可以在 path 規則層級引用。 上述命令會建立預設的原則設定和受管理的規則。
使用者可以使用 New-AzApplicationGatewayFirewallPolicySettings 和 New-AzApplicationGatewayFirewallPolicyManagedRules 分別指定 PolicySettings、ManagedRules，而不是預設值。

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
指定現有最上層 web 應用程式防火牆資源的 ID。
您可以使用 Get-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet 傳回防火牆原則識別碼。 我們擁有 ID 之後，您可以使用 *FirewallPolicyId* 參數，而不是 *FirewallPolicy* 參數。
例如：-FirewallPolicyId "/subscriptions/<訂閱識別碼>/resourceGroups/<資源群組-識別碼>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

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
指定此 Cmdlet 所建立之路徑規則配置的名稱。

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
指定一個或多個應用程式閘道路徑規則。

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
應用程式閘道 RedirectConfiguration 的 ID

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
應用程式閘道 RewriteRuleSet 的 ID

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSApplicationGatewayPathRule 中的 [.]

## 筆記

## 相關連結

[附加 AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[AzApplicationGateway](./Get-AzApplicationGateway.md)

[AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[新-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[新-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[新-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[新-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[移除-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


