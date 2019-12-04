---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 8c1369cdedf8848f3c62ca6b6bc4eb3d2d78be95
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/28/2019
ms.locfileid: "74656820"
---
## <a name="280---october-2019"></a>2.8.0 - 2019 年10月
### <a name="general"></a>一般
* Az.HealthcareApis 1.0.0 版本

#### <a name="azaccounts"></a>Az.Accounts
* 針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援
    - 修正 https://github.com/Azure/azure-powershell/issues/10068 的問題

#### <a name="azautomation"></a>Az.Automation
* 已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。 

#### <a name="azbatch"></a>Az.Batch
* **Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。

#### <a name="azcompute"></a>Az.Compute
* 在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數
* 修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件
* 修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。 
* 修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。

#### <a name="azdatafactory"></a>Az.DataFactory
* 針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。
* 針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。
* 將 ADF .Net SDK 版本更新為 4.2.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* 已將 Powershell 版本更新為 1.0.0
* 已將 SDK 版本更新為 1.0.2
* 更新測試以參考新的 SDK 版本
* 已將輸出結構從巢狀更新為壓平合併。

#### <a name="aziothub"></a>Az.IotHub
* 新增新的路由來源：DigitalTwinChangeEvents
* 次要錯誤修正：Get-AzIothub 未傳回 subscriptionId 

#### <a name="azmonitor"></a>Az.Monitor
* 已針對 New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver 新增了新的動作群組接收器
* 針對接收器使用已啟用的一般警示結構描述。 這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器
* Webhooks 現在支援 Azure Active Directory 驗證。

#### <a name="aznetwork"></a>Az.Network
* 新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。
* 已在虛擬網路閘道連線新增了流量選取器的支援
    - 已新增新的 Cmdlet：
        - New-AzIpsecTrafficSelectorPolicy
    - 已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection
* 新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援
    - 已更新的 Cmdlet：
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* 改善 Cortex Cmdlet 中的例外狀況處理
* 適用於 VirtualNetworkGateways 的新項目和 SKU
  - 引進新一代的 VirtualNetworkGateways。
  - 引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。

#### <a name="azrediscache"></a>Az.RedisCache
* 更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值

#### <a name="azsql"></a>Az.Sql
* 新增在受控執行個體上設定 Active Directory 系統管理員的支援

#### <a name="azstorage"></a>Az.Storage
* 將儲存體用戶端程式庫升級為 11.1.0
* 列出具有管理平面 API 的容器，將會以 NextPageLink 列出
    -  Get-AzRmStorageContainer
* 列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* 修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp 更新應用程式的 ASP 時失敗

## <a name="270---september-2019"></a>2.7.0 - 2019 年 9 月
#### <a name="azapimanagement"></a>Az.ApiManagement
* 更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述
* 已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。 改為使用 'Set-AzApiManagement'。

#### <a name="azautomation"></a>Az.Automation
* 已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字
* 已新增 Register-AzAutomationDSCNode 的 OS 限制說明
* 已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。

#### <a name="azcompute"></a>Az.Compute
* 在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數
* 在 New-AzSnapshotConfig 中新增增量參數
* 新增低優先順序虛擬機器功能：
    - 已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。
    - 已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。
* 修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。
* 修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。
* 修正適用於端點相關位置的 VHD Seek 方法。
* 修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。

#### <a name="azdatafactory"></a>Az.DataFactory
* 為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus
* 已將 ADF .Net SDK 版本更新為 4.1.3

#### <a name="azhdinsight"></a>Az.HDInsight
* 呼叫重大變更

#### <a name="aziothub"></a>Az.IotHub
* 針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。
* 新增管理 IotHub 訊息擴充的支援。 這些新 Cmdlet 包括：
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* 指向最近的監視 SDK，例如 0.24.1-preview
   - 在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。 這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。
   - **ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。 已針對此項變更新增多個案例測試。
   - **EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。 目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。 **注意**：這是暫時性的變更，必須由警示小組驗證。
   - **Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。 此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。
   - **AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。 此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。
* 適用於計量警示 V2 的支援動態閾值準則
    - New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則
    - Add-AzMetricAlertRuleV2：目前也接受動態閾值準則
* 已排程查詢規則 Cmdlet (SQR) 中的改善項目
 - Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)
 - 在說明檔案中適當地描述 ’Enabled’ 參數
 - 已新增 'ActionGroup' 選用參數的範例
 - 說明檔內容全面改善
* 修正判斷 'Set-AzActionRule' 範圍類型的錯誤

#### <a name="aznetwork"></a>Az.Network
* 修正 'New-AzApplicationGateway' 參考文件中不正確的範例 
* 在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊
* 已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC
* 改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)
* 改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型
* 修正了不正確的安全性規則模型對應
* 在網路介面中新增了屬性以提供 IP 功能
    - 在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型
    - 在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型
    - 新增了模型類別 PSIpConfigurationConnectivityInformation
* 針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'
* 在虛擬 WAN 中支援多連結
    - 新的 Cmdlet
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - 已更新 Cmdlet：
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* 修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件
* 新增了 VM 原則和原始儲存體帳戶還原的測試

#### <a name="azresources"></a>Az.Resources
* 修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字
* 新增 Cmdlet 以管理應用程式和服務：
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* 已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。

#### <a name="azsignalr"></a>Az.SignalR
* 新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet

#### <a name="azsql"></a>Az.Sql
* 更新 'Get-AzSqlElasticPool' 參考文件中的範例
* 新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。
* 移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false
* 當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。
* 修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。

#### <a name="azstorage"></a>Az.Storage
* 已更新 'Get-AzStorageAccountKey' 參考文件中的範例
* 在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* 修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。
    -  Set-AzStorageBlobContent
