---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 951f9e5843987d1ad36378716b7a95e5d7a1f0a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905026"
---
# <span data-ttu-id="884f2-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="884f2-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="884f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="884f2-102">SYNOPSIS</span></span>
<span data-ttu-id="884f2-103">建立可用於建立新計量警示的當地準則物件</span><span class="sxs-lookup"><span data-stu-id="884f2-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="884f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="884f2-104">SYNTAX</span></span>

### <span data-ttu-id="884f2-105">StaticThresholdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="884f2-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="884f2-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="884f2-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="884f2-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="884f2-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="884f2-108">描述</span><span class="sxs-lookup"><span data-stu-id="884f2-108">DESCRIPTION</span></span>
<span data-ttu-id="884f2-109">**New-AzMetricAlertRuleV2Criteria** Cmdlet 會建立一個當地公制準則物件，做為 [輸入 Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) Cmdlet，以建立新的公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="884f2-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="884f2-110">例子</span><span class="sxs-lookup"><span data-stu-id="884f2-110">EXAMPLES</span></span>

### <span data-ttu-id="884f2-111">範例 1：建立簡單的公制警示準則</span><span class="sxs-lookup"><span data-stu-id="884f2-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="884f2-112">此命令會建立簡易的公制警示準則，可用於公制警示規則</span><span class="sxs-lookup"><span data-stu-id="884f2-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="884f2-113">範例 2：建立動態公制警示準則</span><span class="sxs-lookup"><span data-stu-id="884f2-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
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

<span data-ttu-id="884f2-114">此命令會建立可在公制警示規則中使用的動態計量警示準則</span><span class="sxs-lookup"><span data-stu-id="884f2-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="884f2-115">範例 3：建立更複雜的公制警示準則</span><span class="sxs-lookup"><span data-stu-id="884f2-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="884f2-116">這組命令會建立更複雜的公制警示準則，其中包含維度選取範圍</span><span class="sxs-lookup"><span data-stu-id="884f2-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="884f2-117">範例 4：建立 Webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="884f2-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="884f2-118">此命令會建立可在公制警示規則中使用的 Webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="884f2-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="884f2-119">參數</span><span class="sxs-lookup"><span data-stu-id="884f2-119">PARAMETERS</span></span>

### <span data-ttu-id="884f2-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="884f2-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="884f2-121">應用程式深入資訊資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="884f2-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884f2-122">-DefaultProfile</span></span>
<span data-ttu-id="884f2-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="884f2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884f2-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="884f2-124">-DimensionSelection</span></span>
<span data-ttu-id="884f2-125">維度條件清單</span><span class="sxs-lookup"><span data-stu-id="884f2-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="884f2-126">-DynamicThreshold</span></span>
<span data-ttu-id="884f2-127">切換參數以使用動態閾數值型別</span><span class="sxs-lookup"><span data-stu-id="884f2-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="884f2-128">-一次使用一個</span><span class="sxs-lookup"><span data-stu-id="884f2-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="884f2-129">點總數</span><span class="sxs-lookup"><span data-stu-id="884f2-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="884f2-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="884f2-130">-FailedLocationCount</span></span>
<span data-ttu-id="884f2-131">要提醒的失敗位置數目的最小值。</span><span class="sxs-lookup"><span data-stu-id="884f2-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="884f2-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="884f2-133">IgnoreDataBefore 參數</span><span class="sxs-lookup"><span data-stu-id="884f2-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="884f2-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="884f2-134">-MetricName</span></span>
<span data-ttu-id="884f2-135">規則的公制名稱</span><span class="sxs-lookup"><span data-stu-id="884f2-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="884f2-136">-MetricNamespace</span></span>
<span data-ttu-id="884f2-137">度量的命名空間</span><span class="sxs-lookup"><span data-stu-id="884f2-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-138">-運算子</span><span class="sxs-lookup"><span data-stu-id="884f2-138">-Operator</span></span>
<span data-ttu-id="884f2-139">規則條件運算子</span><span class="sxs-lookup"><span data-stu-id="884f2-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="884f2-140">-SkipMetricValidation</span></span>
<span data-ttu-id="884f2-141">允許讓系統略過公制驗證，以建立尚未過系統化之自訂計量的警示規則</span><span class="sxs-lookup"><span data-stu-id="884f2-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-142">-閾值</span><span class="sxs-lookup"><span data-stu-id="884f2-142">-Threshold</span></span>
<span data-ttu-id="884f2-143">規則條件的閾值</span><span class="sxs-lookup"><span data-stu-id="884f2-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="884f2-144">-閾值敏感度</span><span class="sxs-lookup"><span data-stu-id="884f2-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="884f2-145">規則條件的敏感度</span><span class="sxs-lookup"><span data-stu-id="884f2-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="884f2-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="884f2-146">-TimeAggregation</span></span>
<span data-ttu-id="884f2-147">用來跨視窗間隔匯總多個公制值的匯總作業</span><span class="sxs-lookup"><span data-stu-id="884f2-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="884f2-148">-ViolationCount</span></span>
<span data-ttu-id="884f2-149">在選取的回視時間範圍內，提高警示所需的最低違規次數</span><span class="sxs-lookup"><span data-stu-id="884f2-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="884f2-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="884f2-150">-WebTest</span></span>
<span data-ttu-id="884f2-151">切換參數以使用可用性準則類型</span><span class="sxs-lookup"><span data-stu-id="884f2-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="884f2-152">-WebTestId</span></span>
<span data-ttu-id="884f2-153">應用程式深入資訊 Web 測試識別碼。</span><span class="sxs-lookup"><span data-stu-id="884f2-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884f2-154">CommonParameters</span></span>
<span data-ttu-id="884f2-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="884f2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884f2-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="884f2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884f2-157">輸入</span><span class="sxs-lookup"><span data-stu-id="884f2-157">INPUTS</span></span>

### <span data-ttu-id="884f2-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="884f2-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="884f2-159">輸出</span><span class="sxs-lookup"><span data-stu-id="884f2-159">OUTPUTS</span></span>

### <span data-ttu-id="884f2-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="884f2-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="884f2-161">筆記</span><span class="sxs-lookup"><span data-stu-id="884f2-161">NOTES</span></span>

## <span data-ttu-id="884f2-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="884f2-162">RELATED LINKS</span></span>
