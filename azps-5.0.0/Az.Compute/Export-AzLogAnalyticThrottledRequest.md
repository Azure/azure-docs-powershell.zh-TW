---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140648"
---
# <span data-ttu-id="cb3c1-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="cb3c1-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="cb3c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3c1-103">在指定的時間視窗中，針對此訂閱顯示總限制 Api 要求的匯出記錄。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="cb3c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb3c1-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb3c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="cb3c1-106">這會匯出已限制的 Microsoft 的總數。計算 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="cb3c1-107">記錄可以由三個選項進一步匯總： GroupByOperationName、GroupByThrottlePolicy 或 GroupByResourceName。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="cb3c1-108">請注意，這個 Cmdlet 只會收集 CRP 記錄。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="cb3c1-109">如需計算資源提供者的 API 節流概覽，請參閱 https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits 。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="cb3c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="cb3c1-110">EXAMPLES</span></span>

### <span data-ttu-id="cb3c1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cb3c1-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="cb3c1-112">這個命令會儲存總的 Microsoft. 在 2018-02-20T17：54：14和 2018-02-22T17：54：17（依作業名稱匯總），在指定的 SAS URI 中計算 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="cb3c1-113">參數</span><span class="sxs-lookup"><span data-stu-id="cb3c1-113">PARAMETERS</span></span>

### <span data-ttu-id="cb3c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb3c1-114">-AsJob</span></span>
<span data-ttu-id="cb3c1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb3c1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb3c1-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="cb3c1-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="cb3c1-117">LogAnalytics Api 將輸出記錄寫入到其中的記錄 blob 容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="cb3c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3c1-118">-DefaultProfile</span></span>
<span data-ttu-id="cb3c1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3c1-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="cb3c1-120">-FromTime</span></span>
<span data-ttu-id="cb3c1-121">查詢的開始時間</span><span class="sxs-lookup"><span data-stu-id="cb3c1-121">From time of the query</span></span>

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

### <span data-ttu-id="cb3c1-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="cb3c1-122">-GroupByOperationName</span></span>
<span data-ttu-id="cb3c1-123">依作業名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="cb3c1-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="cb3c1-124">-GroupByResourceName</span></span>
<span data-ttu-id="cb3c1-125">依資源名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="cb3c1-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c1-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="cb3c1-127">已套用節流原則的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="cb3c1-128">-位置</span><span class="sxs-lookup"><span data-stu-id="cb3c1-128">-Location</span></span>
<span data-ttu-id="cb3c1-129">查詢記錄分析的位置。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="cb3c1-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cb3c1-130">-NoWait</span></span>
<span data-ttu-id="cb3c1-131">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cb3c1-132">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cb3c1-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="cb3c1-133">-ToTime</span></span>
<span data-ttu-id="cb3c1-134">查詢的 [到] 時間</span><span class="sxs-lookup"><span data-stu-id="cb3c1-134">To time of the query</span></span>

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

### <span data-ttu-id="cb3c1-135">-確認</span><span class="sxs-lookup"><span data-stu-id="cb3c1-135">-Confirm</span></span>
<span data-ttu-id="cb3c1-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3c1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3c1-137">-WhatIf</span></span>
<span data-ttu-id="cb3c1-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb3c1-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3c1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3c1-140">CommonParameters</span></span>
<span data-ttu-id="cb3c1-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3c1-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3c1-143">輸入</span><span class="sxs-lookup"><span data-stu-id="cb3c1-143">INPUTS</span></span>

### <span data-ttu-id="cb3c1-144">System.object</span><span class="sxs-lookup"><span data-stu-id="cb3c1-144">System.String</span></span>

## <span data-ttu-id="cb3c1-145">輸出</span><span class="sxs-lookup"><span data-stu-id="cb3c1-145">OUTPUTS</span></span>

### <span data-ttu-id="cb3c1-146">PSLogAnalyticsOperationResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="cb3c1-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="cb3c1-147">筆記</span><span class="sxs-lookup"><span data-stu-id="cb3c1-147">NOTES</span></span>

## <span data-ttu-id="cb3c1-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb3c1-148">RELATED LINKS</span></span>
