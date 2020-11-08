---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8d60b8f7ff28e6c2a4f5a177f5cad222b1a3014c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135567"
---
# <span data-ttu-id="cc48a-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="cc48a-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="cc48a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc48a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc48a-103">建立新的 Azure 防火牆策略規則集合群組</span><span class="sxs-lookup"><span data-stu-id="cc48a-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="cc48a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc48a-104">SYNTAX</span></span>

### <span data-ttu-id="cc48a-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc48a-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc48a-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc48a-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc48a-107">說明</span><span class="sxs-lookup"><span data-stu-id="cc48a-107">DESCRIPTION</span></span>
<span data-ttu-id="cc48a-108">**新的 AzFirewallPolicyRuleCollectionGroup** Cmdlet 會在 Azure 防火牆原則中建立規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="cc48a-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="cc48a-109">示例</span><span class="sxs-lookup"><span data-stu-id="cc48a-109">EXAMPLES</span></span>

### <span data-ttu-id="cc48a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cc48a-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="cc48a-111">這個範例會在防火牆原則中建立規則集合群組 $fp</span><span class="sxs-lookup"><span data-stu-id="cc48a-111">This example creates a rule collection group in the firewall policy $fp</span></span>

### <span data-ttu-id="cc48a-112">範例2</span><span class="sxs-lookup"><span data-stu-id="cc48a-112">Example 2</span></span>

<span data-ttu-id="cc48a-113">建立新的 Azure 防火牆策略規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="cc48a-113">Create a new Azure Firewall Policy Rule Collection Group.</span></span> <span data-ttu-id="cc48a-114"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="cc48a-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzFirewallPolicyRuleCollectionGroup -FirewallPolicyName <String> -Name rg1 -Priority 200 -ResourceGroupName TestRg
```

## <span data-ttu-id="cc48a-115">參數</span><span class="sxs-lookup"><span data-stu-id="cc48a-115">PARAMETERS</span></span>

### <span data-ttu-id="cc48a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc48a-116">-DefaultProfile</span></span>
<span data-ttu-id="cc48a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc48a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc48a-118">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="cc48a-118">-FirewallPolicyName</span></span>
<span data-ttu-id="cc48a-119">防火牆原則的名稱</span><span class="sxs-lookup"><span data-stu-id="cc48a-119">The name of the firewall policy</span></span>

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

### <span data-ttu-id="cc48a-120">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="cc48a-120">-FirewallPolicyObject</span></span>
<span data-ttu-id="cc48a-121">防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="cc48a-121">Firewall Policy.</span></span>

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

### <span data-ttu-id="cc48a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc48a-122">-Name</span></span>
<span data-ttu-id="cc48a-123">規則群組的名稱</span><span class="sxs-lookup"><span data-stu-id="cc48a-123">The name of the Rule Group</span></span>

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

### <span data-ttu-id="cc48a-124">-優先順序</span><span class="sxs-lookup"><span data-stu-id="cc48a-124">-Priority</span></span>
<span data-ttu-id="cc48a-125">規則群組的優先順序</span><span class="sxs-lookup"><span data-stu-id="cc48a-125">The priority of the rule group</span></span>

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

### <span data-ttu-id="cc48a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc48a-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc48a-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc48a-127">The resource group name.</span></span>

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

### <span data-ttu-id="cc48a-128">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="cc48a-128">-RuleCollection</span></span>
<span data-ttu-id="cc48a-129">規則清單</span><span class="sxs-lookup"><span data-stu-id="cc48a-129">The list of rules</span></span>

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

### <span data-ttu-id="cc48a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cc48a-130">-Confirm</span></span>
<span data-ttu-id="cc48a-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc48a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc48a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc48a-132">-WhatIf</span></span>
<span data-ttu-id="cc48a-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc48a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc48a-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc48a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc48a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc48a-135">CommonParameters</span></span>
<span data-ttu-id="cc48a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc48a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc48a-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc48a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc48a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cc48a-138">INPUTS</span></span>

### <span data-ttu-id="cc48a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cc48a-139">System.String</span></span>

### <span data-ttu-id="cc48a-140">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cc48a-140">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="cc48a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cc48a-141">OUTPUTS</span></span>

### <span data-ttu-id="cc48a-142">PSAzureFirewallPolicyRuleCollectionGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cc48a-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="cc48a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cc48a-143">NOTES</span></span>

## <span data-ttu-id="cc48a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc48a-144">RELATED LINKS</span></span>