* 支援透過管理平面 API 管理 Azure 檔案共用
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* 修正了將應用程式遷移到新的 ASP 時，webapp 標籤遭到刪除的問題
* 修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作
* 更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例

## <a name="260---august-2019"></a>2.6.0 - 2019 年 8 月
#### <a name="general"></a>一般
* 修正了多個模組中的各種錯字問題

#### <a name="azaccounts"></a>Az.Accounts
* 支援 Azure Functions 驗證中使用者指派的 MSI (#9479)

#### <a name="azaks"></a>Az.Aks
* 修正 'Get-AzAks' 的輸出問題
    * 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* 修正 https://github.com/Azure/azure-powershell/issues/9351 的問題
    - 更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制
* **Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752
* 將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'

#### <a name="azbatch"></a>Az.Batch
* 修正了說明訊息和文件中的錯字，將 Windows 首字變大寫

#### <a name="azcdn"></a>Az.Cdn
* 修正了 CDN 模組轉換協助程式中的錯字

#### <a name="azcompute"></a>Az.Compute
* 將 VmssId 新增到 New-AzVMConfig Cmdlet
* 將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中
* 將 HyperVGeneration 屬性新增到 VM 映像物件中
* 新增 Host 和 HostGroup 功能
    - 新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - 已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中
* 更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱
* 更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述

#### <a name="azdatafactory"></a>Az.DataFactory
* 修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫
* 已將 ADF .Net SDK 版本更新為 4.1.2
* 對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy
* 更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。

#### <a name="azeventhub"></a>Az.EventHub
* 修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題
* 修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT
* 已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet
* 修正 #9786 的問題：無法建立僅限接聽權限的規則

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* 修正了文件中 'Azure'均為小寫的錯字問題

#### <a name="azmonitor"></a>Az.Monitor
* 已修正說明文件中不正確的參數名稱

#### <a name="aznetwork"></a>Az.Network
* 更新了 New-AzPrivateLinkServiceIpConfig
    - 取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。
    - 新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。
* 改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題
* 調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。 
* 更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。
* 對 AzNetworkServiceTag 新增位置參數的描述

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件
    - 新增了範例
    - 更新了 '-Name' 參數的說明
* 新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例
* 對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 更新 'Get-AzRecoveryServicesBackupJobDetail.md'

#### <a name="azresources"></a>Az.Resources
* 新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援
    - 新增對 'copy.count = 0' 中的變數、資源和屬性的支援
    - 完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源
* 在說明文件的訂閱層級中新增了指派原則範例

#### <a name="azservicebus"></a>Az.ServiceBus
* 修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字
* 修正 #9786 的問題：無法建立僅限接聽權限的規則
* 新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性 

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 修正新增節點類型 Cmdlet 錯誤 (bug)：
    - 當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。 修正問題： https://github.com/Azure/azure-powershell/issues/8681
    - 修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。 修正問題： https://github.com/Azure/azure-powershell/issues/8407
    - 取代 Add-AzServiceFabricApplicationCertificate Cmdlet

#### <a name="azsql"></a>Az.Sql
* 更新舊版 Auditing Cmdlet 文件。

#### <a name="azstorage"></a>Az.Storage
* 更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述
* 支援上傳 Blob 和複製 Blob 中的 StandardBlobTier
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* 支援複製 Blob 中的 Rehydrate Priority
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* 釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的

## <a name="250---july-2019"></a>2.5.0 - 2019 年 7 月
#### <a name="azaccounts"></a>Az.Accounts
* 更新通用程式碼，以使用最新版 ClientRuntime

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* 修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字 

#### <a name="azautomation"></a>Az.Automation
* 修正資源字串中的錯字 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 新增了 NetworkRuleSet 支援。

#### <a name="azcompute"></a>Az.Compute
* 新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* 修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字
    - 如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 4.1.0
* 修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字

#### <a name="azeventhub"></a>Az.EventHub
* 新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken
* 在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息

#### <a name="azkeyvault"></a>Az.KeyVault
* 新增了為憑證原則指定 KeySize 的支援

#### <a name="azlogicapp"></a>Az.LogicApp
* 修正 Get-AzIntegrationAccountMap 以列出所有對應類型
    - 新增了用於篩選的 MapType 參數

#### <a name="azmanagedservices"></a>Az.ManagedServices
* 新增了 API 版本 2019-06-01 (GA) 的支援

#### <a name="aznetwork"></a>Az.Network
* 新增私人端點和私人連結服務的支援
    - 新的 Cmdlet
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* 已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標
    - 更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig
        - 新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。
        - 新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。
* AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性
* 針對網路安全性規則組態啟用 ICMP 通訊協定
    - 更新的 Cmdlet
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* 新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數
* 在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion
    - 已更新 Cmdlet：
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* 更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠
    - 更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。 此參數適用於 Standard_V2 和 WAF_V2 SKU。

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 更新了預設版本，讓已儲存的搜尋為 1。 
* 修正了自訂記錄 Null 處理

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 更新 'Get-AzRecoveryServicesBackupJob.md'
* 更新 'Get-AzRecoveryServicesBackupContainer.md'
* 更新 'Get-AzRecoveryServicesVault.md'
* 更新 'Wait-AzRecoveryServicesBackupJob.md'
* 更新 'Set-AzRecoveryServicesVaultContext.md'
* 更新 'Get-AzRecoveryServicesBackupItem.md'
* 更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'
* 更新 'Restore-AzRecoveryServicesBackupItem.md'
* 針對 Azure File Share 的 Unregistering 容器更新了服務呼叫
* 更新 'Set-AzRecoveryServicesAsrAlertSetting.md'

#### <a name="azresources"></a>Az.Resources
- 移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet
- 更新原則 Cmdlet 以使用新的 API 版本 2019-01-01

#### <a name="azservicebus"></a>Az.ServiceBus
* 新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken
* 在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息

#### <a name="azsql"></a>Az.Sql
* 修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例
* 修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題
* 修正警告訊息中的錯字。

#### <a name="azstorage"></a>Az.Storage
* 更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱

#### <a name="azstoragesync"></a>Az.StorageSync
* 新增 Invoke-AzStorageSyncChangeDetection Cmdlet。
* 修正問題 9551 以接受 TierFilesOlderThanDays

#### <a name="azwebsites"></a>Az.Websites
* 修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)
* 新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數
* 修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)

