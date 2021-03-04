---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911386"
---
# <span data-ttu-id="e64a2-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e64a2-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="e64a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e64a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e64a2-103">在建立或更新資源時，獲得產生之策略評估事件。</span><span class="sxs-lookup"><span data-stu-id="e64a2-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="e64a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="e64a2-104">SYNTAX</span></span>

### <span data-ttu-id="e64a2-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="e64a2-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e64a2-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="e64a2-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e64a2-113">描述</span><span class="sxs-lookup"><span data-stu-id="e64a2-113">DESCRIPTION</span></span>
<span data-ttu-id="e64a2-114">在建立或更新資源時，獲得產生之策略評估事件。</span><span class="sxs-lookup"><span data-stu-id="e64a2-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="e64a2-115">根據預設為最後一天所指定的時間間隔， (以各種範圍查詢) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="e64a2-116">結果可以篩選、分組，也可以計算群組匯總。</span><span class="sxs-lookup"><span data-stu-id="e64a2-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="e64a2-117">例子</span><span class="sxs-lookup"><span data-stu-id="e64a2-117">EXAMPLES</span></span>

### <span data-ttu-id="e64a2-118">範例 1：取得目前訂閱範圍中的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="e64a2-119">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e64a2-120">範例 2：取得指定訂閱範圍中的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="e64a2-121">為指定訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="e64a2-122">範例 3：在管理群組範圍中取得策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="e64a2-123">為指定管理群組內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="e64a2-124">範例 4：取得目前訂閱中資源群組範圍中的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e64a2-125">針對指定資源群組內的所有資源，于最後一天產生 (目前會話上下文的訂閱) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="e64a2-126">範例 5：取得指定訂閱中資源群組範圍中的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e64a2-127">針對指定資源群組內的所有資源，于最後一天產生 (指定訂閱) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="e64a2-128">範例 6：取得資源的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="e64a2-129">為指定的資源，獲得最後一天產生的策略事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="e64a2-130">範例 7：取得目前訂閱中之策略集定義之政策事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e64a2-131">在目前的會話內容中 (租使用者內的所有資源 ，) 會受目前會話內容中訂閱中指定的 (定義影響) 而最後一天產生的所有資源之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e64a2-132">範例 8：取得指定訂閱中之策略集定義之策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e64a2-133">針對目前會話內容中租使用者內的所有資源 (在前一天產生) 受指定訂閱中指定的 (定義影響) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e64a2-134">範例 9：取得目前訂閱中之策略定義之政策事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e64a2-135">在目前的會話內容中 (租使用者內的所有資源 ，) 會受目前會話內容中訂閱中指定的 (影響，而最後一天產生的所有資源之政策事件記錄) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e64a2-136">範例 10：取得指定訂閱中之策略定義之政策事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e64a2-137">在租使用者目前的會話內容中， (在租使用者內的所有資源) 于最後一天產生 (受指定訂閱中指定的 (影響) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e64a2-138">範例 11：取得目前訂閱中之策略工作分派的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e64a2-139">在目前的會話內容中 (租使用者內的所有資源 ，) 會受目前會話內容中存在於訂閱中的指定 (影響之資源的最後一天產生) 之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e64a2-140">範例 12：取得指定訂閱中之策略工作分派的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e64a2-141">針對目前會話內容中租使用者內的所有資源 (在前一天產生) 受指定訂閱中指定的 (指派影響) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e64a2-142">範例 13：取得目前訂閱中指定資源群組中之策略工作分派的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e64a2-143">在目前的會話內容中 (租使用者內的所有資源 ，) 會受目前會話內容中訂閱中資源群組中指定的 (影響) 之最後一天產生的所有資源之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="e64a2-144">範例 14：使用 OrderBy、Top 和 Select 查詢選項，取得目前訂閱範圍中的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="e64a2-145">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e64a2-146">命令會按時間戳記和策略工作分派名稱屬性排序結果，並僅取用該順序所列的前 5 個。</span><span class="sxs-lookup"><span data-stu-id="e64a2-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="e64a2-147">它也選取只列出每一個記錄的欄子集。</span><span class="sxs-lookup"><span data-stu-id="e64a2-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="e64a2-148">範例 15：取得目前訂閱範圍中的策略事件，以及從和到查詢選項</span><span class="sxs-lookup"><span data-stu-id="e64a2-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="e64a2-149">在目前的會話內容中，為訂閱內的所有資源，在日期範圍內產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e64a2-150">範例 16：使用篩選查詢選項，取得目前訂閱範圍中的策略事件</span><span class="sxs-lookup"><span data-stu-id="e64a2-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="e64a2-151">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e64a2-152">命令會限制根據策略定義動作篩選的結果 (包括拒絕或稽核動作) 和資源位置 (排除 eastus 位置) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="e64a2-153">範例 17：取得目前訂閱範圍中的原則事件，使用 Apply 指定列計數匯總</span><span class="sxs-lookup"><span data-stu-id="e64a2-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="e64a2-154">在目前的會話內容中，為訂閱內的所有資源，獲得最後一天產生之政策事件記錄的數量。</span><span class="sxs-lookup"><span data-stu-id="e64a2-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e64a2-155">該命令僅會返回在 AdditionalProperties 屬性內所返回之策略事件記錄的計數。</span><span class="sxs-lookup"><span data-stu-id="e64a2-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="e64a2-156">範例 18：取得目前訂閱範圍中的原則事件，使用 Apply 指定群組與匯總</span><span class="sxs-lookup"><span data-stu-id="e64a2-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="e64a2-157">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e64a2-158">命令會限制根據策略定義動作篩選所 (僅包含稽核和拒絕事件) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="e64a2-159">它會根據策略指派、策略定義、策略定義動作和資源識別碼將結果組成群組，並計算每個群組中的記錄數目，此數目是在 AdditionalProperties 屬性內所返回。</span><span class="sxs-lookup"><span data-stu-id="e64a2-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="e64a2-160">它會根據計數匯總以遞減順序排序結果，而且只會取用該順序中列出的前 5 個結果。</span><span class="sxs-lookup"><span data-stu-id="e64a2-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="e64a2-161">範例 19：取得目前訂閱範圍中的原則事件，使用 Apply 指定群組而不匯總</span><span class="sxs-lookup"><span data-stu-id="e64a2-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="e64a2-162">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e64a2-163">命令會限制根據策略定義動作篩選所 (僅包含稽核和拒絕事件) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="e64a2-164">它會根據資源識別碼將結果分組。這會在訂閱內產生至少一個稽核或拒絕政策之政策事件的所有資源清單。</span><span class="sxs-lookup"><span data-stu-id="e64a2-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="e64a2-165">範例 20：取得目前訂閱範圍中的原則事件，使用 Apply 指定多個群組</span><span class="sxs-lookup"><span data-stu-id="e64a2-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="e64a2-166">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生之政策事件記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e64a2-167">命令會限制根據規則定義動作篩選所 (僅包含拒絕事件) 。</span><span class="sxs-lookup"><span data-stu-id="e64a2-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="e64a2-168">它會根據策略指派、政策定義和資源識別碼，先將結果組成群組。接著，它會使用資源識別碼以外的相同屬性進一步將此群組的結果分組，並計算每個群組中的記錄數目，此數目是在 AdditionalProperties 屬性內所返回。</span><span class="sxs-lookup"><span data-stu-id="e64a2-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="e64a2-169">它會根據計數匯總以遞減順序排序結果，而且只會取用該順序中列出的前 5 個結果。</span><span class="sxs-lookup"><span data-stu-id="e64a2-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="e64a2-170">這會產生拒絕資源數量最多的前 5 個拒絕策略。</span><span class="sxs-lookup"><span data-stu-id="e64a2-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="e64a2-171">參數</span><span class="sxs-lookup"><span data-stu-id="e64a2-171">PARAMETERS</span></span>

