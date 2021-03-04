---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: aeb86609e06417147f5ef4600c430665f28da454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911357"
---
# <span data-ttu-id="4c165-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4c165-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="4c165-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c165-102">SYNOPSIS</span></span>
<span data-ttu-id="4c165-103">建立並啟動策略工作分派的策略補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="4c165-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c165-104">SYNTAX</span></span>

### <span data-ttu-id="4c165-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="4c165-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c165-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c165-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c165-107">描述</span><span class="sxs-lookup"><span data-stu-id="4c165-107">DESCRIPTION</span></span>
<span data-ttu-id="4c165-108">**Start-AzPolicyRemediation** Cmdlet 會為特定的策略指派建立一個策略補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="4c165-109">所有在補救範圍以下的不符合規範資源都會進行補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="4c165-110">只有具有 'deployIfNotExists' 效果之政策才支援補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="4c165-111">例子</span><span class="sxs-lookup"><span data-stu-id="4c165-111">EXAMPLES</span></span>

### <span data-ttu-id="4c165-112">範例 1：在訂閱範圍開始修復</span><span class="sxs-lookup"><span data-stu-id="4c165-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="4c165-113">此命令會針對指定之策略指派，在訂閱的 '我的訂閱' 中建立新策略補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="4c165-114">範例 2：使用選擇性篩選在管理群組範圍開始補救</span><span class="sxs-lookup"><span data-stu-id="4c165-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="4c165-115">此命令會針對指定之策略指派，在管理群組 "mg1" 中建立新策略補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="4c165-116">只有 'westus' 或 'eastus' 位置中的資源會進行補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="4c165-117">範例 3：在資源群組範圍中開始修復一個策略集定義工作分派</span><span class="sxs-lookup"><span data-stu-id="4c165-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="4c165-118">此命令會針對指定之策略指派，在資源群組的 "myRG" 中建立新策略補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="4c165-119">該策略指派會指派一個 (定義，也稱為計畫) 。</span><span class="sxs-lookup"><span data-stu-id="4c165-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="4c165-120">該政策定義參照識別碼指出應補救計畫內哪些政策。</span><span class="sxs-lookup"><span data-stu-id="4c165-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="4c165-121">範例 4：開始修復，並等待它于背景中完成</span><span class="sxs-lookup"><span data-stu-id="4c165-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="4c165-122">此命令會針對指定之政策指派，在訂閱的 '我的訂閱' 中開始新的策略修復。</span><span class="sxs-lookup"><span data-stu-id="4c165-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="4c165-123">它會等待補救完成，再返回最終的補救狀態。</span><span class="sxs-lookup"><span data-stu-id="4c165-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="4c165-124">範例 5：開始補救，在修復之前，先探索不符合規範的資源</span><span class="sxs-lookup"><span data-stu-id="4c165-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="4c165-125">此命令會針對指定之策略指派，在訂閱的 '我的訂閱' 中建立新策略補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="4c165-126">訂閱中資源的合規性狀態會根據政策指派重新進行評估，而不符合規範的資源將會進行補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="4c165-127">參數</span><span class="sxs-lookup"><span data-stu-id="4c165-127">PARAMETERS</span></span>

### <span data-ttu-id="4c165-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c165-128">-AsJob</span></span>
<span data-ttu-id="4c165-129">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c165-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4c165-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c165-130">-DefaultProfile</span></span>
<span data-ttu-id="4c165-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c165-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c165-132">-位置篩選</span><span class="sxs-lookup"><span data-stu-id="4c165-132">-LocationFilter</span></span>
<span data-ttu-id="4c165-133">應包含在補救中的資源位置。</span><span class="sxs-lookup"><span data-stu-id="4c165-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="4c165-134">不位於這些位置的資源將不會補救。</span><span class="sxs-lookup"><span data-stu-id="4c165-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="4c165-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4c165-135">-ManagementGroupName</span></span>
<span data-ttu-id="4c165-136">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c165-136">Management group ID.</span></span>

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

### <span data-ttu-id="4c165-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c165-137">-Name</span></span>
<span data-ttu-id="4c165-138">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4c165-138">Resource name.</span></span>

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

### <span data-ttu-id="4c165-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="4c165-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="4c165-140">策略工作分派識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c165-140">Policy assignment ID.</span></span>
<span data-ttu-id="4c165-141">例如</span><span class="sxs-lookup"><span data-stu-id="4c165-141">E.g.</span></span>
<span data-ttu-id="4c165-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'。</span><span class="sxs-lookup"><span data-stu-id="4c165-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="4c165-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="4c165-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="4c165-144">獲得正在修復之個別定義之策略定義參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c165-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="4c165-145">當策略指派指派了一個策略集定義時，即為必填項。</span><span class="sxs-lookup"><span data-stu-id="4c165-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="4c165-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="4c165-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="4c165-147">說明補救工作將如何探索需要補救的資源。</span><span class="sxs-lookup"><span data-stu-id="4c165-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="4c165-148">修復管理群組範圍時，不支援 ReEvaluateCompliance。</span><span class="sxs-lookup"><span data-stu-id="4c165-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="4c165-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c165-149">-ResourceGroupName</span></span>
<span data-ttu-id="4c165-150">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4c165-150">Resource group name.</span></span>

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

### <span data-ttu-id="4c165-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c165-151">-ResourceId</span></span>
<span data-ttu-id="4c165-152">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c165-152">Resource ID.</span></span>

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

### <span data-ttu-id="4c165-153">-範圍</span><span class="sxs-lookup"><span data-stu-id="4c165-153">-Scope</span></span>
<span data-ttu-id="4c165-154">資源的範圍。</span><span class="sxs-lookup"><span data-stu-id="4c165-154">Scope of the resource.</span></span>
<span data-ttu-id="4c165-155">例如</span><span class="sxs-lookup"><span data-stu-id="4c165-155">E.g.</span></span>
<span data-ttu-id="4c165-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'。</span><span class="sxs-lookup"><span data-stu-id="4c165-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="4c165-157">-確認</span><span class="sxs-lookup"><span data-stu-id="4c165-157">-Confirm</span></span>
<span data-ttu-id="4c165-158">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4c165-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c165-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c165-159">-WhatIf</span></span>
<span data-ttu-id="4c165-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c165-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c165-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c165-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c165-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c165-162">CommonParameters</span></span>
<span data-ttu-id="4c165-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c165-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c165-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c165-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c165-165">輸入</span><span class="sxs-lookup"><span data-stu-id="4c165-165">INPUTS</span></span>

### <span data-ttu-id="4c165-166">System.String</span><span class="sxs-lookup"><span data-stu-id="4c165-166">System.String</span></span>

### <span data-ttu-id="4c165-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4c165-167">System.String[]</span></span>

## <span data-ttu-id="4c165-168">輸出</span><span class="sxs-lookup"><span data-stu-id="4c165-168">OUTPUTS</span></span>

### <span data-ttu-id="4c165-169">Microsoft.Azure.Commands.PolicyInsights.models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="4c165-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="4c165-170">筆記</span><span class="sxs-lookup"><span data-stu-id="4c165-170">NOTES</span></span>

## <span data-ttu-id="4c165-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c165-171">RELATED LINKS</span></span>
