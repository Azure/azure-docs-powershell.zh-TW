---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136290"
---
# <span data-ttu-id="26fe5-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="26fe5-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="26fe5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="26fe5-103">建立網路規則的 Azure 防火牆網路集合。</span><span class="sxs-lookup"><span data-stu-id="26fe5-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="26fe5-104">句法</span><span class="sxs-lookup"><span data-stu-id="26fe5-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26fe5-105">說明</span><span class="sxs-lookup"><span data-stu-id="26fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="26fe5-106">**新的-AzFirewallNetworkRuleCollection** Cmdlet 會建立防火牆網路規則的集合。</span><span class="sxs-lookup"><span data-stu-id="26fe5-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="26fe5-107">示例</span><span class="sxs-lookup"><span data-stu-id="26fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="26fe5-108">範例1：使用兩個規則建立網路集合</span><span class="sxs-lookup"><span data-stu-id="26fe5-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="26fe5-109">這個範例會建立集合，以允許符合兩個規則中任一種的流量。</span><span class="sxs-lookup"><span data-stu-id="26fe5-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="26fe5-110">第一個規則是適用于所有的 UDP 流量。</span><span class="sxs-lookup"><span data-stu-id="26fe5-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="26fe5-111">第二個規則是從10.0.0.0 至60.1.5.0：4040的 TCP 流量。</span><span class="sxs-lookup"><span data-stu-id="26fe5-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="26fe5-112">如果有具有較高優先順序的另一個網路規則集合 (較小的數位) ，也就是與 $rule 1 或 $rule 2 中所識別的流量相符，具有較高優先順序的 rule 集合的動作將會生效。</span><span class="sxs-lookup"><span data-stu-id="26fe5-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="26fe5-113">範例2：在規則集合中加入規則</span><span class="sxs-lookup"><span data-stu-id="26fe5-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="26fe5-114">這個範例會建立一個含有一個規則的新網路規則集合，然後使用規則集合物件上的方法 AddRule，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="26fe5-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="26fe5-115">指定規則集合中的每個規則名稱必須具有唯一的名稱，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="26fe5-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="26fe5-116">範例3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="26fe5-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="26fe5-117">這個範例會建立一個含有一條規則的新網路規則集合，然後依名稱取得規則，並在規則集合物件上呼叫方法 GetRuleByName。</span><span class="sxs-lookup"><span data-stu-id="26fe5-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="26fe5-118">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="26fe5-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="26fe5-119">範例4：從規則集合中移除規則</span><span class="sxs-lookup"><span data-stu-id="26fe5-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="26fe5-120">這個範例會建立具有兩個規則的新網路規則集合，然後在規則集合物件上呼叫方法 RemoveRuleByName，移除規則集合中的第一個規則。</span><span class="sxs-lookup"><span data-stu-id="26fe5-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="26fe5-121">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="26fe5-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="26fe5-122">參數</span><span class="sxs-lookup"><span data-stu-id="26fe5-122">PARAMETERS</span></span>

### <span data-ttu-id="26fe5-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="26fe5-123">-ActionType</span></span>
<span data-ttu-id="26fe5-124">指定要針對此規則的流量相符之情況採取的動作。</span><span class="sxs-lookup"><span data-stu-id="26fe5-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="26fe5-125">已接受的動作為「允許」或「拒絕」。</span><span class="sxs-lookup"><span data-stu-id="26fe5-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fe5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fe5-126">-DefaultProfile</span></span>
<span data-ttu-id="26fe5-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26fe5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26fe5-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="26fe5-128">-Name</span></span>
<span data-ttu-id="26fe5-129">指定此網路規則集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="26fe5-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="26fe5-130">該名稱在所有網路規則集合中都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="26fe5-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fe5-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="26fe5-131">-Priority</span></span>
<span data-ttu-id="26fe5-132">指定此規則集合的優先順序。</span><span class="sxs-lookup"><span data-stu-id="26fe5-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="26fe5-133">[優先順序] 是介於100和65000之間的數位。</span><span class="sxs-lookup"><span data-stu-id="26fe5-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="26fe5-134">數值越小，優先順序越高。</span><span class="sxs-lookup"><span data-stu-id="26fe5-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fe5-135">-規則</span><span class="sxs-lookup"><span data-stu-id="26fe5-135">-Rule</span></span>
<span data-ttu-id="26fe5-136">指定要在此集合下組成群組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="26fe5-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fe5-137">-確認</span><span class="sxs-lookup"><span data-stu-id="26fe5-137">-Confirm</span></span>
<span data-ttu-id="26fe5-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26fe5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fe5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26fe5-139">-WhatIf</span></span>
<span data-ttu-id="26fe5-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26fe5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26fe5-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26fe5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fe5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fe5-142">CommonParameters</span></span>
<span data-ttu-id="26fe5-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26fe5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fe5-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26fe5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fe5-145">輸入</span><span class="sxs-lookup"><span data-stu-id="26fe5-145">INPUTS</span></span>

### <span data-ttu-id="26fe5-146">所有</span><span class="sxs-lookup"><span data-stu-id="26fe5-146">None</span></span>

## <span data-ttu-id="26fe5-147">輸出</span><span class="sxs-lookup"><span data-stu-id="26fe5-147">OUTPUTS</span></span>

### <span data-ttu-id="26fe5-148">PSAzureFirewallNetworkRuleCollection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26fe5-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="26fe5-149">筆記</span><span class="sxs-lookup"><span data-stu-id="26fe5-149">NOTES</span></span>

## <span data-ttu-id="26fe5-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="26fe5-150">RELATED LINKS</span></span>

[<span data-ttu-id="26fe5-151">新-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="26fe5-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="26fe5-152">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="26fe5-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="26fe5-153">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="26fe5-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)