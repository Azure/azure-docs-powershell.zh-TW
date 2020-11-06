---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621791"
---
# <span data-ttu-id="dcea7-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcea7-101">New-AzFirewall</span></span>

## <span data-ttu-id="dcea7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcea7-102">SYNOPSIS</span></span>
<span data-ttu-id="dcea7-103">在資源群組中建立新的防火牆。</span><span class="sxs-lookup"><span data-stu-id="dcea7-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="dcea7-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcea7-104">SYNTAX</span></span>

### <span data-ttu-id="dcea7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="dcea7-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcea7-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="dcea7-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcea7-107">說明</span><span class="sxs-lookup"><span data-stu-id="dcea7-107">DESCRIPTION</span></span>
<span data-ttu-id="dcea7-108">**新的-AzFirewall** Cmdlet 會建立 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="dcea7-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="dcea7-109">示例</span><span class="sxs-lookup"><span data-stu-id="dcea7-109">EXAMPLES</span></span>

### <span data-ttu-id="dcea7-110">1：建立附加至虛擬網路的防火牆</span><span class="sxs-lookup"><span data-stu-id="dcea7-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="dcea7-111">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="dcea7-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="dcea7-112">因為未指定任何規則，所以防火牆會封鎖所有流量 (預設行為) 。</span><span class="sxs-lookup"><span data-stu-id="dcea7-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="dcea7-113">威脅英特爾也會在預設模式下執行-警示-這表示惡意流量會記錄，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="dcea7-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="dcea7-114">2：建立可讓所有 HTTPS 流量使用的防火牆</span><span class="sxs-lookup"><span data-stu-id="dcea7-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="dcea7-115">這個範例會建立可讓埠443上所有 HTTPS 流量的防火牆。</span><span class="sxs-lookup"><span data-stu-id="dcea7-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="dcea7-116">威脅英特爾將在預設模式下執行-警示-這表示會記錄惡意流量，但不會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="dcea7-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="dcea7-117">3： DNAT-將流向10.1.2.3：80的流量重新導向至10.2.3.4：8080</span><span class="sxs-lookup"><span data-stu-id="dcea7-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="dcea7-118">這個範例會建立一個已將10.1.2.3：80到10.2.3.4：8080威脅的 [所有資料包] 的目標 IP 和埠，將其轉換為此範例中的 [Intel]。</span><span class="sxs-lookup"><span data-stu-id="dcea7-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="dcea7-119">4：建立不含規則的防火牆，並在警示模式中與 Intel 威脅</span><span class="sxs-lookup"><span data-stu-id="dcea7-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="dcea7-120">這個範例會建立一個防火牆，該防火牆會封鎖 (預設行為的所有通訊，) 且在 [警示] 模式中受到 Intel 執行的威脅。</span><span class="sxs-lookup"><span data-stu-id="dcea7-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="dcea7-121">這表示在此情況下，將其他 (規則用於在此案例中針對惡意流量發出報警記錄-[全部拒絕]) </span><span class="sxs-lookup"><span data-stu-id="dcea7-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="dcea7-122">5：建立可允許埠8080上所有 HTTP 流量的防火牆，但會封鎖由威脅 Intel 所識別的惡意網域</span><span class="sxs-lookup"><span data-stu-id="dcea7-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="dcea7-123">這個範例會建立一個防火牆，以允許埠8080上的所有 HTTP 流量，除非受威脅 Intel 認為是惡意的。</span><span class="sxs-lookup"><span data-stu-id="dcea7-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="dcea7-124">在 [拒絕] 模式中執行時，不像是 [警示]，而受威脅威脅的流量則不只是已登入，但也會封鎖。</span><span class="sxs-lookup"><span data-stu-id="dcea7-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="dcea7-125">參數</span><span class="sxs-lookup"><span data-stu-id="dcea7-125">PARAMETERS</span></span>

