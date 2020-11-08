---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136307"
---
# <span data-ttu-id="f4d20-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4d20-101">New-AzFirewall</span></span>

## <span data-ttu-id="f4d20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4d20-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d20-103">在資源群組中建立新的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="f4d20-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4d20-104">SYNTAX</span></span>

### <span data-ttu-id="f4d20-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f4d20-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d20-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="f4d20-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d20-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="f4d20-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d20-108">說明</span><span class="sxs-lookup"><span data-stu-id="f4d20-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d20-109">**新的-AzFirewall** Cmdlet 會建立 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="f4d20-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4d20-110">EXAMPLES</span></span>

### <span data-ttu-id="f4d20-111">範例1：建立附加至虛擬網路的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="f4d20-112">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f4d20-113">因為未指定任何規則，所以防火牆會封鎖所有流量 (預設行為) 。</span><span class="sxs-lookup"><span data-stu-id="f4d20-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="f4d20-114">威脅英特爾也會在預設模式下執行-警示-這表示惡意流量會記錄，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="f4d20-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="f4d20-115">範例2：建立可讓所有 HTTPS 流量使用的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="f4d20-116">這個範例會建立可讓埠443上所有 HTTPS 流量的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="f4d20-117">威脅英特爾將在預設模式下執行-警示-這表示會記錄惡意流量，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="f4d20-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="f4d20-118">範例3： DNAT-重新導向流向10.1.2.3：80至10.2.3.4：8080的流量</span><span class="sxs-lookup"><span data-stu-id="f4d20-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="f4d20-119">這個範例會建立一個已將10.1.2.3：80到10.2.3.4：8080威脅的 [所有資料包] 的目標 IP 和埠，將其轉換為此範例中的 [Intel]。</span><span class="sxs-lookup"><span data-stu-id="f4d20-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="f4d20-120">範例4：建立不含規則的防火牆，並在警示模式中與 Intel 威脅</span><span class="sxs-lookup"><span data-stu-id="f4d20-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="f4d20-121">這個範例會建立一個防火牆，該防火牆會封鎖 (預設行為的所有通訊，) 且在 [警示] 模式中受到 Intel 執行的威脅。</span><span class="sxs-lookup"><span data-stu-id="f4d20-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="f4d20-122">這表示在此情況下，將其他 (規則用於在此案例中針對惡意流量發出報警記錄-[全部拒絕]) </span><span class="sxs-lookup"><span data-stu-id="f4d20-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="f4d20-123">範例5：建立可允許埠8080上所有 HTTP 流量的防火牆，但會封鎖由威脅 Intel 所識別的惡意網域</span><span class="sxs-lookup"><span data-stu-id="f4d20-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="f4d20-124">這個範例會建立一個防火牆，以允許埠8080上的所有 HTTP 流量，除非受威脅 Intel 認為是惡意的。</span><span class="sxs-lookup"><span data-stu-id="f4d20-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="f4d20-125">在 [拒絕] 模式中執行時，不像是 [警示]，而受威脅威脅的流量則不只是已登入，但也會封鎖。</span><span class="sxs-lookup"><span data-stu-id="f4d20-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="f4d20-126">範例6：建立沒有規則及可用性區域的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="f4d20-127">這個範例會建立具有所有可用的可用性區域的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="f4d20-128">範例7：建立含有兩個或多個公用 IP 位址的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="f4d20-129">這個範例會建立一個附加至虛擬網路 "vnet" 且具有兩個公用 IP 位址的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="f4d20-130">範例8：建立可讓 MSSQL 流量到特定 SQL 資料庫的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="f4d20-131">這個範例會建立可讓標準埠1433上的 MSSQL 流量的防火牆，以使用 SQL database sql1.database.windows.net。</span><span class="sxs-lookup"><span data-stu-id="f4d20-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="f4d20-132">範例9：建立附加至虛擬中樞的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="f4d20-133">這個範例會建立一個附加至虛擬中樞 "vHub" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="f4d20-134">防火牆原則 $fp 將會附加到防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="f4d20-135">此防火牆可根據防火牆原則 $fp 中提到的規則來允許/拒絕流量。</span><span class="sxs-lookup"><span data-stu-id="f4d20-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="f4d20-136">虛擬中樞和防火牆應該位於同一個區域中。</span><span class="sxs-lookup"><span data-stu-id="f4d20-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="f4d20-137">範例10：建立含威脅智慧白名單設定的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="f4d20-138">這個範例會建立一個從威脅情報白名單 "www.microsoft.com" 和 "8.8.8.8" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="f4d20-139">範例11：建立含自訂的專用範圍設定的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="f4d20-140">這個範例會建立一個將 "99.99.99.0/24" 和 "66.66.0.0/16" 視為私人 ip 範圍的防火牆，且不會對這些位址進行 snat 通訊</span><span class="sxs-lookup"><span data-stu-id="f4d20-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="f4d20-141">範例12：建立擁有管理子網及公用 IP 位址的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="f4d20-142">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f4d20-143">因為未指定任何規則，所以防火牆會封鎖所有流量 (預設行為) 。</span><span class="sxs-lookup"><span data-stu-id="f4d20-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="f4d20-144">威脅英特爾也會在預設模式下執行-警示-這表示惡意流量會記錄，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="f4d20-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="f4d20-145">為了支援「強制性隧道」案例，此防火牆將使用子網 "AzureFirewallManagementSubnet" 和管理公用 IP 位址進行管理流量</span><span class="sxs-lookup"><span data-stu-id="f4d20-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="f4d20-146">範例13：建立已將防火牆原則附加至虛擬網路的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="f4d20-147">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f4d20-148">將會從防火牆原則中取得將套用到防火牆的規則和威脅情報</span><span class="sxs-lookup"><span data-stu-id="f4d20-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="f4d20-149">範例14：建立具有 DNS Proxy 與 DNS 伺服器的防火牆</span><span class="sxs-lookup"><span data-stu-id="f4d20-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="f4d20-150">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f4d20-151">此防火牆已啟用 DNS Proxy，且提供了2個 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4d20-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="f4d20-152">此外，您也需要設定 DNS Proxy 來建立網路規則，因此如果有 Fqdn 的網路規則，也會同時使用 DNS proxy。</span><span class="sxs-lookup"><span data-stu-id="f4d20-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="f4d20-153">範例15：建立具有多個 Ip 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="f4d20-154">防火牆可以與虛擬中樞建立關聯</span><span class="sxs-lookup"><span data-stu-id="f4d20-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="f4d20-155">這個範例會建立一個附加至虛擬中樞「中樞」的防火牆，該防火牆是與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f4d20-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f4d20-156">系統會為防火牆指派2個已隱含建立的公用 Ip。</span><span class="sxs-lookup"><span data-stu-id="f4d20-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="f4d20-157">16：使用 [允許 Active FTP] 建立防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="f4d20-158">這個範例會建立一個具有 [允許] 動態 FTP 標誌的防火牆。</span><span class="sxs-lookup"><span data-stu-id="f4d20-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="f4d20-159">參數</span><span class="sxs-lookup"><span data-stu-id="f4d20-159">PARAMETERS</span></span>

