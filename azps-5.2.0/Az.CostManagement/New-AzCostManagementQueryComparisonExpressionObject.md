---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277443"
---
# <span data-ttu-id="8dff6-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="8dff6-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="8dff6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dff6-102">SYNOPSIS</span></span>
<span data-ttu-id="8dff6-103">為 QueryComparisonExpression 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="8dff6-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="8dff6-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dff6-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="8dff6-105">說明</span><span class="sxs-lookup"><span data-stu-id="8dff6-105">DESCRIPTION</span></span>
<span data-ttu-id="8dff6-106">為 QueryComparisonExpression 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="8dff6-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="8dff6-107">示例</span><span class="sxs-lookup"><span data-stu-id="8dff6-107">EXAMPLES</span></span>

### <span data-ttu-id="8dff6-108">範例1：建立成本管理匯出查詢的比較運算式物件</span><span class="sxs-lookup"><span data-stu-id="8dff6-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="8dff6-109">這個命令會針對成本管理匯出建立查詢的比較運算式物件。</span><span class="sxs-lookup"><span data-stu-id="8dff6-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="8dff6-110">參數</span><span class="sxs-lookup"><span data-stu-id="8dff6-110">PARAMETERS</span></span>

### <span data-ttu-id="8dff6-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="8dff6-111">-Name</span></span>
<span data-ttu-id="8dff6-112">要用於比較的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="8dff6-112">The name of the column to use in comparison.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dff6-113">-運算子</span><span class="sxs-lookup"><span data-stu-id="8dff6-113">-Operator</span></span>
<span data-ttu-id="8dff6-114">要用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="8dff6-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dff6-115">-值</span><span class="sxs-lookup"><span data-stu-id="8dff6-115">-Value</span></span>
<span data-ttu-id="8dff6-116">要用於比較的值陣列。</span><span class="sxs-lookup"><span data-stu-id="8dff6-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dff6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dff6-117">CommonParameters</span></span>
<span data-ttu-id="8dff6-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dff6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dff6-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8dff6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dff6-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8dff6-120">INPUTS</span></span>

## <span data-ttu-id="8dff6-121">輸出</span><span class="sxs-lookup"><span data-stu-id="8dff6-121">OUTPUTS</span></span>

### <span data-ttu-id="8dff6-122">QueryComparisonExpression （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="8dff6-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="8dff6-123">筆記</span><span class="sxs-lookup"><span data-stu-id="8dff6-123">NOTES</span></span>

<span data-ttu-id="8dff6-124">別名</span><span class="sxs-lookup"><span data-stu-id="8dff6-124">ALIASES</span></span>

## <span data-ttu-id="8dff6-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dff6-125">RELATED LINKS</span></span>

