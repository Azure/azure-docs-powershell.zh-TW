---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911365"
---
# <span data-ttu-id="15c46-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="15c46-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="15c46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15c46-102">SYNOPSIS</span></span>
<span data-ttu-id="15c46-103">為資源獲取政策合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="15c46-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="15c46-104">語法</span><span class="sxs-lookup"><span data-stu-id="15c46-104">SYNTAX</span></span>

### <span data-ttu-id="15c46-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="15c46-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="15c46-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="15c46-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="15c46-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="15c46-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="15c46-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="15c46-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c46-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="15c46-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c46-113">描述</span><span class="sxs-lookup"><span data-stu-id="15c46-113">DESCRIPTION</span></span>
<span data-ttu-id="15c46-114">為資源獲取政策合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="15c46-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="15c46-115">可以在各種範圍中查詢策略狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="15c46-116">根據指定的時間間隔 (預設為最後一天) ，可以查詢最新的政策狀態或所有政策狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="15c46-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="15c46-117">結果可以篩選、分組，也可以計算群組匯總。</span><span class="sxs-lookup"><span data-stu-id="15c46-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="15c46-118">例子</span><span class="sxs-lookup"><span data-stu-id="15c46-118">EXAMPLES</span></span>

### <span data-ttu-id="15c46-119">範例 1：取得目前訂閱範圍中的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="15c46-120">在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="15c46-121">範例 2：取得指定訂閱範圍中的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="15c46-122">為指定訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="15c46-123">範例 3：取得目前訂閱範圍的所有策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="15c46-124">在所有歷史政策狀態記錄中 (包括) 目前會話內容中，訂閱內所有資源最後一天產生的最新記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="15c46-125">範例 4：取得管理群組範圍中的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="15c46-126">為指定管理群組內的所有資源，獲得過去一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="15c46-127">範例 5：取得目前訂閱中資源群組範圍中的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="15c46-128">在訂閱的目前會話內容中，針對指定資源群組內的所有資源， (過去一天產生的最新) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="15c46-129">範例 6：取得指定訂閱中資源群組範圍中的最新策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="15c46-130">針對指定資源群組內的所有資源，于最後一天產生的最新 (指定訂閱) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="15c46-131">範例 7：取得資源的最新策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="15c46-132">為指定的資源，獲得最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="15c46-133">範例 8：取得目前訂閱中之策略集定義的最新策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="15c46-134">在目前的會話內容中 (租使用者內的所有資源) 受目前會話內容中之訂閱中指定的 (定義影響) ，最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="15c46-135">範例 9：取得指定訂閱中之策略集定義的最新策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="15c46-136">針對目前會話內容中租使用者內的所有資源 (過去一天產生的最新政策狀態記錄) 受指定訂閱環境中指定的 (定義影響) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="15c46-137">範例 10：取得目前訂閱中之策略定義的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="15c46-138">在目前的會話內容中 (租使用者內的所有資源) 會受目前會話內容中存在於訂閱中的指定 (影響，而最後一天產生的所有資源的最新政策狀態記錄) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="15c46-139">範例 11：取得指定訂閱中之策略定義的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="15c46-140">在租使用者目前的會話內容中， (在租使用者內的所有資源) 在前一天產生的最新政策狀態記錄 (會受指定訂閱) 中指定的) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="15c46-141">範例 12：取得目前訂閱中之策略工作分派的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="15c46-142">在目前的會話內容中 (租使用者內的所有資源) 在前一天產生的最新政策狀態記錄 (會受目前會話內容中訂閱中指定的) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="15c46-143">範例 13：取得指定訂閱中之策略指派的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="15c46-144">在目前的會話內容中 (租使用者內的所有資源) 會受指定訂閱環境中指定的 (影響 (產生的最新政策狀態記錄) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="15c46-145">範例 14：取得目前訂閱中指定資源群組中之策略工作分派的最新政策狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="15c46-146">在目前的會話內容中 (租使用者內的所有資源 ，) 會受目前會話內容中訂閱中資源群組中指定的 (影響，而最後一天產生的最新政策狀態記錄) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="15c46-147">範例 15：使用 OrderBy、Top 和 Select 查詢選項，取得目前訂閱範圍中的最新策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="15c46-148">在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="15c46-149">命令會按時間戳記和策略工作分派名稱屬性排序結果，並僅取用該順序所列的前 5 個。</span><span class="sxs-lookup"><span data-stu-id="15c46-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="15c46-150">它也選取只列出每一個記錄的欄子集。</span><span class="sxs-lookup"><span data-stu-id="15c46-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="15c46-151">範例 16：取得目前訂閱範圍中的最新策略狀態，以及從和到查詢選項</span><span class="sxs-lookup"><span data-stu-id="15c46-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="15c46-152">在目前的會話內容中，為訂閱內的所有資源，在日期範圍內產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="15c46-153">範例 17：使用篩選查詢選項，取得目前訂閱範圍中的最新策略狀態</span><span class="sxs-lookup"><span data-stu-id="15c46-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="15c46-154">在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="15c46-155">命令會根據策略定義動作 (包含拒絕或稽核動作) 、合規性狀態 (僅包含不符合規範的狀態) 和資源位置 (排除 eastus 位置) 來限制篩選的結果。</span><span class="sxs-lookup"><span data-stu-id="15c46-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="15c46-156">範例 18：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定列計數匯總</span><span class="sxs-lookup"><span data-stu-id="15c46-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="15c46-157">在目前的會話內容中，為訂閱內的所有資源，獲得最後一天產生的最新政策狀態記錄數目。</span><span class="sxs-lookup"><span data-stu-id="15c46-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="15c46-158">該命令僅會返回在 AdditionalProperties 屬性內所返回之策略狀態記錄的計數。</span><span class="sxs-lookup"><span data-stu-id="15c46-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="15c46-159">範例 19：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定群組與匯總</span><span class="sxs-lookup"><span data-stu-id="15c46-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="15c46-160">在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="15c46-161">命令會根據合規性狀態限制篩選所 (只包含不符合規範的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="15c46-162">它會根據策略指派、策略集定義和策略定義將結果組成群組，並計算每個群組中的記錄數目，此數目是在 AdditionalProperties 屬性內所返回。</span><span class="sxs-lookup"><span data-stu-id="15c46-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="15c46-163">它會根據計數匯總以遞減順序排序結果，而且只會取用該順序中列出的前 5 個結果。</span><span class="sxs-lookup"><span data-stu-id="15c46-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="15c46-164">範例 20：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定群組而不匯總</span><span class="sxs-lookup"><span data-stu-id="15c46-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="15c46-165">在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="15c46-166">命令會根據合規性狀態限制篩選所 (只包含不符合規範的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="15c46-167">它會根據資源識別碼將結果分組。這會在訂閱內產生至少一個不符合一個政策之所有資源的清單。</span><span class="sxs-lookup"><span data-stu-id="15c46-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="15c46-168">範例 21：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定多個群組</span><span class="sxs-lookup"><span data-stu-id="15c46-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="15c46-169">範例 22：取得最新的策略狀態，包括資源的策略評估詳細資料</span><span class="sxs-lookup"><span data-stu-id="15c46-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="15c46-170">在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="15c46-171">命令會根據合規性狀態限制篩選所 (只包含不符合規範的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="15c46-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="15c46-172">它會根據策略指派、策略集定義、策略定義和資源識別碼，先將結果組成群組。接著，它會使用資源識別碼以外的相同屬性進一步將此群組的結果分組，並計算每個群組中的記錄數目，此數目是在 AdditionalProperties 屬性內所返回。</span><span class="sxs-lookup"><span data-stu-id="15c46-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="15c46-173">它會根據計數匯總以遞減順序排序結果，而且只會取用該順序中列出的前 5 個結果。</span><span class="sxs-lookup"><span data-stu-id="15c46-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="15c46-174">這會產生最符合規範資源的前 5 個策略。</span><span class="sxs-lookup"><span data-stu-id="15c46-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="15c46-175">參數</span><span class="sxs-lookup"><span data-stu-id="15c46-175">PARAMETERS</span></span>

