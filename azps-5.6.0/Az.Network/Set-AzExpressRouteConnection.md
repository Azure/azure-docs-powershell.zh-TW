---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: ad31bd55c86a785ce45a7f2ca43a20f5a1a97c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904934"
---
# <span data-ttu-id="8e335-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e335-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="8e335-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e335-102">SYNOPSIS</span></span>
<span data-ttu-id="8e335-103">更新在快速路由閘道與內部部署 Express 路由回路對等互連之間建立快速路由連接。</span><span class="sxs-lookup"><span data-stu-id="8e335-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8e335-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e335-104">SYNTAX</span></span>

### <span data-ttu-id="8e335-105">ByExpressRouteConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="8e335-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e335-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="8e335-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e335-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8e335-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e335-108">描述</span><span class="sxs-lookup"><span data-stu-id="8e335-108">DESCRIPTION</span></span>
<span data-ttu-id="8e335-109">**Set-AzExpressRouteConnteConnection** Cmdlet 會更新在快速路由閘道與內部部署 Express 路由回路對等互連之間建立快速路由連接。</span><span class="sxs-lookup"><span data-stu-id="8e335-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8e335-110">例子</span><span class="sxs-lookup"><span data-stu-id="8e335-110">EXAMPLES</span></span>

### <span data-ttu-id="8e335-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8e335-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
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

<span data-ttu-id="8e335-112">上述步驟將在 Azure 的 「testRG」資源群組中，建立美國西部的資源群組、虛擬 WAN、虛擬網路、虛擬中樞和 ExpressRouteSite。</span><span class="sxs-lookup"><span data-stu-id="8e335-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8e335-113">在此之後，將會以 2 個縮放單位在虛擬中心中建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="8e335-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8e335-114">閘道建立之後，即會使用 New-AzExpressRouteConnection 命令連接到內部部署 ExpressRoute 回路對等。</span><span class="sxs-lookup"><span data-stu-id="8e335-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="8e335-115">接著，使用 Set-AzExpressRouteConnection 命令更新該連接，以擁有不同的 RoutingWeight。</span><span class="sxs-lookup"><span data-stu-id="8e335-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="8e335-116">參數</span><span class="sxs-lookup"><span data-stu-id="8e335-116">PARAMETERS</span></span>

### <span data-ttu-id="8e335-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e335-117">-AsJob</span></span>
<span data-ttu-id="8e335-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e335-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e335-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="8e335-119">-AuthorizationKey</span></span>
<span data-ttu-id="8e335-120">用來建立 ExpressRoute 閘道連接的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="8e335-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="8e335-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e335-121">-DefaultProfile</span></span>
<span data-ttu-id="8e335-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e335-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e335-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8e335-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="8e335-124">針對此 ExpressRoute 閘道連接啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="8e335-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="8e335-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="8e335-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="8e335-126">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8e335-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e335-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e335-127">-InputObject</span></span>
<span data-ttu-id="8e335-128">要更新的 ExpressRouteConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="8e335-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e335-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e335-129">-Name</span></span>
<span data-ttu-id="8e335-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8e335-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e335-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e335-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e335-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8e335-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e335-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e335-133">-ResourceId</span></span>
<span data-ttu-id="8e335-134">要刪除的 ExpressRouteConnection 物件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e335-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e335-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e335-135">-RoutingConfiguration</span></span>
<span data-ttu-id="8e335-136">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="8e335-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="8e335-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="8e335-137">-RoutingWeight</span></span>
<span data-ttu-id="8e335-138">封包路由需要指派給此連接的粗細。</span><span class="sxs-lookup"><span data-stu-id="8e335-138">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="8e335-139">-確認</span><span class="sxs-lookup"><span data-stu-id="8e335-139">-Confirm</span></span>
<span data-ttu-id="8e335-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8e335-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e335-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e335-141">-WhatIf</span></span>
<span data-ttu-id="8e335-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e335-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e335-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e335-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e335-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e335-144">CommonParameters</span></span>
<span data-ttu-id="8e335-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e335-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e335-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e335-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e335-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8e335-147">INPUTS</span></span>

### <span data-ttu-id="8e335-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8e335-148">System.String</span></span>

### <span data-ttu-id="8e335-149">Microsoft.Azure.Commands.Network.models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e335-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8e335-150">輸出</span><span class="sxs-lookup"><span data-stu-id="8e335-150">OUTPUTS</span></span>

### <span data-ttu-id="8e335-151">Microsoft.Azure.Commands.Network.models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e335-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8e335-152">筆記</span><span class="sxs-lookup"><span data-stu-id="8e335-152">NOTES</span></span>

## <span data-ttu-id="8e335-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e335-153">RELATED LINKS</span></span>

[<span data-ttu-id="8e335-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e335-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
