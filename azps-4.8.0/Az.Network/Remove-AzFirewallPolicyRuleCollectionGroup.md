---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970887"
---
# <span data-ttu-id="3a198-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="3a198-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="3a198-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a198-102">SYNOPSIS</span></span>
<span data-ttu-id="3a198-103">移除 Azure 防火牆原則中的 Azure 防火牆策略規則集合群組</span><span class="sxs-lookup"><span data-stu-id="3a198-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="3a198-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a198-104">SYNTAX</span></span>

### <span data-ttu-id="3a198-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3a198-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a198-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a198-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a198-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a198-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a198-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a198-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a198-109">說明</span><span class="sxs-lookup"><span data-stu-id="3a198-109">DESCRIPTION</span></span>
<span data-ttu-id="3a198-110">**AzFirewallPolicyRuleCollectionGroup** Cmdlet 會從 Azure 防火牆原則中移除規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="3a198-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="3a198-111">示例</span><span class="sxs-lookup"><span data-stu-id="3a198-111">EXAMPLES</span></span>

### <span data-ttu-id="3a198-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3a198-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="3a198-113">這個範例會移除防火牆原則物件中名為「testRcGroup」的防火牆原則規則 colelction 群組 $fp</span><span class="sxs-lookup"><span data-stu-id="3a198-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="3a198-114">範例2</span><span class="sxs-lookup"><span data-stu-id="3a198-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="3a198-115">這個範例會在名為「fpName」的防火牆中，移除名為「testRcGroup」的防火牆原則規則 colelction 群組 frpm resourcegroup 名稱 "testRg"</span><span class="sxs-lookup"><span data-stu-id="3a198-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="3a198-116">參數</span><span class="sxs-lookup"><span data-stu-id="3a198-116">PARAMETERS</span></span>

### <span data-ttu-id="3a198-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a198-117">-AsJob</span></span>
<span data-ttu-id="3a198-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3a198-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a198-119">-DefaultProfile</span></span>
<span data-ttu-id="3a198-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a198-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="3a198-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="3a198-122">防火牆原則的名稱</span><span class="sxs-lookup"><span data-stu-id="3a198-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3a198-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="3a198-124">防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="3a198-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3a198-125">-Force</span></span>
<span data-ttu-id="3a198-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="3a198-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a198-127">-InputObject</span></span>
<span data-ttu-id="3a198-128">防火牆原則規則集合群組物件</span><span class="sxs-lookup"><span data-stu-id="3a198-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a198-129">-Name</span></span>
<span data-ttu-id="3a198-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3a198-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a198-131">-PassThru</span></span>
<span data-ttu-id="3a198-132">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3a198-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a198-133">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3a198-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a198-134">-ResourceGroupName</span></span>
<span data-ttu-id="3a198-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a198-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a198-136">-ResourceId</span></span>
<span data-ttu-id="3a198-137">規則集合 groupy 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3a198-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-138">-確認</span><span class="sxs-lookup"><span data-stu-id="3a198-138">-Confirm</span></span>
<span data-ttu-id="3a198-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a198-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a198-140">-WhatIf</span></span>
<span data-ttu-id="3a198-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a198-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a198-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a198-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a198-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a198-143">CommonParameters</span></span>
<span data-ttu-id="3a198-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a198-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a198-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3a198-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a198-146">輸入</span><span class="sxs-lookup"><span data-stu-id="3a198-146">INPUTS</span></span>

### <span data-ttu-id="3a198-147">System.object</span><span class="sxs-lookup"><span data-stu-id="3a198-147">System.String</span></span>

### <span data-ttu-id="3a198-148">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3a198-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="3a198-149">PSAzureFirewallPolicyRuleCollectionGroupWrapper 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3a198-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="3a198-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3a198-150">OUTPUTS</span></span>

### <span data-ttu-id="3a198-151">System.object</span><span class="sxs-lookup"><span data-stu-id="3a198-151">System.Boolean</span></span>

## <span data-ttu-id="3a198-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3a198-152">NOTES</span></span>

## <span data-ttu-id="3a198-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a198-153">RELATED LINKS</span></span>
