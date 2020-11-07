---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 8974a8a0bf8230b630a848e922527bc0b08bdb02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791317"
---
# <span data-ttu-id="62e73-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="62e73-101">Merge-AzReservation</span></span>

## <span data-ttu-id="62e73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62e73-102">SYNOPSIS</span></span>
<span data-ttu-id="62e73-103">合併兩個 `Reservation` s。</span><span class="sxs-lookup"><span data-stu-id="62e73-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="62e73-104">句法</span><span class="sxs-lookup"><span data-stu-id="62e73-104">SYNTAX</span></span>

### <span data-ttu-id="62e73-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="62e73-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e73-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="62e73-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e73-107">說明</span><span class="sxs-lookup"><span data-stu-id="62e73-107">DESCRIPTION</span></span>
<span data-ttu-id="62e73-108">將指定 `Reservation` 的 s 合併至新的 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="62e73-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="62e73-109">要合併的兩個 `Reservation` 都必須有相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="62e73-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="62e73-110">示例</span><span class="sxs-lookup"><span data-stu-id="62e73-110">EXAMPLES</span></span>

### <span data-ttu-id="62e73-111">範例1</span><span class="sxs-lookup"><span data-stu-id="62e73-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="62e73-112">將兩個指定的 `Reservation` s 合併成一個 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="62e73-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="62e73-113">參數</span><span class="sxs-lookup"><span data-stu-id="62e73-113">PARAMETERS</span></span>

### <span data-ttu-id="62e73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e73-114">-DefaultProfile</span></span>
<span data-ttu-id="62e73-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62e73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e73-116">預留</span><span class="sxs-lookup"><span data-stu-id="62e73-116">-Reservation</span></span>
<span data-ttu-id="62e73-117">要合併的兩個 ReservationIds 的逗號分隔字串</span><span class="sxs-lookup"><span data-stu-id="62e73-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e73-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="62e73-118">-ReservationId</span></span>
<span data-ttu-id="62e73-119">`ReservationOrder`包含兩個 s 的 ReservationOrderId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="62e73-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e73-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="62e73-120">-ReservationOrderId</span></span>
<span data-ttu-id="62e73-121">{{Fill ReservationOrderId 說明}}</span><span class="sxs-lookup"><span data-stu-id="62e73-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="62e73-122">-確認</span><span class="sxs-lookup"><span data-stu-id="62e73-122">-Confirm</span></span>
<span data-ttu-id="62e73-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62e73-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e73-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e73-124">-WhatIf</span></span>
<span data-ttu-id="62e73-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62e73-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62e73-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62e73-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e73-127">CommonParameters</span></span>
<span data-ttu-id="62e73-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62e73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e73-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62e73-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e73-130">輸入</span><span class="sxs-lookup"><span data-stu-id="62e73-130">INPUTS</span></span>

### <span data-ttu-id="62e73-131">所有</span><span class="sxs-lookup"><span data-stu-id="62e73-131">None</span></span>

## <span data-ttu-id="62e73-132">輸出</span><span class="sxs-lookup"><span data-stu-id="62e73-132">OUTPUTS</span></span>

### <span data-ttu-id="62e73-133">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="62e73-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="62e73-134">筆記</span><span class="sxs-lookup"><span data-stu-id="62e73-134">NOTES</span></span>

## <span data-ttu-id="62e73-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="62e73-135">RELATED LINKS</span></span>