## <a name="240---july-2019"></a>2.4.0 - 2019 年 7 月
#### <a name="azaccounts"></a>Az.Accounts
* 新增設定檔 Cmdlet 的支援
* 在產生的 Cmdlet 中新增環境和資料平面的支援
* 修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet

#### <a name="azadvisor"></a>Az.Advisor
* Az.Advisor 的 GA 版本
* 此模組現包含為彙總 `Az` 模組的一部分

#### <a name="azapimanagement"></a>Az.ApiManagement
* 修正 https://github.com/Azure/azure-powershell/issues/8671 的問題
    - **Get-AzApiManagementSubscription**
        - 新增了依使用者和產品查詢訂用帳戶的支援
        - 新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援
* 修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題
    - **Import-AzApiManagementApi**
        - 新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援

#### <a name="azautomation"></a>Az.Automation
* 修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。

#### <a name="azcompute"></a>Az.Compute
* 將 HyperVGeneration 參數新增到 New-AzImageConfig

#### <a name="azdatafactory"></a>Az.DataFactory
* 更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。

#### <a name="azeventgrid"></a>Az.EventGrid
* 修正 'New-AzEventGridSubscription' 文件中的錯字

#### <a name="aziothub"></a>Az.IotHub
* 新增對重新產生授權原則金鑰的支援。

#### <a name="aznetwork"></a>Az.Network
* 已將 'RoutingPreference' 新增到公用 ip 標籤
* 改善 'Get-AzNetworkServiceTag' 參考文件的範例

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 修正 Get-AzPolicyState 中的 Null 參考問題
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 修正 IaaSVM 的 get-policy 命令

#### <a name="azresources"></a>Az.Resources
    - 修正 Get-AzPolicyState -Top 參數的說明文字
    - 新增 Get-AzPolicyAlias 的用戶端分頁支援
    - 新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數
    - 原則 Cmdlet 的幾個文件與範例更新

#### <a name="azservicebus"></a>Az.ServiceBus
* 修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest

#### <a name="azsql"></a>Az.Sql
* 從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本
* 支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* 從弱點評量設定移除電子郵件條件約束

#### <a name="azstorage"></a>Az.Storage
* 在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：
    -  Enable-AzStorageStaticWebsite
* 藉新增範例更新 Get-AzStorageBlobContent 的說明
* 當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊
* 支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* 支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* 此模組現包含為彙總 `Az` 模組的一部分

## <a name="232---june-2019"></a>2.3.2 - 2019 年 6 月
#### <a name="azaccounts"></a>Az.Accounts
* 修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983
* 修正從 AzureRM 到 Az Cmdlet 的別名問題
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。
* 修正 'New-AzVM' 參考文件中的錯字

#### <a name="azdns"></a>Az.Dns
* 修正了 'Set-AzDnsZone' 說明範例中的錯字。

#### <a name="azeventgrid"></a>Az.EventGrid
* 已更新為使用 2019-06-01 API 版本。
* 新的 Cmdlet：
    - New-AzureRmEventGridDomain
        - 建立新的 Azure 事件方格網域。
    - Get-AzureRmEventGridDomain
        - 取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。
    - Remove-AzureRmEventGridDomain
        - 移除 Azure 事件方格網域。
    - New-AzureRmEventGridDomainKey
        - 重新產生 Azure 事件方格網域適用的共用存取金鑰。
    - Get-AzureRmEventGridDomainKey
        - 取得用來; 事件發佈至事件方格網域的共用存取金鑰。
    - New-AzureRmEventGridDomainTopic：
        - 建立新的 Azure事件方格網域主題。
    - Get-AzureRmEventGridDomainTopic
        - 取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單 
    - Remove-AzureRmEventGridDomainTopic：
        - 移除現有的 Azure 事件方格網域主題。
* 已更新的 Cmdlet：
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：
        - 新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。
        - 新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。
        - 為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。
        - 新增選擇性參數來指定：
            - 事件訂用帳戶過期日期，
            - 進階篩選參數。
        - 為 servicebusqueue 新增新的列舉成為目的地。
        - 不允許使用 'All' in -IncludedEventType 選項並取代為 
    - Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：
        - 新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。
    - Remove-AzureRmEventGridSubscription
        - 新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。
        - 新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - 新增轉換支援和新的運算子自動完成值 (RegEx)
* New-AzFrontDoorWafManagedRuleObject
    - 新增新的自動完成值

#### <a name="aznetwork"></a>Az.Network
* 新增對虛擬網路閘道資源的支援
    - 新的 Cmdlet
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* 新增 AvailablePrivateEndpointType
    - 新的 Cmdlet 
        - Get-AzAvailablePrivateEndpointType
* 新增 PrivatePrivateLinkService
    - 新的 Cmdlet 
        - Get-AzPrivateLinkService 
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* 新增 PrivateEndpoint
    - 新的 Cmdlet
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* 已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標
    - 更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。
    - 更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。
* 在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。
* 在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。
* 新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位
* 修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤
* 修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。
* 修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題
* 修正了 Cortex Get Cmdlet 以列出所有部分
* 修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立
* 新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援
* 新增了 Cmdlet Get-AzNetworkServiceTag
* 新增針對 Azure 防火牆的多個公用 IP 位址的支援
    - 更新了 New-AzFirewall Cmdlet：
        - 新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件
        - 新增了參數 -VirtualNetwork 以接受虛擬網路物件
        - 在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入
        - 參數 -PublicIpName 和 -VirtualNetworkName 已被取代 
