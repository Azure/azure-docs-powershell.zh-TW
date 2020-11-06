---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448580"
---
# <span data-ttu-id="ab568-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="ab568-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="ab568-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab568-102">SYNOPSIS</span></span>
<span data-ttu-id="ab568-103">獲取 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="ab568-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab568-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab568-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ab568-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab568-105">DESCRIPTION</span></span>
<span data-ttu-id="ab568-106">`ReservationOrder`使用者在目前租使用者中可存取的所有 s 的清單。</span><span class="sxs-lookup"><span data-stu-id="ab568-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="ab568-107">如果已設定 ReservationOrderId 參數，請取得該特定 ReservationOrder。</span><span class="sxs-lookup"><span data-stu-id="ab568-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="ab568-108">示例</span><span class="sxs-lookup"><span data-stu-id="ab568-108">EXAMPLES</span></span>

### <span data-ttu-id="ab568-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ab568-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="ab568-110">列出 `ReservationOrder` 使用者在目前租使用者中可存取的所有內容</span><span class="sxs-lookup"><span data-stu-id="ab568-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="ab568-111">範例2</span><span class="sxs-lookup"><span data-stu-id="ab568-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="ab568-112">取得 `ReservationOrder` 指定的 ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ab568-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="ab568-113">參數</span><span class="sxs-lookup"><span data-stu-id="ab568-113">PARAMETERS</span></span>

### <span data-ttu-id="ab568-114">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ab568-114">-ReservationOrderId</span></span>
<span data-ttu-id="ab568-115">使用者想要查看的特定 ReservationOrder 識別碼</span><span class="sxs-lookup"><span data-stu-id="ab568-115">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="ab568-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab568-116">CommonParameters</span></span>
<span data-ttu-id="ab568-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab568-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab568-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab568-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab568-119">輸入</span><span class="sxs-lookup"><span data-stu-id="ab568-119">INPUTS</span></span>

### <span data-ttu-id="ab568-120">所有</span><span class="sxs-lookup"><span data-stu-id="ab568-120">None</span></span>

## <span data-ttu-id="ab568-121">輸出</span><span class="sxs-lookup"><span data-stu-id="ab568-121">OUTPUTS</span></span>

### <span data-ttu-id="ab568-122">PSReservationOrderPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="ab568-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="ab568-123">PSReservationOrder 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="ab568-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="ab568-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ab568-124">NOTES</span></span>

## <span data-ttu-id="ab568-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab568-125">RELATED LINKS</span></span>

