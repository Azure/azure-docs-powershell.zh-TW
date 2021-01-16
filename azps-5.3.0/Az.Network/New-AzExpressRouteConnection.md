---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288728"
---
# <span data-ttu-id="7d1b7-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7d1b7-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="7d1b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1b7-103">建立一個 ExpressRoute 連線，將 ExpressRoute 閘道連線到內部部署 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="7d1b7-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="7d1b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d1b7-104">SYNTAX</span></span>

### <span data-ttu-id="7d1b7-105">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="7d1b7-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1b7-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7d1b7-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1b7-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1b7-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1b7-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d1b7-108">DESCRIPTION</span></span>
<span data-ttu-id="7d1b7-109">在虛擬中樞內的 ExpressRoute 閘道內部部署 ExpressRoute 電路 BGP 對等之間建立 ExpressRoute 連線。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="7d1b7-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d1b7-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1b7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7d1b7-111">Example 1</span></span>

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

<span data-ttu-id="7d1b7-112">上述將會建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞、快速路由閘道，以及在 Microsoft 中的 [testRG] 資源群組中使用私人對等的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7d1b7-113">建立閘道之後，就會使用 [New-AzExpressRouteConnection] 命令將其連線至 ExpressRoute 電路對等。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="7d1b7-114">參數</span><span class="sxs-lookup"><span data-stu-id="7d1b7-114">PARAMETERS</span></span>

### <span data-ttu-id="7d1b7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d1b7-115">-AsJob</span></span>
<span data-ttu-id="7d1b7-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7d1b7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d1b7-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7d1b7-117">-AuthorizationKey</span></span>
<span data-ttu-id="7d1b7-118">從 ExpressRoute 回路擁有者取得的金鑰，可以建立與不同訂閱中的閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="7d1b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1b7-119">-DefaultProfile</span></span>
<span data-ttu-id="7d1b7-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d1b7-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7d1b7-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="7d1b7-122">針對 ExpressRoute 閘道連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="7d1b7-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="7d1b7-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="7d1b7-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="7d1b7-124">要建立此快速路由閘道連接之快速路由線路對等的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="7d1b7-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="7d1b7-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="7d1b7-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-126">The resource group name.</span></span>

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

### <span data-ttu-id="7d1b7-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7d1b7-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="7d1b7-128">此連接的父 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-128">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="7d1b7-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d1b7-129">-Name</span></span>
<span data-ttu-id="7d1b7-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-130">The resource name.</span></span>

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

### <span data-ttu-id="7d1b7-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1b7-131">-ParentResourceId</span></span>
<span data-ttu-id="7d1b7-132">此連線之父 ExpressRouteGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="7d1b7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1b7-133">-ResourceGroupName</span></span>
<span data-ttu-id="7d1b7-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-134">The resource group name.</span></span>

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

### <span data-ttu-id="7d1b7-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d1b7-135">-RoutingConfiguration</span></span>
<span data-ttu-id="7d1b7-136">此連線的路由設定</span><span class="sxs-lookup"><span data-stu-id="7d1b7-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="7d1b7-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7d1b7-137">-RoutingWeight</span></span>
<span data-ttu-id="7d1b7-138">需要指派給這個連線之資料包路由的權重。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="7d1b7-139">-確認</span><span class="sxs-lookup"><span data-stu-id="7d1b7-139">-Confirm</span></span>
<span data-ttu-id="7d1b7-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1b7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1b7-141">-WhatIf</span></span>
<span data-ttu-id="7d1b7-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1b7-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1b7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1b7-144">CommonParameters</span></span>
<span data-ttu-id="7d1b7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1b7-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d1b7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1b7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="7d1b7-147">INPUTS</span></span>

### <span data-ttu-id="7d1b7-148">PSExpressRouteGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d1b7-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="7d1b7-149">System.object</span><span class="sxs-lookup"><span data-stu-id="7d1b7-149">System.String</span></span>

## <span data-ttu-id="7d1b7-150">輸出</span><span class="sxs-lookup"><span data-stu-id="7d1b7-150">OUTPUTS</span></span>

### <span data-ttu-id="7d1b7-151">PSExpressRouteConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d1b7-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7d1b7-152">筆記</span><span class="sxs-lookup"><span data-stu-id="7d1b7-152">NOTES</span></span>

## <span data-ttu-id="7d1b7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d1b7-153">RELATED LINKS</span></span>

[<span data-ttu-id="7d1b7-154">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d1b7-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
