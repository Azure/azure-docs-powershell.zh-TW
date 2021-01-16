---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435686"
---
# <span data-ttu-id="75941-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="75941-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="75941-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75941-102">SYNOPSIS</span></span>
<span data-ttu-id="75941-103">取得建立或更新資源時產生的原則評估事件。</span><span class="sxs-lookup"><span data-stu-id="75941-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="75941-104">句法</span><span class="sxs-lookup"><span data-stu-id="75941-104">SYNTAX</span></span>

### <span data-ttu-id="75941-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="75941-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="75941-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="75941-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="75941-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="75941-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="75941-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="75941-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75941-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="75941-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75941-113">說明</span><span class="sxs-lookup"><span data-stu-id="75941-113">DESCRIPTION</span></span>
<span data-ttu-id="75941-114">取得建立或更新資源時產生的原則評估事件。</span><span class="sxs-lookup"><span data-stu-id="75941-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="75941-115">您可以根據 (預設為 [最後一天]) 中指定的時間間隔，在不同的範圍中查詢原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="75941-116">您可以對結果進行篩選、群組和群組匯總的計算。</span><span class="sxs-lookup"><span data-stu-id="75941-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="75941-117">示例</span><span class="sxs-lookup"><span data-stu-id="75941-117">EXAMPLES</span></span>

