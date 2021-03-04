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
# Az.ResourceMover 模組
## 描述
Microsoft Azure PowerShell：ResourceMover Cmdlet

## Az.ResourceMover Cmdlet
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
在移動集合中建立或更新移動資源。

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
獲得移動集合。

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
獲得移動資源。

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
需要 ARM 資源之移動資源的清單。

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
獲得無法解析的相依性清單。

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
移除移動集合中要求內建的一組移動資源。
這項功能是使用服務完成。
為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
承諾要求內內容中包含的一組資源。
在 moveState 'CommitPending' 或 'CommitFailed' 的 moveResources 上觸發該提交作業，在成功完成時，moveResource moveState 會進行移轉至已提交。
為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
捨棄要求內內容中包含的一組資源。
在 moveState 'CommitPending' 或 'DiscardFailed' 的 moveResources 上觸發捨棄作業，在成功完成 moveResource moveState 時，會執行移轉至 MovePending。
為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
移動要求內內容中包含的一組資源。
移動作業是在 moveResources 位於 moveState 'MovePending' 或 'MoveFailed'之後觸發，在成功完成 moveResource moveState 時，會執行轉場至 CommitPending。
為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
初始化準備要求內建的一組資源。
準備作業是在 moveState 'PreparePending' 或 'PrepareFailed' 的 moveResources 上，在成功完成 moveResource moveState 時，執行移轉至 MovePending。
為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
建立或更新移動集合。

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
刪除移動集合。

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
刪除移動集合中的移動資源。

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
計算、解決及驗證移動集合中 moveResources 的相依性。

