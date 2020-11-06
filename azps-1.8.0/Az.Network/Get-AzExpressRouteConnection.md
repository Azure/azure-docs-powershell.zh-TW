---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 01b8c32af3edc6c10070bdbd61c7f84fa055af23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622035"
---
# <span data-ttu-id="a97f7-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a97f7-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="a97f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a97f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a97f7-103">依名稱取得 ExpressRoute 連線，或列出所有連線至 ExpressRouteGateway 的 ExpressRoute 連接。</span><span class="sxs-lookup"><span data-stu-id="a97f7-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="a97f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="a97f7-104">SYNTAX</span></span>

### <span data-ttu-id="a97f7-105">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="a97f7-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a97f7-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a97f7-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a97f7-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a97f7-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a97f7-108">說明</span><span class="sxs-lookup"><span data-stu-id="a97f7-108">DESCRIPTION</span></span>
<span data-ttu-id="a97f7-109">依名稱取得 ExpressRoute 連線，或列出所有連線至 ExpressRouteGateway 的 ExpressRoute 連接。</span><span class="sxs-lookup"><span data-stu-id="a97f7-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="a97f7-110">示例</span><span class="sxs-lookup"><span data-stu-id="a97f7-110">EXAMPLES</span></span>

### <span data-ttu-id="a97f7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a97f7-111">Example 1</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="a97f7-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 ExpressRouteSite。</span><span class="sxs-lookup"><span data-stu-id="a97f7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a97f7-113">在具有2個比例單位的虛擬中樞中，將會建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="a97f7-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a97f7-114">建立閘道之後，就會使用 [New-AzExpressRouteConnection] 命令將它連線到內部部署的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="a97f7-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="a97f7-115">然後它會使用連接名稱取得連線。</span><span class="sxs-lookup"><span data-stu-id="a97f7-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="a97f7-116">範例2</span><span class="sxs-lookup"><span data-stu-id="a97f7-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="a97f7-117">這個命令會取得 ExpressRoute "testExpressRoutegw" 中以「test」開頭的所有連接</span><span class="sxs-lookup"><span data-stu-id="a97f7-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="a97f7-118">參數</span><span class="sxs-lookup"><span data-stu-id="a97f7-118">PARAMETERS</span></span>

### <span data-ttu-id="a97f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97f7-119">-DefaultProfile</span></span>
<span data-ttu-id="a97f7-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a97f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a97f7-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="a97f7-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="a97f7-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a97f7-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a97f7-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a97f7-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="a97f7-124">此連接的父 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="a97f7-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a97f7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a97f7-125">-Name</span></span>
<span data-ttu-id="a97f7-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a97f7-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a97f7-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a97f7-127">-ParentResourceId</span></span>
<span data-ttu-id="a97f7-128">此連線之父 ExpressRouteGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a97f7-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a97f7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97f7-129">-ResourceGroupName</span></span>
<span data-ttu-id="a97f7-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a97f7-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a97f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97f7-131">CommonParameters</span></span>
<span data-ttu-id="a97f7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a97f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97f7-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a97f7-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97f7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a97f7-134">INPUTS</span></span>

### <span data-ttu-id="a97f7-135">System.object</span><span class="sxs-lookup"><span data-stu-id="a97f7-135">System.String</span></span>

## <span data-ttu-id="a97f7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a97f7-136">OUTPUTS</span></span>

### <span data-ttu-id="a97f7-137">PSExpressRouteConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a97f7-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a97f7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a97f7-138">NOTES</span></span>

## <span data-ttu-id="a97f7-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a97f7-139">RELATED LINKS</span></span>
