---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
ms.openlocfilehash: 4e55da6a5f0fbacab9b7af834c2729a2f79c1995
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800581"
---
# <span data-ttu-id="94da6-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="94da6-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="94da6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94da6-102">SYNOPSIS</span></span>
<span data-ttu-id="94da6-103">在指定的時間視窗中，會顯示此訂閱所進行的 Api 要求的 [匯出記錄]，以顯示節流活動。</span><span class="sxs-lookup"><span data-stu-id="94da6-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94da6-104">句法</span><span class="sxs-lookup"><span data-stu-id="94da6-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94da6-105">說明</span><span class="sxs-lookup"><span data-stu-id="94da6-105">DESCRIPTION</span></span>
<span data-ttu-id="94da6-106">這會匯出 Microsoft 的匯總數。以 [成功]、[失敗] 或 [依時間間隔] 顯示的計算 API 呼叫來分隔。</span><span class="sxs-lookup"><span data-stu-id="94da6-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="94da6-107">記錄可進一步由三個參數組成： GroupByOperationName、GroupByThrottlePolicy 或 GroupByResourceName。</span><span class="sxs-lookup"><span data-stu-id="94da6-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="94da6-108">請注意，這個 Cmdlet 只會收集 CRP 記錄。</span><span class="sxs-lookup"><span data-stu-id="94da6-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="94da6-109">示例</span><span class="sxs-lookup"><span data-stu-id="94da6-109">EXAMPLES</span></span>

### <span data-ttu-id="94da6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="94da6-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="94da6-111">這個命令會儲存 Microsoft 的匯總數：以成功、失敗或在2018之間進行限制的計算 API 呼叫：54：14和 2018-02-22T17：54：17（依作業名稱匯總）。</span><span class="sxs-lookup"><span data-stu-id="94da6-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="94da6-112">參數</span><span class="sxs-lookup"><span data-stu-id="94da6-112">PARAMETERS</span></span>

### <span data-ttu-id="94da6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94da6-113">-AsJob</span></span>
<span data-ttu-id="94da6-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94da6-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="94da6-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="94da6-116">LogAnalytics Api 將輸出記錄寫入到其中的記錄 blob 容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="94da6-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94da6-117">-DefaultProfile</span></span>
<span data-ttu-id="94da6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94da6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94da6-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="94da6-119">-FromTime</span></span>
<span data-ttu-id="94da6-120">查詢的開始時間</span><span class="sxs-lookup"><span data-stu-id="94da6-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="94da6-121">-GroupByOperationName</span></span>
<span data-ttu-id="94da6-122">依作業名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="94da6-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="94da6-123">-GroupByResourceName</span></span>
<span data-ttu-id="94da6-124">依資源名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="94da6-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="94da6-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="94da6-126">已套用節流原則的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="94da6-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="94da6-127">-IntervalLength</span></span>
<span data-ttu-id="94da6-128">用於建立 LogAnalytics 通話率記錄的間隔時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="94da6-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-129">-位置</span><span class="sxs-lookup"><span data-stu-id="94da6-129">-Location</span></span>
<span data-ttu-id="94da6-130">查詢記錄分析的位置。</span><span class="sxs-lookup"><span data-stu-id="94da6-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="94da6-131">-ToTime</span></span>
<span data-ttu-id="94da6-132">查詢的 [到] 時間</span><span class="sxs-lookup"><span data-stu-id="94da6-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-133">-確認</span><span class="sxs-lookup"><span data-stu-id="94da6-133">-Confirm</span></span>
<span data-ttu-id="94da6-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94da6-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94da6-135">-WhatIf</span></span>
<span data-ttu-id="94da6-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94da6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94da6-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94da6-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94da6-138">CommonParameters</span></span>
<span data-ttu-id="94da6-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94da6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94da6-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94da6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94da6-141">輸入</span><span class="sxs-lookup"><span data-stu-id="94da6-141">INPUTS</span></span>

### <span data-ttu-id="94da6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="94da6-142">System.String</span></span>

## <span data-ttu-id="94da6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="94da6-143">OUTPUTS</span></span>

### <span data-ttu-id="94da6-144">PSLogAnalyticsOperationResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="94da6-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="94da6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="94da6-145">NOTES</span></span>

## <span data-ttu-id="94da6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="94da6-146">RELATED LINKS</span></span>

