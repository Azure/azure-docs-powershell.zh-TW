---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 47ad7c00c2db310003dcc87b20405d05ec7f1f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916611"
---
# <span data-ttu-id="897b7-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="897b7-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="897b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="897b7-102">SYNOPSIS</span></span>
<span data-ttu-id="897b7-103">新增網路介面 IP 組配置至網路介面。</span><span class="sxs-lookup"><span data-stu-id="897b7-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="897b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="897b7-104">SYNTAX</span></span>

### <span data-ttu-id="897b7-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="897b7-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="897b7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="897b7-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="897b7-107">描述</span><span class="sxs-lookup"><span data-stu-id="897b7-107">DESCRIPTION</span></span>
<span data-ttu-id="897b7-108">**Add-AzNetworkInterfaceIpConfig** Cmdlet 會將網路介面 IP 組配置新增到 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="897b7-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="897b7-109">例子</span><span class="sxs-lookup"><span data-stu-id="897b7-109">EXAMPLES</span></span>

### <span data-ttu-id="897b7-110">範例 1：使用應用程式安全性群組新增 IP 組</span><span class="sxs-lookup"><span data-stu-id="897b7-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="897b7-111">在此範例中，我們建立新網路介面 MyNetworkInterface，該介面屬於新虛擬網路 MyVNET 中的子網。</span><span class="sxs-lookup"><span data-stu-id="897b7-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="897b7-112">我們也建立空白應用程式安全性群組 MyASG，以與網路介面中的 IP 組建立關聯。</span><span class="sxs-lookup"><span data-stu-id="897b7-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="897b7-113">建立這兩個物件之後，我們會將預設 IP 群組原則連結至 MyASG 物件。</span><span class="sxs-lookup"><span data-stu-id="897b7-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="897b7-114">最後，我們在也連結至應用程式安全性群組物件的網路介面中建立新 IP 組。</span><span class="sxs-lookup"><span data-stu-id="897b7-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="897b7-115">參數</span><span class="sxs-lookup"><span data-stu-id="897b7-115">PARAMETERS</span></span>

### <span data-ttu-id="897b7-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="897b7-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="897b7-117">指定此網路介面 IP 組配置所屬的應用程式閘道後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="897b7-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="897b7-119">指定此網路介面 IP 組配置所屬的應用程式閘道後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="897b7-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="897b7-121">指定此網路介面 IP 組配置所屬的應用程式安全性群組參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="897b7-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="897b7-123">指定此網路介面 IP 組配置所屬的應用程式安全性群組參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897b7-124">-DefaultProfile</span></span>
<span data-ttu-id="897b7-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="897b7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="897b7-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="897b7-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="897b7-127">指定此網路介面 IP 組配置所屬的負載平衡器後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="897b7-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="897b7-129">指定此網路介面 IP 組配置所屬的負載平衡器後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="897b7-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="897b7-131">指定一組負載平衡器輸入網路位址轉譯 (NAT) 此網路介面 IP 配置所屬的規則參照。</span><span class="sxs-lookup"><span data-stu-id="897b7-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="897b7-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="897b7-133">指定此網路介面 IP 組配置所屬的負載平衡器內入 NAT 規則參照集合。</span><span class="sxs-lookup"><span data-stu-id="897b7-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="897b7-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="897b7-134">-Name</span></span>
<span data-ttu-id="897b7-135">指定網路介面 IP 群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="897b7-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="897b7-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="897b7-136">-NetworkInterface</span></span>
<span data-ttu-id="897b7-137">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="897b7-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="897b7-138">此 Cmdlet 會新增網路介面 IP 設定至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="897b7-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="897b7-139">-主要</span><span class="sxs-lookup"><span data-stu-id="897b7-139">-Primary</span></span>
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

### <span data-ttu-id="897b7-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="897b7-140">-PrivateIpAddress</span></span>
<span data-ttu-id="897b7-141">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="897b7-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="897b7-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="897b7-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="897b7-143">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="897b7-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="897b7-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="897b7-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="897b7-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="897b7-145">IPv4</span></span>
- <span data-ttu-id="897b7-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="897b7-146">IPv6</span></span>

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

### <span data-ttu-id="897b7-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="897b7-147">-PublicIpAddress</span></span>
<span data-ttu-id="897b7-148">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="897b7-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="897b7-149">此 Cmdlet 會建立公用 IP 位址的參照，以與這個網路介面 IP 組組建立關聯。</span><span class="sxs-lookup"><span data-stu-id="897b7-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="897b7-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="897b7-150">-PublicIpAddressId</span></span>
<span data-ttu-id="897b7-151">此 Cmdlet 會建立公用 IP 位址的參照，以與這個網路介面 IP 組組建立關聯。</span><span class="sxs-lookup"><span data-stu-id="897b7-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="897b7-152">-子網</span><span class="sxs-lookup"><span data-stu-id="897b7-152">-Subnet</span></span>
<span data-ttu-id="897b7-153">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="897b7-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="897b7-154">此 Cmdlet 會建立子網的參照，以建立此網路介面 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="897b7-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="897b7-155">-子網Id</span><span class="sxs-lookup"><span data-stu-id="897b7-155">-SubnetId</span></span>
<span data-ttu-id="897b7-156">此 Cmdlet 會建立子網的參照，以建立此網路介面 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="897b7-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="897b7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897b7-157">CommonParameters</span></span>
<span data-ttu-id="897b7-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="897b7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897b7-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="897b7-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897b7-160">輸入</span><span class="sxs-lookup"><span data-stu-id="897b7-160">INPUTS</span></span>

### <span data-ttu-id="897b7-161">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="897b7-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="897b7-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="897b7-162">System.String[]</span></span>

### <span data-ttu-id="897b7-163">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="897b7-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="897b7-164">Microsoft.Azure.Commands.Network.models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="897b7-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="897b7-165">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="897b7-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="897b7-166">Microsoft.Azure.Commands.Network.models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="897b7-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="897b7-167">輸出</span><span class="sxs-lookup"><span data-stu-id="897b7-167">OUTPUTS</span></span>

### <span data-ttu-id="897b7-168">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="897b7-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="897b7-169">筆記</span><span class="sxs-lookup"><span data-stu-id="897b7-169">NOTES</span></span>
* <span data-ttu-id="897b7-170">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="897b7-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="897b7-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="897b7-171">RELATED LINKS</span></span>

[<span data-ttu-id="897b7-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="897b7-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="897b7-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="897b7-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="897b7-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="897b7-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="897b7-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="897b7-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
