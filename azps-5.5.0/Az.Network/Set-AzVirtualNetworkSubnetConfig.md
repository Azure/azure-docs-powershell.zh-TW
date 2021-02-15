---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134807"
---
# <span data-ttu-id="38d9b-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38d9b-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="38d9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="38d9b-103">更新虛擬網路的子網配置。</span><span class="sxs-lookup"><span data-stu-id="38d9b-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="38d9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="38d9b-104">SYNTAX</span></span>

### <span data-ttu-id="38d9b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="38d9b-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38d9b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="38d9b-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38d9b-107">說明</span><span class="sxs-lookup"><span data-stu-id="38d9b-107">DESCRIPTION</span></span>
<span data-ttu-id="38d9b-108">AzVirtualNetworkSubnetConfig Cmdlet 會更新虛擬網路的子網 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="38d9b-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="38d9b-109">示例</span><span class="sxs-lookup"><span data-stu-id="38d9b-109">EXAMPLES</span></span>

### <span data-ttu-id="38d9b-110">1：修改子網的位址前置詞</span><span class="sxs-lookup"><span data-stu-id="38d9b-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="38d9b-111">這個範例會建立一個含有一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="38d9b-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="38d9b-112">然後，通話 Set-AzVirtualNetworkSubnetConfig 修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="38d9b-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="38d9b-113">這只會影響虛擬網路在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="38d9b-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="38d9b-114">接著，就會呼叫 Set-AzVirtualNetwork 來修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="38d9b-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="38d9b-115">2：將網路安全性群組新增至子網</span><span class="sxs-lookup"><span data-stu-id="38d9b-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="38d9b-116">這個範例會建立一個包含只有一個子網的虛擬網路的資源群組。</span><span class="sxs-lookup"><span data-stu-id="38d9b-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="38d9b-117">接著，它會建立包含 RDP 流量的 allow 規則的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="38d9b-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="38d9b-118">Set-AzVirtualNetworkSubnetConfig Cmdlet 可用來修改前端子網的記憶體內表示形式，使其指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="38d9b-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="38d9b-119">接著會呼叫 Set-AzVirtualNetwork Cmdlet，以將修改過的狀態寫回服務。</span><span class="sxs-lookup"><span data-stu-id="38d9b-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="38d9b-120">3：將 Nat 閘道附加到子網</span><span class="sxs-lookup"><span data-stu-id="38d9b-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="38d9b-121">參數</span><span class="sxs-lookup"><span data-stu-id="38d9b-121">PARAMETERS</span></span>

### <span data-ttu-id="38d9b-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="38d9b-122">-AddressPrefix</span></span>
<span data-ttu-id="38d9b-123">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="38d9b-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="38d9b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d9b-124">-DefaultProfile</span></span>
<span data-ttu-id="38d9b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38d9b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d9b-126">委派</span><span class="sxs-lookup"><span data-stu-id="38d9b-126">-Delegation</span></span>
<span data-ttu-id="38d9b-127">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="38d9b-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="38d9b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38d9b-128">-InputObject</span></span>
<span data-ttu-id="38d9b-129">指定與子網配置相關聯的 nat 閘道。</span><span class="sxs-lookup"><span data-stu-id="38d9b-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="38d9b-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="38d9b-130">-IpAllocation</span></span>
<span data-ttu-id="38d9b-131">指定子網的 IpAllocations。</span><span class="sxs-lookup"><span data-stu-id="38d9b-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="38d9b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="38d9b-132">-Name</span></span>
<span data-ttu-id="38d9b-133">指定此 Cmdlet 所設定之子網配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="38d9b-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="38d9b-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="38d9b-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="38d9b-135">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="38d9b-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="38d9b-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="38d9b-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="38d9b-137">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="38d9b-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="38d9b-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="38d9b-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="38d9b-139">設定以啟用或停用子網上專用端點的網路原則。</span><span class="sxs-lookup"><span data-stu-id="38d9b-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="38d9b-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="38d9b-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="38d9b-141">設定以啟用或停用子網上私人連結服務的網路原則。</span><span class="sxs-lookup"><span data-stu-id="38d9b-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="38d9b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38d9b-142">-ResourceId</span></span>
<span data-ttu-id="38d9b-143">指定與子網配置相關聯的 NAT 閘道資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d9b-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="38d9b-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="38d9b-144">-RouteTable</span></span>
<span data-ttu-id="38d9b-145">指定與網路安全群組相關聯的路由表物件。</span><span class="sxs-lookup"><span data-stu-id="38d9b-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="38d9b-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="38d9b-146">-RouteTableId</span></span>
<span data-ttu-id="38d9b-147">指定與網路安全群組相關聯之路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d9b-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="38d9b-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="38d9b-148">-ServiceEndpoint</span></span>
<span data-ttu-id="38d9b-149">服務端點值</span><span class="sxs-lookup"><span data-stu-id="38d9b-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="38d9b-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="38d9b-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="38d9b-151">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="38d9b-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="38d9b-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38d9b-152">-VirtualNetwork</span></span>
<span data-ttu-id="38d9b-153">指定包含子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="38d9b-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="38d9b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d9b-154">CommonParameters</span></span>
<span data-ttu-id="38d9b-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38d9b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d9b-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38d9b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d9b-157">輸入</span><span class="sxs-lookup"><span data-stu-id="38d9b-157">INPUTS</span></span>

### <span data-ttu-id="38d9b-158">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="38d9b-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="38d9b-159">System.object</span><span class="sxs-lookup"><span data-stu-id="38d9b-159">System.String</span></span>

### <span data-ttu-id="38d9b-160">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="38d9b-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="38d9b-161">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="38d9b-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="38d9b-162">System.object []</span><span class="sxs-lookup"><span data-stu-id="38d9b-162">System.String[]</span></span>

### <span data-ttu-id="38d9b-163">PSServiceEndpointPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="38d9b-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="38d9b-164">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="38d9b-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="38d9b-165">輸出</span><span class="sxs-lookup"><span data-stu-id="38d9b-165">OUTPUTS</span></span>

### <span data-ttu-id="38d9b-166">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="38d9b-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="38d9b-167">筆記</span><span class="sxs-lookup"><span data-stu-id="38d9b-167">NOTES</span></span>

## <span data-ttu-id="38d9b-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="38d9b-168">RELATED LINKS</span></span>

[<span data-ttu-id="38d9b-169">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38d9b-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="38d9b-170">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38d9b-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="38d9b-171">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38d9b-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="38d9b-172">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38d9b-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
