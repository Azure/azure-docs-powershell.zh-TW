---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: c0016eed43fa315a7bb135153c8b00c47248f235
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914529"
---
# <span data-ttu-id="57cec-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="57cec-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="57cec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57cec-102">SYNOPSIS</span></span>
<span data-ttu-id="57cec-103">取得 `Reservation` 修訂歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="57cec-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="57cec-104">語法</span><span class="sxs-lookup"><span data-stu-id="57cec-104">SYNTAX</span></span>

### <span data-ttu-id="57cec-105">CommandLine (預設) </span><span class="sxs-lookup"><span data-stu-id="57cec-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57cec-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="57cec-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57cec-107">描述</span><span class="sxs-lookup"><span data-stu-id="57cec-107">DESCRIPTION</span></span>
<span data-ttu-id="57cec-108">的修訂清單 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="57cec-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="57cec-109">例子</span><span class="sxs-lookup"><span data-stu-id="57cec-109">EXAMPLES</span></span>

### <span data-ttu-id="57cec-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="57cec-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="57cec-111">取得特定預約的修訂歷程記錄</span><span class="sxs-lookup"><span data-stu-id="57cec-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="57cec-112">參數</span><span class="sxs-lookup"><span data-stu-id="57cec-112">PARAMETERS</span></span>

### <span data-ttu-id="57cec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cec-113">-DefaultProfile</span></span>
<span data-ttu-id="57cec-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57cec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57cec-115">-預約</span><span class="sxs-lookup"><span data-stu-id="57cec-115">-Reservation</span></span>
<span data-ttu-id="57cec-116">s 的管道物件 `Reservation` 參數</span><span class="sxs-lookup"><span data-stu-id="57cec-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="57cec-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="57cec-117">-ReservationId</span></span>
<span data-ttu-id="57cec-118">要顯示歷程記錄 `Reservation` 之保留Id</span><span class="sxs-lookup"><span data-stu-id="57cec-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="57cec-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="57cec-119">-ReservationOrderId</span></span>
<span data-ttu-id="57cec-120">包含 `ReservationOrder``Reservation`</span><span class="sxs-lookup"><span data-stu-id="57cec-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="57cec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cec-121">CommonParameters</span></span>
<span data-ttu-id="57cec-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57cec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cec-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57cec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cec-124">輸入</span><span class="sxs-lookup"><span data-stu-id="57cec-124">INPUTS</span></span>

### <span data-ttu-id="57cec-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="57cec-125">System.Guid</span></span>

### <span data-ttu-id="57cec-126">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="57cec-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="57cec-127">輸出</span><span class="sxs-lookup"><span data-stu-id="57cec-127">OUTPUTS</span></span>

### <span data-ttu-id="57cec-128">Microsoft.Azure.Commands.Reservations.models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="57cec-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="57cec-129">筆記</span><span class="sxs-lookup"><span data-stu-id="57cec-129">NOTES</span></span>

## <span data-ttu-id="57cec-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="57cec-130">RELATED LINKS</span></span>
