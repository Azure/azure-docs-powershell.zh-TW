---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620918"
---
# <span data-ttu-id="9f901-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9f901-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="9f901-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f901-102">SYNOPSIS</span></span>
<span data-ttu-id="9f901-103">取得適用識別碼的清單 `ReservationOrder` 。</span><span class="sxs-lookup"><span data-stu-id="9f901-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="9f901-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f901-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f901-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f901-105">DESCRIPTION</span></span>
<span data-ttu-id="9f901-106">取得 `ReservationOrder` 可套用至此訂閱的適用應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f901-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="9f901-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f901-107">EXAMPLES</span></span>

### <span data-ttu-id="9f901-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9f901-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="9f901-109">適用于 `ReservationOrder` 預設訂閱</span><span class="sxs-lookup"><span data-stu-id="9f901-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="9f901-110">範例2</span><span class="sxs-lookup"><span data-stu-id="9f901-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="9f901-111">適用于 `ReservationOrder` 指定的訂閱</span><span class="sxs-lookup"><span data-stu-id="9f901-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="9f901-112">參數</span><span class="sxs-lookup"><span data-stu-id="9f901-112">PARAMETERS</span></span>

### <span data-ttu-id="9f901-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f901-113">-DefaultProfile</span></span>
<span data-ttu-id="9f901-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f901-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f901-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f901-115">-SubscriptionId</span></span>
<span data-ttu-id="9f901-116">取得已套用之訂閱的識別碼 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="9f901-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="9f901-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f901-117">CommonParameters</span></span>
<span data-ttu-id="9f901-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f901-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f901-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f901-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f901-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9f901-120">INPUTS</span></span>

### <span data-ttu-id="9f901-121">所有</span><span class="sxs-lookup"><span data-stu-id="9f901-121">None</span></span>

## <span data-ttu-id="9f901-122">輸出</span><span class="sxs-lookup"><span data-stu-id="9f901-122">OUTPUTS</span></span>

### <span data-ttu-id="9f901-123">AppliedReservations 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="9f901-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="9f901-124">筆記</span><span class="sxs-lookup"><span data-stu-id="9f901-124">NOTES</span></span>

## <span data-ttu-id="9f901-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f901-125">RELATED LINKS</span></span>
