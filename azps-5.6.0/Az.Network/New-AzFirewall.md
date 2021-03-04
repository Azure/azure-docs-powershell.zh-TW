---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: e1d1e0668458d35496bf6bc3b0f7883c9f3ed00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907338"
---
# <span data-ttu-id="bcc55-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bcc55-101">New-AzFirewall</span></span>

## <span data-ttu-id="bcc55-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bcc55-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc55-103">在資源群組中建立新防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="bcc55-104">語法</span><span class="sxs-lookup"><span data-stu-id="bcc55-104">SYNTAX</span></span>

### <span data-ttu-id="bcc55-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="bcc55-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcc55-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="bcc55-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcc55-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="bcc55-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcc55-108">描述</span><span class="sxs-lookup"><span data-stu-id="bcc55-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc55-109">**New-AzFirewall** Cmdlet 會建立 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="bcc55-110">例子</span><span class="sxs-lookup"><span data-stu-id="bcc55-110">EXAMPLES</span></span>

### <span data-ttu-id="bcc55-111">範例 1：建立附加至虛擬網路的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="bcc55-112">此範例會在同一個資源群組與防火牆建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bcc55-113">由於未指定規則，防火牆會封鎖所有流量 (行為) 。</span><span class="sxs-lookup"><span data-stu-id="bcc55-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="bcc55-114">Threat Intel 也會以預設模式執行 -警示 ，這表示惡意流量會記錄，但無法拒絕。</span><span class="sxs-lookup"><span data-stu-id="bcc55-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="bcc55-115">範例 2：建立允許所有 HTTPS 流量的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="bcc55-116">此範例會建立允許埠 443 上所有 HTTPS 流量的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="bcc55-117">Threat Intel 會以預設模式執行 - 警示 -這表示惡意流量將會記錄，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="bcc55-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="bcc55-118">範例 3：REDIRECTT - 將流量重新導向至 10.1.2.3：80 至 10.2.3.4：8080</span><span class="sxs-lookup"><span data-stu-id="bcc55-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="bcc55-119">此範例建立了防火牆，將目的地為 10.1.2.3：80 到 10.2.3.4：8080 威脅 Intel 的所有封包目的地 IP 和埠在此範例中關閉。</span><span class="sxs-lookup"><span data-stu-id="bcc55-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="bcc55-120">範例 4：在警示模式中建立沒有規則且使用 Threat Intel 的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="bcc55-121">此範例會建立防火牆，以預設行為 (所有流量) 威脅 Intel 在警示模式中執行。</span><span class="sxs-lookup"><span data-stu-id="bcc55-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="bcc55-122">這表示警示記錄會先針對惡意流量進行排 (，然後再將其他規則 (在此案例中只執行預設規則 - 拒絕所有) </span><span class="sxs-lookup"><span data-stu-id="bcc55-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="bcc55-123">範例 5：建立允許埠 8080 上所有 HTTP 流量的防火牆，但會阻止 Threat Intel 識別的惡意網域</span><span class="sxs-lookup"><span data-stu-id="bcc55-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="bcc55-124">此範例會建立防火牆，允許埠 8080 上的所有 HTTP 流量，除非 Threat Intel 認為該流量為惡意。</span><span class="sxs-lookup"><span data-stu-id="bcc55-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="bcc55-125">在拒絕模式中執行時，與通知不同，Threat Intel 視為惡意的流量不僅會記錄，也會被封鎖。</span><span class="sxs-lookup"><span data-stu-id="bcc55-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="bcc55-126">範例 6：建立沒有規則且具有可用性區的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="bcc55-127">此範例會建立具有所有可用可用區的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="bcc55-128">範例 7：使用兩個或多個公用 IP 位址建立防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="bcc55-129">此範例會建立一個附加至有兩個公用 IP 位址之虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="bcc55-130">範例 8：建立允許 MSSQL 流量到特定 SQL 資料庫的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="bcc55-131">此範例會建立防火牆，允許標準埠 1433 的 MSSQL 流量至 SQL 資料庫sql1.database.windows.net。</span><span class="sxs-lookup"><span data-stu-id="bcc55-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="bcc55-132">範例 9：建立附加至虛擬中樞的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="bcc55-133">此範例會建立附加至虛擬中樞 "vHub" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="bcc55-134">防火牆$fp會附加至防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="bcc55-135">此防火牆會根據防火牆原則中提及的規則來允許/拒絕流量$fp。</span><span class="sxs-lookup"><span data-stu-id="bcc55-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="bcc55-136">虛擬中樞和防火牆應該在同一個區域。</span><span class="sxs-lookup"><span data-stu-id="bcc55-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="bcc55-137">範例 10：使用威脅情報白名單設定建立防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="bcc55-138">此範例會建立防火牆，將威脅情報的「www.microsoft.com」和「8.8.8.8」列入白名單</span><span class="sxs-lookup"><span data-stu-id="bcc55-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="bcc55-139">範例 11：使用自訂私人範圍設定建立防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="bcc55-140">此範例會建立一個防火牆，將 "99.99.99.0/24" 和 "66.66.0.0/16" 視為私人 ip 範圍，不會將流量控制在這些位址</span><span class="sxs-lookup"><span data-stu-id="bcc55-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="bcc55-141">範例 12：使用管理子網和公用 IP 位址建立防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="bcc55-142">此範例會在同一個資源群組與防火牆建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bcc55-143">由於未指定規則，防火牆會封鎖所有流量 (行為) 。</span><span class="sxs-lookup"><span data-stu-id="bcc55-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="bcc55-144">Threat Intel 也會以預設模式執行 -警示 ，這表示惡意流量會記錄，但無法拒絕。</span><span class="sxs-lookup"><span data-stu-id="bcc55-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="bcc55-145">為了支援「強制管理」案例，此防火牆會針對其管理流量使用子網「AzureFirewallManagementSubnet」和管理公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bcc55-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="bcc55-146">範例 13：建立附加至虛擬網路之防火牆策略的防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="bcc55-147">此範例會在同一個資源群組與防火牆建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bcc55-148">將適用于防火牆的規則和威脅情報會從防火牆原則中取用</span><span class="sxs-lookup"><span data-stu-id="bcc55-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="bcc55-149">範例 14：使用 DNS Proxy 和 DNS 伺服器建立防火牆</span><span class="sxs-lookup"><span data-stu-id="bcc55-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="bcc55-150">此範例會在同一個資源群組與防火牆建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bcc55-151">此防火牆已啟用 DNS Proxy，並且提供 2 個 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bcc55-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="bcc55-152">此外，網路規則也需要 DNS Proxy，因此如果有任何具有 FQDN 的網路規則，也會使用 DNS Proxy。</span><span class="sxs-lookup"><span data-stu-id="bcc55-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="bcc55-153">範例 15：建立具有多個 IP 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="bcc55-154">防火牆可以與虛擬中樞相關聯</span><span class="sxs-lookup"><span data-stu-id="bcc55-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="bcc55-155">此範例會建立附加至與防火牆相同的資源群組之虛擬中樞「中樞」的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bcc55-156">防火牆會指派 2 個隱含建立之公用 IP。</span><span class="sxs-lookup"><span data-stu-id="bcc55-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="bcc55-157">16：使用允許使用中 FTP 建立防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="bcc55-158">此範例會建立具有允許使用中 FTP 旗標的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bcc55-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="bcc55-159">參數</span><span class="sxs-lookup"><span data-stu-id="bcc55-159">PARAMETERS</span></span>

