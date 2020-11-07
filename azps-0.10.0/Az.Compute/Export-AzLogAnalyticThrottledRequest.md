---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796333"
---
# <span data-ttu-id="66ca6-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="66ca6-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="66ca6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="66ca6-103">在指定的時間視窗中，針對此訂閱顯示總限制 Api 要求的匯出記錄。</span><span class="sxs-lookup"><span data-stu-id="66ca6-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="66ca6-104">句法</span><span class="sxs-lookup"><span data-stu-id="66ca6-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66ca6-105">說明</span><span class="sxs-lookup"><span data-stu-id="66ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="66ca6-106">這會匯出已限制的 Microsoft 的總數。計算 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="66ca6-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="66ca6-107">記錄可以由三個選項進一步匯總： GroupByOperationName、GroupByThrottlePolicy 或 GroupByResourceName。</span><span class="sxs-lookup"><span data-stu-id="66ca6-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="66ca6-108">請注意，這個 Cmdlet 只會收集 CRP 記錄。</span><span class="sxs-lookup"><span data-stu-id="66ca6-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="66ca6-109">示例</span><span class="sxs-lookup"><span data-stu-id="66ca6-109">EXAMPLES</span></span>

### <span data-ttu-id="66ca6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="66ca6-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="66ca6-111">這個命令會儲存總的 Microsoft. 在 2018-02-20T17：54：14和 2018-02-22T17：54：17（依作業名稱匯總），在指定的 SAS URI 中計算 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="66ca6-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="66ca6-112">參數</span><span class="sxs-lookup"><span data-stu-id="66ca6-112">PARAMETERS</span></span>

### <span data-ttu-id="66ca6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66ca6-113">-AsJob</span></span>
<span data-ttu-id="66ca6-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66ca6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66ca6-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="66ca6-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="66ca6-116">LogAnalytics Api 將輸出記錄寫入到其中的記錄 blob 容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="66ca6-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="66ca6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ca6-117">-DefaultProfile</span></span>
<span data-ttu-id="66ca6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66ca6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ca6-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="66ca6-119">-FromTime</span></span>
<span data-ttu-id="66ca6-120">查詢的開始時間</span><span class="sxs-lookup"><span data-stu-id="66ca6-120">From time of the query</span></span>

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

### <span data-ttu-id="66ca6-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="66ca6-121">-GroupByOperationName</span></span>
<span data-ttu-id="66ca6-122">依作業名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="66ca6-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="66ca6-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="66ca6-123">-GroupByResourceName</span></span>
<span data-ttu-id="66ca6-124">依資源名稱對查詢結果進行分組。</span><span class="sxs-lookup"><span data-stu-id="66ca6-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="66ca6-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="66ca6-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="66ca6-126">已套用節流原則的群組查詢結果。</span><span class="sxs-lookup"><span data-stu-id="66ca6-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="66ca6-127">-位置</span><span class="sxs-lookup"><span data-stu-id="66ca6-127">-Location</span></span>
<span data-ttu-id="66ca6-128">查詢記錄分析的位置。</span><span class="sxs-lookup"><span data-stu-id="66ca6-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="66ca6-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="66ca6-129">-ToTime</span></span>
<span data-ttu-id="66ca6-130">查詢的 [到] 時間</span><span class="sxs-lookup"><span data-stu-id="66ca6-130">To time of the query</span></span>

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

### <span data-ttu-id="66ca6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="66ca6-131">-Confirm</span></span>
<span data-ttu-id="66ca6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66ca6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ca6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ca6-133">-WhatIf</span></span>
<span data-ttu-id="66ca6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66ca6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ca6-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66ca6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ca6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ca6-136">CommonParameters</span></span>
<span data-ttu-id="66ca6-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66ca6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ca6-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66ca6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ca6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="66ca6-139">INPUTS</span></span>

### <span data-ttu-id="66ca6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="66ca6-140">System.String</span></span>

## <span data-ttu-id="66ca6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="66ca6-141">OUTPUTS</span></span>

### <span data-ttu-id="66ca6-142">PSLogAnalyticsOperationResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="66ca6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="66ca6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="66ca6-143">NOTES</span></span>

## <span data-ttu-id="66ca6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="66ca6-144">RELATED LINKS</span></span>