### <span data-ttu-id="75941-118">範例1：在目前的訂閱範圍中取得原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="75941-119">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="75941-120">範例2：在指定的訂閱範圍中取得原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="75941-121">針對指定訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="75941-122">範例3：在管理群組範圍中取得原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="75941-123">針對指定管理群組中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="75941-124">範例4：在目前訂閱的資源群組範圍中取得原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="75941-125">取得在目前會話內容) 的訂閱中，在前一天內為指定資源群組中的所有資源所產生的原則事件記錄 (。</span><span class="sxs-lookup"><span data-stu-id="75941-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="75941-126">範例5：在指定訂閱的資源群組範圍中取得原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="75941-127">取得指定之資源群組中的所有資源在最後一天產生的原則事件記錄， (在指定的訂閱) 中。</span><span class="sxs-lookup"><span data-stu-id="75941-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="75941-128">範例6：取得資源的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="75941-129">取得指定資源最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="75941-130">範例7：在目前的訂閱中取得原則集定義的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75941-131">取得在目前會話內容) 中，在訂閱中的所有資源 (在 () 中的所有資源所產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="75941-132">範例8：在指定的訂閱中取得原則集定義的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75941-133">取得在目前會話內容的租使用者中，在最後一天產生的原則事件記錄，) 在指定的訂閱) 中存在的指定原則集定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="75941-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="75941-134">範例9：在目前的訂閱中取得原則定義的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75941-135">取得在目前會話內容的租使用者中，在最後一天為所有資源 (所產生的原則事件記錄) 受指定原則定義 (所產生的原則，) 中存在於訂閱中。</span><span class="sxs-lookup"><span data-stu-id="75941-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="75941-136">範例10：取得指定訂閱中原則定義的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75941-137">取得在目前會話內容的租使用者中的所有資源 (所產生的原則事件記錄，) 在指定的訂閱) 中存在的指定原則定義 (所影響。</span><span class="sxs-lookup"><span data-stu-id="75941-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="75941-138">範例11：取得目前訂閱中原則指派的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="75941-139">取得在目前會話內容的租使用者中，在最後一天為所有資源所產生的原則事件記錄 ()  (在目前會話內容) 中存在的訂閱中。</span><span class="sxs-lookup"><span data-stu-id="75941-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="75941-140">範例12：取得指定訂閱中原則指派的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="75941-141">取得在目前會話內容的租使用者中的所有資源 (所產生的原則事件記錄) 在指定的訂閱) 中存在的指定原則指派 (所影響。</span><span class="sxs-lookup"><span data-stu-id="75941-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="75941-142">範例13：在目前訂閱的指定資源群組中取得原則指派的原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="75941-143">取得在目前會話內容的租使用者的 [資源] 群組中所產生的所有資源 (在最後一天所產生的原則事件記錄 () ) 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="75941-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="75941-144">範例14：在目前的訂閱範圍中取得原則事件，使用 OrderBy、Top 及 Select 查詢選項</span><span class="sxs-lookup"><span data-stu-id="75941-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="75941-145">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="75941-146">命令會依時間戳記與原則指派名稱屬性來排序結果，且只會取得那些順序中所列的前5名。</span><span class="sxs-lookup"><span data-stu-id="75941-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="75941-147">它也會選取，只列出每一筆記錄的資料行子集。</span><span class="sxs-lookup"><span data-stu-id="75941-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="75941-148">範例15：在目前的訂閱範圍中取得原則事件，使用 [寄件者] 和 [至] 查詢選項</span><span class="sxs-lookup"><span data-stu-id="75941-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="75941-149">取得在指定的日期範圍內產生的原則事件記錄（在目前會話內容中，訂閱中的所有資源所指定）。</span><span class="sxs-lookup"><span data-stu-id="75941-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="75941-150">範例16：使用篩選查詢選項，在目前的訂閱範圍中取得原則事件</span><span class="sxs-lookup"><span data-stu-id="75941-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="75941-151">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="75941-152">此命令會根據原則定義動作來限制篩選所傳回的結果 (包括拒絕或審核動作) 與資源位置 (排除 eastus 位置) 。</span><span class="sxs-lookup"><span data-stu-id="75941-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="75941-153">範例17：在目前的訂閱範圍中取得原則事件，並套用指定資料行數匯總</span><span class="sxs-lookup"><span data-stu-id="75941-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="75941-154">取得目前會話內容中訂閱中所有資源在最後一天產生的原則事件記錄數目。</span><span class="sxs-lookup"><span data-stu-id="75941-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="75941-155">命令只會傳回原則事件記錄的計數，在 AdditionalProperties 屬性內傳回。</span><span class="sxs-lookup"><span data-stu-id="75941-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="75941-156">範例18：在目前的訂閱範圍中取得原則事件，並套用含匯總的指定群組</span><span class="sxs-lookup"><span data-stu-id="75941-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="75941-157">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="75941-158">此命令會根據原則定義動作的篩選所傳回的結果加以限制， (只包含審核和拒絕事件) 。</span><span class="sxs-lookup"><span data-stu-id="75941-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="75941-159">它會根據原則指派、原則定義、原則定義動作和資源識別碼來針對結果進行分組，然後計算每個群組中傳回的記錄數（在 AdditionalProperties 屬性內傳回）。</span><span class="sxs-lookup"><span data-stu-id="75941-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="75941-160">它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。</span><span class="sxs-lookup"><span data-stu-id="75941-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="75941-161">範例19：在目前的訂閱範圍中取得原則事件，並套用指定不含匯總的群組</span><span class="sxs-lookup"><span data-stu-id="75941-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="75941-162">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="75941-163">此命令會根據原則定義動作的篩選所傳回的結果加以限制， (只包含審核和拒絕事件) 。</span><span class="sxs-lookup"><span data-stu-id="75941-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="75941-164">它會根據資源識別碼來分組結果。這會產生訂閱中的所有資源清單，其中包含至少一個審核或拒絕原則所產生的原則事件。</span><span class="sxs-lookup"><span data-stu-id="75941-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="75941-165">範例20：在目前的訂閱範圍中取得原則事件，並套用指定多個群組</span><span class="sxs-lookup"><span data-stu-id="75941-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="75941-166">針對目前會話內容中訂閱中的所有資源，取得最後一天產生的原則事件記錄。</span><span class="sxs-lookup"><span data-stu-id="75941-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="75941-167">這個命令會根據原則定義動作來限制篩選所傳回的結果 (只包含拒絕事件) 。</span><span class="sxs-lookup"><span data-stu-id="75941-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="75941-168">它會根據原則指派、原則定義及資源識別碼，先將結果分組。接著，它會進一步將此群組的結果與與資源識別碼不同的屬性組成群組，並計算在 AdditionalProperties 屬性內傳回的每個群組中的記錄數。</span><span class="sxs-lookup"><span data-stu-id="75941-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="75941-169">它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。</span><span class="sxs-lookup"><span data-stu-id="75941-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="75941-170">這會產生最多已拒絕資源數的前5個拒絕原則。</span><span class="sxs-lookup"><span data-stu-id="75941-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="75941-171">參數</span><span class="sxs-lookup"><span data-stu-id="75941-171">PARAMETERS</span></span>

