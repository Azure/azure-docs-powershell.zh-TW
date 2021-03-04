---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 3ccce01d969f6d6601d4db7383aab505923a7063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910417"
---
# <span data-ttu-id="30506-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="30506-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="30506-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30506-102">SYNOPSIS</span></span>
<span data-ttu-id="30506-103">建立 Azure 防火牆網路集合的網路規則。</span><span class="sxs-lookup"><span data-stu-id="30506-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="30506-104">語法</span><span class="sxs-lookup"><span data-stu-id="30506-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30506-105">描述</span><span class="sxs-lookup"><span data-stu-id="30506-105">DESCRIPTION</span></span>
<span data-ttu-id="30506-106">**New-AzFirewallNetworkRuleCollection** Cmdlet 會建立防火牆網路規則的集合。</span><span class="sxs-lookup"><span data-stu-id="30506-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="30506-107">例子</span><span class="sxs-lookup"><span data-stu-id="30506-107">EXAMPLES</span></span>

### <span data-ttu-id="30506-108">範例 1：使用兩個規則建立網路集合</span><span class="sxs-lookup"><span data-stu-id="30506-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="30506-109">此範例會建立一個集合，允許所有符合兩個規則之一的流量。</span><span class="sxs-lookup"><span data-stu-id="30506-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="30506-110">第一個規則是針對所有 UDP 流量。</span><span class="sxs-lookup"><span data-stu-id="30506-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="30506-111">第二個規則適用于從 10.0.0.0 到 60.1.5.0：4040 的 TCP 流量。</span><span class="sxs-lookup"><span data-stu-id="30506-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="30506-112">如果有另一個優先順序較高的網路規則集合 (較小的數位) 也符合 $rule 1 或 $rule 2 中識別的流量，則優先順序較高的規則集合動作會改為生效。</span><span class="sxs-lookup"><span data-stu-id="30506-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="30506-113">範例 2：新增規則至規則集合</span><span class="sxs-lookup"><span data-stu-id="30506-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="30506-114">此範例會使用一個規則建立新網路規則集合，然後使用規則集合物件上的 AddRule 方法，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="30506-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="30506-115">指定規則集合中的每個規則名稱都必須有唯一的名稱，而且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="30506-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="30506-116">範例 3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="30506-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="30506-117">此範例會使用一個規則建立新網路規則集合，然後依名稱取得規則，呼叫方法 GetRuleByName 位於規則集合物件上。</span><span class="sxs-lookup"><span data-stu-id="30506-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="30506-118">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="30506-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="30506-119">範例 4：從規則集合移除規則</span><span class="sxs-lookup"><span data-stu-id="30506-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="30506-120">此範例會建立一個包含兩個規則的新網路規則集合，然後呼叫規則集合物件上的 RemoveRuleByName，從規則集合移除第一個規則。</span><span class="sxs-lookup"><span data-stu-id="30506-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="30506-121">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="30506-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="30506-122">參數</span><span class="sxs-lookup"><span data-stu-id="30506-122">PARAMETERS</span></span>

### <span data-ttu-id="30506-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="30506-123">-ActionType</span></span>
<span data-ttu-id="30506-124">指定針對此規則之流量比對條件要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="30506-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="30506-125">接受的動作為「允許」或「拒絕」。</span><span class="sxs-lookup"><span data-stu-id="30506-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="30506-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30506-126">-DefaultProfile</span></span>
<span data-ttu-id="30506-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30506-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30506-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="30506-128">-Name</span></span>
<span data-ttu-id="30506-129">指定此網路規則集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="30506-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="30506-130">名稱在所有網路規則集合中都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="30506-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="30506-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="30506-131">-Priority</span></span>
<span data-ttu-id="30506-132">指定此規則集合的優先順序。</span><span class="sxs-lookup"><span data-stu-id="30506-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="30506-133">優先順序是介於 100 到 65000 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="30506-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="30506-134">數位越小，優先順序越高。</span><span class="sxs-lookup"><span data-stu-id="30506-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="30506-135">-規則</span><span class="sxs-lookup"><span data-stu-id="30506-135">-Rule</span></span>
<span data-ttu-id="30506-136">指定此集合下要分組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="30506-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="30506-137">-確認</span><span class="sxs-lookup"><span data-stu-id="30506-137">-Confirm</span></span>
<span data-ttu-id="30506-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30506-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30506-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30506-139">-WhatIf</span></span>
<span data-ttu-id="30506-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30506-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30506-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30506-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30506-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30506-142">CommonParameters</span></span>
<span data-ttu-id="30506-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30506-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30506-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="30506-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30506-145">輸入</span><span class="sxs-lookup"><span data-stu-id="30506-145">INPUTS</span></span>

### <span data-ttu-id="30506-146">沒有</span><span class="sxs-lookup"><span data-stu-id="30506-146">None</span></span>

## <span data-ttu-id="30506-147">輸出</span><span class="sxs-lookup"><span data-stu-id="30506-147">OUTPUTS</span></span>

### <span data-ttu-id="30506-148">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="30506-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="30506-149">筆記</span><span class="sxs-lookup"><span data-stu-id="30506-149">NOTES</span></span>

## <span data-ttu-id="30506-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="30506-150">RELATED LINKS</span></span>

[<span data-ttu-id="30506-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="30506-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="30506-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="30506-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="30506-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="30506-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