### <span data-ttu-id="dcea7-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dcea7-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="dcea7-127">指定新防火牆的應用程式規則集合。</span><span class="sxs-lookup"><span data-stu-id="dcea7-127">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="dcea7-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcea7-128">-AsJob</span></span>
<span data-ttu-id="dcea7-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dcea7-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcea7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcea7-130">-DefaultProfile</span></span>
<span data-ttu-id="dcea7-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcea7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcea7-132">-Force</span><span class="sxs-lookup"><span data-stu-id="dcea7-132">-Force</span></span>
<span data-ttu-id="dcea7-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="dcea7-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcea7-134">-位置</span><span class="sxs-lookup"><span data-stu-id="dcea7-134">-Location</span></span>
<span data-ttu-id="dcea7-135">指定防火牆的區域。</span><span class="sxs-lookup"><span data-stu-id="dcea7-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="dcea7-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="dcea7-136">-Name</span></span>
<span data-ttu-id="dcea7-137">指定此 Cmdlet 所建立之 Azure 防火牆的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcea7-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dcea7-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dcea7-138">-NatRuleCollection</span></span>
<span data-ttu-id="dcea7-139">AzureFirewallNatRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="dcea7-139">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="dcea7-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dcea7-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="dcea7-141">AzureFirewallNetworkRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="dcea7-141">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="dcea7-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="dcea7-142">-PublicIpName</span></span>
<span data-ttu-id="dcea7-143">公用 Ip 名稱。</span><span class="sxs-lookup"><span data-stu-id="dcea7-143">Public Ip Name.</span></span> <span data-ttu-id="dcea7-144">公用 IP 必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="dcea7-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcea7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcea7-145">-ResourceGroupName</span></span>
<span data-ttu-id="dcea7-146">指定要包含防火牆之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcea7-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="dcea7-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="dcea7-147">-Tag</span></span>
<span data-ttu-id="dcea7-148">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="dcea7-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dcea7-149">例如：</span><span class="sxs-lookup"><span data-stu-id="dcea7-149">For example:</span></span>

<span data-ttu-id="dcea7-150">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dcea7-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dcea7-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="dcea7-151">-ThreatIntelMode</span></span>
<span data-ttu-id="dcea7-152">指定威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="dcea7-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="dcea7-153">預設模式為 [警示]，而不是 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="dcea7-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcea7-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dcea7-154">-VirtualNetworkName</span></span>
<span data-ttu-id="dcea7-155">指定將部署防火牆的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="dcea7-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="dcea7-156">虛擬網路和防火牆必須屬於相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="dcea7-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcea7-157">-確認</span><span class="sxs-lookup"><span data-stu-id="dcea7-157">-Confirm</span></span>
<span data-ttu-id="dcea7-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcea7-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcea7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcea7-159">-WhatIf</span></span>
<span data-ttu-id="dcea7-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcea7-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcea7-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcea7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcea7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcea7-162">CommonParameters</span></span>
<span data-ttu-id="dcea7-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcea7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcea7-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dcea7-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcea7-165">輸入</span><span class="sxs-lookup"><span data-stu-id="dcea7-165">INPUTS</span></span>

### <span data-ttu-id="dcea7-166">System.object</span><span class="sxs-lookup"><span data-stu-id="dcea7-166">System.String</span></span>

### <span data-ttu-id="dcea7-167">PSAzureFirewallApplicationRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="dcea7-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="dcea7-168">PSAzureFirewallNatRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="dcea7-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="dcea7-169">PSAzureFirewallNetworkRuleCollection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="dcea7-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="dcea7-170">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dcea7-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dcea7-171">輸出</span><span class="sxs-lookup"><span data-stu-id="dcea7-171">OUTPUTS</span></span>

### <span data-ttu-id="dcea7-172">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dcea7-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="dcea7-173">筆記</span><span class="sxs-lookup"><span data-stu-id="dcea7-173">NOTES</span></span>

## <span data-ttu-id="dcea7-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcea7-174">RELATED LINKS</span></span>

[<span data-ttu-id="dcea7-175">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcea7-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dcea7-176">移除-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcea7-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="dcea7-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcea7-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="dcea7-178">新-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dcea7-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="dcea7-179">新-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dcea7-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="dcea7-180">新-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dcea7-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
