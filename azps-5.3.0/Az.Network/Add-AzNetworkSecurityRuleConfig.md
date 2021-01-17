---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436378"
---
# Add-AzNetworkSecurityRuleConfig

## 摘要
新增網路安全規則設定至網路安全性群組。

## 句法

### SetByResource (預設) 
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzNetworkSecurityRuleConfig** Cmdlet 會將網路安全規則設定新增至 Azure 網路安全性群組。

## 示例

### 1：新增網路安全性群組
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

第一個命令會從資源群組 "rg1" 檢索名為 "nsg1" 的 Azure 網路安全性群組。 第二個命令會將一個名為「rdp-rule」的網路安全規則新增，允許從埠3389上的網際網路通訊到檢索到的網路安全群組物件。 保持已修改的 Azure 網路安全性群組。

### 2：使用應用程式安全性群組新增新的安全性規則
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

首先，我們會建立兩個新的應用程式安全性群組。 接著，我們會從資源群組「rg1」檢索名為「nsg1」的 Azure 網路安全性群組。 然後將名為 "rdp-rule" 的網路安全性規則新增至它。 此規則允許從應用程式安全性群組 "srcAsg" 中的所有 IP 設定到埠3389上 "destAsg" 的所有 ip 設定的流量。 新增規則之後，我們會保留已修改的 Azure 網路安全性群組。

## 參數

### -Access
指定是否允許或拒絕網路流量。
此參數可接受的值為： [允許] 和 [拒絕]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

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

### -描述
指定網路安全規則配置的描述。

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

### -DestinationAddressPrefix
指定目的地位址首碼。
此參數可接受的值為：
- 未類別的域間路由 (CIDR) 位址
- 目的地 IP 位址範圍
- 萬用字元 ( * ) 若要與任何 IP 位址相符，您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
針對規則設定為目的地的應用程式安全性群組。 它不能與 "DestinationAddressPrefix" 參數搭配使用。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
針對規則設定為目的地的應用程式安全性群組。 它不能與 "DestinationAddressPrefix" 參數搭配使用。

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
指定目的地埠或範圍。
此參數可接受的值為：
- 整數
- 0到65535之間的整數範圍
- 萬用字元 ( * ) 與任何埠相符

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 方向
指定是否要針對傳入或傳出流量評估規則。
此參數可接受的值為：入站和出站。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定網路安全規則配置的名稱。

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
指定 **NetworkSecurityGroup** 物件。
這個 Cmdlet 會將網路安全規則設定新增至此參數指定的物件。

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

### -優先順序
指定規則配置的優先順序。
此參數可接受的值為：100和4096之間的整數。
對於集合中的每個規則，優先順序編號必須是唯一的。
優先順序編號越低，規則的優先順序就越高。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
指定規則配置適用的網路通訊協定。
此參數可接受的值為：
- Tcp-out
- Udp-in
- 萬用字元 ( * ) 與以上兩個相符

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
指定來源位址首碼。
此參數可接受的值為：
- CIDR
- 來源 IP 範圍
- 通配字元 ( * ) ，以符合任何 IP 位址。
您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
針對規則設定為 [來源] 的應用程式安全性群組。 它不能與 "SourceAddressPrefix" 參數搭配使用。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
針對規則設定為 [來源] 的應用程式安全性群組。 它不能與 "SourceAddressPrefix" 參數搭配使用。

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
指定來源埠或範圍。
這個值會以整數表示，以0到65535之間的範圍，或以萬用字元字元 ( * ) 來與任何來源埠相符。

```yaml
Type: System.String[]
Parameter Sets: (All)
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

### PSNetworkSecurityGroup 中的 [.]

## 輸出

### PSNetworkSecurityGroup 中的 [.]

## 筆記

## 相關連結

[AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[新-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[移除-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


