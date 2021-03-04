---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 193c0c8b263f7ceee62cc7cb99c47769a22c7633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909585"
---
# <span data-ttu-id="ed51d-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="ed51d-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="ed51d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed51d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed51d-103">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="ed51d-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="ed51d-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed51d-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed51d-105">描述</span><span class="sxs-lookup"><span data-stu-id="ed51d-105">DESCRIPTION</span></span>
<span data-ttu-id="ed51d-106">**New-AzAutoscaleRule** Cmdlet 會建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="ed51d-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="ed51d-107">例子</span><span class="sxs-lookup"><span data-stu-id="ed51d-107">EXAMPLES</span></span>

### <span data-ttu-id="ed51d-108">範例 1：建立規則</span><span class="sxs-lookup"><span data-stu-id="ed51d-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="ed51d-109">此命令會建立規則。</span><span class="sxs-lookup"><span data-stu-id="ed51d-109">This command creates a rule.</span></span>

### <span data-ttu-id="ed51d-110">範例 2：建立兩個規則</span><span class="sxs-lookup"><span data-stu-id="ed51d-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="ed51d-111">第一個命令會為要求度量建立規則，然後將它儲存在 $Rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed51d-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="ed51d-112">第二個命令會為要求度量建立第二個規則，然後將它儲存在 $Rule 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed51d-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="ed51d-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="ed51d-113">Example 3</span></span>

<span data-ttu-id="ed51d-114">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="ed51d-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="ed51d-115"> (自動) </span><span class="sxs-lookup"><span data-stu-id="ed51d-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="ed51d-116">參數</span><span class="sxs-lookup"><span data-stu-id="ed51d-116">PARAMETERS</span></span>

### <span data-ttu-id="ed51d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed51d-117">-DefaultProfile</span></span>
<span data-ttu-id="ed51d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ed51d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed51d-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ed51d-119">-MetricName</span></span>
<span data-ttu-id="ed51d-120">指定度量的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed51d-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ed51d-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="ed51d-121">-MetricResourceId</span></span>
<span data-ttu-id="ed51d-122">指定公制資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed51d-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="ed51d-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="ed51d-123">-MetricStatistic</span></span>
<span data-ttu-id="ed51d-124">指定公制統計值。</span><span class="sxs-lookup"><span data-stu-id="ed51d-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="ed51d-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed51d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed51d-126">平均</span><span class="sxs-lookup"><span data-stu-id="ed51d-126">Average</span></span>
- <span data-ttu-id="ed51d-127">最小值</span><span class="sxs-lookup"><span data-stu-id="ed51d-127">Min</span></span>
- <span data-ttu-id="ed51d-128">麥克斯</span><span class="sxs-lookup"><span data-stu-id="ed51d-128">Max</span></span>
- <span data-ttu-id="ed51d-129">和</span><span class="sxs-lookup"><span data-stu-id="ed51d-129">Sum</span></span>

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

### <span data-ttu-id="ed51d-130">-運算子</span><span class="sxs-lookup"><span data-stu-id="ed51d-130">-Operator</span></span>
<span data-ttu-id="ed51d-131">指定運算子。</span><span class="sxs-lookup"><span data-stu-id="ed51d-131">Specifies the operator.</span></span>
<span data-ttu-id="ed51d-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed51d-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed51d-133">等於</span><span class="sxs-lookup"><span data-stu-id="ed51d-133">Equals</span></span>
- <span data-ttu-id="ed51d-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="ed51d-134">NotEquals</span></span>
- <span data-ttu-id="ed51d-135">Greater用</span><span class="sxs-lookup"><span data-stu-id="ed51d-135">GreaterThan</span></span>
- <span data-ttu-id="ed51d-136">GreaterQualOrEqual</span><span class="sxs-lookup"><span data-stu-id="ed51d-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="ed51d-137">Less一維</span><span class="sxs-lookup"><span data-stu-id="ed51d-137">LessThan</span></span>
- <span data-ttu-id="ed51d-138">LessQualOrEqual</span><span class="sxs-lookup"><span data-stu-id="ed51d-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="ed51d-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="ed51d-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="ed51d-140">指定自動縮放動作的結束時間。</span><span class="sxs-lookup"><span data-stu-id="ed51d-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="ed51d-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="ed51d-141">-ScaleActionDirection</span></span>
<span data-ttu-id="ed51d-142">指定縮放比例動作方向。</span><span class="sxs-lookup"><span data-stu-id="ed51d-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="ed51d-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed51d-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed51d-144">沒有</span><span class="sxs-lookup"><span data-stu-id="ed51d-144">None</span></span>
- <span data-ttu-id="ed51d-145">增加</span><span class="sxs-lookup"><span data-stu-id="ed51d-145">Increase</span></span>
- <span data-ttu-id="ed51d-146">減少</span><span class="sxs-lookup"><span data-stu-id="ed51d-146">Decrease</span></span>

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

