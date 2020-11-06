---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447346"
---
# New-AzureRmVirtualNetworkSubnetConfig

## 摘要
建立虛擬網路子網配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### SetByResource (預設) 
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmVirtualNetworkSubnetConfig** Cmdlet 會建立虛擬網路子網配置。

## 示例

### 1：使用兩個子網和網路安全群組建立虛擬網路
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

這個範例會使用 New-AzureRmVirtualSubnetConfig Cmdlet 建立兩個新的子網設定，然後使用它們來建立虛擬網路。 New-AzureRmVirtualSubnetConfig 範本只會建立子網的記憶體內部表示。 在這個範例中，frontendSubnet 有 CIDR 10.0.1.0/24，並參照允許 RDP 存取的網路安全性群組。 BackendSubnet 有 CIDR 10.0.2.0/24，且參照相同的網路安全性群組。

## 參數

### -AddressPrefix
指定子網配置的 IP 位址範圍。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### 委派
具有在該子網上執行作業許可權的服務清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要建立的子網配置名稱。

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

### -NetworkSecurityGroup
指定 NetworkSecurityGroup 物件。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkSecurityGroupId
指定網路安全性群組的 ID。

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTable
指定與子網配置相關聯的路由表。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTableId
指定與子網配置相關聯之路由資料表的識別碼。

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
服務端點值

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpointPolicy
服務端點原則

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### PSNetworkSecurityGroup 中的 [.]

### PSRouteTable 中的 [.]

### [System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

### [System.object]. 清單 ' 1 [PSServiceEndpointPolicy，6.7.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。

### [System.object]。清單 ' 1 [Microsoft.Azure.Commands.Network.Models.PSDelegation，6.7.0.0 "Network，版本 =，Culture = 中性，PublicKeyToken = null]]

## 輸出

### PSSubnet 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmVirtualNetworkSubnetConfig](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[移除-AzureRmVirtualNetworkSubnetConfig](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[Set-AzureRmVirtualNetworkSubnetConfig](./Set-AzureRmVirtualNetworkSubnetConfig.md)


