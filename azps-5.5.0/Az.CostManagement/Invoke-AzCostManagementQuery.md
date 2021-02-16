---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 37f4d4b5650060b490e8c6bb691d938b78fa1166
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129610"
---
# <span data-ttu-id="5608b-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="5608b-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="5608b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5608b-102">SYNOPSIS</span></span>
<span data-ttu-id="5608b-103">查詢已定義範圍的使用資料。</span><span class="sxs-lookup"><span data-stu-id="5608b-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="5608b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5608b-104">SYNTAX</span></span>

### <span data-ttu-id="5608b-105">UsageExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5608b-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5608b-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="5608b-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5608b-107">說明</span><span class="sxs-lookup"><span data-stu-id="5608b-107">DESCRIPTION</span></span>
<span data-ttu-id="5608b-108">查詢已定義範圍的使用資料。</span><span class="sxs-lookup"><span data-stu-id="5608b-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="5608b-109">示例</span><span class="sxs-lookup"><span data-stu-id="5608b-109">EXAMPLES</span></span>

### <span data-ttu-id="5608b-110">範例1：依範圍喚醒呼叫 AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="5608b-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="5608b-111">依範圍來喚醒呼叫 AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="5608b-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="5608b-112">範例2：依範圍在維度中使用 AzCostManagementQuery 來喚醒</span><span class="sxs-lookup"><span data-stu-id="5608b-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="5608b-113">依範圍在維度中使用 AzCostManagementQuery 來喚醒</span><span class="sxs-lookup"><span data-stu-id="5608b-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="5608b-114">參數</span><span class="sxs-lookup"><span data-stu-id="5608b-114">PARAMETERS</span></span>

### <span data-ttu-id="5608b-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="5608b-115">-ConfigurationColumn</span></span>
<span data-ttu-id="5608b-116">要包含在查詢中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="5608b-116">Array of column names to be included in the query.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="5608b-117">-DatasetAggregation</span></span>
<span data-ttu-id="5608b-118">要在查詢中使用之匯總運算式的字典。</span><span class="sxs-lookup"><span data-stu-id="5608b-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="5608b-119">-DatasetFilter</span></span>
<span data-ttu-id="5608b-120">具有要在查詢中使用的篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="5608b-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="5608b-121">若要建立，請參閱 DATASETFILTER 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5608b-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="5608b-122">-DatasetGranularity</span></span>
<span data-ttu-id="5608b-123">查詢中列的細微性。</span><span class="sxs-lookup"><span data-stu-id="5608b-123">The granularity of rows in the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="5608b-124">-DatasetGrouping</span></span>
<span data-ttu-id="5608b-125">要在查詢中使用的 group by 運算式陣列。</span><span class="sxs-lookup"><span data-stu-id="5608b-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="5608b-126">若要建立，請參閱 DATASETGROUPING 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5608b-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5608b-127">-DefaultProfile</span></span>
<span data-ttu-id="5608b-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5608b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="5608b-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="5608b-130">這可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="5608b-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="5608b-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="5608b-132">與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="5608b-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="5608b-133">-Scope</span></span>
<span data-ttu-id="5608b-134">這包括「訂閱/{subscriptionId}/' for 訂閱範圍」、「訂閱/{subscriptionId}/resourceGroups/{resourceGroupName}」（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍和 ' 提供者/Microsoft. 帳單/billingAccounts//{billingAccountId}/部門/{departmentId} ' 代表部門範圍、' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' 提供 EnrollmentAccounts 管理群組範圍、' 提供者/Microsoft. 帳單/billingAccounts//{billingAccountId}/billingProfiles/{billingProfileId} ' for billingProfile managementGroupId 的管理/managementGroups/{} "提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId} ' for invoiceSection 範圍，以及「提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' 特定的合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="5608b-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-135">-時間範圍</span><span class="sxs-lookup"><span data-stu-id="5608b-135">-Timeframe</span></span>
<span data-ttu-id="5608b-136">提取查詢資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="5608b-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="5608b-137">-TimePeriodFrom</span></span>
<span data-ttu-id="5608b-138">要從中提取資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="5608b-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="5608b-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="5608b-139">-TimePeriodTo</span></span>
<span data-ttu-id="5608b-140">要提取資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="5608b-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="5608b-141">-類型</span><span class="sxs-lookup"><span data-stu-id="5608b-141">-Type</span></span>
<span data-ttu-id="5608b-142">查詢的類型。</span><span class="sxs-lookup"><span data-stu-id="5608b-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5608b-143">-確認</span><span class="sxs-lookup"><span data-stu-id="5608b-143">-Confirm</span></span>
<span data-ttu-id="5608b-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5608b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5608b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5608b-145">-WhatIf</span></span>
<span data-ttu-id="5608b-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5608b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5608b-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5608b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5608b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5608b-148">CommonParameters</span></span>
<span data-ttu-id="5608b-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5608b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5608b-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5608b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5608b-151">輸入</span><span class="sxs-lookup"><span data-stu-id="5608b-151">INPUTS</span></span>

## <span data-ttu-id="5608b-152">輸出</span><span class="sxs-lookup"><span data-stu-id="5608b-152">OUTPUTS</span></span>

### <span data-ttu-id="5608b-153">IQueryResult （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="5608b-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="5608b-154">筆記</span><span class="sxs-lookup"><span data-stu-id="5608b-154">NOTES</span></span>

<span data-ttu-id="5608b-155">別名</span><span class="sxs-lookup"><span data-stu-id="5608b-155">ALIASES</span></span>

<span data-ttu-id="5608b-156">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5608b-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5608b-157">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5608b-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5608b-158">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5608b-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5608b-159">DATASETFILTER <IQueryFilter> ：有要在查詢中使用的篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="5608b-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="5608b-160">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="5608b-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="5608b-161">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="5608b-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="5608b-162">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="5608b-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="5608b-163">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="5608b-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="5608b-164">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="5608b-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="5608b-165">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="5608b-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="5608b-166">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="5608b-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="5608b-167">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="5608b-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="5608b-168">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="5608b-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="5608b-169">DATASETGROUPING <IQueryGrouping [] >：要在查詢中使用的 group by 運算式陣列。</span><span class="sxs-lookup"><span data-stu-id="5608b-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="5608b-170">`Name <String>`：要組成群組的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="5608b-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="5608b-171">`Type <QueryColumnType>`：有要分組的欄類型。</span><span class="sxs-lookup"><span data-stu-id="5608b-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="5608b-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="5608b-172">RELATED LINKS</span></span>

