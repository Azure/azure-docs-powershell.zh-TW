---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 18ca6ad068c5478bdb7177a8f53742f90d555dee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620785"
---
# <span data-ttu-id="be534-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="be534-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="be534-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be534-102">SYNOPSIS</span></span>
<span data-ttu-id="be534-103">移除原則指派。</span><span class="sxs-lookup"><span data-stu-id="be534-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="be534-104">句法</span><span class="sxs-lookup"><span data-stu-id="be534-104">SYNTAX</span></span>

### <span data-ttu-id="be534-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be534-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be534-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be534-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be534-107">說明</span><span class="sxs-lookup"><span data-stu-id="be534-107">DESCRIPTION</span></span>
<span data-ttu-id="be534-108">**AzPolicyAssignment** Cmdlet 會移除指定的原則指派。</span><span class="sxs-lookup"><span data-stu-id="be534-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="be534-109">示例</span><span class="sxs-lookup"><span data-stu-id="be534-109">EXAMPLES</span></span>

### <span data-ttu-id="be534-110">範例1：依名稱與作用域移除原則指派</span><span class="sxs-lookup"><span data-stu-id="be534-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="be534-111">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="be534-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="be534-112">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="be534-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="be534-113">第二個命令會移除在資源群組層級指派的名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="be534-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="be534-114">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="be534-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="be534-115">範例2：依識別碼移除原則指派</span><span class="sxs-lookup"><span data-stu-id="be534-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="be534-116">第一個命令會取得名為 ResourceGroup11 的資源群組，然後將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="be534-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="be534-117">第二個命令會在資源群組層級取得原則指派，然後將它儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="be534-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="be534-118">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="be534-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="be534-119">最後一個命令會移除 $PolicyAssignment 的 **ResourceId** 屬性所識別的原則指派。</span><span class="sxs-lookup"><span data-stu-id="be534-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="be534-120">參數</span><span class="sxs-lookup"><span data-stu-id="be534-120">PARAMETERS</span></span>

### <span data-ttu-id="be534-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be534-121">-ApiVersion</span></span>
<span data-ttu-id="be534-122">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="be534-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="be534-123">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="be534-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="be534-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be534-124">-DefaultProfile</span></span>
<span data-ttu-id="be534-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="be534-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be534-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="be534-126">-Id</span></span>
<span data-ttu-id="be534-127">指定此 Cmdlet 移除之原則指派的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="be534-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be534-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="be534-128">-Name</span></span>
<span data-ttu-id="be534-129">指定此 Cmdlet 移除之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="be534-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be534-130">-預先</span><span class="sxs-lookup"><span data-stu-id="be534-130">-Pre</span></span>
<span data-ttu-id="be534-131">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="be534-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be534-132">-範圍</span><span class="sxs-lookup"><span data-stu-id="be534-132">-Scope</span></span>
<span data-ttu-id="be534-133">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="be534-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="be534-134">-確認</span><span class="sxs-lookup"><span data-stu-id="be534-134">-Confirm</span></span>
<span data-ttu-id="be534-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be534-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be534-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be534-136">-WhatIf</span></span>
<span data-ttu-id="be534-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be534-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be534-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be534-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be534-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be534-139">CommonParameters</span></span>
<span data-ttu-id="be534-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be534-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be534-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be534-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be534-142">輸入</span><span class="sxs-lookup"><span data-stu-id="be534-142">INPUTS</span></span>

### <span data-ttu-id="be534-143">System.object</span><span class="sxs-lookup"><span data-stu-id="be534-143">System.String</span></span>

## <span data-ttu-id="be534-144">輸出</span><span class="sxs-lookup"><span data-stu-id="be534-144">OUTPUTS</span></span>

### <span data-ttu-id="be534-145">System.object</span><span class="sxs-lookup"><span data-stu-id="be534-145">System.Boolean</span></span>

## <span data-ttu-id="be534-146">筆記</span><span class="sxs-lookup"><span data-stu-id="be534-146">NOTES</span></span>

## <span data-ttu-id="be534-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="be534-147">RELATED LINKS</span></span>

[<span data-ttu-id="be534-148">AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="be534-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="be534-149">新-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="be534-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="be534-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="be534-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


