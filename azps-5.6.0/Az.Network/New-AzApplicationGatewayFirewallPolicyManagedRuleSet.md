---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: d8cb1e6f36433168d830c79c2bcbf8b5c259cf32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904594"
---
# <span data-ttu-id="ee65e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee65e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="ee65e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee65e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee65e-103">為防火牆策略建立 ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee65e-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="ee65e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee65e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee65e-105">描述</span><span class="sxs-lookup"><span data-stu-id="ee65e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee65e-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleSet** 會建立防火牆原則的受管理規則。</span><span class="sxs-lookup"><span data-stu-id="ee65e-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="ee65e-107">例子</span><span class="sxs-lookup"><span data-stu-id="ee65e-107">EXAMPLES</span></span>

### <span data-ttu-id="ee65e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ee65e-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="ee65e-109">使用 ruleSetType 建立 ManagedRuleSet 做為 $ruleSetType，ruleSetVersion 為 $ruleSetVersion，RuleGroupOverrides 為清單，包含 $ruleGroupOverride 1，$ruleGroupOverride 2 新的 ManagedRuleSet 會指派給 $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee65e-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="ee65e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ee65e-110">PARAMETERS</span></span>

### <span data-ttu-id="ee65e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee65e-111">-DefaultProfile</span></span>
<span data-ttu-id="ee65e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee65e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee65e-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ee65e-113">-RuleGroupOverride</span></span>
<span data-ttu-id="ee65e-114">規則群組會進行重寫。</span><span class="sxs-lookup"><span data-stu-id="ee65e-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee65e-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="ee65e-115">-RuleSetType</span></span>
<span data-ttu-id="ee65e-116">指定 ManagedRuleSet 中的 RuleSetType</span><span class="sxs-lookup"><span data-stu-id="ee65e-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="ee65e-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="ee65e-117">-RuleSetVersion</span></span>
<span data-ttu-id="ee65e-118">指定 ManagedRuleSet 中的 RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="ee65e-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="ee65e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee65e-119">CommonParameters</span></span>
<span data-ttu-id="ee65e-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee65e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee65e-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee65e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee65e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ee65e-122">INPUTS</span></span>

### <span data-ttu-id="ee65e-123">沒有</span><span class="sxs-lookup"><span data-stu-id="ee65e-123">None</span></span>

## <span data-ttu-id="ee65e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ee65e-124">OUTPUTS</span></span>

### <span data-ttu-id="ee65e-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee65e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="ee65e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ee65e-126">NOTES</span></span>

## <span data-ttu-id="ee65e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee65e-127">RELATED LINKS</span></span>
