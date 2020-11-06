---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445487"
---
# <span data-ttu-id="8b307-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="8b307-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="8b307-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b307-102">SYNOPSIS</span></span>
<span data-ttu-id="8b307-103">分割 a `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="8b307-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b307-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b307-104">SYNTAX</span></span>

### <span data-ttu-id="8b307-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="8b307-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b307-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="8b307-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b307-107">說明</span><span class="sxs-lookup"><span data-stu-id="8b307-107">DESCRIPTION</span></span>
<span data-ttu-id="8b307-108">`Reservation`以指定的數量分配分割 a 到兩個 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="8b307-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="8b307-109">示例</span><span class="sxs-lookup"><span data-stu-id="8b307-109">EXAMPLES</span></span>

### <span data-ttu-id="8b307-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8b307-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="8b307-111">將指定的 `Reservation` 數量分割成兩 `Reservation` 秒，並將相對應的數量分割</span><span class="sxs-lookup"><span data-stu-id="8b307-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="8b307-112">參數</span><span class="sxs-lookup"><span data-stu-id="8b307-112">PARAMETERS</span></span>

### <span data-ttu-id="8b307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b307-113">-DefaultProfile</span></span>
<span data-ttu-id="8b307-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b307-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b307-115">數量</span><span class="sxs-lookup"><span data-stu-id="8b307-115">-Quantity</span></span>
<span data-ttu-id="8b307-116">兩個 s 之 [數量] 欄位的逗號分隔整數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8b307-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="8b307-117">預留</span><span class="sxs-lookup"><span data-stu-id="8b307-117">-Reservation</span></span>
<span data-ttu-id="8b307-118">的 Pipe 物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8b307-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="8b307-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8b307-119">-ReservationId</span></span>
<span data-ttu-id="8b307-120">`Reservation`要分割的識別碼</span><span class="sxs-lookup"><span data-stu-id="8b307-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="8b307-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8b307-121">-ReservationOrderId</span></span>
<span data-ttu-id="8b307-122">`ReservationOrder`包含 `Reservation` 要分割之使用者的識別碼</span><span class="sxs-lookup"><span data-stu-id="8b307-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="8b307-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8b307-123">-Confirm</span></span>
<span data-ttu-id="8b307-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b307-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b307-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b307-125">-WhatIf</span></span>
<span data-ttu-id="8b307-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b307-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b307-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b307-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b307-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b307-128">CommonParameters</span></span>
<span data-ttu-id="8b307-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b307-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b307-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b307-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b307-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8b307-131">INPUTS</span></span>

### <span data-ttu-id="8b307-132">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="8b307-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="8b307-133">參數：保留 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8b307-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="8b307-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8b307-134">OUTPUTS</span></span>

### <span data-ttu-id="8b307-135">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="8b307-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8b307-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8b307-136">NOTES</span></span>

## <span data-ttu-id="8b307-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b307-137">RELATED LINKS</span></span>
