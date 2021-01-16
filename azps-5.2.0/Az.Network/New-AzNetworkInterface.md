---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278660"
---
# <span data-ttu-id="cb9d1-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cb9d1-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="cb9d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9d1-103">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-103">Creates a network interface.</span></span>

## <span data-ttu-id="cb9d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb9d1-104">SYNTAX</span></span>

### <span data-ttu-id="cb9d1-105">SetByIpConfigurationResource (預設) </span><span class="sxs-lookup"><span data-stu-id="cb9d1-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb9d1-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb9d1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb9d1-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cb9d1-108">SetByResource</span></span>
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

## <span data-ttu-id="cb9d1-109">說明</span><span class="sxs-lookup"><span data-stu-id="cb9d1-109">DESCRIPTION</span></span>
<span data-ttu-id="cb9d1-110">**新的-AzNetworkInterface** Cmdlet 會建立 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="cb9d1-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb9d1-111">EXAMPLES</span></span>

### <span data-ttu-id="cb9d1-112">範例1：建立 Azure network 介面</span><span class="sxs-lookup"><span data-stu-id="cb9d1-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="cb9d1-113">這個命令會建立一個名為 NetworkInterface001 的網路介面，在名為 VirtualNetwork1 的虛擬網路中，從 Subnet1 動態指派私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="cb9d1-114">命令也會將兩個 DNS 伺服器指派給網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="cb9d1-115">將會使用 name IPConfiguration1 自動建立 IPConfiguration 子資源。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="cb9d1-116">範例2：使用 IP 設定物件建立 Azure 網路介面</span><span class="sxs-lookup"><span data-stu-id="cb9d1-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="cb9d1-117">這個範例會使用 IP 設定物件來建立新的網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="cb9d1-118">[IP 設定] 物件會指定靜態的專用 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="cb9d1-119">第一個命令會在第二個命令中檢索用來指派子網的現有指定虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="cb9d1-120">第二個命令會建立名為 IPConfig1 的網路介面 IP 配置，並將設定儲存在名為 $IPconfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="cb9d1-121">第三個命令會建立一個名為 NetworkInterface1 的網路介面，該介面使用在名為 $IPconfig 的變數中儲存的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="cb9d1-122">範例3</span><span class="sxs-lookup"><span data-stu-id="cb9d1-122">Example 3</span></span>

<span data-ttu-id="cb9d1-123">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-123">Creates a network interface.</span></span> <span data-ttu-id="cb9d1-124"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="cb9d1-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="cb9d1-125">參數</span><span class="sxs-lookup"><span data-stu-id="cb9d1-125">PARAMETERS</span></span>

