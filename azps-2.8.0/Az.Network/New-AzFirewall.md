---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789369"
---
# <span data-ttu-id="b6121-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6121-101">New-AzFirewall</span></span>

## <span data-ttu-id="b6121-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6121-102">SYNOPSIS</span></span>
<span data-ttu-id="b6121-103">在資源群組中建立新的防火牆。</span><span class="sxs-lookup"><span data-stu-id="b6121-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="b6121-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6121-104">SYNTAX</span></span>

### <span data-ttu-id="b6121-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b6121-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6121-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="b6121-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6121-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="b6121-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6121-108">說明</span><span class="sxs-lookup"><span data-stu-id="b6121-108">DESCRIPTION</span></span>
<span data-ttu-id="b6121-109">**新的-AzFirewall** Cmdlet 會建立 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="b6121-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="b6121-110">示例</span><span class="sxs-lookup"><span data-stu-id="b6121-110">EXAMPLES</span></span>

### <span data-ttu-id="b6121-111">1：建立附加至虛擬網路的防火牆</span><span class="sxs-lookup"><span data-stu-id="b6121-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="b6121-112">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="b6121-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="b6121-113">因為未指定任何規則，所以防火牆會封鎖所有流量 (預設行為) 。</span><span class="sxs-lookup"><span data-stu-id="b6121-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="b6121-114">威脅英特爾也會在預設模式下執行-警示-這表示惡意流量會記錄，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="b6121-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="b6121-115">2：建立可讓所有 HTTPS 流量使用的防火牆</span><span class="sxs-lookup"><span data-stu-id="b6121-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="b6121-116">這個範例會建立可讓埠443上所有 HTTPS 流量的防火牆。</span><span class="sxs-lookup"><span data-stu-id="b6121-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="b6121-117">威脅英特爾將在預設模式下執行-警示-這表示會記錄惡意流量，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="b6121-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="b6121-118">3： DNAT-將流向10.1.2.3：80的流量重新導向至10.2.3.4：8080</span><span class="sxs-lookup"><span data-stu-id="b6121-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="b6121-119">這個範例會建立一個已將10.1.2.3：80到10.2.3.4：8080威脅的 [所有資料包] 的目標 IP 和埠，將其轉換為此範例中的 [Intel]。</span><span class="sxs-lookup"><span data-stu-id="b6121-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="b6121-120">4：建立不含規則的防火牆，並在警示模式中與 Intel 威脅</span><span class="sxs-lookup"><span data-stu-id="b6121-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="b6121-121">這個範例會建立一個防火牆，該防火牆會封鎖 (預設行為的所有通訊，) 且在 [警示] 模式中受到 Intel 執行的威脅。</span><span class="sxs-lookup"><span data-stu-id="b6121-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="b6121-122">這表示在此情況下，將其他 (規則用於在此案例中針對惡意流量發出報警記錄-[全部拒絕]) </span><span class="sxs-lookup"><span data-stu-id="b6121-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="b6121-123">5：建立可允許埠8080上所有 HTTP 流量的防火牆，但會封鎖由威脅 Intel 所識別的惡意網域</span><span class="sxs-lookup"><span data-stu-id="b6121-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="b6121-124">這個範例會建立一個防火牆，以允許埠8080上的所有 HTTP 流量，除非受威脅 Intel 認為是惡意的。</span><span class="sxs-lookup"><span data-stu-id="b6121-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="b6121-125">在 [拒絕] 模式中執行時，不像是 [警示]，而受威脅威脅的流量則不只是已登入，但也會封鎖。</span><span class="sxs-lookup"><span data-stu-id="b6121-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="b6121-126">6：建立沒有規則及可用性區域的防火牆</span><span class="sxs-lookup"><span data-stu-id="b6121-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="b6121-127">這個範例會建立具有所有可用的可用性區域的防火牆。</span><span class="sxs-lookup"><span data-stu-id="b6121-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="b6121-128">7：建立具有兩個或多個公用 IP 位址的防火牆</span><span class="sxs-lookup"><span data-stu-id="b6121-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="b6121-129">這個範例會建立一個附加至虛擬網路 "vnet" 且具有兩個公用 IP 位址的防火牆。</span><span class="sxs-lookup"><span data-stu-id="b6121-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="b6121-130">8：建立可讓 MSSQL 流量傳送至特定 SQL 資料庫的防火牆</span><span class="sxs-lookup"><span data-stu-id="b6121-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="b6121-131">這個範例會建立可讓標準埠1433上的 MSSQL 流量的防火牆，以使用 SQL database sql1.database.windows.net。</span><span class="sxs-lookup"><span data-stu-id="b6121-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="b6121-132">參數</span><span class="sxs-lookup"><span data-stu-id="b6121-132">PARAMETERS</span></span>

