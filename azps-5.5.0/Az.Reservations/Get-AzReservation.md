---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142646"
---
# <span data-ttu-id="41024-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="41024-101">Get-AzReservation</span></span>

## <span data-ttu-id="41024-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41024-102">SYNOPSIS</span></span>
<span data-ttu-id="41024-103">`Reservation`以指定的預留順序取得 s</span><span class="sxs-lookup"><span data-stu-id="41024-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="41024-104">句法</span><span class="sxs-lookup"><span data-stu-id="41024-104">SYNTAX</span></span>

### <span data-ttu-id="41024-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="41024-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41024-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="41024-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41024-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="41024-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41024-108">說明</span><span class="sxs-lookup"><span data-stu-id="41024-108">DESCRIPTION</span></span>
<span data-ttu-id="41024-109">清單 `Reservation` s 在單一中 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="41024-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="41024-110">示例</span><span class="sxs-lookup"><span data-stu-id="41024-110">EXAMPLES</span></span>

### <span data-ttu-id="41024-111">範例1</span><span class="sxs-lookup"><span data-stu-id="41024-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="41024-112">清單 `Reservation` s 在指定範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="41024-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="41024-113">範例2</span><span class="sxs-lookup"><span data-stu-id="41024-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="41024-114">取得特定 `Reservation` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41024-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="41024-115">參數</span><span class="sxs-lookup"><span data-stu-id="41024-115">PARAMETERS</span></span>

### <span data-ttu-id="41024-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41024-116">-DefaultProfile</span></span>
<span data-ttu-id="41024-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41024-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41024-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="41024-118">-ReservationId</span></span>
<span data-ttu-id="41024-119">`Reservation`要查看的識別碼</span><span class="sxs-lookup"><span data-stu-id="41024-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="41024-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="41024-120">-ReservationOrder</span></span>
<span data-ttu-id="41024-121">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="41024-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="41024-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="41024-122">-ReservationOrderId</span></span>
<span data-ttu-id="41024-123">包含的的識別碼 `ReservationOrder` `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="41024-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="41024-124">必填。</span><span class="sxs-lookup"><span data-stu-id="41024-124">Required.</span></span>

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

### <span data-ttu-id="41024-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="41024-125">-ReservationOrderPage</span></span>
<span data-ttu-id="41024-126">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="41024-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="41024-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41024-127">CommonParameters</span></span>
<span data-ttu-id="41024-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41024-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41024-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41024-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41024-130">輸入</span><span class="sxs-lookup"><span data-stu-id="41024-130">INPUTS</span></span>

### <span data-ttu-id="41024-131">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="41024-131">System.Guid</span></span>

### <span data-ttu-id="41024-132">PSReservationOrder 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="41024-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="41024-133">PSReservationOrderPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="41024-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="41024-134">輸出</span><span class="sxs-lookup"><span data-stu-id="41024-134">OUTPUTS</span></span>

### <span data-ttu-id="41024-135">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="41024-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="41024-136">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="41024-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="41024-137">筆記</span><span class="sxs-lookup"><span data-stu-id="41024-137">NOTES</span></span>

## <span data-ttu-id="41024-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="41024-138">RELATED LINKS</span></span>
