---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: bb2301fceef993e131472e497e2c89e7ef6ecbf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908910"
---
# <span data-ttu-id="5592f-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="5592f-101">Get-AzMetric</span></span>

## <span data-ttu-id="5592f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5592f-102">SYNOPSIS</span></span>
<span data-ttu-id="5592f-103">獲得資源的公制值。</span><span class="sxs-lookup"><span data-stu-id="5592f-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="5592f-104">語法</span><span class="sxs-lookup"><span data-stu-id="5592f-104">SYNTAX</span></span>

### <span data-ttu-id="5592f-105">GetWithDefaultParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="5592f-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5592f-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="5592f-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5592f-107">描述</span><span class="sxs-lookup"><span data-stu-id="5592f-107">DESCRIPTION</span></span>
<span data-ttu-id="5592f-108">**Get-AzMetric** Cmdlet 會取得指定資源的公制值。</span><span class="sxs-lookup"><span data-stu-id="5592f-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="5592f-109">例子</span><span class="sxs-lookup"><span data-stu-id="5592f-109">EXAMPLES</span></span>

### <span data-ttu-id="5592f-110">範例 1：取得具有摘要輸出的度量</span><span class="sxs-lookup"><span data-stu-id="5592f-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="5592f-111">此命令會以 1 分鐘的時間量獲得網站 3 的公制值。</span><span class="sxs-lookup"><span data-stu-id="5592f-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="5592f-112">範例 2：取得具有詳細輸出的度量</span><span class="sxs-lookup"><span data-stu-id="5592f-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="5592f-113">此命令會以 1 分鐘的時間量獲得網站 3 的公制值。</span><span class="sxs-lookup"><span data-stu-id="5592f-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="5592f-114">輸出為詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5592f-114">The output is detailed.</span></span>

### <span data-ttu-id="5592f-115">範例 3：取得指定公制的詳細輸出</span><span class="sxs-lookup"><span data-stu-id="5592f-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="5592f-116">此命令會獲得要求度量的詳細輸出。</span><span class="sxs-lookup"><span data-stu-id="5592f-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="5592f-117">範例 4：取得具有指定維度篩選之指定度量的摘要輸出</span><span class="sxs-lookup"><span data-stu-id="5592f-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="5592f-118">此命令會針對具有指定維度篩選和匯總類型的 PageViews 度量摘要輸出。</span><span class="sxs-lookup"><span data-stu-id="5592f-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="5592f-119">參數</span><span class="sxs-lookup"><span data-stu-id="5592f-119">PARAMETERS</span></span>

### <span data-ttu-id="5592f-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="5592f-120">-AggregationType</span></span>
<span data-ttu-id="5592f-121">查詢的匯總類型</span><span class="sxs-lookup"><span data-stu-id="5592f-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5592f-122">-DefaultProfile</span></span>
<span data-ttu-id="5592f-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5592f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5592f-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5592f-124">-DetailedOutput</span></span>
<span data-ttu-id="5592f-125">表示此 Cmdlet 會顯示詳細輸出。</span><span class="sxs-lookup"><span data-stu-id="5592f-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="5592f-126">根據預設，輸出會摘要顯示。</span><span class="sxs-lookup"><span data-stu-id="5592f-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5592f-127">-EndTime</span></span>
<span data-ttu-id="5592f-128">指定查詢在本地時間中的結束時間。</span><span class="sxs-lookup"><span data-stu-id="5592f-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="5592f-129">預設值為目前時間。</span><span class="sxs-lookup"><span data-stu-id="5592f-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="5592f-130">-MetricFilter</span></span>
<span data-ttu-id="5592f-131">指定查詢度量的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="5592f-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="5592f-132">-MetricName</span></span>
<span data-ttu-id="5592f-133">指定度量名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="5592f-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="5592f-134">-MetricNamespace</span></span>
<span data-ttu-id="5592f-135">指定查詢計量的公制命名空間。</span><span class="sxs-lookup"><span data-stu-id="5592f-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5592f-136">-OrderBy</span></span>
<span data-ttu-id="5592f-137">指定用於排序結果的匯總，以及排序 (範例：sum asc) 。</span><span class="sxs-lookup"><span data-stu-id="5592f-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5592f-138">-ResourceId</span></span>
<span data-ttu-id="5592f-139">指定計量的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5592f-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="5592f-140">-ResultType</span></span>
<span data-ttu-id="5592f-141">指定要以中繼資料或資料 (的結果) 。</span><span class="sxs-lookup"><span data-stu-id="5592f-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5592f-142">-StartTime</span></span>
<span data-ttu-id="5592f-143">指定查詢在本地時間中的開始時間。</span><span class="sxs-lookup"><span data-stu-id="5592f-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="5592f-144">預設值為目前的當地時間減 1 小時。</span><span class="sxs-lookup"><span data-stu-id="5592f-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="5592f-145">-TimeGrain</span></span>
<span data-ttu-id="5592f-146">以 hh：mm：ss 格式指定公制的時間量做為 **TimeSpan** 物件。</span><span class="sxs-lookup"><span data-stu-id="5592f-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="5592f-147">-頂端</span><span class="sxs-lookup"><span data-stu-id="5592f-147">-Top</span></span>
<span data-ttu-id="5592f-148">指定要以預設 (：10) 來指定要$filter。</span><span class="sxs-lookup"><span data-stu-id="5592f-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5592f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5592f-149">CommonParameters</span></span>
<span data-ttu-id="5592f-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5592f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5592f-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5592f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5592f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="5592f-152">INPUTS</span></span>

### <span data-ttu-id="5592f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5592f-153">System.String</span></span>

### <span data-ttu-id="5592f-154">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="5592f-154">System.TimeSpan</span></span>

### <span data-ttu-id="5592f-155">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5592f-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5592f-156">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="5592f-156">System.DateTime</span></span>

### <span data-ttu-id="5592f-157">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5592f-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5592f-158">System.Nullable'1[[Microsoft.Azure.management.Monitor.models.ResultType，Microsoft.Azure.management.Monitor， Version=0.21.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5592f-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5592f-159">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5592f-159">System.String[]</span></span>

### <span data-ttu-id="5592f-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5592f-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5592f-161">輸出</span><span class="sxs-lookup"><span data-stu-id="5592f-161">OUTPUTS</span></span>

### <span data-ttu-id="5592f-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span><span class="sxs-lookup"><span data-stu-id="5592f-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="5592f-163">筆記</span><span class="sxs-lookup"><span data-stu-id="5592f-163">NOTES</span></span>

<span data-ttu-id="5592f-164">有關支援之計量的資訊，請參閱： https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="5592f-164">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="5592f-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="5592f-165">RELATED LINKS</span></span>

<span data-ttu-id="5592f-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
[New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="5592f-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


