---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
ms.openlocfilehash: a7a4b50198a63329b0d45986f2bce60edb927777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623559"
---
# <span data-ttu-id="23d59-101">Get-AzureRmConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="23d59-101">Get-AzureRmConsumptionReservationDetail</span></span>

## <span data-ttu-id="23d59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23d59-102">SYNOPSIS</span></span>
<span data-ttu-id="23d59-103">取得所提供日期範圍的預訂詳細資料。</span><span class="sxs-lookup"><span data-stu-id="23d59-103">Get reservations details for provided date range.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d59-104">句法</span><span class="sxs-lookup"><span data-stu-id="23d59-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d59-105">說明</span><span class="sxs-lookup"><span data-stu-id="23d59-105">DESCRIPTION</span></span>
<span data-ttu-id="23d59-106">**AzureRmConsumptionReservationDetail** Cmdlet 會取得所提供日期範圍的保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="23d59-106">The **Get-AzureRmConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="23d59-107">示例</span><span class="sxs-lookup"><span data-stu-id="23d59-107">EXAMPLES</span></span>

### <span data-ttu-id="23d59-108">範例1：使用提供之日期範圍的保留訂單識別碼來取得保留詳細資料</span><span class="sxs-lookup"><span data-stu-id="23d59-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
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

### <span data-ttu-id="23d59-109">範例2：使用所提供日期範圍的保留訂單識別碼和保留識別碼來取得保留詳細資料</span><span class="sxs-lookup"><span data-stu-id="23d59-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
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

## <span data-ttu-id="23d59-110">參數</span><span class="sxs-lookup"><span data-stu-id="23d59-110">PARAMETERS</span></span>

### <span data-ttu-id="23d59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d59-111">-DefaultProfile</span></span>
<span data-ttu-id="23d59-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23d59-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d59-113">-結束日期</span><span class="sxs-lookup"><span data-stu-id="23d59-113">-EndDate</span></span>
<span data-ttu-id="23d59-114">[結束資料] (UTC) 的保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="23d59-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="23d59-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="23d59-115">-ReservationId</span></span>
<span data-ttu-id="23d59-116">預留順序中的預訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="23d59-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="23d59-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="23d59-117">-ReservationOrderId</span></span>
<span data-ttu-id="23d59-118">預訂採購的識別碼。</span><span class="sxs-lookup"><span data-stu-id="23d59-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="23d59-119">-開始日期</span><span class="sxs-lookup"><span data-stu-id="23d59-119">-StartDate</span></span>
<span data-ttu-id="23d59-120">[開始資料] (UTC) 的保留詳細資料。</span><span class="sxs-lookup"><span data-stu-id="23d59-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="23d59-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d59-121">CommonParameters</span></span>
<span data-ttu-id="23d59-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23d59-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d59-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23d59-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d59-124">輸入</span><span class="sxs-lookup"><span data-stu-id="23d59-124">INPUTS</span></span>

### <span data-ttu-id="23d59-125">所有</span><span class="sxs-lookup"><span data-stu-id="23d59-125">None</span></span>

## <span data-ttu-id="23d59-126">輸出</span><span class="sxs-lookup"><span data-stu-id="23d59-126">OUTPUTS</span></span>

### <span data-ttu-id="23d59-127">PSReservationDetail 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23d59-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="23d59-128">筆記</span><span class="sxs-lookup"><span data-stu-id="23d59-128">NOTES</span></span>

## <span data-ttu-id="23d59-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="23d59-129">RELATED LINKS</span></span>
