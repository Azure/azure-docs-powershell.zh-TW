---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 5a2490e25d42e6285183d1f78182ce0d7c92f02f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451600"
---
# Remove-AzureRmVirtualNetworkGatewayDefaultSite

## 摘要
從虛擬網路閘道移除預設網站。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVirtualNetworkGatewayDefaultSite** Cmdlet 會從虛擬網路閘道中移除強制隧道預設網站。
強制隧道提供一種將網際網路系結流量從 Azure 虛擬機器重新導向到您的內部部署網路的方式;這可讓您在釋放流量前先檢查並進行審核。
強制隧道是使用虛擬私人網路絡 (VPN) 隧道來執行;這個隧道需要一個預設的網站，即會重新導向所有 Azure 網際網路系結流量的本機閘道。

**移除-AzureRmVirtualNetworkGatewayDefaultSite** 會移除指派給閘道的預設網站。
如果您這麼做，您將需要使用 Set-AzureRmVirtualNetworkGatewayDefaultSite 來指派新的預設網站，然後才能將閘道用於強制性隧道。

## 示例

### 範例1：移除指派給虛擬網路閘道的預設網站
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

這個範例會移除目前指派給名為 ContosoVirtualGateway 的虛擬網路閘道的預設網站。

第一個命令使用 **AzureRmVirtualNetworkGateway** 來建立閘道的物件參照;這個物件參照會儲存在名為 $Gateway 的變數中。

然後，第二個命令會使用 **移除 AzureRmVirtualNetworkGatewayDefaultSite** 來移除指派給該閘道的預設網站。

## 參數

### -VirtualNetworkGateway
指定包含要移除之預設網站之虛擬網路閘道的物件參照。
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

###  
這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。

## 輸出

###  
這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。

## 筆記

## 相關連結

[AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayDefaultSite](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


