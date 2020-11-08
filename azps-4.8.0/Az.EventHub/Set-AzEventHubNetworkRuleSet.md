---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969726"
---
# <span data-ttu-id="ba6e2-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba6e2-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="ba6e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6e2-103">更新目前 Azure 訂閱中指定命名空間的 NetworkruleSet。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ba6e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba6e2-104">SYNTAX</span></span>

### <span data-ttu-id="ba6e2-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ba6e2-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba6e2-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba6e2-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba6e2-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6e2-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba6e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="ba6e2-108">DESCRIPTION</span></span>
<span data-ttu-id="ba6e2-109">更新目前 Azure 訂閱中指定命名空間的 NetworkruleSet。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ba6e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="ba6e2-110">EXAMPLES</span></span>

### <span data-ttu-id="ba6e2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ba6e2-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="ba6e2-112">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： {4.4.4.4、Allow、3.3.3.3、Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，True}</span><span class="sxs-lookup"><span data-stu-id="ba6e2-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ba6e2-113">使用-IPRule 和-VirtualNetworkRule 參數更新 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba6e2-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="ba6e2-114">範例2</span><span class="sxs-lookup"><span data-stu-id="ba6e2-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="ba6e2-115">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： {4.4.4.4、Allow、3.3.3.3、Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，True}</span><span class="sxs-lookup"><span data-stu-id="ba6e2-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ba6e2-116">使用-InputObject 來更新 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba6e2-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="ba6e2-117">範例3</span><span class="sxs-lookup"><span data-stu-id="ba6e2-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="ba6e2-118">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： {4.4.4.4、Allow、3.3.3.3、Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，True}</span><span class="sxs-lookup"><span data-stu-id="ba6e2-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ba6e2-119">更新其他命名空間的 NetworkRuleSet 使用方式。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="ba6e2-120">參數</span><span class="sxs-lookup"><span data-stu-id="ba6e2-120">PARAMETERS</span></span>

### <span data-ttu-id="ba6e2-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ba6e2-121">-DefaultAction</span></span>
<span data-ttu-id="ba6e2-122">NetworkRuleSet 的預設動作</span><span class="sxs-lookup"><span data-stu-id="ba6e2-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="ba6e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6e2-123">-DefaultProfile</span></span>
<span data-ttu-id="ba6e2-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba6e2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba6e2-125">-InputObject</span></span>
<span data-ttu-id="ba6e2-126">NetworkruleSet Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="ba6e2-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e2-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ba6e2-127">-IPRule</span></span>
<span data-ttu-id="ba6e2-128">IPRuleSet 清單</span><span class="sxs-lookup"><span data-stu-id="ba6e2-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e2-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba6e2-129">-Name</span></span>
<span data-ttu-id="ba6e2-130">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="ba6e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="ba6e2-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba6e2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba6e2-133">-ResourceId</span></span>
<span data-ttu-id="ba6e2-134">命名空間的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ba6e2-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="ba6e2-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="ba6e2-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="ba6e2-136">指出是否已啟用 TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="ba6e2-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e2-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ba6e2-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="ba6e2-138">VirtualNetworkRules 清單</span><span class="sxs-lookup"><span data-stu-id="ba6e2-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e2-139">-確認</span><span class="sxs-lookup"><span data-stu-id="ba6e2-139">-Confirm</span></span>
<span data-ttu-id="ba6e2-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6e2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6e2-141">-WhatIf</span></span>
<span data-ttu-id="ba6e2-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6e2-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6e2-144">CommonParameters</span></span>
<span data-ttu-id="ba6e2-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ba6e2-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba6e2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6e2-147">輸入</span><span class="sxs-lookup"><span data-stu-id="ba6e2-147">INPUTS</span></span>

### <span data-ttu-id="ba6e2-148">PSNetworkRuleSetAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="ba6e2-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="ba6e2-149">System.object</span><span class="sxs-lookup"><span data-stu-id="ba6e2-149">System.String</span></span>

## <span data-ttu-id="ba6e2-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ba6e2-150">OUTPUTS</span></span>

### <span data-ttu-id="ba6e2-151">PSNetworkRuleSetAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="ba6e2-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ba6e2-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ba6e2-152">NOTES</span></span>

## <span data-ttu-id="ba6e2-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba6e2-153">RELATED LINKS</span></span>