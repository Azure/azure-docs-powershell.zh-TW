---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916757"
---
# <span data-ttu-id="4424f-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="4424f-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="4424f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4424f-102">SYNOPSIS</span></span>
<span data-ttu-id="4424f-103">為 QueryFilter 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="4424f-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="4424f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4424f-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="4424f-105">描述</span><span class="sxs-lookup"><span data-stu-id="4424f-105">DESCRIPTION</span></span>
<span data-ttu-id="4424f-106">為 QueryFilter 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="4424f-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="4424f-107">例子</span><span class="sxs-lookup"><span data-stu-id="4424f-107">EXAMPLES</span></span>

### <span data-ttu-id="4424f-108">範例 1：建立成本管理匯出查詢的篩選物件</span><span class="sxs-lookup"><span data-stu-id="4424f-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="4424f-109">此命令會建立查詢的篩選物件，以匯出成本管理。</span><span class="sxs-lookup"><span data-stu-id="4424f-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="4424f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4424f-110">PARAMETERS</span></span>

### <span data-ttu-id="4424f-111">-And</span><span class="sxs-lookup"><span data-stu-id="4424f-111">-And</span></span>
<span data-ttu-id="4424f-112">邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-112">The logical "AND" expression.</span></span>
<span data-ttu-id="4424f-113">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-113">Must have at least 2 items.</span></span>
<span data-ttu-id="4424f-114">若要建構，請參閱 AND 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4424f-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="4424f-115">-維度</span><span class="sxs-lookup"><span data-stu-id="4424f-115">-Dimensions</span></span>
<span data-ttu-id="4424f-116">有維度的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="4424f-117">若要建構，請參閱 DIMENSIONS 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4424f-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="4424f-118">-Not</span><span class="sxs-lookup"><span data-stu-id="4424f-118">-Not</span></span>
<span data-ttu-id="4424f-119">邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="4424f-120">若要建構，請參閱 NOT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4424f-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4424f-121">-或</span><span class="sxs-lookup"><span data-stu-id="4424f-121">-Or</span></span>
<span data-ttu-id="4424f-122">邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-122">The logical "OR" expression.</span></span>
<span data-ttu-id="4424f-123">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-123">Must have at least 2 items.</span></span>
<span data-ttu-id="4424f-124">若要建構，請參閱 OR 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4424f-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="4424f-125">-標記</span><span class="sxs-lookup"><span data-stu-id="4424f-125">-Tag</span></span>
<span data-ttu-id="4424f-126">具有標記的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="4424f-127">若要建構，請參閱標記屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4424f-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="4424f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4424f-128">CommonParameters</span></span>
<span data-ttu-id="4424f-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4424f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4424f-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4424f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4424f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4424f-131">INPUTS</span></span>

## <span data-ttu-id="4424f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4424f-132">OUTPUTS</span></span>

### <span data-ttu-id="4424f-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="4424f-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="4424f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4424f-134">NOTES</span></span>

<span data-ttu-id="4424f-135">別名</span><span class="sxs-lookup"><span data-stu-id="4424f-135">ALIASES</span></span>

<span data-ttu-id="4424f-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4424f-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4424f-137">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4424f-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4424f-138">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4424f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4424f-139">AND <IQueryFilter[]>：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="4424f-140">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-141">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4424f-142">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-143">`[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="4424f-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4424f-144">`Name <String>`：要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="4424f-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4424f-145">`Value <String[]>`：要用於比較的數值陣列</span><span class="sxs-lookup"><span data-stu-id="4424f-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4424f-146">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4424f-147">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4424f-148">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-149">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="4424f-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4424f-150">維度 <IQueryComparisonExpression> ：有維度的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="4424f-151">`Name <String>`：要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="4424f-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="4424f-152">`Value <String[]>`：要用於比較的數值陣列</span><span class="sxs-lookup"><span data-stu-id="4424f-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="4424f-153">NOT <IQueryFilter> ：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4424f-154">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4424f-155">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-156">`[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="4424f-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4424f-157">`Name <String>`：要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="4424f-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4424f-158">`Value <String[]>`：要用於比較的數值陣列</span><span class="sxs-lookup"><span data-stu-id="4424f-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4424f-159">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4424f-160">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4424f-161">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-162">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="4424f-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4424f-163">或者<IQueryFilter[]>：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="4424f-164">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-165">`[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4424f-166">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-167">`[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式</span><span class="sxs-lookup"><span data-stu-id="4424f-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4424f-168">`Name <String>`：要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="4424f-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4424f-169">`Value <String[]>`：要用於比較的數值陣列</span><span class="sxs-lookup"><span data-stu-id="4424f-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4424f-170">`[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4424f-171">`[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4424f-172">至少必須有 2 個專案。</span><span class="sxs-lookup"><span data-stu-id="4424f-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4424f-173">`[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式</span><span class="sxs-lookup"><span data-stu-id="4424f-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4424f-174"><IQueryComparisonExpression>TAG：具有標記的比較運算式。</span><span class="sxs-lookup"><span data-stu-id="4424f-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="4424f-175">`Name <String>`：要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="4424f-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="4424f-176">`Value <String[]>`：要用於比較的數值陣列</span><span class="sxs-lookup"><span data-stu-id="4424f-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="4424f-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="4424f-177">RELATED LINKS</span></span>