### <span data-ttu-id="15c46-176">-全部</span><span class="sxs-lookup"><span data-stu-id="15c46-176">-All</span></span>
<span data-ttu-id="15c46-177">在指定的時間間隔內，取得所有政策狀態，而不是只取得最新的狀態。</span><span class="sxs-lookup"><span data-stu-id="15c46-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="15c46-178">-Apply</span><span class="sxs-lookup"><span data-stu-id="15c46-178">-Apply</span></span>
<span data-ttu-id="15c46-179">使用 OData 標記法將運算式適用于匯總。</span><span class="sxs-lookup"><span data-stu-id="15c46-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="15c46-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c46-180">-DefaultProfile</span></span>
<span data-ttu-id="15c46-181">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15c46-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c46-182">-展開</span><span class="sxs-lookup"><span data-stu-id="15c46-182">-Expand</span></span>
<span data-ttu-id="15c46-183">使用 OData 標記法展開運算式。</span><span class="sxs-lookup"><span data-stu-id="15c46-183">Expand expression using OData notation.</span></span>

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

### <span data-ttu-id="15c46-184">-篩選</span><span class="sxs-lookup"><span data-stu-id="15c46-184">-Filter</span></span>
<span data-ttu-id="15c46-185">使用 OData 標記法篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="15c46-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="15c46-186">-從</span><span class="sxs-lookup"><span data-stu-id="15c46-186">-From</span></span>
<span data-ttu-id="15c46-187">ISO 8601 格式化的時間戳記，指定查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="15c46-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="15c46-188">未指定時，預設為 "To" 參數值減 1 天。</span><span class="sxs-lookup"><span data-stu-id="15c46-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="15c46-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="15c46-189">-ManagementGroupName</span></span>
<span data-ttu-id="15c46-190">管理組名。</span><span class="sxs-lookup"><span data-stu-id="15c46-190">Management group name.</span></span>

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

