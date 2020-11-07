---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 6d0935b0b2c5296a5d45d25c56cd7feb9e269a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788985"
---
# <span data-ttu-id="dc810-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc810-101">Set-AzFirewall</span></span>

## <span data-ttu-id="dc810-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc810-102">SYNOPSIS</span></span>
<span data-ttu-id="dc810-103">儲存已修改的防火牆。</span><span class="sxs-lookup"><span data-stu-id="dc810-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="dc810-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc810-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc810-105">說明</span><span class="sxs-lookup"><span data-stu-id="dc810-105">DESCRIPTION</span></span>
<span data-ttu-id="dc810-106">**AzFirewall** Cmdlet 會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="dc810-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="dc810-107">示例</span><span class="sxs-lookup"><span data-stu-id="dc810-107">EXAMPLES</span></span>

### <span data-ttu-id="dc810-108">1：更新防火牆應用程式規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="dc810-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="dc810-109">此範例更新現有的 Azure 防火牆規則集合的優先順序。</span><span class="sxs-lookup"><span data-stu-id="dc810-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="dc810-110">假設資源群組 "rg" 中的 Azure 防火牆「AzureFirewall」包含名為「ruleCollectionName」的應用程式規則集合，則上述命令將會變更該規則集合的優先順序，之後就會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="dc810-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="dc810-111">如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="dc810-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="dc810-112">2：建立 Azure 防火牆並稍後設定應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="dc810-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="dc810-113">在這個範例中，首先會建立不含任何應用程式規則集合的防火牆。</span><span class="sxs-lookup"><span data-stu-id="dc810-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="dc810-114">接著會建立應用程式規則和應用程式規則集合，然後在記憶體中修改 Firewall 物件，而不會影響雲端的實際設定。</span><span class="sxs-lookup"><span data-stu-id="dc810-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="dc810-115">若要在雲端反射的變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="dc810-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="dc810-116">3：更新 Microsoft Azure 防火牆的 [Intel 作業] 模式</span><span class="sxs-lookup"><span data-stu-id="dc810-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="dc810-117">這個範例會更新資源群組 "rg" 中的 Azure 防火牆 "AzureFirewall" 的威脅 Intel 作業模式。</span><span class="sxs-lookup"><span data-stu-id="dc810-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="dc810-118">如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="dc810-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="dc810-119">4：解除配置並指派防火牆</span><span class="sxs-lookup"><span data-stu-id="dc810-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```

<span data-ttu-id="dc810-120">這個範例會檢索防火牆、解除防火牆的釋放並儲存防火牆。</span><span class="sxs-lookup"><span data-stu-id="dc810-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="dc810-121">解除配置命令會移除執行中的服務，但會保留防火牆的設定。</span><span class="sxs-lookup"><span data-stu-id="dc810-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="dc810-122">若要在雲端反射的變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="dc810-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="dc810-123">如果使用者想要再次啟動服務，請在防火牆上呼叫 Allocate 方法。</span><span class="sxs-lookup"><span data-stu-id="dc810-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="dc810-124">新的 VNet 和公用 IP 必須與防火牆在相同的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="dc810-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="dc810-125">同樣地，若要在雲端中反映變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="dc810-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="dc810-126">5：將公用 IP 位址新增至 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="dc810-126">5:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="dc810-127">在這個範例中，公用 IP 位址 "azFwPublicIp1" 已附加到防火牆。</span><span class="sxs-lookup"><span data-stu-id="dc810-127">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="dc810-128">6：從 Azure 防火牆移除公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dc810-128">6:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="dc810-129">在這個範例中，公用 IP 位址「azFwPublicIp1」已從防火牆中分離。</span><span class="sxs-lookup"><span data-stu-id="dc810-129">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

## <span data-ttu-id="dc810-130">參數</span><span class="sxs-lookup"><span data-stu-id="dc810-130">PARAMETERS</span></span>

### <span data-ttu-id="dc810-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc810-131">-AsJob</span></span>
<span data-ttu-id="dc810-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc810-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc810-133">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="dc810-133">-AzureFirewall</span></span>
<span data-ttu-id="dc810-134">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="dc810-134">The AzureFirewall</span></span>

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

### <span data-ttu-id="dc810-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc810-135">-DefaultProfile</span></span>
<span data-ttu-id="dc810-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc810-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc810-137">-確認</span><span class="sxs-lookup"><span data-stu-id="dc810-137">-Confirm</span></span>
<span data-ttu-id="dc810-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc810-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc810-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc810-139">-WhatIf</span></span>
<span data-ttu-id="dc810-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc810-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc810-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc810-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc810-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc810-142">CommonParameters</span></span>
<span data-ttu-id="dc810-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc810-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc810-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc810-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc810-145">輸入</span><span class="sxs-lookup"><span data-stu-id="dc810-145">INPUTS</span></span>

### <span data-ttu-id="dc810-146">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc810-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="dc810-147">輸出</span><span class="sxs-lookup"><span data-stu-id="dc810-147">OUTPUTS</span></span>

### <span data-ttu-id="dc810-148">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc810-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="dc810-149">筆記</span><span class="sxs-lookup"><span data-stu-id="dc810-149">NOTES</span></span>

## <span data-ttu-id="dc810-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc810-150">RELATED LINKS</span></span>

[<span data-ttu-id="dc810-151">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc810-151">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dc810-152">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc810-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dc810-153">移除-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc810-153">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
