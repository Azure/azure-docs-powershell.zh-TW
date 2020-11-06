---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 8889a0957dec645b987e97012948c18f0527bc92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448417"
---
# <span data-ttu-id="44ceb-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="44ceb-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="44ceb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="44ceb-103">取得資源的度量值。</span><span class="sxs-lookup"><span data-stu-id="44ceb-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44ceb-104">句法</span><span class="sxs-lookup"><span data-stu-id="44ceb-104">SYNTAX</span></span>

### <span data-ttu-id="44ceb-105">GetWithDefaultParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="44ceb-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ceb-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="44ceb-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ceb-107">說明</span><span class="sxs-lookup"><span data-stu-id="44ceb-107">DESCRIPTION</span></span>
<span data-ttu-id="44ceb-108">**AzureRmMetric** Cmdlet 會取得指定資源的規格值。</span><span class="sxs-lookup"><span data-stu-id="44ceb-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="44ceb-109">示例</span><span class="sxs-lookup"><span data-stu-id="44ceb-109">EXAMPLES</span></span>

### <span data-ttu-id="44ceb-110">範例1：使用摘要輸出取得量度</span><span class="sxs-lookup"><span data-stu-id="44ceb-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="44ceb-111">這個命令會取得含1分鐘時間細微性之 website3 的公制值。</span><span class="sxs-lookup"><span data-stu-id="44ceb-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="44ceb-112">範例2：取得詳細輸出的規格</span><span class="sxs-lookup"><span data-stu-id="44ceb-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="44ceb-113">這個命令會取得含1分鐘時間細微性之 website3 的公制值。</span><span class="sxs-lookup"><span data-stu-id="44ceb-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="44ceb-114">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="44ceb-114">The output is detailed.</span></span>

### <span data-ttu-id="44ceb-115">範例3：取得指定指標的詳細輸出</span><span class="sxs-lookup"><span data-stu-id="44ceb-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricNames "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="44ceb-116">這個命令會針對要求規格取得詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="44ceb-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="44ceb-117">範例4：使用指定的維度篩選取得指定指標的摘要輸出</span><span class="sxs-lookup"><span data-stu-id="44ceb-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzureRmMetricFilter -Dimension City -Operator eq -Values "Seattle","Toronto"), (New-AzureRmMetricDimensionFilter -Dimension AuthenticationType -Operator eq -Values User))

PS C:\> Get-AzureRmMetricValues -ResourceId <resourcId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
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

<span data-ttu-id="44ceb-118">這個命令會以指定的 dimesion 篩選和匯總類型，取得 PageViews 規格的摘要輸出。</span><span class="sxs-lookup"><span data-stu-id="44ceb-118">This command gets summarized output for the PageViews metric with specified dimesion filter and aggregation type.</span></span>

## <span data-ttu-id="44ceb-119">參數</span><span class="sxs-lookup"><span data-stu-id="44ceb-119">PARAMETERS</span></span>

### <span data-ttu-id="44ceb-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="44ceb-120">-AggregationType</span></span>
<span data-ttu-id="44ceb-121">查詢的聚合類型</span><span class="sxs-lookup"><span data-stu-id="44ceb-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="44ceb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ceb-122">-DefaultProfile</span></span>
<span data-ttu-id="44ceb-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="44ceb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44ceb-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="44ceb-124">-DetailedOutput</span></span>
<span data-ttu-id="44ceb-125">表示此 Cmdlet 會顯示詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="44ceb-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="44ceb-126">根據預設，輸出是匯總的。</span><span class="sxs-lookup"><span data-stu-id="44ceb-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="44ceb-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="44ceb-127">-EndTime</span></span>
<span data-ttu-id="44ceb-128">指定當地時間的查詢結束時間。</span><span class="sxs-lookup"><span data-stu-id="44ceb-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="44ceb-129">預設為目前時間。</span><span class="sxs-lookup"><span data-stu-id="44ceb-129">The default is the current time.</span></span>

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