### <span data-ttu-id="ed51d-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="ed51d-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="ed51d-148">指定縮放比例類型。</span><span class="sxs-lookup"><span data-stu-id="ed51d-148">Specifies the scale type.</span></span>
<span data-ttu-id="ed51d-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed51d-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed51d-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="ed51d-150">ChangeSize</span></span>
- <span data-ttu-id="ed51d-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="ed51d-151">ChangeCount</span></span>
- <span data-ttu-id="ed51d-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="ed51d-152">PercentChangeCount</span></span>
- <span data-ttu-id="ed51d-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="ed51d-153">ExactCount</span></span>

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

### <span data-ttu-id="ed51d-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="ed51d-154">-ScaleActionValue</span></span>
<span data-ttu-id="ed51d-155">指定動作值。</span><span class="sxs-lookup"><span data-stu-id="ed51d-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="ed51d-156">-閾值</span><span class="sxs-lookup"><span data-stu-id="ed51d-156">-Threshold</span></span>
<span data-ttu-id="ed51d-157">指定公制值的閾值。</span><span class="sxs-lookup"><span data-stu-id="ed51d-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="ed51d-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="ed51d-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="ed51d-159">指定時間匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="ed51d-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="ed51d-160">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed51d-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed51d-161">平均</span><span class="sxs-lookup"><span data-stu-id="ed51d-161">Average</span></span>
- <span data-ttu-id="ed51d-162">最低</span><span class="sxs-lookup"><span data-stu-id="ed51d-162">Minimum</span></span>
- <span data-ttu-id="ed51d-163">最大</span><span class="sxs-lookup"><span data-stu-id="ed51d-163">Maximum</span></span>
- <span data-ttu-id="ed51d-164">最後</span><span class="sxs-lookup"><span data-stu-id="ed51d-164">Last</span></span>
- <span data-ttu-id="ed51d-165">總計、計數</span><span class="sxs-lookup"><span data-stu-id="ed51d-165">Total, Count</span></span>

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

### <span data-ttu-id="ed51d-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ed51d-166">-TimeGrain</span></span>
<span data-ttu-id="ed51d-167">指定時間紋理。</span><span class="sxs-lookup"><span data-stu-id="ed51d-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="ed51d-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="ed51d-168">-TimeWindow</span></span>
<span data-ttu-id="ed51d-169">指定時間視窗。</span><span class="sxs-lookup"><span data-stu-id="ed51d-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="ed51d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed51d-170">CommonParameters</span></span>
<span data-ttu-id="ed51d-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed51d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed51d-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed51d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed51d-173">輸入</span><span class="sxs-lookup"><span data-stu-id="ed51d-173">INPUTS</span></span>

### <span data-ttu-id="ed51d-174">System.String</span><span class="sxs-lookup"><span data-stu-id="ed51d-174">System.String</span></span>

### <span data-ttu-id="ed51d-175">Microsoft.Azure.management.monitor.management.models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="ed51d-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="ed51d-176">Microsoft.Azure.management.monitor.management.models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="ed51d-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="ed51d-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="ed51d-177">System.Double</span></span>

### <span data-ttu-id="ed51d-178">Microsoft.Azure.management.monitor.management.models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="ed51d-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="ed51d-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ed51d-179">System.TimeSpan</span></span>

### <span data-ttu-id="ed51d-180">Microsoft.Azure.management.monitor.management.models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="ed51d-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="ed51d-181">Microsoft.Azure.management.monitor.management.models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="ed51d-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="ed51d-182">輸出</span><span class="sxs-lookup"><span data-stu-id="ed51d-182">OUTPUTS</span></span>

### <span data-ttu-id="ed51d-183">Microsoft.Azure.management.monitor.management.models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="ed51d-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="ed51d-184">筆記</span><span class="sxs-lookup"><span data-stu-id="ed51d-184">NOTES</span></span>

## <span data-ttu-id="ed51d-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed51d-185">RELATED LINKS</span></span>

[<span data-ttu-id="ed51d-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ed51d-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="ed51d-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="ed51d-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="ed51d-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ed51d-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="ed51d-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="ed51d-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="ed51d-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ed51d-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