### <span data-ttu-id="e64a2-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="e64a2-172">-Apply</span></span>
<span data-ttu-id="e64a2-173">使用 OData 標記法將運算式適用于匯總。</span><span class="sxs-lookup"><span data-stu-id="e64a2-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="e64a2-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64a2-174">-DefaultProfile</span></span>
<span data-ttu-id="e64a2-175">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e64a2-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64a2-176">-篩選</span><span class="sxs-lookup"><span data-stu-id="e64a2-176">-Filter</span></span>
<span data-ttu-id="e64a2-177">使用 OData 標記法篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="e64a2-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="e64a2-178">-從</span><span class="sxs-lookup"><span data-stu-id="e64a2-178">-From</span></span>
<span data-ttu-id="e64a2-179">ISO 8601 格式化的時間戳記，指定查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="e64a2-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="e64a2-180">未指定時，預設為 "To" 參數值減 1 天。</span><span class="sxs-lookup"><span data-stu-id="e64a2-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="e64a2-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e64a2-181">-ManagementGroupName</span></span>
<span data-ttu-id="e64a2-182">管理組名。</span><span class="sxs-lookup"><span data-stu-id="e64a2-182">Management group name.</span></span>

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

### <span data-ttu-id="e64a2-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e64a2-183">-OrderBy</span></span>
<span data-ttu-id="e64a2-184">使用 OData 標記法排序運算式。</span><span class="sxs-lookup"><span data-stu-id="e64a2-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="e64a2-185">一或多個以逗號分隔的欄名稱，以及預設 (或'asc) 名稱。</span><span class="sxs-lookup"><span data-stu-id="e64a2-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="e64a2-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e64a2-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="e64a2-187">策略工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="e64a2-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="e64a2-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e64a2-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="e64a2-189">策略定義名稱。</span><span class="sxs-lookup"><span data-stu-id="e64a2-189">Policy definition name.</span></span>

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