### <span data-ttu-id="75941-172">-套用</span><span class="sxs-lookup"><span data-stu-id="75941-172">-Apply</span></span>
<span data-ttu-id="75941-173">使用 OData 符號將運算式套用至匯總。</span><span class="sxs-lookup"><span data-stu-id="75941-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="75941-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75941-174">-DefaultProfile</span></span>
<span data-ttu-id="75941-175">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75941-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75941-176">-篩選</span><span class="sxs-lookup"><span data-stu-id="75941-176">-Filter</span></span>
<span data-ttu-id="75941-177">使用 OData 符號篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="75941-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="75941-178">-從</span><span class="sxs-lookup"><span data-stu-id="75941-178">-From</span></span>
<span data-ttu-id="75941-179">ISO 8601 格式化的時間戳記，指定要查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="75941-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="75941-180">如果未指定，則預設為「To」參數值減去1天。</span><span class="sxs-lookup"><span data-stu-id="75941-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="75941-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="75941-181">-ManagementGroupName</span></span>
<span data-ttu-id="75941-182">管理組名。</span><span class="sxs-lookup"><span data-stu-id="75941-182">Management group name.</span></span>

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

### <span data-ttu-id="75941-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="75941-183">-OrderBy</span></span>
<span data-ttu-id="75941-184">使用 OData 符號排序運算式。</span><span class="sxs-lookup"><span data-stu-id="75941-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="75941-185">一或多個以逗號分隔的欄名稱，其中包含 [desc "預設) 或" asc " (。</span><span class="sxs-lookup"><span data-stu-id="75941-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="75941-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="75941-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="75941-187">原則作業名稱。</span><span class="sxs-lookup"><span data-stu-id="75941-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="75941-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="75941-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="75941-189">原則定義名稱。</span><span class="sxs-lookup"><span data-stu-id="75941-189">Policy definition name.</span></span>

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

### <span data-ttu-id="75941-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="75941-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="75941-191">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="75941-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="75941-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75941-192">-ResourceGroupName</span></span>
<span data-ttu-id="75941-193">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="75941-193">Resource group name.</span></span>

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

### <span data-ttu-id="75941-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75941-194">-ResourceId</span></span>
<span data-ttu-id="75941-195">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="75941-195">Resource ID.</span></span>

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

### <span data-ttu-id="75941-196">-選取</span><span class="sxs-lookup"><span data-stu-id="75941-196">-Select</span></span>
<span data-ttu-id="75941-197">選取 [使用 OData 符號的運算式]。</span><span class="sxs-lookup"><span data-stu-id="75941-197">Select expression using OData notation.</span></span>
<span data-ttu-id="75941-198">一或多個以逗號分隔的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="75941-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="75941-199">將每筆記錄的欄限制為僅限所要求的資料行。</span><span class="sxs-lookup"><span data-stu-id="75941-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="75941-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75941-200">-SubscriptionId</span></span>
<span data-ttu-id="75941-201">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="75941-201">Subscription ID.</span></span>

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

### <span data-ttu-id="75941-202">-To</span><span class="sxs-lookup"><span data-stu-id="75941-202">-To</span></span>
<span data-ttu-id="75941-203">ISO 8601 格式化的時間戳記，指定要查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="75941-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="75941-204">如果未指定，則預設為要求的時間。</span><span class="sxs-lookup"><span data-stu-id="75941-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="75941-205">-上方</span><span class="sxs-lookup"><span data-stu-id="75941-205">-Top</span></span>
<span data-ttu-id="75941-206">要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="75941-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="75941-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75941-207">CommonParameters</span></span>
<span data-ttu-id="75941-208">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75941-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75941-209">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75941-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75941-210">輸入</span><span class="sxs-lookup"><span data-stu-id="75941-210">INPUTS</span></span>

### <span data-ttu-id="75941-211">System.object</span><span class="sxs-lookup"><span data-stu-id="75941-211">System.String</span></span>

## <span data-ttu-id="75941-212">輸出</span><span class="sxs-lookup"><span data-stu-id="75941-212">OUTPUTS</span></span>

### <span data-ttu-id="75941-213">PolicyEvent 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="75941-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="75941-214">筆記</span><span class="sxs-lookup"><span data-stu-id="75941-214">NOTES</span></span>

## <span data-ttu-id="75941-215">相關連結</span><span class="sxs-lookup"><span data-stu-id="75941-215">RELATED LINKS</span></span>
