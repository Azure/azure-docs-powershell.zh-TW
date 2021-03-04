---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: e4bb2a3020ba2e07fca065f1f70f9d6b4fadee6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916361"
---
# <span data-ttu-id="4b3b9-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b3b9-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="4b3b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3b9-103">為給定命名空間新增單一 VirtualNetworkRule 到 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b3b9-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="4b3b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b3b9-104">SYNTAX</span></span>

### <span data-ttu-id="4b3b9-105">VirtualNetworkRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4b3b9-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b3b9-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b3b9-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b3b9-107">描述</span><span class="sxs-lookup"><span data-stu-id="4b3b9-107">DESCRIPTION</span></span>
<span data-ttu-id="4b3b9-108">為給定命名空間新增單一 VirtualNetworkRule 到 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b3b9-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="4b3b9-109">例子</span><span class="sxs-lookup"><span data-stu-id="4b3b9-109">EXAMPLES</span></span>

### <span data-ttu-id="4b3b9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="4b3b9-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="4b3b9-111">名稱 ：預設 DefaultAction ： Allow Id ： /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-1122/networkRuleSets/default Type ： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules ： {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/子網/default， False}</span><span class="sxs-lookup"><span data-stu-id="4b3b9-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="4b3b9-112">將給定子網和 IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) 新加入到給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b3b9-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="4b3b9-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="4b3b9-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="4b3b9-114">名稱 ：預設 DefaultAction ： Allow Id ： /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-1122/networkRuleSets/default Type ： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules ： {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/子網/default， False}</span><span class="sxs-lookup"><span data-stu-id="4b3b9-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="4b3b9-115">將 $virtualruleset 1 新增到給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b3b9-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="4b3b9-116">參數</span><span class="sxs-lookup"><span data-stu-id="4b3b9-116">PARAMETERS</span></span>

### <span data-ttu-id="4b3b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3b9-117">-DefaultProfile</span></span>
<span data-ttu-id="4b3b9-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b3b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b3b9-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b3b9-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4b3b9-120">子網的 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="4b3b9-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3b9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b3b9-121">-Name</span></span>
<span data-ttu-id="4b3b9-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="4b3b9-122">Namespace Name</span></span>

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

### <span data-ttu-id="4b3b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b3b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b3b9-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="4b3b9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4b3b9-125">-子網Id</span><span class="sxs-lookup"><span data-stu-id="4b3b9-125">-SubnetId</span></span>
<span data-ttu-id="4b3b9-126">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4b3b9-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b3b9-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="4b3b9-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="4b3b9-128">VirtualNetworkRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="4b3b9-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b3b9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4b3b9-129">-Confirm</span></span>
<span data-ttu-id="4b3b9-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4b3b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b3b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b3b9-131">-WhatIf</span></span>
<span data-ttu-id="4b3b9-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b3b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b3b9-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b3b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b3b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3b9-134">CommonParameters</span></span>
<span data-ttu-id="4b3b9-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b3b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4b3b9-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4b3b9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3b9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4b3b9-137">INPUTS</span></span>

### <span data-ttu-id="4b3b9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4b3b9-138">System.String</span></span>

### <span data-ttu-id="4b3b9-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b3b9-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4b3b9-140">Microsoft.Azure.Commands.ServiceBus.models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4b3b9-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="4b3b9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4b3b9-141">OUTPUTS</span></span>

### <span data-ttu-id="4b3b9-142">Microsoft.Azure.Commands.ServiceBus.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="4b3b9-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="4b3b9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4b3b9-143">NOTES</span></span>

## <span data-ttu-id="4b3b9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b3b9-144">RELATED LINKS</span></span>