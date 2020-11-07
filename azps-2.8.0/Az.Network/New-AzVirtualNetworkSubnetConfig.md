---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16aae4a0eb0f070a63cd8ce87c39d968dd982872
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790754"
---
# <span data-ttu-id="3eb35-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3eb35-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="3eb35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3eb35-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb35-103">建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="3eb35-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="3eb35-104">句法</span><span class="sxs-lookup"><span data-stu-id="3eb35-104">SYNTAX</span></span>

### <span data-ttu-id="3eb35-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="3eb35-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3eb35-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3eb35-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb35-107">說明</span><span class="sxs-lookup"><span data-stu-id="3eb35-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb35-108">**新的-AzVirtualNetworkSubnetConfig** Cmdlet 會建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="3eb35-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="3eb35-109">示例</span><span class="sxs-lookup"><span data-stu-id="3eb35-109">EXAMPLES</span></span>

### <span data-ttu-id="3eb35-110">1：使用兩個子網和網路安全群組建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="3eb35-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
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

<span data-ttu-id="3eb35-111">這個範例會使用 New-AzVirtualSubnetConfig Cmdlet 建立兩個新的子網設定，然後使用它們來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="3eb35-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="3eb35-112">New-AzVirtualSubnetConfig 範本只會建立子網的記憶體內部表示。</span><span class="sxs-lookup"><span data-stu-id="3eb35-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="3eb35-113">在這個範例中，frontendSubnet 有 CIDR 10.0.1.0/24，並參照允許 RDP 存取的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3eb35-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="3eb35-114">BackendSubnet 有 CIDR 10.0.2.0/24，且參照相同的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3eb35-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="3eb35-115">參數</span><span class="sxs-lookup"><span data-stu-id="3eb35-115">PARAMETERS</span></span>

### <span data-ttu-id="3eb35-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3eb35-116">-AddressPrefix</span></span>
<span data-ttu-id="3eb35-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="3eb35-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="3eb35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb35-118">-DefaultProfile</span></span>
<span data-ttu-id="3eb35-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3eb35-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eb35-120">委派</span><span class="sxs-lookup"><span data-stu-id="3eb35-120">-Delegation</span></span>
<span data-ttu-id="3eb35-121">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="3eb35-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="3eb35-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb35-122">-InputObject</span></span>
<span data-ttu-id="3eb35-123">指定與子網配置相關聯的 nat 閘道</span><span class="sxs-lookup"><span data-stu-id="3eb35-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="3eb35-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3eb35-124">-Name</span></span>
<span data-ttu-id="3eb35-125">指定要建立的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3eb35-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="3eb35-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eb35-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3eb35-127">指定 NetworkSecurityGroup 物件。</span><span class="sxs-lookup"><span data-stu-id="3eb35-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="3eb35-128">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3eb35-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="3eb35-129">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="3eb35-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="3eb35-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="3eb35-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="3eb35-131">設定以啟用或停用子網上專用端點的網路原則。</span><span class="sxs-lookup"><span data-stu-id="3eb35-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="3eb35-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="3eb35-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="3eb35-133">設定以啟用或停用子網上私人連結服務的網路原則。</span><span class="sxs-lookup"><span data-stu-id="3eb35-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="3eb35-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eb35-134">-ResourceId</span></span>
<span data-ttu-id="3eb35-135">指定與子網配置相關聯的 NAT 閘道資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3eb35-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="3eb35-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="3eb35-136">-RouteTable</span></span>
<span data-ttu-id="3eb35-137">指定與子網配置相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="3eb35-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="3eb35-138">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="3eb35-138">-RouteTableId</span></span>
<span data-ttu-id="3eb35-139">指定與子網配置相關聯之路由資料表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3eb35-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="3eb35-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3eb35-140">-ServiceEndpoint</span></span>
<span data-ttu-id="3eb35-141">服務端點值</span><span class="sxs-lookup"><span data-stu-id="3eb35-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="3eb35-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3eb35-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="3eb35-143">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="3eb35-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="3eb35-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb35-144">CommonParameters</span></span>
<span data-ttu-id="3eb35-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3eb35-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb35-146">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3eb35-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb35-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3eb35-147">INPUTS</span></span>

### <span data-ttu-id="3eb35-148">System.object</span><span class="sxs-lookup"><span data-stu-id="3eb35-148">System.String</span></span>

### <span data-ttu-id="3eb35-149">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3eb35-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="3eb35-150">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3eb35-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="3eb35-151">PSNatGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3eb35-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="3eb35-152">System.object []</span><span class="sxs-lookup"><span data-stu-id="3eb35-152">System.String[]</span></span>

### <span data-ttu-id="3eb35-153">PSServiceEndpointPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="3eb35-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="3eb35-154">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="3eb35-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="3eb35-155">輸出</span><span class="sxs-lookup"><span data-stu-id="3eb35-155">OUTPUTS</span></span>

### <span data-ttu-id="3eb35-156">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3eb35-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="3eb35-157">筆記</span><span class="sxs-lookup"><span data-stu-id="3eb35-157">NOTES</span></span>

## <span data-ttu-id="3eb35-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eb35-158">RELATED LINKS</span></span>

[<span data-ttu-id="3eb35-159">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3eb35-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3eb35-160">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3eb35-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3eb35-161">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3eb35-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3eb35-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3eb35-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
