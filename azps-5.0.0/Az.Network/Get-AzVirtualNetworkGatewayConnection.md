---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139782"
---
# Get-AzVirtualNetworkGatewayConnection

## 摘要
取得虛擬網路閘道連線

## 句法

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
虛擬網路閘道連線是代表連接至 Azure 中虛擬網路閘道的 IPsec 隧道 (點對點或 Vnet 到 Vnet) 的物件。
**AzVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源群組名稱，傳回連線物件。
如果未指定-Name 參數就發出 **AzVirtualNetworkGatewayConnection** Cmdlet，則輸出將不會顯示 ConnectionStatus 和 SharedKey 詳細資料。

## 示例

### 1：取得虛擬網路閘道連線
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

傳回資源群組 "myRG" 中名稱為 "myTunnel" 的虛擬網路閘道連線物件

### 2：使用篩選來取得所有虛擬網路閘道連線
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

傳回在資源群組 "myRG" 中以 "myTunnel" 為開頭的所有虛擬網路閘道連接

## 參數

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

### -名稱
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSVirtualNetworkGatewayConnection 中的 [.]

## 筆記

## 相關連結

[新-AzVirtualNetworkGatewayConnection](./New-AzVirtualNetworkGatewayConnection.md)

[移除-AzVirtualNetworkGatewayConnection](./Remove-AzVirtualNetworkGatewayConnection.md)

[Set-AzVirtualNetworkGatewayConnection](./Set-AzVirtualNetworkGatewayConnection.md)
