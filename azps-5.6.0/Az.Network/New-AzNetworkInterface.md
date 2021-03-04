---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 994c0e85745e08d4a01e7b5a20b90a25513a983f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910030"
---
# <span data-ttu-id="405af-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="405af-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="405af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="405af-102">SYNOPSIS</span></span>
<span data-ttu-id="405af-103">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="405af-103">Creates a network interface.</span></span>

## <span data-ttu-id="405af-104">語法</span><span class="sxs-lookup"><span data-stu-id="405af-104">SYNTAX</span></span>

### <span data-ttu-id="405af-105">SetByIpConfigurationResource (預設) </span><span class="sxs-lookup"><span data-stu-id="405af-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405af-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="405af-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405af-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="405af-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405af-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="405af-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="405af-109">描述</span><span class="sxs-lookup"><span data-stu-id="405af-109">DESCRIPTION</span></span>
<span data-ttu-id="405af-110">**New-AzNetworkInterface** Cmdlet 會建立 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="405af-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="405af-111">例子</span><span class="sxs-lookup"><span data-stu-id="405af-111">EXAMPLES</span></span>

### <span data-ttu-id="405af-112">範例 1：建立 Azure 網路介面</span><span class="sxs-lookup"><span data-stu-id="405af-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="405af-113">此命令會建立名為 NetworkInterface001 的網路介面，其虛擬網路中名為 VirtualNetwork1 的子網 1 動態指派私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="405af-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="405af-114">該命令也會將兩個 DNS 伺服器指派給網路介面。</span><span class="sxs-lookup"><span data-stu-id="405af-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="405af-115">IPConfiguration 子資源會自動使用名稱 IPConfiguration1 建立。</span><span class="sxs-lookup"><span data-stu-id="405af-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="405af-116">範例 2：使用 IP 組組物件建立 Azure 網路介面</span><span class="sxs-lookup"><span data-stu-id="405af-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="405af-117">此範例會使用 IP 組設定物件建立新網路介面。</span><span class="sxs-lookup"><span data-stu-id="405af-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="405af-118">IP 群組原則物件會指定靜態私人 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="405af-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="405af-119">第一個命令會取回現有的指定虛擬網路，用來指派第二個命令中的子網。</span><span class="sxs-lookup"><span data-stu-id="405af-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="405af-120">第二個命令會建立名為 IPConfig1 的網路介面 IP 組$IPconfig。</span><span class="sxs-lookup"><span data-stu-id="405af-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="405af-121">第三個命令會建立名為 NetworkInterface1 的網路介面，該網路介面會使用儲存在名為 networkInterface 的變數中的網路介面 IP $IPconfig。</span><span class="sxs-lookup"><span data-stu-id="405af-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="405af-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="405af-122">Example 3</span></span>

<span data-ttu-id="405af-123">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="405af-123">Creates a network interface.</span></span> <span data-ttu-id="405af-124"> (自動) </span><span class="sxs-lookup"><span data-stu-id="405af-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="405af-125">參數</span><span class="sxs-lookup"><span data-stu-id="405af-125">PARAMETERS</span></span>

