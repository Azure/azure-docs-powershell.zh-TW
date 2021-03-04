---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911362"
---
# <span data-ttu-id="7b4f2-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="7b4f2-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="7b4f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4f2-103">獲得資源的最新政策合規性狀態摘要。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="7b4f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b4f2-104">SYNTAX</span></span>

### <span data-ttu-id="7b4f2-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="7b4f2-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b4f2-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="7b4f2-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b4f2-113">描述</span><span class="sxs-lookup"><span data-stu-id="7b4f2-113">DESCRIPTION</span></span>
<span data-ttu-id="7b4f2-114">從不同範圍中，以摘要方式查看最新的政策合規性狀態號碼，細分為政策指派和策略定義。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="7b4f2-115">它只包含不符合規定狀態。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="7b4f2-116">例子</span><span class="sxs-lookup"><span data-stu-id="7b4f2-116">EXAMPLES</span></span>

### <span data-ttu-id="7b4f2-117">範例 1：取得目前訂閱範圍中最新的不相容性政策狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="7b4f2-118">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生的最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="7b4f2-119">範例 2：取得指定訂閱範圍中最新的不相容性政策狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="7b4f2-120">針對指定訂閱內的所有資源，獲得過去一天產生的最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="7b4f2-121">範例 3：在管理群組範圍中取得最新的不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="7b4f2-122">針對指定管理群組內的所有資源，獲得過去一天產生的最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="7b4f2-123">範例 4：取得目前訂閱中資源群組範圍中最新的不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="7b4f2-124">針對訂閱中指定資源群組內的所有資源 ，于最後一天產生的最新政策合規性狀態摘要 (目前會話內容中的) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="7b4f2-125">範例 5：取得指定訂閱中資源群組範圍中最新的不相容性政策狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="7b4f2-126">針對指定訂閱訂閱中指定資源群組內的所有資源，于最後一天產生的最新 (狀態摘要) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="7b4f2-127">範例 6：取得資源的最新不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="7b4f2-128">獲得指定資源最後一天所產生之最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="7b4f2-129">範例 7：取得目前訂閱中之策略集定義的最新不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="7b4f2-130">針對租使用者內所有資源 (在目前的會話內容中) 受目前會話內容中訂閱中指定的策略集定義 (影響的所有資源，最後一天產生的最新政策合規性狀態摘要視圖) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="7b4f2-131">範例 8：取得指定訂閱中之策略集定義的最新不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="7b4f2-132">針對租使用者內所有資源 ， (在目前的會話內容中) 受指定訂閱 (中指定的策略集定義 (影響的所有資源，獲得最後一天產生的最新政策合規性狀態摘要) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="7b4f2-133">範例 9：取得目前訂閱中之策略定義的最新不相容性政策狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="7b4f2-134">針對租使用者內所有資源 (在目前的會話內容中) 受目前會話內容中存在於訂閱中的指定政策定義 (影響的所有資源，獲得最後一天產生的最新政策合規性狀態摘要) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="7b4f2-135">範例 10：取得指定訂閱中之策略定義的最新不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="7b4f2-136">針對租使用者內所有資源 (在目前的會話內容中) 受指定訂閱 (中指定的策略定義 (影響的所有資源，獲得最後一天產生的最新政策合規性狀態摘要) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="7b4f2-137">範例 11：取得目前訂閱中之策略工作分派的最新不相容性政策狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="7b4f2-138">針對租使用者內所有資源 (目前會話內容中) 受目前會話內容中存在於訂閱中的指定策略指派 (影響的所有資源，最後一天產生的最新政策合規性狀態摘要) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="7b4f2-139">範例 12：取得指定訂閱中之策略工作分派的最新不相容性政策狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="7b4f2-140">針對租使用者內所有資源 (在目前的會話內容中) 受指定訂閱 (中指定的策略指派影響之所有資源 ，最後一天產生的最新政策合規性狀態摘要) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="7b4f2-141">範例 13：取得目前訂閱中指定資源群組中之策略工作分派的最新不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="7b4f2-142">針對租使用者內所有資源 (目前會話內容中) 受目前會話內容中訂閱中資源群組中指定的策略指派 (影響的所有資源，最後一天產生的最新政策合規性狀態摘要視圖) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="7b4f2-143">範例 14：使用 Top 查詢選項，取得目前訂閱範圍中最新的不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="7b4f2-144">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生的最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="7b4f2-145">該命令會以不相容的資源計數遞減順序排序結果中的策略工作分派摘要，並且只會佔用那些策略工作分派摘要的前 5 個。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="7b4f2-146">範例 15：取得目前訂閱範圍中最新的不相容性政策狀態摘要，以及 From 和 To 查詢選項</span><span class="sxs-lookup"><span data-stu-id="7b4f2-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="7b4f2-147">在目前的會話內容中，為訂閱內所有資源指定的日期範圍內產生的最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="7b4f2-148">範例 16：使用篩選查詢選項，取得目前訂閱範圍中最新的不符合規定狀態摘要</span><span class="sxs-lookup"><span data-stu-id="7b4f2-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="7b4f2-149">在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生的最新政策合規性狀態摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="7b4f2-150">命令會限制根據策略定義動作篩選的結果 (包括拒絕或稽核動作) ，而資源位置 (排除 eastus 位置) 。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="7b4f2-151">參數</span><span class="sxs-lookup"><span data-stu-id="7b4f2-151">PARAMETERS</span></span>

