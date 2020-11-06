---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447302"
---
# <span data-ttu-id="ed142-101">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ed142-101">Get-AzureRmPolicyStateSummary</span></span>

## <span data-ttu-id="ed142-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-102">SYNOPSIS</span></span>
<span data-ttu-id="ed142-103">取得資源的最新原則規範狀態摘要。</span><span class="sxs-lookup"><span data-stu-id="ed142-103">Gets latest policy compliance states summary for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed142-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed142-104">SYNTAX</span></span>

### <span data-ttu-id="ed142-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ed142-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed142-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="ed142-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed142-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="ed142-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed142-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="ed142-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed142-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="ed142-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed142-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="ed142-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed142-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="ed142-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed142-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="ed142-112">ResourceScope</span></span>
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed142-113">說明</span><span class="sxs-lookup"><span data-stu-id="ed142-113">DESCRIPTION</span></span>
<span data-ttu-id="ed142-114">取得各種作用中的最新原則合規性狀態編號摘要視圖，細分為原則指派與原則定義。</span><span class="sxs-lookup"><span data-stu-id="ed142-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="ed142-115">它只包含不相容的原則狀態。</span><span class="sxs-lookup"><span data-stu-id="ed142-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="ed142-116">示例</span><span class="sxs-lookup"><span data-stu-id="ed142-116">EXAMPLES</span></span>

### <span data-ttu-id="ed142-117">範例1：取得目前訂閱範圍中的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

