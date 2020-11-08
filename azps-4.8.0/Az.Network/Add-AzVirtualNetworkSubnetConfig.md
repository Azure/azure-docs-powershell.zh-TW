---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128987"
---
# <span data-ttu-id="e80e9-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e80e9-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e80e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e80e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e80e9-103">新增子網配置至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e80e9-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="e80e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e80e9-104">SYNTAX</span></span>

### <span data-ttu-id="e80e9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e80e9-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e80e9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e80e9-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e80e9-107">說明</span><span class="sxs-lookup"><span data-stu-id="e80e9-107">DESCRIPTION</span></span>
<span data-ttu-id="e80e9-108">**AzVirtualNetworkSubnetConfig** Cmdlet 會將子網配置新增至現有的 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e80e9-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="e80e9-109">示例</span><span class="sxs-lookup"><span data-stu-id="e80e9-109">EXAMPLES</span></span>

### <span data-ttu-id="e80e9-110">範例1：將子網新增至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="e80e9-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="e80e9-111">這個範例會先建立資源群組做為要建立的資源容器。</span><span class="sxs-lookup"><span data-stu-id="e80e9-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="e80e9-112">接著，它會建立子網設定，並使用它來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e80e9-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="e80e9-113">然後，使用 Add-AzVirtualNetworkSubnetConfig 將子網新增至虛擬網路的記憶體內表示形式。</span><span class="sxs-lookup"><span data-stu-id="e80e9-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e80e9-114">[Set-AzVirtualNetwork] 命令會以新的子網來更新現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e80e9-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="e80e9-115">範例2：在要新增到現有虛擬網路的子網中新增委派</span><span class="sxs-lookup"><span data-stu-id="e80e9-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="e80e9-116">這個範例會先取得現有的 vnet。</span><span class="sxs-lookup"><span data-stu-id="e80e9-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="e80e9-117">接著，它會在記憶體中建立委派物件。</span><span class="sxs-lookup"><span data-stu-id="e80e9-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="e80e9-118">最後，它會建立一個新的子網，並將該委派新增至 vnet。</span><span class="sxs-lookup"><span data-stu-id="e80e9-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="e80e9-119">修改後的設定就會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="e80e9-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="e80e9-120">參數</span><span class="sxs-lookup"><span data-stu-id="e80e9-120">PARAMETERS</span></span>

### <span data-ttu-id="e80e9-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e80e9-121">-AddressPrefix</span></span>
<span data-ttu-id="e80e9-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="e80e9-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="e80e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80e9-123">-DefaultProfile</span></span>
<span data-ttu-id="e80e9-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e80e9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e80e9-125">委派</span><span class="sxs-lookup"><span data-stu-id="e80e9-125">-Delegation</span></span>
<span data-ttu-id="e80e9-126">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="e80e9-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="e80e9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e80e9-127">-InputObject</span></span>
<span data-ttu-id="e80e9-128">指定與子網配置相關聯的 nat 閘道。</span><span class="sxs-lookup"><span data-stu-id="e80e9-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e80e9-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="e80e9-129">-IpAllocation</span></span>
<span data-ttu-id="e80e9-130">指定子網的 IpAllocations。</span><span class="sxs-lookup"><span data-stu-id="e80e9-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="e80e9-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="e80e9-131">-Name</span></span>
<span data-ttu-id="e80e9-132">指定要新增的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="e80e9-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="e80e9-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e80e9-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e80e9-134">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="e80e9-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="e80e9-135">這個 Cmdlet 會將虛擬網路子網配置新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="e80e9-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e80e9-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e80e9-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e80e9-137">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="e80e9-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e80e9-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e80e9-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="e80e9-139">設定以啟用或停用子網上專用端點的網路原則。</span><span class="sxs-lookup"><span data-stu-id="e80e9-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="e80e9-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e80e9-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="e80e9-141">設定以啟用或停用子網上私人連結服務的網路原則。</span><span class="sxs-lookup"><span data-stu-id="e80e9-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="e80e9-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e80e9-142">-ResourceId</span></span>
<span data-ttu-id="e80e9-143">指定與子網配置相關聯的 NAT 閘道資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e80e9-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e80e9-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e80e9-144">-RouteTable</span></span>
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

### <span data-ttu-id="e80e9-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e80e9-145">-RouteTableId</span></span>
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

### <span data-ttu-id="e80e9-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e80e9-146">-ServiceEndpoint</span></span>
<span data-ttu-id="e80e9-147">服務端點值</span><span class="sxs-lookup"><span data-stu-id="e80e9-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e80e9-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e80e9-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e80e9-149">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="e80e9-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="e80e9-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e80e9-150">-VirtualNetwork</span></span>
<span data-ttu-id="e80e9-151">指定要在其中新增子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="e80e9-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="e80e9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80e9-152">CommonParameters</span></span>
<span data-ttu-id="e80e9-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e80e9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80e9-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e80e9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80e9-155">輸入</span><span class="sxs-lookup"><span data-stu-id="e80e9-155">INPUTS</span></span>

### <span data-ttu-id="e80e9-156">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e80e9-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="e80e9-157">System.object</span><span class="sxs-lookup"><span data-stu-id="e80e9-157">System.String</span></span>

### <span data-ttu-id="e80e9-158">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e80e9-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e80e9-159">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e80e9-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e80e9-160">System.object []</span><span class="sxs-lookup"><span data-stu-id="e80e9-160">System.String[]</span></span>

### <span data-ttu-id="e80e9-161">PSServiceEndpointPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="e80e9-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="e80e9-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="e80e9-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="e80e9-163">輸出</span><span class="sxs-lookup"><span data-stu-id="e80e9-163">OUTPUTS</span></span>

### <span data-ttu-id="e80e9-164">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e80e9-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e80e9-165">筆記</span><span class="sxs-lookup"><span data-stu-id="e80e9-165">NOTES</span></span>

## <span data-ttu-id="e80e9-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="e80e9-166">RELATED LINKS</span></span>

[<span data-ttu-id="e80e9-167">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e80e9-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e80e9-168">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e80e9-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e80e9-169">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e80e9-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e80e9-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e80e9-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
