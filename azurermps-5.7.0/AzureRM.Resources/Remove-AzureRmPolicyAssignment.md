---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448562"
---
# <span data-ttu-id="f5df6-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5df6-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f5df6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5df6-102">SYNOPSIS</span></span>
<span data-ttu-id="f5df6-103">移除原則指派。</span><span class="sxs-lookup"><span data-stu-id="f5df6-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5df6-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5df6-104">SYNTAX</span></span>

### <span data-ttu-id="f5df6-105">RemoveByPolicyAssignmentName (預設) </span><span class="sxs-lookup"><span data-stu-id="f5df6-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5df6-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="f5df6-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5df6-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5df6-107">DESCRIPTION</span></span>
<span data-ttu-id="f5df6-108">**AzureRmPolicyAssignment** Cmdlet 會移除指定的原則指派。</span><span class="sxs-lookup"><span data-stu-id="f5df6-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="f5df6-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5df6-109">EXAMPLES</span></span>

### <span data-ttu-id="f5df6-110">範例1：依名稱與作用域移除原則指派</span><span class="sxs-lookup"><span data-stu-id="f5df6-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="f5df6-111">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5df6-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f5df6-112">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5df6-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f5df6-113">第二個命令會移除在資源群組層級指派的名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="f5df6-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="f5df6-114">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5df6-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="f5df6-115">範例2：依識別碼移除原則指派</span><span class="sxs-lookup"><span data-stu-id="f5df6-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="f5df6-116">第一個命令會取得名為 ResourceGroup11 的資源群組，然後將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5df6-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f5df6-117">第二個命令會在資源群組層級取得原則指派，然後將它儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5df6-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="f5df6-118">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5df6-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="f5df6-119">最後一個命令會移除 $PolicyAssignment 的 **ResourceId** 屬性所識別的原則指派。</span><span class="sxs-lookup"><span data-stu-id="f5df6-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="f5df6-120">參數</span><span class="sxs-lookup"><span data-stu-id="f5df6-120">PARAMETERS</span></span>

### <span data-ttu-id="f5df6-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5df6-121">-ApiVersion</span></span>
<span data-ttu-id="f5df6-122">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f5df6-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5df6-123">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f5df6-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5df6-124">-DefaultProfile</span></span>
<span data-ttu-id="f5df6-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f5df6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f5df6-126">-Id</span></span>
<span data-ttu-id="f5df6-127">指定此 Cmdlet 移除之原則指派的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5df6-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f5df6-128">-InformationAction</span></span>
<span data-ttu-id="f5df6-129">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="f5df6-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f5df6-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f5df6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5df6-131">持續</span><span class="sxs-lookup"><span data-stu-id="f5df6-131">Continue</span></span>
- <span data-ttu-id="f5df6-132">理會</span><span class="sxs-lookup"><span data-stu-id="f5df6-132">Ignore</span></span>
- <span data-ttu-id="f5df6-133">看</span><span class="sxs-lookup"><span data-stu-id="f5df6-133">Inquire</span></span>
- <span data-ttu-id="f5df6-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f5df6-134">SilentlyContinue</span></span>
- <span data-ttu-id="f5df6-135">停止</span><span class="sxs-lookup"><span data-stu-id="f5df6-135">Stop</span></span>
- <span data-ttu-id="f5df6-136">封存</span><span class="sxs-lookup"><span data-stu-id="f5df6-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f5df6-137">-InformationVariable</span></span>
<span data-ttu-id="f5df6-138">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="f5df6-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5df6-139">-Name</span></span>
<span data-ttu-id="f5df6-140">指定此 Cmdlet 移除之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5df6-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-141">-預先</span><span class="sxs-lookup"><span data-stu-id="f5df6-141">-Pre</span></span>
<span data-ttu-id="f5df6-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f5df6-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5df6-143">-範圍</span><span class="sxs-lookup"><span data-stu-id="f5df6-143">-Scope</span></span>
<span data-ttu-id="f5df6-144">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="f5df6-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-145">-確認</span><span class="sxs-lookup"><span data-stu-id="f5df6-145">-Confirm</span></span>
<span data-ttu-id="f5df6-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5df6-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5df6-147">-WhatIf</span></span>
<span data-ttu-id="f5df6-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5df6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5df6-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5df6-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5df6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5df6-150">CommonParameters</span></span>
<span data-ttu-id="f5df6-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5df6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5df6-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5df6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5df6-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f5df6-153">INPUTS</span></span>

### <span data-ttu-id="f5df6-154">所有</span><span class="sxs-lookup"><span data-stu-id="f5df6-154">None</span></span>
<span data-ttu-id="f5df6-155">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f5df6-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5df6-156">輸出</span><span class="sxs-lookup"><span data-stu-id="f5df6-156">OUTPUTS</span></span>

### <span data-ttu-id="f5df6-157">System.object</span><span class="sxs-lookup"><span data-stu-id="f5df6-157">System.Boolean</span></span>

## <span data-ttu-id="f5df6-158">筆記</span><span class="sxs-lookup"><span data-stu-id="f5df6-158">NOTES</span></span>

## <span data-ttu-id="f5df6-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5df6-159">RELATED LINKS</span></span>

[<span data-ttu-id="f5df6-160">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5df6-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f5df6-161">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5df6-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f5df6-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5df6-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