* 已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。 
    - 已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。
    - 已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。
    - 已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層

#### <a name="azresources"></a>Az.Resources
* 支援其他範本匯出選項
    - 將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup
    - 將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup
    - 將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題

#### <a name="azsql"></a>Az.Sql
* 修正進階威脅防護儲存體端點尾碼
* 修正進階威脅防護啟用覆寫進階威脅防護原則
* 為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* 在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS
    - New-AzStorageAccount
* 釐清了 Blob 不變性 Cmdlet 的說明
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* 將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選
* 將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot

## <a name="220---june-2019"></a>2.2.0 - 2019 年 6 月
#### <a name="azcdn"></a>Az.Cdn
* 已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。

#### <a name="azcompute"></a>Az.Compute
* 已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。
    - 已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* 修正 #9231 - Get-AzEventHubNamespace 不會傳回標記
* 修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName

#### <a name="aznetwork"></a>Az.Network
* 更新 Nat 閘道的 ResourceId 和 InputObject
    - 新增 ResourceId 和 InputObject 的別名

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 修正 Get-AzPolicyEvent 中的 Null 參考問題

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* IaaSVM 原則的最小保留天數從 1 天變更為 7 天

#### <a name="azservicebus"></a>Az.ServiceBus
* 修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字
* 修正 Service Fabric 命令列中的遺漏字元

#### <a name="azsql"></a>Az.Sql
* 為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。
* 即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet
* 將威脅偵測 Cmdlet 重新命名為進階威脅防護
* New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。

#### <a name="azwebsites"></a>Az.Websites
* 修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題

## <a name="210---may-2019"></a>2.1.0 - 2019 年 5 月
#### <a name="azapimanagement"></a>Az.ApiManagement
* 已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷
    - **Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷
    - **New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷
    - **New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定
    - **New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。
    - **New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定
    - **Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體
    - **Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體
* 已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取
    - **Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料
    - **New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取
    - **Remove-AzApiManagementCache** - 移除快取
    - **Update-AzApiManagementCache** - 更新快取
* 已建立新的 Cmdlet 用以管理 API 結構描述
    - **New-AzApiManagementSchema** - 為 API 建立新的結構描述
    - **Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述
    - **Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述
    - **Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述
* 已建立新的 Cmdlet 用以產生使用者權杖。 
    - **New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/
* 已建立新的 Cmdlet 用以擷取網路狀態
    - **Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。 這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。
* 已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務 
    - 已加入新的「使用量」SKU 的支援
    - 已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援
    - 新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。 這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。
    - 已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。
* 已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入
* 已更新 Cmdlet 以顯示內嵌錯誤訊息 
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]
* 已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API
* 已更新 Cmdlet **Import-AzApiManagementApi**
    - 以從 'OpenApi 3.0' 文件規格匯入 API
    - 以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。
    - 以覆寫任何文件中指定的 'ServiceUrl' 屬性。
* 已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則
* 已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則
* 已更新 Cmdlet **New-AzApiManagementApi** 
    - 以透過 'OpenId' 授權伺服器設定 API。
    - 以在 'ApiVersionSet' 中建立 API
    - 以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。
    - 能夠在 API 範圍設定 'SubscriptionRequired'。 
* 已更新 Cmdlet **Set-AzApiManagementApi**
    - 以透過 'OpenId' 授權伺服器設定 API。
    - 以在 'ApiVersionSet' 中更新 API    
    - 能夠在 API 範圍設定 'SubscriptionRequired'。 
* 已更新 Cmdlet **New-AzApiManagementRevision**
    - 以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。 新的修訂會採用父代的 'ApiId'。
    - 以提供 'ApiRevisionDescription'
    - 以在複製 API 時覆寫 'ServiceUrl'。
* 已更新 Cmdlet **New-AzApiManagementIdentityProvider**
    - 以透過 'Authority' 設定 'AAD' 或 'AADB2C'
    - 以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'
* 已更新 Cmdlet **New-AzApiManagementSubscription**
    - 以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel
    - 以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型
    - 加入在訂用帳戶層級啟用 'AllowTracing' 的支援。
* 已更新 Cmdlet **Set-AzApiManagementSubscription**
    - 以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel
    - 以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型
    - 加入在訂用帳戶層級啟用 'AllowTracing' 的支援。
* 已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入
    - 'New-AzApiManagementContext'
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - 'Get-AzApiManagementApiRelease'
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - 'Get-AzApiManagementApiVersionSet'
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - 'Get-AzApiManagementAuthorizationServer'
    - 'Get-AzApiManagementBackend'
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - 'Get-AzApiManagementCertificate' 
    - 'Remove-AzApiManagementApiVersionSet'
    - 'Remove-AzApiManagementSubscription'

#### <a name="azautomation"></a>Az.Automation
* 已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。
    - 修正 https://github.com/Azure/azure-powershell/issues/7977 的問題
    - 修正 https://github.com/Azure/azure-powershell/issues/8600 的問題
* 已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。
    * 修正 https://github.com/Azure/azure-powershell/issues/8347 的問題
* 修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。 現在它只會相符的節點。

#### <a name="azcompute"></a>Az.Compute
* 將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。
* 在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試

#### <a name="azmonitor"></a>Az.Monitor
* 已修正說明範例中不正確的參數名稱

#### <a name="aznetwork"></a>Az.Network
* 將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出
    - 已更新 Cmdlet：
        - Get-AzEffectiveRouteTable
* 修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號

#### <a name="azresources"></a>Az.Resources
* 新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派