### <span data-ttu-id="f4d20-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f4d20-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="f4d20-161">指定新防火牆的應用程式規則集合。</span><span class="sxs-lookup"><span data-stu-id="f4d20-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4d20-162">-AsJob</span></span>
<span data-ttu-id="f4d20-163">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4d20-163">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4d20-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d20-164">-DefaultProfile</span></span>
<span data-ttu-id="f4d20-165">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4d20-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f4d20-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="f4d20-167">在網路規則中需要 Fqdn 的 DNS Proxy 功能。</span><span class="sxs-lookup"><span data-stu-id="f4d20-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

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

### <span data-ttu-id="f4d20-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="f4d20-168">-DnsServer</span></span>
<span data-ttu-id="f4d20-169">要用於 DNS 解析的 DNS 伺服器清單，</span><span class="sxs-lookup"><span data-stu-id="f4d20-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="f4d20-170">-EnableDnsProxy</span></span>
<span data-ttu-id="f4d20-171">[啟用 DNS Proxy]。</span><span class="sxs-lookup"><span data-stu-id="f4d20-171">Enable DNS Proxy.</span></span> <span data-ttu-id="f4d20-172">預設為停用。</span><span class="sxs-lookup"><span data-stu-id="f4d20-172">By default it is disabled.</span></span>


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

### <span data-ttu-id="f4d20-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="f4d20-173">-AllowActiveFTP</span></span>
<span data-ttu-id="f4d20-174">允許在防火牆上使用 Active FTP。</span><span class="sxs-lookup"><span data-stu-id="f4d20-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="f4d20-175">預設為停用。</span><span class="sxs-lookup"><span data-stu-id="f4d20-175">By default it is disabled.</span></span>


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

