---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907217"
---
# Az.StorageSync 模組
## 描述
儲存同步處理模組中的 Cmdlet 可啟用 PowerShell 中與 Azure 檔案同步處理相關的作業。

## Az.StorageSync Cmdlet
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
此命令會列出特定同步處理群組內的所有雲端端點。

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
此命令會列出給定儲存同步服務內的所有同步群組。

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
此命令會列出所有註冊至給定儲存同步處理服務的伺服器。

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
此命令會列出特定同步處理群組內的所有伺服器端點。

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
此命令會列出訂閱/資源群組範圍內的所有儲存同步服務。

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
此命令可用來手動啟動命名空間變更的偵測。 它可以鎖定至整個共用、子資料夾或一組檔案。 最多可偵測到 10，000 個變更。 如果您知道變更的範圍，將此命令的執行限制為命名空間的一部分，以便快速完成變更偵測，且在 10，000 個變更限制內完成。

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
檢查系統與 Azure 檔案同步處理之間潛在的相容性問題。

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
此命令會回收所有分層檔案回局磁片。

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
此命令在同步處理群組中建立 Azure 檔案同步處理雲端端點。

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
此命令會于指定的儲存同步服務中建立新同步組。

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
此命令在已登錄的伺服器上建立新伺服器端點。 這可讓伺服器上指定的路徑開始同步處理群組中與其他端點的檔案。

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
此命令在資源群組中建立新的儲存同步服務。

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
此命令會設定資源群組中的儲存空間同步服務。

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
此命令會註冊伺服器至儲存同步處理服務，服務會建立信任關係。 PowerShell 或 Azure 入口網站之後，就可以在此伺服器上設定同步處理。

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
此命令會從同步處理群組中刪除指定的雲端端點。 沒有至少一個雲端端點，此同步處理群組中沒有任何其他伺服器端點可以同步處理。

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
此命令將會刪除指定的同步組。

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
此命令將會刪除指定的伺服器端點。 同步處理到這個位置將會立即停止。

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
此命令將會刪除指定的儲存同步服務。

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
僅適用于疑難排解。 此命令會匯總儲存同步處理伺服器憑證，用來描述儲存空間同步處理服務的伺服器身分識別。

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
此命令允許變更伺服器端點的可調整參數。

### [取消註冊-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
警告：取消註冊伺服器會導致此伺服器上所有伺服器端點的串聯刪除。 此命令會從儲存同步處理服務取消註冊伺服器。

