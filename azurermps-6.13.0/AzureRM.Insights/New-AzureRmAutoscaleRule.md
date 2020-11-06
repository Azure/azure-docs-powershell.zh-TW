---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 5addf4bae7024d86b6a517a40a4033992047fe08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449805"
---
# <span data-ttu-id="1bf5b-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="1bf5b-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="1bf5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bf5b-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf5b-103">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bf5b-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf5b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1bf5b-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf5b-106">**新的-AzureRmAutoscaleRule** Cmdlet 會建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="1bf5b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1bf5b-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf5b-108">範例1：建立規則</span><span class="sxs-lookup"><span data-stu-id="1bf5b-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="1bf5b-109">這個命令會建立規則。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-109">This command creates a rule.</span></span>

### <span data-ttu-id="1bf5b-110">範例2：建立兩個規則</span><span class="sxs-lookup"><span data-stu-id="1bf5b-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="1bf5b-111">第一個命令會針對要求公制建立規則，然後將它儲存在 $Rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="1bf5b-112">第二個命令會針對要求公制建立第二個規則，然後將它儲存在 $Rule 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="1bf5b-113">參數</span><span class="sxs-lookup"><span data-stu-id="1bf5b-113">PARAMETERS</span></span>

### <span data-ttu-id="1bf5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf5b-114">-DefaultProfile</span></span>
<span data-ttu-id="1bf5b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1bf5b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf5b-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="1bf5b-116">-MetricName</span></span>
<span data-ttu-id="1bf5b-117">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="1bf5b-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf5b-118">-MetricResourceId</span></span>
<span data-ttu-id="1bf5b-119">指定公制資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="1bf5b-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="1bf5b-120">-MetricStatistic</span></span>
<span data-ttu-id="1bf5b-121">指定度量統計值。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="1bf5b-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1bf5b-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bf5b-123">而言</span><span class="sxs-lookup"><span data-stu-id="1bf5b-123">Average</span></span>
- <span data-ttu-id="1bf5b-124">Dtu</span><span class="sxs-lookup"><span data-stu-id="1bf5b-124">Min</span></span>
- <span data-ttu-id="1bf5b-125">大會</span><span class="sxs-lookup"><span data-stu-id="1bf5b-125">Max</span></span>
- <span data-ttu-id="1bf5b-126">總計</span><span class="sxs-lookup"><span data-stu-id="1bf5b-126">Sum</span></span>

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

### <span data-ttu-id="1bf5b-127">-運算子</span><span class="sxs-lookup"><span data-stu-id="1bf5b-127">-Operator</span></span>
<span data-ttu-id="1bf5b-128">指定運算子。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-128">Specifies the operator.</span></span>
<span data-ttu-id="1bf5b-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1bf5b-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bf5b-130">等於</span><span class="sxs-lookup"><span data-stu-id="1bf5b-130">Equals</span></span>
- <span data-ttu-id="1bf5b-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="1bf5b-131">NotEquals</span></span>
- <span data-ttu-id="1bf5b-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="1bf5b-132">GreaterThan</span></span>
- <span data-ttu-id="1bf5b-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="1bf5b-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="1bf5b-134">小於</span><span class="sxs-lookup"><span data-stu-id="1bf5b-134">LessThan</span></span>
- <span data-ttu-id="1bf5b-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="1bf5b-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="1bf5b-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="1bf5b-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="1bf5b-137">指定自動縮放動作 cooldown 時間。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="1bf5b-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="1bf5b-138">-ScaleActionDirection</span></span>
<span data-ttu-id="1bf5b-139">指定縮放動作方向。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="1bf5b-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1bf5b-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bf5b-141">所有</span><span class="sxs-lookup"><span data-stu-id="1bf5b-141">None</span></span>
- <span data-ttu-id="1bf5b-142">遞增</span><span class="sxs-lookup"><span data-stu-id="1bf5b-142">Increase</span></span>
- <span data-ttu-id="1bf5b-143">縮減</span><span class="sxs-lookup"><span data-stu-id="1bf5b-143">Decrease</span></span>

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

