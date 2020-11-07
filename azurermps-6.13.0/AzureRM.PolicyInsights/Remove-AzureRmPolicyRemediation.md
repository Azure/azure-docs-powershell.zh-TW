---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623747"
---
# <span data-ttu-id="e75c4-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e75c4-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="e75c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e75c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e75c4-103">刪除原則修正。</span><span class="sxs-lookup"><span data-stu-id="e75c4-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e75c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e75c4-104">SYNTAX</span></span>

### <span data-ttu-id="e75c4-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e75c4-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e75c4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e75c4-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e75c4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e75c4-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e75c4-108">說明</span><span class="sxs-lookup"><span data-stu-id="e75c4-108">DESCRIPTION</span></span>
<span data-ttu-id="e75c4-109">**AzureRmPolicyRemediation** Cmdlet 會刪除原則修正。</span><span class="sxs-lookup"><span data-stu-id="e75c4-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="e75c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="e75c4-110">EXAMPLES</span></span>

### <span data-ttu-id="e75c4-111">範例1：在資源群組範圍刪除原則修正</span><span class="sxs-lookup"><span data-stu-id="e75c4-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="e75c4-112">這個命令會在資源群組 ' myRG ' 中刪除名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="e75c4-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="e75c4-113">範例2：透過 [管道] 刪除管理群組修正</span><span class="sxs-lookup"><span data-stu-id="e75c4-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="e75c4-114">這個命令會從管理組 "mg1" 刪除名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="e75c4-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="e75c4-115">刪除資源前，會出現確認提示。</span><span class="sxs-lookup"><span data-stu-id="e75c4-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="e75c4-116">範例3：取消並刪除原則修正</span><span class="sxs-lookup"><span data-stu-id="e75c4-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="e75c4-117">這個命令會在資源群組 ' myRG ' 中刪除名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="e75c4-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="e75c4-118">如果修正程式正在進行中，將會取消，然後才會被刪除。</span><span class="sxs-lookup"><span data-stu-id="e75c4-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="e75c4-119">參數</span><span class="sxs-lookup"><span data-stu-id="e75c4-119">PARAMETERS</span></span>

### <span data-ttu-id="e75c4-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="e75c4-120">-AllowStop</span></span>
<span data-ttu-id="e75c4-121">允許修正程式在進行中時取消。</span><span class="sxs-lookup"><span data-stu-id="e75c4-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="e75c4-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e75c4-122">-AsJob</span></span>
<span data-ttu-id="e75c4-123">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e75c4-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e75c4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75c4-124">-DefaultProfile</span></span>
<span data-ttu-id="e75c4-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e75c4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e75c4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e75c4-126">-InputObject</span></span>
<span data-ttu-id="e75c4-127">修正物件。</span><span class="sxs-lookup"><span data-stu-id="e75c4-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c4-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e75c4-128">-ManagementGroupName</span></span>
<span data-ttu-id="e75c4-129">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e75c4-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c4-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="e75c4-130">-Name</span></span>
<span data-ttu-id="e75c4-131">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e75c4-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e75c4-132">-PassThru</span></span>
<span data-ttu-id="e75c4-133">如果命令順利完成，則傳回 True。</span><span class="sxs-lookup"><span data-stu-id="e75c4-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="e75c4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e75c4-134">-ResourceGroupName</span></span>
<span data-ttu-id="e75c4-135">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e75c4-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e75c4-136">-ResourceId</span></span>
<span data-ttu-id="e75c4-137">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e75c4-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c4-138">-範圍</span><span class="sxs-lookup"><span data-stu-id="e75c4-138">-Scope</span></span>
<span data-ttu-id="e75c4-139">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="e75c4-139">Scope of the resource.</span></span>
<span data-ttu-id="e75c4-140">例如.</span><span class="sxs-lookup"><span data-stu-id="e75c4-140">E.g.</span></span>
<span data-ttu-id="e75c4-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="e75c4-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c4-142">-確認</span><span class="sxs-lookup"><span data-stu-id="e75c4-142">-Confirm</span></span>
<span data-ttu-id="e75c4-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e75c4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e75c4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e75c4-144">-WhatIf</span></span>
<span data-ttu-id="e75c4-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e75c4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e75c4-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e75c4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e75c4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75c4-147">CommonParameters</span></span>
<span data-ttu-id="e75c4-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e75c4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75c4-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e75c4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75c4-150">輸入</span><span class="sxs-lookup"><span data-stu-id="e75c4-150">INPUTS</span></span>

### <span data-ttu-id="e75c4-151">System.object</span><span class="sxs-lookup"><span data-stu-id="e75c4-151">System.String</span></span>

### <span data-ttu-id="e75c4-152">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="e75c4-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="e75c4-153">輸出</span><span class="sxs-lookup"><span data-stu-id="e75c4-153">OUTPUTS</span></span>

### <span data-ttu-id="e75c4-154">System.object</span><span class="sxs-lookup"><span data-stu-id="e75c4-154">System.Boolean</span></span>

## <span data-ttu-id="e75c4-155">筆記</span><span class="sxs-lookup"><span data-stu-id="e75c4-155">NOTES</span></span>

## <span data-ttu-id="e75c4-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="e75c4-156">RELATED LINKS</span></span>