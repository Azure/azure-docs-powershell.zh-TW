---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457383"
---
# <span data-ttu-id="918ad-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="918ad-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="918ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="918ad-102">SYNOPSIS</span></span>
<span data-ttu-id="918ad-103">取得 `Reservation` 修訂歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="918ad-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="918ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="918ad-104">SYNTAX</span></span>

### <span data-ttu-id="918ad-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="918ad-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="918ad-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="918ad-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="918ad-107">說明</span><span class="sxs-lookup"><span data-stu-id="918ad-107">DESCRIPTION</span></span>
<span data-ttu-id="918ad-108">所有修訂版本的清單 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="918ad-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="918ad-109">示例</span><span class="sxs-lookup"><span data-stu-id="918ad-109">EXAMPLES</span></span>

### <span data-ttu-id="918ad-110">範例1</span><span class="sxs-lookup"><span data-stu-id="918ad-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="918ad-111">取得特定保留的修訂歷程記錄</span><span class="sxs-lookup"><span data-stu-id="918ad-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="918ad-112">參數</span><span class="sxs-lookup"><span data-stu-id="918ad-112">PARAMETERS</span></span>

### <span data-ttu-id="918ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918ad-113">-DefaultProfile</span></span>
<span data-ttu-id="918ad-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="918ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="918ad-115">預留</span><span class="sxs-lookup"><span data-stu-id="918ad-115">-Reservation</span></span>
<span data-ttu-id="918ad-116">S 的管道物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="918ad-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="918ad-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="918ad-117">-ReservationId</span></span>
<span data-ttu-id="918ad-118">`Reservation`要顯示其記錄的 ReservationId</span><span class="sxs-lookup"><span data-stu-id="918ad-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="918ad-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="918ad-119">-ReservationOrderId</span></span>
<span data-ttu-id="918ad-120">ReservationOrderId `ReservationOrder` 包含 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="918ad-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="918ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918ad-121">CommonParameters</span></span>
<span data-ttu-id="918ad-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="918ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918ad-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="918ad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918ad-124">輸入</span><span class="sxs-lookup"><span data-stu-id="918ad-124">INPUTS</span></span>

### <span data-ttu-id="918ad-125">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="918ad-125">System.Guid</span></span>

### <span data-ttu-id="918ad-126">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="918ad-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="918ad-127">參數：保留 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="918ad-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="918ad-128">輸出</span><span class="sxs-lookup"><span data-stu-id="918ad-128">OUTPUTS</span></span>

### <span data-ttu-id="918ad-129">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="918ad-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="918ad-130">筆記</span><span class="sxs-lookup"><span data-stu-id="918ad-130">NOTES</span></span>

## <span data-ttu-id="918ad-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="918ad-131">RELATED LINKS</span></span>
