---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448577"
---
# <span data-ttu-id="a4cac-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a4cac-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="a4cac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4cac-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cac-103">取得適用識別碼的清單 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="a4cac-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4cac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4cac-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a4cac-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4cac-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cac-106">取得 `ReservationOrder` 可套用至此訂閱的適用應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4cac-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="a4cac-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4cac-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cac-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4cac-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="a4cac-109">適用于 `ReservationOrder` 預設訂閱</span><span class="sxs-lookup"><span data-stu-id="a4cac-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="a4cac-110">範例2</span><span class="sxs-lookup"><span data-stu-id="a4cac-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="a4cac-111">適用于 `ReservationOrder` 指定的訂閱</span><span class="sxs-lookup"><span data-stu-id="a4cac-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="a4cac-112">參數</span><span class="sxs-lookup"><span data-stu-id="a4cac-112">PARAMETERS</span></span>

### <span data-ttu-id="a4cac-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4cac-113">-SubscriptionId</span></span>
<span data-ttu-id="a4cac-114">取得已套用之訂閱的識別碼 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a4cac-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cac-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cac-115">CommonParameters</span></span>
<span data-ttu-id="a4cac-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4cac-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cac-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4cac-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cac-118">輸入</span><span class="sxs-lookup"><span data-stu-id="a4cac-118">INPUTS</span></span>

### <span data-ttu-id="a4cac-119">所有</span><span class="sxs-lookup"><span data-stu-id="a4cac-119">None</span></span>

## <span data-ttu-id="a4cac-120">輸出</span><span class="sxs-lookup"><span data-stu-id="a4cac-120">OUTPUTS</span></span>

### <span data-ttu-id="a4cac-121">PSAppliedReservationOrderId 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="a4cac-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="a4cac-122">筆記</span><span class="sxs-lookup"><span data-stu-id="a4cac-122">NOTES</span></span>

## <span data-ttu-id="a4cac-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4cac-123">RELATED LINKS</span></span>

