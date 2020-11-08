---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135871"
---
# <span data-ttu-id="e1ed8-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e1ed8-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="e1ed8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ed8-103">建立可以用來建立新度量警示的 [局部準則] 物件</span><span class="sxs-lookup"><span data-stu-id="e1ed8-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="e1ed8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1ed8-104">SYNTAX</span></span>

### <span data-ttu-id="e1ed8-105">StaticThresholdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e1ed8-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ed8-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ed8-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ed8-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ed8-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ed8-108">說明</span><span class="sxs-lookup"><span data-stu-id="e1ed8-108">DESCRIPTION</span></span>
<span data-ttu-id="e1ed8-109">**新的-AzMetricAlertRuleV2Criteria** Cmdlet 會建立一個 [局部公制準則] 物件，以做為建立新度量警示規則的輸入 Add-AzMetricAlertRuleV2 Cmdlet 使用。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="e1ed8-110">示例</span><span class="sxs-lookup"><span data-stu-id="e1ed8-110">EXAMPLES</span></span>

### <span data-ttu-id="e1ed8-111">範例1：建立簡單的度量警示準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="e1ed8-112">這個命令會建立可在度量警報規則中使用的簡單度量警報準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="e1ed8-113">範例2：建立動態度量警示準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="e1ed8-114">這個命令會建立可在度量警示規則中使用的動態度量警示準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="e1ed8-115">範例3：建立更複雜的度量警報準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="e1ed8-116">這組命令會建立更複雜的度量警示準則，包括維度選取</span><span class="sxs-lookup"><span data-stu-id="e1ed8-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="e1ed8-117">範例4：建立 webtest 的可用性準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="e1ed8-118">這個命令會建立可在度量警示規則中使用的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="e1ed8-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="e1ed8-119">參數</span><span class="sxs-lookup"><span data-stu-id="e1ed8-119">PARAMETERS</span></span>

### <span data-ttu-id="e1ed8-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="e1ed8-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="e1ed8-121">Application Insights 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="e1ed8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ed8-122">-DefaultProfile</span></span>
<span data-ttu-id="e1ed8-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ed8-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e1ed8-124">-DimensionSelection</span></span>
<span data-ttu-id="e1ed8-125">維度條件清單</span><span class="sxs-lookup"><span data-stu-id="e1ed8-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="e1ed8-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="e1ed8-126">-DynamicThreshold</span></span>
<span data-ttu-id="e1ed8-127">使用動態閾數值型別的切換參數</span><span class="sxs-lookup"><span data-stu-id="e1ed8-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="e1ed8-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="e1ed8-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="e1ed8-129">檢查點的總數</span><span class="sxs-lookup"><span data-stu-id="e1ed8-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="e1ed8-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="e1ed8-130">-FailedLocationCount</span></span>
<span data-ttu-id="e1ed8-131">產生警示之失敗位置的最小數目。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="e1ed8-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="e1ed8-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="e1ed8-133">IgnoreDataBefore 參數</span><span class="sxs-lookup"><span data-stu-id="e1ed8-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="e1ed8-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e1ed8-134">-MetricName</span></span>
<span data-ttu-id="e1ed8-135">規則的度量名稱</span><span class="sxs-lookup"><span data-stu-id="e1ed8-135">The metric name for rule</span></span>

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

### <span data-ttu-id="e1ed8-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e1ed8-136">-MetricNamespace</span></span>
<span data-ttu-id="e1ed8-137">公制的命名空間</span><span class="sxs-lookup"><span data-stu-id="e1ed8-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="e1ed8-138">-運算子</span><span class="sxs-lookup"><span data-stu-id="e1ed8-138">-Operator</span></span>
<span data-ttu-id="e1ed8-139">規則條件運算子</span><span class="sxs-lookup"><span data-stu-id="e1ed8-139">The rule condition operator</span></span>

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

### <span data-ttu-id="e1ed8-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="e1ed8-140">-SkipMetricValidation</span></span>
<span data-ttu-id="e1ed8-141">可讓您在尚未發出的自訂度量上建立警示規則，方法是使指標驗證略過</span><span class="sxs-lookup"><span data-stu-id="e1ed8-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="e1ed8-142">-閾值</span><span class="sxs-lookup"><span data-stu-id="e1ed8-142">-Threshold</span></span>
<span data-ttu-id="e1ed8-143">規則條件的閾值</span><span class="sxs-lookup"><span data-stu-id="e1ed8-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="e1ed8-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="e1ed8-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="e1ed8-145">規則條件的敏感度</span><span class="sxs-lookup"><span data-stu-id="e1ed8-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="e1ed8-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="e1ed8-146">-TimeAggregation</span></span>
<span data-ttu-id="e1ed8-147">用於在整個視窗間隔中累加多個公制值的聚合運算</span><span class="sxs-lookup"><span data-stu-id="e1ed8-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="e1ed8-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="e1ed8-148">-ViolationCount</span></span>
<span data-ttu-id="e1ed8-149">在所選的 lookback 時間視窗中產生提醒所需的最小違規數量</span><span class="sxs-lookup"><span data-stu-id="e1ed8-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="e1ed8-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="e1ed8-150">-WebTest</span></span>
<span data-ttu-id="e1ed8-151">使用可用性準則類型的切換參數</span><span class="sxs-lookup"><span data-stu-id="e1ed8-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="e1ed8-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="e1ed8-152">-WebTestId</span></span>
<span data-ttu-id="e1ed8-153">Application Insights web 測試 Id。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="e1ed8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ed8-154">CommonParameters</span></span>
<span data-ttu-id="e1ed8-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ed8-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ed8-157">輸入</span><span class="sxs-lookup"><span data-stu-id="e1ed8-157">INPUTS</span></span>

### <span data-ttu-id="e1ed8-158">PSMetricDimension [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="e1ed8-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="e1ed8-159">輸出</span><span class="sxs-lookup"><span data-stu-id="e1ed8-159">OUTPUTS</span></span>

### <span data-ttu-id="e1ed8-160">IPSMultiMetricCriteria 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e1ed8-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="e1ed8-161">筆記</span><span class="sxs-lookup"><span data-stu-id="e1ed8-161">NOTES</span></span>

## <span data-ttu-id="e1ed8-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1ed8-162">RELATED LINKS</span></span>