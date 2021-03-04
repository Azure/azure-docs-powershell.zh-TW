---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 02d78a36bcd2afc6eef037a0b043c5db89d37f0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906273"
---
# <span data-ttu-id="c0af7-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="c0af7-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="c0af7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0af7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0af7-103">匯出記錄，在給定時間視窗中顯示此訂閱的節流 Api 總要求。</span><span class="sxs-lookup"><span data-stu-id="c0af7-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="c0af7-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0af7-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0af7-105">描述</span><span class="sxs-lookup"><span data-stu-id="c0af7-105">DESCRIPTION</span></span>
<span data-ttu-id="c0af7-106">這會匯出節流 Microsoft.Compute API 呼叫的總數。</span><span class="sxs-lookup"><span data-stu-id="c0af7-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="c0af7-107">記錄可以五個選項進一步匯總：GroupByOperationName、GroupByThrottlePolicy、GroupByResourceName、GroupByUserAgent 或 GroupByApplicationId。</span><span class="sxs-lookup"><span data-stu-id="c0af7-107">The logs can be further aggregated by five options: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="c0af7-108">請注意，此 Cmdlet 只會收集 CRP 記錄。</span><span class="sxs-lookup"><span data-stu-id="c0af7-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="c0af7-109">有關計算資源提供者 API 節流概觀，請參閱 https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits 。</span><span class="sxs-lookup"><span data-stu-id="c0af7-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="c0af7-110">例子</span><span class="sxs-lookup"><span data-stu-id="c0af7-110">EXAMPLES</span></span>

### <span data-ttu-id="c0af7-111">範例 1：匯出根據作業名稱匯總的記錄</span><span class="sxs-lookup"><span data-stu-id="c0af7-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="c0af7-112">此命令將 2018-02-20T17：54：14 和 2018-02-22T17：54：17：54：17 之間的總節流 Microsoft.Compute API 呼叫儲存在指定 SAS URI 中，並按作業名稱匯總。</span><span class="sxs-lookup"><span data-stu-id="c0af7-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="c0af7-113">範例 2：匯出根據應用程式識別碼匯總的記錄</span><span class="sxs-lookup"><span data-stu-id="c0af7-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="c0af7-114">此命令將 2018-02-20T17：54：14 與 2018-02-22T17：54：17 之間受節流 Microsoft.Compute API 呼叫的總時間儲存于所給的 SAS URI 中，並按應用程式識別碼匯總。</span><span class="sxs-lookup"><span data-stu-id="c0af7-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="c0af7-115">範例 3：匯出使用者代理程式匯總的記錄</span><span class="sxs-lookup"><span data-stu-id="c0af7-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="c0af7-116">此命令將 2018-02-20T17：54：14 和 2018-02-22T17：54：17 之間受節流 Microsoft.Compute API 呼叫的總時間儲存于由使用者代理程式匯總的 MICROSOFT.Compute API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c0af7-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="c0af7-117">參數</span><span class="sxs-lookup"><span data-stu-id="c0af7-117">PARAMETERS</span></span>

### <span data-ttu-id="c0af7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0af7-118">-AsJob</span></span>
<span data-ttu-id="c0af7-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0af7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0af7-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c0af7-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="c0af7-121">LogAnalytics Api 寫入輸出記錄至之記錄 Blob 容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="c0af7-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="c0af7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0af7-122">-DefaultProfile</span></span>
<span data-ttu-id="c0af7-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0af7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0af7-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="c0af7-124">-FromTime</span></span>
<span data-ttu-id="c0af7-125">從查詢的時間</span><span class="sxs-lookup"><span data-stu-id="c0af7-125">From time of the query</span></span>

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

### <span data-ttu-id="c0af7-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="c0af7-126">-GroupByApplicationId</span></span>
<span data-ttu-id="c0af7-127">按應用程式識別碼分組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="c0af7-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="c0af7-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="c0af7-128">-GroupByOperationName</span></span>
<span data-ttu-id="c0af7-129">按作業名稱分組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="c0af7-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="c0af7-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="c0af7-130">-GroupByResourceName</span></span>
<span data-ttu-id="c0af7-131">按資源名稱分組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="c0af7-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="c0af7-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="c0af7-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="c0af7-133">已使用節流原則的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="c0af7-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="c0af7-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="c0af7-134">-GroupByUserAgent</span></span>
<span data-ttu-id="c0af7-135">UserAgent 的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="c0af7-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="c0af7-136">-位置</span><span class="sxs-lookup"><span data-stu-id="c0af7-136">-Location</span></span>
<span data-ttu-id="c0af7-137">查詢記錄分析的位置。</span><span class="sxs-lookup"><span data-stu-id="c0af7-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="c0af7-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0af7-138">-NoWait</span></span>
<span data-ttu-id="c0af7-139">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="c0af7-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c0af7-140">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="c0af7-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c0af7-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="c0af7-141">-ToTime</span></span>
<span data-ttu-id="c0af7-142">查詢時間</span><span class="sxs-lookup"><span data-stu-id="c0af7-142">To time of the query</span></span>

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

### <span data-ttu-id="c0af7-143">-確認</span><span class="sxs-lookup"><span data-stu-id="c0af7-143">-Confirm</span></span>
<span data-ttu-id="c0af7-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0af7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0af7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0af7-145">-WhatIf</span></span>
<span data-ttu-id="c0af7-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0af7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0af7-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0af7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0af7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0af7-148">CommonParameters</span></span>
<span data-ttu-id="c0af7-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0af7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0af7-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0af7-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0af7-151">輸入</span><span class="sxs-lookup"><span data-stu-id="c0af7-151">INPUTS</span></span>

### <span data-ttu-id="c0af7-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c0af7-152">System.String</span></span>

## <span data-ttu-id="c0af7-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c0af7-153">OUTPUTS</span></span>

### <span data-ttu-id="c0af7-154">Microsoft.Azure.Commands.Compute.Automation.models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="c0af7-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="c0af7-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c0af7-155">NOTES</span></span>

## <span data-ttu-id="c0af7-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0af7-156">RELATED LINKS</span></span>
