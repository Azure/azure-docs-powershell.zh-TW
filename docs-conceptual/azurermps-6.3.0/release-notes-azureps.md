---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237622"
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

---
## <a name="630---june-2018"></a>6.3.0 - 2018 年 6 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 已更新的 Enable-AzureRmContextAutoSave 錯誤訊息
* 執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容

#### <a name="azurestorage"></a>Azure.Storage
* 在說明檔中新增了關於 -Permissions 參數的其他資訊。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題 
* 更新 Compute 用戶端程式庫版本來修正下列 Cmdlet
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* 已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Policy Insights Cmdlet 的公開版本
    - 使用 API 版本 2018-04-04
    - 將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。 當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。

#### <a name="azurermsql"></a>AzureRM.Sql
* 說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings
* 'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數

## <a name="621---june-2018"></a>6.2.1 - 2018 年 6 月
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數

## <a name="620---june-2018"></a>6.2.0 - 2018 年 6 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS VM 更新功能
    - 新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet
    - 將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：
    - 新增設定中心存放庫的作業
    - 將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性
    - 更新從 SecretBase 到 Object 的數個模型類型
    - 新增 Blob 事件觸發程序

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 更新文件和範例輸出

### <a name="azurermnetwork"></a>AzureRM.Network
* 啟用網路監看員 Cmdlet 上的流量分析參數

#### <a name="azurermresources"></a>AzureRM.Resources
* 針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題

### <a name="azurermsql"></a>AzureRM.Sql
* 透過選擇性 LicenseType 參數更新下列 Cmdlet
    - New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。

## <a name="610---may-2018"></a>6.1.0 - 2018 年 5 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 啟用 AS 上的閘道建立關聯/取消關聯作業。

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援
* 已新增 ServiceFabric 後端支援
* 已新增 Application Insights 記錄器支援
* 已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援
* 已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援
* 已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援
* 已新增 MSI 身分識別支援
* 已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* 發行新的 Cmdlet Get-AzureBatchPoolNodeCounts
* 發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* 在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例
* 修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況 
* 修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔 

#### <a name="azurermnetwork"></a>AzureRM.Network
* 將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽
* 新增 Cmdlet 來建立通訊協定設定
    - New-AzureRmNetworkWatcherProtocolConfiguration
* 新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* 新增 Cmdlet 以將線路連線從現有的快速路由線路移除。
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* 新增 Cmdlet 來擷取線路連線
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* 已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups
* 已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。 請提交具有新彈性保留原則的要求。
* 更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。
* 更新的 Cmdlet 包括： 
    - New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。