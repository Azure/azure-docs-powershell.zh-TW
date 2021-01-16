---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277435"
---
# <span data-ttu-id="f467d-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="f467d-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="f467d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f467d-102">SYNOPSIS</span></span>
<span data-ttu-id="f467d-103">為 QueryFilter 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="f467d-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="f467d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f467d-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="f467d-105">說明</span><span class="sxs-lookup"><span data-stu-id="f467d-105">DESCRIPTION</span></span>
<span data-ttu-id="f467d-106">為 QueryFilter 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="f467d-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="f467d-107">示例</span><span class="sxs-lookup"><span data-stu-id="f467d-107">EXAMPLES</span></span>

### <span data-ttu-id="f467d-108">範例1：建立成本管理匯出查詢的篩選物件</span><span class="sxs-lookup"><span data-stu-id="f467d-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="f467d-109">這個命令會針對成本管理匯出建立查詢的篩選物件。</span><span class="sxs-lookup"><span data-stu-id="f467d-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="f467d-110">參數</span><span class="sxs-lookup"><span data-stu-id="f467d-110">PARAMETERS</span></span>

### <span data-ttu-id="f467d-111">-以及</span><span class="sxs-lookup"><span data-stu-id="f467d-111">-And</span></span>
<span data-ttu-id="f467d-112">邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-112">The logical "AND" expression.</span></span>
<span data-ttu-id="f467d-113">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-113">Must have at least 2 items.</span></span>
<span data-ttu-id="f467d-114">若要構造，請參閱記事區段和屬性，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f467d-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f467d-115">-維度</span><span class="sxs-lookup"><span data-stu-id="f467d-115">-Dimensions</span></span>
<span data-ttu-id="f467d-116">具有維度的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="f467d-117">若要建立，請參閱維度屬性的 [記事] 區段，然後建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f467d-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f467d-118">-Not</span><span class="sxs-lookup"><span data-stu-id="f467d-118">-Not</span></span>
<span data-ttu-id="f467d-119">邏輯「NOT」運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="f467d-120">若要建立，請參閱 NOT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="f467d-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f467d-121">-或</span><span class="sxs-lookup"><span data-stu-id="f467d-121">-Or</span></span>
<span data-ttu-id="f467d-122">邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-122">The logical "OR" expression.</span></span>
<span data-ttu-id="f467d-123">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-123">Must have at least 2 items.</span></span>
<span data-ttu-id="f467d-124">若要建立，請參閱 [記事] 區段或 [屬性]，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f467d-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f467d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f467d-125">-Tag</span></span>
<span data-ttu-id="f467d-126">具有標記的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="f467d-127">若要建立，請參閱標記摘要資訊和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="f467d-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f467d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f467d-128">CommonParameters</span></span>
<span data-ttu-id="f467d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f467d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f467d-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f467d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f467d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f467d-131">INPUTS</span></span>

## <span data-ttu-id="f467d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f467d-132">OUTPUTS</span></span>

### <span data-ttu-id="f467d-133">QueryFilter （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="f467d-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="f467d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f467d-134">NOTES</span></span>

<span data-ttu-id="f467d-135">別名</span><span class="sxs-lookup"><span data-stu-id="f467d-135">ALIASES</span></span>

<span data-ttu-id="f467d-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f467d-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f467d-137">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f467d-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f467d-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f467d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f467d-139">然後 <IQueryFilter [] >：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="f467d-140">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-141">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="f467d-142">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-143">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="f467d-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="f467d-144">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f467d-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="f467d-145">`Operator <OperatorType>`：用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="f467d-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="f467d-146">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="f467d-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="f467d-147">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="f467d-148">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="f467d-149">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-150">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="f467d-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="f467d-151">維度 <IQueryComparisonExpression> ：具有維度的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="f467d-152">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f467d-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="f467d-153">`Operator <OperatorType>`：用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="f467d-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="f467d-154">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="f467d-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="f467d-155">NOT <IQueryFilter> ：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="f467d-156">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="f467d-157">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-158">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="f467d-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="f467d-159">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f467d-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="f467d-160">`Operator <OperatorType>`：用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="f467d-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="f467d-161">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="f467d-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="f467d-162">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="f467d-163">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="f467d-164">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-165">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="f467d-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="f467d-166">或 <IQueryFilter [] >：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="f467d-167">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-168">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="f467d-169">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-170">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="f467d-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="f467d-171">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f467d-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="f467d-172">`Operator <OperatorType>`：用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="f467d-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="f467d-173">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="f467d-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="f467d-174">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="f467d-175">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="f467d-176">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="f467d-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f467d-177">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="f467d-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="f467d-178">TAG <IQueryComparisonExpression> ：具有標記的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="f467d-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="f467d-179">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f467d-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="f467d-180">`Operator <OperatorType>`：用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="f467d-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="f467d-181">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="f467d-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="f467d-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="f467d-182">RELATED LINKS</span></span>