<span data-ttu-id="ed142-118">取得目前會話內容中訂閱中所有資源在最後一天產生之最新原則合規性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ed142-119">範例2：取得指定訂閱範圍中的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="ed142-120">取得指定訂閱內所有資源之最後一天產生之最新原則規範狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="ed142-121">範例3：取得管理群組範圍中的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="ed142-122">取得指定管理群組內所有資源之最後一天產生之最新原則合規性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="ed142-123">範例4：取得目前訂閱之資源群組範圍中的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ed142-124">取得在目前會話內容) 的訂閱中，在最後一天內為指定資源 (群組中的所有資源所產生之最新原則相容性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="ed142-125">範例5：取得指定訂閱之資源群組範圍中的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ed142-126">取得指定之資源群組中的所有資源在最後一天內所產生之最新原則規範狀態的摘要視圖， (于指定的訂閱) 中。</span><span class="sxs-lookup"><span data-stu-id="ed142-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="ed142-127">範例6：取得資源的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="ed142-128">取得指定資源最後一天產生之最新原則合規性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="ed142-129">範例7：取得目前訂閱中原則集定義的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ed142-130">取得目前會話內容) 中的所有資源在) 租使用者的最後一天中所產生之最新原則符合性狀態的摘要視圖， (在訂閱中存在的指定原則集定義 (。</span><span class="sxs-lookup"><span data-stu-id="ed142-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ed142-131">範例8：取得指定訂閱中原則集定義的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ed142-132">取得在目前會話內容的租使用者中的所有資源所產生之最新原則相容性狀態的摘要視圖，) 在指定的訂閱) 中存在的指定原則集定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="ed142-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ed142-133">範例9：取得目前訂閱中原則定義的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ed142-134">取得目前會話內容中的租使用者中的所有資源在前一天內所產生之最新原則相容性狀態的摘要視圖，) 在目前會話內容) 中存在於訂閱中之原則定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="ed142-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ed142-135">範例10：取得指定訂閱中原則定義的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ed142-136">取得在目前會話內容的租使用者中的所有資源所產生之最新原則相容性狀態的摘要視圖，) 在指定的訂閱) 中存在的指定原則定義 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="ed142-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ed142-137">範例11：取得目前訂閱中原則指派的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ed142-138">取得目前會話內容中，在所有資源的最後一天所產生的最新原則相容性狀態的摘要視圖，) 在目前會話內容) 中的訂閱中， (在訂閱中存在的特定原則指派 (。</span><span class="sxs-lookup"><span data-stu-id="ed142-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ed142-139">範例12：取得指定訂閱中原則指派的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ed142-140">取得在目前會話內容的租使用者中的所有資源所產生之最新原則相容性狀態的摘要視圖，) 在指定的訂閱) 中存在的指定原則指派 (所影響的 (。</span><span class="sxs-lookup"><span data-stu-id="ed142-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ed142-141">範例13：取得目前訂閱之指定資源群組中原則指派的最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ed142-142">取得 [ () 目前會話內容] 中的 [資源] 群組中存在於 [目前會話內容]) 中之 [資源] 群組中的所有 (資源所產生之最新原則規範狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="ed142-143">範例14：在目前的訂閱範圍中取得最新不相容原則狀態摘要，並使用 Top 查詢選項</span><span class="sxs-lookup"><span data-stu-id="ed142-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

<span data-ttu-id="ed142-144">取得目前會話內容中訂閱中所有資源在最後一天產生之最新原則合規性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ed142-145">此命令會根據不符合的資源計數以遞減順序，在結果中排序原則指派摘要，而且只會取得這些原則指派摘要的前5個。</span><span class="sxs-lookup"><span data-stu-id="ed142-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="ed142-146">範例15：取得目前訂閱範圍中的最新不相容原則狀態摘要，使用 From 和 To 查詢選項</span><span class="sxs-lookup"><span data-stu-id="ed142-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="ed142-147">取得在針對目前會話內容中訂閱之所有資源指定之日期範圍內所產生之最新原則合規性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ed142-148">範例16：使用篩選查詢選項，在目前的訂閱範圍中取得最新不相容原則狀態摘要</span><span class="sxs-lookup"><span data-stu-id="ed142-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="ed142-149">取得目前會話內容中訂閱中所有資源在最後一天產生之最新原則合規性狀態的摘要視圖。</span><span class="sxs-lookup"><span data-stu-id="ed142-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="ed142-150">此命令會根據原則定義動作來限制篩選所傳回的結果 (包括拒絕或審核動作) 以及資源位置 (排除 eastus 位置) 。</span><span class="sxs-lookup"><span data-stu-id="ed142-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="ed142-151">參數</span><span class="sxs-lookup"><span data-stu-id="ed142-151">PARAMETERS</span></span>

### <span data-ttu-id="ed142-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed142-152">-DefaultProfile</span></span>
<span data-ttu-id="ed142-153">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed142-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed142-154">-篩選</span><span class="sxs-lookup"><span data-stu-id="ed142-154">-Filter</span></span>
<span data-ttu-id="ed142-155">使用 OData 符號篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="ed142-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="ed142-156">-從</span><span class="sxs-lookup"><span data-stu-id="ed142-156">-From</span></span>
<span data-ttu-id="ed142-157">ISO 8601 格式化的時間戳記，指定要查詢間隔的開始時間。</span><span class="sxs-lookup"><span data-stu-id="ed142-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="ed142-158">如果未指定，則預設為「To」參數值減去1天。</span><span class="sxs-lookup"><span data-stu-id="ed142-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="ed142-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ed142-159">-ManagementGroupName</span></span>
<span data-ttu-id="ed142-160">管理組名。</span><span class="sxs-lookup"><span data-stu-id="ed142-160">Management group name.</span></span>

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

### <span data-ttu-id="ed142-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ed142-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="ed142-162">原則作業名稱。</span><span class="sxs-lookup"><span data-stu-id="ed142-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="ed142-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ed142-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="ed142-164">原則定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ed142-164">Policy definition name.</span></span>

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

### <span data-ttu-id="ed142-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ed142-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="ed142-166">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ed142-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="ed142-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed142-167">-ResourceGroupName</span></span>
<span data-ttu-id="ed142-168">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ed142-168">Resource group name.</span></span>

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

### <span data-ttu-id="ed142-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed142-169">-ResourceId</span></span>
<span data-ttu-id="ed142-170">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ed142-170">Resource ID.</span></span>

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

### <span data-ttu-id="ed142-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed142-171">-SubscriptionId</span></span>
<span data-ttu-id="ed142-172">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ed142-172">Subscription ID.</span></span>

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

### <span data-ttu-id="ed142-173">-To</span><span class="sxs-lookup"><span data-stu-id="ed142-173">-To</span></span>
<span data-ttu-id="ed142-174">ISO 8601 格式化的時間戳記，指定要查詢間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="ed142-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="ed142-175">如果未指定，則預設為要求的時間。</span><span class="sxs-lookup"><span data-stu-id="ed142-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="ed142-176">-上方</span><span class="sxs-lookup"><span data-stu-id="ed142-176">-Top</span></span>
<span data-ttu-id="ed142-177">要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="ed142-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="ed142-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed142-178">CommonParameters</span></span>
<span data-ttu-id="ed142-179">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed142-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed142-180">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed142-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed142-181">輸入</span><span class="sxs-lookup"><span data-stu-id="ed142-181">INPUTS</span></span>

### <span data-ttu-id="ed142-182">System.object</span><span class="sxs-lookup"><span data-stu-id="ed142-182">System.String</span></span>

## <span data-ttu-id="ed142-183">輸出</span><span class="sxs-lookup"><span data-stu-id="ed142-183">OUTPUTS</span></span>

### <span data-ttu-id="ed142-184">PolicyStateSummary 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="ed142-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="ed142-185">筆記</span><span class="sxs-lookup"><span data-stu-id="ed142-185">NOTES</span></span>

## <span data-ttu-id="ed142-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed142-186">RELATED LINKS</span></span>

[<span data-ttu-id="ed142-187">AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="ed142-187">Get-AzureRmPolicyState</span></span>](./Get-AzureRmPolicyState.md)
