---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444384"
---
# <span data-ttu-id="5cb50-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="5cb50-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="5cb50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5cb50-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb50-103">`Reservation`以指定的預留順序取得 s</span><span class="sxs-lookup"><span data-stu-id="5cb50-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb50-104">句法</span><span class="sxs-lookup"><span data-stu-id="5cb50-104">SYNTAX</span></span>

### <span data-ttu-id="5cb50-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="5cb50-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="5cb50-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="5cb50-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="5cb50-107">說明</span><span class="sxs-lookup"><span data-stu-id="5cb50-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb50-108">清單 `Reservation` s 在單一中 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="5cb50-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="5cb50-109">示例</span><span class="sxs-lookup"><span data-stu-id="5cb50-109">EXAMPLES</span></span>

### <span data-ttu-id="5cb50-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5cb50-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5cb50-111">清單 `Reservation` s 在指定範圍內 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="5cb50-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="5cb50-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5cb50-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="5cb50-113">取得特定 `Reservation` 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5cb50-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="5cb50-114">參數</span><span class="sxs-lookup"><span data-stu-id="5cb50-114">PARAMETERS</span></span>

### <span data-ttu-id="5cb50-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="5cb50-115">-ReservationId</span></span>
<span data-ttu-id="5cb50-116">`Reservation`要查看的識別碼</span><span class="sxs-lookup"><span data-stu-id="5cb50-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb50-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="5cb50-117">-ReservationOrder</span></span>
<span data-ttu-id="5cb50-118">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5cb50-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb50-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5cb50-119">-ReservationOrderId</span></span>
<span data-ttu-id="5cb50-120">包含的的識別碼 `ReservationOrder` `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="5cb50-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="5cb50-121">必填。</span><span class="sxs-lookup"><span data-stu-id="5cb50-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb50-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="5cb50-122">-ReservationOrderPage</span></span>
<span data-ttu-id="5cb50-123">的 Pipe 物件參數 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5cb50-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb50-124">CommonParameters</span></span>
<span data-ttu-id="5cb50-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5cb50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb50-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5cb50-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb50-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5cb50-127">INPUTS</span></span>

### <span data-ttu-id="5cb50-128">System.object</span><span class="sxs-lookup"><span data-stu-id="5cb50-128">System.String</span></span>
<span data-ttu-id="5cb50-129">PSReservationOrder PSReservationOrderPage 中的 [#.]...。</span><span class="sxs-lookup"><span data-stu-id="5cb50-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="5cb50-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5cb50-130">OUTPUTS</span></span>

### <span data-ttu-id="5cb50-131">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="5cb50-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="5cb50-132">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="5cb50-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5cb50-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5cb50-133">NOTES</span></span>

## <span data-ttu-id="5cb50-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5cb50-134">RELATED LINKS</span></span>

