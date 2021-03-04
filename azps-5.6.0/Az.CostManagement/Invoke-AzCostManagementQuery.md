---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: c1bc78747807d0f481c35fc75ff6fcfc80a83787
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907142"
---
# <span data-ttu-id="3b98c-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="3b98c-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="3b98c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b98c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b98c-103">查詢已定義範圍的使用資料。</span><span class="sxs-lookup"><span data-stu-id="3b98c-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="3b98c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b98c-104">SYNTAX</span></span>

### <span data-ttu-id="3b98c-105">UsageExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="3b98c-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b98c-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="3b98c-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b98c-107">描述</span><span class="sxs-lookup"><span data-stu-id="3b98c-107">DESCRIPTION</span></span>
<span data-ttu-id="3b98c-108">查詢已定義範圍的使用資料。</span><span class="sxs-lookup"><span data-stu-id="3b98c-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="3b98c-109">例子</span><span class="sxs-lookup"><span data-stu-id="3b98c-109">EXAMPLES</span></span>

### <span data-ttu-id="3b98c-110">範例 1：Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="3b98c-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="3b98c-111">按範圍來 Invoke AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="3b98c-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="3b98c-112">範例 2：Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="3b98c-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="3b98c-113">使用維度以範圍來調用 AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="3b98c-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="3b98c-114">參數</span><span class="sxs-lookup"><span data-stu-id="3b98c-114">PARAMETERS</span></span>

### <span data-ttu-id="3b98c-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="3b98c-115">-ConfigurationColumn</span></span>
<span data-ttu-id="3b98c-116">要包含在查詢中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="3b98c-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="3b98c-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="3b98c-117">-DatasetAggregation</span></span>
<span data-ttu-id="3b98c-118">要用於查詢的匯總運算式字典。</span><span class="sxs-lookup"><span data-stu-id="3b98c-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="3b98c-119">-資料集篩選</span><span class="sxs-lookup"><span data-stu-id="3b98c-119">-DatasetFilter</span></span>
<span data-ttu-id="3b98c-120">在查詢中可以使用篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="3b98c-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="3b98c-121">若要建構，請參閱 DATASETFILTER 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3b98c-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b98c-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="3b98c-122">-DatasetGranularity</span></span>
<span data-ttu-id="3b98c-123">查詢中列的細微程度。</span><span class="sxs-lookup"><span data-stu-id="3b98c-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="3b98c-124">-資料集工作組</span><span class="sxs-lookup"><span data-stu-id="3b98c-124">-DatasetGrouping</span></span>
<span data-ttu-id="3b98c-125">要用於查詢的運算式群組陣列。</span><span class="sxs-lookup"><span data-stu-id="3b98c-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="3b98c-126">若要建構，請參閱 DATASETGROUPING 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3b98c-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b98c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b98c-127">-DefaultProfile</span></span>
<span data-ttu-id="3b98c-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b98c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b98c-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="3b98c-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="3b98c-130">這可以是連結帳戶的 '{externalSubscriptionId}'，或用於維度/查詢作業之合併帳戶的 '{externalBillingAccountId}'。</span><span class="sxs-lookup"><span data-stu-id="3b98c-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

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

### <span data-ttu-id="3b98c-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="3b98c-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="3b98c-132">與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="3b98c-132">The external cloud provider type associated with dimension/query operations.</span></span>

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

### <span data-ttu-id="3b98c-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="3b98c-133">-Scope</span></span>
<span data-ttu-id="3b98c-134">這包括訂閱範圍的'subscriptions/{subscriptionId}/'、resourceGroup 範圍中的'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}'、帳單帳戶範圍的'提供者/Microsoft.Billing/billingAccounts/{billingAccountId}'，以及部門範圍中的'提供者/Microsoft.Billing/billingAccounts/{billingAccountId}/department/{departmentId}'， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount範圍，'providers/Microsoft.management/managementGroups/{managementGroupId}for Management Group 範圍， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfile 適用于發票範圍和合作夥伴專用'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}'的 invoiceSections/{invoiceSectionId}'。</span><span class="sxs-lookup"><span data-stu-id="3b98c-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

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

### <span data-ttu-id="3b98c-135">-時間範圍</span><span class="sxs-lookup"><span data-stu-id="3b98c-135">-Timeframe</span></span>
<span data-ttu-id="3b98c-136">提取查詢資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="3b98c-136">The time frame for pulling data for the query.</span></span>

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

### <span data-ttu-id="3b98c-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="3b98c-137">-TimePeriodFrom</span></span>
<span data-ttu-id="3b98c-138">提取資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="3b98c-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="3b98c-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="3b98c-139">-TimePeriodTo</span></span>
<span data-ttu-id="3b98c-140">要提取資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="3b98c-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="3b98c-141">-類型</span><span class="sxs-lookup"><span data-stu-id="3b98c-141">-Type</span></span>
<span data-ttu-id="3b98c-142">查詢的類型。</span><span class="sxs-lookup"><span data-stu-id="3b98c-142">The type of the query.</span></span>

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

### <span data-ttu-id="3b98c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="3b98c-143">-Confirm</span></span>
<span data-ttu-id="3b98c-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3b98c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b98c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b98c-145">-WhatIf</span></span>
<span data-ttu-id="3b98c-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b98c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b98c-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b98c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b98c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b98c-148">CommonParameters</span></span>
<span data-ttu-id="3b98c-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b98c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b98c-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b98c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b98c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="3b98c-151">INPUTS</span></span>

## <span data-ttu-id="3b98c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="3b98c-152">OUTPUTS</span></span>

### <span data-ttu-id="3b98c-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="3b98c-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="3b98c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="3b98c-154">NOTES</span></span>

<span data-ttu-id="3b98c-155">別名</span><span class="sxs-lookup"><span data-stu-id="3b98c-155">ALIASES</span></span>

<span data-ttu-id="3b98c-156">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3b98c-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b98c-157">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3b98c-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b98c-158">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3b98c-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b98c-159"><IQueryFilter>DATASETFILTER：在查詢中可使用篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="3b98c-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="3b98c-160">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="3b98c-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="3b98c-161">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="3b98c-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3b98c-162">`[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="3b98c-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="3b98c-163">`Name <String>`：要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="3b98c-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="3b98c-164">`Value <String[]>`：要用於比較的數值陣列</span><span class="sxs-lookup"><span data-stu-id="3b98c-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="3b98c-165">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="3b98c-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="3b98c-166">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="3b98c-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="3b98c-167">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="3b98c-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3b98c-168">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="3b98c-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="3b98c-169">DATASETGROUPING <IQueryGrouping[]>：要用於查詢的運算式群組陣列。</span><span class="sxs-lookup"><span data-stu-id="3b98c-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="3b98c-170">`Name <String>`：要分組的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="3b98c-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="3b98c-171">`Type <QueryColumnType>`：有要分組的欄類型。</span><span class="sxs-lookup"><span data-stu-id="3b98c-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="3b98c-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b98c-172">RELATED LINKS</span></span>

