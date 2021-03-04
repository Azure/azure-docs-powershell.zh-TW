---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908782"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## 簡介
設定虛擬網路閘道的預設網站。

## 語法

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-AzVirtualNetworkGatewayDefaultSite** Cmdlet 會指派強制設定預設網站至虛擬網路閘道。
強制導向提供一種將受網際網路限制的流量從 Azure 虛擬機器重新導向到內部部署網路的方法;這可讓您在發行之前檢查和稽核流量。
使用虛擬私人網路或 VPN (進行強制) 部署;此管道需要預設網站，即重新導向所有 Azure 網際網路流量的一個本地閘道。
**Set-AzVirtualNetworkGatewayDefaultSite** 提供變更指派給閘道的預設網站的方法。

## 例子

### 範例 1：將預設網站指派給虛擬網路閘道
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

此範例會指派預設網站給名為 ContosoVirtualGateway 的虛擬網路閘道。
第一個命令會建立名為 ContosoLocalGateway 之本地閘道的物件參照。
儲存在名為 $LocalGateway 的變數中的這個物件參照代表要當做預設網站的閘道。
接著，第二個命令會建立虛擬網路閘道的物件參照，然後將結果儲存在名為 $VirtualGateway 的變數中。
第三個命令使用 **Set-AzVirtualNetworkGatewayDefaultSite** Cmdlet 將預設網站指派給 ContosoVirtualGateway。

## 參數

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

### -GatewayDefaultSite
指定要指派為指定之虛擬網路預設網站之本地網路閘道的物件參照。
您可以使用 Get-AzLocalNetworkGateway Cmdlet 建立本地閘道的物件參照。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
指定將指派預設網站之虛擬網路閘道的物件參照。
您可以使用 **Get-AzVirtualNetworkGateway** 並指定閘道名稱，來建立虛擬網路閘道的物件參照。
然後$VirtualGateway變數做為 *VirtualNetworkGateway* 參數的參數值：

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway

### Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway

## 輸出

### Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway

## 筆記

## 相關連結

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


