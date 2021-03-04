---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906274"
---
# <span data-ttu-id="96f0a-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="96f0a-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="96f0a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="96f0a-103">匯出記錄，顯示此訂閱在給定時間視窗中提出的 Api 要求，以顯示節流活動。</span><span class="sxs-lookup"><span data-stu-id="96f0a-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="96f0a-104">語法</span><span class="sxs-lookup"><span data-stu-id="96f0a-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f0a-105">描述</span><span class="sxs-lookup"><span data-stu-id="96f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="96f0a-106">在預先定義的時間間隔內，以成功、失敗或節流狀態匯出訂閱呼叫 Microsoft.Compute API 的統計資料。</span><span class="sxs-lookup"><span data-stu-id="96f0a-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="96f0a-107">記錄可以進一步按五個參數分組：GroupByOperationName、GroupByThrottlePolicy、GroupByResourceName、GroupByUserAgent 或 GroupByApplicationId。</span><span class="sxs-lookup"><span data-stu-id="96f0a-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="96f0a-108">請注意，此 Cmdlet 只會收集計算資源提供者記錄;此外，目前還無法提供磁片和快照資源類型的資料。</span><span class="sxs-lookup"><span data-stu-id="96f0a-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="96f0a-109">有關計算資源提供者 API 節流概觀，請參閱 https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits 。</span><span class="sxs-lookup"><span data-stu-id="96f0a-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="96f0a-110">例子</span><span class="sxs-lookup"><span data-stu-id="96f0a-110">EXAMPLES</span></span>

### <span data-ttu-id="96f0a-111">範例 1：匯出根據作業名稱匯總的記錄</span><span class="sxs-lookup"><span data-stu-id="96f0a-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="96f0a-112">此命令會儲存 Microsoft.Compute API 呼叫的匯總數位，在 2018-02-20T17：54：14 和 2018-02-22T17：54：17 之間，以操作名稱匯總。</span><span class="sxs-lookup"><span data-stu-id="96f0a-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="96f0a-113">範例 2：匯出根據應用程式識別碼匯總的記錄</span><span class="sxs-lookup"><span data-stu-id="96f0a-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="96f0a-114">此命令會儲存 Microsoft.Compute API 呼叫的匯總數位，以成功、失敗或節流分隔于 2018-02-20T17：54：14 和 2018-02-22T17：54：17 之間，以應用程式識別碼匯總。</span><span class="sxs-lookup"><span data-stu-id="96f0a-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="96f0a-115">範例 3：匯出使用者代理程式匯總的記錄</span><span class="sxs-lookup"><span data-stu-id="96f0a-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="96f0a-116">此命令會儲存 Microsoft.Compute API 呼叫的匯總數位，以成功、失敗或節流分隔于 2018-02-20T17：54：14 和 2018-02-22T17：54：17 之間，由使用者代理程式匯總。</span><span class="sxs-lookup"><span data-stu-id="96f0a-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="96f0a-117">參數</span><span class="sxs-lookup"><span data-stu-id="96f0a-117">PARAMETERS</span></span>

### <span data-ttu-id="96f0a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96f0a-118">-AsJob</span></span>
<span data-ttu-id="96f0a-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96f0a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96f0a-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="96f0a-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="96f0a-121">LogAnalytics Api 寫入輸出記錄至之記錄 Blob 容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="96f0a-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="96f0a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f0a-122">-DefaultProfile</span></span>
<span data-ttu-id="96f0a-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96f0a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f0a-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="96f0a-124">-FromTime</span></span>
<span data-ttu-id="96f0a-125">從查詢的時間</span><span class="sxs-lookup"><span data-stu-id="96f0a-125">From time of the query</span></span>

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

### <span data-ttu-id="96f0a-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="96f0a-126">-GroupByApplicationId</span></span>
<span data-ttu-id="96f0a-127">按應用程式識別碼分組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="96f0a-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="96f0a-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="96f0a-128">-GroupByOperationName</span></span>
<span data-ttu-id="96f0a-129">按作業名稱分組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="96f0a-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="96f0a-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="96f0a-130">-GroupByResourceName</span></span>
<span data-ttu-id="96f0a-131">按資源名稱分組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="96f0a-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="96f0a-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="96f0a-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="96f0a-133">已使用節流原則的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="96f0a-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="96f0a-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="96f0a-134">-GroupByUserAgent</span></span>
<span data-ttu-id="96f0a-135">UserAgent 的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="96f0a-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="96f0a-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="96f0a-136">-IntervalLength</span></span>
<span data-ttu-id="96f0a-137">用來建立 LogAnalytics 通話費率記錄之間隔值 ，以分鐘為單位。</span><span class="sxs-lookup"><span data-stu-id="96f0a-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="96f0a-138">-位置</span><span class="sxs-lookup"><span data-stu-id="96f0a-138">-Location</span></span>
<span data-ttu-id="96f0a-139">查詢記錄分析的位置。</span><span class="sxs-lookup"><span data-stu-id="96f0a-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="96f0a-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="96f0a-140">-NoWait</span></span>
<span data-ttu-id="96f0a-141">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="96f0a-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="96f0a-142">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="96f0a-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="96f0a-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="96f0a-143">-ToTime</span></span>
<span data-ttu-id="96f0a-144">查詢時間</span><span class="sxs-lookup"><span data-stu-id="96f0a-144">To time of the query</span></span>

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

### <span data-ttu-id="96f0a-145">-確認</span><span class="sxs-lookup"><span data-stu-id="96f0a-145">-Confirm</span></span>
<span data-ttu-id="96f0a-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96f0a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f0a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f0a-147">-WhatIf</span></span>
<span data-ttu-id="96f0a-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96f0a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f0a-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96f0a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f0a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f0a-150">CommonParameters</span></span>
<span data-ttu-id="96f0a-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96f0a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f0a-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96f0a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f0a-153">輸入</span><span class="sxs-lookup"><span data-stu-id="96f0a-153">INPUTS</span></span>

### <span data-ttu-id="96f0a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="96f0a-154">System.String</span></span>

## <span data-ttu-id="96f0a-155">輸出</span><span class="sxs-lookup"><span data-stu-id="96f0a-155">OUTPUTS</span></span>

### <span data-ttu-id="96f0a-156">Microsoft.Azure.Commands.Compute.Automation.models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="96f0a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="96f0a-157">筆記</span><span class="sxs-lookup"><span data-stu-id="96f0a-157">NOTES</span></span>

## <span data-ttu-id="96f0a-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="96f0a-158">RELATED LINKS</span></span>
