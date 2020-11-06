---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448292"
---
# Set-AzureRmVirtualNetworkGatewayVpnClientConfig

## 摘要
為虛擬網路閘道設定 VPN 用戶端位址集區。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 預設 (預設) 
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RadiusServerConfiguration
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
AzureRmVirtualNetworkVpnClientConfig Cmdlet 會為虛擬網路閘道 **設定** 用戶端位址集區。
虛擬私人網路絡 (VPN) 連線至此閘道的用戶端，都會從該位址集區中指派 IP 位址。

## 示例

### 範例1：將 VPN 用戶端位址集區指派給虛擬網路閘道
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

這個範例會將 VPN 用戶端位址集區指派給名為 ContosoVirtualGateway 的虛擬網路閘道。
第一個命令會建立閘道的物件參照，而物件會儲存在名為 $Gateway 的變數中。
接著，這個範例中的第二個命令會使用 **AzureRmVirtualNetworkGatewayVpnClientConfig** Cmdlet 來指派位址集區 10.0.0.0/16 到 ContosoVirtualGateway。

### 範例2：在現有閘道設定外部 radius 驗證
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

這個範例會將 VPN 用戶端位址集區指派給名為 ContosoVirtualGateway 的虛擬網路閘道。
第一個命令會建立閘道的物件參照，而物件會儲存在名為 $Gateway 的變數中。
接著，這個範例中的第二個命令會使用 **AzureRmVirtualNetworkGatewayVpnClientConfig** Cmdlet 來指派位址集區 10.0.0.0/16 到 ContosoVirtualGateway。 它也會將外部 radius 伺服器「TestRadiusServer」設定為用於 vpn 用戶端的驗證。

## 參數

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

### -RadiusServerAddress
P2S 外部 Radius 伺服器位址。

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerSecret
P2S [外部 Radius 伺服器] 密碼。

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
指定包含此 Cmdlet 所修改之 VPN 用戶端配置設定的虛擬網路閘道物件參照。
您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱，以建立虛擬閘道的物件參考。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnClientAddressPool
指定要指派給連接至此閘道之用戶端的 IP 位址

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
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

### PSVirtualNetworkGateway 中的 [.]
參數： VirtualNetworkGateway (ByValue) 

### [System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

### System.object

### SecureString

## 輸出

### PSVirtualNetworkGateway 中的 [.]

## 筆記

## 相關連結

[AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[調整大小-AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)


