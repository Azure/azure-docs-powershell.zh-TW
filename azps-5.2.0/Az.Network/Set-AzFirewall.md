---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274348"
---
# <span data-ttu-id="68f14-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="68f14-101">Set-AzFirewall</span></span>

## <span data-ttu-id="68f14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68f14-102">SYNOPSIS</span></span>
<span data-ttu-id="68f14-103">儲存已修改的防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="68f14-104">句法</span><span class="sxs-lookup"><span data-stu-id="68f14-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f14-105">說明</span><span class="sxs-lookup"><span data-stu-id="68f14-105">DESCRIPTION</span></span>
<span data-ttu-id="68f14-106">**AzFirewall** Cmdlet 會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="68f14-107">示例</span><span class="sxs-lookup"><span data-stu-id="68f14-107">EXAMPLES</span></span>

### <span data-ttu-id="68f14-108">1：更新防火牆應用程式規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="68f14-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="68f14-109">此範例更新現有的 Azure 防火牆規則集合的優先順序。</span><span class="sxs-lookup"><span data-stu-id="68f14-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="68f14-110">假設資源群組 "rg" 中的 Azure 防火牆「AzureFirewall」包含名為「ruleCollectionName」的應用程式規則集合，則上述命令將會變更該規則集合的優先順序，之後就會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="68f14-111">如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="68f14-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="68f14-112">2：建立 Azure 防火牆並稍後設定應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="68f14-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="68f14-113">在這個範例中，首先會建立不含任何應用程式規則集合的防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="68f14-114">接著會建立應用程式規則和應用程式規則集合，然後在記憶體中修改 Firewall 物件，而不會影響雲端的實際設定。</span><span class="sxs-lookup"><span data-stu-id="68f14-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="68f14-115">若要在雲端反射的變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="68f14-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="68f14-116">3：更新 Microsoft Azure 防火牆的 [Intel 作業] 模式</span><span class="sxs-lookup"><span data-stu-id="68f14-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="68f14-117">這個範例會更新資源群組 "rg" 中的 Azure 防火牆 "AzureFirewall" 的威脅 Intel 作業模式。</span><span class="sxs-lookup"><span data-stu-id="68f14-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="68f14-118">如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="68f14-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="68f14-119">4：解除配置並指派防火牆</span><span class="sxs-lookup"><span data-stu-id="68f14-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="68f14-120">這個範例會檢索防火牆、解除防火牆的釋放並儲存防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="68f14-121">解除配置命令會移除執行中的服務，但會保留防火牆的設定。</span><span class="sxs-lookup"><span data-stu-id="68f14-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="68f14-122">若要在雲端反射的變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="68f14-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="68f14-123">如果使用者想要再次啟動服務，請在防火牆上呼叫 Allocate 方法。</span><span class="sxs-lookup"><span data-stu-id="68f14-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="68f14-124">新的 VNet 和公用 IP 必須與防火牆在相同的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="68f14-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="68f14-125">同樣地，若要在雲端中反映變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="68f14-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="68f14-126">5：使用強制隧道案例的管理公用 IP 位址進行配置</span><span class="sxs-lookup"><span data-stu-id="68f14-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="68f14-127">這個範例會將防火牆與管理公用 IP 位址和子網結合在一起，以進行強制隧道案例的配置。</span><span class="sxs-lookup"><span data-stu-id="68f14-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="68f14-128">VNet 必須包含一個名為 "AzureFirewallManagementSubnet" 的子網。</span><span class="sxs-lookup"><span data-stu-id="68f14-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="68f14-129">6：將公用 IP 位址新增至 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="68f14-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="68f14-130">在這個範例中，公用 IP 位址 "azFwPublicIp1" 已附加到防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="68f14-131">7：從 Azure 防火牆移除公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="68f14-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="68f14-132">在這個範例中，公用 IP 位址「azFwPublicIp1」已從防火牆中分離。</span><span class="sxs-lookup"><span data-stu-id="68f14-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="68f14-133">8：變更 Azure 防火牆上的管理公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="68f14-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="68f14-134">在這個範例中，防火牆的管理公用 IP 位址會變更為 "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="68f14-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="68f14-135">9：新增 DNS 配置至 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="68f14-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="68f14-136">在這個範例中，DNS Proxy 和 DNS 伺服器設定會附加到防火牆。</span><span class="sxs-lookup"><span data-stu-id="68f14-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="68f14-137">10：更新防火牆應用程式規則集合中現有規則的目的地</span><span class="sxs-lookup"><span data-stu-id="68f14-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="68f14-138">這個範例會更新 Azure 防火牆的規則集合中現有規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="68f14-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="68f14-139">這可讓您在 IP 位址動態變更時，自動更新您的規則。</span><span class="sxs-lookup"><span data-stu-id="68f14-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="68f14-140">11：允許 Azure 防火牆上的 Active FTP</span><span class="sxs-lookup"><span data-stu-id="68f14-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="68f14-141">在這個範例中，防火牆允許使用活動的 FTP。</span><span class="sxs-lookup"><span data-stu-id="68f14-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="68f14-142">參數</span><span class="sxs-lookup"><span data-stu-id="68f14-142">PARAMETERS</span></span>

### <span data-ttu-id="68f14-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68f14-143">-AsJob</span></span>
<span data-ttu-id="68f14-144">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="68f14-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68f14-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="68f14-145">-AzureFirewall</span></span>
<span data-ttu-id="68f14-146">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="68f14-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68f14-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f14-147">-DefaultProfile</span></span>
<span data-ttu-id="68f14-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68f14-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68f14-149">-確認</span><span class="sxs-lookup"><span data-stu-id="68f14-149">-Confirm</span></span>
<span data-ttu-id="68f14-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68f14-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f14-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f14-151">-WhatIf</span></span>
<span data-ttu-id="68f14-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68f14-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68f14-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68f14-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f14-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f14-154">CommonParameters</span></span>
<span data-ttu-id="68f14-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68f14-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f14-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68f14-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f14-157">輸入</span><span class="sxs-lookup"><span data-stu-id="68f14-157">INPUTS</span></span>

### <span data-ttu-id="68f14-158">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="68f14-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="68f14-159">輸出</span><span class="sxs-lookup"><span data-stu-id="68f14-159">OUTPUTS</span></span>

### <span data-ttu-id="68f14-160">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="68f14-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="68f14-161">筆記</span><span class="sxs-lookup"><span data-stu-id="68f14-161">NOTES</span></span>

## <span data-ttu-id="68f14-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="68f14-162">RELATED LINKS</span></span>

[<span data-ttu-id="68f14-163">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="68f14-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="68f14-164">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="68f14-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="68f14-165">移除-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="68f14-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