### <span data-ttu-id="bcc55-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="bcc55-160">-AllowActiveFTP</span></span>
<span data-ttu-id="bcc55-161">允許防火牆上的使用中 FTP。</span><span class="sxs-lookup"><span data-stu-id="bcc55-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="bcc55-162">根據預設，它會停用。</span><span class="sxs-lookup"><span data-stu-id="bcc55-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="bcc55-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bcc55-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="bcc55-164">指定新防火牆的應用程式規則集合。</span><span class="sxs-lookup"><span data-stu-id="bcc55-164">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc55-165">-AsJob</span></span>
<span data-ttu-id="bcc55-166">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bcc55-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcc55-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc55-167">-DefaultProfile</span></span>
<span data-ttu-id="bcc55-168">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcc55-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcc55-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="bcc55-169">-DnsServer</span></span>
<span data-ttu-id="bcc55-170">DNS 解析所使用的 DNS 伺服器清單，</span><span class="sxs-lookup"><span data-stu-id="bcc55-170">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="bcc55-171">-EnableDnsProxy</span></span>
<span data-ttu-id="bcc55-172">啟用 DNS Proxy。</span><span class="sxs-lookup"><span data-stu-id="bcc55-172">Enable DNS Proxy.</span></span> <span data-ttu-id="bcc55-173">根據預設，它會停用。</span><span class="sxs-lookup"><span data-stu-id="bcc55-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="bcc55-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="bcc55-174">-FirewallPolicyId</span></span>
<span data-ttu-id="bcc55-175">附加至防火牆的防火牆政策</span><span class="sxs-lookup"><span data-stu-id="bcc55-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="bcc55-176">-強制</span><span class="sxs-lookup"><span data-stu-id="bcc55-176">-Force</span></span>
<span data-ttu-id="bcc55-177">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bcc55-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcc55-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="bcc55-178">-HubIPAddress</span></span>
<span data-ttu-id="bcc55-179">附加至虛擬中樞之防火牆的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bcc55-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-180">-位置</span><span class="sxs-lookup"><span data-stu-id="bcc55-180">-Location</span></span>
<span data-ttu-id="bcc55-181">指定防火牆的區域。</span><span class="sxs-lookup"><span data-stu-id="bcc55-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="bcc55-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bcc55-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="bcc55-183">用於管理流量的一或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bcc55-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="bcc55-184">公用 IP 位址必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bcc55-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-185">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcc55-185">-Name</span></span>
<span data-ttu-id="bcc55-186">指定此 Cmdlet 所建立之 Azure 防火牆的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcc55-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bcc55-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bcc55-187">-NatRuleCollection</span></span>
<span data-ttu-id="bcc55-188">AzureFirewallNatRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="bcc55-188">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bcc55-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="bcc55-190">AzureFirewallNetworkRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="bcc55-190">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="bcc55-191">-PrivateRange</span></span>
<span data-ttu-id="bcc55-192">流量不會為 SNAT 的專用 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="bcc55-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bcc55-193">-PublicIpAddress</span></span>
<span data-ttu-id="bcc55-194">一或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bcc55-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="bcc55-195">公用 IP 位址必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bcc55-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="bcc55-196">-PublicIpName</span></span>
<span data-ttu-id="bcc55-197">公用 Ip 名稱。</span><span class="sxs-lookup"><span data-stu-id="bcc55-197">Public Ip Name.</span></span> <span data-ttu-id="bcc55-198">公用 IP 必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bcc55-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc55-199">-ResourceGroupName</span></span>
<span data-ttu-id="bcc55-200">指定要包含防火牆的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bcc55-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="bcc55-201">-SKUName</span><span class="sxs-lookup"><span data-stu-id="bcc55-201">-SkuName</span></span>
<span data-ttu-id="bcc55-202">防火牆的 SKU 名稱</span><span class="sxs-lookup"><span data-stu-id="bcc55-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bcc55-203">-SkuTier</span></span>
<span data-ttu-id="bcc55-204">防火牆的 SKU 層級</span><span class="sxs-lookup"><span data-stu-id="bcc55-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-205">-標記</span><span class="sxs-lookup"><span data-stu-id="bcc55-205">-Tag</span></span>
<span data-ttu-id="bcc55-206">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="bcc55-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bcc55-207">例如：</span><span class="sxs-lookup"><span data-stu-id="bcc55-207">For example:</span></span>

