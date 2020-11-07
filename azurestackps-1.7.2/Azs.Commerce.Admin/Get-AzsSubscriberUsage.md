---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792619"
---
# <span data-ttu-id="45b6c-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="45b6c-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="45b6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="45b6c-103">在指定的 timespan 期間取得使用資料。</span><span class="sxs-lookup"><span data-stu-id="45b6c-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="45b6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="45b6c-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="45b6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="45b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="45b6c-106">在指定的 timespan 期間取得使用資料。</span><span class="sxs-lookup"><span data-stu-id="45b6c-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="45b6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="45b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="45b6c-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45b6c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="45b6c-109">從過去24小時取得使用資料。</span><span class="sxs-lookup"><span data-stu-id="45b6c-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="45b6c-110">參數</span><span class="sxs-lookup"><span data-stu-id="45b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="45b6c-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="45b6c-111">-AggregationGranularity</span></span>
<span data-ttu-id="45b6c-112">匯總細微性。</span><span class="sxs-lookup"><span data-stu-id="45b6c-112">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b6c-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="45b6c-113">-ContinuationToken</span></span>
<span data-ttu-id="45b6c-114">延續標記。</span><span class="sxs-lookup"><span data-stu-id="45b6c-114">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b6c-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="45b6c-115">-ReportedEndTime</span></span>
<span data-ttu-id="45b6c-116">報告的結束時間 (獨佔) 。</span><span class="sxs-lookup"><span data-stu-id="45b6c-116">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b6c-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="45b6c-117">-ReportedStartTime</span></span>
<span data-ttu-id="45b6c-118">報告的開始時間 (包含) 。</span><span class="sxs-lookup"><span data-stu-id="45b6c-118">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="45b6c-119">-略過</span><span class="sxs-lookup"><span data-stu-id="45b6c-119">-Skip</span></span>
<span data-ttu-id="45b6c-120">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="45b6c-120">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b6c-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="45b6c-121">-SubscriberId</span></span>
<span data-ttu-id="45b6c-122">租使用者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="45b6c-122">The tenant subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b6c-123">-上方</span><span class="sxs-lookup"><span data-stu-id="45b6c-123">-Top</span></span>
<span data-ttu-id="45b6c-124">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="45b6c-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45b6c-125">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="45b6c-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b6c-126">CommonParameters</span></span>
<span data-ttu-id="45b6c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45b6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b6c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45b6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b6c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="45b6c-129">INPUTS</span></span>

## <span data-ttu-id="45b6c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="45b6c-130">OUTPUTS</span></span>

### <span data-ttu-id="45b6c-131">[AzureStack] 管理. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="45b6c-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="45b6c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="45b6c-132">NOTES</span></span>

## <span data-ttu-id="45b6c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="45b6c-133">RELATED LINKS</span></span>

