---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 42592e1d72303c98a27890e2ac7721d95c37f928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905870"
---
# <span data-ttu-id="e02a2-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e02a2-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e02a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e02a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e02a2-103">Cmdlet New-AzVirtualHubVnetConnection建立 HubVirtualNetworkConnection 資源，將虛擬網路對等至 Azure 虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="e02a2-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="e02a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="e02a2-104">SYNTAX</span></span>

### <span data-ttu-id="e02a2-105">ByVirtualHubNameByRemoteVirtualNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="e02a2-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02a2-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e02a2-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02a2-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e02a2-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02a2-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e02a2-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e02a2-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e02a2-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02a2-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e02a2-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e02a2-111">描述</span><span class="sxs-lookup"><span data-stu-id="e02a2-111">DESCRIPTION</span></span>
<span data-ttu-id="e02a2-112">Cmdlet New-AzVirtualHubVnetConnection建立 HubVirtualNetworkConnection 資源，將虛擬網路對等至 Azure 虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="e02a2-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="e02a2-113">例子</span><span class="sxs-lookup"><span data-stu-id="e02a2-113">EXAMPLES</span></span>

### <span data-ttu-id="e02a2-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="e02a2-114">Example 1</span></span>

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

<span data-ttu-id="e02a2-115">上述步驟將在 Azure 的資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中心的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="e02a2-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e02a2-116">在此之後，將會建立一個虛擬網路連接，將虛擬網路對等至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="e02a2-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="e02a2-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="e02a2-117">Example 2</span></span>

<span data-ttu-id="e02a2-118">Cmdlet New-AzVirtualHubVnetConnection建立 HubVirtualNetworkConnection 資源，將虛擬網路對等至 Azure 虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="e02a2-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="e02a2-119"> (自動) </span><span class="sxs-lookup"><span data-stu-id="e02a2-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="e02a2-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="e02a2-120">Example 3</span></span>
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
<span data-ttu-id="e02a2-121">上述步驟會建立新的路由組式，在路由設定檔中建立靜態路由，下一個躍點會做為指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e02a2-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="e02a2-122">然後，這個路由設定可以傳遞至 New-AzVirtualHubVnetConnection 命令做為參數 -RoutingConfiguration。</span><span class="sxs-lookup"><span data-stu-id="e02a2-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="e02a2-123">參數</span><span class="sxs-lookup"><span data-stu-id="e02a2-123">PARAMETERS</span></span>

### <span data-ttu-id="e02a2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e02a2-124">-AsJob</span></span>
<span data-ttu-id="e02a2-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e02a2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e02a2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02a2-126">-DefaultProfile</span></span>
<span data-ttu-id="e02a2-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e02a2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02a2-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e02a2-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="e02a2-129">啟用此連接的網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="e02a2-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="e02a2-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="e02a2-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="e02a2-131">啟用此連接的網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="e02a2-131">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="e02a2-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="e02a2-132">-Name</span></span>
<span data-ttu-id="e02a2-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e02a2-133">The resource name.</span></span>

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

### <span data-ttu-id="e02a2-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e02a2-134">-ParentObject</span></span>
<span data-ttu-id="e02a2-135">父資源。</span><span class="sxs-lookup"><span data-stu-id="e02a2-135">The parent resource.</span></span>

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

### <span data-ttu-id="e02a2-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e02a2-136">-ParentResourceId</span></span>
<span data-ttu-id="e02a2-137">父資源。</span><span class="sxs-lookup"><span data-stu-id="e02a2-137">The parent resource.</span></span>

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

### <span data-ttu-id="e02a2-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e02a2-138">-ParentResourceName</span></span>
<span data-ttu-id="e02a2-139">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e02a2-139">The resource group name.</span></span>

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

### <span data-ttu-id="e02a2-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e02a2-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="e02a2-141">此中樞虛擬網路連接所連接的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e02a2-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="e02a2-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e02a2-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="e02a2-143">此中樞虛擬網路連接所連接的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e02a2-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="e02a2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02a2-144">-ResourceGroupName</span></span>
<span data-ttu-id="e02a2-145">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e02a2-145">The resource group name.</span></span>

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

### <span data-ttu-id="e02a2-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e02a2-146">-RoutingConfiguration</span></span>
<span data-ttu-id="e02a2-147">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="e02a2-147">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="e02a2-148">-確認</span><span class="sxs-lookup"><span data-stu-id="e02a2-148">-Confirm</span></span>
<span data-ttu-id="e02a2-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e02a2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e02a2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02a2-150">-WhatIf</span></span>
<span data-ttu-id="e02a2-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e02a2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02a2-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e02a2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e02a2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02a2-153">CommonParameters</span></span>
<span data-ttu-id="e02a2-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e02a2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02a2-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e02a2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02a2-156">輸入</span><span class="sxs-lookup"><span data-stu-id="e02a2-156">INPUTS</span></span>

### <span data-ttu-id="e02a2-157">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e02a2-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e02a2-158">System.String</span><span class="sxs-lookup"><span data-stu-id="e02a2-158">System.String</span></span>

## <span data-ttu-id="e02a2-159">輸出</span><span class="sxs-lookup"><span data-stu-id="e02a2-159">OUTPUTS</span></span>

### <span data-ttu-id="e02a2-160">Microsoft.Azure.Commands.Network.models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e02a2-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e02a2-161">筆記</span><span class="sxs-lookup"><span data-stu-id="e02a2-161">NOTES</span></span>

## <span data-ttu-id="e02a2-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="e02a2-162">RELATED LINKS</span></span>

[<span data-ttu-id="e02a2-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e02a2-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e02a2-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e02a2-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e02a2-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e02a2-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
