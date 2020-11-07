---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957754"
---
# <span data-ttu-id="42e0b-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="42e0b-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="42e0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="42e0b-103">建立新的 Azure 防火牆策略規則集合群組</span><span class="sxs-lookup"><span data-stu-id="42e0b-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="42e0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="42e0b-104">SYNTAX</span></span>

### <span data-ttu-id="42e0b-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e0b-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42e0b-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e0b-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42e0b-107">說明</span><span class="sxs-lookup"><span data-stu-id="42e0b-107">DESCRIPTION</span></span>
<span data-ttu-id="42e0b-108">**新的 AzFirewallPolicyRuleCollectionGroup** Cmdlet 會在 Azure 防火牆原則中建立規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="42e0b-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="42e0b-109">示例</span><span class="sxs-lookup"><span data-stu-id="42e0b-109">EXAMPLES</span></span>

### <span data-ttu-id="42e0b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="42e0b-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="42e0b-111">這個範例會在防火牆原則中建立規則集合群組 $fp</span><span class="sxs-lookup"><span data-stu-id="42e0b-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="42e0b-112">參數</span><span class="sxs-lookup"><span data-stu-id="42e0b-112">PARAMETERS</span></span>

### <span data-ttu-id="42e0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e0b-113">-DefaultProfile</span></span>
<span data-ttu-id="42e0b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42e0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e0b-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="42e0b-115">-FirewallPolicyName</span></span>
<span data-ttu-id="42e0b-116">防火牆原則的名稱</span><span class="sxs-lookup"><span data-stu-id="42e0b-116">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e0b-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="42e0b-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="42e0b-118">防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="42e0b-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e0b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="42e0b-119">-Name</span></span>
<span data-ttu-id="42e0b-120">規則群組的名稱</span><span class="sxs-lookup"><span data-stu-id="42e0b-120">The name of the Rule Group</span></span>

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

### <span data-ttu-id="42e0b-121">-優先順序</span><span class="sxs-lookup"><span data-stu-id="42e0b-121">-Priority</span></span>
<span data-ttu-id="42e0b-122">規則群組的優先順序</span><span class="sxs-lookup"><span data-stu-id="42e0b-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="42e0b-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42e0b-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e0b-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="42e0b-125">-RuleCollection</span></span>
<span data-ttu-id="42e0b-126">規則清單</span><span class="sxs-lookup"><span data-stu-id="42e0b-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e0b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="42e0b-127">-Confirm</span></span>
<span data-ttu-id="42e0b-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42e0b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e0b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e0b-129">-WhatIf</span></span>
<span data-ttu-id="42e0b-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42e0b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e0b-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42e0b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e0b-132">CommonParameters</span></span>
<span data-ttu-id="42e0b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42e0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e0b-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42e0b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e0b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="42e0b-135">INPUTS</span></span>

### <span data-ttu-id="42e0b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="42e0b-136">System.String</span></span>

### <span data-ttu-id="42e0b-137">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="42e0b-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="42e0b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="42e0b-138">OUTPUTS</span></span>

### <span data-ttu-id="42e0b-139">PSAzureFirewallPolicyRuleCollectionGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="42e0b-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="42e0b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="42e0b-140">NOTES</span></span>

## <span data-ttu-id="42e0b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="42e0b-141">RELATED LINKS</span></span>
