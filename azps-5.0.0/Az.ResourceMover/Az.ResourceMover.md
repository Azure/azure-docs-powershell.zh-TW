---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138994"
---
# <span data-ttu-id="c2877-101">Az ResourceMover 模組</span><span class="sxs-lookup"><span data-stu-id="c2877-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="c2877-102">說明</span><span class="sxs-lookup"><span data-stu-id="c2877-102">Description</span></span>
<span data-ttu-id="c2877-103">Microsoft Azure PowerShell： ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2877-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="c2877-104">Az ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2877-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="c2877-105">附加 AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c2877-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="c2877-106">在移動集合中建立或更新移動資源。</span><span class="sxs-lookup"><span data-stu-id="c2877-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="c2877-107">AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c2877-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="c2877-108">取得移動集合。</span><span class="sxs-lookup"><span data-stu-id="c2877-108">Gets the move collection.</span></span>

### [<span data-ttu-id="c2877-109">AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c2877-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="c2877-110">取得移動資源。</span><span class="sxs-lookup"><span data-stu-id="c2877-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="c2877-111">AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c2877-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="c2877-112">取得未解析的相依性清單。</span><span class="sxs-lookup"><span data-stu-id="c2877-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="c2877-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="c2877-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="c2877-114">提交要求內文中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="c2877-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="c2877-115">在成功完成時，會在 moveState "CommitPending" 或 "CommitFailed" 的 moveResources 上觸發 commit 作業，moveResource moveState 執行轉換以進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2877-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="c2877-116">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="c2877-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c2877-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="c2877-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="c2877-118">捨棄包含在要求主體中的資源集。</span><span class="sxs-lookup"><span data-stu-id="c2877-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="c2877-119">在成功完成時，會在 moveState "CommitPending" 或 "DiscardFailed" 的 moveResources 上觸發放棄作業，moveResource moveState 會轉換成 MovePending。</span><span class="sxs-lookup"><span data-stu-id="c2877-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="c2877-120">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="c2877-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c2877-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="c2877-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="c2877-122">移動包含在要求主體中的資源集。</span><span class="sxs-lookup"><span data-stu-id="c2877-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="c2877-123">在 moveResources 處於 moveState "MovePending" 或 "MoveFailed" 之後，就會觸發移動作業，moveResource moveState 會轉換成 CommitPending。</span><span class="sxs-lookup"><span data-stu-id="c2877-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="c2877-124">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="c2877-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c2877-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="c2877-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="c2877-126">開始準備包含在要求內文中的一組資源。</span><span class="sxs-lookup"><span data-stu-id="c2877-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="c2877-127">[準備] 作業是在 moveState "PreparePending" 或 "PrepareFailed" 中的 moveResources 上，在成功完成後，moveResource moveState 會轉換成 MovePending。</span><span class="sxs-lookup"><span data-stu-id="c2877-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="c2877-128">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="c2877-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="c2877-129">新-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c2877-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="c2877-130">建立或更新移動收藏。</span><span class="sxs-lookup"><span data-stu-id="c2877-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="c2877-131">移除-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c2877-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="c2877-132">刪除移動收藏。</span><span class="sxs-lookup"><span data-stu-id="c2877-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="c2877-133">移除-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c2877-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="c2877-134">從移動收藏集中刪除移動資源。</span><span class="sxs-lookup"><span data-stu-id="c2877-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="c2877-135">解決-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="c2877-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="c2877-136">計算、解析並驗證移動集合中 moveResources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="c2877-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>
