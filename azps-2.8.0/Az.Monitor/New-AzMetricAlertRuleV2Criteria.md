---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 2495b819ee96252ec8e3ae00389ef9dc13a1b8f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789813"
---
# <span data-ttu-id="9adde-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="9adde-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="9adde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9adde-102">SYNOPSIS</span></span>
<span data-ttu-id="9adde-103">建立可以用來建立新度量警示的 [局部準則] 物件</span><span class="sxs-lookup"><span data-stu-id="9adde-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="9adde-104">句法</span><span class="sxs-lookup"><span data-stu-id="9adde-104">SYNTAX</span></span>

### <span data-ttu-id="9adde-105">StaticThresholdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9adde-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9adde-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9adde-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9adde-107">說明</span><span class="sxs-lookup"><span data-stu-id="9adde-107">DESCRIPTION</span></span>
<span data-ttu-id="9adde-108">**新的-AzMetricAlertRuleV2Criteria** Cmdlet 會建立一個 [局部公制準則] 物件，以做為建立新度量警示規則的輸入 Add-AzMetricAlertRuleV2 Cmdlet 使用。</span><span class="sxs-lookup"><span data-stu-id="9adde-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="9adde-109">示例</span><span class="sxs-lookup"><span data-stu-id="9adde-109">EXAMPLES</span></span>

### <span data-ttu-id="9adde-110">範例1：建立簡單的度量警示準則</span><span class="sxs-lookup"><span data-stu-id="9adde-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="9adde-111">這個命令會建立可在度量警報規則中使用的簡單度量警報準則</span><span class="sxs-lookup"><span data-stu-id="9adde-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="9adde-112">範例2：建立動態度量警示準則</span><span class="sxs-lookup"><span data-stu-id="9adde-112">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -NumberOfViolations 2 -NumberOfExaminedAggregatedPoints 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="9adde-113">這個命令會建立可在度量警示規則中使用的動態度量警示準則</span><span class="sxs-lookup"><span data-stu-id="9adde-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="9adde-114">範例3：建立更複雜的度量警報準則</span><span class="sxs-lookup"><span data-stu-id="9adde-114">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="9adde-115">這組命令會建立更複雜的度量警示準則，包括維度選取</span><span class="sxs-lookup"><span data-stu-id="9adde-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="9adde-116">參數</span><span class="sxs-lookup"><span data-stu-id="9adde-116">PARAMETERS</span></span>

### <span data-ttu-id="9adde-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adde-117">-DefaultProfile</span></span>
<span data-ttu-id="9adde-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9adde-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9adde-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="9adde-119">-DimensionSelection</span></span>
<span data-ttu-id="9adde-120">維度條件清單</span><span class="sxs-lookup"><span data-stu-id="9adde-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="9adde-121">-DynamicThreshold</span></span>
<span data-ttu-id="9adde-122">使用動態閾數值型別的切換參數</span><span class="sxs-lookup"><span data-stu-id="9adde-122">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="9adde-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="9adde-124">檢查點的總數</span><span class="sxs-lookup"><span data-stu-id="9adde-124">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="9adde-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="9adde-126">IgnoreDataBefore 參數</span><span class="sxs-lookup"><span data-stu-id="9adde-126">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9adde-127">-MetricName</span></span>
<span data-ttu-id="9adde-128">規則的度量名稱</span><span class="sxs-lookup"><span data-stu-id="9adde-128">The metric name for rule</span></span>

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

### <span data-ttu-id="9adde-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="9adde-129">-MetricNamespace</span></span>
<span data-ttu-id="9adde-130">公制的命名空間</span><span class="sxs-lookup"><span data-stu-id="9adde-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-131">-運算子</span><span class="sxs-lookup"><span data-stu-id="9adde-131">-Operator</span></span>
<span data-ttu-id="9adde-132">規則條件運算子</span><span class="sxs-lookup"><span data-stu-id="9adde-132">The rule condition operator</span></span>

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

### <span data-ttu-id="9adde-133">-閾值</span><span class="sxs-lookup"><span data-stu-id="9adde-133">-Threshold</span></span>
<span data-ttu-id="9adde-134">規則條件的閾值</span><span class="sxs-lookup"><span data-stu-id="9adde-134">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="9adde-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="9adde-136">規則條件的敏感度</span><span class="sxs-lookup"><span data-stu-id="9adde-136">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="9adde-137">-TimeAggregation</span></span>
<span data-ttu-id="9adde-138">用於在整個視窗間隔中累加多個公制值的聚合運算</span><span class="sxs-lookup"><span data-stu-id="9adde-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="9adde-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="9adde-139">-ViolationCount</span></span>
<span data-ttu-id="9adde-140">在所選的 lookback 時間視窗中產生提醒所需的最小違規數量</span><span class="sxs-lookup"><span data-stu-id="9adde-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adde-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adde-141">CommonParameters</span></span>
<span data-ttu-id="9adde-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9adde-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adde-143">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9adde-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adde-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9adde-144">INPUTS</span></span>

### <span data-ttu-id="9adde-145">PSMetricDimension [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="9adde-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="9adde-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9adde-146">OUTPUTS</span></span>

### <span data-ttu-id="9adde-147">IPSMultiMetricCriteria 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="9adde-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="9adde-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9adde-148">NOTES</span></span>

## <span data-ttu-id="9adde-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9adde-149">RELATED LINKS</span></span>
