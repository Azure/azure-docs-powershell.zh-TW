---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786682"
---
# <span data-ttu-id="7a50c-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7a50c-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="7a50c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a50c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a50c-103">建立可以用來建立新度量警示的 [局部準則] 物件</span><span class="sxs-lookup"><span data-stu-id="7a50c-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="7a50c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a50c-104">SYNTAX</span></span>

### <span data-ttu-id="7a50c-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a50c-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a50c-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a50c-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a50c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7a50c-107">DESCRIPTION</span></span>
<span data-ttu-id="7a50c-108">**新的-AzMetricAlertRuleV2Criteria** Cmdlet 會建立一個 [局部公制準則] 物件，以做為建立新度量警示規則的輸入 Add-AzMetricAlertRuleV2 Cmdlet 使用。</span><span class="sxs-lookup"><span data-stu-id="7a50c-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="7a50c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7a50c-109">EXAMPLES</span></span>

### <span data-ttu-id="7a50c-110">範例1：建立簡單的度量警示準則</span><span class="sxs-lookup"><span data-stu-id="7a50c-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="7a50c-111">這個命令會建立可在度量警報規則中使用的簡單度量警報準則</span><span class="sxs-lookup"><span data-stu-id="7a50c-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="7a50c-112">範例2：建立更複雜的度量警報準則</span><span class="sxs-lookup"><span data-stu-id="7a50c-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="7a50c-113">這組命令會建立更複雜的度量警示準則，包括維度選取</span><span class="sxs-lookup"><span data-stu-id="7a50c-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="7a50c-114">參數</span><span class="sxs-lookup"><span data-stu-id="7a50c-114">PARAMETERS</span></span>

### <span data-ttu-id="7a50c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a50c-115">-DefaultProfile</span></span>
<span data-ttu-id="7a50c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a50c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7a50c-117">-DimensionSelection</span></span>
<span data-ttu-id="7a50c-118">維度條件清單</span><span class="sxs-lookup"><span data-stu-id="7a50c-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="7a50c-119">-DynamicThreshold</span></span>
<span data-ttu-id="7a50c-120">規則條件的動態閾值</span><span class="sxs-lookup"><span data-stu-id="7a50c-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="7a50c-121">-FailingPeriod</span></span>
<span data-ttu-id="7a50c-122">規則條件的失敗期間</span><span class="sxs-lookup"><span data-stu-id="7a50c-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="7a50c-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="7a50c-124">IgnoreDataBefore 參數</span><span class="sxs-lookup"><span data-stu-id="7a50c-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="7a50c-125">-MetricName</span></span>
<span data-ttu-id="7a50c-126">規則的度量名稱</span><span class="sxs-lookup"><span data-stu-id="7a50c-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="7a50c-127">-MetricNamespace</span></span>
<span data-ttu-id="7a50c-128">公制的命名空間</span><span class="sxs-lookup"><span data-stu-id="7a50c-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-129">-運算子</span><span class="sxs-lookup"><span data-stu-id="7a50c-129">-Operator</span></span>
<span data-ttu-id="7a50c-130">規則條件運算子</span><span class="sxs-lookup"><span data-stu-id="7a50c-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-131">敏感度</span><span class="sxs-lookup"><span data-stu-id="7a50c-131">-Sensitivity</span></span>
<span data-ttu-id="7a50c-132">規則條件的敏感度</span><span class="sxs-lookup"><span data-stu-id="7a50c-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-133">-閾值</span><span class="sxs-lookup"><span data-stu-id="7a50c-133">-Threshold</span></span>
<span data-ttu-id="7a50c-134">規則條件的閾值</span><span class="sxs-lookup"><span data-stu-id="7a50c-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="7a50c-135">-TimeAggregation</span></span>
<span data-ttu-id="7a50c-136">用於在整個視窗間隔中累加多個公制值的聚合運算</span><span class="sxs-lookup"><span data-stu-id="7a50c-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="7a50c-137">-TotalPeriod</span></span>
<span data-ttu-id="7a50c-138">規則條件的總期間</span><span class="sxs-lookup"><span data-stu-id="7a50c-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a50c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a50c-139">CommonParameters</span></span>
<span data-ttu-id="7a50c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a50c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7a50c-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a50c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a50c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7a50c-142">INPUTS</span></span>

### <span data-ttu-id="7a50c-143">PSMetricDimension [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="7a50c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="7a50c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7a50c-144">OUTPUTS</span></span>

### <span data-ttu-id="7a50c-145">PSMetricCriteria 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="7a50c-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="7a50c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7a50c-146">NOTES</span></span>

## <span data-ttu-id="7a50c-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a50c-147">RELATED LINKS</span></span>