<span data-ttu-id="bcc55-208">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="bcc55-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bcc55-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="bcc55-209">-ThreatIntelMode</span></span>
<span data-ttu-id="bcc55-210">指定威脅情報的作業模式。</span><span class="sxs-lookup"><span data-stu-id="bcc55-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="bcc55-211">預設模式為警示，而非關閉。</span><span class="sxs-lookup"><span data-stu-id="bcc55-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="bcc55-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="bcc55-213">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="bcc55-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="bcc55-214">-VirtualHubId</span></span>
<span data-ttu-id="bcc55-215">附加防火牆的虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="bcc55-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="bcc55-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bcc55-216">-VirtualNetwork</span></span>
<span data-ttu-id="bcc55-217">虛擬網路</span><span class="sxs-lookup"><span data-stu-id="bcc55-217">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bcc55-218">-VirtualNetworkName</span></span>
<span data-ttu-id="bcc55-219">指定要部署防火牆的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="bcc55-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="bcc55-220">虛擬網路和防火牆必須屬於同一個資源群組。</span><span class="sxs-lookup"><span data-stu-id="bcc55-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-221">-區域</span><span class="sxs-lookup"><span data-stu-id="bcc55-221">-Zone</span></span>
<span data-ttu-id="bcc55-222">顯示區域清單，表示防火牆必須來自何處。</span><span class="sxs-lookup"><span data-stu-id="bcc55-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc55-223">-確認</span><span class="sxs-lookup"><span data-stu-id="bcc55-223">-Confirm</span></span>
<span data-ttu-id="bcc55-224">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bcc55-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc55-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc55-225">-WhatIf</span></span>
<span data-ttu-id="bcc55-226">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcc55-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc55-227">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcc55-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc55-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc55-228">CommonParameters</span></span>
<span data-ttu-id="bcc55-229">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bcc55-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc55-230">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcc55-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc55-231">輸入</span><span class="sxs-lookup"><span data-stu-id="bcc55-231">INPUTS</span></span>

### <span data-ttu-id="bcc55-232">System.String</span><span class="sxs-lookup"><span data-stu-id="bcc55-232">System.String</span></span>

### <span data-ttu-id="bcc55-233">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bcc55-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="bcc55-234">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="bcc55-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="bcc55-235">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bcc55-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="bcc55-236">Microsoft.Azure.Commands.Network.models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="bcc55-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="bcc55-237">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="bcc55-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="bcc55-238">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="bcc55-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="bcc55-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bcc55-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bcc55-240">輸出</span><span class="sxs-lookup"><span data-stu-id="bcc55-240">OUTPUTS</span></span>

### <span data-ttu-id="bcc55-241">Microsoft.Azure.Commands.Network.models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bcc55-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bcc55-242">筆記</span><span class="sxs-lookup"><span data-stu-id="bcc55-242">NOTES</span></span>

## <span data-ttu-id="bcc55-243">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcc55-243">RELATED LINKS</span></span>

[<span data-ttu-id="bcc55-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bcc55-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="bcc55-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bcc55-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="bcc55-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bcc55-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="bcc55-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bcc55-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="bcc55-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bcc55-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="bcc55-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bcc55-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
