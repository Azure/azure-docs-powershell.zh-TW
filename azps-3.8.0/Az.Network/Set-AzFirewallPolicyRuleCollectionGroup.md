---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958451"
---
# <span data-ttu-id="bf886-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="bf886-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="bf886-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf886-102">SYNOPSIS</span></span>
<span data-ttu-id="bf886-103">儲存已修改的 azure 防火牆策略規則集合群組</span><span class="sxs-lookup"><span data-stu-id="bf886-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="bf886-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf886-104">SYNTAX</span></span>

### <span data-ttu-id="bf886-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf886-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf886-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf886-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf886-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf886-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf886-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf886-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf886-109">說明</span><span class="sxs-lookup"><span data-stu-id="bf886-109">DESCRIPTION</span></span>
<span data-ttu-id="bf886-110">**AzFirewallPolicyRuleCollectionGroup** Cmdlet 會更新 Azure 防火牆原則中的規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="bf886-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="bf886-111">示例</span><span class="sxs-lookup"><span data-stu-id="bf886-111">EXAMPLES</span></span>

### <span data-ttu-id="bf886-112">範例1</span><span class="sxs-lookup"><span data-stu-id="bf886-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="bf886-113">這個範例會在防火牆原則中更新規則集合群組 $fp</span><span class="sxs-lookup"><span data-stu-id="bf886-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="bf886-114">參數</span><span class="sxs-lookup"><span data-stu-id="bf886-114">PARAMETERS</span></span>

### <span data-ttu-id="bf886-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf886-115">-DefaultProfile</span></span>
<span data-ttu-id="bf886-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf886-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf886-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="bf886-117">-FirewallPolicyName</span></span>
<span data-ttu-id="bf886-118">防火牆原則的名稱</span><span class="sxs-lookup"><span data-stu-id="bf886-118">The name of the firewall policy</span></span>

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

### <span data-ttu-id="bf886-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="bf886-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="bf886-120">防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="bf886-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf886-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf886-121">-InputObject</span></span>
<span data-ttu-id="bf886-122">規則清單</span><span class="sxs-lookup"><span data-stu-id="bf886-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf886-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf886-123">-Name</span></span>
<span data-ttu-id="bf886-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bf886-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf886-125">-優先順序</span><span class="sxs-lookup"><span data-stu-id="bf886-125">-Priority</span></span>
<span data-ttu-id="bf886-126">規則群組的優先順序</span><span class="sxs-lookup"><span data-stu-id="bf886-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf886-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf886-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf886-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf886-128">The resource group name.</span></span>

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

### <span data-ttu-id="bf886-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf886-129">-ResourceId</span></span>
<span data-ttu-id="bf886-130">規則集合 groupy 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bf886-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf886-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="bf886-131">-RuleCollection</span></span>
<span data-ttu-id="bf886-132">規則集合清單</span><span class="sxs-lookup"><span data-stu-id="bf886-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf886-133">-確認</span><span class="sxs-lookup"><span data-stu-id="bf886-133">-Confirm</span></span>
<span data-ttu-id="bf886-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf886-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf886-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf886-135">-WhatIf</span></span>
<span data-ttu-id="bf886-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf886-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf886-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf886-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf886-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf886-138">CommonParameters</span></span>
<span data-ttu-id="bf886-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf886-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf886-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf886-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf886-141">輸入</span><span class="sxs-lookup"><span data-stu-id="bf886-141">INPUTS</span></span>

### <span data-ttu-id="bf886-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bf886-142">System.String</span></span>

### <span data-ttu-id="bf886-143">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bf886-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="bf886-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bf886-144">OUTPUTS</span></span>

### <span data-ttu-id="bf886-145">PSAzureFirewallPolicyRuleCollectionGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bf886-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="bf886-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bf886-146">NOTES</span></span>

## <span data-ttu-id="bf886-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf886-147">RELATED LINKS</span></span>