### <span data-ttu-id="1bf5b-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="1bf5b-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="1bf5b-145">指定縮放類型。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-145">Specifies the scale type.</span></span>
<span data-ttu-id="1bf5b-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1bf5b-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bf5b-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="1bf5b-147">ChangeSize</span></span>
- <span data-ttu-id="1bf5b-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="1bf5b-148">ChangeCount</span></span>
- <span data-ttu-id="1bf5b-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="1bf5b-149">PercentChangeCount</span></span>
- <span data-ttu-id="1bf5b-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="1bf5b-150">ExactCount</span></span>

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

### <span data-ttu-id="1bf5b-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="1bf5b-151">-ScaleActionValue</span></span>
<span data-ttu-id="1bf5b-152">指定 [動作] 值。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="1bf5b-153">-閾值</span><span class="sxs-lookup"><span data-stu-id="1bf5b-153">-Threshold</span></span>
<span data-ttu-id="1bf5b-154">指定公制值的閾值。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="1bf5b-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="1bf5b-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="1bf5b-156">指定時間匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="1bf5b-157">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1bf5b-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bf5b-158">而言</span><span class="sxs-lookup"><span data-stu-id="1bf5b-158">Average</span></span>
- <span data-ttu-id="1bf5b-159">基本</span><span class="sxs-lookup"><span data-stu-id="1bf5b-159">Minimum</span></span>
- <span data-ttu-id="1bf5b-160">大化</span><span class="sxs-lookup"><span data-stu-id="1bf5b-160">Maximum</span></span>
- <span data-ttu-id="1bf5b-161">年</span><span class="sxs-lookup"><span data-stu-id="1bf5b-161">Last</span></span>
- <span data-ttu-id="1bf5b-162">總計、計數</span><span class="sxs-lookup"><span data-stu-id="1bf5b-162">Total, Count</span></span>

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

### <span data-ttu-id="1bf5b-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="1bf5b-163">-TimeGrain</span></span>
<span data-ttu-id="1bf5b-164">指定時間細微性。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="1bf5b-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="1bf5b-165">-TimeWindow</span></span>
<span data-ttu-id="1bf5b-166">指定時間範圍。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="1bf5b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf5b-167">CommonParameters</span></span>
<span data-ttu-id="1bf5b-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf5b-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf5b-170">輸入</span><span class="sxs-lookup"><span data-stu-id="1bf5b-170">INPUTS</span></span>

### <span data-ttu-id="1bf5b-171">System.object</span><span class="sxs-lookup"><span data-stu-id="1bf5b-171">System.String</span></span>

### <span data-ttu-id="1bf5b-172">ComparisonOperationType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="1bf5b-173">MetricStatisticType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="1bf5b-174">Double</span><span class="sxs-lookup"><span data-stu-id="1bf5b-174">System.Double</span></span>

### <span data-ttu-id="1bf5b-175">TimeAggregationType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="1bf5b-176">System.object</span><span class="sxs-lookup"><span data-stu-id="1bf5b-176">System.TimeSpan</span></span>

### <span data-ttu-id="1bf5b-177">ScaleDirection 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="1bf5b-178">ScaleType 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="1bf5b-179">輸出</span><span class="sxs-lookup"><span data-stu-id="1bf5b-179">OUTPUTS</span></span>

### <span data-ttu-id="1bf5b-180">ScaleRule 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1bf5b-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="1bf5b-181">筆記</span><span class="sxs-lookup"><span data-stu-id="1bf5b-181">NOTES</span></span>

## <span data-ttu-id="1bf5b-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bf5b-182">RELATED LINKS</span></span>

[<span data-ttu-id="1bf5b-183">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1bf5b-183">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1bf5b-184">AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="1bf5b-184">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="1bf5b-185">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1bf5b-185">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1bf5b-186">新-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="1bf5b-186">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="1bf5b-187">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1bf5b-187">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


