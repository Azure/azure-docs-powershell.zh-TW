---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134075"
---
# <span data-ttu-id="31b3e-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="31b3e-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="31b3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="31b3e-103">建立可用於構造標準警示準則的局部維度選擇物件。</span><span class="sxs-lookup"><span data-stu-id="31b3e-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="31b3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="31b3e-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b3e-105">說明</span><span class="sxs-lookup"><span data-stu-id="31b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="31b3e-106">**AzMetricAlertRuleV2DimensionSelection** Cmdlet 會建立局部維度選取物件，以協助使用 [新的-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) Cmdlet 來構造公制警報準則。</span><span class="sxs-lookup"><span data-stu-id="31b3e-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="31b3e-107">示例</span><span class="sxs-lookup"><span data-stu-id="31b3e-107">EXAMPLES</span></span>

### <span data-ttu-id="31b3e-108">範例1：建立維度選取物件</span><span class="sxs-lookup"><span data-stu-id="31b3e-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="31b3e-109">這個命令會建立一個維度選取物件，指定 {1,3,4} 需要選取維度 "LUN" 的值</span><span class="sxs-lookup"><span data-stu-id="31b3e-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="31b3e-110">參數</span><span class="sxs-lookup"><span data-stu-id="31b3e-110">PARAMETERS</span></span>

### <span data-ttu-id="31b3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b3e-111">-DefaultProfile</span></span>
<span data-ttu-id="31b3e-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31b3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b3e-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="31b3e-113">-DimensionName</span></span>
<span data-ttu-id="31b3e-114">維度名稱</span><span class="sxs-lookup"><span data-stu-id="31b3e-114">The Dimension name</span></span>

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

### <span data-ttu-id="31b3e-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="31b3e-115">-ValuesToExclude</span></span>
<span data-ttu-id="31b3e-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="31b3e-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="31b3e-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="31b3e-117">-ValuesToInclude</span></span>
<span data-ttu-id="31b3e-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="31b3e-118">The IncludeValues</span></span>

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

### <span data-ttu-id="31b3e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b3e-119">CommonParameters</span></span>
<span data-ttu-id="31b3e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31b3e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b3e-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="31b3e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b3e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="31b3e-122">INPUTS</span></span>

### <span data-ttu-id="31b3e-123">System.object</span><span class="sxs-lookup"><span data-stu-id="31b3e-123">System.String</span></span>

### <span data-ttu-id="31b3e-124">System.object []</span><span class="sxs-lookup"><span data-stu-id="31b3e-124">System.String[]</span></span>

## <span data-ttu-id="31b3e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="31b3e-125">OUTPUTS</span></span>

### <span data-ttu-id="31b3e-126">PSMetricDimension 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="31b3e-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="31b3e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="31b3e-127">NOTES</span></span>

## <span data-ttu-id="31b3e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="31b3e-128">RELATED LINKS</span></span>
