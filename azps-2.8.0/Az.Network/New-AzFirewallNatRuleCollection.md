---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 171431e02627177bbb62f64c9a170c02234e0c61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789885"
---
# <span data-ttu-id="eda6a-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="eda6a-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="eda6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eda6a-102">SYNOPSIS</span></span>
<span data-ttu-id="eda6a-103">建立防火牆 NAT 規則的集合。</span><span class="sxs-lookup"><span data-stu-id="eda6a-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="eda6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="eda6a-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="eda6a-105">DESCRIPTION</span></span>
<span data-ttu-id="eda6a-106">**新的-AzFirewallNatRuleCollection** Cmdlet 會建立一個防火牆 NAT 規則集合。</span><span class="sxs-lookup"><span data-stu-id="eda6a-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="eda6a-107">示例</span><span class="sxs-lookup"><span data-stu-id="eda6a-107">EXAMPLES</span></span>

### <span data-ttu-id="eda6a-108">1：使用單一規則建立集合</span><span class="sxs-lookup"><span data-stu-id="eda6a-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="eda6a-109">這個範例會使用一條規則建立集合。</span><span class="sxs-lookup"><span data-stu-id="eda6a-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="eda6a-110">符合 $rule 1 中所識別之條件的所有通信量都會 DNAT'ed 到已翻譯的位址和埠。</span><span class="sxs-lookup"><span data-stu-id="eda6a-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="eda6a-111">2：在規則集合中加入規則</span><span class="sxs-lookup"><span data-stu-id="eda6a-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="eda6a-112">這個範例會使用一個規則建立新的 NAT 規則集合，然後使用 rule 集合物件上的方法 AddRule，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="eda6a-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="eda6a-113">指定規則集合中的每個規則名稱必須具有唯一的名稱，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="eda6a-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="eda6a-114">3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="eda6a-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="eda6a-115">這個範例會使用一個規則建立新的 NAT 規則集合，然後依名稱取得規則，並在規則集合物件上呼叫方法 GetRuleByName。</span><span class="sxs-lookup"><span data-stu-id="eda6a-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="eda6a-116">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="eda6a-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="eda6a-117">4：移除規則集合中的規則</span><span class="sxs-lookup"><span data-stu-id="eda6a-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="eda6a-118">這個範例會使用兩個規則建立新的 NAT 規則集合，然後在規則集合物件上呼叫 method RemoveRuleByName，移除規則集合中的第一個規則。</span><span class="sxs-lookup"><span data-stu-id="eda6a-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="eda6a-119">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="eda6a-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="eda6a-120">參數</span><span class="sxs-lookup"><span data-stu-id="eda6a-120">PARAMETERS</span></span>

### <span data-ttu-id="eda6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda6a-121">-DefaultProfile</span></span>
<span data-ttu-id="eda6a-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eda6a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda6a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="eda6a-123">-Name</span></span>
<span data-ttu-id="eda6a-124">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="eda6a-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="eda6a-125">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="eda6a-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="eda6a-126">-優先順序</span><span class="sxs-lookup"><span data-stu-id="eda6a-126">-Priority</span></span>
<span data-ttu-id="eda6a-127">指定此規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="eda6a-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="eda6a-128">[優先順序] 是介於100和65000之間的數位。</span><span class="sxs-lookup"><span data-stu-id="eda6a-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="eda6a-129">數值越小，優先順序就越大。</span><span class="sxs-lookup"><span data-stu-id="eda6a-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="eda6a-130">-規則</span><span class="sxs-lookup"><span data-stu-id="eda6a-130">-Rule</span></span>
<span data-ttu-id="eda6a-131">指定要在此集合下組成群組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="eda6a-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="eda6a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="eda6a-132">-Confirm</span></span>
<span data-ttu-id="eda6a-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eda6a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda6a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda6a-134">-WhatIf</span></span>
<span data-ttu-id="eda6a-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eda6a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda6a-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eda6a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda6a-137">CommonParameters</span></span>
<span data-ttu-id="eda6a-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eda6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda6a-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eda6a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda6a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="eda6a-140">INPUTS</span></span>

### <span data-ttu-id="eda6a-141">所有</span><span class="sxs-lookup"><span data-stu-id="eda6a-141">None</span></span>

## <span data-ttu-id="eda6a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="eda6a-142">OUTPUTS</span></span>

### <span data-ttu-id="eda6a-143">PSAzureFirewallNatRuleCollection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eda6a-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="eda6a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="eda6a-144">NOTES</span></span>

## <span data-ttu-id="eda6a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="eda6a-145">RELATED LINKS</span></span>

[<span data-ttu-id="eda6a-146">新-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="eda6a-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="eda6a-147">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eda6a-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="eda6a-148">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eda6a-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
