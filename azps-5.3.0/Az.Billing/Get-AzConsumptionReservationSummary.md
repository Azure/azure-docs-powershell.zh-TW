---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450002"
---
# <span data-ttu-id="181b7-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="181b7-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="181b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="181b7-102">SYNOPSIS</span></span>
<span data-ttu-id="181b7-103">取得 [每日] 或 [每月] 細微性的保留摘要。</span><span class="sxs-lookup"><span data-stu-id="181b7-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="181b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="181b7-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181b7-105">說明</span><span class="sxs-lookup"><span data-stu-id="181b7-105">DESCRIPTION</span></span>
<span data-ttu-id="181b7-106">**AzConsumptionReservationSummary** Cmdlet 會取得 [每天] 或 [每月] 細微性的保留摘要。</span><span class="sxs-lookup"><span data-stu-id="181b7-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="181b7-107">示例</span><span class="sxs-lookup"><span data-stu-id="181b7-107">EXAMPLES</span></span>

### <span data-ttu-id="181b7-108">範例1：取得含每月顆粒之預留訂單 Id 的保留摘要</span><span class="sxs-lookup"><span data-stu-id="181b7-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="181b7-109">範例2：取得保留摘要，以及每月顆粒的預留訂單識別碼和預留 Id</span><span class="sxs-lookup"><span data-stu-id="181b7-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="181b7-110">範例3：取得保留摘要，並為每日提供的保留訂單識別碼提供日期範圍</span><span class="sxs-lookup"><span data-stu-id="181b7-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="181b7-111">範例4：取得保留摘要，並為每日提供的保留訂單 Id 和保留 Id 提供日期範圍</span><span class="sxs-lookup"><span data-stu-id="181b7-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="181b7-112">參數</span><span class="sxs-lookup"><span data-stu-id="181b7-112">PARAMETERS</span></span>

### <span data-ttu-id="181b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181b7-113">-DefaultProfile</span></span>
<span data-ttu-id="181b7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="181b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181b7-115">-結束日期</span><span class="sxs-lookup"><span data-stu-id="181b7-115">-EndDate</span></span>
<span data-ttu-id="181b7-116">[結束資料] (UTC) 的 [保留摘要] （僅適用于日）。</span><span class="sxs-lookup"><span data-stu-id="181b7-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181b7-117">細微性</span><span class="sxs-lookup"><span data-stu-id="181b7-117">-Grain</span></span>
<span data-ttu-id="181b7-118">[預留摘要] 的時間細微性可以是 [每天] 或 [每月]。</span><span class="sxs-lookup"><span data-stu-id="181b7-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181b7-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="181b7-119">-ReservationId</span></span>
<span data-ttu-id="181b7-120">預留順序中的預訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="181b7-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="181b7-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="181b7-121">-ReservationOrderId</span></span>
<span data-ttu-id="181b7-122">預訂採購的識別碼。</span><span class="sxs-lookup"><span data-stu-id="181b7-122">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181b7-123">-開始日期</span><span class="sxs-lookup"><span data-stu-id="181b7-123">-StartDate</span></span>
<span data-ttu-id="181b7-124">[開始資料] (UTC) 的 [保留摘要] （僅適用于 [每日細微性]）。</span><span class="sxs-lookup"><span data-stu-id="181b7-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181b7-125">CommonParameters</span></span>
<span data-ttu-id="181b7-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="181b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181b7-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="181b7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181b7-128">輸入</span><span class="sxs-lookup"><span data-stu-id="181b7-128">INPUTS</span></span>

### <span data-ttu-id="181b7-129">所有</span><span class="sxs-lookup"><span data-stu-id="181b7-129">None</span></span>

## <span data-ttu-id="181b7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="181b7-130">OUTPUTS</span></span>

### <span data-ttu-id="181b7-131">PSReservationSummary 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="181b7-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="181b7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="181b7-132">NOTES</span></span>

## <span data-ttu-id="181b7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="181b7-133">RELATED LINKS</span></span>
