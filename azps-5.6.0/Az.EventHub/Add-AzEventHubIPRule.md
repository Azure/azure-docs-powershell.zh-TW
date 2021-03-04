---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 6b01211b7efa20983f868c7e70e54be02d5ad5c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914845"
---
# <span data-ttu-id="13322-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="13322-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="13322-102">簡介</span><span class="sxs-lookup"><span data-stu-id="13322-102">SYNOPSIS</span></span>
<span data-ttu-id="13322-103">新增單一 IP 規則至給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="13322-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="13322-104">語法</span><span class="sxs-lookup"><span data-stu-id="13322-104">SYNTAX</span></span>

### <span data-ttu-id="13322-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="13322-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13322-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13322-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13322-107">描述</span><span class="sxs-lookup"><span data-stu-id="13322-107">DESCRIPTION</span></span>
<span data-ttu-id="13322-108">新增單一 IP 規則至給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="13322-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="13322-109">例子</span><span class="sxs-lookup"><span data-stu-id="13322-109">EXAMPLES</span></span>

### <span data-ttu-id="13322-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="13322-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="13322-111">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/命名空間/Eventhub-命名空間-2389/networkRuleSets/default Type ： Microsoft.Eventhub/命名空間/NetworkRuleSet IpRules ： {11.22.33.44， Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="13322-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="13322-112">將 IPRule 與 IpMask "11.22.33.44" 和 「動作允許」新增為所給命名空間。</span><span class="sxs-lookup"><span data-stu-id="13322-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="13322-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="13322-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="13322-114">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/命名空間/Eventhub-命名空間-2389/networkRuleSets/default Type ： Microsoft.Eventhub/命名空間/NetworkRuleSet IpRules ： {11.22.33.44， Allow} VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="13322-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="13322-115">將 IPRule 與 IpMask "11.22.33.44" 和 「動作允許」新增為所給命名空間。</span><span class="sxs-lookup"><span data-stu-id="13322-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="13322-116">參數</span><span class="sxs-lookup"><span data-stu-id="13322-116">PARAMETERS</span></span>

### <span data-ttu-id="13322-117">-動作</span><span class="sxs-lookup"><span data-stu-id="13322-117">-Action</span></span>
<span data-ttu-id="13322-118">IP 篩選動作</span><span class="sxs-lookup"><span data-stu-id="13322-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="13322-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13322-119">-DefaultProfile</span></span>
<span data-ttu-id="13322-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="13322-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13322-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="13322-121">-IpMask</span></span>
<span data-ttu-id="13322-122">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13322-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="13322-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="13322-123">-IpRuleObject</span></span>
<span data-ttu-id="13322-124">要新增的 IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="13322-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="13322-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="13322-125">-Name</span></span>
<span data-ttu-id="13322-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="13322-126">Namespace Name</span></span>

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

### <span data-ttu-id="13322-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13322-127">-ResourceGroupName</span></span>
<span data-ttu-id="13322-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="13322-128">Resource Group Name</span></span>

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

### <span data-ttu-id="13322-129">-確認</span><span class="sxs-lookup"><span data-stu-id="13322-129">-Confirm</span></span>
<span data-ttu-id="13322-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="13322-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13322-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13322-131">-WhatIf</span></span>
<span data-ttu-id="13322-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13322-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13322-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13322-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13322-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13322-134">CommonParameters</span></span>
<span data-ttu-id="13322-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="13322-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="13322-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="13322-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13322-137">輸入</span><span class="sxs-lookup"><span data-stu-id="13322-137">INPUTS</span></span>

### <span data-ttu-id="13322-138">System.String</span><span class="sxs-lookup"><span data-stu-id="13322-138">System.String</span></span>

### <span data-ttu-id="13322-139">Microsoft.Azure.Commands.EventHub.models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="13322-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="13322-140">輸出</span><span class="sxs-lookup"><span data-stu-id="13322-140">OUTPUTS</span></span>

### <span data-ttu-id="13322-141">Microsoft.Azure.Commands.EventHub.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="13322-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="13322-142">筆記</span><span class="sxs-lookup"><span data-stu-id="13322-142">NOTES</span></span>

## <span data-ttu-id="13322-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="13322-143">RELATED LINKS</span></span>
