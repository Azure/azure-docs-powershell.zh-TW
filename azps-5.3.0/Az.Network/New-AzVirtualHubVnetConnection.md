---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438804"
---
# <span data-ttu-id="d5c71-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d5c71-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="d5c71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5c71-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c71-103">New-AzVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="d5c71-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="d5c71-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5c71-104">SYNTAX</span></span>

### <span data-ttu-id="d5c71-105">ByVirtualHubNameByRemoteVirtualNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d5c71-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c71-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c71-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c71-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="d5c71-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c71-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c71-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5c71-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="d5c71-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c71-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c71-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c71-111">說明</span><span class="sxs-lookup"><span data-stu-id="d5c71-111">DESCRIPTION</span></span>
<span data-ttu-id="d5c71-112">New-AzVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="d5c71-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="d5c71-113">示例</span><span class="sxs-lookup"><span data-stu-id="d5c71-113">EXAMPLES</span></span>

### <span data-ttu-id="d5c71-114">範例1</span><span class="sxs-lookup"><span data-stu-id="d5c71-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="d5c71-115">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="d5c71-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d5c71-116">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d5c71-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="d5c71-117">範例2</span><span class="sxs-lookup"><span data-stu-id="d5c71-117">Example 2</span></span>

<span data-ttu-id="d5c71-118">New-AzVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="d5c71-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="d5c71-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="d5c71-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="d5c71-120">範例3</span><span class="sxs-lookup"><span data-stu-id="d5c71-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="d5c71-121">上述將會建立新的路由設定，並在路由配置中使用下一個躍點作為指定 IP 位址來建立靜態路由。</span><span class="sxs-lookup"><span data-stu-id="d5c71-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="d5c71-122">然後，就可以使用參數 RoutingConfiguration，將這種路由設定傳遞到 [New-AzVirtualHubVnetConnection] 命令。</span><span class="sxs-lookup"><span data-stu-id="d5c71-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="d5c71-123">參數</span><span class="sxs-lookup"><span data-stu-id="d5c71-123">PARAMETERS</span></span>

### <span data-ttu-id="d5c71-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5c71-124">-AsJob</span></span>
<span data-ttu-id="d5c71-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d5c71-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5c71-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c71-126">-DefaultProfile</span></span>
<span data-ttu-id="d5c71-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5c71-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c71-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d5c71-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="d5c71-129">針對此連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="d5c71-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="d5c71-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="d5c71-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="d5c71-131">針對此連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="d5c71-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5c71-132">-Name</span></span>
<span data-ttu-id="d5c71-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d5c71-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d5c71-134">-ParentObject</span></span>
<span data-ttu-id="d5c71-135">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="d5c71-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c71-136">-ParentResourceId</span></span>
<span data-ttu-id="d5c71-137">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="d5c71-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d5c71-138">-ParentResourceName</span></span>
<span data-ttu-id="d5c71-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5c71-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d5c71-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="d5c71-141">此中樞虛擬網路連線所連結的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="d5c71-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d5c71-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="d5c71-143">此中樞虛擬網路連線所連結的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="d5c71-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c71-144">-ResourceGroupName</span></span>
<span data-ttu-id="d5c71-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5c71-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5c71-146">-RoutingConfiguration</span></span>
<span data-ttu-id="d5c71-147">此連線的路由設定</span><span class="sxs-lookup"><span data-stu-id="d5c71-147">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c71-148">-確認</span><span class="sxs-lookup"><span data-stu-id="d5c71-148">-Confirm</span></span>
<span data-ttu-id="d5c71-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5c71-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c71-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c71-150">-WhatIf</span></span>
<span data-ttu-id="d5c71-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5c71-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c71-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5c71-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c71-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c71-153">CommonParameters</span></span>
<span data-ttu-id="d5c71-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5c71-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c71-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5c71-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c71-156">輸入</span><span class="sxs-lookup"><span data-stu-id="d5c71-156">INPUTS</span></span>

### <span data-ttu-id="d5c71-157">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d5c71-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d5c71-158">System.object</span><span class="sxs-lookup"><span data-stu-id="d5c71-158">System.String</span></span>

## <span data-ttu-id="d5c71-159">輸出</span><span class="sxs-lookup"><span data-stu-id="d5c71-159">OUTPUTS</span></span>

### <span data-ttu-id="d5c71-160">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d5c71-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d5c71-161">筆記</span><span class="sxs-lookup"><span data-stu-id="d5c71-161">NOTES</span></span>

## <span data-ttu-id="d5c71-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5c71-162">RELATED LINKS</span></span>

[<span data-ttu-id="d5c71-163">AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d5c71-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="d5c71-164">移除-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d5c71-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="d5c71-165">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5c71-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
