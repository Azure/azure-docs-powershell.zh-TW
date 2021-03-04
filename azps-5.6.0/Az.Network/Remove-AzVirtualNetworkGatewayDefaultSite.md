---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915954"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## 簡介
從虛擬網路閘道移除預設網站。

## 語法

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Remove-AzVirtualNetworkGatewayDefaultSite** Cmdlet 會從虛擬網路閘道移除強制設置預設網站。
強制導向提供一種將受網際網路限制的流量從 Azure 虛擬機器重新導向到內部部署網路的方法;這可讓您在發行之前檢查和稽核流量。
使用虛擬私人網路或 VPN (進行強制) 部署;此管道需要預設網站，即重新導向所有 Azure 網際網路流量的一個本地閘道。
**Remove-AzVirtualNetworkGatewayDefaultSite** 會移除指派給閘道的預設網站。
如果您這麼做，您必須使用 Set-AzVirtualNetworkGatewayDefaultSite 指派新的預設網站，閘道才能用於強制呼叫。

## 例子

### 範例 1：移除指派給虛擬網路閘道的預設網站
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

此範例會移除目前指派給名為 ContosoVirtualGateway 之虛擬網路閘道的預設網站。
第一個命令 **使用 Get-AzVirtualNetworkGateway** 建立閘道的物件參照;此物件參照會儲存在名為 $Gateway 的$Gateway。
接著，第二個命令會使用 **Remove-AzVirtualNetworkGatewayDefaultSite** 來移除指派給該閘道的預設網站。

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

### -VirtualNetworkGateway
指定虛擬網路閘道的物件參照，其中包含要移除的預設網站。
您可以使用虛擬網路閘道建立物件參照Get-AzVirtualNetworkGateway指定閘道的名稱。

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

## 輸出

### Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway

## 筆記

## 相關連結

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