### <span data-ttu-id="e64a2-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e64a2-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="e64a2-191">策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="e64a2-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="e64a2-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64a2-192">-ResourceGroupName</span></span>
<span data-ttu-id="e64a2-193">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e64a2-193">Resource group name.</span></span>

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

### <span data-ttu-id="e64a2-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e64a2-194">-ResourceId</span></span>
<span data-ttu-id="e64a2-195">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e64a2-195">Resource ID.</span></span>

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

### <span data-ttu-id="e64a2-196">-選取</span><span class="sxs-lookup"><span data-stu-id="e64a2-196">-Select</span></span>
<span data-ttu-id="e64a2-197">使用 OData 標記法選取運算式。</span><span class="sxs-lookup"><span data-stu-id="e64a2-197">Select expression using OData notation.</span></span>
<span data-ttu-id="e64a2-198">一或多個以逗號分隔的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="e64a2-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="e64a2-199">將每一個記錄上的欄限制為只有要求的記錄。</span><span class="sxs-lookup"><span data-stu-id="e64a2-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="e64a2-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e64a2-200">-SubscriptionId</span></span>
<span data-ttu-id="e64a2-201">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e64a2-201">Subscription ID.</span></span>

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

### <span data-ttu-id="e64a2-202">-To</span><span class="sxs-lookup"><span data-stu-id="e64a2-202">-To</span></span>
<span data-ttu-id="e64a2-203">ISO 8601 格式化的時間戳記，指定查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="e64a2-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="e64a2-204">未指定時，預設為要求時間。</span><span class="sxs-lookup"><span data-stu-id="e64a2-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="e64a2-205">-頂端</span><span class="sxs-lookup"><span data-stu-id="e64a2-205">-Top</span></span>
<span data-ttu-id="e64a2-206">要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="e64a2-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="e64a2-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64a2-207">CommonParameters</span></span>
<span data-ttu-id="e64a2-208">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e64a2-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64a2-209">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e64a2-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64a2-210">輸入</span><span class="sxs-lookup"><span data-stu-id="e64a2-210">INPUTS</span></span>

### <span data-ttu-id="e64a2-211">System.String</span><span class="sxs-lookup"><span data-stu-id="e64a2-211">System.String</span></span>

## <span data-ttu-id="e64a2-212">輸出</span><span class="sxs-lookup"><span data-stu-id="e64a2-212">OUTPUTS</span></span>

### <span data-ttu-id="e64a2-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e64a2-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="e64a2-214">筆記</span><span class="sxs-lookup"><span data-stu-id="e64a2-214">NOTES</span></span>

## <span data-ttu-id="e64a2-215">相關連結</span><span class="sxs-lookup"><span data-stu-id="e64a2-215">RELATED LINKS</span></span>
