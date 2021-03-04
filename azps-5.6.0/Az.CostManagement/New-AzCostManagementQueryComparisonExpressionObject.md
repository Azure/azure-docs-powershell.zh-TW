---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: b41c5a30a1425778e69fbfff42cfe7062c6b71b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913958"
---
# <span data-ttu-id="ddcab-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="ddcab-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="ddcab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddcab-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcab-103">為 QueryComparisonExpression 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="ddcab-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="ddcab-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddcab-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="ddcab-105">描述</span><span class="sxs-lookup"><span data-stu-id="ddcab-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcab-106">為 QueryComparisonExpression 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="ddcab-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="ddcab-107">例子</span><span class="sxs-lookup"><span data-stu-id="ddcab-107">EXAMPLES</span></span>

### <span data-ttu-id="ddcab-108">範例 1：建立成本管理匯出查詢的比較運算式物件</span><span class="sxs-lookup"><span data-stu-id="ddcab-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="ddcab-109">此命令會針對成本管理匯出建立查詢的比較運算式物件。</span><span class="sxs-lookup"><span data-stu-id="ddcab-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="ddcab-110">參數</span><span class="sxs-lookup"><span data-stu-id="ddcab-110">PARAMETERS</span></span>

### <span data-ttu-id="ddcab-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddcab-111">-Name</span></span>
<span data-ttu-id="ddcab-112">要用於比較的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="ddcab-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="ddcab-113">-運算子</span><span class="sxs-lookup"><span data-stu-id="ddcab-113">-Operator</span></span>
<span data-ttu-id="ddcab-114">要用於比較的運算子。</span><span class="sxs-lookup"><span data-stu-id="ddcab-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="ddcab-115">-值</span><span class="sxs-lookup"><span data-stu-id="ddcab-115">-Value</span></span>
<span data-ttu-id="ddcab-116">要用於比較的數值陣列。</span><span class="sxs-lookup"><span data-stu-id="ddcab-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="ddcab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcab-117">CommonParameters</span></span>
<span data-ttu-id="ddcab-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddcab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcab-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddcab-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcab-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ddcab-120">INPUTS</span></span>

## <span data-ttu-id="ddcab-121">輸出</span><span class="sxs-lookup"><span data-stu-id="ddcab-121">OUTPUTS</span></span>

### <span data-ttu-id="ddcab-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="ddcab-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="ddcab-123">筆記</span><span class="sxs-lookup"><span data-stu-id="ddcab-123">NOTES</span></span>

<span data-ttu-id="ddcab-124">別名</span><span class="sxs-lookup"><span data-stu-id="ddcab-124">ALIASES</span></span>

## <span data-ttu-id="ddcab-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddcab-125">RELATED LINKS</span></span>

