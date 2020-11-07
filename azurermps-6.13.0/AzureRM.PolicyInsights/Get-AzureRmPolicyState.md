---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
ms.openlocfilehash: 6f5f1c341db0c5f57ffb541b9455369c0c6e5ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623749"
---
# <span data-ttu-id="ba807-101">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="ba807-101">Get-AzureRmPolicyState</span></span>

## <span data-ttu-id="ba807-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba807-102">SYNOPSIS</span></span>
<span data-ttu-id="ba807-103">取得資源的原則合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="ba807-103">Gets policy compliance states for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba807-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba807-104">SYNTAX</span></span>

### <span data-ttu-id="ba807-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ba807-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="ba807-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="ba807-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="ba807-108">ResourceScope</span></span>
```
Get-AzureRmPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="ba807-109">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="ba807-110">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="ba807-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba807-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="ba807-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba807-113">說明</span><span class="sxs-lookup"><span data-stu-id="ba807-113">DESCRIPTION</span></span>
<span data-ttu-id="ba807-114">取得資源的原則合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="ba807-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="ba807-115">您可以在不同的範圍中查詢原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="ba807-116">根據指定的時間間隔 (預設為 [最後一天]) ，可以查詢最新的原則狀態或所有原則狀態轉移。</span><span class="sxs-lookup"><span data-stu-id="ba807-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="ba807-117">您可以對結果進行篩選、群組和群組匯總的計算。</span><span class="sxs-lookup"><span data-stu-id="ba807-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="ba807-118">示例</span><span class="sxs-lookup"><span data-stu-id="ba807-118">EXAMPLES</span></span>

### <span data-ttu-id="ba807-119">範例1：在目前的訂閱範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState
```

