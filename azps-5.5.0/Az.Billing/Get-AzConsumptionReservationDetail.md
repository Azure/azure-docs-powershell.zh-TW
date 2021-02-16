---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 2a49cb88fc25643cd26e7ed75d226b8abf6ee50f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138747"
---
# <span data-ttu-id="d1728-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="d1728-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="d1728-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1728-102">SYNOPSIS</span></span>
<span data-ttu-id="d1728-103">取得所提供日期範圍的預訂詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1728-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="d1728-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1728-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1728-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1728-105">DESCRIPTION</span></span>
<span data-ttu-id="d1728-106">**AzConsumptionReservationDetail** Cmdlet 會取得所提供日期範圍的保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1728-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="d1728-107">示例</span><span class="sxs-lookup"><span data-stu-id="d1728-107">EXAMPLES</span></span>

### <span data-ttu-id="d1728-108">範例1：使用提供之日期範圍的保留訂單識別碼來取得保留詳細資料</span><span class="sxs-lookup"><span data-stu-id="d1728-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
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

### <span data-ttu-id="d1728-109">範例2：使用所提供日期範圍的保留訂單識別碼和保留識別碼來取得保留詳細資料</span><span class="sxs-lookup"><span data-stu-id="d1728-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
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

## <span data-ttu-id="d1728-110">參數</span><span class="sxs-lookup"><span data-stu-id="d1728-110">PARAMETERS</span></span>

### <span data-ttu-id="d1728-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1728-111">-DefaultProfile</span></span>
<span data-ttu-id="d1728-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1728-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1728-113">-結束日期</span><span class="sxs-lookup"><span data-stu-id="d1728-113">-EndDate</span></span>
<span data-ttu-id="d1728-114">[結束資料] (UTC) 的保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1728-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="d1728-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d1728-115">-ReservationId</span></span>
<span data-ttu-id="d1728-116">預留順序中的預訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1728-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="d1728-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d1728-117">-ReservationOrderId</span></span>
<span data-ttu-id="d1728-118">預訂採購的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1728-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="d1728-119">-開始日期</span><span class="sxs-lookup"><span data-stu-id="d1728-119">-StartDate</span></span>
<span data-ttu-id="d1728-120">[開始資料] (UTC) 的保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1728-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="d1728-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1728-121">CommonParameters</span></span>
<span data-ttu-id="d1728-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1728-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1728-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1728-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1728-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d1728-124">INPUTS</span></span>

### <span data-ttu-id="d1728-125">所有</span><span class="sxs-lookup"><span data-stu-id="d1728-125">None</span></span>

## <span data-ttu-id="d1728-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d1728-126">OUTPUTS</span></span>

### <span data-ttu-id="d1728-127">PSReservationDetail 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d1728-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="d1728-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d1728-128">NOTES</span></span>

## <span data-ttu-id="d1728-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1728-129">RELATED LINKS</span></span>
