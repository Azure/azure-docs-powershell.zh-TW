---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 9c52a5f234b374612b07d53b21ac9409a45cc35a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624593"
---
# <span data-ttu-id="e6272-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6272-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="e6272-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6272-102">SYNOPSIS</span></span>
<span data-ttu-id="e6272-103">建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6272-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6272-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-EnableVmProtection] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6272-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6272-105">DESCRIPTION</span></span>
<span data-ttu-id="e6272-106">**新的-AzureRmVirtualNetwork** Cmdlet 會建立 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="e6272-107">示例</span><span class="sxs-lookup"><span data-stu-id="e6272-107">EXAMPLES</span></span>

### <span data-ttu-id="e6272-108">1：建立具有兩個子網的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="e6272-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="e6272-109">這個範例會建立具有兩個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="e6272-110">首先，在 centralus 區域中建立新的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e6272-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="e6272-111">接著，此範例會建立兩個子網的記憶體內表示形式。</span><span class="sxs-lookup"><span data-stu-id="e6272-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="e6272-112">New-AzureRmVirtualNetworkSubnetConfig Cmdlet 不會在伺服器端建立任何子網。</span><span class="sxs-lookup"><span data-stu-id="e6272-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="e6272-113">有一個名為 frontendSubnet 的子網，另一個名為 backendSubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="e6272-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="e6272-114">然後，New-AzureRmVirtualNetwork Cmdlet 會使用 CIDR 10.0.0.0/16 作為位址首碼和兩個子網來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="e6272-115">2：使用 DNS 設定建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="e6272-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="e6272-116">這個範例會建立具有兩個子網和兩個 DNS 伺服器的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="e6272-117">在虛擬網路上指定 DNS 伺服器的效果是，部署到此虛擬網路的 Nic/Vm 會繼承這些 DNS 伺服器作為預設值。</span><span class="sxs-lookup"><span data-stu-id="e6272-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="e6272-118">您可以透過 NIC 層級設定，在每個 NIC 中覆寫這些預設值。</span><span class="sxs-lookup"><span data-stu-id="e6272-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="e6272-119">如果在 VNET 中沒有指定 DNS 伺服器，且 Nic 上沒有任何 DNS 伺服器，則會使用預設的 Azure DNS 伺服器進行 DNS 解析。</span><span class="sxs-lookup"><span data-stu-id="e6272-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="e6272-120">3：使用子網參照網路安全群組建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="e6272-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="e6272-121">這個範例會建立具有參照網路安全性群組之子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="e6272-122">首先，這個範例會建立一個資源群組做為要建立之資源的容器。</span><span class="sxs-lookup"><span data-stu-id="e6272-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="e6272-123">接著，建立允許入站 RDP 存取的網路安全群組，但其他強制執行預設網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="e6272-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="e6272-124">New-AzureRmVirtualNetworkSubnetConfig Cmdlet 會建立兩個子網的記憶體中表示形式，兩者都參照所建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="e6272-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="e6272-125">[New-AzureRmVirtualNetwork] 命令接著會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="e6272-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="e6272-126">參數</span><span class="sxs-lookup"><span data-stu-id="e6272-126">PARAMETERS</span></span>

### <span data-ttu-id="e6272-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e6272-127">-AddressPrefix</span></span>
<span data-ttu-id="e6272-128">指定虛擬網路的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="e6272-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="e6272-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6272-129">-AsJob</span></span>
<span data-ttu-id="e6272-130">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e6272-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6272-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="e6272-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="e6272-132">參考與虛擬網路相關聯的 DDoS 保護方案資源。</span><span class="sxs-lookup"><span data-stu-id="e6272-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="e6272-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6272-133">-DefaultProfile</span></span>
<span data-ttu-id="e6272-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6272-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6272-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="e6272-135">-DnsServer</span></span>
<span data-ttu-id="e6272-136">指定子網的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6272-136">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="e6272-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="e6272-137">-EnableDdosProtection</span></span>
<span data-ttu-id="e6272-138">代表是否已啟用 DDoS 保護的切換參數。</span><span class="sxs-lookup"><span data-stu-id="e6272-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="e6272-139">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="e6272-139">-EnableVmProtection</span></span>
<span data-ttu-id="e6272-140">代表是否已啟用 Vm 保護的 switch 參數。</span><span class="sxs-lookup"><span data-stu-id="e6272-140">A switch parameter which represents if Vm protection is enabled or not.</span></span>

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

### <span data-ttu-id="e6272-141">-Force</span><span class="sxs-lookup"><span data-stu-id="e6272-141">-Force</span></span>
<span data-ttu-id="e6272-142">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e6272-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6272-143">-位置</span><span class="sxs-lookup"><span data-stu-id="e6272-143">-Location</span></span>
<span data-ttu-id="e6272-144">指定虛擬網路的地區。</span><span class="sxs-lookup"><span data-stu-id="e6272-144">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="e6272-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6272-145">-Name</span></span>
<span data-ttu-id="e6272-146">指定此 Cmdlet 所建立之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6272-146">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e6272-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6272-147">-ResourceGroupName</span></span>
<span data-ttu-id="e6272-148">指定要包含虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6272-148">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="e6272-149">-子網</span><span class="sxs-lookup"><span data-stu-id="e6272-149">-Subnet</span></span>
<span data-ttu-id="e6272-150">指定要與虛擬網路關聯的子網清單。</span><span class="sxs-lookup"><span data-stu-id="e6272-150">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="e6272-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6272-151">-Tag</span></span>
<span data-ttu-id="e6272-152">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e6272-152">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e6272-153">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e6272-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e6272-154">-確認</span><span class="sxs-lookup"><span data-stu-id="e6272-154">-Confirm</span></span>
<span data-ttu-id="e6272-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6272-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6272-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6272-156">-WhatIf</span></span>
<span data-ttu-id="e6272-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6272-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6272-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6272-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6272-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6272-159">CommonParameters</span></span>
<span data-ttu-id="e6272-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6272-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6272-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6272-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6272-162">輸入</span><span class="sxs-lookup"><span data-stu-id="e6272-162">INPUTS</span></span>

### <span data-ttu-id="e6272-163">System.object</span><span class="sxs-lookup"><span data-stu-id="e6272-163">System.String</span></span>

### <span data-ttu-id="e6272-164">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e6272-164">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e6272-165">[System.object]. 清單 ' 1 [PSSubnet，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="e6272-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSubnet, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e6272-166">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6272-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6272-167">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e6272-167">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6272-168">輸出</span><span class="sxs-lookup"><span data-stu-id="e6272-168">OUTPUTS</span></span>

### <span data-ttu-id="e6272-169">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6272-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e6272-170">筆記</span><span class="sxs-lookup"><span data-stu-id="e6272-170">NOTES</span></span>

## <span data-ttu-id="e6272-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6272-171">RELATED LINKS</span></span>

[<span data-ttu-id="e6272-172">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6272-172">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e6272-173">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6272-173">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e6272-174">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6272-174">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e6272-175">新-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e6272-175">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)
