---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624723"
---
# <span data-ttu-id="aacb5-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="aacb5-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="aacb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aacb5-102">SYNOPSIS</span></span>
<span data-ttu-id="aacb5-103">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="aacb5-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aacb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="aacb5-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aacb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="aacb5-105">DESCRIPTION</span></span>
<span data-ttu-id="aacb5-106">**新的-AzureRmAutoscaleRule** Cmdlet 會建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="aacb5-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="aacb5-107">示例</span><span class="sxs-lookup"><span data-stu-id="aacb5-107">EXAMPLES</span></span>

### <span data-ttu-id="aacb5-108">範例1：建立規則</span><span class="sxs-lookup"><span data-stu-id="aacb5-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="aacb5-109">這個命令會建立規則。</span><span class="sxs-lookup"><span data-stu-id="aacb5-109">This command creates a rule.</span></span>

### <span data-ttu-id="aacb5-110">範例2：建立兩個規則</span><span class="sxs-lookup"><span data-stu-id="aacb5-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="aacb5-111">第一個命令會針對要求公制建立規則，然後將它儲存在 $Rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="aacb5-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="aacb5-112">第二個命令會針對要求公制建立第二個規則，然後將它儲存在 $Rule 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="aacb5-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="aacb5-113">參數</span><span class="sxs-lookup"><span data-stu-id="aacb5-113">PARAMETERS</span></span>

### <span data-ttu-id="aacb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacb5-114">-DefaultProfile</span></span>
<span data-ttu-id="aacb5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aacb5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="aacb5-116">-MetricName</span></span>
<span data-ttu-id="aacb5-117">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacb5-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="aacb5-118">-MetricResourceId</span></span>
<span data-ttu-id="aacb5-119">指定公制資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aacb5-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="aacb5-120">-MetricStatistic</span></span>
<span data-ttu-id="aacb5-121">指定度量統計值。</span><span class="sxs-lookup"><span data-stu-id="aacb5-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="aacb5-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aacb5-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aacb5-123">而言</span><span class="sxs-lookup"><span data-stu-id="aacb5-123">Average</span></span>
- <span data-ttu-id="aacb5-124">Dtu</span><span class="sxs-lookup"><span data-stu-id="aacb5-124">Min</span></span>
- <span data-ttu-id="aacb5-125">大會</span><span class="sxs-lookup"><span data-stu-id="aacb5-125">Max</span></span>
- <span data-ttu-id="aacb5-126">總計</span><span class="sxs-lookup"><span data-stu-id="aacb5-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-127">-運算子</span><span class="sxs-lookup"><span data-stu-id="aacb5-127">-Operator</span></span>
<span data-ttu-id="aacb5-128">指定運算子。</span><span class="sxs-lookup"><span data-stu-id="aacb5-128">Specifies the operator.</span></span>
<span data-ttu-id="aacb5-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aacb5-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aacb5-130">等於</span><span class="sxs-lookup"><span data-stu-id="aacb5-130">Equals</span></span>
- <span data-ttu-id="aacb5-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="aacb5-131">NotEquals</span></span>
- <span data-ttu-id="aacb5-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="aacb5-132">GreaterThan</span></span>
- <span data-ttu-id="aacb5-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="aacb5-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="aacb5-134">小於</span><span class="sxs-lookup"><span data-stu-id="aacb5-134">LessThan</span></span>
- <span data-ttu-id="aacb5-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="aacb5-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="aacb5-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="aacb5-137">指定自動縮放動作 cooldown 時間。</span><span class="sxs-lookup"><span data-stu-id="aacb5-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="aacb5-138">-ScaleActionDirection</span></span>
<span data-ttu-id="aacb5-139">指定縮放動作方向。</span><span class="sxs-lookup"><span data-stu-id="aacb5-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="aacb5-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aacb5-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aacb5-141">所有</span><span class="sxs-lookup"><span data-stu-id="aacb5-141">None</span></span>
- <span data-ttu-id="aacb5-142">遞增</span><span class="sxs-lookup"><span data-stu-id="aacb5-142">Increase</span></span>
- <span data-ttu-id="aacb5-143">縮減</span><span class="sxs-lookup"><span data-stu-id="aacb5-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="aacb5-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="aacb5-145">指定縮放類型。</span><span class="sxs-lookup"><span data-stu-id="aacb5-145">Specifies the scale type.</span></span>
<span data-ttu-id="aacb5-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aacb5-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aacb5-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="aacb5-147">ChangeSize</span></span>
- <span data-ttu-id="aacb5-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="aacb5-148">ChangeCount</span></span>
- <span data-ttu-id="aacb5-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="aacb5-149">PercentChangeCount</span></span>
- <span data-ttu-id="aacb5-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="aacb5-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="aacb5-151">-ScaleActionValue</span></span>
<span data-ttu-id="aacb5-152">指定 [動作] 值。</span><span class="sxs-lookup"><span data-stu-id="aacb5-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-153">-閾值</span><span class="sxs-lookup"><span data-stu-id="aacb5-153">-Threshold</span></span>
<span data-ttu-id="aacb5-154">指定公制值的閾值。</span><span class="sxs-lookup"><span data-stu-id="aacb5-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="aacb5-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="aacb5-156">指定時間匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="aacb5-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="aacb5-157">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aacb5-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aacb5-158">而言</span><span class="sxs-lookup"><span data-stu-id="aacb5-158">Average</span></span>
- <span data-ttu-id="aacb5-159">基本</span><span class="sxs-lookup"><span data-stu-id="aacb5-159">Minimum</span></span>
- <span data-ttu-id="aacb5-160">大化</span><span class="sxs-lookup"><span data-stu-id="aacb5-160">Maximum</span></span>
- <span data-ttu-id="aacb5-161">年</span><span class="sxs-lookup"><span data-stu-id="aacb5-161">Last</span></span>
- <span data-ttu-id="aacb5-162">總計、計數</span><span class="sxs-lookup"><span data-stu-id="aacb5-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="aacb5-163">-TimeGrain</span></span>
<span data-ttu-id="aacb5-164">指定時間細微性。</span><span class="sxs-lookup"><span data-stu-id="aacb5-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="aacb5-165">-TimeWindow</span></span>
<span data-ttu-id="aacb5-166">指定時間範圍。</span><span class="sxs-lookup"><span data-stu-id="aacb5-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacb5-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacb5-167">CommonParameters</span></span>
<span data-ttu-id="aacb5-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aacb5-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacb5-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aacb5-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacb5-170">輸入</span><span class="sxs-lookup"><span data-stu-id="aacb5-170">INPUTS</span></span>

### <span data-ttu-id="aacb5-171">所有</span><span class="sxs-lookup"><span data-stu-id="aacb5-171">None</span></span>
<span data-ttu-id="aacb5-172">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="aacb5-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aacb5-173">輸出</span><span class="sxs-lookup"><span data-stu-id="aacb5-173">OUTPUTS</span></span>

### <span data-ttu-id="aacb5-174">ScaleRule 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="aacb5-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="aacb5-175">筆記</span><span class="sxs-lookup"><span data-stu-id="aacb5-175">NOTES</span></span>

## <span data-ttu-id="aacb5-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="aacb5-176">RELATED LINKS</span></span>

[<span data-ttu-id="aacb5-177">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="aacb5-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="aacb5-178">AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="aacb5-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="aacb5-179">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="aacb5-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="aacb5-180">新-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="aacb5-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="aacb5-181">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="aacb5-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


