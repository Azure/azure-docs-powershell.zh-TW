---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958078"
---
# <span data-ttu-id="7de28-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7de28-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="7de28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7de28-102">SYNOPSIS</span></span>
<span data-ttu-id="7de28-103">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="7de28-103">Creates a network interface.</span></span>

## <span data-ttu-id="7de28-104">句法</span><span class="sxs-lookup"><span data-stu-id="7de28-104">SYNTAX</span></span>

### <span data-ttu-id="7de28-105">SetByIpConfigurationResource (預設) </span><span class="sxs-lookup"><span data-stu-id="7de28-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de28-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="7de28-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de28-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7de28-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de28-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7de28-108">SetByResource</span></span>
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

## <span data-ttu-id="7de28-109">說明</span><span class="sxs-lookup"><span data-stu-id="7de28-109">DESCRIPTION</span></span>
<span data-ttu-id="7de28-110">**新的-AzNetworkInterface** Cmdlet 會建立 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="7de28-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="7de28-111">示例</span><span class="sxs-lookup"><span data-stu-id="7de28-111">EXAMPLES</span></span>

### <span data-ttu-id="7de28-112">範例1：建立 Azure network 介面</span><span class="sxs-lookup"><span data-stu-id="7de28-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="7de28-113">這個命令會建立一個名為 NetworkInterface001 的網路介面，在名為 VirtualNetwork1 的虛擬網路中，從 Subnet1 動態指派私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7de28-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="7de28-114">命令也會將兩個 DNS 伺服器指派給網路介面。</span><span class="sxs-lookup"><span data-stu-id="7de28-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="7de28-115">將會使用 name IPConfiguration1 自動建立 IPConfiguration 子資源。</span><span class="sxs-lookup"><span data-stu-id="7de28-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="7de28-116">範例2：使用 IP 設定物件建立 Azure 網路介面</span><span class="sxs-lookup"><span data-stu-id="7de28-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="7de28-117">這個範例會使用 IP 設定物件來建立新的網路介面。</span><span class="sxs-lookup"><span data-stu-id="7de28-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="7de28-118">[IP 設定] 物件會指定靜態的專用 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="7de28-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="7de28-119">第一個命令會在第二個命令中檢索用來指派子網的現有指定虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="7de28-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="7de28-120">第二個命令會建立名為 IPConfig1 的網路介面 IP 配置，並將設定儲存在名為 $IPconfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7de28-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="7de28-121">第三個命令會建立一個名為 NetworkInterface1 的網路介面，該介面使用在名為 $IPconfig 的變數中儲存的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7de28-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="7de28-122">參數</span><span class="sxs-lookup"><span data-stu-id="7de28-122">PARAMETERS</span></span>

