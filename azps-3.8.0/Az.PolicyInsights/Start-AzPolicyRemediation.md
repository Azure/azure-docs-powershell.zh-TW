---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958911"
---
# <span data-ttu-id="a05e0-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a05e0-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="a05e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a05e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a05e0-103">針對原則指派建立及啟動原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="a05e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a05e0-104">SYNTAX</span></span>

### <span data-ttu-id="a05e0-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a05e0-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a05e0-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a05e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="a05e0-107">DESCRIPTION</span></span>
<span data-ttu-id="a05e0-108">**AzPolicyRemediation** Cmdlet 會針對特定原則指派建立原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="a05e0-109">修正範圍或其下方的所有不相容資源都會修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="a05e0-110">只有「deployIfNotExists」效果的原則支援修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="a05e0-111">示例</span><span class="sxs-lookup"><span data-stu-id="a05e0-111">EXAMPLES</span></span>

### <span data-ttu-id="a05e0-112">範例1：在訂閱範圍中啟動修正</span><span class="sxs-lookup"><span data-stu-id="a05e0-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="a05e0-113">這個命令會在訂閱「我的訂閱」中針對指定原則指派建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="a05e0-114">範例2：使用選用篩選在管理群組範圍中啟動修正</span><span class="sxs-lookup"><span data-stu-id="a05e0-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="a05e0-115">這個命令會針對指定原則指派，在管理群組 ' mg1」中建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="a05e0-116">只有 ' westus」或「eastus」位置的資源會修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="a05e0-117">範例3：在原則集定義指派的資源群組範圍中啟動修正</span><span class="sxs-lookup"><span data-stu-id="a05e0-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="a05e0-118">這個命令會針對指定原則指派，在資源群組 ' myRG ' 中建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="a05e0-119">原則指派指派原則集定義 (也稱為「方案」) 。</span><span class="sxs-lookup"><span data-stu-id="a05e0-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="a05e0-120">原則定義參考 ID 會指出應修正計畫中的哪個原則。</span><span class="sxs-lookup"><span data-stu-id="a05e0-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="a05e0-121">範例4：啟動修正並等待其在背景完成</span><span class="sxs-lookup"><span data-stu-id="a05e0-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="a05e0-122">這個命令會針對指定原則指派，在訂閱「我的訂閱」中啟動新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="a05e0-123">在返回最終修正狀態之前，它會等到修正程式完成為止。</span><span class="sxs-lookup"><span data-stu-id="a05e0-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="a05e0-124">範例5：啟動修正程式，以在修正前發現不相容的資源</span><span class="sxs-lookup"><span data-stu-id="a05e0-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="a05e0-125">這個命令會在訂閱「我的訂閱」中針對指定原則指派建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="a05e0-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="a05e0-126">訂閱中資源的合規性狀態會根據原則指派和不相容的資源來重新評估。</span><span class="sxs-lookup"><span data-stu-id="a05e0-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="a05e0-127">參數</span><span class="sxs-lookup"><span data-stu-id="a05e0-127">PARAMETERS</span></span>

### <span data-ttu-id="a05e0-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a05e0-128">-AsJob</span></span>
<span data-ttu-id="a05e0-129">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a05e0-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a05e0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05e0-130">-DefaultProfile</span></span>
<span data-ttu-id="a05e0-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a05e0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05e0-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="a05e0-132">-LocationFilter</span></span>
<span data-ttu-id="a05e0-133">應包含在修正中的資源位置。</span><span class="sxs-lookup"><span data-stu-id="a05e0-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="a05e0-134">不會修正位於這些位置的資源。</span><span class="sxs-lookup"><span data-stu-id="a05e0-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05e0-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a05e0-135">-ManagementGroupName</span></span>
<span data-ttu-id="a05e0-136">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a05e0-136">Management group ID.</span></span>

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

### <span data-ttu-id="a05e0-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="a05e0-137">-Name</span></span>
<span data-ttu-id="a05e0-138">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a05e0-138">Resource name.</span></span>

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

### <span data-ttu-id="a05e0-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="a05e0-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="a05e0-140">原則指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="a05e0-140">Policy assignment ID.</span></span>
<span data-ttu-id="a05e0-141">例如.</span><span class="sxs-lookup"><span data-stu-id="a05e0-141">E.g.</span></span>
<span data-ttu-id="a05e0-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="a05e0-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="a05e0-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="a05e0-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="a05e0-144">取得要修正之個別定義的原則定義參考 ID。</span><span class="sxs-lookup"><span data-stu-id="a05e0-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="a05e0-145">當原則指派指派策略集定義時，需要。</span><span class="sxs-lookup"><span data-stu-id="a05e0-145">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05e0-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="a05e0-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="a05e0-147">說明修正任務將如何發現需要修正的資源。</span><span class="sxs-lookup"><span data-stu-id="a05e0-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="a05e0-148">修正管理群組範圍時，不支援 ReEvaluateCompliance。</span><span class="sxs-lookup"><span data-stu-id="a05e0-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05e0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05e0-149">-ResourceGroupName</span></span>
<span data-ttu-id="a05e0-150">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a05e0-150">Resource group name.</span></span>

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

### <span data-ttu-id="a05e0-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a05e0-151">-ResourceId</span></span>
<span data-ttu-id="a05e0-152">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a05e0-152">Resource ID.</span></span>

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

### <span data-ttu-id="a05e0-153">-範圍</span><span class="sxs-lookup"><span data-stu-id="a05e0-153">-Scope</span></span>
<span data-ttu-id="a05e0-154">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="a05e0-154">Scope of the resource.</span></span>
<span data-ttu-id="a05e0-155">例如.</span><span class="sxs-lookup"><span data-stu-id="a05e0-155">E.g.</span></span>
<span data-ttu-id="a05e0-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="a05e0-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="a05e0-157">-確認</span><span class="sxs-lookup"><span data-stu-id="a05e0-157">-Confirm</span></span>
<span data-ttu-id="a05e0-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a05e0-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05e0-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05e0-159">-WhatIf</span></span>
<span data-ttu-id="a05e0-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a05e0-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05e0-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a05e0-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05e0-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05e0-162">CommonParameters</span></span>
<span data-ttu-id="a05e0-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a05e0-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05e0-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a05e0-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05e0-165">輸入</span><span class="sxs-lookup"><span data-stu-id="a05e0-165">INPUTS</span></span>

### <span data-ttu-id="a05e0-166">System.object</span><span class="sxs-lookup"><span data-stu-id="a05e0-166">System.String</span></span>

### <span data-ttu-id="a05e0-167">System.object []</span><span class="sxs-lookup"><span data-stu-id="a05e0-167">System.String[]</span></span>

## <span data-ttu-id="a05e0-168">輸出</span><span class="sxs-lookup"><span data-stu-id="a05e0-168">OUTPUTS</span></span>

### <span data-ttu-id="a05e0-169">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="a05e0-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a05e0-170">筆記</span><span class="sxs-lookup"><span data-stu-id="a05e0-170">NOTES</span></span>

## <span data-ttu-id="a05e0-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="a05e0-171">RELATED LINKS</span></span>
