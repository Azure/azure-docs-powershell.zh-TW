---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446712"
---
# Set-AzureRmVirtualNetworkPeering

## 摘要
配置虛擬網路對等。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzureRmVirtualNetworkPeering Cmdlet 會 **設定** 虛擬網路對等。

## 示例

### 範例1：變更虛擬網路對等的轉寄流量設定
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### 範例2：變更虛擬網路對等的虛擬網路存取權
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### 範例3：變更虛擬網路對等的閘道中轉屬性設定
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### 範例4：在虛擬網路對等中使用遠端閘道
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

透過將此屬性變更為 $True，就可以使用對等的 VNet 閘道。
不過，對等 VNet 必須已設定閘道，且 **AllowGatewayTransit** 必須具有 $True 的值。

如果已設定閘道，則無法使用此屬性。

## 參數

### -VirtualNetworkPeering
指定虛擬網路對等。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSVirtualNetworkPeering
形參 "VirtualNetworkPeering" 接受管線中 "PSVirtualNetworkPeering" 類型的值

## 輸出

### PSVirtualNetworkPeering 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmVirtualNetworkPeering](./Add-AzureRmVirtualNetworkPeering.md)

[AzureRmVirtualNetworkPeering](./Get-AzureRmVirtualNetworkPeering.md)

[移除-AzureRmVirtualNetworkPeering](./Remove-AzureRmVirtualNetworkPeering.md)


