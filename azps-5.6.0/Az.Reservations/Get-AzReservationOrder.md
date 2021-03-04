---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 1878237544cc1b44b5e47814f455638c168e2412
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914522"
---
# <span data-ttu-id="6da31-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="6da31-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="6da31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6da31-102">SYNOPSIS</span></span>
<span data-ttu-id="6da31-103">獲取 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="6da31-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="6da31-104">語法</span><span class="sxs-lookup"><span data-stu-id="6da31-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6da31-105">描述</span><span class="sxs-lookup"><span data-stu-id="6da31-105">DESCRIPTION</span></span>
<span data-ttu-id="6da31-106">使用者目前租使用者中 `ReservationOrder` 所有可存取之專案的清單。</span><span class="sxs-lookup"><span data-stu-id="6da31-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="6da31-107">如果已設定 ReservationOrderId 參數，請取得該特定 ReservationOrder。</span><span class="sxs-lookup"><span data-stu-id="6da31-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="6da31-108">例子</span><span class="sxs-lookup"><span data-stu-id="6da31-108">EXAMPLES</span></span>

### <span data-ttu-id="6da31-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="6da31-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="6da31-110">列出 `ReservationOrder` 目前租使用者中使用者擁有存取權的所有專案</span><span class="sxs-lookup"><span data-stu-id="6da31-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="6da31-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="6da31-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="6da31-112">取得 `ReservationOrder` 指定的 ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6da31-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="6da31-113">參數</span><span class="sxs-lookup"><span data-stu-id="6da31-113">PARAMETERS</span></span>

### <span data-ttu-id="6da31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da31-114">-DefaultProfile</span></span>
<span data-ttu-id="6da31-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6da31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6da31-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6da31-116">-ReservationOrderId</span></span>
<span data-ttu-id="6da31-117">使用者想要查看的特定預約訂單識別碼</span><span class="sxs-lookup"><span data-stu-id="6da31-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="6da31-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da31-118">CommonParameters</span></span>
<span data-ttu-id="6da31-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6da31-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da31-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6da31-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da31-121">輸入</span><span class="sxs-lookup"><span data-stu-id="6da31-121">INPUTS</span></span>

### <span data-ttu-id="6da31-122">沒有</span><span class="sxs-lookup"><span data-stu-id="6da31-122">None</span></span>

## <span data-ttu-id="6da31-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6da31-123">OUTPUTS</span></span>

### <span data-ttu-id="6da31-124">Microsoft.Azure.Commands.Reservations.models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="6da31-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="6da31-125">Microsoft.Azure.Commands.Reservations.models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="6da31-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="6da31-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6da31-126">NOTES</span></span>

## <span data-ttu-id="6da31-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6da31-127">RELATED LINKS</span></span>
