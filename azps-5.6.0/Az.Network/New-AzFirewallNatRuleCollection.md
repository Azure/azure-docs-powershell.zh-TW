---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: d637767f21a34daf5afaf1f2a44e9ebc9b80934a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913149"
---
# <span data-ttu-id="0a875-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0a875-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="0a875-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a875-102">SYNOPSIS</span></span>
<span data-ttu-id="0a875-103">建立防火牆 NAT 規則集合。</span><span class="sxs-lookup"><span data-stu-id="0a875-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="0a875-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a875-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a875-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a875-105">DESCRIPTION</span></span>
<span data-ttu-id="0a875-106">**New-AzFirewallNatRuleCollection** Cmdlet 會建立防火牆 NAT 規則的集合。</span><span class="sxs-lookup"><span data-stu-id="0a875-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="0a875-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a875-107">EXAMPLES</span></span>

### <span data-ttu-id="0a875-108">範例 1：使用一個規則建立集合</span><span class="sxs-lookup"><span data-stu-id="0a875-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="0a875-109">此範例會建立包含一個規則的集合。</span><span class="sxs-lookup"><span data-stu-id="0a875-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="0a875-110">所有符合 $rule 1 中識別條件的流量，都會使用由 $RULE T 轉譯的位址和埠。</span><span class="sxs-lookup"><span data-stu-id="0a875-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="0a875-111">範例 2：新增規則至規則集合</span><span class="sxs-lookup"><span data-stu-id="0a875-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="0a875-112">此範例會使用一個規則建立一個新的 NAT 規則集合，然後使用規則集合物件上的 AddRule 方法，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="0a875-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="0a875-113">指定規則集合中的每個規則名稱都必須有唯一的名稱，而且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0a875-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="0a875-114">範例 3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="0a875-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="0a875-115">此範例會使用一個規則建立新 NAT 規則集合，然後依名稱取得規則，呼叫方法 GetRuleByName 在規則集合物件上。</span><span class="sxs-lookup"><span data-stu-id="0a875-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="0a875-116">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0a875-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="0a875-117">範例 4：從規則集合移除規則</span><span class="sxs-lookup"><span data-stu-id="0a875-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="0a875-118">此範例會建立一個包含兩個規則的新 NAT 規則集合，然後呼叫規則集合物件上的 RemoveRuleByName，從規則集合移除第一個規則。</span><span class="sxs-lookup"><span data-stu-id="0a875-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="0a875-119">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0a875-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="0a875-120">參數</span><span class="sxs-lookup"><span data-stu-id="0a875-120">PARAMETERS</span></span>

### <span data-ttu-id="0a875-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a875-121">-DefaultProfile</span></span>
<span data-ttu-id="0a875-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a875-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a875-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a875-123">-Name</span></span>
<span data-ttu-id="0a875-124">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a875-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="0a875-125">名稱必須在規則集合中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0a875-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="0a875-126">-優先順序</span><span class="sxs-lookup"><span data-stu-id="0a875-126">-Priority</span></span>
<span data-ttu-id="0a875-127">指定此規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="0a875-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="0a875-128">優先順序是介於 100 到 65000 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="0a875-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="0a875-129">數位越小，優先順序越大。</span><span class="sxs-lookup"><span data-stu-id="0a875-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="0a875-130">-規則</span><span class="sxs-lookup"><span data-stu-id="0a875-130">-Rule</span></span>
<span data-ttu-id="0a875-131">指定此集合下要分組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="0a875-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a875-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0a875-132">-Confirm</span></span>
<span data-ttu-id="0a875-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a875-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a875-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a875-134">-WhatIf</span></span>
<span data-ttu-id="0a875-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a875-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a875-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a875-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a875-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a875-137">CommonParameters</span></span>
<span data-ttu-id="0a875-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a875-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a875-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0a875-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a875-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0a875-140">INPUTS</span></span>

### <span data-ttu-id="0a875-141">沒有</span><span class="sxs-lookup"><span data-stu-id="0a875-141">None</span></span>

## <span data-ttu-id="0a875-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0a875-142">OUTPUTS</span></span>

### <span data-ttu-id="0a875-143">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0a875-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="0a875-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0a875-144">NOTES</span></span>

## <span data-ttu-id="0a875-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a875-145">RELATED LINKS</span></span>

[<span data-ttu-id="0a875-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="0a875-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="0a875-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0a875-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="0a875-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0a875-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
