---
Module Name: Az.RecoveryServices
Module Guid: 4aa53b7e-fcfe-4e22-979c-9a4e6380de58
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Az.RecoveryServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Az.RecoveryServices.md
ms.openlocfilehash: e0ba15abf2cbb660efef6ea401901bdcbd74900e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797050"
---
# Az RecoveryServices 模組
## 說明
本主題顯示 Azure 恢復服務 Cmdlet 的說明主題。

## Az RecoveryServices Cmdlet
### [附加 AzRecoveryServicesAsrReplicationProtectedItemDisk](Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md)
新增磁片以保護已受保護的 azure 虛擬機器。

### [備份-AzRecoveryServicesBackupItem](Backup-AzRecoveryServicesBackupItem.md)
啟動備份專案的備份。

### [Disable-AzRecoveryServicesBackupAutoProtection](Disable-AzRecoveryServicesBackupAutoProtection.md)
針對可保護的專案停用自動備份。

### [Disable-AzRecoveryServicesBackupProtection](Disable-AzRecoveryServicesBackupProtection.md)
針對受備份保護的專案停用保護。

### [Disable-AzRecoveryServicesBackupRPMountScript](Disable-AzRecoveryServicesBackupRPMountScript.md)
卸載復原點的所有檔案。

### [編輯-AzRecoveryServicesAsrRecoveryPlan](Edit-AzRecoveryServicesAsrRecoveryPlan.md)
編輯網站復原方案。

### [Enable-AzRecoveryServicesBackupAutoProtection](Enable-AzRecoveryServicesBackupAutoProtection.md)
這個命令可讓使用者自動保護所有現有未受保護的資料庫，以及稍後會以指定原則新增的任何 DB。 然後，Azure 備份服務會定期針對任何新的處理來掃描自動保護的容器，並自動保護它們。

### [Enable-AzRecoveryServicesBackupProtection](Enable-AzRecoveryServicesBackupProtection.md)
啟用具有指定備份保護原則之專案的備份。

### [AzRecoveryServicesAsrAlertSetting](Get-AzRecoveryServicesAsrAlertSetting.md)
取得保存庫的已設定 Azure 網站復原通知設定。

### [AzRecoveryServicesAsrEvent](Get-AzRecoveryServicesAsrEvent.md)
取得保存庫中 Azure Site Recovery 事件的詳細資料。

### [AzRecoveryServicesAsrFabric](Get-AzRecoveryServicesAsrFabric.md)
取得 Azure 網站恢復結構的詳細資料。

### [AzRecoveryServicesAsrJob](Get-AzRecoveryServicesAsrJob.md)
取得所指定 ASR 作業的詳細資料，或 [復原服務] 保存庫中最近的 ASR 作業清單。

### [AzRecoveryServicesAsrNetwork](Get-AzRecoveryServicesAsrNetwork.md)
取得目前電子倉庫的網站復原所管理網路的相關資訊。

### [AzRecoveryServicesAsrNetworkMapping](Get-AzRecoveryServicesAsrNetworkMapping.md)
取得目前電子倉庫之網站復原網路對應的相關資訊。

### [AzRecoveryServicesAsrPolicy](Get-AzRecoveryServicesAsrPolicy.md)
取得 ASR 複製原則。

### [AzRecoveryServicesAsrProtectableItem](Get-AzRecoveryServicesAsrProtectableItem.md)
在 ASR 保護容器中取得可保護的專案。

### [AzRecoveryServicesAsrProtectionContainer](Get-AzRecoveryServicesAsrProtectionContainer.md)
取得恢復服務電子倉庫中的 ASR 保護容器。

### [AzRecoveryServicesAsrProtectionContainerMapping](Get-AzRecoveryServicesAsrProtectionContainerMapping.md)
取得 Azure Site Recovery 保護容器對應。

### [AzRecoveryServicesAsrRecoveryPlan](Get-AzRecoveryServicesAsrRecoveryPlan.md)
在恢復服務保存庫中取得復原方案或所有復原方案

