---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278565"
---
# <span data-ttu-id="8a6a8-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8a6a8-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="8a6a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6a8-103">針對防火牆原則建立 ManagedRules。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="8a6a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a6a8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a6a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6a8-106">**新的-AzApplicationGatewayFirewallPolicyManagedRule** 會建立防火牆原則的管理規則。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="8a6a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a6a8-107">EXAMPLES</span></span>

### <span data-ttu-id="8a6a8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8a6a8-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="8a6a8-109">此命令會建立受管理規則的 $managedRuleSet ManagedRuleSet 清單，其中包含含有 $exclusion 1、$exclusion 2 之專案的 [排除] 清單。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="8a6a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a6a8-110">PARAMETERS</span></span>

### <span data-ttu-id="8a6a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6a8-111">-DefaultProfile</span></span>
<span data-ttu-id="8a6a8-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6a8-113">-排除</span><span class="sxs-lookup"><span data-stu-id="8a6a8-113">-Exclusion</span></span>
<span data-ttu-id="8a6a8-114">排除專案的清單。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="8a6a8-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8a6a8-115">-ManagedRuleSet</span></span>
<span data-ttu-id="8a6a8-116">受管理的規則集清單。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="8a6a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6a8-117">CommonParameters</span></span>
<span data-ttu-id="8a6a8-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6a8-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6a8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8a6a8-120">INPUTS</span></span>

### <span data-ttu-id="8a6a8-121">所有</span><span class="sxs-lookup"><span data-stu-id="8a6a8-121">None</span></span>

## <span data-ttu-id="8a6a8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="8a6a8-122">OUTPUTS</span></span>

### <span data-ttu-id="8a6a8-123">PSApplicationGatewayFirewallPolicyManagedRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8a6a8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="8a6a8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="8a6a8-124">NOTES</span></span>

## <span data-ttu-id="8a6a8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a6a8-125">RELATED LINKS</span></span>
