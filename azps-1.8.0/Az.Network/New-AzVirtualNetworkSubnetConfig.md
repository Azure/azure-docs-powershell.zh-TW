---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 836973c4b1d95445d905bb41f489c48136e12f6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621703"
---
# <span data-ttu-id="b8de0-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b8de0-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b8de0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8de0-102">SYNOPSIS</span></span>
<span data-ttu-id="b8de0-103">建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="b8de0-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="b8de0-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8de0-104">SYNTAX</span></span>

### <span data-ttu-id="b8de0-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b8de0-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8de0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8de0-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8de0-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8de0-107">DESCRIPTION</span></span>
<span data-ttu-id="b8de0-108">**新的-AzVirtualNetworkSubnetConfig** Cmdlet 會建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="b8de0-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="b8de0-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8de0-109">EXAMPLES</span></span>

### <span data-ttu-id="b8de0-110">1：使用兩個子網和網路安全群組建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="b8de0-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="b8de0-111">這個範例會使用 New-AzVirtualSubnetConfig Cmdlet 建立兩個新的子網設定，然後使用它們來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b8de0-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="b8de0-112">New-AzVirtualSubnetConfig 範本只會建立子網的記憶體內部表示。</span><span class="sxs-lookup"><span data-stu-id="b8de0-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="b8de0-113">在這個範例中，frontendSubnet 有 CIDR 10.0.1.0/24，並參照允許 RDP 存取的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="b8de0-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="b8de0-114">BackendSubnet 有 CIDR 10.0.2.0/24，且參照相同的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="b8de0-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="b8de0-115">參數</span><span class="sxs-lookup"><span data-stu-id="b8de0-115">PARAMETERS</span></span>

### <span data-ttu-id="b8de0-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b8de0-116">-AddressPrefix</span></span>
<span data-ttu-id="b8de0-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="b8de0-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="b8de0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8de0-118">-DefaultProfile</span></span>
<span data-ttu-id="b8de0-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8de0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8de0-120">委派</span><span class="sxs-lookup"><span data-stu-id="b8de0-120">-Delegation</span></span>
<span data-ttu-id="b8de0-121">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="b8de0-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="b8de0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8de0-122">-Name</span></span>
<span data-ttu-id="b8de0-123">指定要建立的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b8de0-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="b8de0-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8de0-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b8de0-125">指定 NetworkSecurityGroup 物件。</span><span class="sxs-lookup"><span data-stu-id="b8de0-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="b8de0-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b8de0-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b8de0-127">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="b8de0-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b8de0-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b8de0-128">-RouteTable</span></span>
<span data-ttu-id="b8de0-129">指定與子網配置相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="b8de0-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b8de0-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="b8de0-130">-RouteTableId</span></span>
<span data-ttu-id="b8de0-131">指定與子網配置相關聯之路由資料表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8de0-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b8de0-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8de0-132">-ServiceEndpoint</span></span>
<span data-ttu-id="b8de0-133">服務端點值</span><span class="sxs-lookup"><span data-stu-id="b8de0-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="b8de0-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b8de0-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b8de0-135">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="b8de0-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="b8de0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8de0-136">CommonParameters</span></span>
<span data-ttu-id="b8de0-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8de0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8de0-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8de0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8de0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b8de0-139">INPUTS</span></span>

### <span data-ttu-id="b8de0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b8de0-140">System.String</span></span>

### <span data-ttu-id="b8de0-141">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8de0-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="b8de0-142">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8de0-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="b8de0-143">System.object []</span><span class="sxs-lookup"><span data-stu-id="b8de0-143">System.String[]</span></span>

### <span data-ttu-id="b8de0-144">PSServiceEndpointPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b8de0-144">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="b8de0-145">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="b8de0-145">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="b8de0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b8de0-146">OUTPUTS</span></span>

### <span data-ttu-id="b8de0-147">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8de0-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b8de0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b8de0-148">NOTES</span></span>

## <span data-ttu-id="b8de0-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8de0-149">RELATED LINKS</span></span>

[<span data-ttu-id="b8de0-150">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b8de0-150">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b8de0-151">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b8de0-151">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b8de0-152">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b8de0-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b8de0-153">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b8de0-153">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