### <span data-ttu-id="44ceb-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="44ceb-130">-MetricFilter</span></span>
<span data-ttu-id="44ceb-131">指定要查詢指標的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="44ceb-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="44ceb-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="44ceb-132">-MetricName</span></span>
<span data-ttu-id="44ceb-133">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="44ceb-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="44ceb-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="44ceb-134">-MetricNamespace</span></span>
<span data-ttu-id="44ceb-135">指定要為其查詢指標的度量命名空間。</span><span class="sxs-lookup"><span data-stu-id="44ceb-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="44ceb-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="44ceb-136">-OrderBy</span></span>
<span data-ttu-id="44ceb-137">指定要用於排序結果的匯總，以及排序 (範例的方向： sum asc) 。</span><span class="sxs-lookup"><span data-stu-id="44ceb-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="44ceb-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44ceb-138">-ResourceId</span></span>
<span data-ttu-id="44ceb-139">指定度量的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="44ceb-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="44ceb-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="44ceb-140">-ResultType</span></span>
<span data-ttu-id="44ceb-141">指定要傳回 (中繼資料或資料) 的結果類型。</span><span class="sxs-lookup"><span data-stu-id="44ceb-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="44ceb-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="44ceb-142">-StartTime</span></span>
<span data-ttu-id="44ceb-143">指定當地時間查詢的開始時間。</span><span class="sxs-lookup"><span data-stu-id="44ceb-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="44ceb-144">預設為目前的當地時間減去1小時。</span><span class="sxs-lookup"><span data-stu-id="44ceb-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="44ceb-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="44ceb-145">-TimeGrain</span></span>
<span data-ttu-id="44ceb-146">以 hh： mm： ss 格式指定公制的時間細微性，以 Timespan.zero 物件為 **TimeSpan** 。</span><span class="sxs-lookup"><span data-stu-id="44ceb-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="44ceb-147">-上方</span><span class="sxs-lookup"><span data-stu-id="44ceb-147">-Top</span></span>
<span data-ttu-id="44ceb-148">指定 (預設： 10) 中要檢索的記錄數目上限，以 $filter 加以指定。</span><span class="sxs-lookup"><span data-stu-id="44ceb-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="44ceb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ceb-149">CommonParameters</span></span>
<span data-ttu-id="44ceb-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44ceb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ceb-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="44ceb-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ceb-152">輸入</span><span class="sxs-lookup"><span data-stu-id="44ceb-152">INPUTS</span></span>

### <span data-ttu-id="44ceb-153">System.object</span><span class="sxs-lookup"><span data-stu-id="44ceb-153">System.String</span></span>

### <span data-ttu-id="44ceb-154">System.object</span><span class="sxs-lookup"><span data-stu-id="44ceb-154">System.TimeSpan</span></span>

### <span data-ttu-id="44ceb-155">可為 Null 的 ' 1 [AggregationType、0.19.1.0、31bf3856ad364e35、Version =、Culture = 中性、PublicKeyToken =」]」。</span><span class="sxs-lookup"><span data-stu-id="44ceb-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="44ceb-156">System.object</span><span class="sxs-lookup"><span data-stu-id="44ceb-156">System.DateTime</span></span>

### <span data-ttu-id="44ceb-157">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="44ceb-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="44ceb-158">"0.19.1.0" 1 [[31bf3856ad364e35]。監視器，版本 =，Culture = 中性，PublicKeyToken = "]] （"）]</span><span class="sxs-lookup"><span data-stu-id="44ceb-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="44ceb-159">System.object []</span><span class="sxs-lookup"><span data-stu-id="44ceb-159">System.String[]</span></span>

### <span data-ttu-id="44ceb-160">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="44ceb-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="44ceb-161">輸出</span><span class="sxs-lookup"><span data-stu-id="44ceb-161">OUTPUTS</span></span>

### <span data-ttu-id="44ceb-162">PSMetric 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="44ceb-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="44ceb-163">筆記</span><span class="sxs-lookup"><span data-stu-id="44ceb-163">NOTES</span></span>

## <span data-ttu-id="44ceb-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="44ceb-164">RELATED LINKS</span></span>

<span data-ttu-id="44ceb-165">[AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md) 
[新-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="44ceb-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


