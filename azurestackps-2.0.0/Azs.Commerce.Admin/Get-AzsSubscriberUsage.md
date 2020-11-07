---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796542"
---
# <span data-ttu-id="db9f4-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="db9f4-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="db9f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="db9f4-103">取得從使用者 UsageAggregates 的 SubscriberUsageAggregates 集合。</span><span class="sxs-lookup"><span data-stu-id="db9f4-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="db9f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="db9f4-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="db9f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="db9f4-105">DESCRIPTION</span></span>
<span data-ttu-id="db9f4-106">取得從使用者 UsageAggregates 的 SubscriberUsageAggregates 集合。</span><span class="sxs-lookup"><span data-stu-id="db9f4-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="db9f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="db9f4-107">EXAMPLES</span></span>

### <span data-ttu-id="db9f4-108">範例1：取得依日匯總的使用資料</span><span class="sxs-lookup"><span data-stu-id="db9f4-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="db9f4-109">取得以當天匯總之提供者所代表的所有租使用者在)  (2019 年12月30日的使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="db9f4-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="db9f4-110">ReportedStartTime 和 ReportedEndTime 必須四捨五入為天。</span><span class="sxs-lookup"><span data-stu-id="db9f4-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="db9f4-111">如果您是以服務管理員身分呼叫，這會有效地顯示每個租使用者的所有使用資料。</span><span class="sxs-lookup"><span data-stu-id="db9f4-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="db9f4-112">範例2：取得依小時匯總的使用方式資料</span><span class="sxs-lookup"><span data-stu-id="db9f4-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="db9f4-113">在 12am-2am 的 30 Dec 2019 (之間取得使用方式資料，) 匯總依據小時。</span><span class="sxs-lookup"><span data-stu-id="db9f4-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="db9f4-114">ReportedStartTime 和 ReportedEndTime 必須四捨五入為小時。</span><span class="sxs-lookup"><span data-stu-id="db9f4-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="db9f4-115">同樣地，如果是以服務管理員身分呼叫，這會有效顯示每個租使用者的所有使用資料。</span><span class="sxs-lookup"><span data-stu-id="db9f4-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="db9f4-116">參數</span><span class="sxs-lookup"><span data-stu-id="db9f4-116">PARAMETERS</span></span>

### <span data-ttu-id="db9f4-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="db9f4-117">-AggregationGranularity</span></span>
<span data-ttu-id="db9f4-118">匯總細微性。</span><span class="sxs-lookup"><span data-stu-id="db9f4-118">The aggregation granularity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="db9f4-119">-ContinuationToken</span></span>
<span data-ttu-id="db9f4-120">延續標記。</span><span class="sxs-lookup"><span data-stu-id="db9f4-120">The continuation token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9f4-121">-DefaultProfile</span></span>
<span data-ttu-id="db9f4-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db9f4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="db9f4-123">-ReportedEndTime</span></span>
<span data-ttu-id="db9f4-124">報告的結束時間 (獨佔) 。</span><span class="sxs-lookup"><span data-stu-id="db9f4-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="db9f4-125">-ReportedStartTime</span></span>
<span data-ttu-id="db9f4-126">報告的開始時間 (包含) 。</span><span class="sxs-lookup"><span data-stu-id="db9f4-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="db9f4-127">-SubscriberId</span></span>
<span data-ttu-id="db9f4-128">租使用者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="db9f4-128">The tenant subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db9f4-129">-SubscriptionId</span></span>
<span data-ttu-id="db9f4-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="db9f4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="db9f4-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="db9f4-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db9f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9f4-132">CommonParameters</span></span>
<span data-ttu-id="db9f4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db9f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9f4-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db9f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9f4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="db9f4-135">INPUTS</span></span>

## <span data-ttu-id="db9f4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="db9f4-136">OUTPUTS</span></span>

### <span data-ttu-id="db9f4-137">[Api20150601Preview.]... IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="db9f4-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="db9f4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="db9f4-138">NOTES</span></span>

## <span data-ttu-id="db9f4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="db9f4-139">RELATED LINKS</span></span>

