---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 47c56f2f55a07dc2567ca3ee2030e075d90dc324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901929"
---
# <span data-ttu-id="efa0a-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efa0a-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="efa0a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="efa0a-102">SYNOPSIS</span></span>
<span data-ttu-id="efa0a-103">更新虛擬網路的子網組配置。</span><span class="sxs-lookup"><span data-stu-id="efa0a-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="efa0a-104">語法</span><span class="sxs-lookup"><span data-stu-id="efa0a-104">SYNTAX</span></span>

### <span data-ttu-id="efa0a-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="efa0a-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efa0a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="efa0a-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efa0a-107">描述</span><span class="sxs-lookup"><span data-stu-id="efa0a-107">DESCRIPTION</span></span>
<span data-ttu-id="efa0a-108">**Set-AzVirtualNetworkSubnetConfig** Cmdlet 會更新虛擬網路的子網設定。</span><span class="sxs-lookup"><span data-stu-id="efa0a-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="efa0a-109">例子</span><span class="sxs-lookup"><span data-stu-id="efa0a-109">EXAMPLES</span></span>

### <span data-ttu-id="efa0a-110">1：修改子網的位址首碼</span><span class="sxs-lookup"><span data-stu-id="efa0a-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="efa0a-111">此範例會建立一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="efa0a-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="efa0a-112">接著是呼叫Set-AzVirtualNetworkSubnetConfig修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="efa0a-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="efa0a-113">這只會影響虛擬網路的記憶體中表示。</span><span class="sxs-lookup"><span data-stu-id="efa0a-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="efa0a-114">Set-AzVirtualNetwork，系統隨即會要求修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="efa0a-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="efa0a-115">2：新增網路安全性群組至子網</span><span class="sxs-lookup"><span data-stu-id="efa0a-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="efa0a-116">此範例會建立一個資源群組，其中一個虛擬網路只包含一個子網。</span><span class="sxs-lookup"><span data-stu-id="efa0a-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="efa0a-117">接著，它會建立一個網路安全性群組，並針對 RDP 流量建立允許規則。</span><span class="sxs-lookup"><span data-stu-id="efa0a-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="efa0a-118">Cmdlet Set-AzVirtualNetworkSubnetConfig修改前端子網的記憶體內表示方式，以指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="efa0a-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="efa0a-119">接著Set-AzVirtualNetwork Cmdlet，將修改後的狀態寫入服務。</span><span class="sxs-lookup"><span data-stu-id="efa0a-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="efa0a-120">3：將 Nat 閘道附加至子網</span><span class="sxs-lookup"><span data-stu-id="efa0a-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="efa0a-121">參數</span><span class="sxs-lookup"><span data-stu-id="efa0a-121">PARAMETERS</span></span>

### <span data-ttu-id="efa0a-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="efa0a-122">-AddressPrefix</span></span>
<span data-ttu-id="efa0a-123">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="efa0a-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa0a-124">-DefaultProfile</span></span>
<span data-ttu-id="efa0a-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="efa0a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa0a-126">-委派</span><span class="sxs-lookup"><span data-stu-id="efa0a-126">-Delegation</span></span>
<span data-ttu-id="efa0a-127">有權在此子網上執行作業的服務清單。</span><span class="sxs-lookup"><span data-stu-id="efa0a-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa0a-128">-InputObject</span></span>
<span data-ttu-id="efa0a-129">指定與子網群組原則相關聯的 nat 閘道。</span><span class="sxs-lookup"><span data-stu-id="efa0a-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="efa0a-130">-IpAllocation</span></span>
<span data-ttu-id="efa0a-131">指定子網的 IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="efa0a-131">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="efa0a-132">-Name</span></span>
<span data-ttu-id="efa0a-133">指定此 Cmdlet 所設定之子網設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="efa0a-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa0a-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="efa0a-135">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="efa0a-135">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="efa0a-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="efa0a-137">指定網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="efa0a-137">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="efa0a-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="efa0a-139">設定為啟用或停用在子網中的私人端點上應用程式網路原則。</span><span class="sxs-lookup"><span data-stu-id="efa0a-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="efa0a-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="efa0a-141">設定為啟用或停用在子網中的私人連結服務上應用程式網路原則。</span><span class="sxs-lookup"><span data-stu-id="efa0a-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efa0a-142">-ResourceId</span></span>
<span data-ttu-id="efa0a-143">指定與子網組配置相關聯的 NAT 閘道資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="efa0a-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="efa0a-144">-RouteTable</span></span>
<span data-ttu-id="efa0a-145">指定與網路安全性群組相關聯的路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="efa0a-145">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="efa0a-146">-RouteTableId</span></span>
<span data-ttu-id="efa0a-147">指定與網路安全性群組相關聯的路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="efa0a-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="efa0a-148">-ServiceEndpoint</span></span>
<span data-ttu-id="efa0a-149">服務端點值</span><span class="sxs-lookup"><span data-stu-id="efa0a-149">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="efa0a-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="efa0a-151">服務端點策略</span><span class="sxs-lookup"><span data-stu-id="efa0a-151">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="efa0a-152">-VirtualNetwork</span></span>
<span data-ttu-id="efa0a-153">指定 **包含子網配置的 VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="efa0a-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa0a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa0a-154">CommonParameters</span></span>
<span data-ttu-id="efa0a-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="efa0a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa0a-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa0a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa0a-157">輸入</span><span class="sxs-lookup"><span data-stu-id="efa0a-157">INPUTS</span></span>

### <span data-ttu-id="efa0a-158">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="efa0a-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="efa0a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="efa0a-159">System.String</span></span>

### <span data-ttu-id="efa0a-160">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa0a-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="efa0a-161">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="efa0a-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="efa0a-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="efa0a-162">System.String[]</span></span>

### <span data-ttu-id="efa0a-163">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="efa0a-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="efa0a-164">Microsoft.Azure.Commands.Network.Models.PSD表示[]</span><span class="sxs-lookup"><span data-stu-id="efa0a-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="efa0a-165">輸出</span><span class="sxs-lookup"><span data-stu-id="efa0a-165">OUTPUTS</span></span>

### <span data-ttu-id="efa0a-166">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="efa0a-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="efa0a-167">筆記</span><span class="sxs-lookup"><span data-stu-id="efa0a-167">NOTES</span></span>

## <span data-ttu-id="efa0a-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="efa0a-168">RELATED LINKS</span></span>

[<span data-ttu-id="efa0a-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efa0a-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="efa0a-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efa0a-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="efa0a-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efa0a-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="efa0a-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efa0a-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