### [AzRecoveryServicesAsrRecoveryPoint](Get-AzRecoveryServicesAsrRecoveryPoint.md)
取得受複製受保護專案的可用復原點數。

### [AzRecoveryServicesAsrReplicationProtectedItem](Get-AzRecoveryServicesAsrReplicationProtectedItem.md)
取得 Azure 網站復原複製受保護專案的屬性。

### [AzRecoveryServicesAsrServicesProvider](Get-AzRecoveryServicesAsrServicesProvider.md)
取得已登錄至 [恢復服務] 保存庫的 ASR 恢復服務提供者詳細資料。

### [AzRecoveryServicesAsrStorageClassification](Get-AzRecoveryServicesAsrStorageClassification.md)
取得在復原服務電子倉庫中) ASR 儲存空間分類中發現的可用 (。

### [AzRecoveryServicesAsrStorageClassificationMapping](Get-AzRecoveryServicesAsrStorageClassificationMapping.md)
取得 ASR 儲存分類對應。

### [AzRecoveryServicesAsrVaultCoNtext](Get-AzRecoveryServicesAsrVaultContext.md)
取得恢復服務電子倉庫的 ASR vault 設定資訊。

### [AzRecoveryServicesAsrvCenter](Get-AzRecoveryServicesAsrvCenter.md)
取得在 ASR 結構指定之設定伺服器上登錄探索的 vCenter 伺服器詳細資料。

### [AzRecoveryServicesBackupContainer](Get-AzRecoveryServicesBackupContainer.md)
取得備份容器。

### [AzRecoveryServicesBackupItem](Get-AzRecoveryServicesBackupItem.md)
從 [備份] 中的容器取得專案。

### [AzRecoveryServicesBackupJob](Get-AzRecoveryServicesBackupJob.md)
取得備份作業。

### [AzRecoveryServicesBackupJobDetail](Get-AzRecoveryServicesBackupJobDetail.md)
取得備份作業的詳細資料。

### [AzRecoveryServicesBackupManagementServer](Get-AzRecoveryServicesBackupManagementServer.md)
取得 SCDPM 和 Azure 備份管理伺服器。

### [AzRecoveryServicesBackupProperty](Get-AzRecoveryServicesBackupProperty.md)
取得備份屬性。

### [AzRecoveryServicesBackupProtectableItem](Get-AzRecoveryServicesBackupProtectableItem.md)
這個命令會在特定的容器內，或跨所有已註冊的容器，檢索所有可保護的專案。 它將由應用程式階層的所有元素所組成。 傳回諸如 Instance、AvailabilityGroup 等的存儲和高層實體。

### [AzRecoveryServicesBackupProtectionPolicy](Get-AzRecoveryServicesBackupProtectionPolicy.md)
取得保存庫的備份保護原則。

### [AzRecoveryServicesBackupRecoveryLogChain](Get-AzRecoveryServicesBackupRecoveryLogChain.md)
這個命令會列出所指定備份專案的連續記錄鏈起點和終點。 使用它來判斷使用者想要還原資料庫的時間點是否有效或不正確。

### [AzRecoveryServicesBackupRecoveryPoint](Get-AzRecoveryServicesBackupRecoveryPoint.md)
取得已備份專案的復原點。

### [AzRecoveryServicesBackupRetentionPolicyObject](Get-AzRecoveryServicesBackupRetentionPolicyObject.md)
取得基本保留原則物件。

### [AzRecoveryServicesBackupRPMountScript](Get-AzRecoveryServicesBackupRPMountScript.md)
下載腳本以掛載復原點的所有檔案。

### [AzRecoveryServicesBackupSchedulePolicyObject](Get-AzRecoveryServicesBackupSchedulePolicyObject.md)
取得基本排程原則物件。

### [AzRecoveryServicesBackupStatus](Get-AzRecoveryServicesBackupStatus.md)
檢查您的 ARM 資源是否已備份。

### [AzRecoveryServicesBackupWorkloadRecoveryConfig](Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md)
這個命令會構造已備份專案（例如 SQL 資料庫）的恢復設定。 [設定] 物件會儲存所有詳細資料，例如 [還原] 模式、[還原] 和 [應用程式特定] 參數（例如 [SQL] 的目標實體路徑）。

### [AzRecoveryServicesVault](Get-AzRecoveryServicesVault.md)
取得恢復服務電子倉庫的清單。

### [AzRecoveryServicesVaultSettingsFile](Get-AzRecoveryServicesVaultSettingsFile.md)
取得 Azure Site Recovery 保存庫設定檔。

### [匯入-AzRecoveryServicesAsrVaultSettingsFile](Import-AzRecoveryServicesAsrVaultSettingsFile.md)
匯入指定的 ASR 電子倉庫設定檔案，以便在 PowerShell 會話中針對後續的 ASR 作業 (PowerShell 會話內容) 設定 vault 內容。 

### [Initialize-AzRecoveryServicesBackupProtectableItem](Initialize-AzRecoveryServicesBackupProtectableItem.md)
這個命令會在指定的容器中觸發發現指定工作負荷類型的任何未受保護專案。 如果資料庫應用程式不是自動受保護的，請使用此命令，在新資料庫新增後進行探索並繼續保護它們。

### [新-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig](New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md)
建立要複製之 Azure 虛擬機器磁片的磁片對應物件。

### [新-AzRecoveryServicesAsrFabric](New-AzRecoveryServicesAsrFabric.md)
建立 Azure Site Recovery 結構。

### [新-AzRecoveryServicesAsrInMageAzureV2DiskInput](New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md)
建立要複製之 vMWare 虛擬機器磁片的磁片對應物件。

### [新-AzRecoveryServicesAsrNetworkMapping](New-AzRecoveryServicesAsrNetworkMapping.md)
在兩個網路之間建立 ASR 網路對應。

### [新-AzRecoveryServicesAsrPolicy](New-AzRecoveryServicesAsrPolicy.md)
建立 Azure Site Recovery 複製原則。

### [新-AzRecoveryServicesAsrProtectableItem](New-AzRecoveryServicesAsrProtectableItem.md)
將 (探索) 物理伺服器新增至可保護的專案清單。

### [新-AzRecoveryServicesAsrProtectionContainer](New-AzRecoveryServicesAsrProtectionContainer.md)
在指定的結構中建立 Azure Site Recovery 保護容器。

### [新-AzRecoveryServicesAsrProtectionContainerMapping](New-AzRecoveryServicesAsrProtectionContainerMapping.md)
將指定的複製原則與指定的 ASR 保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。

### [新-AzRecoveryServicesAsrRecoveryPlan](New-AzRecoveryServicesAsrRecoveryPlan.md)
建立 ASR 恢復方案。

### [新-AzRecoveryServicesAsrReplicationProtectedItem](New-AzRecoveryServicesAsrReplicationProtectedItem.md)
透過建立受禁止複製的專案，為 ASR 可保護的專案啟用複製。

### [新-AzRecoveryServicesAsrStorageClassificationMapping](New-AzRecoveryServicesAsrStorageClassificationMapping.md)
在 [恢復服務] 保存庫中建立 ASR 儲存分類對應。

### [新-AzRecoveryServicesAsrvCenter](New-AzRecoveryServicesAsrvCenter.md)
新增 vCenter 伺服器以探索可保護的專案。

### [新-AzRecoveryServicesBackupProtectionPolicy](New-AzRecoveryServicesBackupProtectionPolicy.md)
建立備份保護原則。

### [新-AzRecoveryServicesVault](New-AzRecoveryServicesVault.md)
建立新的 [恢復服務] 保存庫。

### [Register-AzRecoveryServicesBackupContainer](Register-AzRecoveryServicesBackupContainer.md)
這個命令可讓 Azure Backup 將資源轉換成備份容器，然後再將登錄到指定的 [恢復服務] 保存庫。 然後，Azure 備份服務就可以在此容器中發現指定工作負荷類型的工作負荷，以備日後受到保護。

### [移除-AzRecoveryServicesAsrFabric](Remove-AzRecoveryServicesAsrFabric.md)
從 [恢復服務] 保存庫刪除指定的 Azure 網站復原結構。

### [移除-AzRecoveryServicesAsrNetworkMapping](Remove-AzRecoveryServicesAsrNetworkMapping.md)
從 [恢復服務] 保存庫刪除指定的 ASR 網路對應。

### [移除-AzRecoveryServicesAsrPolicy](Remove-AzRecoveryServicesAsrPolicy.md)
從 [恢復服務] 保存庫刪除指定的 ASR 複製原則。

### [移除-AzRecoveryServicesAsrProtectionContainer](Remove-AzRecoveryServicesAsrProtectionContainer.md)
從其結構中刪除指定的保護容器。

### [移除-AzRecoveryServicesAsrProtectionContainerMapping](Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
刪除指定的 Azure Site Recovery 防護容器對應。

### [移除-AzRecoveryServicesAsrRecoveryPlan](Remove-AzRecoveryServicesAsrRecoveryPlan.md)
從 [恢復服務] 保存庫刪除指定的 ASR 恢復方案。

### [移除-AzRecoveryServicesAsrReplicationProtectedItem](Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
停止/停用 Azure Site Recovery 複製受保護的專案的複製。

### [移除-AzRecoveryServicesAsrServicesProvider](Remove-AzRecoveryServicesAsrServicesProvider.md)
從 [恢復服務] 保存庫刪除/取消註冊指定的 Azure Site Recovery 復原服務提供者。

### [移除-AzRecoveryServicesAsrStorageClassificationMapping](Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
刪除指定的 ASR 儲存分類對應。

### [移除-AzRecoveryServicesAsrvCenter](Remove-AzRecoveryServicesAsrvCenter.md)
從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。

### [移除-AzRecoveryServicesBackupProtectionPolicy](Remove-AzRecoveryServicesBackupProtectionPolicy.md)
從保存庫刪除備份保護原則。

### [移除-AzRecoveryServicesVault](Remove-AzRecoveryServicesVault.md)
刪除恢復服務電子倉庫。

### [重新開機-AzRecoveryServicesAsrJob](Restart-AzRecoveryServicesAsrJob.md)
重新開機 Azure Site Recovery 作業。

### [Restore-AzRecoveryServicesBackupItem](Restore-AzRecoveryServicesBackupItem.md)
將備份專案的資料和設定還原到復原點。

### [Resume-AzRecoveryServicesAsrJob](Resume-AzRecoveryServicesAsrJob.md)
繼續已暫停的 Azure 網站還原作業。

### [Set-AzRecoveryServicesAsrAlertSetting](Set-AzRecoveryServicesAsrAlertSetting.md)
針對保存庫 (電子郵件通知) 設定 Azure 網站復原通知設定。

### [Set-AzRecoveryServicesAsrReplicationProtectedItem](Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
針對指定的複製受保護專案設定恢復屬性，例如目標網路和虛擬機器大小。

### [Set-AzRecoveryServicesAsrVaultCoNtext](Set-AzRecoveryServicesAsrVaultContext.md)
設定要用於在目前 PowerShell 會話中進行後續 Azure 網站恢復作業的復原服務電子倉庫內容。

### [Set-AzRecoveryServicesBackupProperty](Set-AzRecoveryServicesBackupProperty.md)
設定備份管理的屬性。

### [Set-AzRecoveryServicesBackupProtectionPolicy](Set-AzRecoveryServicesBackupProtectionPolicy.md)
修改備份保護原則。

### [Set-AzRecoveryServicesVaultCoNtext](Set-AzRecoveryServicesVaultContext.md)
設定電子倉庫內容。

### [開始-AzRecoveryServicesAsrApplyRecoveryPoint](Start-AzRecoveryServicesAsrApplyRecoveryPoint.md)
在提交容錯移轉作業之前，變更失敗的受保護專案的復原點。

### [開始-AzRecoveryServicesAsrCommitFailoverJob](Start-AzRecoveryServicesAsrCommitFailoverJob.md)
啟動針對網站復原物件的 [確認容錯移轉] 動作。

### [開始-AzRecoveryServicesAsrPlannedFailoverJob](Start-AzRecoveryServicesAsrPlannedFailoverJob.md)
啟動計畫的容錯移轉作業。

### [開始-AzRecoveryServicesAsrResynchronizeReplicationJob](Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md)
開始複製重新同步。

### [開始-AzRecoveryServicesAsrSwitchProcessServerJob](Start-AzRecoveryServicesAsrSwitchProcessServerJob.md)
將複製從一個進程伺服器切換到另一個處理，以進行負載平衡。

### [開始-AzRecoveryServicesAsrTestFailoverCleanupJob](Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md)
啟動測試容錯移轉清除操作。

### [開始-AzRecoveryServicesAsrTestFailoverJob](Start-AzRecoveryServicesAsrTestFailoverJob.md)
啟動測試容錯移轉作業。

### [開始-AzRecoveryServicesAsrUnplannedFailoverJob](Start-AzRecoveryServicesAsrUnplannedFailoverJob.md)
啟動未計畫的容錯移轉作業。

### [停止 AzRecoveryServicesAsrJob](Stop-AzRecoveryServicesAsrJob.md)
停止 Azure Site Recovery 作業。

### [停止 AzRecoveryServicesBackupJob](Stop-AzRecoveryServicesBackupJob.md)
取消正在執行的工作。

### [取消註冊-AzRecoveryServicesBackupContainer](Unregister-AzRecoveryServicesBackupContainer.md)
從保存庫登出 Windows Server 或其他容器。

### [取消註冊-AzRecoveryServicesBackupManagementServer](Unregister-AzRecoveryServicesBackupManagementServer.md)
從保存庫登出 SCDPM 服務器或備份伺服器。

### [更新-AzRecoveryServicesAsrMobilityService](Update-AzRecoveryServicesAsrMobilityService.md)
將行動服務代理程式更新推入受保護的電腦。

### [更新-AzRecoveryServicesAsrNetworkMapping](Update-AzRecoveryServicesAsrNetworkMapping.md)
更新指定的 azure site recovery 網路對應。

### [更新-AzRecoveryServicesAsrPolicy](Update-AzRecoveryServicesAsrPolicy.md)
更新 Azure 網站恢復複製原則。

### [更新-AzRecoveryServicesAsrProtectionContainerMapping](Update-AzRecoveryServicesAsrProtectionContainerMapping.md)
更新 Azure site recovery 防護容器對應。

### [更新-AzRecoveryServicesAsrProtectionDirection](Update-AzRecoveryServicesAsrProtectionDirection.md)
更新指定的複製受保護專案或復原方案的複製方向。 用來重新保護/反向複製失敗的複製專案或復原方案。

### [更新-AzRecoveryServicesAsrRecoveryPlan](Update-AzRecoveryServicesAsrRecoveryPlan.md)
更新 Azure 網站復原方案的內容。

### [更新-AzRecoveryServicesAsrServicesProvider](Update-AzRecoveryServicesAsrServicesProvider.md)
更新) 從 Azure Site Recovery 服務提供者收到的資訊， (重新整理伺服器。

### [更新-AzRecoveryServicesAsrvCenter](Update-AzRecoveryServicesAsrvCenter.md)
更新已註冊 vCenter 的探索詳細資料。

### [稍候-AzRecoveryServicesBackupJob](Wait-AzRecoveryServicesBackupJob.md)
等待備份作業完成。

