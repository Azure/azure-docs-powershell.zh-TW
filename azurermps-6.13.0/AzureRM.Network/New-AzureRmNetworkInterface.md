---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 90a3696b4f641f0518d08f821cab813effdbc74a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449028"
---
# <span data-ttu-id="f163a-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f163a-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="f163a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f163a-102">SYNOPSIS</span></span>
<span data-ttu-id="f163a-103">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="f163a-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f163a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f163a-104">SYNTAX</span></span>

### <span data-ttu-id="f163a-105">SetByIpConfigurationResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f163a-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f163a-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f163a-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f163a-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f163a-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f163a-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f163a-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f163a-109">說明</span><span class="sxs-lookup"><span data-stu-id="f163a-109">DESCRIPTION</span></span>
<span data-ttu-id="f163a-110">**新的-AzureRmNetworkInterface** Cmdlet 會建立 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="f163a-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="f163a-111">示例</span><span class="sxs-lookup"><span data-stu-id="f163a-111">EXAMPLES</span></span>

### <span data-ttu-id="f163a-112">範例1：建立 Azure network 介面</span><span class="sxs-lookup"><span data-stu-id="f163a-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="f163a-113">這個命令會建立一個名為 NetworkInterface001 的網路介面，在名為 VirtualNetwork1 的虛擬網路中，從 Subnet1 動態指派私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f163a-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="f163a-114">命令也會將兩個 DNS 伺服器指派給網路介面。</span><span class="sxs-lookup"><span data-stu-id="f163a-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="f163a-115">將會使用 name IPConfiguration1 自動建立 IPConfiguration 子資源。</span><span class="sxs-lookup"><span data-stu-id="f163a-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="f163a-116">範例2：使用 IP 設定物件建立 Azure 網路介面</span><span class="sxs-lookup"><span data-stu-id="f163a-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="f163a-117">這個範例會使用 IP 設定物件來建立新的網路介面。</span><span class="sxs-lookup"><span data-stu-id="f163a-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="f163a-118">[IP 設定] 物件會指定靜態的專用 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="f163a-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="f163a-119">第一個命令會建立名為 IPConfig1 的網路介面 IP 配置，並將設定儲存在名為 $IPconfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f163a-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="f163a-120">第二個命令會建立一個名為 NetworkInterface1 的網路介面，該介面使用在名為 $IPconfig 的變數中儲存的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="f163a-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="f163a-121">參數</span><span class="sxs-lookup"><span data-stu-id="f163a-121">PARAMETERS</span></span>

