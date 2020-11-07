---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802249"
---
# Resize-AzureRmVirtualNetworkGateway

## 摘要
重新調整現有虛擬網路閘道的大小。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
重 **設大小 AzureRmVirtualNetworkGateway** Cmdlet 能讓您變更虛擬閘道 (SKU) 的庫存單位。
Sku 決定閘道的功能，包括輸送量與允許的 IP 隧道數目上限等。
Azure 支援基本、標準、高效能、VpnGw1、VpnGw2 和 VpnGw3 Sku， (有時稱為小型、中型及大型 Sku) 。
如需有關每個 SKU 類型之功能的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 。

請記住，Sku 與定價及功能有不同。
如需詳細資訊，請參閱 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 。

## 示例

### 範例1：變更虛擬閘道的大小
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

這個範例會變更名為 ContosoVirtualGateway 的虛擬網路閘道的大小。

第一個命令會建立 ContosoVirtualGateway 的物件參照;這個物件參照會儲存在名為 $Gateway 的變數中。

然後，第二個命令會使用 **AzureRmVirtualNetworkGateway** Cmdlet，將 *GatewaySku* 屬性設為 Basic。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewaySku
指定新的閘道 SKU 類型。
此參數可接受的值為：

- 空白
- 標準
- 高效能
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
指定要調整其大小的虛擬網路閘道物件參照。
您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱來建立此物件參照。

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

###  
這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。

## 輸出

###  
這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。

## 筆記
您無法將基本/標準/HighPerformance Sku 的大小調整成新的 VpnGw1/VpnGw2/VpnGw3 Sku。 https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways如需相關指示，請參閱。

## 相關連結

[AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


