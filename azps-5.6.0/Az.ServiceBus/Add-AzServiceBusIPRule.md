---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: e0450df003b474cae57319d5450423af58f4d3eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905821"
---
# <span data-ttu-id="57aef-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="57aef-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="57aef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57aef-102">SYNOPSIS</span></span>
<span data-ttu-id="57aef-103">新增單一 IP 規則至給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="57aef-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="57aef-104">語法</span><span class="sxs-lookup"><span data-stu-id="57aef-104">SYNTAX</span></span>

### <span data-ttu-id="57aef-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57aef-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57aef-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57aef-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57aef-107">描述</span><span class="sxs-lookup"><span data-stu-id="57aef-107">DESCRIPTION</span></span>
<span data-ttu-id="57aef-108">新增單一 IP 規則至給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="57aef-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="57aef-109">例子</span><span class="sxs-lookup"><span data-stu-id="57aef-109">EXAMPLES</span></span>

### <span data-ttu-id="57aef-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="57aef-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="57aef-111">名稱： default DefaultAction ： Allow Id ： /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-2389/networkRuleSets/default Type： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules ： {11.22.33.44， Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="57aef-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="57aef-112">使用 IpMask "11.22.33.44" 新增 IPRule，並新增 「動作允許」以取代所給予的命名空間。</span><span class="sxs-lookup"><span data-stu-id="57aef-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="57aef-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="57aef-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="57aef-114">名稱： default DefaultAction ： Allow Id ： /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-2389/networkRuleSets/default Type： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules ： {11.22.33.44， Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="57aef-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="57aef-115">使用 IpMask "11.22.33.44" 新增 IPRule，並新增 「動作允許」以取代所給予的命名空間。</span><span class="sxs-lookup"><span data-stu-id="57aef-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="57aef-116">參數</span><span class="sxs-lookup"><span data-stu-id="57aef-116">PARAMETERS</span></span>

### <span data-ttu-id="57aef-117">-動作</span><span class="sxs-lookup"><span data-stu-id="57aef-117">-Action</span></span>
<span data-ttu-id="57aef-118">IP 篩選動作</span><span class="sxs-lookup"><span data-stu-id="57aef-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57aef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57aef-119">-DefaultProfile</span></span>
<span data-ttu-id="57aef-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57aef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57aef-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="57aef-121">-IpMask</span></span>
<span data-ttu-id="57aef-122">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="57aef-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57aef-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="57aef-123">-IpRuleObject</span></span>
<span data-ttu-id="57aef-124">要新增的 IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="57aef-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57aef-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="57aef-125">-Name</span></span>
<span data-ttu-id="57aef-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="57aef-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57aef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57aef-127">-ResourceGroupName</span></span>
<span data-ttu-id="57aef-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="57aef-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57aef-129">-確認</span><span class="sxs-lookup"><span data-stu-id="57aef-129">-Confirm</span></span>
<span data-ttu-id="57aef-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57aef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57aef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57aef-131">-WhatIf</span></span>
<span data-ttu-id="57aef-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57aef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57aef-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57aef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57aef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57aef-134">CommonParameters</span></span>
<span data-ttu-id="57aef-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57aef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="57aef-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="57aef-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57aef-137">輸入</span><span class="sxs-lookup"><span data-stu-id="57aef-137">INPUTS</span></span>

### <span data-ttu-id="57aef-138">System.String</span><span class="sxs-lookup"><span data-stu-id="57aef-138">System.String</span></span>

### <span data-ttu-id="57aef-139">Microsoft.Azure.Commands.ServiceBus.models.PSNWRuleSetipRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="57aef-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="57aef-140">輸出</span><span class="sxs-lookup"><span data-stu-id="57aef-140">OUTPUTS</span></span>

### <span data-ttu-id="57aef-141">Microsoft.Azure.Commands.ServiceBus.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="57aef-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="57aef-142">筆記</span><span class="sxs-lookup"><span data-stu-id="57aef-142">NOTES</span></span>

## <span data-ttu-id="57aef-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="57aef-143">RELATED LINKS</span></span>