### <span data-ttu-id="f163a-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f163a-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="f163a-123">指定 **ApplicationGatewayBackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="f163a-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f163a-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f163a-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="f163a-125">指定 **ApplicationGatewayBackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f163a-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f163a-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f163a-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="f163a-127">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="f163a-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="f163a-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f163a-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="f163a-129">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="f163a-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="f163a-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f163a-130">-AsJob</span></span>
<span data-ttu-id="f163a-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f163a-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f163a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f163a-132">-DefaultProfile</span></span>
<span data-ttu-id="f163a-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f163a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f163a-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="f163a-134">-DnsServer</span></span>
<span data-ttu-id="f163a-135">指定網路介面的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f163a-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="f163a-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="f163a-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="f163a-137">啟用快速網路。</span><span class="sxs-lookup"><span data-stu-id="f163a-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="f163a-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f163a-138">-EnableIPForwarding</span></span>
<span data-ttu-id="f163a-139">表示此 Cmdlet 為網路介面啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="f163a-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="f163a-140">IP 轉寄可讓虛擬機器接收傳送到其他目的地的流量。</span><span class="sxs-lookup"><span data-stu-id="f163a-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="f163a-141">-Force</span><span class="sxs-lookup"><span data-stu-id="f163a-141">-Force</span></span>
<span data-ttu-id="f163a-142">即使已存在相同名稱的網路介面，也會強制建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="f163a-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="f163a-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="f163a-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="f163a-144">指定新網路介面的內部 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="f163a-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="f163a-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f163a-145">-IpConfiguration</span></span>
<span data-ttu-id="f163a-146">指定此 Cmdlet 針對網路介面使用的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="f163a-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f163a-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f163a-147">-IpConfigurationName</span></span>
<span data-ttu-id="f163a-148">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f163a-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="f163a-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f163a-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="f163a-150">指定 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="f163a-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f163a-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f163a-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="f163a-152">指定 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f163a-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f163a-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f163a-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="f163a-154">指定負載平衡器的輸入 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="f163a-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="f163a-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="f163a-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="f163a-156">指定負載平衡器的輸入 NAT 規則配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f163a-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="f163a-157">-位置</span><span class="sxs-lookup"><span data-stu-id="f163a-157">-Location</span></span>
<span data-ttu-id="f163a-158">指定網路介面的區域。</span><span class="sxs-lookup"><span data-stu-id="f163a-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="f163a-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="f163a-159">-Name</span></span>
<span data-ttu-id="f163a-160">指定要建立之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="f163a-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="f163a-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f163a-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f163a-162">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="f163a-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="f163a-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f163a-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f163a-164">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="f163a-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="f163a-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f163a-165">-PrivateIpAddress</span></span>
<span data-ttu-id="f163a-166">指定要指派給此網路介面的靜態 IPv4 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f163a-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="f163a-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f163a-167">-PublicIpAddress</span></span>
<span data-ttu-id="f163a-168">指定要指派給網路介面的 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="f163a-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="f163a-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f163a-169">-PublicIpAddressId</span></span>
<span data-ttu-id="f163a-170">指定要指派給網路介面之 **PublicIPAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f163a-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="f163a-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f163a-171">-ResourceGroupName</span></span>
<span data-ttu-id="f163a-172">指定網路介面所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f163a-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="f163a-173">-子網</span><span class="sxs-lookup"><span data-stu-id="f163a-173">-Subnet</span></span>
<span data-ttu-id="f163a-174">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="f163a-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="f163a-175">這個 Cmdlet 會為此參數指定的子網建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="f163a-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="f163a-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f163a-176">-SubnetId</span></span>
<span data-ttu-id="f163a-177">指定要為其建立網路介面的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="f163a-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="f163a-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="f163a-178">-Tag</span></span>
<span data-ttu-id="f163a-179">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f163a-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f163a-180">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f163a-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f163a-181">-確認</span><span class="sxs-lookup"><span data-stu-id="f163a-181">-Confirm</span></span>
<span data-ttu-id="f163a-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f163a-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f163a-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f163a-183">-WhatIf</span></span>
<span data-ttu-id="f163a-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f163a-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f163a-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f163a-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f163a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f163a-186">CommonParameters</span></span>
<span data-ttu-id="f163a-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f163a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f163a-188">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f163a-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f163a-189">輸入</span><span class="sxs-lookup"><span data-stu-id="f163a-189">INPUTS</span></span>

### <span data-ttu-id="f163a-190">System.object</span><span class="sxs-lookup"><span data-stu-id="f163a-190">System.String</span></span>

### <span data-ttu-id="f163a-191">[System.object]. 清單 ' 1 [PSNetworkInterfaceIPConfiguration，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="f163a-191">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f163a-192">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f163a-192">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f163a-193">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f163a-193">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="f163a-194">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f163a-194">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="f163a-195">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f163a-195">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f163a-196">[System.object]. 清單 ' 1 [PSBackendAddressPool，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="f163a-196">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f163a-197">[System.object]. 清單 ' 1 [PSInboundNatRule，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="f163a-197">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f163a-198">[System.object]. 清單 ' 1 [PSApplicationGatewayBackendAddressPool，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="f163a-198">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f163a-199">[System.object]. 清單 ' 1 [PSApplicationSecurityGroup，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="f163a-199">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f163a-200">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f163a-200">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f163a-201">輸出</span><span class="sxs-lookup"><span data-stu-id="f163a-201">OUTPUTS</span></span>

### <span data-ttu-id="f163a-202">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f163a-202">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f163a-203">筆記</span><span class="sxs-lookup"><span data-stu-id="f163a-203">NOTES</span></span>

## <span data-ttu-id="f163a-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="f163a-204">RELATED LINKS</span></span>

[<span data-ttu-id="f163a-205">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f163a-205">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="f163a-206">移除-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f163a-206">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="f163a-207">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f163a-207">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
