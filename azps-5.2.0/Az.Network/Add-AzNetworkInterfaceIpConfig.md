---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281738"
---
# <span data-ttu-id="a33f8-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a33f8-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="a33f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a33f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a33f8-103">將網路介面 IP 設定新增至網路介面。</span><span class="sxs-lookup"><span data-stu-id="a33f8-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="a33f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="a33f8-104">SYNTAX</span></span>

### <span data-ttu-id="a33f8-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a33f8-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33f8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a33f8-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33f8-107">說明</span><span class="sxs-lookup"><span data-stu-id="a33f8-107">DESCRIPTION</span></span>
<span data-ttu-id="a33f8-108">**AzNetworkInterfaceIpConfig** Cmdlet 會將網路介面 IP 配置新增至 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="a33f8-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="a33f8-109">示例</span><span class="sxs-lookup"><span data-stu-id="a33f8-109">EXAMPLES</span></span>

### <span data-ttu-id="a33f8-110">範例1：使用應用程式安全性群組新增新的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="a33f8-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="a33f8-111">在這個範例中，我們會在新的虛擬網路 MyVNET 中建立屬於子網的新網路介面 MyNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="a33f8-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="a33f8-112">我們也會建立一個空白的應用程式安全性群組 MyASG，以與網路介面中的 IP 配置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a33f8-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="a33f8-113">建立兩個物件之後，我們會將預設的 IP 設定連結到 MyASG 物件。</span><span class="sxs-lookup"><span data-stu-id="a33f8-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="a33f8-114">最後，我們會在網路介面中建立新的 IP 設定，也就是連結到應用程式安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="a33f8-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="a33f8-115">參數</span><span class="sxs-lookup"><span data-stu-id="a33f8-115">PARAMETERS</span></span>

### <span data-ttu-id="a33f8-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a33f8-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="a33f8-117">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a33f8-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="a33f8-119">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a33f8-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="a33f8-121">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a33f8-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="a33f8-123">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33f8-124">-DefaultProfile</span></span>
<span data-ttu-id="a33f8-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a33f8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a33f8-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a33f8-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="a33f8-127">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a33f8-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="a33f8-129">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a33f8-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="a33f8-131">指定一個負載平衡器入站網路位址的集合， (NAT) 規則參照，此網路介面 IP 設定屬於這個配置。</span><span class="sxs-lookup"><span data-stu-id="a33f8-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="a33f8-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="a33f8-133">指定此網路介面 IP 配置所屬的負載等化器入站 NAT 規則參照集合。</span><span class="sxs-lookup"><span data-stu-id="a33f8-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a33f8-134">-Name</span></span>
<span data-ttu-id="a33f8-135">指定網路介面 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a33f8-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="a33f8-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a33f8-136">-NetworkInterface</span></span>
<span data-ttu-id="a33f8-137">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="a33f8-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="a33f8-138">這個 Cmdlet 會將網路介面 IP 設定新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="a33f8-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-139">-主要</span><span class="sxs-lookup"><span data-stu-id="a33f8-139">-Primary</span></span>
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

### <span data-ttu-id="a33f8-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a33f8-140">-PrivateIpAddress</span></span>
<span data-ttu-id="a33f8-141">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a33f8-141">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a33f8-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="a33f8-143">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="a33f8-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="a33f8-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a33f8-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a33f8-145">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="a33f8-145">IPv4</span></span>
- <span data-ttu-id="a33f8-146">Ipv4</span><span class="sxs-lookup"><span data-stu-id="a33f8-146">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a33f8-147">-PublicIpAddress</span></span>
<span data-ttu-id="a33f8-148">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="a33f8-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="a33f8-149">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a33f8-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a33f8-150">-PublicIpAddressId</span></span>
<span data-ttu-id="a33f8-151">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a33f8-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-152">-子網</span><span class="sxs-lookup"><span data-stu-id="a33f8-152">-Subnet</span></span>
<span data-ttu-id="a33f8-153">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="a33f8-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="a33f8-154">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="a33f8-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a33f8-155">-SubnetId</span></span>
<span data-ttu-id="a33f8-156">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="a33f8-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33f8-157">CommonParameters</span></span>
<span data-ttu-id="a33f8-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a33f8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33f8-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a33f8-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33f8-160">輸入</span><span class="sxs-lookup"><span data-stu-id="a33f8-160">INPUTS</span></span>

### <span data-ttu-id="a33f8-161">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a33f8-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="a33f8-162">System.object []</span><span class="sxs-lookup"><span data-stu-id="a33f8-162">System.String[]</span></span>

### <span data-ttu-id="a33f8-163">PSBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a33f8-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="a33f8-164">PSInboundNatRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a33f8-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="a33f8-165">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a33f8-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="a33f8-166">PSApplicationSecurityGroup [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a33f8-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="a33f8-167">輸出</span><span class="sxs-lookup"><span data-stu-id="a33f8-167">OUTPUTS</span></span>

### <span data-ttu-id="a33f8-168">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a33f8-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a33f8-169">筆記</span><span class="sxs-lookup"><span data-stu-id="a33f8-169">NOTES</span></span>
* <span data-ttu-id="a33f8-170">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="a33f8-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a33f8-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="a33f8-171">RELATED LINKS</span></span>

[<span data-ttu-id="a33f8-172">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a33f8-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a33f8-173">新-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a33f8-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a33f8-174">移除-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a33f8-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a33f8-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a33f8-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
