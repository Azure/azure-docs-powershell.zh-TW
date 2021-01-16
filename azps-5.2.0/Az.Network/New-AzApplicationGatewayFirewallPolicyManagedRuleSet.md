---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279619"
---
# <span data-ttu-id="881f4-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="881f4-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="881f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="881f4-102">SYNOPSIS</span></span>
<span data-ttu-id="881f4-103">建立 firewallPolicy 的 ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="881f4-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="881f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="881f4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="881f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="881f4-105">DESCRIPTION</span></span>
<span data-ttu-id="881f4-106">**新的-AzApplicationGatewayFirewallPolicyManagedRuleSet** 會建立防火牆原則的管理規則。</span><span class="sxs-lookup"><span data-stu-id="881f4-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="881f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="881f4-107">EXAMPLES</span></span>

### <span data-ttu-id="881f4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="881f4-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="881f4-109">建立一個 ManagedRuleSet，並將 ruleSetType 設為 $ruleSetType，ruleSetVersion 為 $ruleSetVersion，而 RuleGroupOverrides 做為 entires 為 $ruleGroupOverride 1 的清單，$ruleGroupOverride 2 新的 ManagedRuleSet 指派給 $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="881f4-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="881f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="881f4-110">PARAMETERS</span></span>

### <span data-ttu-id="881f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881f4-111">-DefaultProfile</span></span>
<span data-ttu-id="881f4-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="881f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="881f4-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="881f4-113">-RuleGroupOverride</span></span>
<span data-ttu-id="881f4-114">規則群組覆蓋。</span><span class="sxs-lookup"><span data-stu-id="881f4-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="881f4-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="881f4-115">-RuleSetType</span></span>
<span data-ttu-id="881f4-116">在 managedRuleSet 中指定 RuleSetType</span><span class="sxs-lookup"><span data-stu-id="881f4-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="881f4-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="881f4-117">-RuleSetVersion</span></span>
<span data-ttu-id="881f4-118">在 managedRuleSet 中指定 RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="881f4-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="881f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881f4-119">CommonParameters</span></span>
<span data-ttu-id="881f4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="881f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881f4-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="881f4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881f4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="881f4-122">INPUTS</span></span>

### <span data-ttu-id="881f4-123">所有</span><span class="sxs-lookup"><span data-stu-id="881f4-123">None</span></span>

## <span data-ttu-id="881f4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="881f4-124">OUTPUTS</span></span>

### <span data-ttu-id="881f4-125">PSApplicationGatewayFirewallPolicyManagedRuleSet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="881f4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="881f4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="881f4-126">NOTES</span></span>

## <span data-ttu-id="881f4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="881f4-127">RELATED LINKS</span></span>
