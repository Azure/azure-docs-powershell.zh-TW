---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625688"
---
# <span data-ttu-id="37e90-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37e90-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="37e90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37e90-102">SYNOPSIS</span></span>
<span data-ttu-id="37e90-103">移除原則指派。</span><span class="sxs-lookup"><span data-stu-id="37e90-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37e90-104">句法</span><span class="sxs-lookup"><span data-stu-id="37e90-104">SYNTAX</span></span>

### <span data-ttu-id="37e90-105">原則指派名稱參數已設定。</span><span class="sxs-lookup"><span data-stu-id="37e90-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="37e90-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="37e90-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e90-107">原則指派識別碼參數已設定。</span><span class="sxs-lookup"><span data-stu-id="37e90-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e90-108">說明</span><span class="sxs-lookup"><span data-stu-id="37e90-108">DESCRIPTION</span></span>
<span data-ttu-id="37e90-109">**AzureRmPolicyAssignment** Cmdlet 會移除指定的原則指派。</span><span class="sxs-lookup"><span data-stu-id="37e90-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="37e90-110">示例</span><span class="sxs-lookup"><span data-stu-id="37e90-110">EXAMPLES</span></span>

### <span data-ttu-id="37e90-111">範例1：依名稱與作用域移除原則指派</span><span class="sxs-lookup"><span data-stu-id="37e90-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="37e90-112">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="37e90-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="37e90-113">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="37e90-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="37e90-114">第二個命令會移除在資源群組層級指派的名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="37e90-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="37e90-115">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="37e90-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="37e90-116">範例2：依識別碼移除原則指派</span><span class="sxs-lookup"><span data-stu-id="37e90-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="37e90-117">第一個命令會取得名為 ResourceGroup11 的資源群組，然後將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="37e90-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="37e90-118">第二個命令會在資源群組層級取得原則指派，然後將它儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="37e90-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="37e90-119">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="37e90-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="37e90-120">最後一個命令會移除 $PolicyAssignment 的 **ResourceId** 屬性所識別的原則指派。</span><span class="sxs-lookup"><span data-stu-id="37e90-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="37e90-121">參數</span><span class="sxs-lookup"><span data-stu-id="37e90-121">PARAMETERS</span></span>

### <span data-ttu-id="37e90-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="37e90-122">-ApiVersion</span></span>
<span data-ttu-id="37e90-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="37e90-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="37e90-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="37e90-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="37e90-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="37e90-125">-Id</span></span>
<span data-ttu-id="37e90-126">指定此 Cmdlet 移除之原則指派的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="37e90-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e90-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="37e90-127">-InformationAction</span></span>
<span data-ttu-id="37e90-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="37e90-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="37e90-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="37e90-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37e90-130">持續</span><span class="sxs-lookup"><span data-stu-id="37e90-130">Continue</span></span>
- <span data-ttu-id="37e90-131">理會</span><span class="sxs-lookup"><span data-stu-id="37e90-131">Ignore</span></span>
- <span data-ttu-id="37e90-132">看</span><span class="sxs-lookup"><span data-stu-id="37e90-132">Inquire</span></span>
- <span data-ttu-id="37e90-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="37e90-133">SilentlyContinue</span></span>
- <span data-ttu-id="37e90-134">停止</span><span class="sxs-lookup"><span data-stu-id="37e90-134">Stop</span></span>
- <span data-ttu-id="37e90-135">封存</span><span class="sxs-lookup"><span data-stu-id="37e90-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e90-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="37e90-136">-InformationVariable</span></span>
<span data-ttu-id="37e90-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="37e90-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e90-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="37e90-138">-Name</span></span>
<span data-ttu-id="37e90-139">指定此 Cmdlet 移除之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="37e90-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e90-140">-預先</span><span class="sxs-lookup"><span data-stu-id="37e90-140">-Pre</span></span>
<span data-ttu-id="37e90-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="37e90-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="37e90-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="37e90-142">-Scope</span></span>
<span data-ttu-id="37e90-143">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="37e90-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e90-144">-確認</span><span class="sxs-lookup"><span data-stu-id="37e90-144">-Confirm</span></span>
<span data-ttu-id="37e90-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37e90-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e90-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e90-146">-WhatIf</span></span>
<span data-ttu-id="37e90-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37e90-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e90-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37e90-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e90-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e90-149">-DefaultProfile</span></span>
<span data-ttu-id="37e90-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37e90-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e90-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e90-151">CommonParameters</span></span>
<span data-ttu-id="37e90-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37e90-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e90-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37e90-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e90-154">輸入</span><span class="sxs-lookup"><span data-stu-id="37e90-154">INPUTS</span></span>

## <span data-ttu-id="37e90-155">輸出</span><span class="sxs-lookup"><span data-stu-id="37e90-155">OUTPUTS</span></span>

### <span data-ttu-id="37e90-156">System.object</span><span class="sxs-lookup"><span data-stu-id="37e90-156">System.Boolean</span></span>

## <span data-ttu-id="37e90-157">筆記</span><span class="sxs-lookup"><span data-stu-id="37e90-157">NOTES</span></span>

## <span data-ttu-id="37e90-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="37e90-158">RELATED LINKS</span></span>

[<span data-ttu-id="37e90-159">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37e90-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="37e90-160">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37e90-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="37e90-161">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37e90-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


