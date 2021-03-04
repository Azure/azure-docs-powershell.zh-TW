---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 6b105ab242f9ffb64d1d523cad5930c48714c724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914745"
---
# <span data-ttu-id="87f6b-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="87f6b-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="87f6b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="87f6b-103">在 ManagedRuleSets 中為防火牆原則建立 RuleGroupOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="87f6b-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="87f6b-104">語法</span><span class="sxs-lookup"><span data-stu-id="87f6b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87f6b-105">描述</span><span class="sxs-lookup"><span data-stu-id="87f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="87f6b-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** 會針對防火牆原則在 ManagedRuleSet 中建立 ruleGroupOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="87f6b-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="87f6b-107">例子</span><span class="sxs-lookup"><span data-stu-id="87f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="87f6b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="87f6b-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="87f6b-109">建立 RuleGroupOverride 專案，將組名做為$ruleName規則，$rule 1，$rule 2。</span><span class="sxs-lookup"><span data-stu-id="87f6b-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="87f6b-110">將相同的指派給$overrideEntry</span><span class="sxs-lookup"><span data-stu-id="87f6b-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="87f6b-111">參數</span><span class="sxs-lookup"><span data-stu-id="87f6b-111">PARAMETERS</span></span>

### <span data-ttu-id="87f6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f6b-112">-DefaultProfile</span></span>
<span data-ttu-id="87f6b-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="87f6b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f6b-114">-規則</span><span class="sxs-lookup"><span data-stu-id="87f6b-114">-Rule</span></span>
<span data-ttu-id="87f6b-115">規則清單。</span><span class="sxs-lookup"><span data-stu-id="87f6b-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f6b-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="87f6b-116">-RuleGroupName</span></span>
<span data-ttu-id="87f6b-117">在重寫 RuleGroup 專案指定 ruleGroupName。</span><span class="sxs-lookup"><span data-stu-id="87f6b-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="87f6b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f6b-118">CommonParameters</span></span>
<span data-ttu-id="87f6b-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87f6b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f6b-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87f6b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f6b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="87f6b-121">INPUTS</span></span>

### <span data-ttu-id="87f6b-122">沒有</span><span class="sxs-lookup"><span data-stu-id="87f6b-122">None</span></span>

## <span data-ttu-id="87f6b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="87f6b-123">OUTPUTS</span></span>

### <span data-ttu-id="87f6b-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="87f6b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="87f6b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="87f6b-125">NOTES</span></span>

## <span data-ttu-id="87f6b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="87f6b-126">RELATED LINKS</span></span>
