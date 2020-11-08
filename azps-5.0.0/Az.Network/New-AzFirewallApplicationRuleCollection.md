---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139771"
---
# <span data-ttu-id="21564-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="21564-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="21564-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21564-102">SYNOPSIS</span></span>
<span data-ttu-id="21564-103">建立防火牆應用程式規則的集合。</span><span class="sxs-lookup"><span data-stu-id="21564-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="21564-104">句法</span><span class="sxs-lookup"><span data-stu-id="21564-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21564-105">說明</span><span class="sxs-lookup"><span data-stu-id="21564-105">DESCRIPTION</span></span>
<span data-ttu-id="21564-106">**AzFirewallApplicationRuleCollection** Cmdlet 會建立防火牆應用程式規則的集合。</span><span class="sxs-lookup"><span data-stu-id="21564-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="21564-107">示例</span><span class="sxs-lookup"><span data-stu-id="21564-107">EXAMPLES</span></span>

### <span data-ttu-id="21564-108">範例1：使用單一規則建立集合</span><span class="sxs-lookup"><span data-stu-id="21564-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="21564-109">這個範例會使用一條規則建立集合。</span><span class="sxs-lookup"><span data-stu-id="21564-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="21564-110">會允許符合 $rule 1 中所識別之條件的所有流量。</span><span class="sxs-lookup"><span data-stu-id="21564-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="21564-111">第一個規則是針對埠443上的所有 HTTPS 流量（10.0.0.0）。</span><span class="sxs-lookup"><span data-stu-id="21564-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="21564-112">如果有具有較高優先順序的另一個應用程式規則集合 (較小的數位) ，這也會與 $rule 1 中所識別的流量相符，而具有較高優先順序的 rule 集合的動作將會生效。</span><span class="sxs-lookup"><span data-stu-id="21564-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="21564-113">範例2：在規則集合中加入規則</span><span class="sxs-lookup"><span data-stu-id="21564-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="21564-114">這個範例會建立一個含有一個規則的新應用程式規則集合，然後使用規則集合物件上的方法 AddRule，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="21564-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="21564-115">指定規則集合中的每個規則名稱必須具有唯一的名稱，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="21564-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="21564-116">範例3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="21564-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="21564-117">這個範例會建立一個含有一個規則的新應用程式規則集合，然後依名稱取得規則，並在規則集合物件上呼叫方法 GetRuleByName。</span><span class="sxs-lookup"><span data-stu-id="21564-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="21564-118">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="21564-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="21564-119">範例4：從規則集合中移除規則</span><span class="sxs-lookup"><span data-stu-id="21564-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="21564-120">這個範例會建立具有兩個規則的新應用程式規則集合，然後在規則集合物件上呼叫方法 RemoveRuleByName，移除規則集合中的第一個規則。</span><span class="sxs-lookup"><span data-stu-id="21564-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="21564-121">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="21564-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="21564-122">參數</span><span class="sxs-lookup"><span data-stu-id="21564-122">PARAMETERS</span></span>

### <span data-ttu-id="21564-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="21564-123">-ActionType</span></span>
<span data-ttu-id="21564-124">規則集合的動作</span><span class="sxs-lookup"><span data-stu-id="21564-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="21564-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21564-125">-DefaultProfile</span></span>
<span data-ttu-id="21564-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21564-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21564-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="21564-127">-Name</span></span>
<span data-ttu-id="21564-128">指定此應用程式規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="21564-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="21564-129">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="21564-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="21564-130">-優先順序</span><span class="sxs-lookup"><span data-stu-id="21564-130">-Priority</span></span>
<span data-ttu-id="21564-131">指定此規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="21564-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="21564-132">[優先順序] 是介於100和65000之間的數位。</span><span class="sxs-lookup"><span data-stu-id="21564-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="21564-133">數值越小，優先順序就越大。</span><span class="sxs-lookup"><span data-stu-id="21564-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="21564-134">-規則</span><span class="sxs-lookup"><span data-stu-id="21564-134">-Rule</span></span>
<span data-ttu-id="21564-135">指定要在此集合下組成群組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="21564-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21564-136">-確認</span><span class="sxs-lookup"><span data-stu-id="21564-136">-Confirm</span></span>
<span data-ttu-id="21564-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21564-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21564-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21564-138">-WhatIf</span></span>
<span data-ttu-id="21564-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21564-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21564-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21564-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21564-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21564-141">CommonParameters</span></span>
<span data-ttu-id="21564-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21564-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21564-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21564-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21564-144">輸入</span><span class="sxs-lookup"><span data-stu-id="21564-144">INPUTS</span></span>

### <span data-ttu-id="21564-145">所有</span><span class="sxs-lookup"><span data-stu-id="21564-145">None</span></span>

## <span data-ttu-id="21564-146">輸出</span><span class="sxs-lookup"><span data-stu-id="21564-146">OUTPUTS</span></span>

### <span data-ttu-id="21564-147">PSAzureFirewallApplicationRuleCollection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="21564-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="21564-148">筆記</span><span class="sxs-lookup"><span data-stu-id="21564-148">NOTES</span></span>

## <span data-ttu-id="21564-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="21564-149">RELATED LINKS</span></span>

[<span data-ttu-id="21564-150">新-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="21564-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="21564-151">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="21564-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="21564-152">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="21564-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)