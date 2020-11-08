---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138315"
---
# <span data-ttu-id="8c60c-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8c60c-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="8c60c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c60c-102">SYNOPSIS</span></span>
<span data-ttu-id="8c60c-103">取得資源的原則合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="8c60c-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="8c60c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c60c-104">SYNTAX</span></span>

### <span data-ttu-id="8c60c-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="8c60c-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c60c-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="8c60c-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c60c-113">說明</span><span class="sxs-lookup"><span data-stu-id="8c60c-113">DESCRIPTION</span></span>
<span data-ttu-id="8c60c-114">取得資源的原則合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="8c60c-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="8c60c-115">您可以在不同的範圍中查詢原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="8c60c-116">根據指定的時間間隔 (預設為 [最後一天]) ，可以查詢最新的原則狀態或所有原則狀態轉移。</span><span class="sxs-lookup"><span data-stu-id="8c60c-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="8c60c-117">您可以對結果進行篩選、群組和群組匯總的計算。</span><span class="sxs-lookup"><span data-stu-id="8c60c-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="8c60c-118">示例</span><span class="sxs-lookup"><span data-stu-id="8c60c-118">EXAMPLES</span></span>

### <span data-ttu-id="8c60c-119">範例1：在目前的訂閱範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="8c60c-120">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c60c-121">範例2：在指定的訂閱範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="8c60c-122">針對指定訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="8c60c-123">範例3：取得目前訂閱範圍中的所有原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="8c60c-124">取得所有的歷史原則狀態記錄 (，包括在目前會話內容中訂閱中所有資源的最後一天所產生的最新) 。</span><span class="sxs-lookup"><span data-stu-id="8c60c-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c60c-125">範例4：取得管理群組範圍中的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="8c60c-126">針對指定管理群組中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="8c60c-127">範例5：在目前訂閱的資源群組範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="8c60c-128">取得在目前會話內容) 的訂閱中，在最後一天內為指定資源群組中的所有資源所產生的最新原則狀態記錄 (。</span><span class="sxs-lookup"><span data-stu-id="8c60c-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="8c60c-129">範例6：在指定訂閱的資源群組範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="8c60c-130">取得指定的 [訂閱]) 中，在最後一天為指定資源群組中的所有資源所產生的最新原則狀態記錄 (。</span><span class="sxs-lookup"><span data-stu-id="8c60c-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="8c60c-131">範例7：取得資源的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="8c60c-132">取得指定資源最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="8c60c-133">範例8：在目前的訂閱中取得原則集定義的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c60c-134">取得目前會話內容中的所有資源在最後一天中產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中的原則集定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="8c60c-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c60c-135">範例9：取得指定訂閱中原則集定義的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c60c-136">取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則集定義 (所影響。</span><span class="sxs-lookup"><span data-stu-id="8c60c-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c60c-137">範例10：取得目前訂閱中原則定義的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c60c-138">取得目前會話內容中的所有資源在最後一天內所產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中之原則定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="8c60c-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c60c-139">範例11：針對指定訂閱中的原則定義取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c60c-140">取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則定義 (所影響。</span><span class="sxs-lookup"><span data-stu-id="8c60c-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c60c-141">範例12：取得目前訂閱中原則指派的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c60c-142">取得目前會話內容中的所有資源在最後一天內所產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中之 (的原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="8c60c-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c60c-143">範例13：針對指定訂閱中的原則指派取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c60c-144">取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="8c60c-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c60c-145">範例14：針對目前訂閱中指定的資源群組中的原則指派取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c60c-146">取得目前會話內容的所有 (資源在最後一天中所產生的最新原則狀態記錄，) 目前會話內容) 中的 [資源] 群組中存在的指定原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="8c60c-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="8c60c-147">範例15：使用 OrderBy、Top 及 Select 查詢選項，在目前的訂閱範圍中取得最新的原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="8c60c-148">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c60c-149">命令會依時間戳記與原則指派名稱屬性來排序結果，且只會取得那些順序中所列的前5名。</span><span class="sxs-lookup"><span data-stu-id="8c60c-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="8c60c-150">它也會選取，只列出每一筆記錄的資料行子集。</span><span class="sxs-lookup"><span data-stu-id="8c60c-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="8c60c-151">範例16：在目前的訂閱範圍中取得最新原則狀態，使用 From 和 To 查詢選項</span><span class="sxs-lookup"><span data-stu-id="8c60c-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="8c60c-152">取得在目前會話內容的訂閱中，在指定的日期範圍內產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c60c-153">範例17：使用篩選查詢選項，在目前的訂閱範圍中取得最新的原則狀態</span><span class="sxs-lookup"><span data-stu-id="8c60c-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="8c60c-154">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="8c60c-155">此命令會根據原則定義動作所傳回的結果加以限制， (包括拒絕或審核動作) 、相容性狀態 (只包含不相容狀態) 與資源位置 (排除 eastus 位置) 。</span><span class="sxs-lookup"><span data-stu-id="8c60c-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="8c60c-156">範例18：在目前的訂閱範圍中取得最新原則狀態，並套用指定資料列計數匯總</span><span class="sxs-lookup"><span data-stu-id="8c60c-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="8c60c-157">取得目前會話內容中訂閱之所有資源在最後一天內產生的最新原則狀態記錄數。</span><span class="sxs-lookup"><span data-stu-id="8c60c-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="8c60c-158">命令只會傳回原則狀態記錄的計數，在 AdditionalProperties 屬性內傳回。</span><span class="sxs-lookup"><span data-stu-id="8c60c-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="8c60c-159">範例19：在目前的訂閱範圍中取得最新原則狀態，並套用 [使用匯總指定群組]</span><span class="sxs-lookup"><span data-stu-id="8c60c-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="8c60c-160">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c60c-161">此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="8c60c-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c60c-162">根據原則指派、原則集定義及原則定義來分組結果，然後計算每個群組中傳回的記錄數（在 AdditionalProperties 屬性內傳回）。</span><span class="sxs-lookup"><span data-stu-id="8c60c-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="8c60c-163">它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。</span><span class="sxs-lookup"><span data-stu-id="8c60c-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="8c60c-164">範例20：在目前的訂閱範圍中取得最新的原則狀態，並套用指定不含匯總的群組</span><span class="sxs-lookup"><span data-stu-id="8c60c-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="8c60c-165">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c60c-166">此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="8c60c-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c60c-167">它會根據資源識別碼來分組結果。這會產生與至少一個原則不相容的訂閱中所有資源的清單。</span><span class="sxs-lookup"><span data-stu-id="8c60c-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="8c60c-168">範例21：在目前的訂閱範圍中取得最新原則狀態，並套用指定多重群組</span><span class="sxs-lookup"><span data-stu-id="8c60c-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="8c60c-169">範例22：取得最新的原則狀態，包括資源的原則評估詳細資料</span><span class="sxs-lookup"><span data-stu-id="8c60c-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="8c60c-170">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="8c60c-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c60c-171">此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="8c60c-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c60c-172">它會先根據原則指派、原則集定義、原則定義及資源識別碼，將結果分組。接著，它會進一步將此群組的結果與與資源識別碼不同的屬性組成群組，並計算在 AdditionalProperties 屬性內傳回的每個群組中的記錄數。</span><span class="sxs-lookup"><span data-stu-id="8c60c-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="8c60c-173">它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。</span><span class="sxs-lookup"><span data-stu-id="8c60c-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="8c60c-174">這會產生最多不相容資源數的前5個原則。</span><span class="sxs-lookup"><span data-stu-id="8c60c-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="8c60c-175">參數</span><span class="sxs-lookup"><span data-stu-id="8c60c-175">PARAMETERS</span></span>

