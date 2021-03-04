---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4b2963d77d2182821bb4950907ef278950e410f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903461"
---
# Resize-AzVirtualNetworkGateway

## 簡介
調整現有虛擬網路閘道的大小。

## 語法

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Resize-AzVirtualNetworkGateway** Cmdlet 可讓您變更 (SKU) 的庫存單位。
SKUS 會決定閘道的功能，包括輸送量和允許的最大 IP 數量等。
Azure 支援基本、標準、高績效、VpnGw1、VpnGw2、VpnGw3、VpnGw1AZ、VpnGw2AZ、VpnGw3AZ、ErGw1AZ、ErGw2AZ、ErGw3AZ SKUS (有時稱為小型、中型和大型 SKUS) 。
有關每個 SKU 類型功能的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 。
請記住，SKUS 在定價和功能上有所不同。
詳細資訊請參閱 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 。

## 例子

### 範例 1：變更虛擬網路閘道的大小
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

此範例會變更名為 ContosoVirtualGateway 的虛擬網路閘道大小。
第一個命令會建立 ContosoVirtualGateway 的物件參照;此物件參照會儲存在名為 $Gateway 的$Gateway。
接著，第二個命令會使用 **Resize-AzVirtualNetworkGateway** Cmdlet 將 *GatewaySku* 屬性設為 Basic。

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

### -GatewaySku
指定新類型的閘道 SKU。
此參數可接受的值為：
- 基本
- 標準
- 高績效
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
指定要調整大小之虛擬網路閘道的物件參照。
您可以使用資料Get-AzVirtualNetworkGateway指定閘道名稱，以建立此物件參照。

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

### System.String

## 輸出

### Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway

## 筆記
您無法將基本/標準/HighPerformance SKUS 的大小調整為新的 VpnGw1/VpnGw2/VpnGw3 SKUS。 不允許進一步調整大小，從/到 VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 或 ErGw1AZ/ErGw2AZ/ErGw3AZ。 只有在 SKU 'series' 內允許調整大小，例如 VpnGw1AZ 可以調整大小至/從 VpnGw2AZ/VpnGw3AZ 和 ErGw1AZ 可以調整大小至/從 ErGw2AZ/ErGw3AZ。 請參閱 https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways 指示。

## 相關連結

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-Az VpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGateway VpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
