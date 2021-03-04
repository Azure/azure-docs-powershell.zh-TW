---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: 92647c861f2616d8c9cf8c44534dc2cf6a1138e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916285"
---
# <span data-ttu-id="88b38-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="88b38-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="88b38-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88b38-102">SYNOPSIS</span></span>
<span data-ttu-id="88b38-103">取得每日或每月谷類的預約摘要。</span><span class="sxs-lookup"><span data-stu-id="88b38-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="88b38-104">語法</span><span class="sxs-lookup"><span data-stu-id="88b38-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b38-105">描述</span><span class="sxs-lookup"><span data-stu-id="88b38-105">DESCRIPTION</span></span>
<span data-ttu-id="88b38-106">**Get-AzConsumptionReservationSummary Cmdlet** 會取得每日或每月谷類的預約摘要。</span><span class="sxs-lookup"><span data-stu-id="88b38-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="88b38-107">例子</span><span class="sxs-lookup"><span data-stu-id="88b38-107">EXAMPLES</span></span>

### <span data-ttu-id="88b38-108">範例 1：取得具有每月谷類預定訂單識別碼的保留摘要</span><span class="sxs-lookup"><span data-stu-id="88b38-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
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

### <span data-ttu-id="88b38-109">範例 2：取得保留訂單識別碼的預約摘要，以及每月谷類的預約識別碼</span><span class="sxs-lookup"><span data-stu-id="88b38-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
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

### <span data-ttu-id="88b38-110">範例 3：取得包含每日谷類提供日期範圍的保留訂單識別碼的預約摘要</span><span class="sxs-lookup"><span data-stu-id="88b38-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
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

### <span data-ttu-id="88b38-111">範例 4：取得包含預訂訂單識別碼的預約摘要，以及每日提供日期範圍的保留識別碼</span><span class="sxs-lookup"><span data-stu-id="88b38-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
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

## <span data-ttu-id="88b38-112">參數</span><span class="sxs-lookup"><span data-stu-id="88b38-112">PARAMETERS</span></span>

### <span data-ttu-id="88b38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b38-113">-DefaultProfile</span></span>
<span data-ttu-id="88b38-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88b38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b38-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="88b38-115">-EndDate</span></span>
<span data-ttu-id="88b38-116">保留摘要 (UTC) YYYY-MM-DD 的結束資料，僅適用于每日谷類。</span><span class="sxs-lookup"><span data-stu-id="88b38-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="88b38-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="88b38-117">-Grain</span></span>
<span data-ttu-id="88b38-118">保留摘要的時間分項可以是每天或每月。</span><span class="sxs-lookup"><span data-stu-id="88b38-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="88b38-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="88b38-119">-ReservationId</span></span>
<span data-ttu-id="88b38-120">保留訂單內的保留識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b38-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="88b38-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="88b38-121">-ReservationOrderId</span></span>
<span data-ttu-id="88b38-122">購買預約的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b38-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="88b38-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="88b38-123">-StartDate</span></span>
<span data-ttu-id="88b38-124">保留摘要 (UTC) YYYY-MM-DD 的起始資料，僅適用于每日谷類。</span><span class="sxs-lookup"><span data-stu-id="88b38-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="88b38-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b38-125">CommonParameters</span></span>
<span data-ttu-id="88b38-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88b38-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b38-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="88b38-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b38-128">輸入</span><span class="sxs-lookup"><span data-stu-id="88b38-128">INPUTS</span></span>

### <span data-ttu-id="88b38-129">沒有</span><span class="sxs-lookup"><span data-stu-id="88b38-129">None</span></span>

## <span data-ttu-id="88b38-130">輸出</span><span class="sxs-lookup"><span data-stu-id="88b38-130">OUTPUTS</span></span>

### <span data-ttu-id="88b38-131">Microsoft.Azure.Commands.Consumption.models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="88b38-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="88b38-132">筆記</span><span class="sxs-lookup"><span data-stu-id="88b38-132">NOTES</span></span>

## <span data-ttu-id="88b38-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="88b38-133">RELATED LINKS</span></span>
