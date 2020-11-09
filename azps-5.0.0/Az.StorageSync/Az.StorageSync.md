---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287692"
---
# Az StorageSync 模組
## 說明
[儲存同步處理] 模組中的 Cmdlet 可讓您管理有關 PowerShell 中 Azure 檔案同步處理的作業。

## Az StorageSync Cmdlet
### [AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
這個命令會列出指定同步群組中的所有雲端端點。

### [AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
這個命令會列出特定儲存同步處理服務中的所有同步處理群組。

### [AzStorageSyncServer](Get-AzStorageSyncServer.md)
這個命令會列出已登錄至特定儲存同步處理服務的所有伺服器。

### [AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
這個命令會列出指定同步群組中的所有伺服器端點。

### [AzStorageSyncService](Get-AzStorageSyncService.md)
這個命令會列出 [訂閱/資源群組] 的指定範圍內的所有儲存同步處理服務。

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
這個命令可以用來手動啟動命名空間變更的偵測。 您可以將它設定為整個共用、子資料夾或一組檔案的目標。 最多可以檢測到10000變更。 如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
這個命令會將所有的分層檔案撤回回本機磁片。

### [新-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
這個命令會在同步處理群組中建立 Azure 檔案同步處理雲端端點。

### [新-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。

### [新-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
這個命令會在已註冊的伺服器上建立新的伺服器端點。 這可讓伺服器上的指定路徑開始與同步群組中的其他端點同步處理檔案。

### [新-AzStorageSyncService](New-AzStorageSyncService.md)
這個命令會在資源群組中建立新的儲存同步處理服務。

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
這個命令會設定資源群組中的儲存同步處理服務。

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
這個命令會將伺服器註冊至儲存同步處理服務，這會建立信任關係。 然後，您可以使用 PowerShell 或 Azure 入口網站來設定此伺服器上的同步處理。

### [移除-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
這個命令會從同步處理群組中刪除指定的雲端端點。 若沒有至少一個雲端端點，此同步處理群組中則不能同步處理任何其他伺服器端點。

### [移除-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
這個命令會刪除指定的同步處理群組。

### [移除-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
這個命令會刪除指定的伺服器端點。 同步處理到這個位置將會立即停止。

### [移除-AzStorageSyncService](Remove-AzStorageSyncService.md)
這個命令會刪除指定的儲存同步處理服務。

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
僅用於疑難排解。 這個命令會將用來描述伺服器身分識別的儲存同步處理伺服器憑證滾到儲存同步處理服務。

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
這個命令可讓您變更伺服器端點的可調參數。

### [取消註冊-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
警告：取消註冊伺服器會導致層疊刪除此伺服器上的所有伺服器端點。 這個命令會從它的儲存同步處理服務登出伺服器。

