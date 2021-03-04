---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 961edb46c71b60f0c3c43523d8d88486f1414d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916054"
---
# Get-AzLocalNetworkGateway

## 簡介
獲得本地網路閘道

## 語法

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
Local Network Gateway 是代表您的 VPN 裝置內部部署的物件。
**Get-AzLocalNetworkGateway** Cmdlet 會根據名稱和資源組名，會返回代表您部署閘道的物件。

## 例子

### 範例 1：取得本地網路閘道
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

在資源群組 "myRG" 中，會返回名稱為 "myLocalGW1" 的 Local Network Gateway 物件

### 範例 2：使用篩選取得本地網路閘道
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

會以名稱從資源群組 "myRG" 內的 "myLocalGW" 開始，返回 Local Network 閘道的物件

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway

## 筆記

## 相關連結

[New-AzLocalNetworkGateway](./New-AzLocalNetworkGateway.md)

[Remove-AzLocalNetworkGateway](./Remove-AzLocalNetworkGateway.md)

[Set-AzLocalNetworkGateway](./Set-AzLocalNetworkGateway.md)
