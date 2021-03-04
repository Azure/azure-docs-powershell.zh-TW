---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 83c6cc2ba8103b95aed6d6d365c700e656ac16a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915906"
---
# <span data-ttu-id="4cf0b-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4cf0b-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="4cf0b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4cf0b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf0b-103">移除一個策略指派。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="4cf0b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4cf0b-104">SYNTAX</span></span>

### <span data-ttu-id="4cf0b-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4cf0b-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cf0b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf0b-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cf0b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf0b-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cf0b-108">描述</span><span class="sxs-lookup"><span data-stu-id="4cf0b-108">DESCRIPTION</span></span>
<span data-ttu-id="4cf0b-109">**Remove-AzPolicyAssignment Cmdlet** 會移除指定的策略指派。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="4cf0b-110">例子</span><span class="sxs-lookup"><span data-stu-id="4cf0b-110">EXAMPLES</span></span>

### <span data-ttu-id="4cf0b-111">範例 1：根據名稱和範圍移除策略指派</span><span class="sxs-lookup"><span data-stu-id="4cf0b-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="4cf0b-112">第一個命令會使用 Get-AzResourceGroup Cmdlet，獲得一個名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="4cf0b-113">該命令將該物件儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4cf0b-114">第二個命令會移除在資源群組層級指派的名為 PolicyAssignment07 的策略工作分派。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="4cf0b-115">資源的 **ResourceId** 屬性$ResourceGroup識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="4cf0b-116">範例 2：根據識別碼移除策略指派</span><span class="sxs-lookup"><span data-stu-id="4cf0b-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="4cf0b-117">第一個命令會獲得名為 ResourceGroup11 的資源群組，然後將該物件儲存在$ResourceGroup變數。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4cf0b-118">第二個命令會以資源群組層級獲得策略指派，然後將它儲存在$PolicyAssignment變數。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4cf0b-119">資源的 **ResourceId** 屬性$ResourceGroup識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="4cf0b-120">最後一個命令會移除 **ResourceId** 屬性所識別$PolicyAssignment指派。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="4cf0b-121">參數</span><span class="sxs-lookup"><span data-stu-id="4cf0b-121">PARAMETERS</span></span>

### <span data-ttu-id="4cf0b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4cf0b-122">-ApiVersion</span></span>
<span data-ttu-id="4cf0b-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4cf0b-124">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf0b-125">-DefaultProfile</span></span>
<span data-ttu-id="4cf0b-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4cf0b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cf0b-127">-Id</span><span class="sxs-lookup"><span data-stu-id="4cf0b-127">-Id</span></span>
<span data-ttu-id="4cf0b-128">指定此 Cmdlet 移除之策略工作分派的完全合格資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cf0b-129">-InputObject</span></span>
<span data-ttu-id="4cf0b-130">移除來自另一個 Cmdlet 之命令指派物件。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cf0b-131">-Name</span></span>
<span data-ttu-id="4cf0b-132">指定此 Cmdlet 移除之策略指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="4cf0b-133">-Pre</span></span>
<span data-ttu-id="4cf0b-134">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-135">-範圍</span><span class="sxs-lookup"><span data-stu-id="4cf0b-135">-Scope</span></span>
<span data-ttu-id="4cf0b-136">指定原則的適用範圍。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4cf0b-137">-Confirm</span></span>
<span data-ttu-id="4cf0b-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf0b-139">-WhatIf</span></span>
<span data-ttu-id="4cf0b-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf0b-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf0b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf0b-142">CommonParameters</span></span>
<span data-ttu-id="4cf0b-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4cf0b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf0b-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cf0b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf0b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4cf0b-145">INPUTS</span></span>

### <span data-ttu-id="4cf0b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf0b-146">System.String</span></span>

## <span data-ttu-id="4cf0b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="4cf0b-147">OUTPUTS</span></span>

### <span data-ttu-id="4cf0b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cf0b-148">System.Boolean</span></span>

## <span data-ttu-id="4cf0b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="4cf0b-149">NOTES</span></span>

## <span data-ttu-id="4cf0b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cf0b-150">RELATED LINKS</span></span>

[<span data-ttu-id="4cf0b-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4cf0b-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="4cf0b-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4cf0b-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="4cf0b-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4cf0b-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


