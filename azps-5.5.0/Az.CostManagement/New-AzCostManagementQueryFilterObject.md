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
# New-AzCostManagementQueryFilterObject

## 摘要
為 QueryFilter 建立記憶體內建物件

## 句法

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## 說明
為 QueryFilter 建立記憶體內建物件

## 示例

### 範例1：建立成本管理匯出查詢的篩選物件
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

這個命令會針對成本管理匯出建立查詢的篩選物件。

## 參數

### -以及
邏輯 "AND" 運算式。
至少必須有2個專案。
若要構造，請參閱記事區段和屬性，並建立雜湊資料表。

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

### -維度
具有維度的比較運算式。
若要建立，請參閱維度屬性的 [記事] 區段，然後建立雜湊資料表。

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

### -Not
邏輯「NOT」運算式。
若要建立，請參閱 NOT 屬性和建立雜湊資料表的備忘稿區段。

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

### -或
邏輯 "OR" 運算式。
至少必須有2個專案。
若要建立，請參閱 [記事] 區段或 [屬性]，然後建立雜湊表。

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

### -Tag
具有標記的比較運算式。
若要建立，請參閱標記摘要資訊和建立雜湊資料表的備忘稿區段。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### QueryFilter （CostManagement）。 Api20200601。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


然後 <IQueryFilter [] >：邏輯 "AND" 運算式。 至少必須有2個專案。
  - `[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。 至少必須有2個專案。
  - `[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式
    - `Name <String>`：要用於比較的資料行名稱。
    - `Value <String[]>`：要用於比較的值陣列
  - `[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。
  - `[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。 至少必須有2個專案。
  - `[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式

維度 <IQueryComparisonExpression> ：具有維度的比較運算式。
  - `Name <String>`：要用於比較的資料行名稱。
  - `Value <String[]>`：要用於比較的值陣列

NOT <IQueryFilter> ：邏輯 "NOT" 運算式。
  - `[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。 至少必須有2個專案。
  - `[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式
    - `Name <String>`：要用於比較的資料行名稱。
    - `Value <String[]>`：要用於比較的值陣列
  - `[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。
  - `[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。 至少必須有2個專案。
  - `[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式

或 <IQueryFilter [] >：邏輯 "OR" 運算式。 至少必須有2個專案。
  - `[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。 至少必須有2個專案。
  - `[Dimensions <IQueryComparisonExpression>]`：具有維度的比較運算式
    - `Name <String>`：要用於比較的資料行名稱。
    - `Value <String[]>`：要用於比較的值陣列
  - `[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。
  - `[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。 至少必須有2個專案。
  - `[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式

TAG <IQueryComparisonExpression> ：具有標記的比較運算式。
  - `Name <String>`：要用於比較的資料行名稱。
  - `Value <String[]>`：要用於比較的值陣列

## 相關連結

