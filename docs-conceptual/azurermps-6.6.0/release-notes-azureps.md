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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368172"
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

---
## <a name="660---july-2018"></a>6.6.0 - 2018 年 7 月
#### <a name="general"></a>一般
* 已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。

#### <a name="azurermprofile"></a>AzureRM.Profile
* 已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。 預設一律為 True，個別資源並覆寫預設。
* 已將 ps1xml 類型新增至 Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* 支援從 DefaulfProfile 取得儲存體內容
* 將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6370
    - 已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6515
    - 已修正 File.Save 中的錯誤，不多載編碼類型
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6560
    - 已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況

#### <a name="azurermcompute"></a>AzureRM.Compute
* 修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。
* 修正 Invoke-AzureRmVMRunCommand Cmdlet
* 更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。  (ResouceGroupName 參數現在為選用。)
* 更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。
* 更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。
* 更新 New-AzureRmDisk 的範例
* 新增 'New-AzureRmVM' 的範例
* 更新 Set-AzureRmVMOSDisk 的說明
* 更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已將 ADF .Net SDK 版本更新為 1.1.0。
* 支援跨資料處理站的自我裝載整合執行階段共用。
     - 新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。
     - 將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線

#### <a name="azurerminsights"></a>AzureRM.Insights
* 已修正說明檔案中的 OutputType 格式
* 使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。

#### <a name="azurermresources"></a>AzureRM.Resources
* 修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題
    - https://github.com/Azure/azure-powershell/issues/6765
* 修正 'Set-AzureRmResource' 的管線狀況

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線
* 已修正一些問題
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* 透過下列 Cmdlet 新增伺服器進階威脅防護支援：
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* 透過下列 Cmdlet 新增弱點評量支援：
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* 已修正 Remove-AzureRmSqlServerFirewallRule 的範例
* 修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式

#### <a name="azurermstorage"></a>AzureRM.Storage
* 將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性
* 在資料表檢視中顯示 StorageAccount Cmdlet 輸出
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* 移除標籤 Cmdlet 說明中不正確的陳述式
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - 2018 年 7 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 已更新 'Get-AzureRmContextAutosaveSetting' 的說明

#### <a name="azurestorage"></a>Azure.Storage
* 支援使用唯寫 SAS 權杖上傳 Blob 或檔案
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 將必要屬性 ResourceGroupName 新增至 AS。

#### <a name="azurermautomation"></a>AzureRM.Automation
* 針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例

#### <a name="azurermcompute"></a>AzureRM.Compute
* 將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet
* 新增 'Add-AzureRmVmssExtension' 的範例
* 新增 'Remove-AzureRmVmssExtension' 的範例
* 更新 'Set-AzureRmVMAccessExtension' 的說明
* 針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤

#### <a name="azurermnetwork"></a>AzureRM.Network
* 針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連
* 已更新應用程式閘道的下列 Cmdlet
    - New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援
    - New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2
    - Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2
* 已使用最新的產生器版本重新產生 RouteTable Cmdlet

#### <a name="azurermrelay"></a>AzureRM.Relay
* 已更新 Markdown 檔案，修正範例中的參數名稱問題

#### <a name="azurermresources"></a>AzureRM.Resources
* 更新 Roleassignment 和 roledefinition Cmdlet：
    - 移除分頁時完成的額外 roledefinition 呼叫。
* 修正 Get-AzureRmRoleAssignment Cmdlet
    - 修正 -ExpandPrincipalGroups 命令參數功能
* 修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已將 top 和 skip 參數新增至清單 Cmdlet
* 已將標準新增至進階命名空間移轉 Cmdlet：
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* 已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 更新 'New-AzureRmServiceFabricCluster' 的範例

#### <a name="azurermsql"></a>AzureRM.Sql
* 新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* `Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。
* `Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新
* `Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本

## <a name="640---july-2018"></a>6.4.0 - 2018 年 7 月
#### <a name="general"></a>一般
* 已修正大部分模組說明檔案中的 OutputType 格式

#### <a name="azurermprofile"></a>AzureRM.Profile
* Ps1Xml 屬性已新增至基本輸出類型

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS 的 IP 標記功能
    - 已新增 'New-AzureRmVmssIpTagConfig' Cmdlet
    - IpTag 參數已新增至 New-AzureRmVmssIpConfig
* VMSS 的自動 OS 復原功能
    - DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss
* VMSS 的 OS 升級記錄功能
    - OSUpgradeHistory 參數已新增至 Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 透過下列命令，新增目錄 ACL 的支援：
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤
* 新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援
* 修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清
* 修正 DataLake Cmdlet 的測試位置

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup
* 已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。 提供預設參數集。
* 將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題

#### <a name="azurermnetwork"></a>AzureRM.Network
* 針對區域備援 VirtualNetworkGateways 公開新的 SKU
* 已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令
    - 已新增 Get-AzureRmExpressRouteCrossConnection
    - 已新增 Set-AzureRmExpressRouteCrossConnection
    - 已新增 Add-AzureRmExpressRouteCrossConnectionPeering
    - 已新增 Get-AzureRmExpressRouteCrossConnectionPeering
    - 已新增 Remove-AzureRmExpressRouteCrossConnectionPeering
    - 已新增 Get-AzureRMExpressRouteCrossConnectionArpTable
    - 已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable
    - 已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。 此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。 如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。

#### <a name="azurermresources"></a>AzureRM.Resources
* 更新 Get-AzureRmPolicyAssignment Cmdlet：
    - 在管理群組層級新增清單 -Scope 值的支援
    - 在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援
    - 將 -Effective 和 -All 參數新增至 control 參數
* 更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet
    - 新增 -ManagementGroupName 參數，以將作業套用至指定管理群組
    - 新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶
* 更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet
    - 新增 -ManagementGroupName 參數，以將作業套用至指定管理群組
    - 新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶
* 在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援
* 修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題
    - https://github.com/Azure/azure-powershell/issues/6505
* 修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。

#### <a name="azurermsql"></a>AzureRM.Sql
* 在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點
* 已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件

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