<span data-ttu-id="ba807-120">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ba807-121">範例2：在指定的訂閱範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="ba807-122">針對指定訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="ba807-123">範例3：取得目前訂閱範圍中的所有原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -All
```

<span data-ttu-id="ba807-124">取得所有的歷史原則狀態記錄 (，包括在目前會話內容中訂閱中所有資源的最後一天所產生的最新) 。</span><span class="sxs-lookup"><span data-stu-id="ba807-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ba807-125">範例4：取得管理群組範圍中的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="ba807-126">針對指定管理群組中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="ba807-127">範例5：在目前訂閱的資源群組範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ba807-128">取得在目前會話內容) 的訂閱中，在最後一天內為指定資源群組中的所有資源所產生的最新原則狀態記錄 (。</span><span class="sxs-lookup"><span data-stu-id="ba807-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="ba807-129">範例6：在指定訂閱的資源群組範圍中取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ba807-130">取得指定的 [訂閱]) 中，在最後一天為指定資源群組中的所有資源所產生的最新原則狀態記錄 (。</span><span class="sxs-lookup"><span data-stu-id="ba807-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="ba807-131">範例7：取得資源的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="ba807-132">取得指定資源最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="ba807-133">範例8：在目前的訂閱中取得原則集定義的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ba807-134">取得目前會話內容中的所有資源在最後一天中產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中的原則集定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="ba807-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ba807-135">範例9：取得指定訂閱中原則集定義的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ba807-136">取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則集定義 (所影響。</span><span class="sxs-lookup"><span data-stu-id="ba807-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ba807-137">範例10：取得目前訂閱中原則定義的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ba807-138">取得目前會話內容中的所有資源在最後一天內所產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中之原則定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="ba807-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ba807-139">範例11：針對指定訂閱中的原則定義取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ba807-140">取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則定義 (所影響。</span><span class="sxs-lookup"><span data-stu-id="ba807-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ba807-141">範例12：取得目前訂閱中原則指派的最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ba807-142">取得目前會話內容中的所有資源在最後一天內所產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中之 (的原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="ba807-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ba807-143">範例13：針對指定訂閱中的原則指派取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ba807-144">取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="ba807-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ba807-145">範例14：針對目前訂閱中指定的資源群組中的原則指派取得最新原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ba807-146">取得目前會話內容的所有 (資源在最後一天中所產生的最新原則狀態記錄，) 目前會話內容) 中的 [資源] 群組中存在的指定原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="ba807-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="ba807-147">範例15：使用 OrderBy、Top 及 Select 查詢選項，在目前的訂閱範圍中取得最新的原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="ba807-148">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ba807-149">命令會依時間戳記與原則指派名稱屬性來排序結果，且只會取得那些順序中所列的前5名。</span><span class="sxs-lookup"><span data-stu-id="ba807-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="ba807-150">它也會選取，只列出每一筆記錄的資料行子集。</span><span class="sxs-lookup"><span data-stu-id="ba807-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="ba807-151">範例16：在目前的訂閱範圍中取得最新原則狀態，使用 From 和 To 查詢選項</span><span class="sxs-lookup"><span data-stu-id="ba807-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="ba807-152">取得在目前會話內容的訂閱中，在指定的日期範圍內產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ba807-153">範例17：使用篩選查詢選項，在目前的訂閱範圍中取得最新的原則狀態</span><span class="sxs-lookup"><span data-stu-id="ba807-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="ba807-154">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="ba807-155">此命令會根據原則定義動作所傳回的結果加以限制， (包括拒絕或審核動作) 、相容性狀態 (只包含不相容狀態) 與資源位置 (排除 eastus 位置) 。</span><span class="sxs-lookup"><span data-stu-id="ba807-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="ba807-156">範例18：在目前的訂閱範圍中取得最新原則狀態，並套用指定資料列計數匯總</span><span class="sxs-lookup"><span data-stu-id="ba807-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="ba807-157">取得目前會話內容中訂閱之所有資源在最後一天內產生的最新原則狀態記錄數。</span><span class="sxs-lookup"><span data-stu-id="ba807-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="ba807-158">命令只會傳回原則狀態記錄的計數，在 AdditionalProperties 屬性內傳回。</span><span class="sxs-lookup"><span data-stu-id="ba807-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="ba807-159">範例19：在目前的訂閱範圍中取得最新原則狀態，並套用 [使用匯總指定群組]</span><span class="sxs-lookup"><span data-stu-id="ba807-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="ba807-160">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ba807-161">此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="ba807-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="ba807-162">根據原則指派、原則集定義及原則定義來分組結果，然後計算每個群組中傳回的記錄數（在 AdditionalProperties 屬性內傳回）。</span><span class="sxs-lookup"><span data-stu-id="ba807-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="ba807-163">它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。</span><span class="sxs-lookup"><span data-stu-id="ba807-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="ba807-164">範例20：在目前的訂閱範圍中取得最新的原則狀態，並套用指定不含匯總的群組</span><span class="sxs-lookup"><span data-stu-id="ba807-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="ba807-165">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ba807-166">此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="ba807-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="ba807-167">它會根據資源識別碼來分組結果。這會產生與至少一個原則不相容的訂閱中所有資源的清單。</span><span class="sxs-lookup"><span data-stu-id="ba807-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="ba807-168">範例21：在目前的訂閱範圍中取得最新原則狀態，並套用指定多重群組</span><span class="sxs-lookup"><span data-stu-id="ba807-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="ba807-169">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="ba807-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ba807-170">此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="ba807-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="ba807-171">它會先根據原則指派、原則集定義、原則定義及資源識別碼，將結果分組。接著，它會進一步將此群組的結果與與資源識別碼不同的屬性組成群組，並計算在 AdditionalProperties 屬性內傳回的每個群組中的記錄數。</span><span class="sxs-lookup"><span data-stu-id="ba807-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="ba807-172">它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。</span><span class="sxs-lookup"><span data-stu-id="ba807-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="ba807-173">這會產生最多不相容資源數的前5個原則。</span><span class="sxs-lookup"><span data-stu-id="ba807-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="ba807-174">參數</span><span class="sxs-lookup"><span data-stu-id="ba807-174">PARAMETERS</span></span>

### <span data-ttu-id="ba807-175">-全部</span><span class="sxs-lookup"><span data-stu-id="ba807-175">-All</span></span>
<span data-ttu-id="ba807-176">在指定的時間間隔內，取得所有原則狀態，而不是最新的。</span><span class="sxs-lookup"><span data-stu-id="ba807-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="ba807-177">-套用</span><span class="sxs-lookup"><span data-stu-id="ba807-177">-Apply</span></span>
<span data-ttu-id="ba807-178">使用 OData 符號將運算式套用至匯總。</span><span class="sxs-lookup"><span data-stu-id="ba807-178">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="ba807-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba807-179">-DefaultProfile</span></span>
<span data-ttu-id="ba807-180">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba807-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba807-181">-篩選</span><span class="sxs-lookup"><span data-stu-id="ba807-181">-Filter</span></span>
<span data-ttu-id="ba807-182">使用 OData 符號篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="ba807-182">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="ba807-183">-從</span><span class="sxs-lookup"><span data-stu-id="ba807-183">-From</span></span>
<span data-ttu-id="ba807-184">ISO 8601 格式化的時間戳記，指定要查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="ba807-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="ba807-185">如果未指定，則預設為「To」參數值減去1天。</span><span class="sxs-lookup"><span data-stu-id="ba807-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="ba807-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ba807-186">-ManagementGroupName</span></span>
<span data-ttu-id="ba807-187">管理組名。</span><span class="sxs-lookup"><span data-stu-id="ba807-187">Management group name.</span></span>

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

### <span data-ttu-id="ba807-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ba807-188">-OrderBy</span></span>
<span data-ttu-id="ba807-189">使用 OData 符號排序運算式。</span><span class="sxs-lookup"><span data-stu-id="ba807-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="ba807-190">一或多個以逗號分隔的欄名稱，其中包含 [desc "預設) 或" asc " (。</span><span class="sxs-lookup"><span data-stu-id="ba807-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="ba807-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ba807-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="ba807-192">原則作業名稱。</span><span class="sxs-lookup"><span data-stu-id="ba807-192">Policy assignment name.</span></span>

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

### <span data-ttu-id="ba807-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ba807-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="ba807-194">原則定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ba807-194">Policy definition name.</span></span>

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

### <span data-ttu-id="ba807-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ba807-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="ba807-196">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ba807-196">Policy set definition name.</span></span>

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

### <span data-ttu-id="ba807-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba807-197">-ResourceGroupName</span></span>
<span data-ttu-id="ba807-198">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ba807-198">Resource group name.</span></span>

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

### <span data-ttu-id="ba807-199">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba807-199">-ResourceId</span></span>
<span data-ttu-id="ba807-200">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ba807-200">Resource ID.</span></span>

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

### <span data-ttu-id="ba807-201">-選取</span><span class="sxs-lookup"><span data-stu-id="ba807-201">-Select</span></span>
<span data-ttu-id="ba807-202">選取 [使用 OData 符號的運算式]。</span><span class="sxs-lookup"><span data-stu-id="ba807-202">Select expression using OData notation.</span></span>
<span data-ttu-id="ba807-203">一或多個以逗號分隔的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="ba807-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="ba807-204">將每筆記錄的欄限制為僅限所要求的資料行。</span><span class="sxs-lookup"><span data-stu-id="ba807-204">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="ba807-205">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba807-205">-SubscriptionId</span></span>
<span data-ttu-id="ba807-206">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ba807-206">Subscription ID.</span></span>

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

### <span data-ttu-id="ba807-207">-To</span><span class="sxs-lookup"><span data-stu-id="ba807-207">-To</span></span>
<span data-ttu-id="ba807-208">ISO 8601 格式化的時間戳記，指定要查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="ba807-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="ba807-209">如果未指定，則預設為要求的時間。</span><span class="sxs-lookup"><span data-stu-id="ba807-209">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="ba807-210">-上方</span><span class="sxs-lookup"><span data-stu-id="ba807-210">-Top</span></span>
<span data-ttu-id="ba807-211">要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="ba807-211">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="ba807-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba807-212">CommonParameters</span></span>
<span data-ttu-id="ba807-213">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba807-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba807-214">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba807-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba807-215">輸入</span><span class="sxs-lookup"><span data-stu-id="ba807-215">INPUTS</span></span>

### <span data-ttu-id="ba807-216">System.object</span><span class="sxs-lookup"><span data-stu-id="ba807-216">System.String</span></span>

## <span data-ttu-id="ba807-217">輸出</span><span class="sxs-lookup"><span data-stu-id="ba807-217">OUTPUTS</span></span>

### <span data-ttu-id="ba807-218">PolicyState 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="ba807-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="ba807-219">筆記</span><span class="sxs-lookup"><span data-stu-id="ba807-219">NOTES</span></span>

## <span data-ttu-id="ba807-220">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba807-220">RELATED LINKS</span></span>

[<span data-ttu-id="ba807-221">AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ba807-221">Get-AzureRmPolicyStateSummary</span></span>](./Get-AzureRmPolicyStateSummary.md)
