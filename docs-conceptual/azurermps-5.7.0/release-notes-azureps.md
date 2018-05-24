---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 8d96cae28a582f7c2dd74bae858f98a836c89cd2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

---

# <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Azure PowerShell 5.7.0 安裝程式：[連結](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

適用於 ARM Cmdlet 的資源庫模組：[連結](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

若要從 PowerShell 資源庫安裝 `AzureRM`，請執行以下命令：

```powershell
Install-Module -Name AzureRM -Repository PSGallery -Force
```

若要從舊版的 `AzureRM` 更新，請執行以下命令：

```powershell
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a>自上次發行後的變更

#### <a name="general"></a>一般
* 已更新至最新版本的 Azure ClientRuntime

#### <a name="azurestorage"></a>Azure.Storage
* 修正在啟用 FIPS 原則的電腦上無法上傳 Blob 和檔案 Cmdlet 的問題
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* 新 Cmdlet Get-AzureRmEnrollmentAccount
  - 擷取註冊帳戶的 Cmdlet

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 整合認知服務管理 SDK 4.0.0 版。
* 新增 Get-AzureRmCognitiveServicesAccountUsage 作業。

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus` 支援資料磁碟層級的加密狀態
* `Get-AzureRmVmssVmDiskEncryptionStatus` 支援資料磁碟層級的加密狀態
* 更新以進行區域復原
* 'New-AzureRmVm' 和 'New-AzureRmVmss' (簡單參數集全) 支援可用性區域。

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* 降低對 Commands.Resources.Rest 和 ARM/儲存體 SDK 的依賴。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 新增偵錯功能
* 將 ADLS dataplane SDK 的版本更新至 1.1.2
* Export-AzureRmDataLakeStoreItem - 已取代 PerFileThreadCount、ConcurrentFileCount 參數並導入了參數並行
* Import-AzureRMDataLakeStoreItem - 已取代 parametersPerFileThreadCount、ConcurrentFileCount 並導入了參數並行
* Get-AzureRMDataLakeStoreItemContent - 已修正內容大於 4MB 的結尾行為
* Set-AzureRMDataLakeStoreItemExpiry - 已導入新的參數集合 SetRelativeExpiry 以便設定相對的到期時間
* Remove-AzureRmDataLakeStoreItem - 已取代 Clean 參數。

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已修正 New-AzureRmEventHubGeoDRConfiguration 中的 AlternameName

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 已將 Cmdlet 更新為包含管線案例
* 在即將推出的重大變更版本中新增取代資訊

#### <a name="azurermnetwork"></a>AzureRM.Network
* 使用 Network Cmdlet 修正錯誤訊息

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已在規則的 CorrelationFilter 中新增「屬性」，以便支援 CustomProperties
* 已更新 New-AzureRmServiceBusGeoDRConfiguration 說明，並修正了規則 Cmdlet 輸出
* 已修正 New-AzureRmServiceBusQueue 和 New-AzureRmServiceBusSubscription Cmdlet 中的自動轉送屬性

#### <a name="azurermsql"></a>AzureRM.Sql
* 新增 Cmdlet 'Stop-AzureRmSqlElasticPoolActivity' 以支援在彈性集區中取消非同步作業
* 更新 Get-AzureRmSqlDatabaseActivity 和 Get-AzureRmSqlElasticPoolActivity Cmdlet 的回應，以在回應中反映更多資訊

自上次發行後的變更：https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 - 2018 年 3 月

#### <a name="general"></a>一般
* 修正 CloudShell 中的預設資源群組問題
* 修正在模組匯入期間執行不正確啟動指令碼的問題

#### <a name="azurermprofile"></a>AzureRM.Profile
* 在不支援的案例中啟用 MSI 驗證
* 新增使用者定義的受控服務識別支援

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 修正在組建中清理指令碼的問題

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 修正在組建中清理指令碼的問題

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVM' 和 'New-AzureRmVMSS' 支援資料磁碟機。
* 'New-AzureRmVM' 和 'New-AzureRmVMSS' 支援依名稱或識別碼的自訂映像。
* 記錄分析功能
    - 已新增 'Export-AzureRmLogAnalyticRequestRateByInterval' Cmdlet
    - 已新增 'Export-AzureRmLogAnalyticThrottledRequests' Cmdlet

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 修正登錄容器和 Azure 檔案磁碟區裝載的參數集問題

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已將 ADF .Net SDK 更新為版本 0.6.0-preview，包含以下變更：
    - 已新增新的 AzureDatabricks LinkedService 和 DatabricksNotebook 活動
    - 已在 HDInsightOnDemand LinkedService 中新增 headNodeSize 和 dataNodeSize 屬性
    - 已為 SalesforceMarketingCloud 新增 LinkedService、Dataset、CopySource
    - 已在所有活動上新增對 SecureOutput 的支援
    - 已在 ForEach 新增新的 BatchCount 屬性，可控制要執行的並行活動數量
    - 已新增新的篩選條件活動
    - 已新增連結服務參數的支援

#### <a name="azurermdns"></a>AzureRM.Dns
* 支援私人 DNS 區域 (公開預覽)
    - 新增建立只有相關的虛擬網路才能看見的 DNS 區域之功能

#### <a name="azurermnetwork"></a>AzureRM.Network
* 更新模型類型以與 DNS Cmdlet 相容。

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* ASR Azure 到 Azure Site Recovery 的變更 (Cmdlet 目前支援企業到企業、企業到 Azure、HyperV 到 Azure 以及 VMware 到 Azure 的作業)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* 在新的和設定的儲存體帳戶 Cmdlet 中淘汰下列參數：EnableEncryptionService 和 DisableEncryptionService，因為預設會啟用待用加密，且無法加以停用。
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已修正 Remove-AzureRmWebAppSlot 的說明

## <a name="550---march-2018"></a>5.5.0 - 2018 年 3 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 已修正匯入別名的問題
* 與版本 6.0.8 並行載入 Newtonsoft.Json 版本 10.0.3

#### <a name="azurestorage"></a>Azure.Storage
* 支援虛刪除功能
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 已修正匯入別名的問題
* 新增防火牆和查詢向外延展功能的支援，並支援 2017-08-01 API 版本。

#### <a name="azurermautomation"></a>AzureRM.Automation
* 已修正匯入別名的問題

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 已修正匯入別名的問題

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 更新 notice.txt 和通知訊息。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVMSS' 在詳細資訊模式中列印連接字串。
* 'New-AzureRmVmss' 支援公用 IP 位址、載入平衡規則、傳入的 NAT 規則。
* WriteAccelerator 功能
    - 已將 WriteAccelerator 切換參數新增至下列 Cmdlet：Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - 已將 OsDiskWriteAccelerator 切換參數新增至下列 Cmdlet：Set-AzureRmVmssStorageProfile。
    - 已將 OsDiskWriteAccelerator 布林值參數新增至下列 Cdlets：Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 修正會造成部分加密作業生產無意義錯誤的認證加密問題
* 啟用要在資料處理站間共用的整合執行階段

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 為 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd 新增參數 "SetupScriptContainerSasUri" 和 "Edition"，以啟用自訂設定和編輯選項功能
* 修正會造成部分加密作業生產無意義錯誤的認證加密問題。
* 啟用要在資料處理站間共用的整合執行階段

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 已修正匯入別名的問題

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 已修正 Set-AzureRmKeyVaultAccessPolicy 範例

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已修正匯入別名的問題

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 已修正匯入別名的問題

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 已修正匯入別名的問題

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 已修正匯入別名的問題

#### <a name="azurermresources"></a>AzureRM.Resources
* 已修正匯入別名的問題

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已將 EnableBatchedOperations 屬性新增至佇列
* 已將 DeadLetteringOnFilterEvaluationExceptions 屬性新增至訂用帳戶

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Service Fabric Cmdlet 重新整理
  - 已更新 ARM 範本
  - 不再復原失敗的作業
  - Add-AzureRmServiceFabricNodeType
    - VM 預設位於受控磁碟
    - 使用現有的 VMSS 子網路
    - 均為等冪作業
  - Remove-AzureRmServiceFabricNodeType 會清除所立的部分 VMSS 和/或叢集節點類型
  - 已修正複雜屬性類型的 PSCluster 物件輸出

#### <a name="azurermsql"></a>AzureRM.Sql
* 已修正匯入別名的問題
* Get-AzureRmSqlServer、New-AzureRmSqlServer 和 Remove-AzureRmSqlServer 回覆現在包括 FullyQualifiedDomainName 屬性。

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已修正匯入別名的問題
* New-AzureRMWebApp - 已新增參數集供建立簡化 WebApp 之用，搭配本機 GIT 存放庫支援。

## <a name="540---february-2018"></a>5.4.0 - 2018 年 2 月
#### <a name="azurermautomation"></a>AzureRM.Automation
* 將別名從 New-AzureRmAutomationModule 新增至 Import-AzureRmAutomationModule

#### <a name="azurermcompute"></a>AzureRM.Compute
* 修正某些 Get Cmdlet 的 ErrorAction 問題。

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 套用 Azure 容器執行個體 SDK 2018-02-01
    - 支援 DNS 名稱標籤

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 修正所有先前未正常運作的 GET Cmdlet。

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 修正 Get-AzureRmEventHubGeoDRConfiguration 說明中的錯誤

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已新增用來建立新連線監視的 Cmdlet
    - New-AzureRmNetworkWatcherConnectionMonitor
* 已新增用來更新連線監視的 Cmdlet
    - Set-AzureRmNetworkWatcherConnectionMonitor
* 已新增用來取得連線監視或連線監視清單的 Cmdlet
    - Get-AzureRmNetworkWatcherConnectionMonitor
* 已新增用來查詢連線監視的 Cmdlet
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* 已新增用來啟動連線監視的 Cmdlet
    - Start-AzureRmNetworkWatcherConnectionMonitor
* 已新增用來停止連線監視的 Cmdlet
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* 已新增用來移除連線監視的 Cmdlet
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* 已更新 Set-AzureRmApplicationGatewayBackendAddressPool 文件從而移除已淘汰的範例
* 已對應用程式閘道新增 EnableHttp2 旗標
    - 已更新 New-AzureRmApplicationGateway：已新增選擇性參數 -EnableHttp2
* 將 IpTags 新增至 PublicIpAddress
    - 已更新 New-AzureRmPublicIpAddress：已新增 IpTags
    - New-AzureRmPublicIpTag 以新增 Iptag
* 在 RouteTable 和 effectiveRoute 中新增 DisableBgpRoutePropagation 屬性。

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature：已在文件中新增遺漏的範例
* Register-AzureRmResourceProvider：已在文件中新增遺漏的範例

#### <a name="azurermstorage"></a>AzureRM.Storage
* 在新的和設定的儲存體帳戶 Cmdlet 中淘汰下列參數：EnableEncryptionService 和 DisableEncryptionService，因為預設會啟用待用加密，且無法加以停用。
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 - 2018 年 2 月
### <a name="azurermprofile"></a>AzureRM.Profile
* 已新增 PowerShell 3 和 4 的取代警告
* `Add-AzureRmAccount` 已重新命名為 `Connect-AzureRmAccount`；舊的 Cmdlet 名稱已新增別名，而其他別名 (`Login-AzAccount` 和 `Login-AzureRmAccount`) 已重新導向至新的 Cmdlet 名稱。
* `Remove-AzureRmAccount` 已重新命名為 `Disconnect-AzureRmAccount`；舊的 Cmdlet 名稱已新增別名，而其他別名 (`Logout-AzAccount` 和 `Logout-AzureRmAccount`) 已重新導向至新的 Cmdlet 名稱。
* 已更正資源字串使用 `Connect-AzureRmAccount`，而不是 `Login-AzureRmAccount`
* `Add-AzureRmEnvironment`和`Set-AzureRmEnvironment`
  - 已將 `-AzureOperationalInsightsEndpoint` 和 `-AzureOperationalInsightsEndpointResourceId`新增為參數，搭配 OperationalInsights 資料平面 RP 使用。

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`

### <a name="azurermcompute"></a>AzureRM.Compute
* 已將 `-AvailabilitySetName` 參數新增至簡化的 `New-AzureRmVM` 參數集。
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`
* 適用於 VM 和 VM 擴展集的使用者指派識別身分支援
    - 已將 `-IdentityType` 和 `-IdentityId` 參數新增至 `New-AzureRmVMConfig`、`New-AzureRmVmssConfig`、`Update-AzureRmVM` 和 `Update-AzureRmVmss`
* 在 `Add-AzureRmVmssNetworkInterfaceConfig` 中新增 `-EnableIPForwarding` 參數
* 在 `New-AzureRmVmssConfig` 中新增 `-Priority` 參數

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`
* 已更正執行此 Cmdlet 而不需要登入 `Login-AzureRmAccount` 時的 `Test-AzureRmDataLakeStoreAccount` 錯誤訊息

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 已更新使用 2018-01-01 API 版本。

### <a name="azurermeventhub"></a>AzureRM.EventHub

* 已新增下列異地災害復原作業的新命令。
  - 建立新的別名 (災害復原設定)：
    - `New-AzureRmEventHubGeoDRConfiguration`
  - 擷取別名 (災害復原設定)：
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - 停用災害復原，並停止將變更從主要命名空間複寫至次要命名空間
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - 叫用災害復原容錯移轉，並將別名重新設定為指向次要命名空間
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - 刪除別名 (災害復原設定)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* 已新增下列命令，用以檢查命名空間名稱和 GeoDr 設定名稱 - 別名可用性。
  - 檢查命名空間名稱或別名 (災害復原設定) 名稱的可用性：
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`

### <a name="azurermnetwork"></a>AzureRM.Network
* 修正覆寫訊息「您確定要覆寫來源嗎」

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 已新增透過 `Invoke-AzureRmOperationalInsightsQuery` 進行 V2 API 查詢的支援。 請參閱 [https://dev.loganalytics.io/](https://dev.loganalytics.io/) 以取得新 API 的詳細資訊。

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`：已將 `-ServicePrincipalName` 從預設的空參數集移除，因為它是多餘的 SPN 參數集

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* 已新增 `Remove-AzureRmServiceBusRule` 和 `Get-AzureRmServiceBusKey` 的功能修正
* 已新增下列異地災害復原作業的新 Commandlet。
  - 建立新的別名 (災害復原設定)：
    - `New-AzureRmServiceBusDRConfigurations`
  - 擷取別名 (災害復原設定)：
    - `Get-AzureRmServiceBusDRConfigurations`
  - 停用災害復原，並停止將變更從主要命名空間複寫至次要命名空間
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - 叫用災害復原容錯移轉，並將別名重新設定為指向次要命名空間
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - 刪除別名 (災害復原設定)
    - `Remove-AzureRmServiceBusDRConfigurations`
* 已更新 `Test-AzureRmServiceBusName` Commandlet 以支援異地災害復原 - 別名名稱檢查可用性作業。
  - 檢查命名空間名稱或別名 (災害復原設定) 名稱的可用性：
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* 已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`

## <a name="520---january-2018"></a>5.2.0 - 2018 年 1 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* Add-AzureRmAccount
  * 已新增 -MSI 登入，以便使用目前虛擬機器/服務的受管理服務身分識別之認證來進行驗證
  * 修正了以使用者所提供的存取權杖登入時，KeyVault 驗證所發生的問題

#### <a name="azurestorage"></a>Azure.Storage
* 新增用以取得和設定儲存體服務屬性的 Cmdlet
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmApiManagementProperty、Set-AzureRmApiManagementProperty 和 New-AzureRmApiManagement，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermautomation"></a>AzureRM.Automation
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 Set-AzureRmAutomationRunbook，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermbackup"></a>AzureRM.Backup
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermbatch"></a>AzureRM.Batch
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmCdnEndpoint 和 New-AzureRmCdnProfile，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 整合認知服務管理 SDK 3.0.0 版。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 已將簡化的參數新增到 New-AzureRmVmss，後者會使用智慧型預設值建立虛擬機器擴展集和所有必要的資源
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmVm 和 Update-AzureRmVm，已淘汰 -Tags 並改用 -Tag
* 修正了限制中包含區域時，Get-AzureRmComputeResourceSku Cmdlet 所發生的問題。
* 為了支援 Azure 監視器的接收，已更新診斷代理程式的設定結構描述。

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 已讓所有資料存放區所連結的服務都支援 Azure Key Vault
* 已新增 Azure SSIS 整合執行階段的授權類型屬性
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmDataFactory，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已讓所有資料存放區所連結的服務都支援 Azure Key Vault
* 已新增 Azure SSIS 整合執行階段的授權類型屬性
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 新增「Set-AzureRmDataFactoryV2IntegrationRuntime」cmd 的參數「LicenseType」以啟用 AHUB 功能

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 AzureRmDataLakeAnalyticsAccount 和 Set-AzureRmDataLakeAnalyticsAccount，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmDataLakeStoreAccount 和 Set-AzureRmDataLakeStoreAccount，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermdns"></a>AzureRM.Dns
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 已新增下列的新 Cmdlet：
  - Update-AzureRmEventGridSubscription
    - 更新 Event Grid 事件訂閱的屬性。
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurerminsights"></a>AzureRM.Insights
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermiothub"></a>AzureRM.IotHub
* 新增 IoTHub Cmdlet 的憑證支援
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 已針對長時間執行的 KeyVault Cmdlet 新增 -AsJob 支援。 允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。
  * 受影響的 Cmdlet 是：Remove-AzureRmKeyVault
* 修正了 Set-AzureRmKeyVaultAccessPolicy 中，AAD 篩選器會將 SPN 設為提供的 UPN 而非設定 UPN 本身的錯誤
  - 請參閱下列問題以取得更多資訊：https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 Update-AzureRmMlCommitmentPlan，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* 將 IncludeAllResources 參數新增到 Remove-AzureRmMlOpCluster Cmdlet
  - 使用此切換參數，將移除原本與叢集一起建立的所有資源
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermmedia"></a>AzureRM.Media
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 Set-AzureRmMediaService 和 New-AzureRmMediaService，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已針對長時間執行的 Network Cmdlet 新增 -AsJob 支援。 允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmNotificationHubsNamespace 和 Set-AzureRmNotificationHubsNamespace，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmOperationalInsightsSavedSearch、Set-AzureRmOperationalInsightsSavedSearch、New-AzureRmOperationalInsightsWorkspace 和 Set-AzureRmOperationalInsightsWorkspace，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 已將 -UseOriginalStorageAccount 選項新增到 Restore-AzureRmRecoveryServicesBackupItem Cmdlet。
  - 啟用此旗標會將磁碟還原到原始的儲存體帳戶，這可讓使用者將所還原虛擬機器的設定，盡可能重設回原始虛擬機器的設定。
  - 這也有助於改善還原作業的效能。

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 已新增 3 個防火牆規則的新 Cmdlet
* 已新增 3 個異地複寫的新 Cmdlet
* 已新增區域和標籤的支援
* 盡可能將 ResourceGroup 設為選用。

#### <a name="azurermrelay"></a>AzureRM.Relay
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermresources"></a>AzureRM.Resources
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 已針對長時間執行的 Resources Cmdlet 新增 -AsJob 支援。 允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。
* 已從 Get-AzureRmProviderOperation 新增別名到 Get-AzureRmResourceProviderAction 以符合命名慣例

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 針對 New-AzureRmServerManagementNode 和 New-AzureRmServerManagementGateway，已淘汰 -Tags 並改用 -Tag

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermsql"></a>AzureRM.Sql
* 更新 Auditing 命令參數描述
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 已將 -AsJob 參數新增到長時間執行的 Cmdlet
* 已從 Get-AzureRmSqlServiceObjective 中淘汰了 -DatabaseName 參數

#### <a name="azurermstorage"></a>AzureRM.Storage
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 修正了以參數 -EnableEncryptionService None 執行 Cmdlet New-AzureRMStorageAccount 時，所發生的 null 參考問題
* 已針對長時間執行的 Storage Cmdlet 新增 -AsJob 支援。 允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。
    - 受影響的 Cmdlet 是適用於儲存體帳戶和儲存體帳戶網路規則的 New-、Remove-、Add- 和 Update-。

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成
* 已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成
* 已針對長時間執行的 Websites Cmdlet 新增 -AsJob 支援。 允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。
     - WebApps、AppServicePlan 和 Slots中，受影響的 Cmdlet 是 New-、Remove-、Add- 和 Set-

## <a name="2017128-version-511"></a>2017.12.8 版本 5.1.1
* AnalysisServices
  - 將位置的驗證集變更為動態對應，以便支援所有雲端。
* 自動化
  - 更新至 Import-AzureRMAutomationRunbook
    - 現在可支援 Python2 Runbook
* Batch
  - 修正錯誤：不含資源群組的帳戶作業無法自動偵測資源群組
* 計算
  - Get-AzureRmComputeResourceSku 會顯示區域資訊。
  - 更新 Disable-AzureRmVmssDiskEncryption 以修正問題 https://github.com/Azure/azure-powershell/issues/5038
  - 針對長時間執行的計算 Cmdlet 新增 -AsJob 支援。 允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。
    - 受影響的 Cmdlet 包括：適用於虛擬機器和虛擬機器擴展集的 New-、Update-、Set-、Remove-、Start-、Restart- 和 Stop- Cmdlet
    - 將簡化的參數集新增至 New-AzureRmVM，New-AzureRmVM 可使用智慧型預設值建立虛擬機器和所有必要的資源
* ContainerInstance
  - 套用 Azure 容器執行個體 SDK 2017-10-01
    - 支援容器的「執行到完成」作業
    - 支援 Azure 檔案磁碟區掛接
    - 支援開啟多個公用 IP 的連接埠
* ContainerRegistry
  - 新增異地複寫與 Webhook 的 Cmdlet
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - 認證加密功能現在可與啟用的「遠端存取」(透過網路) 和停用的「遠端存取」(本機電腦) 搭配使用。
* DataFactoryV2
  - 新增兩個 Cmdlet：Update-AzureRmDataFactoryV2 和 Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - 將名為 ScriptParameter 的參數新增至 Submit-AzureRmDataLakeAnalyticsJob
    - 可在 Submit-AzureRmDataLakeAnalyticsJob 上使用 Get-help 找到 ScriptParameter 的詳細資訊
  - 針對 New-AzureRmDataLakeAnalyticsAccount，已將參數 MaxDegreeOfParallelism 變更為 MaxAnalyticsUnits
    - 新增參數 MaxAnalyticsUnits 的別名：MaxDegreeOfParallelism
  - 針對 New-AzureRmDataLakeAnalyticsComputePolicy，已將參數 MaxDegreeOfParallelismPerJob 變更為 MaxAnalyticsUnitsPerJob
    - 新增參數 MaxAnalyticsUnitsPerJob 的別名：MaxDegreeOfParallelismPerJob
  - 針對 Set-AzureRmDataLakeAnalyticsAccount，已將參數 MaxDegreeOfParallelism 變更為 MaxAnalyticsUnits
    - 新增參數 MaxAnalyticsUnits 的別名：MaxDegreeOfParallelism
  - 針對 Submit-AzureRmDataLakeAnalyticsJob，已將參數 DegreeOfParallelism 變更為 AnalyticsUnits
    - 新增參數 AnalyticsUnits 的別名：DegreeOfParallelism
  - 針對 Update-AzureRmDataLakeAnalyticsComputePolicy，已將參數 MaxDegreeOfParallelismPerJob 變更為 MaxAnalyticsUnitsPerJob
    - 新增參數 MaxAnalyticsUnitsPerJob 的別名：MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - 新增 Set-AzureRmMlOpCluster
    - 更新叢集的代理程式計數或 SSL 設定
  - 協調器屬性是選擇性項目
    - 服務會建立服務主體 (如果未提供的話)，因此協調器屬性現在是選擇性項目
* PowerBIEmbedded
  - 新增 Power BI Embedded 容量 Cmdlet 的支援
  - 新增 Get-AzureRmPowerBIEmbeddedCapacity Cmdlet - 取得 PowerBI Embedded 容量的詳細資料。
  - 新增 New-AzureRmPowerBIEmbeddedCapacity Cmdlet - 建立新的 PowerBI Embedded 容量
  - 新增 Remove-AzureRmPowerBIEmbeddedCapacity Cmdlet - 刪除 PowerBI Embedded 容量的執行個體
  - 新增 Resume-AzureRmPowerBIEmbeddedCapacity Cmdlet - 恢復 PowerBI Embedded 容量的執行個體
  - 新增 Suspend-AzureRmPowerBIEmbeddedCapacity Cmdlet - 暫止 PowerBI Embedded 容量的執行個體
  - 新增 Test-AzureRmPowerBIEmbeddedCapacity Cmdlet - 測試 PowerBI Embedded 容量執行個體是否存在
  - 新增 Update-AzureRmPowerBIEmbeddedCapacity Cmdlet - 修改 PowerBI Embedded 容量的執行個體
* 設定檔
  - 已將 USGovernmentActiveDirectoryEndpoint 更新為 https://login.microsoftonline.us/
    - 如需更多關於 Azure Government 端點對應的資訊，請參閱以下文章：https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - 新增 Cmdlet 的 -AsJob 支援，讓選取的 Cmdlet 可在背景中執行並傳回作業以追蹤和控制進度
    - 將 -AsJob 參數新增至 Get-AzureRmSubscription Cmdlet
* RecoveryServices.Backup
  - 修正錯誤：Get-AzureRmRecoveryServicesBackupItem 應針對容器名稱的篩選，執行不區分大小寫的比較。
  - 修正錯誤：AzureVmItem 現在有屬性可顯示最後一次發生備份作業的時間 (LastBackupTime)。
* 資源
  - 修正問題：Get-AzureRMRoleAssignment 產生的指派結果沒有自訂角色的角色定義名稱
    - 使用者現在使用 Get-AzureRMRoleAssignment 產生的指派，會具有任何角色類型的角色定義名稱
  - 修正問題：當可指派的範圍內有新範圍時，Set-AzureRMRoleRoleDefinition 會用來擲回找不到 RD 的錯誤
    - 使用者現在能在可指派的範圍內有新範圍時，使用 Set-AzureRMRoleRoleDefinition，且不受限於範圍的位置
  - 允許範圍以 "/" 結尾
    - 使用者現在可以使用範圍結尾為 "/" 的 RoleDefinition 和 RoleAssignment Commandlet (與 API 和 CLI 一致)
  - 允許使用者使用委派旗標建立 RoleAssignment
    - 使用者現在可以使用具有新增委派旗標選項的 New-AzureRMRoleAssignment
  - 修正 RoleAssignment 以遵守範圍參數
  - 在 New-AzureRmRoleAssignment Commandlet 中新增 ServicePrincipalName 的別名
    - 使用者現在使用 New-AzureRmRoleAssignment Commandlet 時，可使用 ApplicationId 而不是 ServicePrincipalName
* SiteRecovery
  - 針對此模組中的所有 Cmdlet 新增取代警告，為下一次的重大變更發行做好準備。
    - 請參閱即將發行的重大變更指南，以了解如何從 AzureRM 移轉您的 Cmdlet。
* Sql
  - 新增使用 Set-AzureRmSqlDatabase 重新命名資料庫的功能
  - 已修正的問題 https://github.com/Azure/azure-powershell/issues/4974
    - 對稽核 Cmdlet 提供無效的 AUDIT_CHANGED_GROUP 值不會再擲回錯誤，並且將在近期版本中移除。
  - 已修正的問題 https://github.com/Azure/azure-powershell/issues/5046
    - 稽核 Cmdlet 中的 AuditAction 參數不再遭到忽略
  - 修正在稽核 Cmdlet 中提供 'Secondary' StorageKeyType 時的問題
    - 在設定 Blob 稽核時，針對 StorageKeyType 參數提供 'Secondary' 值時，系統使用的不是次要金鑰，而是主要儲存體帳戶金鑰。
  - 變更 Set-AzureRmSqlServerTransparentDataEncryptionProtector 中的確認訊息文字
* Azure (RDFE)
    - 移除所有 RemoteApp Cmdlet
* Azure.Storage
    - 升級至 Azure 儲存體用戶端程式庫 8.6.0 及 Azure 儲存體資料移動程式庫 0.6.5

## <a name="20171110-version-501"></a>2017.11.10 版本 5.0.1
* 固定組件載入問題造成在下列模組中執行 Cmdlet 時失敗：
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017.11.8 - 版本 5.0.0
* 注意：這是重大變更版本。 有關導入的重大變更完整清單，請參閱移轉指南 (https://aka.ms/azps-migration-guide)。
* AzureRM 中所有的 Cmdlet 現在都支援線上說明
  - 執行 Get-Help 搭配 -Online 參數，以在您的預設網際網路瀏覽器中開啟線上說明
* AnalysisServices
  * 固定的 Synchronize-AzureAsInstance 命令搭配使用新 AsAzure REST API 以進行同步處理
* ApiManagement
  * 有關 ApiManagement 在這一版所做的重大變更，請參閱移轉指南
  * 已更新 Cmdlet Get-AzureRmApiManagementUser 以修正問題 https://github.com/Azure/azure-powershell/issues/4510
  * 已更新 Cmdlet New-AzureRmApiManagementApi 以建立具備 Empty Path 的 API https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
  * 新增命令以取得/建立/移除應用程式深入解析資源
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * 新增命令以取得/更新價格/應用程式深入解析資源的每日上限
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * 新增命令以取得/建立/更新/移除應用程式深入解析資源的連續匯出
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * 新增命令以取得/建立/移除應用程式深入解析資源的 API 金鑰
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * 將新參數新增至 `New-AzureRmBatchAccount`。
    - `PoolAllocationMode`：在 Batch 帳戶中建立集區所使用的配置模式。 若要在使用者的訂用帳戶中建立配置集區節點的 Batch 帳戶，請將此設為 `UserSubscription`。
    - `KeyVaultId`：與 Batch 帳戶相關的 Azure 金鑰保存庫之資源識別碼。
    - `KeyVaultUrl`：與 Batch 帳戶相關的 Azure 金鑰保存庫之 URL。
  * 將參數更新為 `New-AzureBatchTask`。
    - 移除 `RunElevated` 參數。 已新增 `UserIdentity` 參數來取代 `RunElevated`，且對等的行為可藉由建構 `PSUserIdentity` 來達成，如下所示：
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - 新增 `AuthenticationTokenSettings` 參數。 這個參數可讓您要求 Batch 服務在執行時向工作提供驗證權杖，而不必先將 Batch 帳戶金鑰傳遞至工作，才能對 Batch 服務發出要求。
    - 新增 `ContainerSettings` 參數。
      - 這個參數可讓您要求 Batch 服務在容器內執行工作。
    - 新增 `OutputFiles` 參數。
      - 這個參數可讓您設定在工作完成之後將檔案上傳至 Azure 儲存體。
  * 將參數更新為 `New-AzureBatchPool`。
    - 新增 `UserAccounts` 參數。
      - 這個參數可定義集區中每個節點上所建立的使用者帳戶。
    - 新增 `TargetLowPriorityComputeNodes` 並將 `TargetDedicated` 重新命名為 `TargetDedicatedComputeNodes`。
      - 針對 `TargetDedicatedComputeNodes` 參數已建立 `TargetDedicated` 別名。
    - 新增 `NetworkConfiguration` 參數。
      - 這個參數可讓您設定集區的網路設定。
  * 將參數更新為 `New-AzureBatchCertificate`。
    - `Password` 參數現在是 `SecureString`。
  * 將參數更新為 `New-AzureBatchComputeNodeUser`。
    - `Password` 參數現在是 `SecureString`。
  * 將參數更新為 `Set-AzureBatchComputeNodeUser`。
    - `Password` 參數現在是 `SecureString`。
  * 在 `Get-AzureBatchNodeFile`、`Get-AzureBatchNodeFileContent` 和 `Remove-AzureBatchNodeFile` 上將 `Name` 參數重新命名為 `Path`。
    - 針對 `Path` 參數已建立 `Name` 別名。
  * 物件的變更
    - 請參閱 Batch 變更記錄取得完整清單
  * 新增 Azure Active Directory 型驗證支援。
    - 若要使用 Azure Active Directory 驗證，請使用 `Get-AzureRmBatchAccount` Cmdlet 擷取 `BatchAccountContext` 物件，並將此 `BatchAccountContext` 提供至 Batch 服務 Cmdlet 的 `-BatchContext` 參數。 對於具有 `PoolAllocationMode = UserSubscription` 的帳戶，Azure Active Directory 驗證為必要。
    - 對於現有帳戶或以 `PoolAllocationMode = BatchService` 建立的新帳戶，您可以藉由使用 `Get-AzureRmBatchAccoutKeys` Cmdlet 擷取 `BatchAccountContext` 物件，繼續使用共用金鑰驗證。
* 計算
  * Azure 磁碟加密延伸模組命令
    - 'Set-AzureRmVmDiskEncryptionExtension' 的新參數：'-EncryptFormatAll' 加密格式資料磁碟
    - 'Set-AzureRmVmDiskEncryptionExtension' 的新參數：'-ExtensionPublisherName' 和 '-ExtensionType' 允許切換至延伸模組的其他版本
    - 'Disable-AzureRmVmDiskEncryption' 的新參數：'-ExtensionPublisherName' 和 '-ExtensionType' 允許切換至延伸模組的其他版本
    - 'Get-AzureRmVmDiskEncryptionStatus' 的新參數：'-ExtensionPublisherName' 和 '-ExtensionType' 允許切換至延伸模組的其他版本
* DataLakeAnalytics
  * 有關 DataLakeAnalytics 在這一版所做的重大變更，請參閱移轉指南
  * 變更 Get-AzureRmDataLakeAnalyticsAccount 兩種 OutputTypes 的其中一種
    - List\<DataLakeAnalyticsAccount> 到 List\<PSDataLakeAnalyticsAccountBasic>
    - PSDataLakeAnalyticsAccountBasic 的屬性是 DataLakeAnalyticsAccount 屬性的 strict 子集
    - 服務不會傳回 DataLakeAnalyticsAccount 中的其他屬性。  因此，這項變更是為了準確反映此情況。 這些額外屬性仍然在 PSDataLakeAnalyticsAccountBasic 中，但被標記為 [已淘汰]。
  * 變更 Get-AzureRmDataLakeAnalyticsJob 兩種 OutputTypes 的其中一種
    - List\<JobInformation> 到 List\<PSJobInformationBasic>
    - PSJobInformationBasic 的屬性是 JobInformation 屬性的 strict 子集
    - 服務不會傳回 JobInformation 中的其他屬性。  因此，這項變更是為了準確反映此情況。 這些額外屬性仍然在 PSJobInformationBasic 中，但被標記為 [已淘汰]。
* DataLakeStore
  * 有關 DataLakeStore 在這一版所做的重大變更，請參閱移轉指南
  * 變更 Get-AzureRmDataLakeStoreAccount 兩種 OutputTypes 的其中一種
    - List\<PSDataLakeStoreAccount> 到 List\<PSDataLakeStoreAccountBasic>
    - PSDataLakeStoreAccountBasic 的屬性是 PSDataLakeStoreAccount 屬性的 strict 子集
    - 服務不會傳回 PSDataLakeStoreAccount 中的其他屬性。  因此，這項變更是為了準確反映此情況。 這些額外屬性仍然在 PSDataLakeStoreAccountBasic 中，但被標記為 [已淘汰]。
* Dns
  * Azure DNS 中 CAA 記錄型別的支援
    - 支援 CAA 記錄型別上的所有作業
* EventHub
  * 有關 EventHub 在這一版所做的重大變更，請參閱移轉指南
* 深入解析
  * 有關深入解析在這一版所做的重大變更，請參閱移轉指南
* 網路
  * 有關網路在這一版所做的重大變更，請參閱移轉指南
  * 新增 Cmdlet 以針對指定的 Azure 區域列出可用的網際網路服務提供者
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * 新增 Cmdlet 以取得從指定位置到 Azure 區域的網際網路服務提供者相對延遲分數
    - Get-AzureRmNetworkWatcherReachabilityReport
* 設定檔
  - Set-AzureRmDefault
    - 使用這個 Cmdlet 設定預設的資源群組。  對於某些 Cmdlet，這會讓 -ResourceGroup 參數成為選用，且在未指定資源群組時將使用預設值
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - 如果指定的資源群組存在於訂用帳戶中，則此資源群組將會設為預設值。  否則，將會建立該資源群組，並將其設為預設值。
  - Get-AzureRmDefault
    - 使用這個 Cmdlet 取得目前預設的資源群組 (和未來其他的預設)。
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - 使用這個 Cmdlet 移除目前預設的資源群組
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment 和 Set-AzureRmEnvironment
    - 新增 BatchAudience 參數，可讓您指定在取得 Batch 服務驗證權杖時所要使用的 Azure Batch Active Directory 對象。
* RecoveryServices.Backup
  * 新增 Cmdlet 以執行立即檔案復原。
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * 將 RecoveryServices.Backup SDK 更新至最新版本
  * 更新 Azure VM 工作負載的測試，如此一來測試回合所需的所有設定便由測試本身完成。
  * 修正 https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
  * ASR VMware 到 Azure Site Recovery 的變更 (Cmdlet 目前支援企業到企業、企業到 Azure、HyperV 到 Azure 的作業)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * 新增以 AAD 為基礎的保存庫支援
  * 新增 Cmdlet 以管理 VCenter 資源
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * 新增其他 Cmdlet
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - 有關 ServiceBus 在這一版所做的重大變更，請參閱移轉指南
* Sql
  * 新增對列出和取消資料庫上非同步 updateslo 作業的支援
    - 更新現有的 Cmdlet Get-AzureRmSqlDatabaseActivity 以傳回 DB updateslo 作業狀態。
    - 新增新的 Cmdlet Stop-AzureRmSqlDatabaseActivity 以取消資料庫上的非同步 updateslo 作業。
  * 新增對資料庫和彈性集區的區域備援支援
    - 將 ZoneRedundant 切換參數新增至 New-AzureRmSqlDatabase
    - 將 ZoneRedundant 切換參數新增至 Set-AzureRmSqlDatabase
    - 將 ZoneRedundant 切換參數新增至 New-AzureRmSqlElasticPool
    - 將 ZoneRedundant 切換參數新增至 Set-AzureRmSqlElasticPool
  * 新增對伺服器 DNS 別名的支援
    - 新增 Get-AzureRmSqlServerDnsAlias Cmdlet，其可按照伺服器和別名名稱取得伺服器 dns 別名，或 Azure Sql Server 的伺服器 dns 別名清單。
    - 新增 New-AzureRmSqlServerDnsAlias Cmdlet，其可建立指定的 Azure Sql 伺服器的新伺服器 dns 別名
    - 新增 Set-AzurermSqlServerDnsAlias Cmdlet，其可讓伺服器 dns 別名指向的 Azure Sql Server 進行更新
    - 新增 Remove-AzureRmSqlServerDnsAlias Cmdlet，其可移除 Azure Sql 伺服器的伺服器 dns 別名
* Azure.Storage
  * 升級至 Azure 儲存體用戶端程式庫 8.5.0 及 Azure 儲存體資料移動程式庫 0.6.3
  * 新增檔案共用快照集支援功能
    - 將 'SnapshotTime' 參數新增至 Get-AzureStorageShare
    - 將 'IncludeAllSnapshot' 參數新增至 Remove-AzureStorageShare
