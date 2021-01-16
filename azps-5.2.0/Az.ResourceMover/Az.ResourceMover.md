---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281598"
---
# Az ResourceMover 模組
## 說明
Microsoft Azure PowerShell： ResourceMover Cmdlet

## Az ResourceMover Cmdlet
### [附加 AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
在移動集合中建立或更新移動資源。

### [AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
取得移動集合。

### [AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
取得移動資源。

### [AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
取得未解析的相依性清單。

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
提交要求內文中包含的一組資源。
在成功完成時，會在 moveState "CommitPending" 或 "CommitFailed" 的 moveResources 上觸發 commit 作業，moveResource moveState 執行轉換以進行確認。
若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
捨棄包含在要求主體中的資源集。
在成功完成時，會在 moveState "CommitPending" 或 "DiscardFailed" 的 moveResources 上觸發放棄作業，moveResource moveState 會轉換成 MovePending。
若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
移動包含在要求主體中的資源集。
在 moveResources 處於 moveState "MovePending" 或 "MoveFailed" 之後，就會觸發移動作業，moveResource moveState 會轉換成 CommitPending。
若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
開始準備包含在要求內文中的一組資源。
[準備] 作業是在 moveState "PreparePending" 或 "PrepareFailed" 中的 moveResources 上，在成功完成後，moveResource moveState 會轉換成 MovePending。
若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。

### [新-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
建立或更新移動收藏。

### [移除-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
刪除移動收藏。

### [移除-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
從移動收藏集中刪除移動資源。

### [解決-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
計算、解析並驗證移動集合中 moveResources 的相依性。

