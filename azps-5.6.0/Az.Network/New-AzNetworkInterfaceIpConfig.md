---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 72d2439e66245e8469e440cb5e501cd9e9379fa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902406"
---
# <span data-ttu-id="53a34-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53a34-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="53a34-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53a34-102">SYNOPSIS</span></span>
<span data-ttu-id="53a34-103">建立網路介面 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="53a34-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="53a34-104">語法</span><span class="sxs-lookup"><span data-stu-id="53a34-104">SYNTAX</span></span>

### <span data-ttu-id="53a34-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="53a34-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53a34-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53a34-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a34-107">描述</span><span class="sxs-lookup"><span data-stu-id="53a34-107">DESCRIPTION</span></span>
<span data-ttu-id="53a34-108">**New-AzNetworkInterfaceIpConfig** Cmdlet 會為網路介面建立 Azure 網路介面 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="53a34-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="53a34-109">例子</span><span class="sxs-lookup"><span data-stu-id="53a34-109">EXAMPLES</span></span>

### <span data-ttu-id="53a34-110">1：使用公用 IP 位址建立網路介面的 IP 組配置</span><span class="sxs-lookup"><span data-stu-id="53a34-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="53a34-111">前兩個命令會分別取得稱為 myvnet 的虛擬網路和先前建立名為 mysubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="53a34-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="53a34-112">這些分別儲存在 $vnet 和 $Subnet 中。</span><span class="sxs-lookup"><span data-stu-id="53a34-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="53a34-113">第三個命令會獲得先前建立公用 IP 位址，稱為PIP1。</span><span class="sxs-lookup"><span data-stu-id="53a34-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="53a34-114">第四個命令會建立一個稱為「IPConfig-1」的新 IP 組式，做為與它相關聯的公用 IP 位址的主要 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="53a34-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="53a34-115">最後一個命令接著會使用此 IP 組配置建立稱為 mynic1 的網路介面。</span><span class="sxs-lookup"><span data-stu-id="53a34-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="53a34-116">2：使用私人 IP 位址建立 IP 組</span><span class="sxs-lookup"><span data-stu-id="53a34-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="53a34-117">前兩個命令會分別取得稱為 myvnet 的虛擬網路和先前建立名為 mysubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="53a34-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="53a34-118">這些分別儲存在 $vnet 和 $Subnet 中。</span><span class="sxs-lookup"><span data-stu-id="53a34-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="53a34-119">第三個命令會建立名為「IPConfig-2」的新 IP 組式，並與其相關聯的私人 IP 位址 10.0.0.5。</span><span class="sxs-lookup"><span data-stu-id="53a34-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="53a34-120">最後一個命令接著會使用此 IP 組配置建立稱為 mynic1 的網路介面。</span><span class="sxs-lookup"><span data-stu-id="53a34-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="53a34-121">參數</span><span class="sxs-lookup"><span data-stu-id="53a34-121">PARAMETERS</span></span>

### <span data-ttu-id="53a34-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53a34-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="53a34-123">指定此網路介面 IP 組配置所屬的應用程式閘道後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="53a34-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="53a34-125">指定此網路介面 IP 組配置所屬的應用程式閘道後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53a34-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="53a34-127">指定此網路介面 IP 組配置所屬的應用程式安全性群組參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="53a34-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="53a34-129">指定此網路介面 IP 組配置所屬的應用程式安全性群組參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a34-130">-DefaultProfile</span></span>
<span data-ttu-id="53a34-131">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a34-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a34-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53a34-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="53a34-133">指定此網路介面 IP 組配置所屬的負載平衡器後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="53a34-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="53a34-135">指定此網路介面 IP 組配置所屬的負載平衡器後端位址集區參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="53a34-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="53a34-137">指定此網路介面 IPConfiguration 所屬的負載平衡器內入 Nat Rule 參照集合。</span><span class="sxs-lookup"><span data-stu-id="53a34-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="53a34-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="53a34-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="53a34-139">指定一組負載平衡器輸入網路位址轉譯 (NAT) 此網路介面 IP 配置所屬的規則參照。</span><span class="sxs-lookup"><span data-stu-id="53a34-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="53a34-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="53a34-140">-Name</span></span>
<span data-ttu-id="53a34-141">指定網路介面 IP 群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a34-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="53a34-142">-主要</span><span class="sxs-lookup"><span data-stu-id="53a34-142">-Primary</span></span>
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

### <span data-ttu-id="53a34-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="53a34-143">-PrivateIpAddress</span></span>
<span data-ttu-id="53a34-144">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="53a34-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="53a34-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="53a34-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="53a34-146">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="53a34-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="53a34-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="53a34-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53a34-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="53a34-148">IPv4</span></span>
- <span data-ttu-id="53a34-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="53a34-149">IPv6</span></span>

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

### <span data-ttu-id="53a34-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53a34-150">-PublicIpAddress</span></span>
<span data-ttu-id="53a34-151">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="53a34-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="53a34-152">此 Cmdlet 會建立公用 IP 位址的參照，以與這個網路介面 IP 組組建立關聯。</span><span class="sxs-lookup"><span data-stu-id="53a34-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="53a34-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="53a34-153">-PublicIpAddressId</span></span>
<span data-ttu-id="53a34-154">此 Cmdlet 會建立公用 IP 位址的參照，以與這個網路介面 IP 組組建立關聯。</span><span class="sxs-lookup"><span data-stu-id="53a34-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="53a34-155">-子網</span><span class="sxs-lookup"><span data-stu-id="53a34-155">-Subnet</span></span>
<span data-ttu-id="53a34-156">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="53a34-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="53a34-157">此 Cmdlet 會建立子網的參照，以建立此網路介面 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="53a34-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="53a34-158">-子網Id</span><span class="sxs-lookup"><span data-stu-id="53a34-158">-SubnetId</span></span>
<span data-ttu-id="53a34-159">指定建立此網路介面 IP 配置的子網參照。</span><span class="sxs-lookup"><span data-stu-id="53a34-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="53a34-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a34-160">CommonParameters</span></span>
<span data-ttu-id="53a34-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53a34-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a34-162">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="53a34-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a34-163">輸入</span><span class="sxs-lookup"><span data-stu-id="53a34-163">INPUTS</span></span>

### <span data-ttu-id="53a34-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53a34-164">System.String[]</span></span>

### <span data-ttu-id="53a34-165">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="53a34-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="53a34-166">Microsoft.Azure.Commands.Network.models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="53a34-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="53a34-167">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="53a34-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="53a34-168">Microsoft.Azure.Commands.Network.models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="53a34-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="53a34-169">輸出</span><span class="sxs-lookup"><span data-stu-id="53a34-169">OUTPUTS</span></span>

### <span data-ttu-id="53a34-170">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53a34-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="53a34-171">筆記</span><span class="sxs-lookup"><span data-stu-id="53a34-171">NOTES</span></span>
* <span data-ttu-id="53a34-172">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="53a34-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="53a34-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a34-173">RELATED LINKS</span></span>

[<span data-ttu-id="53a34-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53a34-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="53a34-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53a34-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="53a34-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53a34-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="53a34-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53a34-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
