---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 9783d1ff8d3a42d3ad6627abcaae792f966b7828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914521"
---
# <span data-ttu-id="e89a1-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e89a1-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="e89a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e89a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e89a1-103">取得適用的 `ReservationOrder` 識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="e89a1-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="e89a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="e89a1-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e89a1-105">描述</span><span class="sxs-lookup"><span data-stu-id="e89a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e89a1-106">取得可適用于此訂閱 `ReservationOrder` 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e89a1-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="e89a1-107">例子</span><span class="sxs-lookup"><span data-stu-id="e89a1-107">EXAMPLES</span></span>

### <span data-ttu-id="e89a1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e89a1-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="e89a1-109">適用于 `ReservationOrder` 預設訂閱</span><span class="sxs-lookup"><span data-stu-id="e89a1-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="e89a1-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="e89a1-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e89a1-111">取得 `ReservationOrder` 適用于指定的訂閱</span><span class="sxs-lookup"><span data-stu-id="e89a1-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="e89a1-112">參數</span><span class="sxs-lookup"><span data-stu-id="e89a1-112">PARAMETERS</span></span>

### <span data-ttu-id="e89a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89a1-113">-DefaultProfile</span></span>
<span data-ttu-id="e89a1-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e89a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e89a1-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e89a1-115">-SubscriptionId</span></span>
<span data-ttu-id="e89a1-116">訂閱的識別碼，以取得已申請 `ReservationOrder` 的</span><span class="sxs-lookup"><span data-stu-id="e89a1-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="e89a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89a1-117">CommonParameters</span></span>
<span data-ttu-id="e89a1-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e89a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89a1-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e89a1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89a1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e89a1-120">INPUTS</span></span>

### <span data-ttu-id="e89a1-121">沒有</span><span class="sxs-lookup"><span data-stu-id="e89a1-121">None</span></span>

## <span data-ttu-id="e89a1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e89a1-122">OUTPUTS</span></span>

### <span data-ttu-id="e89a1-123">Microsoft.Azure.management.Reservations.models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="e89a1-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="e89a1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e89a1-124">NOTES</span></span>

## <span data-ttu-id="e89a1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e89a1-125">RELATED LINKS</span></span>
