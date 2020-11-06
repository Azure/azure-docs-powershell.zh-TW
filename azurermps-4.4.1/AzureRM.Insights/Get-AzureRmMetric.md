---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453508"
---
# <span data-ttu-id="0cf0d-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="0cf0d-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="0cf0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf0d-103">取得資源的度量值。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cf0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cf0d-104">SYNTAX</span></span>

### <span data-ttu-id="0cf0d-105">預設模式中 Get-AzureRmMetric Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="0cf0d-105">Parameters for Get-AzureRmMetric cmdlet in the default mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf0d-106">完整參數集模式中 Get-AzureRmMetric Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="0cf0d-106">Parameters for Get-AzureRmMetric cmdlet in the full param set mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf0d-107">說明</span><span class="sxs-lookup"><span data-stu-id="0cf0d-107">DESCRIPTION</span></span>
<span data-ttu-id="0cf0d-108">**AzureRmMetric** Cmdlet 會取得指定資源的規格值。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="0cf0d-109">示例</span><span class="sxs-lookup"><span data-stu-id="0cf0d-109">EXAMPLES</span></span>

### <span data-ttu-id="0cf0d-110">範例1：使用摘要輸出取得量度</span><span class="sxs-lookup"><span data-stu-id="0cf0d-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="0cf0d-111">這個命令會取得含1分鐘時間細微性之 website3 的公制值。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="0cf0d-112">範例2：取得詳細輸出的規格</span><span class="sxs-lookup"><span data-stu-id="0cf0d-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="0cf0d-113">這個命令會取得含1分鐘時間細微性之 website3 的公制值。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="0cf0d-114">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-114">The output is detailed.</span></span>

### <span data-ttu-id="0cf0d-115">範例3：取得指定指標的詳細輸出</span><span class="sxs-lookup"><span data-stu-id="0cf0d-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="0cf0d-116">這個命令會針對要求規格取得詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="0cf0d-117">參數</span><span class="sxs-lookup"><span data-stu-id="0cf0d-117">PARAMETERS</span></span>

### <span data-ttu-id="0cf0d-118">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="0cf0d-118">-DetailedOutput</span></span>
<span data-ttu-id="0cf0d-119">表示此 Cmdlet 會顯示詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-119">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="0cf0d-120">根據預設，輸出是匯總的。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-120">By default, output is summarized.</span></span>

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

### <span data-ttu-id="0cf0d-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0cf0d-121">-EndTime</span></span>
<span data-ttu-id="0cf0d-122">指定當地時間的查詢結束時間。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-122">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="0cf0d-123">預設為目前時間。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-123">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-124">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="0cf0d-124">-MetricNames</span></span>
<span data-ttu-id="0cf0d-125">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-125">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf0d-126">-ResourceId</span></span>
<span data-ttu-id="0cf0d-127">指定度量的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-127">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="0cf0d-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0cf0d-128">-StartTime</span></span>
<span data-ttu-id="0cf0d-129">指定當地時間查詢的開始時間。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-129">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="0cf0d-130">預設為目前的當地時間減去1小時。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-130">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-131">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="0cf0d-131">-TimeGrain</span></span>
<span data-ttu-id="0cf0d-132">以 hh： mm： ss 格式指定公制的時間細微性，以 Timespan.zero 物件為 **TimeSpan** 。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-132">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-133">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="0cf0d-133">-AggregationType</span></span>
<span data-ttu-id="0cf0d-134">Quer 的聚合類型</span><span class="sxs-lookup"><span data-stu-id="0cf0d-134">The aggregation type of the quer</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf0d-135">-DefaultProfile</span></span>
<span data-ttu-id="0cf0d-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf0d-137">CommonParameters</span></span>
<span data-ttu-id="0cf0d-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf0d-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0cf0d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf0d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0cf0d-140">INPUTS</span></span>

## <span data-ttu-id="0cf0d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0cf0d-141">OUTPUTS</span></span>

### <span data-ttu-id="0cf0d-142">PSMetric [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="0cf0d-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="0cf0d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0cf0d-143">NOTES</span></span>

## <span data-ttu-id="0cf0d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cf0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="0cf0d-145">AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="0cf0d-145">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