### <span data-ttu-id="405af-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="405af-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="405af-127">指定 **ApplicationGatewayBackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="405af-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="405af-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="405af-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="405af-129">指定 **ApplicationGatewayBackendAddressPool 物件的識別碼** 。</span><span class="sxs-lookup"><span data-stu-id="405af-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="405af-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="405af-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="405af-131">指定網路介面 IP 組配置應所屬的應用程式安全性群組參照集合。</span><span class="sxs-lookup"><span data-stu-id="405af-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="405af-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="405af-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="405af-133">指定網路介面 IP 組配置應所屬的應用程式安全性群組參照集合。</span><span class="sxs-lookup"><span data-stu-id="405af-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="405af-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="405af-134">-AsJob</span></span>
<span data-ttu-id="405af-135">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="405af-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="405af-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405af-136">-DefaultProfile</span></span>
<span data-ttu-id="405af-137">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="405af-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="405af-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="405af-138">-DnsServer</span></span>
<span data-ttu-id="405af-139">指定網路介面的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="405af-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="405af-140">-EnableAcceworkNetworking</span><span class="sxs-lookup"><span data-stu-id="405af-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="405af-141">啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="405af-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="405af-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="405af-142">-EnableIPForwarding</span></span>
<span data-ttu-id="405af-143">表示此 Cmdlet 啟用網路介面的 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="405af-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="405af-144">IP 轉轉可讓虛擬機器接收目的地為其他目的地的流量。</span><span class="sxs-lookup"><span data-stu-id="405af-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="405af-145">-強制</span><span class="sxs-lookup"><span data-stu-id="405af-145">-Force</span></span>
<span data-ttu-id="405af-146">強制建立網路介面，即使已存在相同名稱的網路介面也一樣。</span><span class="sxs-lookup"><span data-stu-id="405af-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="405af-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="405af-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="405af-148">指定新網路介面的內部 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="405af-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="405af-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="405af-149">-IpConfiguration</span></span>
<span data-ttu-id="405af-150">指定此 Cmdlet 用於網路介面的 IP 群組原則。</span><span class="sxs-lookup"><span data-stu-id="405af-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="405af-151">-IpConfigurationName</span></span>
<span data-ttu-id="405af-152">指定 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="405af-152">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="405af-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="405af-154">指定 **一個後端AddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="405af-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="405af-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="405af-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="405af-156">指定 **後端AddressPool 物件的識別碼** 。</span><span class="sxs-lookup"><span data-stu-id="405af-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="405af-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="405af-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="405af-158">指定負載平衡器中的內入 NAT 規則組。</span><span class="sxs-lookup"><span data-stu-id="405af-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="405af-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="405af-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="405af-160">指定負載平衡器之內入 NAT 規則配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="405af-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="405af-161">-位置</span><span class="sxs-lookup"><span data-stu-id="405af-161">-Location</span></span>
<span data-ttu-id="405af-162">指定網路介面的區域。</span><span class="sxs-lookup"><span data-stu-id="405af-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="405af-163">-名稱</span><span class="sxs-lookup"><span data-stu-id="405af-163">-Name</span></span>
<span data-ttu-id="405af-164">指定要建立的網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="405af-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="405af-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="405af-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="405af-166">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="405af-166">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="405af-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="405af-168">指定網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="405af-168">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="405af-169">-PrivateIpAddress</span></span>
<span data-ttu-id="405af-170">指定要指派給此網路介面的靜態 IPv4 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="405af-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="405af-171">-PublicIpAddress</span></span>
<span data-ttu-id="405af-172">指定 **要指派給網路介面的 PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="405af-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="405af-173">-PublicIpAddressId</span></span>
<span data-ttu-id="405af-174">指定要指派給 **網路介面的 PublicIPAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="405af-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="405af-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="405af-175">-ResourceGroupName</span></span>
<span data-ttu-id="405af-176">指定網路介面所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="405af-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="405af-177">-子網</span><span class="sxs-lookup"><span data-stu-id="405af-177">-Subnet</span></span>
<span data-ttu-id="405af-178">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="405af-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="405af-179">此 Cmdlet 會為此參數指定的子網建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="405af-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-180">-子網Id</span><span class="sxs-lookup"><span data-stu-id="405af-180">-SubnetId</span></span>
<span data-ttu-id="405af-181">指定要建立網路介面之子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="405af-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405af-182">-標記</span><span class="sxs-lookup"><span data-stu-id="405af-182">-Tag</span></span>
<span data-ttu-id="405af-183">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="405af-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="405af-184">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="405af-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="405af-185">-確認</span><span class="sxs-lookup"><span data-stu-id="405af-185">-Confirm</span></span>
<span data-ttu-id="405af-186">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="405af-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="405af-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="405af-187">-WhatIf</span></span>
<span data-ttu-id="405af-188">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="405af-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="405af-189">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="405af-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="405af-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405af-190">CommonParameters</span></span>
<span data-ttu-id="405af-191">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="405af-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405af-192">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="405af-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405af-193">輸入</span><span class="sxs-lookup"><span data-stu-id="405af-193">INPUTS</span></span>

### <span data-ttu-id="405af-194">System.String</span><span class="sxs-lookup"><span data-stu-id="405af-194">System.String</span></span>

### <span data-ttu-id="405af-195">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="405af-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="405af-196">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="405af-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="405af-197">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="405af-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="405af-198">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="405af-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="405af-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="405af-199">System.String[]</span></span>

### <span data-ttu-id="405af-200">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="405af-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="405af-201">Microsoft.Azure.Commands.Network.models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="405af-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="405af-202">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="405af-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="405af-203">Microsoft.Azure.Commands.Network.models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="405af-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="405af-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="405af-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="405af-205">輸出</span><span class="sxs-lookup"><span data-stu-id="405af-205">OUTPUTS</span></span>

### <span data-ttu-id="405af-206">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="405af-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="405af-207">筆記</span><span class="sxs-lookup"><span data-stu-id="405af-207">NOTES</span></span>

## <span data-ttu-id="405af-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="405af-208">RELATED LINKS</span></span>

[<span data-ttu-id="405af-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="405af-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="405af-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="405af-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="405af-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="405af-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
