---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: d7eab73fbe6bed4a51df7c5056a0dc52787de845
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791341"
---
# <span data-ttu-id="85b4b-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="85b4b-101">Get-AzReservation</span></span>

## <span data-ttu-id="85b4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="85b4b-103">`Reservation`以指定的預留順序取得 s</span><span class="sxs-lookup"><span data-stu-id="85b4b-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="85b4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="85b4b-104">SYNTAX</span></span>

### <span data-ttu-id="85b4b-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="85b4b-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85b4b-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="85b4b-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85b4b-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="85b4b-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85b4b-108">說明</span><span class="sxs-lookup"><span data-stu-id="85b4b-108">DESCRIPTION</span></span>
<span data-ttu-id="85b4b-109">清單 `Reservation` s 在單一中 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="85b4b-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="85b4b-110">示例</span><span class="sxs-lookup"><span data-stu-id="85b4b-110">EXAMPLES</span></span>

### <span data-ttu-id="85b4b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="85b4b-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="85b4b-112">清單 `Reservation` s 在指定範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="85b4b-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="85b4b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="85b4b-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="85b4b-114">取得特定 `Reservation` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="85b4b-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="85b4b-115">參數</span><span class="sxs-lookup"><span data-stu-id="85b4b-115">PARAMETERS</span></span>

### <span data-ttu-id="85b4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b4b-116">-DefaultProfile</span></span>
<span data-ttu-id="85b4b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85b4b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85b4b-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="85b4b-118">-ReservationId</span></span>
<span data-ttu-id="85b4b-119">`Reservation`要查看的識別碼</span><span class="sxs-lookup"><span data-stu-id="85b4b-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="85b4b-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="85b4b-120">-ReservationOrder</span></span>
<span data-ttu-id="85b4b-121">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="85b4b-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="85b4b-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="85b4b-122">-ReservationOrderId</span></span>
<span data-ttu-id="85b4b-123">包含的的識別碼 `ReservationOrder` `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="85b4b-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="85b4b-124">必填。</span><span class="sxs-lookup"><span data-stu-id="85b4b-124">Required.</span></span>

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

### <span data-ttu-id="85b4b-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="85b4b-125">-ReservationOrderPage</span></span>
<span data-ttu-id="85b4b-126">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="85b4b-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="85b4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b4b-127">CommonParameters</span></span>
<span data-ttu-id="85b4b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85b4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b4b-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85b4b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b4b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="85b4b-130">INPUTS</span></span>

### <span data-ttu-id="85b4b-131">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="85b4b-131">System.Guid</span></span>

### <span data-ttu-id="85b4b-132">PSReservationOrder 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="85b4b-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="85b4b-133">PSReservationOrderPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="85b4b-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="85b4b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="85b4b-134">OUTPUTS</span></span>

### <span data-ttu-id="85b4b-135">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="85b4b-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="85b4b-136">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="85b4b-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="85b4b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="85b4b-137">NOTES</span></span>

## <span data-ttu-id="85b4b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="85b4b-138">RELATED LINKS</span></span>
