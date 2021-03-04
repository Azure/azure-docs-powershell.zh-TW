---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 73404a44ea26a07aad2869cc8fc94ef1c74ee987
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910445"
---
# <span data-ttu-id="b5835-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="b5835-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="b5835-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5835-102">SYNOPSIS</span></span>
<span data-ttu-id="b5835-103">建立防火牆策略的 ManagedRules。</span><span class="sxs-lookup"><span data-stu-id="b5835-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="b5835-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5835-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5835-105">描述</span><span class="sxs-lookup"><span data-stu-id="b5835-105">DESCRIPTION</span></span>
<span data-ttu-id="b5835-106">**New-AzApplicationGatewayFirewallPolicyManagedRule** 會建立防火牆原則的受管理規則。</span><span class="sxs-lookup"><span data-stu-id="b5835-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="b5835-107">例子</span><span class="sxs-lookup"><span data-stu-id="b5835-107">EXAMPLES</span></span>

### <span data-ttu-id="b5835-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5835-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="b5835-109">該命令會建立 ManagedRuleSet 清單與 $managedRuleSet，以及包含專案為 $exclusion 1，$exclusion 2 的排除清單。</span><span class="sxs-lookup"><span data-stu-id="b5835-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="b5835-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5835-110">PARAMETERS</span></span>

### <span data-ttu-id="b5835-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5835-111">-DefaultProfile</span></span>
<span data-ttu-id="b5835-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5835-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5835-113">-排除</span><span class="sxs-lookup"><span data-stu-id="b5835-113">-Exclusion</span></span>
<span data-ttu-id="b5835-114">排除專案清單。</span><span class="sxs-lookup"><span data-stu-id="b5835-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5835-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5835-115">-ManagedRuleSet</span></span>
<span data-ttu-id="b5835-116">受管理的規則集清單。</span><span class="sxs-lookup"><span data-stu-id="b5835-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5835-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5835-117">CommonParameters</span></span>
<span data-ttu-id="b5835-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5835-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5835-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5835-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5835-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b5835-120">INPUTS</span></span>

### <span data-ttu-id="b5835-121">沒有</span><span class="sxs-lookup"><span data-stu-id="b5835-121">None</span></span>

## <span data-ttu-id="b5835-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b5835-122">OUTPUTS</span></span>

### <span data-ttu-id="b5835-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="b5835-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="b5835-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b5835-124">NOTES</span></span>

## <span data-ttu-id="b5835-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5835-125">RELATED LINKS</span></span>