#### <a name="azsql"></a>Az.Sql
* 將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量

## <a name="200---may-2019"></a>2.0.0 - 2019 年 5 月
#### <a name="azaccounts"></a>Az.Accounts
* 更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 只顯示 Bing 搜尋服務的 Bing 免責聲明。
* 改善建立帳戶失敗時的錯誤。

#### <a name="azcompute"></a>Az.Compute
* 鄰近放置群組功能。
    - 新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - 將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* 將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。
* New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。
* 將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss       
* 重大變更
    - 將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。
    - 將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* 第一版正式運作的 Azure 部署管理員 Cmdlet

#### <a name="azdns"></a>Az.Dns
* 自動的 DNS NameServer 委派
    - 建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。
    - 針對新建立的子系區域，在父代區域中新增 NS 記錄。

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 第一版正式運作的 Azure FrontDoor Cmdlet
* 重新命名 WAF Cmdlet 以包含 'Waf'
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* 移除兩個 Cmdlet：
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* 已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess
* 更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：
    - 具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。
    - 具有 HDInsight 操作員角色的使用者不會受到影響。

#### <a name="azmonitor"></a>Az.Monitor
* SQR API 的新 Cmdlet (已排程的查詢規則)  
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊
    - 更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet

#### <a name="aznetwork"></a>Az.Network
* 新增 Nat 閘道資源的支援
    - 新的 Cmdlet
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - 更新的 Cmdlet
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* 已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。
    - 已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。
    - 已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 支援查詢原則的評估詳細資料。
    - 將 '-Expand' 參數新增至 Get-AzPolicyState。 支援 '-Expand PolicyEvaluationDetails'。

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 支援跨訂用帳戶的 Azure 到 Azure 站台復原。
* 標示 Azure Site Recovery 上即將進行的重大變更。
* Azure Site Recovery 復原計劃和行動計劃的修正。
* Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。
* 受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。
* 其他小幅修正。

#### <a name="azrelay"></a>Az.Relay
* 修正客戶訊息中的錯字

#### <a name="azservicebus"></a>Az.ServiceBus
* 已針對命名空間的 NetworkRuleSet 新增 Cmdlet

#### <a name="azstorage"></a>Az.Storage
* 升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')
* 升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。
* 建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'
    - New-AzStorageAccount
* 藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性
* Get-AzWebApp*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰

## <a name="180---april-2019"></a>1.8.0 - 2019 年 4 月
### <a name="highlights-since-the-last-major-release"></a>上次發佈主要版本之後的更新重點
* `Az` 模組的一般可用性
* 如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce
* 新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/
* 新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援
* 新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證
* 新增了 Az.Automation 中 Python 2 Runbook 的支援
* Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet

#### <a name="azaccounts"></a>Az.Accounts
* 更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組

#### <a name="azbatch"></a>Az.Batch
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azcdn"></a>Az.Cdn
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azcompute"></a>Az.Compute
* 如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。
* 修正文件中的萬用字元

#### <a name="azdatafactory"></a>Az.DataFactory
* 如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azeventgrid"></a>Az.EventGrid
* 已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。

#### <a name="azeventhub"></a>Az.EventHub
* 已針對命名空間的 NetworkRuleSet 新增 Cmdlet 

#### <a name="azhdinsight"></a>Az.HDInsight
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="aziothub"></a>Az.IotHub
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azkeyvault"></a>Az.KeyVault
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。
* 修正文件中的萬用字元

#### <a name="azmachinelearning"></a>Az.MachineLearning
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azmedia"></a>Az.Media
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azmonitor"></a>Az.Monitor
  * 適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * 監視器 SDK 已更新為版本 0.22.0-preview

#### <a name="aznetwork"></a>Az.Network
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。
* 修正文件中的萬用字元

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。
* 已更新 Azure VM 中 SQL 的資料表格式
* 已新增替代方法來擷取 AzureFileShare 中的位置
* 已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays

#### <a name="azrediscache"></a>Az.RedisCache
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。

#### <a name="azresources"></a>Az.Resources
* 修正文件中的萬用字元

#### <a name="azsql"></a>Az.Sql
* 以通用程式碼取代監視器 SDK 的相依性
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。
* 已增強多個資料行分類的程序。
* 在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。
* 依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。
* 在受控執行個體中支援建立時區參數。
* 修正文件中的萬用字元

#### <a name="azwebsites"></a>Az.Websites
* 將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記
* 已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。
* 已更新網站 SDK。
* 已從 PSAppServicePlan 中移除 AdminSiteName 屬性。

## <a name="170---april-2019"></a>1.7.0 - 2019 年 4 月
### <a name="highlights-since-the-last-major-release"></a>上次發佈主要版本之後的更新重點
* `Az` 模組的一般可用性
* 如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce
* 新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/
* 新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援
* 新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證
* 新增了 Az.Automation 中 Python 2 Runbook 的支援
* Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet

#### <a name="azaccounts"></a>Az.Accounts
* 已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* 在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯
* 讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更

#### <a name="azautomation"></a>Az.Automation
* 修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。 現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。
* 修正 Azure 自動化更新管理動態群組的錯誤 (bug)

#### <a name="azcompute"></a>Az.Compute
* 將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig
* 允許使用其他租用戶的資源庫映像來建立 VM。 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* 已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 3.0.2
* 已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。

#### <a name="azresources"></a>Az.Resources
* 改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理
* 改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理
    - 處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856
* 將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* 支援資料庫的資料分類。

#### <a name="azstorage"></a>Az.Storage
* 報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)
    - New-AzStorageContext
* 支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 - 2019 年 3 月
### <a name="highlights-since-the-last-major-release"></a>上次發佈主要版本之後的更新重點
* `Az` 模組的一般可用性
* 如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce
* 新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/
* 新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援
* 新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證
* 新增了 Az.Automation 中 Python 2 Runbook 的支援
* Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet

#### <a name="azautomation"></a>Az.Automation
* Azure 自動化更新管理變更為支援下列各項新功能：
    * 動態分組
    * 預先貼文指令碼
    * 重新啟動設定

#### <a name="azcompute"></a>Az.Compute
* 修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題
* 將計算用戶端程式庫更新為 25.0.0。

#### <a name="azkeyvault"></a>Az.KeyVault
* 新增了 KeyVault Cmdlet 的萬用字元支援

#### <a name="aznetwork"></a>Az.Network
* 新增適用於 Azure 防火牆的威脅智慧支援
* 新增應用程式閘道防火牆原則頂層資源和自訂規則

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP
* 新增了取消註冊容器的管道支援

#### <a name="azresources"></a>Az.Resources
* 更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援
* 更新在對 ARM 進行一般呼叫時使用的認證

#### <a name="azsql"></a>Az.Sql
* 變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。

#### <a name="azstorage"></a>Az.Storage
* 支援儲存體帳戶上的 Get/Set/Remove 管理原則
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* 修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況 

## <a name="150---march-2019"></a>1.5.0 - 2019 年 3 月
#### <a name="azaccounts"></a>Az.Accounts
* 新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet
* 適用於 Connect-AzAccount 的更新範例

#### <a name="azautomation"></a>Az.Automation
* 修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題
* 修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。 現在可以傳回所有節點

#### <a name="azcdn"></a>Az.Cdn
* 新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet

#### <a name="azcompute"></a>Az.Compute
* 新增 Get Cmdlet 的萬用字元支援

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 3.0.1

#### <a name="azlogicapp"></a>Az.LogicApp
* 修正 ListWorkflows，僅擷取結果的第一頁資料

#### <a name="aznetwork"></a>Az.Network
* 新增 Network Cmdlet 的萬用字元支援

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 新增了Azure VM 中 SQL 伺服器的支援
* SDK 更新
* 移除了 Get-ProtectableItem 中的 VMappContainer 檢查
* 新增了 Get-ProtectableItem 的 Name 和 ServerName 參數

#### <a name="azresources"></a>Az.Resources
* 將 `-TemplateObject` 參數新增至部署 Cmdlet
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933
* 修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240
* 修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* 更新 AuditingEndpointsCommunicator。
    - 修正在建立新診斷設定時邊緣案例的行為。

#### <a name="azstorage"></a>Az.Storage
* 在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 - 2019 年 2 月
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* 即將淘汰 AddAzureASAccount Cmdlet

#### <a name="azautomation"></a>Az.Automation
* 更新 Import-AzAutomationDscNodeConfiguration 的說明
* 已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet
* 已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。

#### <a name="azcompute"></a>Az.Compute
* 修正識別碼參數集問題
* 如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組
* 將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet
* 沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 為 ADL 刪除的項目列舉和還原新增 Cmdlet

#### <a name="azeventhub"></a>Az.EventHub
* 在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives 

#### <a name="azkeyvault"></a>Az.KeyVault
* 修正 Set-AzKeyVaultSecret 的標記

#### <a name="azlogicapp"></a>Az.LogicApp
* 在整合帳戶的基本 sku 新增
* 在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增
* 整合帳戶組件的新 Cmdlet
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* 整合帳戶批次設定的新 Cmdlet
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* 將邏輯應用程式 SDK 更新至 4.1.0 版

#### <a name="azmonitor"></a>Az.Monitor
* 更新 Get-AzMetric 的說明

#### <a name="aznetwork"></a>Az.Network
* 更新 Add-AzApplicationGatewayCustomError 的說明範例

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 取得 ApplicationInsights 與新資料來源的其他支援。
    - 已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。 
    - 已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。 

#### <a name="azresources"></a>Az.Resources
* 修正 https://github.com/Azure/azure-powershell/issues/8166 的問題
* 修正 https://github.com/Azure/azure-powershell/issues/8235 的問題
* 修正 https://github.com/Azure/azure-powershell/issues/6219 的問題
* 修正防止重複建立 KeyCredentials 的錯誤

#### <a name="azsql"></a>Az.Sql
* 新增 SQL DB 超大規模層支援
* 已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗

#### <a name="azwebsites"></a>Az.Websites
* Get-AzWebAppSlotMetrics 中的正確範例

## <a name="130---february-2019"></a>1.3.0 - 2019 年 2 月
#### <a name="azaccounts"></a>Az.Accounts
* 更新至最新版本的 ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Az.AnalysisServices 模組的正式運作。

#### <a name="azcompute"></a>Az.Compute
* AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援
* 更新 AzVMBootDiagnostics 的說明描述
* 更新 Update-AzImage 的說明描述和範例

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Az.RecoveryServices 模組的正式運作。

#### <a name="azresources"></a>Az.Resources
* 修正資源群組標記 
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166
* 修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題 
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* 新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* 修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題
* 已修正 Get AzSqlCapability 中的 Null 參考例外狀況

## <a name="121---january-2019"></a>1.2.1 - 2019 年 1 月
#### <a name="azaccounts"></a>Az.Accounts
* 包含正確驗證版本的發行

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* 包含更新驗證相依性的版本

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 包含更新驗證相依性的版本

## <a name="120---january-2019"></a>1.2.0 - 2019 年 1 月
#### <a name="azaccounts"></a>Az.Accounts
* 僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證
* 更新不正確的線上說明 URL
* 在 PS Core 中新增 Uninstall-AzureRm 的警告訊息

#### <a name="azaks"></a>Az.Aks
* 更新不正確的線上說明 URL

#### <a name="azautomation"></a>Az.Automation
* 已新增 Python 2 Runbook 的支援
* 更新不正確的線上說明 URL

