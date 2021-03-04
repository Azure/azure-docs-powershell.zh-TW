---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904646"
---
# <span data-ttu-id="5b24c-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5b24c-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="5b24c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5b24c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b24c-103">建立可用於建構公制警示準則的當地維度選取物件。</span><span class="sxs-lookup"><span data-stu-id="5b24c-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="5b24c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5b24c-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b24c-105">描述</span><span class="sxs-lookup"><span data-stu-id="5b24c-105">DESCRIPTION</span></span>
<span data-ttu-id="5b24c-106">**New-AzMetricAlertRuleV2DimensionSelection** Cmdlet 會建立一個本地維度選取物件，以使用 [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) Cmdlet 協助建立公制警示準則。</span><span class="sxs-lookup"><span data-stu-id="5b24c-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="5b24c-107">例子</span><span class="sxs-lookup"><span data-stu-id="5b24c-107">EXAMPLES</span></span>

### <span data-ttu-id="5b24c-108">範例 1：建立維度選取物件</span><span class="sxs-lookup"><span data-stu-id="5b24c-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="5b24c-109">此命令會建立維度選取物件，指定需要選取 {1,3,4} 維度 "進位" 的值</span><span class="sxs-lookup"><span data-stu-id="5b24c-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="5b24c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5b24c-110">PARAMETERS</span></span>

### <span data-ttu-id="5b24c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b24c-111">-DefaultProfile</span></span>
<span data-ttu-id="5b24c-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b24c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b24c-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="5b24c-113">-DimensionName</span></span>
<span data-ttu-id="5b24c-114">維度名稱</span><span class="sxs-lookup"><span data-stu-id="5b24c-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b24c-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="5b24c-115">-ValuesToExclude</span></span>
<span data-ttu-id="5b24c-116">The ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="5b24c-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b24c-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="5b24c-117">-ValuesToInclude</span></span>
<span data-ttu-id="5b24c-118">The IncludeValues</span><span class="sxs-lookup"><span data-stu-id="5b24c-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b24c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b24c-119">CommonParameters</span></span>
<span data-ttu-id="5b24c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5b24c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b24c-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b24c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b24c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5b24c-122">INPUTS</span></span>

### <span data-ttu-id="5b24c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5b24c-123">System.String</span></span>

### <span data-ttu-id="5b24c-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5b24c-124">System.String[]</span></span>

## <span data-ttu-id="5b24c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="5b24c-125">OUTPUTS</span></span>

### <span data-ttu-id="5b24c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="5b24c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="5b24c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5b24c-127">NOTES</span></span>

## <span data-ttu-id="5b24c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b24c-128">RELATED LINKS</span></span>
