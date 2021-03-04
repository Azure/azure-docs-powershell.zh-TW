---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 50dd0f1b4f224b343d827ed3d07457d86352e96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912697"
---
# <span data-ttu-id="69c7c-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="69c7c-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="69c7c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="69c7c-103">移除 Azure 防火牆原則中的 Azure 防火牆原則規則集合群組</span><span class="sxs-lookup"><span data-stu-id="69c7c-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="69c7c-104">語法</span><span class="sxs-lookup"><span data-stu-id="69c7c-104">SYNTAX</span></span>

### <span data-ttu-id="69c7c-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="69c7c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c7c-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c7c-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69c7c-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c7c-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69c7c-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c7c-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c7c-109">描述</span><span class="sxs-lookup"><span data-stu-id="69c7c-109">DESCRIPTION</span></span>
<span data-ttu-id="69c7c-110">**Remove-AzFirewallPolicyRuleCollectionGroup** Cmdlet 會從 Azure 防火牆原則移除規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="69c7c-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="69c7c-111">例子</span><span class="sxs-lookup"><span data-stu-id="69c7c-111">EXAMPLES</span></span>

### <span data-ttu-id="69c7c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="69c7c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="69c7c-113">此範例會移除防火牆原則物件中名為"testRcGroup"的防火牆原則規則$fp</span><span class="sxs-lookup"><span data-stu-id="69c7c-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="69c7c-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="69c7c-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="69c7c-115">此範例會移除名為 "fpName" frpm 之防火牆中名為 "testRcGroup" 的防火牆原則規則 colelction 群組 "testRg"</span><span class="sxs-lookup"><span data-stu-id="69c7c-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="69c7c-116">參數</span><span class="sxs-lookup"><span data-stu-id="69c7c-116">PARAMETERS</span></span>

### <span data-ttu-id="69c7c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69c7c-117">-AsJob</span></span>
<span data-ttu-id="69c7c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="69c7c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69c7c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c7c-119">-DefaultProfile</span></span>
<span data-ttu-id="69c7c-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69c7c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c7c-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="69c7c-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="69c7c-122">防火牆政策的名稱</span><span class="sxs-lookup"><span data-stu-id="69c7c-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="69c7c-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="69c7c-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="69c7c-124">防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="69c7c-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="69c7c-125">-強制</span><span class="sxs-lookup"><span data-stu-id="69c7c-125">-Force</span></span>
<span data-ttu-id="69c7c-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="69c7c-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="69c7c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69c7c-127">-InputObject</span></span>
<span data-ttu-id="69c7c-128">防火牆原則規則集合群組物件</span><span class="sxs-lookup"><span data-stu-id="69c7c-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="69c7c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="69c7c-129">-Name</span></span>
<span data-ttu-id="69c7c-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="69c7c-130">The resource name.</span></span>

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

### <span data-ttu-id="69c7c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69c7c-131">-PassThru</span></span>
<span data-ttu-id="69c7c-132">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="69c7c-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69c7c-133">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="69c7c-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69c7c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c7c-134">-ResourceGroupName</span></span>
<span data-ttu-id="69c7c-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="69c7c-135">The resource group name.</span></span>

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

### <span data-ttu-id="69c7c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69c7c-136">-ResourceId</span></span>
<span data-ttu-id="69c7c-137">規則集合群組的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="69c7c-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="69c7c-138">-確認</span><span class="sxs-lookup"><span data-stu-id="69c7c-138">-Confirm</span></span>
<span data-ttu-id="69c7c-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69c7c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c7c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c7c-140">-WhatIf</span></span>
<span data-ttu-id="69c7c-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69c7c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c7c-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69c7c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c7c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c7c-143">CommonParameters</span></span>
<span data-ttu-id="69c7c-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69c7c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c7c-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69c7c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c7c-146">輸入</span><span class="sxs-lookup"><span data-stu-id="69c7c-146">INPUTS</span></span>

### <span data-ttu-id="69c7c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="69c7c-147">System.String</span></span>

### <span data-ttu-id="69c7c-148">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="69c7c-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="69c7c-149">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyRuleCollectionGroupWallapper</span><span class="sxs-lookup"><span data-stu-id="69c7c-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="69c7c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="69c7c-150">OUTPUTS</span></span>

### <span data-ttu-id="69c7c-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69c7c-151">System.Boolean</span></span>

## <span data-ttu-id="69c7c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="69c7c-152">NOTES</span></span>

## <span data-ttu-id="69c7c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="69c7c-153">RELATED LINKS</span></span>
