---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958435"
---
# <span data-ttu-id="e4b26-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4b26-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e4b26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4b26-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b26-103">更新網路介面的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="e4b26-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="e4b26-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4b26-104">SYNTAX</span></span>

### <span data-ttu-id="e4b26-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e4b26-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4b26-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4b26-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4b26-107">說明</span><span class="sxs-lookup"><span data-stu-id="e4b26-107">DESCRIPTION</span></span>
<span data-ttu-id="e4b26-108">**AzNetworkInterfaceIpConfig** Cmdlet 會更新網路介面的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="e4b26-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="e4b26-109">示例</span><span class="sxs-lookup"><span data-stu-id="e4b26-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b26-110">1：變更 IP 配置的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="e4b26-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="e4b26-111">前兩個命令會取得名為 myvnet 的虛擬網路，以及稱為 mysubnet 的子網，並將它儲存在 $vnet 與 $subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e4b26-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="e4b26-112">第三個命令會取得與需要更新之 IP 配置相關聯的網路介面 nic1。</span><span class="sxs-lookup"><span data-stu-id="e4b26-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="e4b26-113">第三個命令會將主要 IP 配置 ipconfig1 的私人 IP 位址設定為10.0.0.11。</span><span class="sxs-lookup"><span data-stu-id="e4b26-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="e4b26-114">最後，最後一個命令會更新網路介面，以確保已成功進行變更。</span><span class="sxs-lookup"><span data-stu-id="e4b26-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="e4b26-115">2：將 IP 設定與應用程式安全性群組建立關聯</span><span class="sxs-lookup"><span data-stu-id="e4b26-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="e4b26-116">在這個範例中，變數 $asg 包含對應用程式安全性群組的參照。</span><span class="sxs-lookup"><span data-stu-id="e4b26-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="e4b26-117">第四個命令會取得與需要更新之 IP 配置相關聯的網路介面 nic1。</span><span class="sxs-lookup"><span data-stu-id="e4b26-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="e4b26-118">Set-AzNetworkInterfaceIpConfig 將主要 IP 配置 ipconfig1 的私人 IP 位址設定為10.0.0.11，並建立與已檢索的應用程式安全性群組的關聯。</span><span class="sxs-lookup"><span data-stu-id="e4b26-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="e4b26-119">最後，最後一個命令會更新網路介面，以確保已成功進行變更。</span><span class="sxs-lookup"><span data-stu-id="e4b26-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="e4b26-120">參數</span><span class="sxs-lookup"><span data-stu-id="e4b26-120">PARAMETERS</span></span>

### <span data-ttu-id="e4b26-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4b26-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="e4b26-122">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e4b26-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="e4b26-124">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4b26-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="e4b26-126">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e4b26-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="e4b26-128">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b26-129">-DefaultProfile</span></span>
<span data-ttu-id="e4b26-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4b26-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4b26-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4b26-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="e4b26-132">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e4b26-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="e4b26-134">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e4b26-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="e4b26-136">指定一個負載平衡器入站網路位址的集合， (NAT) 規則參照，此網路介面 IP 設定屬於這個配置。</span><span class="sxs-lookup"><span data-stu-id="e4b26-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="e4b26-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="e4b26-138">指定此網路介面 IP 配置所屬的負載等化器入站 NAT 規則參照集合。</span><span class="sxs-lookup"><span data-stu-id="e4b26-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e4b26-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4b26-139">-Name</span></span>
<span data-ttu-id="e4b26-140">指定此 Cmdlet 設定的網路 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="e4b26-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="e4b26-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e4b26-141">-NetworkInterface</span></span>
<span data-ttu-id="e4b26-142">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="e4b26-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="e4b26-143">這個 Cmdlet 會將網路介面 IP 設定新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="e4b26-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4b26-144">-主要</span><span class="sxs-lookup"><span data-stu-id="e4b26-144">-Primary</span></span>
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

### <span data-ttu-id="e4b26-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e4b26-145">-PrivateIpAddress</span></span>
<span data-ttu-id="e4b26-146">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e4b26-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="e4b26-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e4b26-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="e4b26-148">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="e4b26-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="e4b26-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e4b26-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4b26-150">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="e4b26-150">IPv4</span></span>
- <span data-ttu-id="e4b26-151">Ipv4</span><span class="sxs-lookup"><span data-stu-id="e4b26-151">IPv6</span></span>

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

### <span data-ttu-id="e4b26-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e4b26-152">-PublicIpAddress</span></span>
<span data-ttu-id="e4b26-153">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="e4b26-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="e4b26-154">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="e4b26-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="e4b26-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e4b26-155">-PublicIpAddressId</span></span>
<span data-ttu-id="e4b26-156">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="e4b26-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="e4b26-157">-子網</span><span class="sxs-lookup"><span data-stu-id="e4b26-157">-Subnet</span></span>
<span data-ttu-id="e4b26-158">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="e4b26-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="e4b26-159">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e4b26-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="e4b26-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e4b26-160">-SubnetId</span></span>
<span data-ttu-id="e4b26-161">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e4b26-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="e4b26-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b26-162">CommonParameters</span></span>
<span data-ttu-id="e4b26-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4b26-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b26-164">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4b26-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b26-165">輸入</span><span class="sxs-lookup"><span data-stu-id="e4b26-165">INPUTS</span></span>

### <span data-ttu-id="e4b26-166">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4b26-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="e4b26-167">System.object []</span><span class="sxs-lookup"><span data-stu-id="e4b26-167">System.String[]</span></span>

### <span data-ttu-id="e4b26-168">PSBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="e4b26-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="e4b26-169">PSInboundNatRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="e4b26-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="e4b26-170">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="e4b26-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="e4b26-171">PSApplicationSecurityGroup [] （[]）</span><span class="sxs-lookup"><span data-stu-id="e4b26-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="e4b26-172">輸出</span><span class="sxs-lookup"><span data-stu-id="e4b26-172">OUTPUTS</span></span>

### <span data-ttu-id="e4b26-173">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4b26-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e4b26-174">筆記</span><span class="sxs-lookup"><span data-stu-id="e4b26-174">NOTES</span></span>
* <span data-ttu-id="e4b26-175">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="e4b26-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e4b26-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4b26-176">RELATED LINKS</span></span>

[<span data-ttu-id="e4b26-177">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4b26-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e4b26-178">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4b26-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e4b26-179">新-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4b26-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e4b26-180">移除-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4b26-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
