---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452084"
---
# <span data-ttu-id="905e0-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="905e0-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="905e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="905e0-102">SYNOPSIS</span></span>
<span data-ttu-id="905e0-103">取得 `Reservation` 修訂歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="905e0-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="905e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="905e0-104">SYNTAX</span></span>

### <span data-ttu-id="905e0-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="905e0-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="905e0-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="905e0-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="905e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="905e0-107">DESCRIPTION</span></span>
<span data-ttu-id="905e0-108">所有修訂版本的清單 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="905e0-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="905e0-109">示例</span><span class="sxs-lookup"><span data-stu-id="905e0-109">EXAMPLES</span></span>

### <span data-ttu-id="905e0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="905e0-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="905e0-111">取得特定保留的修訂歷程記錄</span><span class="sxs-lookup"><span data-stu-id="905e0-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="905e0-112">參數</span><span class="sxs-lookup"><span data-stu-id="905e0-112">PARAMETERS</span></span>

### <span data-ttu-id="905e0-113">預留</span><span class="sxs-lookup"><span data-stu-id="905e0-113">-Reservation</span></span>
<span data-ttu-id="905e0-114">S 的管道物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="905e0-114">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="905e0-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="905e0-115">-ReservationId</span></span>
<span data-ttu-id="905e0-116">`Reservation`要顯示其記錄的 ReservationId</span><span class="sxs-lookup"><span data-stu-id="905e0-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="905e0-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="905e0-117">-ReservationOrderId</span></span>
<span data-ttu-id="905e0-118">ReservationOrderId `ReservationOrder` 包含 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="905e0-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="905e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905e0-119">CommonParameters</span></span>
<span data-ttu-id="905e0-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="905e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905e0-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="905e0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905e0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="905e0-122">INPUTS</span></span>

### <span data-ttu-id="905e0-123">System.object</span><span class="sxs-lookup"><span data-stu-id="905e0-123">System.String</span></span>
<span data-ttu-id="905e0-124">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="905e0-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="905e0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="905e0-125">OUTPUTS</span></span>

### <span data-ttu-id="905e0-126">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="905e0-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="905e0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="905e0-127">NOTES</span></span>

## <span data-ttu-id="905e0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="905e0-128">RELATED LINKS</span></span>