#### <a name="azcdn"></a>Az.Cdn
* 更新不正確的線上說明 URL

#### <a name="azcompute"></a>Az.Compute
* 新增 Invoke-AzVMReimage Cmdlet
* 將 TempDisk 參數新增至 Set-AzVmss
* 修正 New-AzVM 的警告訊息

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* 更新不正確的線上說明 URL

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 3.0.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 修正使用 MSI 時 ADLS 端點的問題
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462
* 更新不正確的線上說明 URL

#### <a name="aziothub"></a>Az.IotHub
* 將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。

#### <a name="azkeyvault"></a>Az.KeyVault
* 更新不正確的線上說明 URL

#### <a name="aznetwork"></a>Az.Network
* 更新不正確的線上說明 URL

#### <a name="azresources"></a>Az.Resources
* 修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例
* 修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題
* Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件
* Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題
* Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題
* 修正「PSResourceGroupDeployment」物件格式化的問題
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932
* 修正某些錯誤訊息。
* 修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。
* 檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。

#### <a name="azsignalr"></a>Az.SignalR
* 更新不正確的線上說明 URL

#### <a name="azsql"></a>Az.Sql
* 更新不正確的線上說明 URL
* 更新了 LicenseType 參數的描述並新增了可能的值
* 修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題
* 支援在受控執行個體上的自訂定序

#### <a name="azstorage"></a>Az.Storage
* 更新不正確的線上說明 URL
* 在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* 更新不正確的線上說明 URL

#### <a name="azwebsites"></a>Az.Websites
* 更新不正確的線上說明 URL
* 修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。
* 修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記

## <a name="110---january-2019"></a>1.1.0 - 2019 年 1 月
#### <a name="azaccounts"></a>Az.Accounts
* 將 'Local' 範圍新增至 Enable-AzureRmAlias

#### <a name="azcompute"></a>Az.Compute
* 在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目
* 已更新說明檔案中的識別碼描述
* 修正 Az.Accounts 模組的回溯相容性問題

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。
    - 針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖

#### <a name="azeventgrid"></a>Az.EventGrid
* 已更新為使用 2019-01-01 API 版本。
* 更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例
    - New-AzureRmEventGridSubscription:新增選擇性參數來指定：
        - 事件存留時間、
        - 嘗試傳遞事件的次數上限、
        - 無效信件端點。
    - Update-AzureRmEventGridSubscription:新增選擇性參數來指定：
        - 事件存留時間、
        - 嘗試傳遞事件的次數上限、
        - 無效信件端點。
* 針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。
* 如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。

#### <a name="aziothub"></a>Az.IotHub
* 已更新至最新版本的 IotHub SDK

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp 會列出所有項目，無須指定名稱

#### <a name="azresources"></a>Az.Resources
* 修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875
* 修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理
* 修正 New-AzDeployment 文件中的錯字
* 使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目
    - 如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* 修正 Az.Accounts 模組的回溯相容性問題

#### <a name="azsql"></a>Az.Sql
* 將儲存體管理用戶端相依性轉換為一般的 SDK 實作。

#### <a name="azstorage"></a>Az.Storage
* 使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱
    - New-AzStorageContext
* 使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* 修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤
* 修正 Az.Accounts 模組的回溯相容性問題

## <a name="100---december-2018"></a>1.0.0 - 2018 年 12 月
### <a name="general"></a>一般

- Az 模組正式運作
- 每個模組的線上說明
- 如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)
- 如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azaccounts"></a>Az.Accounts
- 已從 Az.Profile 變更
- 設定檔和內容類型有固定的資料表格式

