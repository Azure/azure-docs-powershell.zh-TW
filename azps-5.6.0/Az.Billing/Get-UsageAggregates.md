---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911193"
---
# <span data-ttu-id="8c9d6-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="8c9d6-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="8c9d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9d6-103">獲得報告的 Azure 訂閱使用方式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="8c9d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c9d6-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c9d6-105">描述</span><span class="sxs-lookup"><span data-stu-id="8c9d6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c9d6-106">**Get-UsageAggregates** Cmdlet 會根據下列屬性取得匯總的 Azure 訂閱使用量資料：</span><span class="sxs-lookup"><span data-stu-id="8c9d6-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="8c9d6-107">報告使用量的開始與結束時間。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="8c9d6-108">每日或每小時的匯總精確度。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="8c9d6-109">相同資源之多個實例的實例層級詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="8c9d6-110">為取得一致的結果，所返回的資料是根據 Azure 資源報告使用方式詳細資料時所根據。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="8c9d6-111">詳細資訊請參閱 Microsoft 開發人員網路庫中的 Azure Billing REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) 參考資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="8c9d6-112">例子</span><span class="sxs-lookup"><span data-stu-id="8c9d6-112">EXAMPLES</span></span>

### <span data-ttu-id="8c9d6-113">範例 1：取回訂閱資料</span><span class="sxs-lookup"><span data-stu-id="8c9d6-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="8c9d6-114">此命令會針對 2015/5/2 和 2015/5/5 之間的訂閱，取回報告使用量資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="8c9d6-115">參數</span><span class="sxs-lookup"><span data-stu-id="8c9d6-115">PARAMETERS</span></span>

### <span data-ttu-id="8c9d6-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="8c9d6-116">-AggregationGranularity</span></span>
<span data-ttu-id="8c9d6-117">指定資料的匯總精確度。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="8c9d6-118">有效的值為：每日和每小時。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="8c9d6-119">預設值為每日。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d6-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="8c9d6-120">-ContinuationToken</span></span>
<span data-ttu-id="8c9d6-121">指定從上一個呼叫的回應內內容所取的延續權杖。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="8c9d6-122">對於大型結果集，會使用連續權杖來分頁回應。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="8c9d6-123">延續權杖可做為進度的書簽。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="8c9d6-124">如果您未指定此參數，資料會從 *在 ReportedStartTime* 中指定的一天或一小時的開頭進行取用。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="8c9d6-125">我們建議您追蹤回應頁面中的下一個連結，但請注意資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="8c9d6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9d6-126">-DefaultProfile</span></span>
<span data-ttu-id="8c9d6-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c9d6-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="8c9d6-128">-ReportedEndTime</span></span>
<span data-ttu-id="8c9d6-129">指定在 Azure 計費系統中記錄資源使用量時的報告結束時間。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="8c9d6-130">Azure 是一個分散式系統，橫跨全球的多個資料中心，因此實際使用資源的時間之間會延遲，即資源使用時間，以及到達計費系統時 ，即報告的資源使用量時間。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="8c9d6-131">若要取得一段期間所報告之訂閱的所有使用事件，請根據報告的時間進行查詢。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="8c9d6-132">即使您是按報告的時間進行查詢，Cmdlet 還是會根據資源使用時間匯總回應資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="8c9d6-133">資源使用狀況資料是分析資料的實用樞紐。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="8c9d6-134">-報告StartTime</span><span class="sxs-lookup"><span data-stu-id="8c9d6-134">-ReportedStartTime</span></span>
<span data-ttu-id="8c9d6-135">指定在 Azure 計費系統中記錄資源使用量時的報告開始時間。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="8c9d6-136">-顯示詳細</span><span class="sxs-lookup"><span data-stu-id="8c9d6-136">-ShowDetails</span></span>
<span data-ttu-id="8c9d6-137">指出此 Cmdlet 是否會以使用方式資料來返回實例層級詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="8c9d6-138">預設值會$True。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-138">The default value is $True.</span></span>
<span data-ttu-id="8c9d6-139">如果$False，服務會匯總伺服器端的結果，因此會較少的匯總群組。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="8c9d6-140">例如，如果您經營三個網站，根據預設，您就會收到三個供網站使用的專案。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="8c9d6-141">不過，當值為 $False時，同一個 **subscriptionId、meterId、usageStartTime** 和  **usageEndTime** 的所有資料會轉換為單行專案。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9d6-142">CommonParameters</span></span>
<span data-ttu-id="8c9d6-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9d6-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8c9d6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9d6-145">輸入</span><span class="sxs-lookup"><span data-stu-id="8c9d6-145">INPUTS</span></span>

### <span data-ttu-id="8c9d6-146">沒有</span><span class="sxs-lookup"><span data-stu-id="8c9d6-146">None</span></span>

## <span data-ttu-id="8c9d6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8c9d6-147">OUTPUTS</span></span>

### <span data-ttu-id="8c9d6-148">Microsoft.Azure.Commerce.UsageAggregates.models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="8c9d6-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="8c9d6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8c9d6-149">NOTES</span></span>

## <span data-ttu-id="8c9d6-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c9d6-150">RELATED LINKS</span></span>
