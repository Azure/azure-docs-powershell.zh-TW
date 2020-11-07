---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 2464a3b7fb35cce28dd06884cd8ed69e5197eced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786685"
---
# <span data-ttu-id="ab6fe-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="ab6fe-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="ab6fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6fe-103">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="ab6fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab6fe-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab6fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab6fe-105">DESCRIPTION</span></span>
<span data-ttu-id="ab6fe-106">**新的-AzAutoscaleRule** Cmdlet 會建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="ab6fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab6fe-107">EXAMPLES</span></span>

### <span data-ttu-id="ab6fe-108">範例1：建立規則</span><span class="sxs-lookup"><span data-stu-id="ab6fe-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="ab6fe-109">這個命令會建立規則。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-109">This command creates a rule.</span></span>

### <span data-ttu-id="ab6fe-110">範例2：建立兩個規則</span><span class="sxs-lookup"><span data-stu-id="ab6fe-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="ab6fe-111">第一個命令會針對要求公制建立規則，然後將它儲存在 $Rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="ab6fe-112">第二個命令會針對要求公制建立第二個規則，然後將它儲存在 $Rule 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="ab6fe-113">參數</span><span class="sxs-lookup"><span data-stu-id="ab6fe-113">PARAMETERS</span></span>

### <span data-ttu-id="ab6fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6fe-114">-DefaultProfile</span></span>
<span data-ttu-id="ab6fe-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ab6fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab6fe-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ab6fe-116">-MetricName</span></span>
<span data-ttu-id="ab6fe-117">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ab6fe-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="ab6fe-118">-MetricResourceId</span></span>
<span data-ttu-id="ab6fe-119">指定公制資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="ab6fe-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="ab6fe-120">-MetricStatistic</span></span>
<span data-ttu-id="ab6fe-121">指定度量統計值。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="ab6fe-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab6fe-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab6fe-123">而言</span><span class="sxs-lookup"><span data-stu-id="ab6fe-123">Average</span></span>
- <span data-ttu-id="ab6fe-124">Dtu</span><span class="sxs-lookup"><span data-stu-id="ab6fe-124">Min</span></span>
- <span data-ttu-id="ab6fe-125">大會</span><span class="sxs-lookup"><span data-stu-id="ab6fe-125">Max</span></span>
- <span data-ttu-id="ab6fe-126">總計</span><span class="sxs-lookup"><span data-stu-id="ab6fe-126">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-127">-運算子</span><span class="sxs-lookup"><span data-stu-id="ab6fe-127">-Operator</span></span>
<span data-ttu-id="ab6fe-128">指定運算子。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-128">Specifies the operator.</span></span>
<span data-ttu-id="ab6fe-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab6fe-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab6fe-130">等於</span><span class="sxs-lookup"><span data-stu-id="ab6fe-130">Equals</span></span>
- <span data-ttu-id="ab6fe-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="ab6fe-131">NotEquals</span></span>
- <span data-ttu-id="ab6fe-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="ab6fe-132">GreaterThan</span></span>
- <span data-ttu-id="ab6fe-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="ab6fe-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="ab6fe-134">小於</span><span class="sxs-lookup"><span data-stu-id="ab6fe-134">LessThan</span></span>
- <span data-ttu-id="ab6fe-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="ab6fe-135">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="ab6fe-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="ab6fe-137">指定自動縮放動作 cooldown 時間。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="ab6fe-138">-ScaleActionDirection</span></span>
<span data-ttu-id="ab6fe-139">指定縮放動作方向。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="ab6fe-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab6fe-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab6fe-141">所有</span><span class="sxs-lookup"><span data-stu-id="ab6fe-141">None</span></span>
- <span data-ttu-id="ab6fe-142">遞增</span><span class="sxs-lookup"><span data-stu-id="ab6fe-142">Increase</span></span>
- <span data-ttu-id="ab6fe-143">縮減</span><span class="sxs-lookup"><span data-stu-id="ab6fe-143">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="ab6fe-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="ab6fe-145">指定縮放類型。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-145">Specifies the scale type.</span></span>
<span data-ttu-id="ab6fe-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab6fe-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab6fe-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="ab6fe-147">ChangeSize</span></span>
- <span data-ttu-id="ab6fe-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="ab6fe-148">ChangeCount</span></span>
- <span data-ttu-id="ab6fe-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="ab6fe-149">PercentChangeCount</span></span>
- <span data-ttu-id="ab6fe-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="ab6fe-150">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="ab6fe-151">-ScaleActionValue</span></span>
<span data-ttu-id="ab6fe-152">指定 [動作] 值。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="ab6fe-153">-閾值</span><span class="sxs-lookup"><span data-stu-id="ab6fe-153">-Threshold</span></span>
<span data-ttu-id="ab6fe-154">指定公制值的閾值。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="ab6fe-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="ab6fe-156">指定時間匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="ab6fe-157">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab6fe-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab6fe-158">而言</span><span class="sxs-lookup"><span data-stu-id="ab6fe-158">Average</span></span>
- <span data-ttu-id="ab6fe-159">基本</span><span class="sxs-lookup"><span data-stu-id="ab6fe-159">Minimum</span></span>
- <span data-ttu-id="ab6fe-160">大化</span><span class="sxs-lookup"><span data-stu-id="ab6fe-160">Maximum</span></span>
- <span data-ttu-id="ab6fe-161">年</span><span class="sxs-lookup"><span data-stu-id="ab6fe-161">Last</span></span>
- <span data-ttu-id="ab6fe-162">總計、計數</span><span class="sxs-lookup"><span data-stu-id="ab6fe-162">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ab6fe-163">-TimeGrain</span></span>
<span data-ttu-id="ab6fe-164">指定時間細微性。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-164">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="ab6fe-165">-TimeWindow</span></span>
<span data-ttu-id="ab6fe-166">指定時間範圍。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-166">Specifies the time window.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6fe-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6fe-167">CommonParameters</span></span>
<span data-ttu-id="ab6fe-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6fe-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6fe-170">輸入</span><span class="sxs-lookup"><span data-stu-id="ab6fe-170">INPUTS</span></span>

### <span data-ttu-id="ab6fe-171">System.object</span><span class="sxs-lookup"><span data-stu-id="ab6fe-171">System.String</span></span>

### <span data-ttu-id="ab6fe-172">ComparisonOperationType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="ab6fe-173">MetricStatisticType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="ab6fe-174">Double</span><span class="sxs-lookup"><span data-stu-id="ab6fe-174">System.Double</span></span>

### <span data-ttu-id="ab6fe-175">TimeAggregationType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="ab6fe-176">System.object</span><span class="sxs-lookup"><span data-stu-id="ab6fe-176">System.TimeSpan</span></span>

### <span data-ttu-id="ab6fe-177">ScaleDirection 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="ab6fe-178">ScaleType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="ab6fe-179">輸出</span><span class="sxs-lookup"><span data-stu-id="ab6fe-179">OUTPUTS</span></span>

### <span data-ttu-id="ab6fe-180">ScaleRule 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ab6fe-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="ab6fe-181">筆記</span><span class="sxs-lookup"><span data-stu-id="ab6fe-181">NOTES</span></span>

## <span data-ttu-id="ab6fe-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab6fe-182">RELATED LINKS</span></span>

[<span data-ttu-id="ab6fe-183">附加 AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ab6fe-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="ab6fe-184">AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="ab6fe-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="ab6fe-185">AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ab6fe-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="ab6fe-186">新-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="ab6fe-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="ab6fe-187">移除-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ab6fe-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


