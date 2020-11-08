---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139979"
---
# New-AzVirtualHub

## 摘要
建立 Azure VirtualHub 資源。

## 句法

### ByVirtualWanObject (預設) 
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualWanResourceId
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
建立 Azure VirtualHub 資源。

## 示例

### 範例1

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。 虛擬中樞會將位址空間 "10.0.1.0/24"。

### 範例2

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。 虛擬中樞會將位址空間 "10.0.1.0/24"。 

這個範例與範例1類似，但使用資源識別碼來參照建立虛擬中樞所需的虛擬 WAN。

### 範例3

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。 虛擬中樞會將位址空間 "10.0.1.0/24" 和附加路由表。

這個範例與範例2類似，但也會將路由資料表附加至虛擬中樞。

## 參數

### -AddressPrefix
此虛擬中樞的位址空間字串。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HubVnetConnection
與此虛擬中樞相關聯的中心虛擬網路連線。

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
位於.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
資源名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RouteTable
與此虛擬中樞相關聯的路由表。

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
虛擬中樞的 sku。

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

### -Tag
代表資源標記的 hashtable。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualWan
此中樞所連結的虛擬 wan 物件。

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualWanId
此中樞所連結的虛擬 wan 物件的識別碼。

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSVirtualWan 中的 [.]

### System.object

## 輸出

### PSVirtualHub 中的 [.]

## 筆記

## 相關連結

[AzVirtualHub](./Get-AzVirtualHub.md)

[移除-AzVirtualHub](./Remove-AzVirtualHub.md)

[更新-AzVirtualHub](./Update-AzVirtualHub.md)
