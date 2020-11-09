---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 90b467ccd046bf7d08b9faff4c03dcc858ae0076
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286628"
---
# <span data-ttu-id="e52a3-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="e52a3-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="e52a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e52a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e52a3-103">在指定的時間視窗中，會顯示此訂閱所進行的 Api 要求的 [匯出記錄]，以顯示節流活動。</span><span class="sxs-lookup"><span data-stu-id="e52a3-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="e52a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e52a3-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e52a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="e52a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e52a3-106">在預先定義的時間間隔中，將有關訂閱之呼叫的統計資料匯出到 Microsoft. 根據成功、失敗或節流狀態來計算 API。</span><span class="sxs-lookup"><span data-stu-id="e52a3-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="e52a3-107">記錄可進一步由三個參數組成： GroupByOperationName、GroupByThrottlePolicy 或 GroupByResourceName。</span><span class="sxs-lookup"><span data-stu-id="e52a3-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="e52a3-108">請注意，這個 Cmdlet 只會收集計算資源提供者記錄;此外，磁片與快照資源類型的相關資料尚無法使用。</span><span class="sxs-lookup"><span data-stu-id="e52a3-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="e52a3-109">如需計算資源提供者的 API 節流概覽，請參閱 https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits 。</span><span class="sxs-lookup"><span data-stu-id="e52a3-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="e52a3-110">示例</span><span class="sxs-lookup"><span data-stu-id="e52a3-110">EXAMPLES</span></span>

### <span data-ttu-id="e52a3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e52a3-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="e52a3-112">這個命令會儲存 Microsoft 的匯總數：以成功、失敗或在2018之間進行限制的計算 API 呼叫：54：14和 2018-02-22T17：54：17（依作業名稱匯總）。</span><span class="sxs-lookup"><span data-stu-id="e52a3-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="e52a3-113">參數</span><span class="sxs-lookup"><span data-stu-id="e52a3-113">PARAMETERS</span></span>

### <span data-ttu-id="e52a3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e52a3-114">-AsJob</span></span>
<span data-ttu-id="e52a3-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e52a3-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="e52a3-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="e52a3-117">LogAnalytics Api 將輸出記錄寫入到其中的記錄 blob 容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="e52a3-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52a3-118">-DefaultProfile</span></span>
<span data-ttu-id="e52a3-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e52a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e52a3-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="e52a3-120">-FromTime</span></span>
<span data-ttu-id="e52a3-121">查詢的開始時間</span><span class="sxs-lookup"><span data-stu-id="e52a3-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="e52a3-122">-GroupByOperationName</span></span>
<span data-ttu-id="e52a3-123">依作業名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="e52a3-123">Group query result by Operation Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="e52a3-124">-GroupByResourceName</span></span>
<span data-ttu-id="e52a3-125">依資源名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="e52a3-125">Group query result by Resource Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="e52a3-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="e52a3-127">已套用節流原則的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="e52a3-127">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="e52a3-128">-IntervalLength</span></span>
<span data-ttu-id="e52a3-129">用於建立 LogAnalytics 通話率記錄的間隔時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="e52a3-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="e52a3-130">-Location</span></span>
<span data-ttu-id="e52a3-131">查詢記錄分析的位置。</span><span class="sxs-lookup"><span data-stu-id="e52a3-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="e52a3-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e52a3-132">-NoWait</span></span>
<span data-ttu-id="e52a3-133">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="e52a3-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e52a3-134">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="e52a3-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="e52a3-135">-ToTime</span></span>
<span data-ttu-id="e52a3-136">查詢的 [到] 時間</span><span class="sxs-lookup"><span data-stu-id="e52a3-136">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e52a3-137">-Confirm</span></span>
<span data-ttu-id="e52a3-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e52a3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e52a3-139">-WhatIf</span></span>
<span data-ttu-id="e52a3-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e52a3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e52a3-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e52a3-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52a3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52a3-142">CommonParameters</span></span>
<span data-ttu-id="e52a3-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e52a3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52a3-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e52a3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52a3-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e52a3-145">INPUTS</span></span>

### <span data-ttu-id="e52a3-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e52a3-146">System.String</span></span>

## <span data-ttu-id="e52a3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e52a3-147">OUTPUTS</span></span>

### <span data-ttu-id="e52a3-148">PSLogAnalyticsOperationResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e52a3-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="e52a3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e52a3-149">NOTES</span></span>

## <span data-ttu-id="e52a3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e52a3-150">RELATED LINKS</span></span>
