---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 3089d3654e471bbf31eb81e42e4374525d84010d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907617"
---
# <span data-ttu-id="b7de3-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="b7de3-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="b7de3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7de3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7de3-103">建立 ExpressRoute 連接，將 ExpressRoute 閘道連接至內部部署 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="b7de3-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="b7de3-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7de3-104">SYNTAX</span></span>

### <span data-ttu-id="b7de3-105">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="b7de3-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7de3-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b7de3-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7de3-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b7de3-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7de3-108">描述</span><span class="sxs-lookup"><span data-stu-id="b7de3-108">DESCRIPTION</span></span>
<span data-ttu-id="b7de3-109">在內部部署 ExpressRoute 回路 BGP 對等到虛擬中樞內的 ExpressRoute 閘道之間建立 ExpressRoute 連接。</span><span class="sxs-lookup"><span data-stu-id="b7de3-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="b7de3-110">例子</span><span class="sxs-lookup"><span data-stu-id="b7de3-110">EXAMPLES</span></span>

### <span data-ttu-id="b7de3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b7de3-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
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

<span data-ttu-id="b7de3-112">上述將建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞、Express Route 閘道，以及美國中西部 Azure 中「testRG」資源群組中具有私人對等的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="b7de3-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b7de3-113">閘道建立之後，會使用 New-AzExpressRouteConnection 命令連接到 ExpressRoute 回路對等。</span><span class="sxs-lookup"><span data-stu-id="b7de3-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="b7de3-114">參數</span><span class="sxs-lookup"><span data-stu-id="b7de3-114">PARAMETERS</span></span>

### <span data-ttu-id="b7de3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7de3-115">-AsJob</span></span>
<span data-ttu-id="b7de3-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7de3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7de3-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="b7de3-117">-AuthorizationKey</span></span>
<span data-ttu-id="b7de3-118">從 ExpressRoute 回路擁有者取得金鑰，以建立與不同訂閱中閘道的關聯。</span><span class="sxs-lookup"><span data-stu-id="b7de3-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="b7de3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7de3-119">-DefaultProfile</span></span>
<span data-ttu-id="b7de3-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7de3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7de3-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b7de3-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="b7de3-122">針對此 ExpressRoute 閘道連接啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="b7de3-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="b7de3-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="b7de3-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="b7de3-124">要建立此 Express Route 閘道連接之 Express 路由回路對等的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7de3-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="b7de3-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="b7de3-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="b7de3-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b7de3-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de3-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b7de3-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="b7de3-128">此連接的父 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="b7de3-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7de3-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7de3-129">-Name</span></span>
<span data-ttu-id="b7de3-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b7de3-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de3-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b7de3-131">-ParentResourceId</span></span>
<span data-ttu-id="b7de3-132">此連接的父 ExpressRouteGateway 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7de3-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7de3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7de3-133">-ResourceGroupName</span></span>
<span data-ttu-id="b7de3-134">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b7de3-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de3-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7de3-135">-RoutingConfiguration</span></span>
<span data-ttu-id="b7de3-136">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="b7de3-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="b7de3-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="b7de3-137">-RoutingWeight</span></span>
<span data-ttu-id="b7de3-138">需要指派給此連接之封包路由的粗細。</span><span class="sxs-lookup"><span data-stu-id="b7de3-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de3-139">-確認</span><span class="sxs-lookup"><span data-stu-id="b7de3-139">-Confirm</span></span>
<span data-ttu-id="b7de3-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7de3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7de3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7de3-141">-WhatIf</span></span>
<span data-ttu-id="b7de3-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7de3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7de3-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7de3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7de3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7de3-144">CommonParameters</span></span>
<span data-ttu-id="b7de3-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7de3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7de3-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7de3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7de3-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b7de3-147">INPUTS</span></span>

### <span data-ttu-id="b7de3-148">Microsoft.Azure.Commands.Network.models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b7de3-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="b7de3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b7de3-149">System.String</span></span>

## <span data-ttu-id="b7de3-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b7de3-150">OUTPUTS</span></span>

### <span data-ttu-id="b7de3-151">Microsoft.Azure.Commands.Network.models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="b7de3-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="b7de3-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b7de3-152">NOTES</span></span>

## <span data-ttu-id="b7de3-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7de3-153">RELATED LINKS</span></span>

[<span data-ttu-id="b7de3-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7de3-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
