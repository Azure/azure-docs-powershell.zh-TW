---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 9ea53203bc07cca5ca5a8b7909f9fbab558e3c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914497"
---
# <span data-ttu-id="2bb5d-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="2bb5d-101">Split-AzReservation</span></span>

## <span data-ttu-id="2bb5d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2bb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb5d-103">分割 `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="2bb5d-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="2bb5d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2bb5d-104">SYNTAX</span></span>

### <span data-ttu-id="2bb5d-105">CommandLine (預設) </span><span class="sxs-lookup"><span data-stu-id="2bb5d-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bb5d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="2bb5d-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bb5d-107">描述</span><span class="sxs-lookup"><span data-stu-id="2bb5d-107">DESCRIPTION</span></span>
<span data-ttu-id="2bb5d-108">使用指定的 `Reservation` 數量 `Reservation` 分配將一個分割成兩個 s。</span><span class="sxs-lookup"><span data-stu-id="2bb5d-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="2bb5d-109">例子</span><span class="sxs-lookup"><span data-stu-id="2bb5d-109">EXAMPLES</span></span>

### <span data-ttu-id="2bb5d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2bb5d-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="2bb5d-111">使用對應的 `Reservation` 數量將指定的 `Reservation` 專案分割成兩個 s</span><span class="sxs-lookup"><span data-stu-id="2bb5d-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="2bb5d-112">參數</span><span class="sxs-lookup"><span data-stu-id="2bb5d-112">PARAMETERS</span></span>

### <span data-ttu-id="2bb5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb5d-113">-DefaultProfile</span></span>
<span data-ttu-id="2bb5d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bb5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bb5d-115">-數量</span><span class="sxs-lookup"><span data-stu-id="2bb5d-115">-Quantity</span></span>
<span data-ttu-id="2bb5d-116">兩個 s 數量欄位的逗號分隔 `Reservation` 整數</span><span class="sxs-lookup"><span data-stu-id="2bb5d-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="2bb5d-117">-預約</span><span class="sxs-lookup"><span data-stu-id="2bb5d-117">-Reservation</span></span>
<span data-ttu-id="2bb5d-118">的管道物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="2bb5d-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="2bb5d-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="2bb5d-119">-ReservationId</span></span>
<span data-ttu-id="2bb5d-120">要分割 `Reservation` 的識別碼</span><span class="sxs-lookup"><span data-stu-id="2bb5d-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="2bb5d-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2bb5d-121">-ReservationOrderId</span></span>
<span data-ttu-id="2bb5d-122">包含使用者想要 `ReservationOrder` `Reservation` 分割之識別碼</span><span class="sxs-lookup"><span data-stu-id="2bb5d-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="2bb5d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2bb5d-123">-Confirm</span></span>
<span data-ttu-id="2bb5d-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2bb5d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bb5d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bb5d-125">-WhatIf</span></span>
<span data-ttu-id="2bb5d-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bb5d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bb5d-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bb5d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bb5d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb5d-128">CommonParameters</span></span>
<span data-ttu-id="2bb5d-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2bb5d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb5d-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bb5d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb5d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2bb5d-131">INPUTS</span></span>

### <span data-ttu-id="2bb5d-132">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="2bb5d-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2bb5d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2bb5d-133">OUTPUTS</span></span>

### <span data-ttu-id="2bb5d-134">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="2bb5d-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2bb5d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2bb5d-135">NOTES</span></span>

## <span data-ttu-id="2bb5d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bb5d-136">RELATED LINKS</span></span>
