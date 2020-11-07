---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957799"
---
# <span data-ttu-id="e2808-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e2808-101">Split-AzReservation</span></span>

## <span data-ttu-id="e2808-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2808-102">SYNOPSIS</span></span>
<span data-ttu-id="e2808-103">分割 a `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="e2808-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="e2808-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2808-104">SYNTAX</span></span>

### <span data-ttu-id="e2808-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="e2808-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2808-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e2808-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2808-107">說明</span><span class="sxs-lookup"><span data-stu-id="e2808-107">DESCRIPTION</span></span>
<span data-ttu-id="e2808-108">`Reservation`以指定的數量分配分割 a 到兩個 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="e2808-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="e2808-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2808-109">EXAMPLES</span></span>

### <span data-ttu-id="e2808-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e2808-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="e2808-111">將指定的 `Reservation` 數量分割成兩 `Reservation` 秒，並將相對應的數量分割</span><span class="sxs-lookup"><span data-stu-id="e2808-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="e2808-112">參數</span><span class="sxs-lookup"><span data-stu-id="e2808-112">PARAMETERS</span></span>

### <span data-ttu-id="e2808-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2808-113">-DefaultProfile</span></span>
<span data-ttu-id="e2808-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2808-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2808-115">數量</span><span class="sxs-lookup"><span data-stu-id="e2808-115">-Quantity</span></span>
<span data-ttu-id="e2808-116">兩個 s 之 [數量] 欄位的逗號分隔整數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e2808-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-117">預留</span><span class="sxs-lookup"><span data-stu-id="e2808-117">-Reservation</span></span>
<span data-ttu-id="e2808-118">的 Pipe 物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e2808-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e2808-119">-ReservationId</span></span>
<span data-ttu-id="e2808-120">`Reservation`要分割的識別碼</span><span class="sxs-lookup"><span data-stu-id="e2808-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e2808-121">-ReservationOrderId</span></span>
<span data-ttu-id="e2808-122">`ReservationOrder`包含 `Reservation` 要分割之使用者的識別碼</span><span class="sxs-lookup"><span data-stu-id="e2808-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e2808-123">-Confirm</span></span>
<span data-ttu-id="e2808-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2808-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2808-125">-WhatIf</span></span>
<span data-ttu-id="e2808-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2808-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2808-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2808-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2808-128">CommonParameters</span></span>
<span data-ttu-id="e2808-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2808-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2808-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2808-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2808-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e2808-131">INPUTS</span></span>

### <span data-ttu-id="e2808-132">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="e2808-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e2808-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e2808-133">OUTPUTS</span></span>

### <span data-ttu-id="e2808-134">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="e2808-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e2808-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e2808-135">NOTES</span></span>

## <span data-ttu-id="e2808-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2808-136">RELATED LINKS</span></span>
