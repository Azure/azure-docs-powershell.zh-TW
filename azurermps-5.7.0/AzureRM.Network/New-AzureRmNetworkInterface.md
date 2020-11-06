---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 111723b2f0271583d43bd1c845eebe9800190a59
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457680"
---
# <span data-ttu-id="c2809-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2809-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="c2809-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2809-102">SYNOPSIS</span></span>
<span data-ttu-id="c2809-103">建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="c2809-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2809-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2809-104">SYNTAX</span></span>

### <span data-ttu-id="c2809-105">SetByIpConfigurationResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c2809-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2809-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="c2809-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2809-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2809-107">SetByResourceId</span></span>
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

### <span data-ttu-id="c2809-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c2809-108">SetByResource</span></span>
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

## <span data-ttu-id="c2809-109">說明</span><span class="sxs-lookup"><span data-stu-id="c2809-109">DESCRIPTION</span></span>
<span data-ttu-id="c2809-110">**新的-AzureRmNetworkInterface** Cmdlet 會建立 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="c2809-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="c2809-111">示例</span><span class="sxs-lookup"><span data-stu-id="c2809-111">EXAMPLES</span></span>

### <span data-ttu-id="c2809-112">範例1：建立 Azure network 介面</span><span class="sxs-lookup"><span data-stu-id="c2809-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="c2809-113">這個命令會建立一個名為 NetworkInterface001 的網路介面，在名為 VirtualNetwork1 的虛擬網路中，從 Subnet1 動態指派私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c2809-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="c2809-114">命令也會將兩個 DNS 伺服器指派給網路介面。</span><span class="sxs-lookup"><span data-stu-id="c2809-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="c2809-115">將會使用 name IPConfiguration1 自動建立 IPConfiguration 子資源。</span><span class="sxs-lookup"><span data-stu-id="c2809-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="c2809-116">範例2：使用 IP 設定物件建立 Azure 網路介面</span><span class="sxs-lookup"><span data-stu-id="c2809-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="c2809-117">這個範例會使用 IP 設定物件來建立新的網路介面。</span><span class="sxs-lookup"><span data-stu-id="c2809-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="c2809-118">[IP 設定] 物件會指定靜態的專用 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="c2809-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="c2809-119">第一個命令會建立名為 IPConfig1 的網路介面 IP 配置，並將設定儲存在名為 $IPconfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="c2809-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="c2809-120">第二個命令會建立一個名為 NetworkInterface1 的網路介面，該介面使用在名為 $IPconfig 的變數中儲存的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="c2809-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="c2809-121">參數</span><span class="sxs-lookup"><span data-stu-id="c2809-121">PARAMETERS</span></span>

