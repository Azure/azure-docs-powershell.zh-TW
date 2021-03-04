---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4c206bfe4681bfdc1cb622ec90170776e5528ebe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908854"
---
# <span data-ttu-id="a2f3b-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2f3b-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a2f3b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f3b-103">新增子網組配置至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="a2f3b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2f3b-104">SYNTAX</span></span>

### <span data-ttu-id="a2f3b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a2f3b-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2f3b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f3b-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2f3b-107">描述</span><span class="sxs-lookup"><span data-stu-id="a2f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="a2f3b-108">**Add-AzVirtualNetworkSubnetConfig** Cmdlet 會新增子網組配置至現有的 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="a2f3b-109">例子</span><span class="sxs-lookup"><span data-stu-id="a2f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="a2f3b-110">範例 1：新增子網至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a2f3b-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="a2f3b-111">此範例會先建立資源群組，做為要建立之資源的容器。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="a2f3b-112">接著，它會建立子網組配置，然後使用它來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="a2f3b-113">然後Add-AzVirtualNetworkSubnetConfig，將子網新增到虛擬網路的記憶體中表示。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a2f3b-114">命令Set-AzVirtualNetwork以新的子網更新現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="a2f3b-115">範例 2：將委派新加入現有虛擬網路的子網</span><span class="sxs-lookup"><span data-stu-id="a2f3b-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="a2f3b-116">此範例會先獲得現有的 vnet。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="a2f3b-117">接著，它會在記憶體中建立委派物件。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="a2f3b-118">最後，它會使用該委派建立新子網，並新增到 vnet。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="a2f3b-119">修改後的組配置隨即會送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="a2f3b-120">參數</span><span class="sxs-lookup"><span data-stu-id="a2f3b-120">PARAMETERS</span></span>

### <span data-ttu-id="a2f3b-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a2f3b-121">-AddressPrefix</span></span>
<span data-ttu-id="a2f3b-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="a2f3b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f3b-123">-DefaultProfile</span></span>
<span data-ttu-id="a2f3b-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2f3b-125">-委派</span><span class="sxs-lookup"><span data-stu-id="a2f3b-125">-Delegation</span></span>
<span data-ttu-id="a2f3b-126">有權在此子網上執行作業的服務清單。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="a2f3b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2f3b-127">-InputObject</span></span>
<span data-ttu-id="a2f3b-128">指定與子網群組原則相關聯的 nat 閘道。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a2f3b-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="a2f3b-129">-IpAllocation</span></span>
<span data-ttu-id="a2f3b-130">指定子網的 IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="a2f3b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2f3b-131">-Name</span></span>
<span data-ttu-id="a2f3b-132">指定要新增之子網組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="a2f3b-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2f3b-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a2f3b-134">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="a2f3b-135">此 Cmdlet 會新增虛擬網路子網設定至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2f3b-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a2f3b-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a2f3b-137">指定網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a2f3b-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="a2f3b-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="a2f3b-139">設定為啟用或停用在子網中的私人端點上應用程式網路原則。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="a2f3b-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="a2f3b-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="a2f3b-141">設定為啟用或停用在子網中的私人連結服務上應用程式網路原則。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="a2f3b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f3b-142">-ResourceId</span></span>
<span data-ttu-id="a2f3b-143">指定與子網組配置相關聯的 NAT 閘道資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a2f3b-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a2f3b-144">-RouteTable</span></span>
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

### <span data-ttu-id="a2f3b-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="a2f3b-145">-RouteTableId</span></span>
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

### <span data-ttu-id="a2f3b-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2f3b-146">-ServiceEndpoint</span></span>
<span data-ttu-id="a2f3b-147">服務端點值</span><span class="sxs-lookup"><span data-stu-id="a2f3b-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="a2f3b-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a2f3b-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a2f3b-149">服務端點策略</span><span class="sxs-lookup"><span data-stu-id="a2f3b-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="a2f3b-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a2f3b-150">-VirtualNetwork</span></span>
<span data-ttu-id="a2f3b-151">指定要新增子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="a2f3b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f3b-152">CommonParameters</span></span>
<span data-ttu-id="a2f3b-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2f3b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f3b-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2f3b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f3b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a2f3b-155">INPUTS</span></span>

### <span data-ttu-id="a2f3b-156">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a2f3b-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="a2f3b-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a2f3b-157">System.String</span></span>

### <span data-ttu-id="a2f3b-158">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2f3b-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="a2f3b-159">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2f3b-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="a2f3b-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a2f3b-160">System.String[]</span></span>

### <span data-ttu-id="a2f3b-161">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="a2f3b-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="a2f3b-162">Microsoft.Azure.Commands.Network.Models.PSD表示[]</span><span class="sxs-lookup"><span data-stu-id="a2f3b-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="a2f3b-163">輸出</span><span class="sxs-lookup"><span data-stu-id="a2f3b-163">OUTPUTS</span></span>

### <span data-ttu-id="a2f3b-164">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a2f3b-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a2f3b-165">筆記</span><span class="sxs-lookup"><span data-stu-id="a2f3b-165">NOTES</span></span>

## <span data-ttu-id="a2f3b-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2f3b-166">RELATED LINKS</span></span>

[<span data-ttu-id="a2f3b-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2f3b-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a2f3b-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2f3b-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a2f3b-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2f3b-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a2f3b-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2f3b-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
