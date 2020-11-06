---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455796"
---
# <span data-ttu-id="44bca-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="44bca-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="44bca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44bca-102">SYNOPSIS</span></span>
<span data-ttu-id="44bca-103">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="44bca-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44bca-104">句法</span><span class="sxs-lookup"><span data-stu-id="44bca-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44bca-105">說明</span><span class="sxs-lookup"><span data-stu-id="44bca-105">DESCRIPTION</span></span>
<span data-ttu-id="44bca-106">**新的-AzureRmAutoscaleRule** Cmdlet 會建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="44bca-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="44bca-107">示例</span><span class="sxs-lookup"><span data-stu-id="44bca-107">EXAMPLES</span></span>

### <span data-ttu-id="44bca-108">範例1：建立規則</span><span class="sxs-lookup"><span data-stu-id="44bca-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="44bca-109">這個命令會建立規則。</span><span class="sxs-lookup"><span data-stu-id="44bca-109">This command creates a rule.</span></span>

### <span data-ttu-id="44bca-110">範例2：建立兩個規則</span><span class="sxs-lookup"><span data-stu-id="44bca-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="44bca-111">第一個命令會針對要求公制建立規則，然後將它儲存在 $Rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="44bca-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="44bca-112">第二個命令會針對要求公制建立第二個規則，然後將它儲存在 $Rule 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="44bca-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="44bca-113">參數</span><span class="sxs-lookup"><span data-stu-id="44bca-113">PARAMETERS</span></span>

### <span data-ttu-id="44bca-114">-MetricName</span><span class="sxs-lookup"><span data-stu-id="44bca-114">-MetricName</span></span>
<span data-ttu-id="44bca-115">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="44bca-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="44bca-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="44bca-116">-MetricResourceId</span></span>
<span data-ttu-id="44bca-117">指定公制資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="44bca-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="44bca-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="44bca-118">-MetricStatistic</span></span>
<span data-ttu-id="44bca-119">指定度量統計值。</span><span class="sxs-lookup"><span data-stu-id="44bca-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="44bca-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="44bca-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44bca-121">而言</span><span class="sxs-lookup"><span data-stu-id="44bca-121">Average</span></span>
- <span data-ttu-id="44bca-122">Dtu</span><span class="sxs-lookup"><span data-stu-id="44bca-122">Min</span></span>
- <span data-ttu-id="44bca-123">大會</span><span class="sxs-lookup"><span data-stu-id="44bca-123">Max</span></span>
- <span data-ttu-id="44bca-124">總計</span><span class="sxs-lookup"><span data-stu-id="44bca-124">Sum</span></span>

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

### <span data-ttu-id="44bca-125">-運算子</span><span class="sxs-lookup"><span data-stu-id="44bca-125">-Operator</span></span>
<span data-ttu-id="44bca-126">指定運算子。</span><span class="sxs-lookup"><span data-stu-id="44bca-126">Specifies the operator.</span></span>
<span data-ttu-id="44bca-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="44bca-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44bca-128">等於</span><span class="sxs-lookup"><span data-stu-id="44bca-128">Equals</span></span>
- <span data-ttu-id="44bca-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="44bca-129">NotEquals</span></span>
- <span data-ttu-id="44bca-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="44bca-130">GreaterThan</span></span>
- <span data-ttu-id="44bca-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="44bca-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="44bca-132">小於</span><span class="sxs-lookup"><span data-stu-id="44bca-132">LessThan</span></span>
- <span data-ttu-id="44bca-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="44bca-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="44bca-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="44bca-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="44bca-135">指定自動縮放動作 cooldown 時間。</span><span class="sxs-lookup"><span data-stu-id="44bca-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="44bca-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="44bca-136">-ScaleActionDirection</span></span>
<span data-ttu-id="44bca-137">指定縮放動作方向。</span><span class="sxs-lookup"><span data-stu-id="44bca-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="44bca-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="44bca-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44bca-139">所有</span><span class="sxs-lookup"><span data-stu-id="44bca-139">None</span></span>
- <span data-ttu-id="44bca-140">遞增</span><span class="sxs-lookup"><span data-stu-id="44bca-140">Increase</span></span>
- <span data-ttu-id="44bca-141">縮減</span><span class="sxs-lookup"><span data-stu-id="44bca-141">Decrease</span></span>

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

### <span data-ttu-id="44bca-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="44bca-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="44bca-143">指定縮放類型。</span><span class="sxs-lookup"><span data-stu-id="44bca-143">Specifies the scale type.</span></span>
<span data-ttu-id="44bca-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="44bca-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44bca-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="44bca-145">ChangeSize</span></span>
- <span data-ttu-id="44bca-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="44bca-146">ChangeCount</span></span>
- <span data-ttu-id="44bca-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="44bca-147">PercentChangeCount</span></span>
- <span data-ttu-id="44bca-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="44bca-148">ExactCount</span></span>

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

### <span data-ttu-id="44bca-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="44bca-149">-ScaleActionValue</span></span>
<span data-ttu-id="44bca-150">指定 [動作] 值。</span><span class="sxs-lookup"><span data-stu-id="44bca-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="44bca-151">-閾值</span><span class="sxs-lookup"><span data-stu-id="44bca-151">-Threshold</span></span>
<span data-ttu-id="44bca-152">指定公制值的閾值。</span><span class="sxs-lookup"><span data-stu-id="44bca-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="44bca-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="44bca-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="44bca-154">指定時間匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="44bca-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="44bca-155">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="44bca-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44bca-156">而言</span><span class="sxs-lookup"><span data-stu-id="44bca-156">Average</span></span>
- <span data-ttu-id="44bca-157">基本</span><span class="sxs-lookup"><span data-stu-id="44bca-157">Minimum</span></span>
- <span data-ttu-id="44bca-158">大化</span><span class="sxs-lookup"><span data-stu-id="44bca-158">Maximum</span></span>
- <span data-ttu-id="44bca-159">年</span><span class="sxs-lookup"><span data-stu-id="44bca-159">Last</span></span>
- <span data-ttu-id="44bca-160">總計、計數</span><span class="sxs-lookup"><span data-stu-id="44bca-160">Total, Count</span></span>

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

### <span data-ttu-id="44bca-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="44bca-161">-TimeGrain</span></span>
<span data-ttu-id="44bca-162">指定時間細微性。</span><span class="sxs-lookup"><span data-stu-id="44bca-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="44bca-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="44bca-163">-TimeWindow</span></span>
<span data-ttu-id="44bca-164">指定時間範圍。</span><span class="sxs-lookup"><span data-stu-id="44bca-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="44bca-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bca-165">-DefaultProfile</span></span>
<span data-ttu-id="44bca-166">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="44bca-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44bca-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bca-167">CommonParameters</span></span>
<span data-ttu-id="44bca-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44bca-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bca-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="44bca-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bca-170">輸入</span><span class="sxs-lookup"><span data-stu-id="44bca-170">INPUTS</span></span>

## <span data-ttu-id="44bca-171">輸出</span><span class="sxs-lookup"><span data-stu-id="44bca-171">OUTPUTS</span></span>

### <span data-ttu-id="44bca-172">ScaleRule 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="44bca-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="44bca-173">筆記</span><span class="sxs-lookup"><span data-stu-id="44bca-173">NOTES</span></span>

## <span data-ttu-id="44bca-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="44bca-174">RELATED LINKS</span></span>

[<span data-ttu-id="44bca-175">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="44bca-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="44bca-176">AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="44bca-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="44bca-177">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="44bca-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="44bca-178">新-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="44bca-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="44bca-179">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="44bca-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


