---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128810"
---
# <span data-ttu-id="edd5b-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="edd5b-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="edd5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="edd5b-103">建立 VHubRoute 物件，該物件可以作為參數傳遞到 New-AzVHubRouteTable 命令。</span><span class="sxs-lookup"><span data-stu-id="edd5b-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="edd5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="edd5b-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd5b-105">說明</span><span class="sxs-lookup"><span data-stu-id="edd5b-105">DESCRIPTION</span></span>

<span data-ttu-id="edd5b-106">建立 VHubRoute 物件。</span><span class="sxs-lookup"><span data-stu-id="edd5b-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="edd5b-107">示例</span><span class="sxs-lookup"><span data-stu-id="edd5b-107">EXAMPLES</span></span>

### <span data-ttu-id="edd5b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="edd5b-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="edd5b-109">上述命令會建立一個 VHubRoute 物件，並以 nextHop 作為指定的防火牆，然後再將它新增到 VHubRouteTable 資源。</span><span class="sxs-lookup"><span data-stu-id="edd5b-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="edd5b-110">範例2</span><span class="sxs-lookup"><span data-stu-id="edd5b-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="edd5b-111">上述命令會建立一個 VHubRoute 物件，並以 nextHop 作為指定 hubVnetConnection，然後再將它新增至 VHubRouteTable 資源。</span><span class="sxs-lookup"><span data-stu-id="edd5b-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="edd5b-112">範例3</span><span class="sxs-lookup"><span data-stu-id="edd5b-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="edd5b-113">上述命令會取得已存在 AzVHubRoute 的 RoutingConfiguration，然後在連線上新增靜態路由。</span><span class="sxs-lookup"><span data-stu-id="edd5b-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="edd5b-114">或者，如果您想要使用其中的靜態路由建立新的連線，請參閱這裡的範例 1 [。](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="edd5b-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="edd5b-115">參數</span><span class="sxs-lookup"><span data-stu-id="edd5b-115">PARAMETERS</span></span>

### <span data-ttu-id="edd5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd5b-116">-DefaultProfile</span></span>
<span data-ttu-id="edd5b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edd5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd5b-118">-目的地</span><span class="sxs-lookup"><span data-stu-id="edd5b-118">-Destination</span></span>
<span data-ttu-id="edd5b-119">目的地清單。</span><span class="sxs-lookup"><span data-stu-id="edd5b-119">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5b-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="edd5b-120">-DestinationType</span></span>
<span data-ttu-id="edd5b-121">目的地類型。</span><span class="sxs-lookup"><span data-stu-id="edd5b-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="edd5b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="edd5b-122">-Name</span></span>
<span data-ttu-id="edd5b-123">路由名稱。</span><span class="sxs-lookup"><span data-stu-id="edd5b-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5b-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="edd5b-124">-NextHop</span></span>
<span data-ttu-id="edd5b-125">下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="edd5b-125">The next hop.</span></span>

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

### <span data-ttu-id="edd5b-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="edd5b-126">-NextHopType</span></span>
<span data-ttu-id="edd5b-127">下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="edd5b-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="edd5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd5b-128">CommonParameters</span></span>
<span data-ttu-id="edd5b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edd5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd5b-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="edd5b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd5b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="edd5b-131">INPUTS</span></span>

### <span data-ttu-id="edd5b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="edd5b-132">System.String</span></span>

## <span data-ttu-id="edd5b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="edd5b-133">OUTPUTS</span></span>

### <span data-ttu-id="edd5b-134">PSVHubRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="edd5b-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="edd5b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="edd5b-135">NOTES</span></span>

## <span data-ttu-id="edd5b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="edd5b-136">RELATED LINKS</span></span>

[<span data-ttu-id="edd5b-137">AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="edd5b-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="edd5b-138">新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="edd5b-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="edd5b-139">移除-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="edd5b-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="edd5b-140">更新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="edd5b-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)