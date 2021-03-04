---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912378"
---
# <span data-ttu-id="871de-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="871de-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="871de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="871de-102">SYNOPSIS</span></span>
<span data-ttu-id="871de-103">為 RuleGroupOverrideGroup 專案建立 ManagedRuleOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="871de-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="871de-104">語法</span><span class="sxs-lookup"><span data-stu-id="871de-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871de-105">描述</span><span class="sxs-lookup"><span data-stu-id="871de-105">DESCRIPTION</span></span>
<span data-ttu-id="871de-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** 會建立 ruleOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="871de-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="871de-107">例子</span><span class="sxs-lookup"><span data-stu-id="871de-107">EXAMPLES</span></span>

### <span data-ttu-id="871de-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="871de-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="871de-109">使用 RuleId 建立 ruleOverride 專案$ruleId狀態為停用。</span><span class="sxs-lookup"><span data-stu-id="871de-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="871de-110">參數</span><span class="sxs-lookup"><span data-stu-id="871de-110">PARAMETERS</span></span>

### <span data-ttu-id="871de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871de-111">-DefaultProfile</span></span>
<span data-ttu-id="871de-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="871de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="871de-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="871de-113">-RuleId</span></span>
<span data-ttu-id="871de-114">在重寫規則專案指定 RuleId。</span><span class="sxs-lookup"><span data-stu-id="871de-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="871de-115">-State</span><span class="sxs-lookup"><span data-stu-id="871de-115">-State</span></span>
<span data-ttu-id="871de-116">在重寫規則專案指定 RuleId。</span><span class="sxs-lookup"><span data-stu-id="871de-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871de-117">CommonParameters</span></span>
<span data-ttu-id="871de-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="871de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871de-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="871de-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871de-120">輸入</span><span class="sxs-lookup"><span data-stu-id="871de-120">INPUTS</span></span>

### <span data-ttu-id="871de-121">沒有</span><span class="sxs-lookup"><span data-stu-id="871de-121">None</span></span>

## <span data-ttu-id="871de-122">輸出</span><span class="sxs-lookup"><span data-stu-id="871de-122">OUTPUTS</span></span>

### <span data-ttu-id="871de-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="871de-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="871de-124">筆記</span><span class="sxs-lookup"><span data-stu-id="871de-124">NOTES</span></span>

## <span data-ttu-id="871de-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="871de-125">RELATED LINKS</span></span>
