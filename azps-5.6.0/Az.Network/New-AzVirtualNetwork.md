---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 9608dfd5a780006d2ab050a1ca2e85ee26949f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904354"
---
# <span data-ttu-id="cc8e8-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc8e8-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="cc8e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8e8-103">建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-103">Creates a virtual network.</span></span>

## <span data-ttu-id="cc8e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc8e8-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc8e8-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc8e8-105">DESCRIPTION</span></span>
<span data-ttu-id="cc8e8-106">**New-AzVirtualNetwork** Cmdlet 會建立 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="cc8e8-107">例子</span><span class="sxs-lookup"><span data-stu-id="cc8e8-107">EXAMPLES</span></span>

### <span data-ttu-id="cc8e8-108">範例 1：建立有兩個子網的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="cc8e8-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="cc8e8-109">此範例會建立一個包含兩個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="cc8e8-110">首先，在中央地區建立新資源群組。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="cc8e8-111">然後，範例會建立兩個子網的記憶體中標記法。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="cc8e8-112">New-AzVirtualNetworkSubnetConfig Cmdlet 不會在伺服器端建立任何子網。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="cc8e8-113">有一個稱為 frontendSubnet 的子網，以及一個稱為後端Subnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="cc8e8-114">然後New-AzVirtualNetwork Cmdlet 使用 CIDR 10.0.0.0/16 做為位址首碼和兩個子網來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="cc8e8-115">範例 2：使用 DNS 設定建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="cc8e8-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="cc8e8-116">此範例會建立一個包含兩個子網和兩個 DNS 伺服器的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="cc8e8-117">在虛擬網路上指定 DNS 伺服器的效果是，部署至此虛擬網路的 NIC/VMS 會繼承這些 DNS 伺服器做為預設值。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="cc8e8-118">這些預設值可透過 NIC 層級設定來覆蓋每個 NIC。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="cc8e8-119">如果在 VNET 上未指定 DNS 伺服器，且 NIC 上沒有 DNS 伺服器，則預設的 Azure DNS 伺服器會用於 DNS 解析。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="cc8e8-120">範例 3：建立以子網參照網路安全性群組之虛擬網路</span><span class="sxs-lookup"><span data-stu-id="cc8e8-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="cc8e8-121">此範例會建立一個參照網路安全性群組之子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="cc8e8-122">首先，範例會建立資源群組做為要建立之資源的容器。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="cc8e8-123">接著，會建立一個允許內入 RDP 存取的網路安全性群組，但以其他方式強制執行預設的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="cc8e8-124">然後New-AzVirtualNetworkSubnetConfig Cmdlet 建立兩個子網的記憶體中標記法，兩個子網都參照所建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="cc8e8-125">接著New-AzVirtualNetwork命令建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="cc8e8-126">參數</span><span class="sxs-lookup"><span data-stu-id="cc8e8-126">PARAMETERS</span></span>

### <span data-ttu-id="cc8e8-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cc8e8-127">-AddressPrefix</span></span>
<span data-ttu-id="cc8e8-128">指定虛擬網路的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc8e8-129">-AsJob</span></span>
<span data-ttu-id="cc8e8-130">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cc8e8-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="cc8e8-131">-BgpCommunity</span></span>
<span data-ttu-id="cc8e8-132">在 ExpressRoute 上宣告的 BGP 社群。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="cc8e8-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="cc8e8-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="cc8e8-134">參照與虛擬網路相關聯的 DDoS 保護計劃資源。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="cc8e8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8e8-135">-DefaultProfile</span></span>
<span data-ttu-id="cc8e8-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc8e8-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="cc8e8-137">-DnsServer</span></span>
<span data-ttu-id="cc8e8-138">指定子網的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="cc8e8-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="cc8e8-139">-EnableDdosProtection</span></span>
<span data-ttu-id="cc8e8-140">參數代表是否已啟用 DDoS 保護。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-141">-強制</span><span class="sxs-lookup"><span data-stu-id="cc8e8-141">-Force</span></span>
<span data-ttu-id="cc8e8-142">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-142">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="cc8e8-143">-IpAllocation</span></span>
<span data-ttu-id="cc8e8-144">指定虛擬網路的 IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-144">Specifies IpAllocations for a virtual network.</span></span>

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

### <span data-ttu-id="cc8e8-145">-位置</span><span class="sxs-lookup"><span data-stu-id="cc8e8-145">-Location</span></span>
<span data-ttu-id="cc8e8-146">指定虛擬網路的區域。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-146">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc8e8-147">-Name</span></span>
<span data-ttu-id="cc8e8-148">指定此 Cmdlet 所建立之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc8e8-149">-ResourceGroupName</span></span>
<span data-ttu-id="cc8e8-150">指定要包含虛擬網路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-150">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-151">-子網</span><span class="sxs-lookup"><span data-stu-id="cc8e8-151">-Subnet</span></span>
<span data-ttu-id="cc8e8-152">指定要與虛擬網路建立關聯的子網清單。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-153">-標記</span><span class="sxs-lookup"><span data-stu-id="cc8e8-153">-Tag</span></span>
<span data-ttu-id="cc8e8-154">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc8e8-155">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="cc8e8-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-156">-確認</span><span class="sxs-lookup"><span data-stu-id="cc8e8-156">-Confirm</span></span>
<span data-ttu-id="cc8e8-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc8e8-158">-WhatIf</span></span>
<span data-ttu-id="cc8e8-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc8e8-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8e8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8e8-161">CommonParameters</span></span>
<span data-ttu-id="cc8e8-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc8e8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8e8-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc8e8-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8e8-164">輸入</span><span class="sxs-lookup"><span data-stu-id="cc8e8-164">INPUTS</span></span>

### <span data-ttu-id="cc8e8-165">System.String</span><span class="sxs-lookup"><span data-stu-id="cc8e8-165">System.String</span></span>

### <span data-ttu-id="cc8e8-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cc8e8-166">System.String[]</span></span>

### <span data-ttu-id="cc8e8-167">Microsoft.Azure.Commands.Network.models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="cc8e8-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="cc8e8-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc8e8-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cc8e8-169">輸出</span><span class="sxs-lookup"><span data-stu-id="cc8e8-169">OUTPUTS</span></span>

### <span data-ttu-id="cc8e8-170">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc8e8-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cc8e8-171">筆記</span><span class="sxs-lookup"><span data-stu-id="cc8e8-171">NOTES</span></span>

## <span data-ttu-id="cc8e8-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc8e8-172">RELATED LINKS</span></span>

[<span data-ttu-id="cc8e8-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc8e8-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="cc8e8-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc8e8-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="cc8e8-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc8e8-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="cc8e8-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="cc8e8-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
