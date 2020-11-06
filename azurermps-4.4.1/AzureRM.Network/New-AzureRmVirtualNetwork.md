---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 7fccc6b16d44e9bd050d40a21a748dbd1d251a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457540"
---
# <span data-ttu-id="fe95f-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe95f-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="fe95f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe95f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe95f-103">建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe95f-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe95f-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe95f-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe95f-105">DESCRIPTION</span></span>
<span data-ttu-id="fe95f-106">**新的-AzureRmVirtualNetwork** Cmdlet 會建立 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="fe95f-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe95f-107">EXAMPLES</span></span>

### <span data-ttu-id="fe95f-108">1：建立具有兩個子網的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="fe95f-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="fe95f-109">這個範例會建立具有兩個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="fe95f-110">首先，在 centralus 區域中建立新的資源群組。</span><span class="sxs-lookup"><span data-stu-id="fe95f-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="fe95f-111">接著，此範例會建立兩個子網的記憶體內表示形式。</span><span class="sxs-lookup"><span data-stu-id="fe95f-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="fe95f-112">New-AzureRmVirtualNetworkSubnetConfig Cmdlet 不會在伺服器端建立任何子網。</span><span class="sxs-lookup"><span data-stu-id="fe95f-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="fe95f-113">有一個名為 frontendSubnet 的子網，另一個名為 backendSubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="fe95f-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="fe95f-114">然後，New-AzureRmVirtualNetwork Cmdlet 會使用 CIDR 10.0.0.0/16 作為位址首碼和兩個子網來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="fe95f-115">2：使用 DNS 設定建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="fe95f-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="fe95f-116">這個範例會建立具有兩個子網和兩個 DNS 伺服器的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="fe95f-117">在虛擬網路上指定 DNS 伺服器的效果是，部署到此虛擬網路的 Nic/Vm 會繼承這些 DNS 伺服器作為預設值。</span><span class="sxs-lookup"><span data-stu-id="fe95f-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="fe95f-118">您可以透過 NIC 層級設定，在每個 NIC 中覆寫這些預設值。</span><span class="sxs-lookup"><span data-stu-id="fe95f-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="fe95f-119">如果在 VNET 中沒有指定 DNS 伺服器，且 Nic 上沒有任何 DNS 伺服器，則會使用預設的 Azure DNS 伺服器進行 DNS 解析。</span><span class="sxs-lookup"><span data-stu-id="fe95f-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="fe95f-120">3：使用子網參照網路安全群組建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="fe95f-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="fe95f-121">這個範例會建立具有參照網路安全性群組之子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="fe95f-122">首先，這個範例會建立一個資源群組做為要建立之資源的容器。</span><span class="sxs-lookup"><span data-stu-id="fe95f-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="fe95f-123">接著，建立允許入站 RDP 存取的網路安全群組，但其他強制執行預設網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="fe95f-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="fe95f-124">New-AzureRmVirtualNetworkSubnetConfig Cmdlet 會建立兩個子網的記憶體中表示形式，兩者都參照所建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe95f-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="fe95f-125">[New-AzureRmVirtualNetwork] 命令接著會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fe95f-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="fe95f-126">參數</span><span class="sxs-lookup"><span data-stu-id="fe95f-126">PARAMETERS</span></span>

### <span data-ttu-id="fe95f-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fe95f-127">-AddressPrefix</span></span>
<span data-ttu-id="fe95f-128">指定虛擬網路的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="fe95f-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe95f-129">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="fe95f-129">-DnsServer</span></span>
<span data-ttu-id="fe95f-130">指定子網的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="fe95f-130">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe95f-131">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="fe95f-131">-EnableVmProtection</span></span>
<span data-ttu-id="fe95f-132">代表是否已啟用 Vm 保護的 switch 參數。</span><span class="sxs-lookup"><span data-stu-id="fe95f-132">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe95f-133">-Force</span><span class="sxs-lookup"><span data-stu-id="fe95f-133">-Force</span></span>
<span data-ttu-id="fe95f-134">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fe95f-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe95f-135">-位置</span><span class="sxs-lookup"><span data-stu-id="fe95f-135">-Location</span></span>
<span data-ttu-id="fe95f-136">指定虛擬網路的地區。</span><span class="sxs-lookup"><span data-stu-id="fe95f-136">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="fe95f-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe95f-137">-Name</span></span>
<span data-ttu-id="fe95f-138">指定此 Cmdlet 所建立之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe95f-138">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe95f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe95f-139">-ResourceGroupName</span></span>
<span data-ttu-id="fe95f-140">指定要包含虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe95f-140">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="fe95f-141">-子網</span><span class="sxs-lookup"><span data-stu-id="fe95f-141">-Subnet</span></span>
<span data-ttu-id="fe95f-142">指定要與虛擬網路關聯的子網清單。</span><span class="sxs-lookup"><span data-stu-id="fe95f-142">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe95f-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe95f-143">-Tag</span></span>
<span data-ttu-id="fe95f-144">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="fe95f-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe95f-145">例如：</span><span class="sxs-lookup"><span data-stu-id="fe95f-145">For example:</span></span>

<span data-ttu-id="fe95f-146">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fe95f-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fe95f-147">-確認</span><span class="sxs-lookup"><span data-stu-id="fe95f-147">-Confirm</span></span>
<span data-ttu-id="fe95f-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe95f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe95f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe95f-149">-WhatIf</span></span>
<span data-ttu-id="fe95f-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe95f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe95f-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe95f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe95f-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe95f-152">-DefaultProfile</span></span>
<span data-ttu-id="fe95f-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe95f-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe95f-154">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="fe95f-154">-EnableDDoSProtection</span></span>
<span data-ttu-id="fe95f-155">代表是否已啟用 DDoS 保護的切換參數。</span><span class="sxs-lookup"><span data-stu-id="fe95f-155">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe95f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe95f-156">CommonParameters</span></span>
<span data-ttu-id="fe95f-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe95f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe95f-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe95f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe95f-159">輸入</span><span class="sxs-lookup"><span data-stu-id="fe95f-159">INPUTS</span></span>

## <span data-ttu-id="fe95f-160">輸出</span><span class="sxs-lookup"><span data-stu-id="fe95f-160">OUTPUTS</span></span>

### <span data-ttu-id="fe95f-161">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe95f-161">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fe95f-162">筆記</span><span class="sxs-lookup"><span data-stu-id="fe95f-162">NOTES</span></span>

## <span data-ttu-id="fe95f-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe95f-163">RELATED LINKS</span></span>

[<span data-ttu-id="fe95f-164">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe95f-164">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fe95f-165">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe95f-165">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fe95f-166">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe95f-166">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