### <span data-ttu-id="8c60c-176">-全部</span><span class="sxs-lookup"><span data-stu-id="8c60c-176">-All</span></span>
<span data-ttu-id="8c60c-177">在指定的時間間隔內，取得所有原則狀態，而不是最新的。</span><span class="sxs-lookup"><span data-stu-id="8c60c-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="8c60c-178">-套用</span><span class="sxs-lookup"><span data-stu-id="8c60c-178">-Apply</span></span>
<span data-ttu-id="8c60c-179">使用 OData 符號將運算式套用至匯總。</span><span class="sxs-lookup"><span data-stu-id="8c60c-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="8c60c-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c60c-180">-DefaultProfile</span></span>
<span data-ttu-id="8c60c-181">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c60c-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c60c-182">-展開</span><span class="sxs-lookup"><span data-stu-id="8c60c-182">-Expand</span></span>
<span data-ttu-id="8c60c-183">使用 OData 符號展開 expression。</span><span class="sxs-lookup"><span data-stu-id="8c60c-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-184">-篩選</span><span class="sxs-lookup"><span data-stu-id="8c60c-184">-Filter</span></span>
<span data-ttu-id="8c60c-185">使用 OData 符號篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="8c60c-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="8c60c-186">-從</span><span class="sxs-lookup"><span data-stu-id="8c60c-186">-From</span></span>
<span data-ttu-id="8c60c-187">ISO 8601 格式化的時間戳記，指定要查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="8c60c-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="8c60c-188">如果未指定，則預設為「To」參數值減去1天。</span><span class="sxs-lookup"><span data-stu-id="8c60c-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8c60c-189">-ManagementGroupName</span></span>
<span data-ttu-id="8c60c-190">管理組名。</span><span class="sxs-lookup"><span data-stu-id="8c60c-190">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="8c60c-191">-OrderBy</span></span>
<span data-ttu-id="8c60c-192">使用 OData 符號排序運算式。</span><span class="sxs-lookup"><span data-stu-id="8c60c-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="8c60c-193">一或多個以逗號分隔的欄名稱，其中包含 [desc "預設) 或" asc " (。</span><span class="sxs-lookup"><span data-stu-id="8c60c-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="8c60c-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="8c60c-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="8c60c-195">原則作業名稱。</span><span class="sxs-lookup"><span data-stu-id="8c60c-195">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8c60c-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="8c60c-197">原則定義名稱。</span><span class="sxs-lookup"><span data-stu-id="8c60c-197">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8c60c-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="8c60c-199">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="8c60c-199">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c60c-200">-ResourceGroupName</span></span>
<span data-ttu-id="8c60c-201">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8c60c-201">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c60c-202">-ResourceId</span></span>
<span data-ttu-id="8c60c-203">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8c60c-203">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-204">-選取</span><span class="sxs-lookup"><span data-stu-id="8c60c-204">-Select</span></span>
<span data-ttu-id="8c60c-205">選取 [使用 OData 符號的運算式]。</span><span class="sxs-lookup"><span data-stu-id="8c60c-205">Select expression using OData notation.</span></span>
<span data-ttu-id="8c60c-206">一或多個以逗號分隔的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="8c60c-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="8c60c-207">將每筆記錄的欄限制為僅限所要求的資料行。</span><span class="sxs-lookup"><span data-stu-id="8c60c-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="8c60c-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c60c-208">-SubscriptionId</span></span>
<span data-ttu-id="8c60c-209">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8c60c-209">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-210">-To</span><span class="sxs-lookup"><span data-stu-id="8c60c-210">-To</span></span>
<span data-ttu-id="8c60c-211">ISO 8601 格式化的時間戳記，指定要查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="8c60c-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="8c60c-212">如果未指定，則預設為要求的時間。</span><span class="sxs-lookup"><span data-stu-id="8c60c-212">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-213">-上方</span><span class="sxs-lookup"><span data-stu-id="8c60c-213">-Top</span></span>
<span data-ttu-id="8c60c-214">要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="8c60c-214">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c60c-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c60c-215">CommonParameters</span></span>
<span data-ttu-id="8c60c-216">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c60c-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c60c-217">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c60c-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c60c-218">輸入</span><span class="sxs-lookup"><span data-stu-id="8c60c-218">INPUTS</span></span>

### <span data-ttu-id="8c60c-219">System.object</span><span class="sxs-lookup"><span data-stu-id="8c60c-219">System.String</span></span>

## <span data-ttu-id="8c60c-220">輸出</span><span class="sxs-lookup"><span data-stu-id="8c60c-220">OUTPUTS</span></span>

### <span data-ttu-id="8c60c-221">PolicyState 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="8c60c-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="8c60c-222">筆記</span><span class="sxs-lookup"><span data-stu-id="8c60c-222">NOTES</span></span>

## <span data-ttu-id="8c60c-223">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c60c-223">RELATED LINKS</span></span>

[<span data-ttu-id="8c60c-224">AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8c60c-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
