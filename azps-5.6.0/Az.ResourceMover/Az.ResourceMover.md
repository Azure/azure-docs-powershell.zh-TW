---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914466"
---
# <span data-ttu-id="3b23f-101">Az.ResourceMover 模組</span><span class="sxs-lookup"><span data-stu-id="3b23f-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="3b23f-102">描述</span><span class="sxs-lookup"><span data-stu-id="3b23f-102">Description</span></span>
<span data-ttu-id="3b23f-103">Microsoft Azure PowerShell：ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3b23f-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="3b23f-104">Az.ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3b23f-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="3b23f-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3b23f-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="3b23f-106">在移動集合中建立或更新移動資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="3b23f-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3b23f-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="3b23f-108">獲得移動集合。</span><span class="sxs-lookup"><span data-stu-id="3b23f-108">Gets the move collection.</span></span>

### [<span data-ttu-id="3b23f-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3b23f-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="3b23f-110">獲得移動資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="3b23f-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="3b23f-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="3b23f-112">需要 ARM 資源之移動資源的清單。</span><span class="sxs-lookup"><span data-stu-id="3b23f-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="3b23f-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="3b23f-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="3b23f-114">獲得無法解析的相依性清單。</span><span class="sxs-lookup"><span data-stu-id="3b23f-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="3b23f-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="3b23f-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="3b23f-116">移除移動集合中要求內建的一組移動資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="3b23f-117">這項功能是使用服務完成。</span><span class="sxs-lookup"><span data-stu-id="3b23f-117">The orchestration is done by service.</span></span>
<span data-ttu-id="3b23f-118">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="3b23f-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3b23f-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="3b23f-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="3b23f-120">承諾要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3b23f-121">在 moveState 'CommitPending' 或 'CommitFailed' 的 moveResources 上觸發該提交作業，在成功完成時，moveResource moveState 會進行移轉至已提交。</span><span class="sxs-lookup"><span data-stu-id="3b23f-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3b23f-122">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="3b23f-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3b23f-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="3b23f-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="3b23f-124">捨棄要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="3b23f-125">在 moveState 'CommitPending' 或 'DiscardFailed' 的 moveResources 上觸發捨棄作業，在成功完成 moveResource moveState 時，會執行移轉至 MovePending。</span><span class="sxs-lookup"><span data-stu-id="3b23f-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="3b23f-126">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="3b23f-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3b23f-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="3b23f-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="3b23f-128">移動要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="3b23f-129">移動作業是在 moveResources 位於 moveState 'MovePending' 或 'MoveFailed'之後觸發，在成功完成 moveResource moveState 時，會執行轉場至 CommitPending。</span><span class="sxs-lookup"><span data-stu-id="3b23f-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="3b23f-130">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="3b23f-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3b23f-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="3b23f-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="3b23f-132">初始化準備要求內建的一組資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="3b23f-133">準備作業是在 moveState 'PreparePending' 或 'PrepareFailed' 的 moveResources 上，在成功完成 moveResource moveState 時，執行移轉至 MovePending。</span><span class="sxs-lookup"><span data-stu-id="3b23f-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="3b23f-134">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="3b23f-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3b23f-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3b23f-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="3b23f-136">建立或更新移動集合。</span><span class="sxs-lookup"><span data-stu-id="3b23f-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="3b23f-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3b23f-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="3b23f-138">刪除移動集合。</span><span class="sxs-lookup"><span data-stu-id="3b23f-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="3b23f-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3b23f-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="3b23f-140">刪除移動集合中的移動資源。</span><span class="sxs-lookup"><span data-stu-id="3b23f-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="3b23f-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="3b23f-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="3b23f-142">計算、解決及驗證移動集合中 moveResources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="3b23f-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

