---
Module Name: AzureRM.Reservations
Module Guid: 43d3b085-6323-4ac4-a7c3-81d75ea036e5
Download Help Link: ''
Help Version: 1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/AzureRM.Reservations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/AzureRM.Reservations.md
ms.openlocfilehash: 10e22af397e5b5861eb9beb043e10abd04e08270
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442168"
---
# <span data-ttu-id="d8781-101">AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="d8781-101">AzureRM.Reservations Module</span></span>
## <span data-ttu-id="d8781-102">說明</span><span class="sxs-lookup"><span data-stu-id="d8781-102">Description</span></span>
<span data-ttu-id="d8781-103">本節中的主題會將 azure 資源管理器中的 azure 保留的 Azure PowerShell Cmdlet 檔 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="d8781-103">The topics in this section document the Azure PowerShell cmdlets for Azure Reservations in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="d8781-104">Cmdlet 會存在於 Microsoft Azure. 將命名空間保留在命令中。</span><span class="sxs-lookup"><span data-stu-id="d8781-104">The cmdlets exist in the Microsoft.Azure.Commands.Reservations namespace.</span></span>

## <span data-ttu-id="d8781-105">AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8781-105">AzureRM.Reservations Cmdlets</span></span>
### [<span data-ttu-id="d8781-106">AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d8781-106">Get-AzureRmReservation</span></span>](Get-AzureRmReservation.md)
<span data-ttu-id="d8781-107">`Reservation`以指定的預留順序取得 s</span><span class="sxs-lookup"><span data-stu-id="d8781-107">Get `Reservation`s in a given reservation Order</span></span>

### [<span data-ttu-id="d8781-108">AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="d8781-108">Get-AzureRmReservationCatalog</span></span>](Get-AzureRmReservationCatalog.md)
<span data-ttu-id="d8781-109">取得可用保留的目錄。</span><span class="sxs-lookup"><span data-stu-id="d8781-109">Get the catalog of available reservation.</span></span>

### [<span data-ttu-id="d8781-110">AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="d8781-110">Get-AzureRmReservationHistory</span></span>](Get-AzureRmReservationHistory.md)
<span data-ttu-id="d8781-111">取得的修訂歷程記錄 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="d8781-111">Get the revision history of a `Reservation`.</span></span>

### [<span data-ttu-id="d8781-112">AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d8781-112">Get-AzureRmReservationOrder</span></span>](Get-AzureRmReservationOrder.md)
<span data-ttu-id="d8781-113">取得 `ReservationOrder` 目前的租使用者。</span><span class="sxs-lookup"><span data-stu-id="d8781-113">Get `ReservationOrder` under current tenant.</span></span> <span data-ttu-id="d8781-114">如果提供了 [訂單識別碼]，則會檢索特定訂單。</span><span class="sxs-lookup"><span data-stu-id="d8781-114">If order id is provided, specific order is retrieved.</span></span>

### [<span data-ttu-id="d8781-115">AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d8781-115">Get-AzureRmReservationOrderId</span></span>](Get-AzureRmReservationOrderId.md)
<span data-ttu-id="d8781-116">取得 `ReservationOrder` 指定訂閱下的適用識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="d8781-116">Get list of applicable `ReservationOrder` Ids under given subscription.</span></span>

### [<span data-ttu-id="d8781-117">合併-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d8781-117">Merge-AzureRmReservation</span></span>](Merge-AzureRmReservation.md)
<span data-ttu-id="d8781-118">將兩個 `Reservation` s 合併成一個 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d8781-118">Merges two `Reservation`s into one `Reservation`</span></span>

### [<span data-ttu-id="d8781-119">分割-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d8781-119">Split-AzureRmReservation</span></span>](Split-AzureRmReservation.md)
<span data-ttu-id="d8781-120">將 a 分割 `Reservation` 成兩 `Reservation` 秒</span><span class="sxs-lookup"><span data-stu-id="d8781-120">Split a `Reservation` into two `Reservation`s</span></span>

### [<span data-ttu-id="d8781-121">更新-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d8781-121">Update-AzureRmReservation</span></span>](Update-AzureRmReservation.md)
<span data-ttu-id="d8781-122">更新已套用的範圍 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="d8781-122">Update the applied scope of a `Reservation`.</span></span>

