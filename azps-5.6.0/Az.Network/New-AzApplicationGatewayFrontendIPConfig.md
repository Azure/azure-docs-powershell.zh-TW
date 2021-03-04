---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910698"
---
# New-AzApplicationGatewayFrontendIPConfig

## 簡介
為應用程式閘道建立前端 IP 組式。

## 語法

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzApplicationGatewayFrontendIPConfig** Cmdlet 會為 Azure 應用程式閘道建立前端 IP 組配置。
應用程式閘道支援兩種類型的前端 IP 組式： 
- 公用 IP 位址 -- 使用內部負載平衡的私人 IP 位址 (ILB) 。
 應用程式閘道最多隻能有一個公用 IP 位址和一個私人 IP 位址。
公用 IP 位址和私人 IP 位址應個別新增為前端 IP 位址。

## 例子

### 範例 1：使用公用 IP 資源物件建立前端 IP 組
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

第一個命令會建立公用 IP 資源物件，並儲存在$PublicIP變數中。
第二個命令$PublicIP建立名為 FrontEndIP01 的新前端 IP 組$FrontEnd變數。

### 範例 2：建立靜態私人 IP 做為前端 IP 位址
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。
第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。
第三個命令會使用第二個命令的 $Subnet 和私人 IP 位址 10.0.1.1 建立名為 FrontEndIP02 的前端 IP 組式，然後將它儲存在 $FrontEnd 變數中。

### 範例 3：建立動態私人 IP 做為前端 IP 位址
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

第一個命令會獲得一個名為 VNet01 的虛擬網路，該網路屬於名為 ResourceGroup01 的資源群組，並儲存在 $VNet 變數中。
第二個命令會使用第一個命令$VNet名為子網01 的子網組$Subnet變數。
第三個命令會使用第二個命令的 $Subnet 建立名為 FrontEndIP03 的前端 IP 組$FrontEnd變數。

## 參數

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所建立前端 IP 組名。

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

### -PrivateIPAddress
指定此 Cmdlet 與應用程式閘道前端 IP 位址關聯的私人 IP 位址。
只有在已指定子網時，才能指定這項功能。
此 IP 是從子網靜態配置。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
指定此 Cmdlet 與應用程式閘道前端 IP 位址關聯之公用 IP 位址物件。

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
指定此 Cmdlet 與應用程式閘道前端 IP 關聯之公用 IP 位址識別碼。

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -子網
指定此 Cmdlet 與應用程式閘道前端 IP 位址關聯之子網物件。
如果您指定此參數，表示閘道使用私人 IP 位址。
如果 *已指定 PrivateIPAddress* 參數，它應屬於此參數指定的子網。
如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -子網Id
指定此 Cmdlet 與應用程式閘道前端 IP 組配置的關聯子網識別碼。
如果您指定 *子網參數* ，表示閘道使用私人 IP 位址。
如果 *已指定 PrivateIPAddress* 參數，它應屬於子網指定的 *子網*。
如果 *未指定 PrivateIPAddress，* 此子網的其中一個 IP 位址會動態取用為應用程式閘道的前端 IP 位址。

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendIPConfiguration

## 筆記

## 相關連結

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


