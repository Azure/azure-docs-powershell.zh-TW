---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448354"
---
# New-AzureRmApplicationGateway

## 摘要
建立應用程式閘道。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmApplicationGateway** Cmdlet 會建立 Azure 應用程式閘道。
應用程式閘道需要下列各項：
- [資源] 群組。
- 虛擬網路。
- 後端伺服器池，包含後端伺服器的 IP 位址。
- 後端伺服器池設定。 每個池都有套用至池中所有伺服器的埠、通訊協定及 cookie 關聯性等設定。
- 前端 IP 位址，也就是在應用程式閘道開啟的 IP 位址。 前端 IP 位址可以是公用 IP 位址或內部 IP 位址。
- 前端埠，即是在應用程式閘道開啟的公用埠。 擊中這些埠的流量會重新導向到後端伺服器。
- 系結監聽器與後端伺服器池的要求路由規則。 規則會定義當通信量擊中特定的監聽程式時，應該會將它導向到哪個後端伺服器池。
偵聽程式有前端埠、前端 IP 位址、通訊協定 (HTTP 或 HTTPS) 以及安全通訊端層 (SSL) 憑證名 (如果設定 SSL 卸載) 。

## 示例

### 範例1：建立應用程式閘道
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

下列範例會先建立資源群組和虛擬網路，以及下列專案來建立應用程式閘道：
- 後端伺服器池
- 後端伺服器池設定
- 前端埠
- 前端 IP 位址
- 要求路由規則這四個命令會建立一個虛擬網路。
第一個命令會建立子網配置。
第二個命令會建立虛擬網路。
第三個命令會驗證子網設定，而第四個命令會驗證虛擬網路已順利建立。
下列命令會建立應用程式閘道。
第一個命令會為先前建立的子網建立名為 GatewayIp01 的 IP 配置。
第二個命令會使用後端 IP 位址清單來建立名為 Pool01 的後端伺服器池，並將該池儲存在 $Pool 變數中。
第三個命令會建立後端伺服器池的設定，並將設定儲存在 $PoolSetting 變數中。
第四個命令會在埠80建立前端埠，將它命名為 FrontEndPort01，並將埠儲存在 $FrontEndPort 變數中。
第五個命令會使用新的 AzureRmPublicIpAddress 建立公用 IP 位址。
第六個命令會使用 $PublicIp 建立前端 IP 設定，並將其命名為 FrontEndPortConfig01，並將它儲存在 $FrontEndIpConfig 變數中。
第七個命令會使用先前建立的 $FrontEndIpConfig $FrontEndPort 來建立偵聽程式。
第八個命令會建立監聽程式的規則。
第九個命令會設定 SKU。
第10個命令會使用先前命令所設定的物件來建立閘道。

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

### -AuthenticationCertificates
指定應用程式閘道的驗證憑證。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoscaleConfiguration
自動縮放設定

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendAddressPools
指定應用程式閘道的後端位址集區清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendHttpSettingsCollection
指定應用程式閘道的後端 HTTP 設定清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EnableFIPS
是否已啟用 FIPS。

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

### -EnableHttp2
是否已啟用 HTTP2。

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

### -FrontendIPConfigurations
指定應用程式閘道的前端 IP 配置清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FrontendPorts
指定應用程式閘道的前端埠清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewayIPConfigurations
指定應用程式閘道的 IP 配置清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HttpListeners
指定應用程式閘道的 HTTP 攔截器清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定要在其中建立應用程式閘道的區域。

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
指定應用程式閘道的名稱。

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

### -探針
指定應用程式閘道的探測器。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedirectConfigurations
重新導向配置清單

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequestRoutingRules
指定應用程式閘道的要求路由規則清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要在其中建立應用程式閘道的資源群組的名稱。

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

### -Sku
指定應用程式閘道 (SKU) 的庫存單位。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SslCertificates
指定 (SSL) 應用程式閘道憑證的安全通訊端層的清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SslPolicy
指定應用程式閘道的 SSL 原則。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
雜湊資料表形式的索引鍵/值對。 例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}

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

### -TrustedRootCertificate
受信任的根憑證清單

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UrlPathMaps
指定應用程式閘道的 URL 路徑對應。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApplicationFirewallConfiguration
指定 (WAF) 設定的 web 應用程式防火牆。 您可以使用 Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 來取得 WAF。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
顯示應用程式閘道需要來源之位置的可用性區域清單。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

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

### PSApplicationGatewaySku 中的 [.]

### PSApplicationGatewaySslPolicy 中的 [.]

### [System.object]. 清單 ' 1 [PSApplicationGatewayIPConfiguration，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewaySslCertificate，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayAuthenticationCertificate，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayFrontendIPConfiguration，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayFrontendPort，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayProbe，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayBackendAddressPool，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayBackendHttpSettings，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayHttpListener，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayUrlPathMap，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayRequestRoutingRule，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]. 清單 ' 1 [PSApplicationGatewayRedirectConfiguration，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]

### [System.object] 集合. Hashtable

## 輸出

### PSApplicationGateway 中的 [.]

## 筆記

## 相關連結

[新-AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[新-AzureRmApplicationGatewayBackendHttpSettings](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[新-AzureRmApplicationGatewayFrontendIPConfig](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[新-AzureRmApplicationGatewayFrontendPort](./New-AzureRmApplicationGatewayFrontendPort.md)

[新-AzureRmApplicationGatewayHttpListener](./New-AzureRmApplicationGatewayHttpListener.md)

[新-AzureRmApplicationGatewayIPConfiguration](./New-AzureRmApplicationGatewayIPConfiguration.md)

[新-AzureRmApplicationGatewayRequestRoutingRule](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[新-AzureRmApplicationGatewaySku](./New-AzureRmApplicationGatewaySku.md)

[新-AzureRmVirtualNetwork](./New-AzureRmVirtualNetwork.md)

[新-AzureRmVirtualNetworkSubnetConfig](./New-AzureRmVirtualNetworkSubnetConfig.md)
