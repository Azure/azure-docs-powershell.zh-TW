---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128120"
---
# <span data-ttu-id="d3ad8-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d3ad8-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="d3ad8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ad8-103">取得適用識別碼的清單 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="d3ad8-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="d3ad8-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3ad8-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3ad8-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ad8-106">取得 `ReservationOrder` 可套用至此訂閱的適用應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3ad8-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="d3ad8-107">示例</span><span class="sxs-lookup"><span data-stu-id="d3ad8-107">EXAMPLES</span></span>

### <span data-ttu-id="d3ad8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d3ad8-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="d3ad8-109">適用于 `ReservationOrder` 預設訂閱</span><span class="sxs-lookup"><span data-stu-id="d3ad8-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="d3ad8-110">範例2</span><span class="sxs-lookup"><span data-stu-id="d3ad8-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d3ad8-111">適用于 `ReservationOrder` 指定的訂閱</span><span class="sxs-lookup"><span data-stu-id="d3ad8-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="d3ad8-112">參數</span><span class="sxs-lookup"><span data-stu-id="d3ad8-112">PARAMETERS</span></span>

### <span data-ttu-id="d3ad8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad8-113">-DefaultProfile</span></span>
<span data-ttu-id="d3ad8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3ad8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3ad8-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3ad8-115">-SubscriptionId</span></span>
<span data-ttu-id="d3ad8-116">取得已套用之訂閱的識別碼 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d3ad8-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ad8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ad8-117">CommonParameters</span></span>
<span data-ttu-id="d3ad8-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3ad8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ad8-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3ad8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ad8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d3ad8-120">INPUTS</span></span>

### <span data-ttu-id="d3ad8-121">所有</span><span class="sxs-lookup"><span data-stu-id="d3ad8-121">None</span></span>

## <span data-ttu-id="d3ad8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d3ad8-122">OUTPUTS</span></span>

### <span data-ttu-id="d3ad8-123">AppliedReservations 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="d3ad8-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="d3ad8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d3ad8-124">NOTES</span></span>

## <span data-ttu-id="d3ad8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3ad8-125">RELATED LINKS</span></span>
