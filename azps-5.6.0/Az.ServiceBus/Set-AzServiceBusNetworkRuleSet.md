---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 72fd6da6c0abc6419acf3917ebe43fda0fdcfa2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909334"
---
# <span data-ttu-id="de2c0-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="de2c0-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="de2c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="de2c0-103">更新目前 Azure 訂閱中給定命名空間的 NetworkruleSet。</span><span class="sxs-lookup"><span data-stu-id="de2c0-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="de2c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="de2c0-104">SYNTAX</span></span>

### <span data-ttu-id="de2c0-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="de2c0-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de2c0-106">NetruleRuleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="de2c0-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de2c0-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de2c0-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de2c0-108">描述</span><span class="sxs-lookup"><span data-stu-id="de2c0-108">DESCRIPTION</span></span>
<span data-ttu-id="de2c0-109">更新目前 Azure 訂閱中給定命名空間的 NetruleSet。</span><span class="sxs-lookup"><span data-stu-id="de2c0-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="de2c0-110">例子</span><span class="sxs-lookup"><span data-stu-id="de2c0-110">EXAMPLES</span></span>

### <span data-ttu-id="de2c0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="de2c0-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="de2c0-112">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourcegroups/resourceGroup/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-1122/networkRuleSets/default Type ： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules ： {4.4.4.4， Allow， 3.3.3， Allow} VirtualNetworkRules ： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/子網/default， True}</span><span class="sxs-lookup"><span data-stu-id="de2c0-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="de2c0-113">使用 -IPRule 和 -VirtualNetworkRule 參數更新 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="de2c0-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="de2c0-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="de2c0-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="de2c0-115">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourcegroups/resourceGroup/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-1122/networkRuleSets/default Type ： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules ： {4.4.4.4， Allow， 3.3.3， Allow} VirtualNetworkRules ： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/子網/default， True}</span><span class="sxs-lookup"><span data-stu-id="de2c0-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="de2c0-116">使用 -InputObject 更新 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="de2c0-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="de2c0-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="de2c0-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="de2c0-118">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourcegroups/resourceGroup/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-1122/networkRuleSets/default Type ： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules ： {4.4.4.4， Allow， 3.3.3， Allow} VirtualNetworkRules ： {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/子網/default， True}</span><span class="sxs-lookup"><span data-stu-id="de2c0-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="de2c0-119">使用另一個命名空間的 -ResourceId 更新 NetworkRuleSet。</span><span class="sxs-lookup"><span data-stu-id="de2c0-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="de2c0-120">參數</span><span class="sxs-lookup"><span data-stu-id="de2c0-120">PARAMETERS</span></span>

### <span data-ttu-id="de2c0-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="de2c0-121">-DefaultAction</span></span>
<span data-ttu-id="de2c0-122">NetworkRuleSet 的預設動作</span><span class="sxs-lookup"><span data-stu-id="de2c0-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="de2c0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2c0-123">-DefaultProfile</span></span>
<span data-ttu-id="de2c0-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de2c0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de2c0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de2c0-125">-InputObject</span></span>
<span data-ttu-id="de2c0-126">NetworkruleSet Configuration Object</span><span class="sxs-lookup"><span data-stu-id="de2c0-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="de2c0-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="de2c0-127">-IPRule</span></span>
<span data-ttu-id="de2c0-128">IPRuleSet 清單</span><span class="sxs-lookup"><span data-stu-id="de2c0-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="de2c0-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="de2c0-129">-Name</span></span>
<span data-ttu-id="de2c0-130">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="de2c0-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="de2c0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2c0-131">-ResourceGroupName</span></span>
<span data-ttu-id="de2c0-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="de2c0-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="de2c0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de2c0-133">-ResourceId</span></span>
<span data-ttu-id="de2c0-134">命名空間的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="de2c0-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="de2c0-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="de2c0-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="de2c0-136">VirtualNetworkRules 清單</span><span class="sxs-lookup"><span data-stu-id="de2c0-136">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="de2c0-137">-確認</span><span class="sxs-lookup"><span data-stu-id="de2c0-137">-Confirm</span></span>
<span data-ttu-id="de2c0-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de2c0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de2c0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de2c0-139">-WhatIf</span></span>
<span data-ttu-id="de2c0-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de2c0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de2c0-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de2c0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de2c0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2c0-142">CommonParameters</span></span>
<span data-ttu-id="de2c0-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de2c0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="de2c0-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="de2c0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2c0-145">輸入</span><span class="sxs-lookup"><span data-stu-id="de2c0-145">INPUTS</span></span>

### <span data-ttu-id="de2c0-146">Microsoft.Azure.Commands.ServiceBus.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="de2c0-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="de2c0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="de2c0-147">System.String</span></span>

## <span data-ttu-id="de2c0-148">輸出</span><span class="sxs-lookup"><span data-stu-id="de2c0-148">OUTPUTS</span></span>

### <span data-ttu-id="de2c0-149">Microsoft.Azure.Commands.ServiceBus.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="de2c0-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="de2c0-150">筆記</span><span class="sxs-lookup"><span data-stu-id="de2c0-150">NOTES</span></span>

## <span data-ttu-id="de2c0-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="de2c0-151">RELATED LINKS</span></span>