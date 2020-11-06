---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445496"
---
# <span data-ttu-id="246c2-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="246c2-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="246c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="246c2-102">SYNOPSIS</span></span>
<span data-ttu-id="246c2-103">`Reservation`以指定的預留順序取得 s</span><span class="sxs-lookup"><span data-stu-id="246c2-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="246c2-104">SYNTAX</span></span>

### <span data-ttu-id="246c2-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="246c2-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="246c2-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="246c2-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="246c2-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="246c2-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246c2-108">說明</span><span class="sxs-lookup"><span data-stu-id="246c2-108">DESCRIPTION</span></span>
<span data-ttu-id="246c2-109">清單 `Reservation` s 在單一中 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="246c2-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="246c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="246c2-110">EXAMPLES</span></span>

### <span data-ttu-id="246c2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="246c2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="246c2-112">清單 `Reservation` s 在指定範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="246c2-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="246c2-113">範例2</span><span class="sxs-lookup"><span data-stu-id="246c2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="246c2-114">取得特定 `Reservation` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="246c2-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="246c2-115">參數</span><span class="sxs-lookup"><span data-stu-id="246c2-115">PARAMETERS</span></span>

### <span data-ttu-id="246c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246c2-116">-DefaultProfile</span></span>
<span data-ttu-id="246c2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="246c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="246c2-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="246c2-118">-ReservationId</span></span>
<span data-ttu-id="246c2-119">`Reservation`要查看的識別碼</span><span class="sxs-lookup"><span data-stu-id="246c2-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="246c2-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="246c2-120">-ReservationOrder</span></span>
<span data-ttu-id="246c2-121">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="246c2-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="246c2-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="246c2-122">-ReservationOrderId</span></span>
<span data-ttu-id="246c2-123">包含的的識別碼 `ReservationOrder` `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="246c2-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="246c2-124">必填。</span><span class="sxs-lookup"><span data-stu-id="246c2-124">Required.</span></span>

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

### <span data-ttu-id="246c2-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="246c2-125">-ReservationOrderPage</span></span>
<span data-ttu-id="246c2-126">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="246c2-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="246c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246c2-127">CommonParameters</span></span>
<span data-ttu-id="246c2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="246c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246c2-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="246c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246c2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="246c2-130">INPUTS</span></span>

### <span data-ttu-id="246c2-131">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="246c2-131">System.Guid</span></span>

### <span data-ttu-id="246c2-132">PSReservationOrder 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="246c2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="246c2-133">參數： ReservationOrder (ByValue) </span><span class="sxs-lookup"><span data-stu-id="246c2-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="246c2-134">PSReservationOrderPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="246c2-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="246c2-135">參數： ReservationOrderPage (ByValue) </span><span class="sxs-lookup"><span data-stu-id="246c2-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="246c2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="246c2-136">OUTPUTS</span></span>

### <span data-ttu-id="246c2-137">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="246c2-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="246c2-138">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="246c2-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="246c2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="246c2-139">NOTES</span></span>

## <span data-ttu-id="246c2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="246c2-140">RELATED LINKS</span></span>
