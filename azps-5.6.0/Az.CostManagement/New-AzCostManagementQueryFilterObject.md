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
# New-AzCostManagementQueryFilterObject

## 簡介
為 QueryFilter 建立記憶體內物件

## 語法

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## 描述
為 QueryFilter 建立記憶體內物件

## 例子

### 範例 1：建立成本管理匯出查詢的篩選物件
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

此命令會建立查詢的篩選物件，以匯出成本管理。

## 參數

### -And
邏輯 "AND" 運算式。
至少必須有 2 個專案。
若要建構，請參閱 AND 屬性的附注區段，然後建立雜湊表。

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
有維度的比較運算式。
若要建構，請參閱 DIMENSIONS 屬性的附注區段，並建立雜湊表。

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
邏輯 "NOT" 運算式。
若要建構，請參閱 NOT 屬性的 NOTES 區段，並建立雜湊表。

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
至少必須有 2 個專案。
若要建構，請參閱 OR 屬性的 NOTES 區段，然後建立雜湊表。

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

### -標記
具有標記的比較運算式。
若要建構，請參閱標記屬性的附注區段，然後建立雜湊表。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.QueryFilter

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


AND <IQueryFilter[]>：邏輯 "AND" 運算式。 至少必須有 2 個專案。
  - `[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。 至少必須有 2 個專案。
  - `[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式
    - `Name <String>`：要用於比較的欄名稱。
    - `Value <String[]>`：要用於比較的數值陣列
  - `[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。
  - `[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。 至少必須有 2 個專案。
  - `[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式

維度 <IQueryComparisonExpression> ：有維度的比較運算式。
  - `Name <String>`：要用於比較的欄名稱。
  - `Value <String[]>`：要用於比較的數值陣列

NOT <IQueryFilter> ：邏輯 "NOT" 運算式。
  - `[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。 至少必須有 2 個專案。
  - `[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式
    - `Name <String>`：要用於比較的欄名稱。
    - `Value <String[]>`：要用於比較的數值陣列
  - `[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。
  - `[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。 至少必須有 2 個專案。
  - `[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式

或者<IQueryFilter[]>：邏輯 "OR" 運算式。 至少必須有 2 個專案。
  - `[And <IQueryFilter[]>]`：邏輯 "AND" 運算式。 至少必須有 2 個專案。
  - `[Dimensions <IQueryComparisonExpression>]`：有維度的比較運算式
    - `Name <String>`：要用於比較的欄名稱。
    - `Value <String[]>`：要用於比較的數值陣列
  - `[Not <IQueryFilter>]`：邏輯 "NOT" 運算式。
  - `[Or <IQueryFilter[]>]`：邏輯 "OR" 運算式。 至少必須有 2 個專案。
  - `[Tag <IQueryComparisonExpression>]`：具有標記的比較運算式

<IQueryComparisonExpression>TAG：具有標記的比較運算式。
  - `Name <String>`：要用於比較的欄名稱。
  - `Value <String[]>`：要用於比較的數值陣列

## 相關連結

