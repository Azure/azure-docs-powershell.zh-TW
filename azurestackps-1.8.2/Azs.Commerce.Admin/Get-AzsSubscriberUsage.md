---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968247"
---
# <span data-ttu-id="6ffc6-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="6ffc6-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="6ffc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ffc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffc6-103">在指定的 timespan 期間取得使用資料。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="6ffc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ffc6-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6ffc6-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ffc6-105">DESCRIPTION</span></span>
<span data-ttu-id="6ffc6-106">在指定的 timespan 期間取得使用資料。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="6ffc6-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ffc6-107">EXAMPLES</span></span>

### <span data-ttu-id="6ffc6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6ffc6-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="6ffc6-109">從過去24小時取得使用資料。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="6ffc6-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ffc6-110">PARAMETERS</span></span>

### <span data-ttu-id="6ffc6-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="6ffc6-111">-SubscriberId</span></span>
<span data-ttu-id="6ffc6-112">租使用者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="6ffc6-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="6ffc6-113">-ReportedStartTime</span></span>
<span data-ttu-id="6ffc6-114">報告的開始時間 (包含) 。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-114">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="6ffc6-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="6ffc6-115">-AggregationGranularity</span></span>
<span data-ttu-id="6ffc6-116">匯總細微性。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="6ffc6-117">-略過</span><span class="sxs-lookup"><span data-stu-id="6ffc6-117">-Skip</span></span>
<span data-ttu-id="6ffc6-118">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6ffc6-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="6ffc6-119">-ReportedEndTime</span></span>
<span data-ttu-id="6ffc6-120">報告的結束時間 (獨佔) 。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-120">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="6ffc6-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="6ffc6-121">-ContinuationToken</span></span>
<span data-ttu-id="6ffc6-122">延續標記。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-122">The continuation token.</span></span>

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

### <span data-ttu-id="6ffc6-123">-上方</span><span class="sxs-lookup"><span data-stu-id="6ffc6-123">-Top</span></span>
<span data-ttu-id="6ffc6-124">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6ffc6-125">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6ffc6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffc6-126">CommonParameters</span></span>
<span data-ttu-id="6ffc6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffc6-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffc6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6ffc6-129">INPUTS</span></span>

## <span data-ttu-id="6ffc6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="6ffc6-130">OUTPUTS</span></span>

### <span data-ttu-id="6ffc6-131">[AzureStack] 管理. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="6ffc6-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="6ffc6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6ffc6-132">NOTES</span></span>

## <span data-ttu-id="6ffc6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ffc6-133">RELATED LINKS</span></span>
