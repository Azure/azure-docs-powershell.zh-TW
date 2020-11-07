---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798470"
---
# <span data-ttu-id="9f6c3-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="9f6c3-101">Get-AzReservation</span></span>

## <span data-ttu-id="9f6c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6c3-103">`Reservation`以指定的預留順序取得 s</span><span class="sxs-lookup"><span data-stu-id="9f6c3-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="9f6c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f6c3-104">SYNTAX</span></span>

### <span data-ttu-id="9f6c3-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="9f6c3-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f6c3-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="9f6c3-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f6c3-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="9f6c3-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f6c3-108">說明</span><span class="sxs-lookup"><span data-stu-id="9f6c3-108">DESCRIPTION</span></span>
<span data-ttu-id="9f6c3-109">清單 `Reservation` s 在單一中 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="9f6c3-110">示例</span><span class="sxs-lookup"><span data-stu-id="9f6c3-110">EXAMPLES</span></span>

### <span data-ttu-id="9f6c3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9f6c3-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="9f6c3-112">清單 `Reservation` s 在指定範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="9f6c3-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9f6c3-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="9f6c3-114">取得特定 `Reservation` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="9f6c3-115">參數</span><span class="sxs-lookup"><span data-stu-id="9f6c3-115">PARAMETERS</span></span>

### <span data-ttu-id="9f6c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6c3-116">-DefaultProfile</span></span>
<span data-ttu-id="9f6c3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6c3-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9f6c3-118">-ReservationId</span></span>
<span data-ttu-id="9f6c3-119">`Reservation`要查看的識別碼</span><span class="sxs-lookup"><span data-stu-id="9f6c3-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="9f6c3-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="9f6c3-120">-ReservationOrder</span></span>
<span data-ttu-id="9f6c3-121">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="9f6c3-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="9f6c3-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9f6c3-122">-ReservationOrderId</span></span>
<span data-ttu-id="9f6c3-123">包含的的識別碼 `ReservationOrder` `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="9f6c3-124">必填。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-124">Required.</span></span>

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

### <span data-ttu-id="9f6c3-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="9f6c3-125">-ReservationOrderPage</span></span>
<span data-ttu-id="9f6c3-126">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="9f6c3-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="9f6c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6c3-127">CommonParameters</span></span>
<span data-ttu-id="9f6c3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6c3-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6c3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="9f6c3-130">INPUTS</span></span>

### <span data-ttu-id="9f6c3-131">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="9f6c3-131">System.Guid</span></span>

### <span data-ttu-id="9f6c3-132">PSReservationOrder 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="9f6c3-133">PSReservationOrderPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="9f6c3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9f6c3-134">OUTPUTS</span></span>

### <span data-ttu-id="9f6c3-135">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="9f6c3-136">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="9f6c3-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9f6c3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9f6c3-137">NOTES</span></span>

## <span data-ttu-id="9f6c3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f6c3-138">RELATED LINKS</span></span>
