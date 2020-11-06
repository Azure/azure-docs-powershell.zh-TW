---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/start-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
ms.openlocfilehash: d5a0d4cd14f86c782defd7b70a1edee209982d2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447298"
---
# <span data-ttu-id="41030-101">Start-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="41030-101">Start-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="41030-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41030-102">SYNOPSIS</span></span>
<span data-ttu-id="41030-103">針對原則指派建立及啟動原則修正。</span><span class="sxs-lookup"><span data-stu-id="41030-103">Creates and starts a policy remediation for a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41030-104">句法</span><span class="sxs-lookup"><span data-stu-id="41030-104">SYNTAX</span></span>

### <span data-ttu-id="41030-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="41030-105">ByName (Default)</span></span>
```
Start-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41030-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41030-106">ByResourceId</span></span>
```
Start-AzureRmPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41030-107">說明</span><span class="sxs-lookup"><span data-stu-id="41030-107">DESCRIPTION</span></span>
<span data-ttu-id="41030-108">**AzureRmPolicyRemediation** Cmdlet 會針對特定原則指派建立原則修正。</span><span class="sxs-lookup"><span data-stu-id="41030-108">The **Start-AzureRmPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="41030-109">修正範圍或其下方的所有不相容資源都會修正。</span><span class="sxs-lookup"><span data-stu-id="41030-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="41030-110">只有「deployIfNotExists」效果的原則支援修正。</span><span class="sxs-lookup"><span data-stu-id="41030-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="41030-111">示例</span><span class="sxs-lookup"><span data-stu-id="41030-111">EXAMPLES</span></span>

### <span data-ttu-id="41030-112">範例1：在訂閱範圍中啟動修正</span><span class="sxs-lookup"><span data-stu-id="41030-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="41030-113">這個命令會在訂閱「我的訂閱」中針對指定原則指派建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="41030-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="41030-114">範例2：使用選用篩選在管理群組範圍中啟動修正</span><span class="sxs-lookup"><span data-stu-id="41030-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzureRmPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="41030-115">這個命令會針對指定原則指派，在管理群組 ' mg1」中建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="41030-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="41030-116">只有 ' westus」或「eastus」位置的資源會修正。</span><span class="sxs-lookup"><span data-stu-id="41030-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="41030-117">範例3：在原則集定義指派的資源群組範圍中啟動修正</span><span class="sxs-lookup"><span data-stu-id="41030-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzureRmPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="41030-118">這個命令會針對指定原則指派，在資源群組 ' myRG ' 中建立新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="41030-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="41030-119">原則指派指派原則集定義 (也稱為「方案」) 。</span><span class="sxs-lookup"><span data-stu-id="41030-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="41030-120">原則定義參考 ID 會指出應修正計畫中的哪個原則。</span><span class="sxs-lookup"><span data-stu-id="41030-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="41030-121">範例4：啟動修正並等待其在背景完成</span><span class="sxs-lookup"><span data-stu-id="41030-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="41030-122">這個命令會針對指定原則指派，在訂閱「我的訂閱」中啟動新的原則修正。</span><span class="sxs-lookup"><span data-stu-id="41030-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="41030-123">在返回最終修正狀態之前，它會等到修正程式完成為止。</span><span class="sxs-lookup"><span data-stu-id="41030-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="41030-124">參數</span><span class="sxs-lookup"><span data-stu-id="41030-124">PARAMETERS</span></span>

### <span data-ttu-id="41030-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41030-125">-AsJob</span></span>
<span data-ttu-id="41030-126">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41030-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="41030-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41030-127">-DefaultProfile</span></span>
<span data-ttu-id="41030-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41030-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41030-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="41030-129">-LocationFilter</span></span>
<span data-ttu-id="41030-130">應包含在修正中的資源位置。</span><span class="sxs-lookup"><span data-stu-id="41030-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="41030-131">不會修正位於這些位置的資源。</span><span class="sxs-lookup"><span data-stu-id="41030-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="41030-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="41030-132">-ManagementGroupName</span></span>
<span data-ttu-id="41030-133">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="41030-133">Management group ID.</span></span>

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

### <span data-ttu-id="41030-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="41030-134">-Name</span></span>
<span data-ttu-id="41030-135">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="41030-135">Resource name.</span></span>

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

### <span data-ttu-id="41030-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="41030-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="41030-137">原則指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="41030-137">Policy assignment ID.</span></span>
<span data-ttu-id="41030-138">例如.</span><span class="sxs-lookup"><span data-stu-id="41030-138">E.g.</span></span>
<span data-ttu-id="41030-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="41030-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="41030-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="41030-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="41030-141">取得要修正之個別定義的原則定義參考 ID。</span><span class="sxs-lookup"><span data-stu-id="41030-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="41030-142">當原則指派指派策略集定義時，需要。</span><span class="sxs-lookup"><span data-stu-id="41030-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="41030-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41030-143">-ResourceGroupName</span></span>
<span data-ttu-id="41030-144">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="41030-144">Resource group name.</span></span>

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

### <span data-ttu-id="41030-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41030-145">-ResourceId</span></span>
<span data-ttu-id="41030-146">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="41030-146">Resource ID.</span></span>

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

### <span data-ttu-id="41030-147">-範圍</span><span class="sxs-lookup"><span data-stu-id="41030-147">-Scope</span></span>
<span data-ttu-id="41030-148">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="41030-148">Scope of the resource.</span></span>
<span data-ttu-id="41030-149">例如.</span><span class="sxs-lookup"><span data-stu-id="41030-149">E.g.</span></span>
<span data-ttu-id="41030-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="41030-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="41030-151">-確認</span><span class="sxs-lookup"><span data-stu-id="41030-151">-Confirm</span></span>
<span data-ttu-id="41030-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41030-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41030-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41030-153">-WhatIf</span></span>
<span data-ttu-id="41030-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41030-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41030-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41030-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41030-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41030-156">CommonParameters</span></span>
<span data-ttu-id="41030-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41030-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41030-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41030-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41030-159">輸入</span><span class="sxs-lookup"><span data-stu-id="41030-159">INPUTS</span></span>

### <span data-ttu-id="41030-160">System.object</span><span class="sxs-lookup"><span data-stu-id="41030-160">System.String</span></span>

### <span data-ttu-id="41030-161">System.object []</span><span class="sxs-lookup"><span data-stu-id="41030-161">System.String[]</span></span>

## <span data-ttu-id="41030-162">輸出</span><span class="sxs-lookup"><span data-stu-id="41030-162">OUTPUTS</span></span>

### <span data-ttu-id="41030-163">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="41030-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="41030-164">筆記</span><span class="sxs-lookup"><span data-stu-id="41030-164">NOTES</span></span>

## <span data-ttu-id="41030-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="41030-165">RELATED LINKS</span></span>