### <span data-ttu-id="7b4f2-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4f2-152">-DefaultProfile</span></span>
<span data-ttu-id="7b4f2-153">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b4f2-154">-篩選</span><span class="sxs-lookup"><span data-stu-id="7b4f2-154">-Filter</span></span>
<span data-ttu-id="7b4f2-155">使用 OData 標記法篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="7b4f2-156">-從</span><span class="sxs-lookup"><span data-stu-id="7b4f2-156">-From</span></span>
<span data-ttu-id="7b4f2-157">ISO 8601 格式化的時間戳記，指定查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="7b4f2-158">未指定時，預設為 "To" 參數值減 1 天。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="7b4f2-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7b4f2-159">-ManagementGroupName</span></span>
<span data-ttu-id="7b4f2-160">管理組名。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-160">Management group name.</span></span>

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

### <span data-ttu-id="7b4f2-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="7b4f2-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="7b4f2-162">策略工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="7b4f2-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7b4f2-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="7b4f2-164">策略定義名稱。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-164">Policy definition name.</span></span>

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

### <span data-ttu-id="7b4f2-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7b4f2-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="7b4f2-166">策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="7b4f2-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b4f2-167">-ResourceGroupName</span></span>
<span data-ttu-id="7b4f2-168">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-168">Resource group name.</span></span>

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

### <span data-ttu-id="7b4f2-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b4f2-169">-ResourceId</span></span>
<span data-ttu-id="7b4f2-170">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-170">Resource ID.</span></span>

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

### <span data-ttu-id="7b4f2-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b4f2-171">-SubscriptionId</span></span>
<span data-ttu-id="7b4f2-172">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-172">Subscription ID.</span></span>

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

### <span data-ttu-id="7b4f2-173">-To</span><span class="sxs-lookup"><span data-stu-id="7b4f2-173">-To</span></span>
<span data-ttu-id="7b4f2-174">ISO 8601 格式化的時間戳記，指定查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="7b4f2-175">未指定時，預設為要求時間。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="7b4f2-176">-頂端</span><span class="sxs-lookup"><span data-stu-id="7b4f2-176">-Top</span></span>
<span data-ttu-id="7b4f2-177">要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="7b4f2-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4f2-178">CommonParameters</span></span>
<span data-ttu-id="7b4f2-179">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b4f2-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4f2-180">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b4f2-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4f2-181">輸入</span><span class="sxs-lookup"><span data-stu-id="7b4f2-181">INPUTS</span></span>

### <span data-ttu-id="7b4f2-182">System.String</span><span class="sxs-lookup"><span data-stu-id="7b4f2-182">System.String</span></span>

## <span data-ttu-id="7b4f2-183">輸出</span><span class="sxs-lookup"><span data-stu-id="7b4f2-183">OUTPUTS</span></span>

### <span data-ttu-id="7b4f2-184">Microsoft.Azure.Commands.PolicyInsights.models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="7b4f2-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="7b4f2-185">筆記</span><span class="sxs-lookup"><span data-stu-id="7b4f2-185">NOTES</span></span>

## <span data-ttu-id="7b4f2-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b4f2-186">RELATED LINKS</span></span>

[<span data-ttu-id="7b4f2-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7b4f2-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
