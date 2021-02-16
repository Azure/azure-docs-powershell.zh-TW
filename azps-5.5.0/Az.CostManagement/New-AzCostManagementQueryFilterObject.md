---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137354"
---
# <span data-ttu-id="08e12-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="08e12-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="08e12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08e12-102">SYNOPSIS</span></span>
<span data-ttu-id="08e12-103">為 QueryFilter 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="08e12-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="08e12-104">句法</span><span class="sxs-lookup"><span data-stu-id="08e12-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="08e12-105">說明</span><span class="sxs-lookup"><span data-stu-id="08e12-105">DESCRIPTION</span></span>
<span data-ttu-id="08e12-106">為 QueryFilter 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="08e12-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="08e12-107">示例</span><span class="sxs-lookup"><span data-stu-id="08e12-107">EXAMPLES</span></span>

### <span data-ttu-id="08e12-108">範例1：建立成本管理匯出查詢的篩選物件</span><span class="sxs-lookup"><span data-stu-id="08e12-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="08e12-109">這個命令會針對成本管理匯出建立查詢的篩選物件。</span><span class="sxs-lookup"><span data-stu-id="08e12-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="08e12-110">參數</span><span class="sxs-lookup"><span data-stu-id="08e12-110">PARAMETERS</span></span>

### <span data-ttu-id="08e12-111">-以及</span><span class="sxs-lookup"><span data-stu-id="08e12-111">-And</span></span>
<span data-ttu-id="08e12-112">邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-112">The logical "AND" expression.</span></span>
<span data-ttu-id="08e12-113">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-113">Must have at least 2 items.</span></span>
<span data-ttu-id="08e12-114">若要構造，請參閱記事區段和屬性，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="08e12-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="08e12-115">-維度</span><span class="sxs-lookup"><span data-stu-id="08e12-115">-Dimensions</span></span>
<span data-ttu-id="08e12-116">具有維度的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="08e12-117">若要建立，請參閱維度屬性的 [記事] 區段，然後建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="08e12-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="08e12-118">-Not</span><span class="sxs-lookup"><span data-stu-id="08e12-118">-Not</span></span>
<span data-ttu-id="08e12-119">邏輯「NOT」運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="08e12-120">若要建立，請參閱 NOT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="08e12-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="08e12-121">-或</span><span class="sxs-lookup"><span data-stu-id="08e12-121">-Or</span></span>
<span data-ttu-id="08e12-122">邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-122">The logical "OR" expression.</span></span>
<span data-ttu-id="08e12-123">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-123">Must have at least 2 items.</span></span>
<span data-ttu-id="08e12-124">若要建立，請參閱 [記事] 區段或 [屬性]，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="08e12-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="08e12-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="08e12-125">-Tag</span></span>
<span data-ttu-id="08e12-126">具有標記的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="08e12-127">若要建立，請參閱標記摘要資訊和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="08e12-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="08e12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e12-128">CommonParameters</span></span>
<span data-ttu-id="08e12-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08e12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e12-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08e12-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e12-131">輸入</span><span class="sxs-lookup"><span data-stu-id="08e12-131">INPUTS</span></span>

## <span data-ttu-id="08e12-132">輸出</span><span class="sxs-lookup"><span data-stu-id="08e12-132">OUTPUTS</span></span>

### <span data-ttu-id="08e12-133">QueryFilter （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="08e12-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="08e12-134">筆記</span><span class="sxs-lookup"><span data-stu-id="08e12-134">NOTES</span></span>

<span data-ttu-id="08e12-135">別名</span><span class="sxs-lookup"><span data-stu-id="08e12-135">ALIASES</span></span>

<span data-ttu-id="08e12-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="08e12-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08e12-137">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="08e12-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08e12-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="08e12-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08e12-139">然後 <IQueryFilter [] >：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="08e12-140">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-141">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="08e12-142">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-143">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="08e12-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="08e12-144">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="08e12-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="08e12-145">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="08e12-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="08e12-146">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="08e12-147">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="08e12-148">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-149">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="08e12-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="08e12-150">維度 <IQueryComparisonExpression> ：具有維度的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="08e12-151">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="08e12-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="08e12-152">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="08e12-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="08e12-153">NOT <IQueryFilter> ：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="08e12-154">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="08e12-155">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-156">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="08e12-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="08e12-157">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="08e12-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="08e12-158">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="08e12-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="08e12-159">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="08e12-160">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="08e12-161">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-162">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="08e12-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="08e12-163">或 <IQueryFilter [] >：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="08e12-164">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-165">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="08e12-166">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-167">`[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="08e12-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="08e12-168">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="08e12-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="08e12-169">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="08e12-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="08e12-170">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="08e12-171">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="08e12-172">至少必須有2個專案。</span><span class="sxs-lookup"><span data-stu-id="08e12-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="08e12-173">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="08e12-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="08e12-174">TAG <IQueryComparisonExpression> ：具有標記的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="08e12-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="08e12-175">`Name <String>`：要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="08e12-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="08e12-176">`Value <String[]>`：要用於比較的值陣列</span><span class="sxs-lookup"><span data-stu-id="08e12-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="08e12-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="08e12-177">RELATED LINKS</span></span>

