---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: ecaf236c04c24241cf285e3d8ca379d3bc52645a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791542"
---
# <span data-ttu-id="734b9-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="734b9-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="734b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="734b9-102">SYNOPSIS</span></span>
<span data-ttu-id="734b9-103">更新虛擬網路的子網配置。</span><span class="sxs-lookup"><span data-stu-id="734b9-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="734b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="734b9-104">SYNTAX</span></span>

### <span data-ttu-id="734b9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="734b9-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="734b9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="734b9-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="734b9-107">說明</span><span class="sxs-lookup"><span data-stu-id="734b9-107">DESCRIPTION</span></span>
<span data-ttu-id="734b9-108">AzVirtualNetworkSubnetConfig Cmdlet 會更新虛擬網路的子網 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="734b9-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="734b9-109">示例</span><span class="sxs-lookup"><span data-stu-id="734b9-109">EXAMPLES</span></span>

### <span data-ttu-id="734b9-110">1：修改子網的位址前置詞</span><span class="sxs-lookup"><span data-stu-id="734b9-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="734b9-111">這個範例會建立一個含有一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="734b9-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="734b9-112">然後，通話 Set-AzVirtualNetworkSubnetConfig 修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="734b9-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="734b9-113">這只會影響虛擬網路在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="734b9-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="734b9-114">接著，就會呼叫 Set-AzVirtualNetwork 來修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="734b9-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="734b9-115">2：將網路安全性群組新增至子網</span><span class="sxs-lookup"><span data-stu-id="734b9-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="734b9-116">這個範例會建立一個包含只有一個子網的虛擬網路的資源群組。</span><span class="sxs-lookup"><span data-stu-id="734b9-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="734b9-117">接著，它會建立包含 RDP 流量的 allow 規則的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="734b9-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="734b9-118">Set-AzVirtualNetworkSubnetConfig Cmdlet 可用來修改前端子網的記憶體內表示形式，使其指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="734b9-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="734b9-119">接著會呼叫 Set-AzVirtualNetwork Cmdlet，以將修改過的狀態寫回服務。</span><span class="sxs-lookup"><span data-stu-id="734b9-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="734b9-120">3：將 Nat 閘道附加到子網</span><span class="sxs-lookup"><span data-stu-id="734b9-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="734b9-121">參數</span><span class="sxs-lookup"><span data-stu-id="734b9-121">PARAMETERS</span></span>

### <span data-ttu-id="734b9-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="734b9-122">-AddressPrefix</span></span>
<span data-ttu-id="734b9-123">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="734b9-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="734b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734b9-124">-DefaultProfile</span></span>
<span data-ttu-id="734b9-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="734b9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="734b9-126">委派</span><span class="sxs-lookup"><span data-stu-id="734b9-126">-Delegation</span></span>
<span data-ttu-id="734b9-127">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="734b9-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="734b9-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="734b9-128">-InputObject</span></span>
<span data-ttu-id="734b9-129">指定與子網配置相關聯的 nat 閘道。</span><span class="sxs-lookup"><span data-stu-id="734b9-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="734b9-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="734b9-130">-Name</span></span>
<span data-ttu-id="734b9-131">指定此 Cmdlet 所設定之子網配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="734b9-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="734b9-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="734b9-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="734b9-133">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="734b9-133">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="734b9-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="734b9-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="734b9-135">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="734b9-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="734b9-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="734b9-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="734b9-137">設定以啟用或停用子網上專用端點的網路原則。</span><span class="sxs-lookup"><span data-stu-id="734b9-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="734b9-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="734b9-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="734b9-139">設定以啟用或停用子網上私人連結服務的網路原則。</span><span class="sxs-lookup"><span data-stu-id="734b9-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="734b9-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="734b9-140">-ResourceId</span></span>
<span data-ttu-id="734b9-141">指定與子網配置相關聯的 NAT 閘道資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="734b9-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="734b9-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="734b9-142">-RouteTable</span></span>
<span data-ttu-id="734b9-143">指定與網路安全群組相關聯的路由表物件。</span><span class="sxs-lookup"><span data-stu-id="734b9-143">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="734b9-144">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="734b9-144">-RouteTableId</span></span>
<span data-ttu-id="734b9-145">指定與網路安全群組相關聯之路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="734b9-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="734b9-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="734b9-146">-ServiceEndpoint</span></span>
<span data-ttu-id="734b9-147">服務端點值</span><span class="sxs-lookup"><span data-stu-id="734b9-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="734b9-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="734b9-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="734b9-149">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="734b9-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="734b9-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="734b9-150">-VirtualNetwork</span></span>
<span data-ttu-id="734b9-151">指定包含子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="734b9-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="734b9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734b9-152">CommonParameters</span></span>
<span data-ttu-id="734b9-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="734b9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734b9-154">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="734b9-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734b9-155">輸入</span><span class="sxs-lookup"><span data-stu-id="734b9-155">INPUTS</span></span>

### <span data-ttu-id="734b9-156">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="734b9-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="734b9-157">System.object</span><span class="sxs-lookup"><span data-stu-id="734b9-157">System.String</span></span>

### <span data-ttu-id="734b9-158">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="734b9-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="734b9-159">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="734b9-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="734b9-160">System.object []</span><span class="sxs-lookup"><span data-stu-id="734b9-160">System.String[]</span></span>

### <span data-ttu-id="734b9-161">PSServiceEndpointPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="734b9-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="734b9-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="734b9-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="734b9-163">輸出</span><span class="sxs-lookup"><span data-stu-id="734b9-163">OUTPUTS</span></span>

### <span data-ttu-id="734b9-164">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="734b9-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="734b9-165">筆記</span><span class="sxs-lookup"><span data-stu-id="734b9-165">NOTES</span></span>

## <span data-ttu-id="734b9-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="734b9-166">RELATED LINKS</span></span>

[<span data-ttu-id="734b9-167">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="734b9-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="734b9-168">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="734b9-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="734b9-169">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="734b9-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="734b9-170">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="734b9-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
