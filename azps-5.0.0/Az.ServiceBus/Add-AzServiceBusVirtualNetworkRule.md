---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 3ff1f64bf65a4474dc9f47aa6bd419c442b49698
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286216"
---
# <span data-ttu-id="c0a15-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c0a15-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="c0a15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0a15-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a15-103">針對指定的命名空間新增單一 VirtualNetworkRule 至 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0a15-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="c0a15-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0a15-104">SYNTAX</span></span>

### <span data-ttu-id="c0a15-105">VirtualNetworkRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0a15-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0a15-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0a15-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0a15-107">說明</span><span class="sxs-lookup"><span data-stu-id="c0a15-107">DESCRIPTION</span></span>
<span data-ttu-id="c0a15-108">針對指定的命名空間新增單一 VirtualNetworkRule 至 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0a15-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="c0a15-109">示例</span><span class="sxs-lookup"><span data-stu-id="c0a15-109">EXAMPLES</span></span>

### <span data-ttu-id="c0a15-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c0a15-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="c0a15-111">名稱：預設 DefaultAction： Allow Id：/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型： NetworkRuleSet = IpRules/命名空間/： VirtualNetworkRules： {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，False}</span><span class="sxs-lookup"><span data-stu-id="c0a15-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c0a15-112">針對指定的命名空間，將指定的子網與 IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) 新增至 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0a15-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="c0a15-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c0a15-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="c0a15-114">名稱：預設 DefaultAction： Allow Id：/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型： NetworkRuleSet = IpRules/命名空間/： VirtualNetworkRules： {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，False}</span><span class="sxs-lookup"><span data-stu-id="c0a15-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c0a15-115">針對指定的命名空間，將 $virtualruleset 1 新增至 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0a15-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="c0a15-116">參數</span><span class="sxs-lookup"><span data-stu-id="c0a15-116">PARAMETERS</span></span>

### <span data-ttu-id="c0a15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a15-117">-DefaultProfile</span></span>
<span data-ttu-id="c0a15-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0a15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a15-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0a15-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c0a15-120">子網的 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="c0a15-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="c0a15-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0a15-121">-Name</span></span>
<span data-ttu-id="c0a15-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c0a15-122">Namespace Name</span></span>

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

### <span data-ttu-id="c0a15-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a15-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0a15-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c0a15-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c0a15-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c0a15-125">-SubnetId</span></span>
<span data-ttu-id="c0a15-126">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c0a15-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="c0a15-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c0a15-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="c0a15-128">VirtualNetworkRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="c0a15-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="c0a15-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c0a15-129">-Confirm</span></span>
<span data-ttu-id="c0a15-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0a15-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0a15-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a15-131">-WhatIf</span></span>
<span data-ttu-id="c0a15-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0a15-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0a15-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0a15-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0a15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a15-134">CommonParameters</span></span>
<span data-ttu-id="c0a15-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0a15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c0a15-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0a15-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a15-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c0a15-137">INPUTS</span></span>

### <span data-ttu-id="c0a15-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c0a15-138">System.String</span></span>

### <span data-ttu-id="c0a15-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="c0a15-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c0a15-140">PSNWRuleSetVirtualNetworkRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0a15-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="c0a15-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c0a15-141">OUTPUTS</span></span>

### <span data-ttu-id="c0a15-142">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0a15-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="c0a15-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c0a15-143">NOTES</span></span>

## <span data-ttu-id="c0a15-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0a15-144">RELATED LINKS</span></span>