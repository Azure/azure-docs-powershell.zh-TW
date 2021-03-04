---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 61ae392b3dbe8b73aaabd617b397e953f5caebec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914506"
---
# <span data-ttu-id="0fc70-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="0fc70-101">Merge-AzReservation</span></span>

## <span data-ttu-id="0fc70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0fc70-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc70-103">合併兩 `Reservation` 個 s。</span><span class="sxs-lookup"><span data-stu-id="0fc70-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="0fc70-104">語法</span><span class="sxs-lookup"><span data-stu-id="0fc70-104">SYNTAX</span></span>

### <span data-ttu-id="0fc70-105">CommandLine (預設) </span><span class="sxs-lookup"><span data-stu-id="0fc70-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc70-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="0fc70-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc70-107">描述</span><span class="sxs-lookup"><span data-stu-id="0fc70-107">DESCRIPTION</span></span>
<span data-ttu-id="0fc70-108">將指定的 `Reservation` s 合併至新 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="0fc70-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="0fc70-109">要 `Reservation` 合併的兩者必須具有相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fc70-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="0fc70-110">例子</span><span class="sxs-lookup"><span data-stu-id="0fc70-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc70-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0fc70-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="0fc70-112">將指定的兩 `Reservation` 個合併成一個 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="0fc70-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="0fc70-113">參數</span><span class="sxs-lookup"><span data-stu-id="0fc70-113">PARAMETERS</span></span>

### <span data-ttu-id="0fc70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc70-114">-DefaultProfile</span></span>
<span data-ttu-id="0fc70-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fc70-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc70-116">-預約</span><span class="sxs-lookup"><span data-stu-id="0fc70-116">-Reservation</span></span>
<span data-ttu-id="0fc70-117">兩個要合併之 ReservationId 的逗號分隔字串</span><span class="sxs-lookup"><span data-stu-id="0fc70-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="0fc70-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="0fc70-118">-ReservationId</span></span>
<span data-ttu-id="0fc70-119">包含兩個 s 的 ReservationOrderId `ReservationOrder` `Reservation`</span><span class="sxs-lookup"><span data-stu-id="0fc70-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="0fc70-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0fc70-120">-ReservationOrderId</span></span>
<span data-ttu-id="0fc70-121">{{fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="0fc70-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="0fc70-122">-確認</span><span class="sxs-lookup"><span data-stu-id="0fc70-122">-Confirm</span></span>
<span data-ttu-id="0fc70-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0fc70-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc70-124">-WhatIf</span></span>
<span data-ttu-id="0fc70-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0fc70-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fc70-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0fc70-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc70-127">CommonParameters</span></span>
<span data-ttu-id="0fc70-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0fc70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc70-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fc70-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc70-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0fc70-130">INPUTS</span></span>

### <span data-ttu-id="0fc70-131">沒有</span><span class="sxs-lookup"><span data-stu-id="0fc70-131">None</span></span>

## <span data-ttu-id="0fc70-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0fc70-132">OUTPUTS</span></span>

### <span data-ttu-id="0fc70-133">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="0fc70-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="0fc70-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0fc70-134">NOTES</span></span>

## <span data-ttu-id="0fc70-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fc70-135">RELATED LINKS</span></span>
