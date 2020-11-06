---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM.UsageAggregates
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
ms.openlocfilehash: 1c5c705ec55889182a38d1586559f59d57e2d366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447899"
---
# <span data-ttu-id="37412-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="37412-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="37412-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37412-102">SYNOPSIS</span></span>
<span data-ttu-id="37412-103">取得報告的 Azure 訂閱使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="37412-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37412-104">句法</span><span class="sxs-lookup"><span data-stu-id="37412-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37412-105">說明</span><span class="sxs-lookup"><span data-stu-id="37412-105">DESCRIPTION</span></span>
<span data-ttu-id="37412-106">**UsageAggregates** Cmdlet 會透過下列屬性取得匯總的 Azure 訂閱使用資料：</span><span class="sxs-lookup"><span data-stu-id="37412-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="37412-107">報告使用方式的開始和結束時間。</span><span class="sxs-lookup"><span data-stu-id="37412-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="37412-108">[每日] 或 [每小時] 的匯總精確度。</span><span class="sxs-lookup"><span data-stu-id="37412-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="37412-109">同一資源多個實例的實例層級詳細資料。</span><span class="sxs-lookup"><span data-stu-id="37412-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="37412-110">針對一致的結果，傳回的資料是根據 Azure 資源報告使用狀況詳細資料的時間。</span><span class="sxs-lookup"><span data-stu-id="37412-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="37412-111">如需詳細資訊，請參閱 https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Microsoft 開發人員網路文件庫中的 AZURE 帳單 REST API 參考 (。</span><span class="sxs-lookup"><span data-stu-id="37412-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="37412-112">示例</span><span class="sxs-lookup"><span data-stu-id="37412-112">EXAMPLES</span></span>

### <span data-ttu-id="37412-113">範例1：檢索訂閱資料</span><span class="sxs-lookup"><span data-stu-id="37412-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="37412-114">這個命令會針對5/2/2015 和5/5/2015 之間的訂閱檢索報告的使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="37412-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="37412-115">參數</span><span class="sxs-lookup"><span data-stu-id="37412-115">PARAMETERS</span></span>

### <span data-ttu-id="37412-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="37412-116">-AggregationGranularity</span></span>
<span data-ttu-id="37412-117">指定資料的匯總精確度。</span><span class="sxs-lookup"><span data-stu-id="37412-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="37412-118">有效值為： [每日] 和 [每小時]。</span><span class="sxs-lookup"><span data-stu-id="37412-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="37412-119">預設值為 [每日]。</span><span class="sxs-lookup"><span data-stu-id="37412-119">The default value is Daily.</span></span>

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

### <span data-ttu-id="37412-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="37412-120">-ContinuationToken</span></span>
<span data-ttu-id="37412-121">指定從先前通話中的回應本文中檢索到的延續標記。</span><span class="sxs-lookup"><span data-stu-id="37412-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="37412-122">針對大型結果集，回應會使用延續標記進行分頁。</span><span class="sxs-lookup"><span data-stu-id="37412-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="37412-123">延續標記會充當進度的書簽。</span><span class="sxs-lookup"><span data-stu-id="37412-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="37412-124">如果您沒有指定此參數，則會從 *ReportedStartTime* 中指定的日期或小時數開始檢索資料。</span><span class="sxs-lookup"><span data-stu-id="37412-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="37412-125">我們建議您追蹤資料的 [回應] 頁面中的下一個連結。</span><span class="sxs-lookup"><span data-stu-id="37412-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="37412-126">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="37412-126">-ReportedEndTime</span></span>
<span data-ttu-id="37412-127">指定在 Azure 帳單系統中記錄資源使用狀況時所報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="37412-127">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="37412-128">Azure 是一種分散式系統，遍佈世界各地的多個資料中心，因此在資源實際使用時間和使用方式事件達到帳單系統之間有延遲，這是資源使用量所報告的時間。</span><span class="sxs-lookup"><span data-stu-id="37412-128">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="37412-129">若要取得針對某個時段報告之訂閱的所有使用方式事件，您需要依報告的時間進行查詢。</span><span class="sxs-lookup"><span data-stu-id="37412-129">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="37412-130">即使您是依報告的時間進行查詢，此 Cmdlet 也會依資源使用時間來匯總回應資料。</span><span class="sxs-lookup"><span data-stu-id="37412-130">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="37412-131">[資源使用狀況] 資料對於分析資料而言是實用的樞紐分析表。</span><span class="sxs-lookup"><span data-stu-id="37412-131">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="37412-132">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="37412-132">-ReportedStartTime</span></span>
<span data-ttu-id="37412-133">指定在 Azure 帳單系統中記錄資源使用狀況時所報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="37412-133">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="37412-134">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="37412-134">-ShowDetails</span></span>
<span data-ttu-id="37412-135">指示此 Cmdlet 是否會傳回使用方式資料的實例層級詳細資料。</span><span class="sxs-lookup"><span data-stu-id="37412-135">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="37412-136">預設值為 [$True]。</span><span class="sxs-lookup"><span data-stu-id="37412-136">The default value is $True.</span></span>

<span data-ttu-id="37412-137">如果 $False，服務會將結果聚集在伺服器端，因此會傳回較少的匯總群組。</span><span class="sxs-lookup"><span data-stu-id="37412-137">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="37412-138">例如，如果您執行的是三個網站，預設會針對網站使用方式取得三個明細專案。</span><span class="sxs-lookup"><span data-stu-id="37412-138">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="37412-139">不過，當此值為 $False 時，相同的 **subscriptionId** 、 **meterId** 、 **usageStartTime** 和 **usageEndTime** 的所有資料都會折迭為單一明細專案。</span><span class="sxs-lookup"><span data-stu-id="37412-139">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

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

### <span data-ttu-id="37412-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37412-140">-DefaultProfile</span></span>
<span data-ttu-id="37412-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37412-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37412-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37412-142">CommonParameters</span></span>
<span data-ttu-id="37412-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37412-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37412-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37412-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37412-145">輸入</span><span class="sxs-lookup"><span data-stu-id="37412-145">INPUTS</span></span>

## <span data-ttu-id="37412-146">輸出</span><span class="sxs-lookup"><span data-stu-id="37412-146">OUTPUTS</span></span>

### <span data-ttu-id="37412-147">UsageAggregationGetResponse 中的 UsageAggregates。</span><span class="sxs-lookup"><span data-stu-id="37412-147">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="37412-148">筆記</span><span class="sxs-lookup"><span data-stu-id="37412-148">NOTES</span></span>

## <span data-ttu-id="37412-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="37412-149">RELATED LINKS</span></span>