### <a name="azapimanagement"></a>Az.ApiManagement
- #7002 的修正
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azbatch"></a>Az.Batch
- 已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。
- `PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azbilling"></a>Az.Billing
- 結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azcognitivservices"></a>Az.CognitivServices
- 針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器
- 已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- 已新增 ManagedIdentity 支援

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azmonitor"></a>Az.Monitor
- Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azkeyvault"></a>Az.KeyVault
- 已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性

### <a name="azmachinelearning"></a>Az.MachineLearning
- 已納入來自 Az.MachineLearningCompute 模組的 Cmdlet

### <a name="azmedia"></a>Az.Media
- 從 New-AzMediaService 移除淘汰的 -Tags 別名

### <a name="aznetwork"></a>Az.Network
已新增在應用程式閘道中設定 RewriteRuleSets 的支援
    - 已新增新的 Cmdlet：
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlets updated with optional parameter -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。
    - 已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - 已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azprofile"></a>Az.Profile
- 模組名稱已變更為 Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azresources"></a>Az.Resources
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azservicefabric"></a>Az.ServiceFabric
- 支援依通用名稱和指紋來指定憑證
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azsignalr"></a>Az.SIgnalR
- SIgnalR 的 PowerShell Cmdlet 正式運作

### <a name="azsql"></a>Az.Sql
- 已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型
- 已更新 SQL 稽核 Cmdlet 的文件範例
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azstorage"></a>Az.Storage
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

### <a name="azwebsites"></a>Az.Websites
- 次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)

## <a name="070---december-2018"></a>0.7.0 - 2018 年 12 月

### <a name="general"></a>一般

* 即將推出的「AzureRM 對 Az 轉換」有些微變更

### <a name="azcompute"></a>Az.Compute

* 針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。

### <a name="azdatalakestore"></a>Az.DataLakeStore

* 修正 adls 帳戶網域的尾端斜線

### <a name="azfrontdoor"></a>Az.FrontDoor

* 已修正一些中斷的連結
    - 在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。
    - 在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* 已針對 Azure 檔案共用的還原作業新增用戶端驗證。
* 已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。

### <a name="azresources"></a>Az.Resources

* 修正 https://github.com/Azure/azure-powershell/issues/7679
    - 將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。

### <a name="azsql"></a>Az.Sql

* 即將推出的「AzureRM 對 Az 轉換」有些微變更
* 已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題
* 已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。

### <a name="azstorage"></a>Az.Storage

* 對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace
* 已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容
    - Start-AzureStorageFileCopy
* 支援靜態網站設定
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot 
    - 已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。 使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。

## <a name="061---november-2018"></a>0.6.1 - 2018 年 11 月

### <a name="azapimanagement"></a>Az.ApiManagement
* 針對類型對應問題更新相依性

### <a name="azautomation"></a>Az.Automation
* 以 Swagger 為基礎的 Azure 自動化 Cmdlet
* 已新增更新管理 Cmdlet
* 已新增原始檔控制 Cmdlet
* 已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet
* 已修正 DSC 註冊節點命令

### <a name="azcompute"></a>Az.Compute
* 已修正 SystemAssigned 身分識別的身份識別問題
* 針對類型對應問題更新相依性

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* 針對類型對應問題更新相依性

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* 更新市集 Cmdlet 的範例描述

### <a name="aznetwork"></a>Az.Network
* 已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError
* 已將 ICMP 加回支援的 AzureFirewall 網路通訊協定
* 更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。 
* 修正 VirtualNetwork 對應中的記憶體使用量問題

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* 提供修正程式以修改受保護的檔案共用原則。
* 已將原則時區轉換為大寫。

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* 已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例
* 針對類型對應問題更新相依性

### <a name="azrelay"></a>Az.Relay
* 已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。

### <a name="azresources"></a>Az.Resources
* 更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件
* 新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例
* 修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫

### <a name="azservicefabric"></a>Az.ServiceFabric
* 針對即將推出的重大變更新增取代資訊

### <a name="azsql"></a>Az.Sql
* 已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* 已在伺服器或資料庫上啟用擴充的稽核原則管理。
    - 已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。
    - 已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。
    - Set-AzureRmSqlServerAuditing。
    - Get-AzureRmSqlServerAuditing。
    - Set-AzureRmSqlDatabaseAuditing。
    - Get-AzureRmSqlDatabaseAuditing。
* 已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題

## <a name="050---november-2018"></a>0.5.0 - 2018 年 11 月
#### <a name="general"></a>一般
* 已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱

#### <a name="azprofile"></a>Az.Profile
* 更新通用程式碼，以使用最新版 ClientRuntime
* 將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名
* 更新 Connect-AzAccount 的 TenantId 說明
* 修正提供租用戶網域時登入失敗的錯誤訊息
    - https://github.com/Azure/azure-powershell/issues/6936
* 修正租用戶中無訂用帳戶之帳戶內容衝突的問題
    - https://github.com/Azure/azure-powershell/issues/7453
* 修正使用 MSI 時 DataLake 端點的問題
    - https://github.com/Azure/azure-powershell/issues/7462
* 修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 新增 Get-AzCognitiveServicesAccountSkus 作業。

#### <a name="azcompute"></a>Az.Compute
* 新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet
* Get-AzVMImage 顯示 AutomaticOSUpgradeProperties
* 已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 將 DataLake 套件更新為 1.1.10。
* 將預設並行新增至多執行作業。

#### <a name="azinsights"></a>Az.Insights
* 已修正問題 #7267 (自動調整區域)
    - 建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。
* 已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格
    - 目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作

#### <a name="aznetwork"></a>Az.Network
* 已將 PeeringType 變更為下列 Cmdlet 的必要參數：-
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 已新增原則修復 Cmdlet

#### <a name="azresources"></a>Az.Resources
* 修正 https://github.com/Azure/azure-powershell/issues/7402
    - 允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源

#### <a name="azservicebus"></a>Az.ServiceBus
* 已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 修正將憑證新增至 Linux Vmss。
* 修正 'Add-AzServiceFabricClusterCertificate'
    - 使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。
    - 正確顯示例外狀況 (Azure/service-fabric-issues#1054)。
* 修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。

## <a name="040---october-2018"></a>0.4.0 - 2018 年 10 月
#### <a name="azprofile"></a>Az.Profile
* 修正 CloudShell 中 Get-AzSubscription 的問題
* 更新通用程式碼，以使用最新版 ClientRuntime

#### <a name="azcompute"></a>Az.Compute
* 已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路
* 已將 ResourceName 引數完成器新增至所有 Cmdlet。

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 新增虛擬網路規則的支援
    - Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。
    - Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。
    - Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。
    - Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。

#### <a name="aznetwork"></a>Az.Network
* 更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。
* 已將 ResourceName 引數完成器新增至所有 Cmdlet。

#### <a name="azresources"></a>Az.Resources
* 修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。 也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。

## <a name="030---october-2018"></a>0.3.0 - 2018 年 10 月
#### <a name="azurestorage"></a>Azure.Storage
* 修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* 支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。

#### <a name="azcompute"></a>Az.Compute
* 修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果
* 已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。
* 已修正 Azure 磁碟加密進度訊息中的錯字

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* 已將 ADF .Net SDK 版本更新為 2.3.0。

#### <a name="aznetwork"></a>Az.Network
* 已新增 NetworkProfile 功能。 已新增新的 Cmdlet
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* 已在子網路模型中新增服務關聯連結
* 已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet
* 已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet

#### <a name="azrediscache"></a>Az.RedisCache
* 日後允許任何字串做為 Size 參數。 在 P5 PSArgumentCompleter 快顯視窗中新增 P5

#### <a name="azresources"></a>Az.Resources
* 將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition
* 修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業

#### <a name="azsql"></a>Az.Sql
* 已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題

#### <a name="azwebsites"></a>Az.Websites
* 新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL
* 新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段

## <a name="020---september-2018"></a>0.2.0 - 2018 年 9 月
 初始版本
