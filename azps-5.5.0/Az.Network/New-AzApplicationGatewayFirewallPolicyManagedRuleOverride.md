---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128882"
---
# <span data-ttu-id="c8f17-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c8f17-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="c8f17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8f17-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f17-103">建立 RuleGroupOverrideGroup 專案的 managedRuleOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="c8f17-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="c8f17-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8f17-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8f17-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8f17-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f17-106">**新的-AzApplicationGatewayFirewallPolicyManagedRuleOverride** 會建立 ruleOverride 專案。</span><span class="sxs-lookup"><span data-stu-id="c8f17-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="c8f17-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8f17-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f17-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c8f17-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="c8f17-109">建立 ruleOverride 專案，並將 RuleId 設為 $ruleId，並將狀態視為 Disabled。</span><span class="sxs-lookup"><span data-stu-id="c8f17-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="c8f17-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8f17-110">PARAMETERS</span></span>

### <span data-ttu-id="c8f17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f17-111">-DefaultProfile</span></span>
<span data-ttu-id="c8f17-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8f17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f17-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="c8f17-113">-RuleId</span></span>
<span data-ttu-id="c8f17-114">在覆寫規則專案中指定 RuleId。</span><span class="sxs-lookup"><span data-stu-id="c8f17-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="c8f17-115">-State</span><span class="sxs-lookup"><span data-stu-id="c8f17-115">-State</span></span>
<span data-ttu-id="c8f17-116">在覆寫規則專案中指定 RuleId。</span><span class="sxs-lookup"><span data-stu-id="c8f17-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="c8f17-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f17-117">CommonParameters</span></span>
<span data-ttu-id="c8f17-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8f17-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f17-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8f17-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f17-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c8f17-120">INPUTS</span></span>

### <span data-ttu-id="c8f17-121">所有</span><span class="sxs-lookup"><span data-stu-id="c8f17-121">None</span></span>

## <span data-ttu-id="c8f17-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c8f17-122">OUTPUTS</span></span>

### <span data-ttu-id="c8f17-123">PSApplicationGatewayFirewallPolicyManagedRuleOverride 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8f17-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="c8f17-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c8f17-124">NOTES</span></span>

## <span data-ttu-id="c8f17-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8f17-125">RELATED LINKS</span></span>