### <span data-ttu-id="f4d20-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f4d20-176">-FirewallPolicyId</span></span>
<span data-ttu-id="f4d20-177">附加到防火牆的防火牆原則</span><span class="sxs-lookup"><span data-stu-id="f4d20-177">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="f4d20-178">-Force</span><span class="sxs-lookup"><span data-stu-id="f4d20-178">-Force</span></span>
<span data-ttu-id="f4d20-179">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f4d20-179">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4d20-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f4d20-180">-HubIPAddresses</span></span>
<span data-ttu-id="f4d20-181">連接至虛擬中樞之防火牆的 ip 位址</span><span class="sxs-lookup"><span data-stu-id="f4d20-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-182">-位置</span><span class="sxs-lookup"><span data-stu-id="f4d20-182">-Location</span></span>
<span data-ttu-id="f4d20-183">指定防火牆的區域。</span><span class="sxs-lookup"><span data-stu-id="f4d20-183">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="f4d20-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4d20-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="f4d20-185">一個或多個用來管理流量的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f4d20-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="f4d20-186">公用 IP 位址必須使用標準 SKU，且必須屬於相同的資源群組（防火牆）。</span><span class="sxs-lookup"><span data-stu-id="f4d20-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-187">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4d20-187">-Name</span></span>
<span data-ttu-id="f4d20-188">指定此 Cmdlet 所建立之 Azure 防火牆的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d20-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f4d20-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f4d20-189">-NatRuleCollection</span></span>
<span data-ttu-id="f4d20-190">AzureFirewallNatRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="f4d20-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f4d20-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="f4d20-192">AzureFirewallNetworkRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="f4d20-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="f4d20-193">-PrivateRange</span></span>
<span data-ttu-id="f4d20-194">無法 SNAT'ed 流量的專用 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="f4d20-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4d20-195">-PublicIpAddress</span></span>
<span data-ttu-id="f4d20-196">一或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f4d20-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="f4d20-197">公用 IP 位址必須使用標準 SKU，且必須屬於相同的資源群組（防火牆）。</span><span class="sxs-lookup"><span data-stu-id="f4d20-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="f4d20-198">-PublicIpName</span></span>
<span data-ttu-id="f4d20-199">公用 Ip 名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d20-199">Public Ip Name.</span></span> <span data-ttu-id="f4d20-200">公用 IP 必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f4d20-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d20-201">-ResourceGroupName</span></span>
<span data-ttu-id="f4d20-202">指定要包含防火牆之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d20-202">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="f4d20-203">-Sku</span><span class="sxs-lookup"><span data-stu-id="f4d20-203">-Sku</span></span>
<span data-ttu-id="f4d20-204">防火牆的 sku 類型</span><span class="sxs-lookup"><span data-stu-id="f4d20-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4d20-205">-Tag</span></span>
<span data-ttu-id="f4d20-206">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f4d20-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f4d20-207">例如：</span><span class="sxs-lookup"><span data-stu-id="f4d20-207">For example:</span></span>

<span data-ttu-id="f4d20-208">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f4d20-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f4d20-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f4d20-209">-ThreatIntelMode</span></span>
<span data-ttu-id="f4d20-210">指定威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="f4d20-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="f4d20-211">預設模式為 [警示]，而不是 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="f4d20-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f4d20-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="f4d20-213">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="f4d20-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="f4d20-214">-VirtualHubId</span></span>
<span data-ttu-id="f4d20-215">已附加防火牆的虛擬中心</span><span class="sxs-lookup"><span data-stu-id="f4d20-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="f4d20-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4d20-216">-VirtualNetwork</span></span>
<span data-ttu-id="f4d20-217">虛擬網路</span><span class="sxs-lookup"><span data-stu-id="f4d20-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f4d20-218">-VirtualNetworkName</span></span>
<span data-ttu-id="f4d20-219">指定將部署防火牆的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d20-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="f4d20-220">虛擬網路和防火牆必須屬於相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f4d20-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="f4d20-221">-Zone</span></span>
<span data-ttu-id="f4d20-222">用來表示防火牆需要的位置的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="f4d20-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d20-223">-確認</span><span class="sxs-lookup"><span data-stu-id="f4d20-223">-Confirm</span></span>
<span data-ttu-id="f4d20-224">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4d20-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d20-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d20-225">-WhatIf</span></span>
<span data-ttu-id="f4d20-226">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4d20-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d20-227">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4d20-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d20-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d20-228">CommonParameters</span></span>
<span data-ttu-id="f4d20-229">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4d20-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d20-230">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4d20-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d20-231">輸入</span><span class="sxs-lookup"><span data-stu-id="f4d20-231">INPUTS</span></span>

### <span data-ttu-id="f4d20-232">System.object</span><span class="sxs-lookup"><span data-stu-id="f4d20-232">System.String</span></span>

### <span data-ttu-id="f4d20-233">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4d20-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="f4d20-234">PSPublicIpAddress [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f4d20-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="f4d20-235">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4d20-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="f4d20-236">PSAzureFirewallApplicationRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f4d20-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="f4d20-237">PSAzureFirewallNatRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f4d20-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="f4d20-238">PSAzureFirewallNetworkRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f4d20-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="f4d20-239">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4d20-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4d20-240">輸出</span><span class="sxs-lookup"><span data-stu-id="f4d20-240">OUTPUTS</span></span>

### <span data-ttu-id="f4d20-241">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4d20-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f4d20-242">筆記</span><span class="sxs-lookup"><span data-stu-id="f4d20-242">NOTES</span></span>

## <span data-ttu-id="f4d20-243">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4d20-243">RELATED LINKS</span></span>

[<span data-ttu-id="f4d20-244">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4d20-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f4d20-245">移除-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4d20-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="f4d20-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4d20-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="f4d20-247">新-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f4d20-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="f4d20-248">新-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f4d20-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="f4d20-249">新-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f4d20-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)