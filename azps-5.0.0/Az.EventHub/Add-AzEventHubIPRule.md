---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138898"
---
# <span data-ttu-id="f6d3c-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="f6d3c-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="f6d3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d3c-103">在指定命名空間的 NetworkRuleSet 中新增單一 IP 規則</span><span class="sxs-lookup"><span data-stu-id="f6d3c-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f6d3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6d3c-104">SYNTAX</span></span>

### <span data-ttu-id="f6d3c-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f6d3c-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6d3c-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6d3c-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6d3c-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6d3c-107">DESCRIPTION</span></span>
<span data-ttu-id="f6d3c-108">在指定命名空間的 NetworkRuleSet 中新增單一 IP 規則</span><span class="sxs-lookup"><span data-stu-id="f6d3c-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f6d3c-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6d3c-109">EXAMPLES</span></span>

### <span data-ttu-id="f6d3c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f6d3c-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="f6d3c-111">名稱：預設 DefaultAction： Allow Id：/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： {11.22.33.44，Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="f6d3c-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="f6d3c-112">新增具有 IpMask "11.22.33.44" 的 IPRule，並針對指定的命名空間加入動作允許。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="f6d3c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f6d3c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="f6d3c-114">名稱：預設 DefaultAction： Allow Id：/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： {11.22.33.44，Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="f6d3c-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="f6d3c-115">新增具有 IpMask "11.22.33.44" 的 IPRule，並針對指定的命名空間加入動作允許。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="f6d3c-116">參數</span><span class="sxs-lookup"><span data-stu-id="f6d3c-116">PARAMETERS</span></span>

### <span data-ttu-id="f6d3c-117">-動作</span><span class="sxs-lookup"><span data-stu-id="f6d3c-117">-Action</span></span>
<span data-ttu-id="f6d3c-118">IP 篩選器動作</span><span class="sxs-lookup"><span data-stu-id="f6d3c-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="f6d3c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d3c-119">-DefaultProfile</span></span>
<span data-ttu-id="f6d3c-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d3c-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="f6d3c-121">-IpMask</span></span>
<span data-ttu-id="f6d3c-122">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f6d3c-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="f6d3c-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f6d3c-123">-IpRuleObject</span></span>
<span data-ttu-id="f6d3c-124">要新增的 IPRule 設定物件</span><span class="sxs-lookup"><span data-stu-id="f6d3c-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d3c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6d3c-125">-Name</span></span>
<span data-ttu-id="f6d3c-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f6d3c-126">Namespace Name</span></span>

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

### <span data-ttu-id="f6d3c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d3c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f6d3c-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f6d3c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f6d3c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f6d3c-129">-Confirm</span></span>
<span data-ttu-id="f6d3c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6d3c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6d3c-131">-WhatIf</span></span>
<span data-ttu-id="f6d3c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6d3c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6d3c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d3c-134">CommonParameters</span></span>
<span data-ttu-id="f6d3c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f6d3c-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6d3c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d3c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f6d3c-137">INPUTS</span></span>

### <span data-ttu-id="f6d3c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f6d3c-138">System.String</span></span>

### <span data-ttu-id="f6d3c-139">PSNWRuleSetIpRulesAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6d3c-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="f6d3c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f6d3c-140">OUTPUTS</span></span>

### <span data-ttu-id="f6d3c-141">PSNetworkRuleSetAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6d3c-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f6d3c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f6d3c-142">NOTES</span></span>

## <span data-ttu-id="f6d3c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6d3c-143">RELATED LINKS</span></span>