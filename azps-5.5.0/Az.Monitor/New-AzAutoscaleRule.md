---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140631"
---
# <span data-ttu-id="899c3-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="899c3-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="899c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="899c3-102">SYNOPSIS</span></span>
<span data-ttu-id="899c3-103">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="899c3-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="899c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="899c3-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="899c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="899c3-105">DESCRIPTION</span></span>
<span data-ttu-id="899c3-106">**新的-AzAutoscaleRule** Cmdlet 會建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="899c3-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="899c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="899c3-107">EXAMPLES</span></span>

### <span data-ttu-id="899c3-108">範例1：建立規則</span><span class="sxs-lookup"><span data-stu-id="899c3-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="899c3-109">這個命令會建立規則。</span><span class="sxs-lookup"><span data-stu-id="899c3-109">This command creates a rule.</span></span>

### <span data-ttu-id="899c3-110">範例2：建立兩個規則</span><span class="sxs-lookup"><span data-stu-id="899c3-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="899c3-111">第一個命令會針對要求公制建立規則，然後將它儲存在 $Rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="899c3-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="899c3-112">第二個命令會針對要求公制建立第二個規則，然後將它儲存在 $Rule 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="899c3-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="899c3-113">範例3</span><span class="sxs-lookup"><span data-stu-id="899c3-113">Example 3</span></span>

<span data-ttu-id="899c3-114">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="899c3-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="899c3-115"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="899c3-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="899c3-116">參數</span><span class="sxs-lookup"><span data-stu-id="899c3-116">PARAMETERS</span></span>

### <span data-ttu-id="899c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899c3-117">-DefaultProfile</span></span>
<span data-ttu-id="899c3-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="899c3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="899c3-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="899c3-119">-MetricName</span></span>
<span data-ttu-id="899c3-120">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="899c3-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="899c3-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="899c3-121">-MetricResourceId</span></span>
<span data-ttu-id="899c3-122">指定公制資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="899c3-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="899c3-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="899c3-123">-MetricStatistic</span></span>
<span data-ttu-id="899c3-124">指定度量統計值。</span><span class="sxs-lookup"><span data-stu-id="899c3-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="899c3-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="899c3-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="899c3-126">而言</span><span class="sxs-lookup"><span data-stu-id="899c3-126">Average</span></span>
- <span data-ttu-id="899c3-127">Dtu</span><span class="sxs-lookup"><span data-stu-id="899c3-127">Min</span></span>
- <span data-ttu-id="899c3-128">大會</span><span class="sxs-lookup"><span data-stu-id="899c3-128">Max</span></span>
- <span data-ttu-id="899c3-129">總計</span><span class="sxs-lookup"><span data-stu-id="899c3-129">Sum</span></span>

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

### <span data-ttu-id="899c3-130">-運算子</span><span class="sxs-lookup"><span data-stu-id="899c3-130">-Operator</span></span>
<span data-ttu-id="899c3-131">指定運算子。</span><span class="sxs-lookup"><span data-stu-id="899c3-131">Specifies the operator.</span></span>
<span data-ttu-id="899c3-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="899c3-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="899c3-133">等於</span><span class="sxs-lookup"><span data-stu-id="899c3-133">Equals</span></span>
- <span data-ttu-id="899c3-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="899c3-134">NotEquals</span></span>
- <span data-ttu-id="899c3-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="899c3-135">GreaterThan</span></span>
- <span data-ttu-id="899c3-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="899c3-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="899c3-137">小於</span><span class="sxs-lookup"><span data-stu-id="899c3-137">LessThan</span></span>
- <span data-ttu-id="899c3-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="899c3-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="899c3-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="899c3-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="899c3-140">指定自動縮放動作 cooldown 時間。</span><span class="sxs-lookup"><span data-stu-id="899c3-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="899c3-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="899c3-141">-ScaleActionDirection</span></span>
<span data-ttu-id="899c3-142">指定縮放動作方向。</span><span class="sxs-lookup"><span data-stu-id="899c3-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="899c3-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="899c3-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="899c3-144">所有</span><span class="sxs-lookup"><span data-stu-id="899c3-144">None</span></span>
- <span data-ttu-id="899c3-145">遞增</span><span class="sxs-lookup"><span data-stu-id="899c3-145">Increase</span></span>
- <span data-ttu-id="899c3-146">縮減</span><span class="sxs-lookup"><span data-stu-id="899c3-146">Decrease</span></span>

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

