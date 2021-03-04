---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: c82b150dd10a293bda1a001e4b930bcc2fe7989b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917681"
---
# <span data-ttu-id="76631-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="76631-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="76631-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76631-102">SYNOPSIS</span></span>
<span data-ttu-id="76631-103">建立防火牆應用程式規則的集合。</span><span class="sxs-lookup"><span data-stu-id="76631-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="76631-104">語法</span><span class="sxs-lookup"><span data-stu-id="76631-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76631-105">描述</span><span class="sxs-lookup"><span data-stu-id="76631-105">DESCRIPTION</span></span>
<span data-ttu-id="76631-106">**New-AzFirewallApplicationRuleCollection** Cmdlet 會建立防火牆應用程式規則的集合。</span><span class="sxs-lookup"><span data-stu-id="76631-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="76631-107">例子</span><span class="sxs-lookup"><span data-stu-id="76631-107">EXAMPLES</span></span>

### <span data-ttu-id="76631-108">範例 1：使用一個規則建立集合</span><span class="sxs-lookup"><span data-stu-id="76631-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="76631-109">此範例會建立包含一個規則的集合。</span><span class="sxs-lookup"><span data-stu-id="76631-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="76631-110">允許所有符合 $rule 1 中識別條件的流量。</span><span class="sxs-lookup"><span data-stu-id="76631-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="76631-111">第一個規則是針對埠 443 上 10.0.0.0 的所有 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="76631-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="76631-112">如果有另一個優先順序較高的應用程式規則集合 (較小的數位) 也符合 $rule 1 中識別的流量，則優先順序較高的規則集合動作會改為生效。</span><span class="sxs-lookup"><span data-stu-id="76631-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="76631-113">範例 2：新增規則至規則集合</span><span class="sxs-lookup"><span data-stu-id="76631-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="76631-114">此範例會使用一個規則建立新應用程式規則集合，然後使用規則集合物件上的 AddRule 方法，將第二個規則新增到規則集合。</span><span class="sxs-lookup"><span data-stu-id="76631-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="76631-115">指定規則集合中的每個規則名稱都必須有唯一的名稱，而且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="76631-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="76631-116">範例 3：從規則集合取得規則</span><span class="sxs-lookup"><span data-stu-id="76631-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="76631-117">此範例會使用一個規則建立新應用程式規則集合，然後依名稱取得規則，即規則集合物件上的呼叫方法 GetRuleByName。</span><span class="sxs-lookup"><span data-stu-id="76631-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="76631-118">方法 GetRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="76631-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="76631-119">範例 4：從規則集合移除規則</span><span class="sxs-lookup"><span data-stu-id="76631-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="76631-120">此範例會建立一個包含兩個規則的新應用程式規則集合，然後呼叫規則集合物件上的 RemoveRuleByName，從規則集合移除第一個規則。</span><span class="sxs-lookup"><span data-stu-id="76631-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="76631-121">方法 RemoveRuleByName 的規則名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="76631-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="76631-122">參數</span><span class="sxs-lookup"><span data-stu-id="76631-122">PARAMETERS</span></span>

### <span data-ttu-id="76631-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="76631-123">-ActionType</span></span>
<span data-ttu-id="76631-124">規則集合的動作</span><span class="sxs-lookup"><span data-stu-id="76631-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="76631-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76631-125">-DefaultProfile</span></span>
<span data-ttu-id="76631-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76631-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76631-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="76631-127">-Name</span></span>
<span data-ttu-id="76631-128">指定此應用程式規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="76631-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="76631-129">名稱必須在規則集合中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="76631-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="76631-130">-優先順序</span><span class="sxs-lookup"><span data-stu-id="76631-130">-Priority</span></span>
<span data-ttu-id="76631-131">指定此規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="76631-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="76631-132">優先順序是介於 100 到 65000 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="76631-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="76631-133">數位越小，優先順序越大。</span><span class="sxs-lookup"><span data-stu-id="76631-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="76631-134">-規則</span><span class="sxs-lookup"><span data-stu-id="76631-134">-Rule</span></span>
<span data-ttu-id="76631-135">指定此集合下要分組的規則清單。</span><span class="sxs-lookup"><span data-stu-id="76631-135">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="76631-136">-確認</span><span class="sxs-lookup"><span data-stu-id="76631-136">-Confirm</span></span>
<span data-ttu-id="76631-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76631-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76631-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76631-138">-WhatIf</span></span>
<span data-ttu-id="76631-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76631-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76631-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76631-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76631-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76631-141">CommonParameters</span></span>
<span data-ttu-id="76631-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76631-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76631-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="76631-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76631-144">輸入</span><span class="sxs-lookup"><span data-stu-id="76631-144">INPUTS</span></span>

### <span data-ttu-id="76631-145">沒有</span><span class="sxs-lookup"><span data-stu-id="76631-145">None</span></span>

## <span data-ttu-id="76631-146">輸出</span><span class="sxs-lookup"><span data-stu-id="76631-146">OUTPUTS</span></span>

### <span data-ttu-id="76631-147">Microsoft.Azure.Commands.Network.models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="76631-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="76631-148">筆記</span><span class="sxs-lookup"><span data-stu-id="76631-148">NOTES</span></span>

## <span data-ttu-id="76631-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="76631-149">RELATED LINKS</span></span>

[<span data-ttu-id="76631-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="76631-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="76631-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="76631-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="76631-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="76631-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
