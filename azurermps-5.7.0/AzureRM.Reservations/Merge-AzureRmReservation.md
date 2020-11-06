---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448578"
---
# <span data-ttu-id="67fa4-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="67fa4-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="67fa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="67fa4-103">合併兩個 `Reservation` s。</span><span class="sxs-lookup"><span data-stu-id="67fa4-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67fa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="67fa4-104">SYNTAX</span></span>

### <span data-ttu-id="67fa4-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="67fa4-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67fa4-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="67fa4-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67fa4-107">說明</span><span class="sxs-lookup"><span data-stu-id="67fa4-107">DESCRIPTION</span></span>
<span data-ttu-id="67fa4-108">將指定 `Reservation` 的 s 合併至新的 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="67fa4-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="67fa4-109">要合併的兩個 `Reservation` 都必須有相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="67fa4-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="67fa4-110">示例</span><span class="sxs-lookup"><span data-stu-id="67fa4-110">EXAMPLES</span></span>

### <span data-ttu-id="67fa4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="67fa4-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="67fa4-112">將兩個指定的 `Reservation` s 合併成一個 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="67fa4-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="67fa4-113">參數</span><span class="sxs-lookup"><span data-stu-id="67fa4-113">PARAMETERS</span></span>

### <span data-ttu-id="67fa4-114">預留</span><span class="sxs-lookup"><span data-stu-id="67fa4-114">-Reservation</span></span>
<span data-ttu-id="67fa4-115">要合併的兩個 ReservationIds 的逗號分隔字串</span><span class="sxs-lookup"><span data-stu-id="67fa4-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67fa4-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="67fa4-116">-ReservationId</span></span>
<span data-ttu-id="67fa4-117">`ReservationOrder`包含兩個 s 的 ReservationOrderId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="67fa4-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa4-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="67fa4-118">-ReservationOrderId</span></span>
<span data-ttu-id="67fa4-119">{{Fill ReservationOrderId 說明}}</span><span class="sxs-lookup"><span data-stu-id="67fa4-119">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa4-120">-確認</span><span class="sxs-lookup"><span data-stu-id="67fa4-120">-Confirm</span></span>
<span data-ttu-id="67fa4-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67fa4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67fa4-122">-WhatIf</span></span>
<span data-ttu-id="67fa4-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67fa4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67fa4-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67fa4-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67fa4-125">CommonParameters</span></span>
<span data-ttu-id="67fa4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67fa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67fa4-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67fa4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67fa4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="67fa4-128">INPUTS</span></span>

### <span data-ttu-id="67fa4-129">PSReservation [] 的 []</span><span class="sxs-lookup"><span data-stu-id="67fa4-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="67fa4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="67fa4-130">OUTPUTS</span></span>

### <span data-ttu-id="67fa4-131">[System.object]。清單 ' 1 [PSReservation，#........ = 1.0.0.0，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="67fa4-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="67fa4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="67fa4-132">NOTES</span></span>

## <span data-ttu-id="67fa4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="67fa4-133">RELATED LINKS</span></span>