### <span data-ttu-id="899c3-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="899c3-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="899c3-148">指定縮放類型。</span><span class="sxs-lookup"><span data-stu-id="899c3-148">Specifies the scale type.</span></span>
<span data-ttu-id="899c3-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="899c3-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="899c3-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="899c3-150">ChangeSize</span></span>
- <span data-ttu-id="899c3-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="899c3-151">ChangeCount</span></span>
- <span data-ttu-id="899c3-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="899c3-152">PercentChangeCount</span></span>
- <span data-ttu-id="899c3-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="899c3-153">ExactCount</span></span>

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

### <span data-ttu-id="899c3-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="899c3-154">-ScaleActionValue</span></span>
<span data-ttu-id="899c3-155">指定 [動作] 值。</span><span class="sxs-lookup"><span data-stu-id="899c3-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="899c3-156">-閾值</span><span class="sxs-lookup"><span data-stu-id="899c3-156">-Threshold</span></span>
<span data-ttu-id="899c3-157">指定公制值的閾值。</span><span class="sxs-lookup"><span data-stu-id="899c3-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="899c3-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="899c3-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="899c3-159">指定時間匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="899c3-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="899c3-160">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="899c3-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="899c3-161">而言</span><span class="sxs-lookup"><span data-stu-id="899c3-161">Average</span></span>
- <span data-ttu-id="899c3-162">基本</span><span class="sxs-lookup"><span data-stu-id="899c3-162">Minimum</span></span>
- <span data-ttu-id="899c3-163">大化</span><span class="sxs-lookup"><span data-stu-id="899c3-163">Maximum</span></span>
- <span data-ttu-id="899c3-164">年</span><span class="sxs-lookup"><span data-stu-id="899c3-164">Last</span></span>
- <span data-ttu-id="899c3-165">總計、計數</span><span class="sxs-lookup"><span data-stu-id="899c3-165">Total, Count</span></span>

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

### <span data-ttu-id="899c3-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="899c3-166">-TimeGrain</span></span>
<span data-ttu-id="899c3-167">指定時間細微性。</span><span class="sxs-lookup"><span data-stu-id="899c3-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="899c3-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="899c3-168">-TimeWindow</span></span>
<span data-ttu-id="899c3-169">指定時間範圍。</span><span class="sxs-lookup"><span data-stu-id="899c3-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="899c3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899c3-170">CommonParameters</span></span>
<span data-ttu-id="899c3-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="899c3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899c3-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="899c3-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899c3-173">輸入</span><span class="sxs-lookup"><span data-stu-id="899c3-173">INPUTS</span></span>

### <span data-ttu-id="899c3-174">System.object</span><span class="sxs-lookup"><span data-stu-id="899c3-174">System.String</span></span>

### <span data-ttu-id="899c3-175">ComparisonOperationType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="899c3-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="899c3-176">MetricStatisticType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="899c3-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="899c3-177">Double</span><span class="sxs-lookup"><span data-stu-id="899c3-177">System.Double</span></span>

### <span data-ttu-id="899c3-178">TimeAggregationType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="899c3-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="899c3-179">System.object</span><span class="sxs-lookup"><span data-stu-id="899c3-179">System.TimeSpan</span></span>

### <span data-ttu-id="899c3-180">ScaleDirection 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="899c3-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="899c3-181">ScaleType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="899c3-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="899c3-182">輸出</span><span class="sxs-lookup"><span data-stu-id="899c3-182">OUTPUTS</span></span>

### <span data-ttu-id="899c3-183">ScaleRule 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="899c3-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="899c3-184">筆記</span><span class="sxs-lookup"><span data-stu-id="899c3-184">NOTES</span></span>

## <span data-ttu-id="899c3-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="899c3-185">RELATED LINKS</span></span>

[<span data-ttu-id="899c3-186">附加 AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="899c3-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="899c3-187">AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="899c3-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="899c3-188">AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="899c3-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="899c3-189">新-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="899c3-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="899c3-190">移除-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="899c3-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


