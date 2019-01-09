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