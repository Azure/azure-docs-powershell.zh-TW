---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284744"
---
# <span data-ttu-id="49a8b-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="49a8b-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="49a8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="49a8b-103">更新目前 Azure 訂閱中指定命名空間的 NetworkruleSet。</span><span class="sxs-lookup"><span data-stu-id="49a8b-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="49a8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="49a8b-104">SYNTAX</span></span>

### <span data-ttu-id="49a8b-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="49a8b-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a8b-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49a8b-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49a8b-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49a8b-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a8b-108">說明</span><span class="sxs-lookup"><span data-stu-id="49a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="49a8b-109">更新目前 Azure 訂閱中指定命名空間的 NetwrokruleSet。</span><span class="sxs-lookup"><span data-stu-id="49a8b-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="49a8b-110">示例</span><span class="sxs-lookup"><span data-stu-id="49a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="49a8b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="49a8b-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="49a8b-112">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型：/命名空間/NetworkRuleSet IpRules： {4.4.4.4，Allow、3.3.3.3、Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，True}</span><span class="sxs-lookup"><span data-stu-id="49a8b-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="49a8b-113">使用-IPRule 和-VirtualNetworkRule 參數更新 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="49a8b-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="49a8b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="49a8b-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="49a8b-115">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型：/命名空間/NetworkRuleSet IpRules： {4.4.4.4，Allow、3.3.3.3、Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，True}</span><span class="sxs-lookup"><span data-stu-id="49a8b-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="49a8b-116">使用-InputObject 來更新 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="49a8b-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="49a8b-117">範例3</span><span class="sxs-lookup"><span data-stu-id="49a8b-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="49a8b-118">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型：/命名空間/NetworkRuleSet IpRules： {4.4.4.4，Allow、3.3.3.3、Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，True}</span><span class="sxs-lookup"><span data-stu-id="49a8b-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="49a8b-119">更新其他命名空間的 NetworkRuleSet 使用方式。</span><span class="sxs-lookup"><span data-stu-id="49a8b-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="49a8b-120">參數</span><span class="sxs-lookup"><span data-stu-id="49a8b-120">PARAMETERS</span></span>

### <span data-ttu-id="49a8b-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="49a8b-121">-DefaultAction</span></span>
<span data-ttu-id="49a8b-122">NetworkRuleSet 的預設動作</span><span class="sxs-lookup"><span data-stu-id="49a8b-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a8b-123">-DefaultProfile</span></span>
<span data-ttu-id="49a8b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49a8b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a8b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49a8b-125">-InputObject</span></span>
<span data-ttu-id="49a8b-126">NetworkruleSet Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="49a8b-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="49a8b-127">-IPRule</span></span>
<span data-ttu-id="49a8b-128">IPRuleSet 清單</span><span class="sxs-lookup"><span data-stu-id="49a8b-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="49a8b-129">-Name</span></span>
<span data-ttu-id="49a8b-130">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="49a8b-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a8b-131">-ResourceGroupName</span></span>
<span data-ttu-id="49a8b-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="49a8b-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49a8b-133">-ResourceId</span></span>
<span data-ttu-id="49a8b-134">命名空間的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="49a8b-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="49a8b-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="49a8b-136">VirtualNetworkRules 清單</span><span class="sxs-lookup"><span data-stu-id="49a8b-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a8b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="49a8b-137">-Confirm</span></span>
<span data-ttu-id="49a8b-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49a8b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a8b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a8b-139">-WhatIf</span></span>
<span data-ttu-id="49a8b-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49a8b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a8b-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49a8b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a8b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a8b-142">CommonParameters</span></span>
<span data-ttu-id="49a8b-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49a8b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49a8b-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49a8b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a8b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="49a8b-145">INPUTS</span></span>

### <span data-ttu-id="49a8b-146">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49a8b-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="49a8b-147">System.object</span><span class="sxs-lookup"><span data-stu-id="49a8b-147">System.String</span></span>

## <span data-ttu-id="49a8b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="49a8b-148">OUTPUTS</span></span>

### <span data-ttu-id="49a8b-149">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49a8b-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="49a8b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="49a8b-150">NOTES</span></span>

## <span data-ttu-id="49a8b-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="49a8b-151">RELATED LINKS</span></span>