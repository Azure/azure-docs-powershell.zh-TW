---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
ms.openlocfilehash: 12b45dd5fd62dabb2650f121f52a539962315513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447349"
---
# <span data-ttu-id="618be-101">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="618be-101">New-AzureRmFirewallNatRuleCollection</span></span>

## <span data-ttu-id="618be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="618be-102">SYNOPSIS</span></span>
<span data-ttu-id="618be-103">建立防火牆 NAT 規則的集合。</span><span class="sxs-lookup"><span data-stu-id="618be-103">Creates a collection of Firewall NAT rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="618be-104">句法</span><span class="sxs-lookup"><span data-stu-id="618be-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="618be-105">說明</span><span class="sxs-lookup"><span data-stu-id="618be-105">DESCRIPTION</span></span>
<span data-ttu-id="618be-106">**新的-AzureRmFirewallNatRuleCollection** Cmdlet 會建立一個防火牆 NAT 規則集合。</span><span class="sxs-lookup"><span data-stu-id="618be-106">The **New-AzureRmFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="618be-107">示例</span><span class="sxs-lookup"><span data-stu-id="618be-107">EXAMPLES</span></span>

### <span data-ttu-id="618be-108">1：使用單一規則建立集合</span><span class="sxs-lookup"><span data-stu-id="618be-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="618be-109">這個範例會使用一條規則建立集合。</span><span class="sxs-lookup"><span data-stu-id="618be-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="618be-110">符合 $rule 1 中所識別之條件的所有通信量都會 DNAT'ed 到已翻譯的位址和埠。</span><span class="sxs-lookup"><span data-stu-id="618be-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="618be-111">2：在規則集合中加入規則</span><span class="sxs-lookup"><span data-stu-id="618be-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="618be-112">這個範例會使用一個規則建立新的 NAT 規則集合，然後使用 rule 集合物件上的方法 AddRule，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="618be-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="618be-113">指定規則集合中的每個規則名稱必須具有唯一的名稱，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="618be-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="618be-114">3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="618be-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="618be-115">這個範例會使用一個規則建立新的 NAT 規則集合，然後依名稱取得規則，並在規則集合物件上呼叫方法 GetRuleByName。</span><span class="sxs-lookup"><span data-stu-id="618be-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="618be-116">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="618be-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="618be-117">4：移除規則集合中的規則</span><span class="sxs-lookup"><span data-stu-id="618be-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="618be-118">這個範例會使用兩個規則建立新的 NAT 規則集合，然後在規則集合物件上呼叫 method RemoveRuleByName，移除規則集合中的第一個規則。</span><span class="sxs-lookup"><span data-stu-id="618be-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="618be-119">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="618be-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="618be-120">參數</span><span class="sxs-lookup"><span data-stu-id="618be-120">PARAMETERS</span></span>

### <span data-ttu-id="618be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618be-121">-DefaultProfile</span></span>
<span data-ttu-id="618be-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="618be-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="618be-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="618be-123">-Name</span></span>
<span data-ttu-id="618be-124">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="618be-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="618be-125">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="618be-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="618be-126">-優先順序</span><span class="sxs-lookup"><span data-stu-id="618be-126">-Priority</span></span>
<span data-ttu-id="618be-127">指定此規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="618be-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="618be-128">[優先順序] 是介於100和65000之間的數位。</span><span class="sxs-lookup"><span data-stu-id="618be-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="618be-129">數值越小，優先順序就越大。</span><span class="sxs-lookup"><span data-stu-id="618be-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="618be-130">-規則</span><span class="sxs-lookup"><span data-stu-id="618be-130">-Rule</span></span>
<span data-ttu-id="618be-131">指定要在此集合下組成群組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="618be-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="618be-132">-確認</span><span class="sxs-lookup"><span data-stu-id="618be-132">-Confirm</span></span>
<span data-ttu-id="618be-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="618be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="618be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618be-134">-WhatIf</span></span>
<span data-ttu-id="618be-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="618be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="618be-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="618be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="618be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618be-137">CommonParameters</span></span>
<span data-ttu-id="618be-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="618be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618be-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="618be-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618be-140">輸入</span><span class="sxs-lookup"><span data-stu-id="618be-140">INPUTS</span></span>

### <span data-ttu-id="618be-141">所有</span><span class="sxs-lookup"><span data-stu-id="618be-141">None</span></span>
<span data-ttu-id="618be-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="618be-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="618be-143">輸出</span><span class="sxs-lookup"><span data-stu-id="618be-143">OUTPUTS</span></span>

### <span data-ttu-id="618be-144">PSFirewallNatRuleCollection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="618be-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRuleCollection</span></span>

## <span data-ttu-id="618be-145">筆記</span><span class="sxs-lookup"><span data-stu-id="618be-145">NOTES</span></span>

## <span data-ttu-id="618be-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="618be-146">RELATED LINKS</span></span>

[<span data-ttu-id="618be-147">新-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="618be-147">New-AzureRmFirewallNatRule</span></span>](./New-AzureRmFirewallNatRule.md)

[<span data-ttu-id="618be-148">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="618be-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="618be-149">AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="618be-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
