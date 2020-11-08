---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135840"
---
# <span data-ttu-id="cf4f2-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cf4f2-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="cf4f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4f2-103">在 ManagedRuleSets 中針對防火牆原則建立 RuleGroupOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="cf4f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf4f2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf4f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="cf4f2-106">**新的-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** 會在防火牆原則的 managedRuleSet 中建立 ruleGroupOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="cf4f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="cf4f2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cf4f2-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="cf4f2-109">建立 RuleGroupOverride 專案，並將組名作為 $rule 1、$rule 2 的 $ruleName 與規則。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="cf4f2-110">指派相同的 $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="cf4f2-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="cf4f2-111">參數</span><span class="sxs-lookup"><span data-stu-id="cf4f2-111">PARAMETERS</span></span>

### <span data-ttu-id="cf4f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4f2-112">-DefaultProfile</span></span>
<span data-ttu-id="cf4f2-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf4f2-114">-規則</span><span class="sxs-lookup"><span data-stu-id="cf4f2-114">-Rule</span></span>
<span data-ttu-id="cf4f2-115">規則清單。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-115">List of Rules.</span></span>

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

### <span data-ttu-id="cf4f2-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4f2-116">-RuleGroupName</span></span>
<span data-ttu-id="cf4f2-117">在 override RuleGroup 專案中指定 ruleGroupName。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="cf4f2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4f2-118">CommonParameters</span></span>
<span data-ttu-id="cf4f2-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4f2-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf4f2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4f2-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cf4f2-121">INPUTS</span></span>

### <span data-ttu-id="cf4f2-122">所有</span><span class="sxs-lookup"><span data-stu-id="cf4f2-122">None</span></span>

## <span data-ttu-id="cf4f2-123">輸出</span><span class="sxs-lookup"><span data-stu-id="cf4f2-123">OUTPUTS</span></span>

### <span data-ttu-id="cf4f2-124">PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cf4f2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="cf4f2-125">筆記</span><span class="sxs-lookup"><span data-stu-id="cf4f2-125">NOTES</span></span>

## <span data-ttu-id="cf4f2-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf4f2-126">RELATED LINKS</span></span>