### <span data-ttu-id="b6121-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6121-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="b6121-134">指定新防火牆的應用程式規則集合。</span><span class="sxs-lookup"><span data-stu-id="b6121-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="b6121-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6121-135">-AsJob</span></span>
<span data-ttu-id="b6121-136">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6121-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6121-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6121-137">-DefaultProfile</span></span>
<span data-ttu-id="b6121-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6121-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6121-139">-Force</span><span class="sxs-lookup"><span data-stu-id="b6121-139">-Force</span></span>
<span data-ttu-id="b6121-140">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b6121-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6121-141">-位置</span><span class="sxs-lookup"><span data-stu-id="b6121-141">-Location</span></span>
<span data-ttu-id="b6121-142">指定防火牆的區域。</span><span class="sxs-lookup"><span data-stu-id="b6121-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="b6121-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6121-143">-Name</span></span>
<span data-ttu-id="b6121-144">指定此 Cmdlet 所建立之 Azure 防火牆的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6121-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b6121-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6121-145">-NatRuleCollection</span></span>
<span data-ttu-id="b6121-146">AzureFirewallNatRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="b6121-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="b6121-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6121-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="b6121-148">AzureFirewallNetworkRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="b6121-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="b6121-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6121-149">-PublicIpAddress</span></span>
<span data-ttu-id="b6121-150">一或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b6121-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="b6121-151">公用 IP 位址必須使用標準 SKU，且必須屬於相同的資源群組（防火牆）。</span><span class="sxs-lookup"><span data-stu-id="b6121-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="b6121-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="b6121-152">-PublicIpName</span></span>
<span data-ttu-id="b6121-153">公用 Ip 名稱。</span><span class="sxs-lookup"><span data-stu-id="b6121-153">Public Ip Name.</span></span> <span data-ttu-id="b6121-154">公用 IP 必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b6121-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="b6121-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6121-155">-ResourceGroupName</span></span>
<span data-ttu-id="b6121-156">指定要包含防火牆之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6121-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="b6121-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="b6121-157">-Zone</span></span>
<span data-ttu-id="b6121-158">用來表示防火牆需要的位置的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="b6121-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="b6121-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6121-159">-Tag</span></span>
<span data-ttu-id="b6121-160">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b6121-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6121-161">例如：</span><span class="sxs-lookup"><span data-stu-id="b6121-161">For example:</span></span>

<span data-ttu-id="b6121-162">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b6121-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b6121-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="b6121-163">-ThreatIntelMode</span></span>
<span data-ttu-id="b6121-164">指定威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="b6121-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="b6121-165">預設模式為 [警示]，而不是 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="b6121-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="b6121-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6121-166">-VirtualNetwork</span></span>
<span data-ttu-id="b6121-167">虛擬網路</span><span class="sxs-lookup"><span data-stu-id="b6121-167">Virtual Network</span></span>

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

### <span data-ttu-id="b6121-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b6121-168">-VirtualNetworkName</span></span>
<span data-ttu-id="b6121-169">指定將部署防火牆的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="b6121-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="b6121-170">虛擬網路和防火牆必須屬於相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b6121-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="b6121-171">-確認</span><span class="sxs-lookup"><span data-stu-id="b6121-171">-Confirm</span></span>
<span data-ttu-id="b6121-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6121-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6121-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6121-173">-WhatIf</span></span>
<span data-ttu-id="b6121-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6121-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6121-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6121-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6121-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6121-176">CommonParameters</span></span>
<span data-ttu-id="b6121-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6121-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6121-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6121-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6121-179">輸入</span><span class="sxs-lookup"><span data-stu-id="b6121-179">INPUTS</span></span>

### <span data-ttu-id="b6121-180">System.object</span><span class="sxs-lookup"><span data-stu-id="b6121-180">System.String</span></span>

### <span data-ttu-id="b6121-181">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b6121-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b6121-182">PSPublicIpAddress [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b6121-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="b6121-183">PSAzureFirewallApplicationRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b6121-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="b6121-184">PSAzureFirewallNatRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b6121-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="b6121-185">PSAzureFirewallNetworkRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b6121-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="b6121-186">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6121-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6121-187">輸出</span><span class="sxs-lookup"><span data-stu-id="b6121-187">OUTPUTS</span></span>

### <span data-ttu-id="b6121-188">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b6121-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b6121-189">筆記</span><span class="sxs-lookup"><span data-stu-id="b6121-189">NOTES</span></span>

## <span data-ttu-id="b6121-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6121-190">RELATED LINKS</span></span>

[<span data-ttu-id="b6121-191">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6121-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="b6121-192">移除-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6121-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="b6121-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6121-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="b6121-194">新-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6121-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="b6121-195">新-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6121-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="b6121-196">新-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6121-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