### <span data-ttu-id="c2809-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2809-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="c2809-123">指定 **ApplicationGatewayBackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="c2809-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="c2809-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c2809-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="c2809-125">指定 **ApplicationGatewayBackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2809-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="c2809-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2809-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="c2809-127">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="c2809-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="c2809-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c2809-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="c2809-129">指定網路介面 IP 設定應該屬於的應用程式安全性群組參考集合。</span><span class="sxs-lookup"><span data-stu-id="c2809-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="c2809-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2809-130">-AsJob</span></span>
<span data-ttu-id="c2809-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2809-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2809-132">-DefaultProfile</span></span>
<span data-ttu-id="c2809-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2809-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="c2809-134">-DnsServer</span></span>
<span data-ttu-id="c2809-135">指定網路介面的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2809-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="c2809-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="c2809-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="c2809-137">啟用快速網路。</span><span class="sxs-lookup"><span data-stu-id="c2809-137">Enables accelerated networking.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="c2809-138">-EnableIPForwarding</span></span>
<span data-ttu-id="c2809-139">表示此 Cmdlet 為網路介面啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="c2809-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="c2809-140">IP 轉寄可讓虛擬機器接收傳送到其他目的地的流量。</span><span class="sxs-lookup"><span data-stu-id="c2809-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-141">-Force</span><span class="sxs-lookup"><span data-stu-id="c2809-141">-Force</span></span>
<span data-ttu-id="c2809-142">即使已存在相同名稱的網路介面，也會強制建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="c2809-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="c2809-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="c2809-144">指定新網路介面的內部 DNS 名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="c2809-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2809-145">-IpConfiguration</span></span>
<span data-ttu-id="c2809-146">指定此 Cmdlet 針對網路介面使用的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="c2809-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="c2809-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c2809-147">-IpConfigurationName</span></span>
<span data-ttu-id="c2809-148">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2809-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2809-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="c2809-150">指定 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="c2809-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="c2809-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c2809-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="c2809-152">指定 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2809-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="c2809-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="c2809-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="c2809-154">指定負載平衡器的輸入 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="c2809-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="c2809-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="c2809-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="c2809-156">指定負載平衡器的輸入 NAT 規則配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2809-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="c2809-157">-位置</span><span class="sxs-lookup"><span data-stu-id="c2809-157">-Location</span></span>
<span data-ttu-id="c2809-158">指定網路介面的區域。</span><span class="sxs-lookup"><span data-stu-id="c2809-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2809-159">-Name</span></span>
<span data-ttu-id="c2809-160">指定要建立之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2809-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2809-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c2809-162">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="c2809-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c2809-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="c2809-164">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="c2809-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2809-165">-PrivateIpAddress</span></span>
<span data-ttu-id="c2809-166">指定要指派給此網路介面的靜態 IPv4 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c2809-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2809-167">-PublicIpAddress</span></span>
<span data-ttu-id="c2809-168">指定要指派給網路介面的 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="c2809-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c2809-169">-PublicIpAddressId</span></span>
<span data-ttu-id="c2809-170">指定要指派給網路介面之 **PublicIPAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2809-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2809-171">-ResourceGroupName</span></span>
<span data-ttu-id="c2809-172">指定網路介面所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2809-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-173">-子網</span><span class="sxs-lookup"><span data-stu-id="c2809-173">-Subnet</span></span>
<span data-ttu-id="c2809-174">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="c2809-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="c2809-175">這個 Cmdlet 會為此參數指定的子網建立網路介面。</span><span class="sxs-lookup"><span data-stu-id="c2809-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c2809-176">-SubnetId</span></span>
<span data-ttu-id="c2809-177">指定要為其建立網路介面的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2809-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2809-178">-Tag</span></span>
<span data-ttu-id="c2809-179">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c2809-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c2809-180">例如：</span><span class="sxs-lookup"><span data-stu-id="c2809-180">For example:</span></span>

<span data-ttu-id="c2809-181">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c2809-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-182">-確認</span><span class="sxs-lookup"><span data-stu-id="c2809-182">-Confirm</span></span>
<span data-ttu-id="c2809-183">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2809-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2809-184">-WhatIf</span></span>
<span data-ttu-id="c2809-185">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2809-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2809-186">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2809-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2809-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2809-187">CommonParameters</span></span>
<span data-ttu-id="c2809-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2809-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2809-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2809-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2809-190">輸入</span><span class="sxs-lookup"><span data-stu-id="c2809-190">INPUTS</span></span>

### <span data-ttu-id="c2809-191">所有</span><span class="sxs-lookup"><span data-stu-id="c2809-191">None</span></span>
<span data-ttu-id="c2809-192">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c2809-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2809-193">輸出</span><span class="sxs-lookup"><span data-stu-id="c2809-193">OUTPUTS</span></span>

### <span data-ttu-id="c2809-194">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2809-194">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c2809-195">筆記</span><span class="sxs-lookup"><span data-stu-id="c2809-195">NOTES</span></span>

## <span data-ttu-id="c2809-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2809-196">RELATED LINKS</span></span>

[<span data-ttu-id="c2809-197">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2809-197">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="c2809-198">移除-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2809-198">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="c2809-199">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2809-199">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