### <span data-ttu-id="7de28-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7de28-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7de28-124">指定 **ApplicationGatewayBackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de28-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7de28-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7de28-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7de28-126">指定 **ApplicationGatewayBackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de28-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7de28-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7de28-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7de28-128">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="7de28-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="7de28-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7de28-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7de28-130">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="7de28-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="7de28-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7de28-131">-AsJob</span></span>
<span data-ttu-id="7de28-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7de28-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7de28-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de28-133">-DefaultProfile</span></span>
<span data-ttu-id="7de28-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7de28-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de28-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="7de28-135">-DnsServer</span></span>
<span data-ttu-id="7de28-136">指定網路介面的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7de28-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="7de28-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="7de28-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="7de28-138">啟用快速網路。</span><span class="sxs-lookup"><span data-stu-id="7de28-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="7de28-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="7de28-139">-EnableIPForwarding</span></span>
<span data-ttu-id="7de28-140">表示此 Cmdlet 為網路介面啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="7de28-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="7de28-141">IP 轉寄可讓虛擬機器接收傳送到其他目的地的流量。</span><span class="sxs-lookup"><span data-stu-id="7de28-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="7de28-142">-Force</span><span class="sxs-lookup"><span data-stu-id="7de28-142">-Force</span></span>
<span data-ttu-id="7de28-143">即使已存在相同名稱的網路介面，也會強制建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="7de28-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="7de28-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="7de28-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="7de28-145">指定新網路介面的內部 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="7de28-145">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="7de28-146">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7de28-146">-IpConfiguration</span></span>
<span data-ttu-id="7de28-147">指定此 Cmdlet 針對網路介面使用的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7de28-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="7de28-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7de28-148">-IpConfigurationName</span></span>
<span data-ttu-id="7de28-149">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7de28-149">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="7de28-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7de28-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7de28-151">指定 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de28-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7de28-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7de28-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7de28-153">指定 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de28-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7de28-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7de28-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7de28-155">指定負載平衡器的輸入 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="7de28-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="7de28-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7de28-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7de28-157">指定負載平衡器的輸入 NAT 規則配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de28-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="7de28-158">-位置</span><span class="sxs-lookup"><span data-stu-id="7de28-158">-Location</span></span>
<span data-ttu-id="7de28-159">指定網路介面的區域。</span><span class="sxs-lookup"><span data-stu-id="7de28-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="7de28-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="7de28-160">-Name</span></span>
<span data-ttu-id="7de28-161">指定要建立之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="7de28-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="7de28-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7de28-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7de28-163">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de28-163">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="7de28-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7de28-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7de28-165">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="7de28-165">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="7de28-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7de28-166">-PrivateIpAddress</span></span>
<span data-ttu-id="7de28-167">指定要指派給此網路介面的靜態 IPv4 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7de28-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="7de28-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7de28-168">-PublicIpAddress</span></span>
<span data-ttu-id="7de28-169">指定要指派給網路介面的 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de28-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="7de28-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7de28-170">-PublicIpAddressId</span></span>
<span data-ttu-id="7de28-171">指定要指派給網路介面之 **PublicIPAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de28-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="7de28-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de28-172">-ResourceGroupName</span></span>
<span data-ttu-id="7de28-173">指定網路介面所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7de28-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="7de28-174">-子網</span><span class="sxs-lookup"><span data-stu-id="7de28-174">-Subnet</span></span>
<span data-ttu-id="7de28-175">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de28-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7de28-176">這個 Cmdlet 會為此參數指定的子網建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="7de28-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="7de28-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7de28-177">-SubnetId</span></span>
<span data-ttu-id="7de28-178">指定要為其建立網路介面的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de28-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="7de28-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="7de28-179">-Tag</span></span>
<span data-ttu-id="7de28-180">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7de28-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7de28-181">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7de28-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7de28-182">-確認</span><span class="sxs-lookup"><span data-stu-id="7de28-182">-Confirm</span></span>
<span data-ttu-id="7de28-183">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7de28-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de28-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de28-184">-WhatIf</span></span>
<span data-ttu-id="7de28-185">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7de28-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de28-186">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7de28-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de28-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de28-187">CommonParameters</span></span>
<span data-ttu-id="7de28-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7de28-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de28-189">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7de28-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de28-190">輸入</span><span class="sxs-lookup"><span data-stu-id="7de28-190">INPUTS</span></span>

### <span data-ttu-id="7de28-191">System.object</span><span class="sxs-lookup"><span data-stu-id="7de28-191">System.String</span></span>

### <span data-ttu-id="7de28-192">PSNetworkInterfaceIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7de28-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="7de28-193">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7de28-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7de28-194">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7de28-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="7de28-195">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7de28-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="7de28-196">System.object []</span><span class="sxs-lookup"><span data-stu-id="7de28-196">System.String[]</span></span>

### <span data-ttu-id="7de28-197">PSBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7de28-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="7de28-198">PSInboundNatRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7de28-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="7de28-199">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7de28-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="7de28-200">PSApplicationSecurityGroup [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7de28-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="7de28-201">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7de28-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7de28-202">輸出</span><span class="sxs-lookup"><span data-stu-id="7de28-202">OUTPUTS</span></span>

### <span data-ttu-id="7de28-203">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7de28-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7de28-204">筆記</span><span class="sxs-lookup"><span data-stu-id="7de28-204">NOTES</span></span>

## <span data-ttu-id="7de28-205">相關連結</span><span class="sxs-lookup"><span data-stu-id="7de28-205">RELATED LINKS</span></span>

[<span data-ttu-id="7de28-206">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7de28-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7de28-207">移除-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7de28-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="7de28-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7de28-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
