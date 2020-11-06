---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447270"
---
# <span data-ttu-id="deafe-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="deafe-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="deafe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="deafe-102">SYNOPSIS</span></span>
<span data-ttu-id="deafe-103">取得適用識別碼的清單 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="deafe-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deafe-104">句法</span><span class="sxs-lookup"><span data-stu-id="deafe-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="deafe-105">說明</span><span class="sxs-lookup"><span data-stu-id="deafe-105">DESCRIPTION</span></span>
<span data-ttu-id="deafe-106">取得 `ReservationOrder` 可套用至此訂閱的適用應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="deafe-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="deafe-107">示例</span><span class="sxs-lookup"><span data-stu-id="deafe-107">EXAMPLES</span></span>

### <span data-ttu-id="deafe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="deafe-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="deafe-109">適用于 `ReservationOrder` 預設訂閱</span><span class="sxs-lookup"><span data-stu-id="deafe-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="deafe-110">範例2</span><span class="sxs-lookup"><span data-stu-id="deafe-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="deafe-111">適用于 `ReservationOrder` 指定的訂閱</span><span class="sxs-lookup"><span data-stu-id="deafe-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="deafe-112">參數</span><span class="sxs-lookup"><span data-stu-id="deafe-112">PARAMETERS</span></span>

### <span data-ttu-id="deafe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deafe-113">-DefaultProfile</span></span>
<span data-ttu-id="deafe-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="deafe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deafe-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="deafe-115">-SubscriptionId</span></span>
<span data-ttu-id="deafe-116">取得已套用之訂閱的識別碼 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="deafe-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="deafe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deafe-117">CommonParameters</span></span>
<span data-ttu-id="deafe-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="deafe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deafe-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="deafe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deafe-120">輸入</span><span class="sxs-lookup"><span data-stu-id="deafe-120">INPUTS</span></span>

### <span data-ttu-id="deafe-121">所有</span><span class="sxs-lookup"><span data-stu-id="deafe-121">None</span></span>

## <span data-ttu-id="deafe-122">輸出</span><span class="sxs-lookup"><span data-stu-id="deafe-122">OUTPUTS</span></span>

### <span data-ttu-id="deafe-123">AppliedReservations 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="deafe-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="deafe-124">筆記</span><span class="sxs-lookup"><span data-stu-id="deafe-124">NOTES</span></span>

## <span data-ttu-id="deafe-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="deafe-125">RELATED LINKS</span></span>
