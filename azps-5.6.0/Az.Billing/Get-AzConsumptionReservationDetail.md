---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 43ecacc0c54a48091680a6f7a9b33c8294461cdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908646"
---
# <span data-ttu-id="93660-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="93660-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="93660-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93660-102">SYNOPSIS</span></span>
<span data-ttu-id="93660-103">取得提供日期範圍的預約詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93660-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="93660-104">語法</span><span class="sxs-lookup"><span data-stu-id="93660-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93660-105">描述</span><span class="sxs-lookup"><span data-stu-id="93660-105">DESCRIPTION</span></span>
<span data-ttu-id="93660-106">**Get-AzConsumptionReservationDetail** Cmdlet 會取得提供日期範圍的預約詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93660-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="93660-107">例子</span><span class="sxs-lookup"><span data-stu-id="93660-107">EXAMPLES</span></span>

### <span data-ttu-id="93660-108">範例 1：取得提供日期範圍的預約訂單識別碼的預約詳細資料</span><span class="sxs-lookup"><span data-stu-id="93660-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="93660-109">範例 2：取得預約訂單識別碼的預約詳細資料，以及提供日期範圍的預約識別碼</span><span class="sxs-lookup"><span data-stu-id="93660-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="93660-110">參數</span><span class="sxs-lookup"><span data-stu-id="93660-110">PARAMETERS</span></span>

### <span data-ttu-id="93660-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93660-111">-DefaultProfile</span></span>
<span data-ttu-id="93660-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93660-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93660-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="93660-113">-EndDate</span></span>
<span data-ttu-id="93660-114">以 UTC (YYYY-MM-DD 的結束) 保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93660-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="93660-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="93660-115">-ReservationId</span></span>
<span data-ttu-id="93660-116">保留訂單內的保留識別碼。</span><span class="sxs-lookup"><span data-stu-id="93660-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="93660-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="93660-117">-ReservationOrderId</span></span>
<span data-ttu-id="93660-118">購買預約的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93660-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="93660-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="93660-119">-StartDate</span></span>
<span data-ttu-id="93660-120">以 UTC (YYYY-MM-DD) 保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93660-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="93660-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93660-121">CommonParameters</span></span>
<span data-ttu-id="93660-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93660-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93660-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="93660-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93660-124">輸入</span><span class="sxs-lookup"><span data-stu-id="93660-124">INPUTS</span></span>

### <span data-ttu-id="93660-125">沒有</span><span class="sxs-lookup"><span data-stu-id="93660-125">None</span></span>

## <span data-ttu-id="93660-126">輸出</span><span class="sxs-lookup"><span data-stu-id="93660-126">OUTPUTS</span></span>

### <span data-ttu-id="93660-127">Microsoft.Azure.Commands.Consumption.models.PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="93660-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="93660-128">筆記</span><span class="sxs-lookup"><span data-stu-id="93660-128">NOTES</span></span>

## <span data-ttu-id="93660-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="93660-129">RELATED LINKS</span></span>
