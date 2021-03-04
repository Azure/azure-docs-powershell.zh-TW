---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 427e715e055cd909d204f92aedd58eca9d7db0f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914533"
---
# <span data-ttu-id="2b0f9-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="2b0f9-101">Get-AzReservation</span></span>

## <span data-ttu-id="2b0f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0f9-103">取得 `Reservation` 預約訂單</span><span class="sxs-lookup"><span data-stu-id="2b0f9-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="2b0f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b0f9-104">SYNTAX</span></span>

### <span data-ttu-id="2b0f9-105">CommandLine (預設) </span><span class="sxs-lookup"><span data-stu-id="2b0f9-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b0f9-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="2b0f9-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b0f9-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="2b0f9-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b0f9-108">描述</span><span class="sxs-lookup"><span data-stu-id="2b0f9-108">DESCRIPTION</span></span>
<span data-ttu-id="2b0f9-109">清單 `Reservation` 位於單一範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="2b0f9-110">例子</span><span class="sxs-lookup"><span data-stu-id="2b0f9-110">EXAMPLES</span></span>

### <span data-ttu-id="2b0f9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2b0f9-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="2b0f9-112">清單 `Reservation` 位於指定的範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="2b0f9-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2b0f9-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="2b0f9-114">取得特定 `Reservation` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="2b0f9-115">參數</span><span class="sxs-lookup"><span data-stu-id="2b0f9-115">PARAMETERS</span></span>

### <span data-ttu-id="2b0f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b0f9-116">-DefaultProfile</span></span>
<span data-ttu-id="2b0f9-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b0f9-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="2b0f9-118">-ReservationId</span></span>
<span data-ttu-id="2b0f9-119">要查看 `Reservation` 的識別碼</span><span class="sxs-lookup"><span data-stu-id="2b0f9-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b0f9-120">-預約訂單</span><span class="sxs-lookup"><span data-stu-id="2b0f9-120">-ReservationOrder</span></span>
<span data-ttu-id="2b0f9-121">的管道物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2b0f9-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0f9-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2b0f9-122">-ReservationOrderId</span></span>
<span data-ttu-id="2b0f9-123">包含的 `ReservationOrder` 識別碼 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="2b0f9-124">必填。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0f9-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="2b0f9-125">-ReservationOrderPage</span></span>
<span data-ttu-id="2b0f9-126">的管道物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2b0f9-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0f9-127">CommonParameters</span></span>
<span data-ttu-id="2b0f9-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b0f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b0f9-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b0f9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0f9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2b0f9-130">INPUTS</span></span>

### <span data-ttu-id="2b0f9-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="2b0f9-131">System.Guid</span></span>

### <span data-ttu-id="2b0f9-132">Microsoft.Azure.Commands.Reservations.models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="2b0f9-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="2b0f9-133">Microsoft.Azure.Commands.Reservations.models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="2b0f9-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="2b0f9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2b0f9-134">OUTPUTS</span></span>

### <span data-ttu-id="2b0f9-135">Microsoft.Azure.Commands.Reservations.models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="2b0f9-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="2b0f9-136">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="2b0f9-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2b0f9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2b0f9-137">NOTES</span></span>

## <span data-ttu-id="2b0f9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b0f9-138">RELATED LINKS</span></span>