### <span data-ttu-id="cb9d1-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb9d1-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="cb9d1-127">指定 **ApplicationGatewayBackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cb9d1-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="cb9d1-129">指定 **ApplicationGatewayBackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cb9d1-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb9d1-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="cb9d1-131">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="cb9d1-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="cb9d1-133">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="cb9d1-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb9d1-134">-AsJob</span></span>
<span data-ttu-id="cb9d1-135">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb9d1-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb9d1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9d1-136">-DefaultProfile</span></span>
<span data-ttu-id="cb9d1-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9d1-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="cb9d1-138">-DnsServer</span></span>
<span data-ttu-id="cb9d1-139">指定網路介面的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="cb9d1-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="cb9d1-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="cb9d1-141">啟用快速網路。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="cb9d1-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="cb9d1-142">-EnableIPForwarding</span></span>
<span data-ttu-id="cb9d1-143">表示此 Cmdlet 為網路介面啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="cb9d1-144">IP 轉寄可讓虛擬機器接收傳送到其他目的地的流量。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="cb9d1-145">-Force</span><span class="sxs-lookup"><span data-stu-id="cb9d1-145">-Force</span></span>
<span data-ttu-id="cb9d1-146">即使已存在相同名稱的網路介面，也會強制建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="cb9d1-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="cb9d1-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="cb9d1-148">指定新網路介面的內部 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="cb9d1-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb9d1-149">-IpConfiguration</span></span>
<span data-ttu-id="cb9d1-150">指定此 Cmdlet 針對網路介面使用的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="cb9d1-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cb9d1-151">-IpConfigurationName</span></span>
<span data-ttu-id="cb9d1-152">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="cb9d1-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb9d1-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="cb9d1-154">指定 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cb9d1-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="cb9d1-156">指定 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cb9d1-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="cb9d1-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="cb9d1-158">指定負載平衡器的輸入 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="cb9d1-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="cb9d1-160">指定負載平衡器的輸入 NAT 規則配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="cb9d1-161">-位置</span><span class="sxs-lookup"><span data-stu-id="cb9d1-161">-Location</span></span>
<span data-ttu-id="cb9d1-162">指定網路介面的區域。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="cb9d1-163">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb9d1-163">-Name</span></span>
<span data-ttu-id="cb9d1-164">指定要建立之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="cb9d1-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb9d1-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cb9d1-166">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="cb9d1-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="cb9d1-168">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="cb9d1-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="cb9d1-169">-PrivateIpAddress</span></span>
<span data-ttu-id="cb9d1-170">指定要指派給此網路介面的靜態 IPv4 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="cb9d1-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cb9d1-171">-PublicIpAddress</span></span>
<span data-ttu-id="cb9d1-172">指定要指派給網路介面的 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="cb9d1-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-173">-PublicIpAddressId</span></span>
<span data-ttu-id="cb9d1-174">指定要指派給網路介面之 **PublicIPAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="cb9d1-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9d1-175">-ResourceGroupName</span></span>
<span data-ttu-id="cb9d1-176">指定網路介面所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="cb9d1-177">-子網</span><span class="sxs-lookup"><span data-stu-id="cb9d1-177">-Subnet</span></span>
<span data-ttu-id="cb9d1-178">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="cb9d1-179">這個 Cmdlet 會為此參數指定的子網建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb9d1-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cb9d1-180">-SubnetId</span></span>
<span data-ttu-id="cb9d1-181">指定要為其建立網路介面的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="cb9d1-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb9d1-182">-Tag</span></span>
<span data-ttu-id="cb9d1-183">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cb9d1-184">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cb9d1-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cb9d1-185">-確認</span><span class="sxs-lookup"><span data-stu-id="cb9d1-185">-Confirm</span></span>
<span data-ttu-id="cb9d1-186">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9d1-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9d1-187">-WhatIf</span></span>
<span data-ttu-id="cb9d1-188">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9d1-189">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9d1-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9d1-190">CommonParameters</span></span>
<span data-ttu-id="cb9d1-191">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9d1-192">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb9d1-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9d1-193">輸入</span><span class="sxs-lookup"><span data-stu-id="cb9d1-193">INPUTS</span></span>

### <span data-ttu-id="cb9d1-194">System.object</span><span class="sxs-lookup"><span data-stu-id="cb9d1-194">System.String</span></span>

### <span data-ttu-id="cb9d1-195">PSNetworkInterfaceIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="cb9d1-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="cb9d1-196">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb9d1-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="cb9d1-197">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb9d1-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="cb9d1-198">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb9d1-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="cb9d1-199">System.object []</span><span class="sxs-lookup"><span data-stu-id="cb9d1-199">System.String[]</span></span>

### <span data-ttu-id="cb9d1-200">PSBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="cb9d1-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="cb9d1-201">PSInboundNatRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="cb9d1-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="cb9d1-202">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="cb9d1-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="cb9d1-203">PSApplicationSecurityGroup [] （[]）</span><span class="sxs-lookup"><span data-stu-id="cb9d1-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="cb9d1-204">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cb9d1-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cb9d1-205">輸出</span><span class="sxs-lookup"><span data-stu-id="cb9d1-205">OUTPUTS</span></span>

### <span data-ttu-id="cb9d1-206">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb9d1-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cb9d1-207">筆記</span><span class="sxs-lookup"><span data-stu-id="cb9d1-207">NOTES</span></span>

## <span data-ttu-id="cb9d1-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb9d1-208">RELATED LINKS</span></span>

[<span data-ttu-id="cb9d1-209">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cb9d1-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="cb9d1-210">移除-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cb9d1-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="cb9d1-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cb9d1-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
