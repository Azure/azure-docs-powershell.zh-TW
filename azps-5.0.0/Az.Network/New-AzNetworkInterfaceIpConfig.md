---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138335"
---
# <span data-ttu-id="72e98-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="72e98-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="72e98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72e98-102">SYNOPSIS</span></span>
<span data-ttu-id="72e98-103">建立網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="72e98-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="72e98-104">句法</span><span class="sxs-lookup"><span data-stu-id="72e98-104">SYNTAX</span></span>

### <span data-ttu-id="72e98-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="72e98-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72e98-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72e98-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e98-107">說明</span><span class="sxs-lookup"><span data-stu-id="72e98-107">DESCRIPTION</span></span>
<span data-ttu-id="72e98-108">**新的 AzNetworkInterfaceIpConfig** Cmdlet 會建立網路介面的 Azure 網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="72e98-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="72e98-109">示例</span><span class="sxs-lookup"><span data-stu-id="72e98-109">EXAMPLES</span></span>

### <span data-ttu-id="72e98-110">1：使用網路介面的公用 IP 位址建立 IP 配置</span><span class="sxs-lookup"><span data-stu-id="72e98-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="72e98-111">前兩個命令會取得稱為 myvnet 的虛擬網路，以及與先前建立的子網 mysubnet。</span><span class="sxs-lookup"><span data-stu-id="72e98-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="72e98-112">這些專案會分別儲存在 $vnet 和 $Subnet 中。</span><span class="sxs-lookup"><span data-stu-id="72e98-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="72e98-113">第三個命令會取得先前建立的公用 IP 位址（稱為 PIP1）。</span><span class="sxs-lookup"><span data-stu-id="72e98-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="72e98-114">向下的命令會建立名為 "IPConfig-1" 的新 IP 配置，作為主要 IP 位址與它相關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="72e98-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="72e98-115">最後一個命令接著會建立一個名為 mynic1 的網路介面，使用這個 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="72e98-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="72e98-116">2：建立含私人 IP 位址的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="72e98-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="72e98-117">前兩個命令會取得稱為 myvnet 的虛擬網路，以及與先前建立的子網 mysubnet。</span><span class="sxs-lookup"><span data-stu-id="72e98-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="72e98-118">這些專案會分別儲存在 $vnet 和 $Subnet 中。</span><span class="sxs-lookup"><span data-stu-id="72e98-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="72e98-119">第三個命令會建立名為 "IPConfig-2" 的新 IP 配置，並提供與其相關聯的私人 IP 位址10.0.0.5。</span><span class="sxs-lookup"><span data-stu-id="72e98-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="72e98-120">最後一個命令接著會建立一個名為 mynic1 的網路介面，使用這個 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="72e98-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="72e98-121">參數</span><span class="sxs-lookup"><span data-stu-id="72e98-121">PARAMETERS</span></span>

### <span data-ttu-id="72e98-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72e98-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="72e98-123">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="72e98-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="72e98-125">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="72e98-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="72e98-127">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="72e98-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="72e98-129">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e98-130">-DefaultProfile</span></span>
<span data-ttu-id="72e98-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72e98-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e98-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72e98-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="72e98-133">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="72e98-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="72e98-135">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="72e98-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="72e98-137">指定此網路介面 IPConfiguration 所屬的負載等化器入站 Nat 規則參照集合。</span><span class="sxs-lookup"><span data-stu-id="72e98-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="72e98-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="72e98-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="72e98-139">指定一個負載平衡器入站網路位址的集合， (NAT) 規則參照，此網路介面 IP 設定屬於這個配置。</span><span class="sxs-lookup"><span data-stu-id="72e98-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="72e98-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="72e98-140">-Name</span></span>
<span data-ttu-id="72e98-141">指定網路介面 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="72e98-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="72e98-142">-主要</span><span class="sxs-lookup"><span data-stu-id="72e98-142">-Primary</span></span>
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

### <span data-ttu-id="72e98-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="72e98-143">-PrivateIpAddress</span></span>
<span data-ttu-id="72e98-144">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="72e98-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="72e98-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="72e98-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="72e98-146">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="72e98-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="72e98-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="72e98-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72e98-148">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="72e98-148">IPv4</span></span>
- <span data-ttu-id="72e98-149">Ipv4</span><span class="sxs-lookup"><span data-stu-id="72e98-149">IPv6</span></span>

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

### <span data-ttu-id="72e98-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="72e98-150">-PublicIpAddress</span></span>
<span data-ttu-id="72e98-151">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="72e98-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="72e98-152">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="72e98-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="72e98-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="72e98-153">-PublicIpAddressId</span></span>
<span data-ttu-id="72e98-154">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="72e98-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="72e98-155">-子網</span><span class="sxs-lookup"><span data-stu-id="72e98-155">-Subnet</span></span>
<span data-ttu-id="72e98-156">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="72e98-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="72e98-157">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="72e98-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="72e98-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="72e98-158">-SubnetId</span></span>
<span data-ttu-id="72e98-159">指定要在其中建立此網路介面 IP 設定之子網上的參照。</span><span class="sxs-lookup"><span data-stu-id="72e98-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="72e98-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e98-160">CommonParameters</span></span>
<span data-ttu-id="72e98-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72e98-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e98-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72e98-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e98-163">輸入</span><span class="sxs-lookup"><span data-stu-id="72e98-163">INPUTS</span></span>

### <span data-ttu-id="72e98-164">System.object []</span><span class="sxs-lookup"><span data-stu-id="72e98-164">System.String[]</span></span>

### <span data-ttu-id="72e98-165">PSBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="72e98-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="72e98-166">PSInboundNatRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="72e98-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="72e98-167">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="72e98-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="72e98-168">PSApplicationSecurityGroup [] （[]）</span><span class="sxs-lookup"><span data-stu-id="72e98-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="72e98-169">輸出</span><span class="sxs-lookup"><span data-stu-id="72e98-169">OUTPUTS</span></span>

### <span data-ttu-id="72e98-170">PSNetworkInterfaceIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72e98-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="72e98-171">筆記</span><span class="sxs-lookup"><span data-stu-id="72e98-171">NOTES</span></span>
* <span data-ttu-id="72e98-172">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="72e98-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="72e98-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="72e98-173">RELATED LINKS</span></span>

[<span data-ttu-id="72e98-174">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="72e98-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="72e98-175">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="72e98-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="72e98-176">移除-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="72e98-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="72e98-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="72e98-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