### <span data-ttu-id="15c46-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="15c46-191">-OrderBy</span></span>
<span data-ttu-id="15c46-192">使用 OData 標記法排序運算式。</span><span class="sxs-lookup"><span data-stu-id="15c46-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="15c46-193">一或多個以逗號分隔的欄名稱，以及預設 (或'asc) 名稱。</span><span class="sxs-lookup"><span data-stu-id="15c46-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="15c46-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="15c46-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="15c46-195">策略工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="15c46-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="15c46-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="15c46-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="15c46-197">策略定義名稱。</span><span class="sxs-lookup"><span data-stu-id="15c46-197">Policy definition name.</span></span>

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

### <span data-ttu-id="15c46-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="15c46-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="15c46-199">策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="15c46-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="15c46-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c46-200">-ResourceGroupName</span></span>
<span data-ttu-id="15c46-201">資源組名。</span><span class="sxs-lookup"><span data-stu-id="15c46-201">Resource group name.</span></span>

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

### <span data-ttu-id="15c46-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15c46-202">-ResourceId</span></span>
<span data-ttu-id="15c46-203">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="15c46-203">Resource ID.</span></span>

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

### <span data-ttu-id="15c46-204">-選取</span><span class="sxs-lookup"><span data-stu-id="15c46-204">-Select</span></span>
<span data-ttu-id="15c46-205">使用 OData 標記法選取運算式。</span><span class="sxs-lookup"><span data-stu-id="15c46-205">Select expression using OData notation.</span></span>
<span data-ttu-id="15c46-206">一或多個以逗號分隔的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="15c46-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="15c46-207">將每一個記錄上的欄限制為只有要求的記錄。</span><span class="sxs-lookup"><span data-stu-id="15c46-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="15c46-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15c46-208">-SubscriptionId</span></span>
<span data-ttu-id="15c46-209">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="15c46-209">Subscription ID.</span></span>

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

### <span data-ttu-id="15c46-210">-To</span><span class="sxs-lookup"><span data-stu-id="15c46-210">-To</span></span>
<span data-ttu-id="15c46-211">ISO 8601 格式化的時間戳記，指定查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="15c46-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="15c46-212">未指定時，預設為要求時間。</span><span class="sxs-lookup"><span data-stu-id="15c46-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="15c46-213">-頂端</span><span class="sxs-lookup"><span data-stu-id="15c46-213">-Top</span></span>
<span data-ttu-id="15c46-214">要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="15c46-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="15c46-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c46-215">CommonParameters</span></span>
<span data-ttu-id="15c46-216">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15c46-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c46-217">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15c46-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c46-218">輸入</span><span class="sxs-lookup"><span data-stu-id="15c46-218">INPUTS</span></span>

### <span data-ttu-id="15c46-219">System.String</span><span class="sxs-lookup"><span data-stu-id="15c46-219">System.String</span></span>

## <span data-ttu-id="15c46-220">輸出</span><span class="sxs-lookup"><span data-stu-id="15c46-220">OUTPUTS</span></span>

### <span data-ttu-id="15c46-221">Microsoft.Azure.Commands.PolicyInsights.models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="15c46-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="15c46-222">筆記</span><span class="sxs-lookup"><span data-stu-id="15c46-222">NOTES</span></span>

## <span data-ttu-id="15c46-223">相關連結</span><span class="sxs-lookup"><span data-stu-id="15c46-223">RELATED LINKS</span></span>

[<span data-ttu-id="15c46-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="15c46-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
