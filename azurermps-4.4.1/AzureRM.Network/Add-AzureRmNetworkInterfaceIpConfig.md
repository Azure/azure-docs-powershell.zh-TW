---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 57c92345537e72a38c5228c0a10d38f6ad61d13a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456523"
---
# <span data-ttu-id="a43e6-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a43e6-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="a43e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a43e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a43e6-103">將網路介面 IP 設定新增至網路介面。</span><span class="sxs-lookup"><span data-stu-id="a43e6-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a43e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a43e6-104">SYNTAX</span></span>

### <span data-ttu-id="a43e6-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a43e6-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43e6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a43e6-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43e6-107">說明</span><span class="sxs-lookup"><span data-stu-id="a43e6-107">DESCRIPTION</span></span>
<span data-ttu-id="a43e6-108">**AzureRmNetworkInterfaceIpConfig** Cmdlet 會將網路介面 IP 配置新增至 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="a43e6-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="a43e6-109">示例</span><span class="sxs-lookup"><span data-stu-id="a43e6-109">EXAMPLES</span></span>

### <span data-ttu-id="a43e6-110">範例1：使用應用程式安全性群組新增新的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="a43e6-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="a43e6-111">在這個範例中，我們會在新的虛擬網路 MyVNET 中建立屬於子網的新網路介面 MyNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="a43e6-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="a43e6-112">我們也會建立一個空白的應用程式安全性群組 MyASG，以與網路介面中的 IP 配置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a43e6-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="a43e6-113">建立兩個物件之後，我們會將預設的 IP 設定連結到 MyASG 物件。</span><span class="sxs-lookup"><span data-stu-id="a43e6-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="a43e6-114">最後，我們會在網路介面中建立新的 IP 設定，也就是連結到應用程式安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="a43e6-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="a43e6-115">參數</span><span class="sxs-lookup"><span data-stu-id="a43e6-115">PARAMETERS</span></span>

### <span data-ttu-id="a43e6-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a43e6-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="a43e6-117">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a43e6-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="a43e6-119">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43e6-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="a43e6-121">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a43e6-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="a43e6-123">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43e6-124">-DefaultProfile</span></span>
<span data-ttu-id="a43e6-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a43e6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a43e6-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a43e6-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="a43e6-127">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a43e6-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="a43e6-129">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a43e6-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="a43e6-131">指定一個負載平衡器入站網路位址的集合， (NAT) 規則參照，此網路介面 IP 設定屬於這個配置。</span><span class="sxs-lookup"><span data-stu-id="a43e6-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="a43e6-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="a43e6-133">指定此網路介面 IP 配置所屬的負載等化器入站 NAT 規則參照集合。</span><span class="sxs-lookup"><span data-stu-id="a43e6-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43e6-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a43e6-134">-Name</span></span>
<span data-ttu-id="a43e6-135">指定網路介面 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a43e6-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="a43e6-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a43e6-136">-NetworkInterface</span></span>
<span data-ttu-id="a43e6-137">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="a43e6-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="a43e6-138">這個 Cmdlet 會將網路介面 IP 設定新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="a43e6-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="a43e6-139">-主要</span><span class="sxs-lookup"><span data-stu-id="a43e6-139">-Primary</span></span>
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

### <span data-ttu-id="a43e6-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a43e6-140">-PrivateIpAddress</span></span>
<span data-ttu-id="a43e6-141">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a43e6-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="a43e6-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a43e6-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="a43e6-143">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="a43e6-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="a43e6-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a43e6-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a43e6-145">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="a43e6-145">IPv4</span></span>
- <span data-ttu-id="a43e6-146">Ipv4</span><span class="sxs-lookup"><span data-stu-id="a43e6-146">IPv6</span></span>

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

### <span data-ttu-id="a43e6-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a43e6-147">-PublicIpAddress</span></span>
<span data-ttu-id="a43e6-148">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="a43e6-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="a43e6-149">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a43e6-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="a43e6-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a43e6-150">-PublicIpAddressId</span></span>
<span data-ttu-id="a43e6-151">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a43e6-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="a43e6-152">-子網</span><span class="sxs-lookup"><span data-stu-id="a43e6-152">-Subnet</span></span>
<span data-ttu-id="a43e6-153">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="a43e6-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="a43e6-154">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="a43e6-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="a43e6-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a43e6-155">-SubnetId</span></span>
<span data-ttu-id="a43e6-156">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="a43e6-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="a43e6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43e6-157">CommonParameters</span></span>
<span data-ttu-id="a43e6-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a43e6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43e6-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a43e6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43e6-160">輸入</span><span class="sxs-lookup"><span data-stu-id="a43e6-160">INPUTS</span></span>

### <span data-ttu-id="a43e6-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a43e6-161">PSNetworkInterface</span></span>
<span data-ttu-id="a43e6-162">形參 "NetworkInterface" 接受管線中 "PSNetworkInterface" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a43e6-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="a43e6-163">輸出</span><span class="sxs-lookup"><span data-stu-id="a43e6-163">OUTPUTS</span></span>

### <span data-ttu-id="a43e6-164">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a43e6-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a43e6-165">筆記</span><span class="sxs-lookup"><span data-stu-id="a43e6-165">NOTES</span></span>
* <span data-ttu-id="a43e6-166">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="a43e6-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a43e6-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="a43e6-167">RELATED LINKS</span></span>

[<span data-ttu-id="a43e6-168">AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a43e6-168">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a43e6-169">新-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a43e6-169">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a43e6-170">移除-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a43e6-170">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a43e6-171">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a43e6-171">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


