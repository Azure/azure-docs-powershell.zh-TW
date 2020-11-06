---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: ecd5df4728e963e8bcf4614a6acb554fdbf17788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451444"
---
# Add-AzureRmRouteConfig

## 摘要
新增路由至路由表。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzureRmRouteConfig** Cmdlet 會將路由新增到 Azure 路由表。

## 示例

### 範例1：在路由表中新增路由
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

第一個命令會使用 Get-AzureRmRouteTable Cmdlet 來取得名為 RouteTable01 的路由表。
該命令會將資料表儲存在 $RouteTable 變數中。

第二個命令會將一個名為 Route13 的路由新增到儲存在 $RouteTable 的路由表中。
此路由會將資料包轉寄到本機虛擬網路。

### 範例2：使用管線將路由新增至路由資料表
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

這個命令會使用 **AzureRmRouteTable 取得** 名為 RouteTable01 的路由資料表。
命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。
目前的 Cmdlet 會新增名為 Route02 的路由，然後將結果傳遞到 **AzureRmRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。

## 參數

### -AddressPrefix
在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -名稱
指定要新增至路由資料表的路由名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopIpAddress
指定您新增至 Azure 虛擬網路的虛擬裝置的 IP 位址。
此路由會將資料包轉寄到該位址。
只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextHopType
指定此路由轉寄資料包的方式。
此參數可接受的值為：

- 互聯.
由 Azure 提供的預設 Internet 閘道。 
- 所有.
如果您指定這個值，路由就不會轉寄資料包。 
- VirtualAppliance.
您新增至 Azure 虛擬網路的虛擬裝置。 
- VirtualNetworkGateway.
Azure 伺服器對伺服器虛擬私人網路關。 
- VnetLocal.
[本機虛擬網路]。
如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTable
指定此 Cmdlet 將路由新增到哪個路由表。

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSRouteTable
形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值

## 輸出

### PSRouteTable 中的 [.]

## 筆記

## 相關連結

[AzureRmRouteConfig](./Get-AzureRmRouteConfig.md)

[AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[新-AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[移除-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Set-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)

[Set-AzureRmRouteTable](./Set-AzureRmRouteTable.md)


