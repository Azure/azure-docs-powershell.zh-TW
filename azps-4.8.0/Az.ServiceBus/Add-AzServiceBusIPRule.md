---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970188"
---
# <span data-ttu-id="ae028-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="ae028-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="ae028-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae028-102">SYNOPSIS</span></span>
<span data-ttu-id="ae028-103">在指定命名空間的 NetworkRuleSet 中新增單一 IP 規則</span><span class="sxs-lookup"><span data-stu-id="ae028-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ae028-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae028-104">SYNTAX</span></span>

### <span data-ttu-id="ae028-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae028-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae028-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae028-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae028-107">說明</span><span class="sxs-lookup"><span data-stu-id="ae028-107">DESCRIPTION</span></span>
<span data-ttu-id="ae028-108">在指定命名空間的 NetworkRuleSet 中新增單一 IP 規則</span><span class="sxs-lookup"><span data-stu-id="ae028-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ae028-109">示例</span><span class="sxs-lookup"><span data-stu-id="ae028-109">EXAMPLES</span></span>

### <span data-ttu-id="ae028-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ae028-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="ae028-111">名稱：預設 DefaultAction： Allow Id：/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default 類型： NetworkRuleSet = IpRules/命名空間/： {11.22.33.44，Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="ae028-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="ae028-112">新增具有 IpMask "11.22.33.44" 的 IPRule，並針對指定的命名空間進行動作允許。</span><span class="sxs-lookup"><span data-stu-id="ae028-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="ae028-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ae028-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="ae028-114">名稱：預設 DefaultAction： Allow Id：/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default 類型： NetworkRuleSet = IpRules/命名空間/： {11.22.33.44，Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="ae028-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="ae028-115">新增具有 IpMask "11.22.33.44" 的 IPRule，並針對指定的命名空間進行動作允許。</span><span class="sxs-lookup"><span data-stu-id="ae028-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="ae028-116">參數</span><span class="sxs-lookup"><span data-stu-id="ae028-116">PARAMETERS</span></span>

### <span data-ttu-id="ae028-117">-動作</span><span class="sxs-lookup"><span data-stu-id="ae028-117">-Action</span></span>
<span data-ttu-id="ae028-118">IP 篩選器動作</span><span class="sxs-lookup"><span data-stu-id="ae028-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="ae028-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae028-119">-DefaultProfile</span></span>
<span data-ttu-id="ae028-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae028-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae028-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="ae028-121">-IpMask</span></span>
<span data-ttu-id="ae028-122">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ae028-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="ae028-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ae028-123">-IpRuleObject</span></span>
<span data-ttu-id="ae028-124">要新增的 IPRule 設定物件</span><span class="sxs-lookup"><span data-stu-id="ae028-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="ae028-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae028-125">-Name</span></span>
<span data-ttu-id="ae028-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="ae028-126">Namespace Name</span></span>

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

### <span data-ttu-id="ae028-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae028-127">-ResourceGroupName</span></span>
<span data-ttu-id="ae028-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ae028-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ae028-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ae028-129">-Confirm</span></span>
<span data-ttu-id="ae028-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae028-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae028-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae028-131">-WhatIf</span></span>
<span data-ttu-id="ae028-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae028-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae028-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae028-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae028-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae028-134">CommonParameters</span></span>
<span data-ttu-id="ae028-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae028-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae028-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae028-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae028-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ae028-137">INPUTS</span></span>

### <span data-ttu-id="ae028-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ae028-138">System.String</span></span>

### <span data-ttu-id="ae028-139">PSNWRuleSetIpRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae028-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="ae028-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ae028-140">OUTPUTS</span></span>

### <span data-ttu-id="ae028-141">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae028-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ae028-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ae028-142">NOTES</span></span>

## <span data-ttu-id="ae028-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae028-143">RELATED LINKS</span></span>