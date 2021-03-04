---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5a874bac2a546a07b2946ec8315065035cabba72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908489"
---
# <span data-ttu-id="f4b2a-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f4b2a-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="f4b2a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b2a-103">建立虛擬網路子網組配置。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="f4b2a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4b2a-104">SYNTAX</span></span>

### <span data-ttu-id="f4b2a-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f4b2a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4b2a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b2a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b2a-107">描述</span><span class="sxs-lookup"><span data-stu-id="f4b2a-107">DESCRIPTION</span></span>
<span data-ttu-id="f4b2a-108">**New-AzVirtualNetworkSubnetConfig** Cmdlet 會建立虛擬網路子網組配置。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="f4b2a-109">例子</span><span class="sxs-lookup"><span data-stu-id="f4b2a-109">EXAMPLES</span></span>

### <span data-ttu-id="f4b2a-110">範例 1：建立包含兩個子網和一個網路安全群組的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="f4b2a-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="f4b2a-111">此範例會使用 New-AzVirtualSubnetConfig Cmdlet 建立兩個新的子網組New-AzVirtualSubnetConfig，然後使用這些組組來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="f4b2a-112">此New-AzVirtualSubnetConfig範本只會建立子網的記憶體中表示。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="f4b2a-113">在此範例中，frontendSubnet 具有 CIDR 10.0.1.0/24，並參照允許 RDP 存取的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="f4b2a-114">後端Subnet 具有 CIDR 10.0.2.0/24，且參照相同的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="f4b2a-115">參數</span><span class="sxs-lookup"><span data-stu-id="f4b2a-115">PARAMETERS</span></span>

### <span data-ttu-id="f4b2a-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f4b2a-116">-AddressPrefix</span></span>
<span data-ttu-id="f4b2a-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="f4b2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b2a-118">-DefaultProfile</span></span>
<span data-ttu-id="f4b2a-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b2a-120">-委派</span><span class="sxs-lookup"><span data-stu-id="f4b2a-120">-Delegation</span></span>
<span data-ttu-id="f4b2a-121">有權在此子網上執行作業的服務清單。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="f4b2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4b2a-122">-InputObject</span></span>
<span data-ttu-id="f4b2a-123">指定與子網群組原則相關聯的 nat 閘道</span><span class="sxs-lookup"><span data-stu-id="f4b2a-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="f4b2a-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="f4b2a-124">-IpAllocation</span></span>
<span data-ttu-id="f4b2a-125">指定子網的 IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="f4b2a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4b2a-126">-Name</span></span>
<span data-ttu-id="f4b2a-127">指定要建立之子網組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="f4b2a-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4b2a-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f4b2a-129">指定 NetworkSecurityGroup 物件。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="f4b2a-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f4b2a-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f4b2a-131">指定網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="f4b2a-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="f4b2a-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="f4b2a-133">設定為啟用或停用在子網中的私人端點上應用程式網路原則。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="f4b2a-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="f4b2a-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="f4b2a-135">設定為啟用或停用在子網中的私人連結服務上應用程式網路原則。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="f4b2a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b2a-136">-ResourceId</span></span>
<span data-ttu-id="f4b2a-137">指定與子網組配置相關聯的 NAT 閘道資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="f4b2a-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f4b2a-138">-RouteTable</span></span>
<span data-ttu-id="f4b2a-139">指定與子網群組原則相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="f4b2a-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="f4b2a-140">-RouteTableId</span></span>
<span data-ttu-id="f4b2a-141">指定與子網群組原則相關聯的路由資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="f4b2a-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-142">-ServiceEndpoint</span></span>
<span data-ttu-id="f4b2a-143">服務端點值</span><span class="sxs-lookup"><span data-stu-id="f4b2a-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="f4b2a-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4b2a-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f4b2a-145">服務端點策略</span><span class="sxs-lookup"><span data-stu-id="f4b2a-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="f4b2a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b2a-146">CommonParameters</span></span>
<span data-ttu-id="f4b2a-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4b2a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b2a-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4b2a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b2a-149">輸入</span><span class="sxs-lookup"><span data-stu-id="f4b2a-149">INPUTS</span></span>

### <span data-ttu-id="f4b2a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f4b2a-150">System.String</span></span>

### <span data-ttu-id="f4b2a-151">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4b2a-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="f4b2a-152">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4b2a-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="f4b2a-153">Microsoft.Azure.Commands.Network.models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4b2a-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="f4b2a-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f4b2a-154">System.String[]</span></span>

### <span data-ttu-id="f4b2a-155">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="f4b2a-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="f4b2a-156">Microsoft.Azure.Commands.Network.Models.PSD表示[]</span><span class="sxs-lookup"><span data-stu-id="f4b2a-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="f4b2a-157">輸出</span><span class="sxs-lookup"><span data-stu-id="f4b2a-157">OUTPUTS</span></span>

### <span data-ttu-id="f4b2a-158">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f4b2a-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="f4b2a-159">筆記</span><span class="sxs-lookup"><span data-stu-id="f4b2a-159">NOTES</span></span>

## <span data-ttu-id="f4b2a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4b2a-160">RELATED LINKS</span></span>

[<span data-ttu-id="f4b2a-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f4b2a-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f4b2a-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f4b2a-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f4b2a-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f4b2a-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f4b2a-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f4b2a-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
