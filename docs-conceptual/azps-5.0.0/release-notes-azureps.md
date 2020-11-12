---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 27073db862b83c5b95f2364355037c1ebd34a3b5
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407488"
---
# <a name="azure-powershell-release-notes"></a>Azure PowerShell 版本資訊

## <a name="500---october-2020"></a>5.0.0 - 2020 年 10 月
#### <a name="azaccounts"></a>Az.Accounts
* [中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'
* 已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)

#### <a name="azaks"></a>Az.Aks
* [中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。
* [中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。
* [中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。
* [中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。

#### <a name="azbilling"></a>Az.Billing
* 已新增 'Get-AzBillingAccount' Cmdlet
* 已新增 'Get-AzBillingProfile' Cmdlet
* 已新增 'Get-AzInvoiceSection' Cmdlet
* 已在 'Get-AzBillingInvoice' Cmdlet 中新增參數
* 已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames

#### <a name="azcdn"></a>Az.Cdn
* 已新增 Cmdlet 來支援多個來源和私人連結功能 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已將 SDK 更新為 7.4.0-preview。

#### <a name="azcompute"></a>Az.Compute
* 已將 '-VmssId' 參數新增至 'New-AzVm'
* 已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。
* 新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'
* 已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。 
* 已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。 

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* [重大變更] 將 API 版本更新為 2019-05-01
* [中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'
* 已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'
* 已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'

#### <a name="azdatabricks"></a>Az.Databricks
* 已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 4.12.0
* 已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7
* 已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* 需要 Location 屬性，才能建立最上層 arm 物件。
        * 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。
        * 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。
        * 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。

#### <a name="azfunctions"></a>Az.Functions
* [中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。 若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。 
* 已更新 'New-AzFunctionApp'：
  - 已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。 [#12728]
  - [中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援
  - [中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。
  - [中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。
  - [中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。

#### <a name="azhdinsight"></a>Az.HDInsight
 * 針對 New-AzHDInsightCluster Cmdlet：
     - 已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'
     - 已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'
     - 已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'
     - 已移除參數 'PublicNetworkAccessType'
     - 已移除參數 'OutboundPublicNetworkAccessType'
     - 已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2
     - 已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式
     - 已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy
 * 針對 New-AzHDInsightClusterConfig Cmdlet：
     - 已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'
     - 已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'
     - 已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'
     - 已移除參數 'PublicNetworkAccessType'
     - 已移除參數 'OutboundPublicNetworkAccessType'
* 針對 AzHDInsightDefaultStorage Cmdlet：
    - 已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'
* 針對 AzHDInsightSecurityProfile Cmdlet：
    - 已將參數 'Domain' 取代為 'DomainResourceId'
    - 已移除參數 'OrganizationalUnitDN' 的強制需求

#### <a name="azkeyvault"></a>Az.KeyVault
* [中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數
* [中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]
* 支援的新資源類型：受控 HSM
    - 受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet
    - 完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC

#### <a name="azmanagedservices"></a>Az.ManagedServices
* [中斷性變更] 已更新參數命名慣例和相關範例

#### <a name="aznetwork"></a>Az.Network
* [中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'
* 已針對虛擬路由器對等路由新增 Cmdlet
    - 'Get-AzVirtualRouterPeerLearnedRoute'
    - 'Get-AzVirtualRouterPeerAdvertisedRoute'
* 更新了 New-AzFirewall Cmdlet：
    - 已新增參數 '-SkuTier'
    - 已新增參數 '-SkuName' 並將 Sku 設為此項的別名
    - 已移除參數 '-Sku'
* [中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數
* [中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'
* [中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'
* 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：
    - 已新增參數 '-Type'
    - 已新增參數 '-CoverageLevel'
    - 已新增參數 '-Scope'
* 已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已修正參與者權限的工作負載還原。
* 已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。

#### <a name="azresources"></a>Az.Resources
* 已修正剖析錯誤 (bug)
* 已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息
* 已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]
* 已修正範本部署 Cmdlet 未保留範本參數大小寫的問題
* 已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本
* 已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet
* 已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數) 
* 已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。
* 已從 '*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。

#### <a name="azsql"></a>Az.Sql
* 已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]
* 已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]
* 在備份儲存體備援警告中更新 Azure 配對區域 URL 

#### <a name="azstorage"></a>Az.Storage
* 已移除淘汰的屬性 RestorePolicy.LastEnabledTime
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - 'Get-AzStorageBlobServiceProperty'
    - 'Update-AzStorageBlobServiceProperty'
* 將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？
    - 'Set-AzStorageAccountManagementPolicy'
    - 'Get-AzStorageAccountManagementPolicy'
    - 'Add-AzStorageAccountManagementPolicyAction'
    - 'New-AzStorageAccountManagementPolicyRule'
* 使用存取層支援的建立/更新檔案共用
    - 'New-AzRmStorageShare'
    - 'Update-AzRmStorageShare'
* 在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl 
    -  'Set-AzDataLakeGen2AclRecursive' 
    -  'Update-AzDataLakeGen2AclRecursive' 
    -  'Remove-AzDataLakeGen2AclRecursive'
* 具有新權限 x,t 支援的容器存取原則
    -  'New-AzStorageContainerStoredAccessPolicy'
    -  'Set-AzStorageContainerStoredAccessPolicy'
* 已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String
    -  'Get-AzStorageContainerStoredAccessPolicy'
    -  'Set-AzStorageContainerStoredAccessPolicy'
* 已修正使用 json 設定管理原則的範例指令碼問題
    -  'Set-AzStorageAccountManagementPolicy'

#### <a name="azwebsites"></a>Az.Websites
* 已新增 Premium V3 定價層的支援
* 已將 WebSites SDK 更新為 3.1.0

### <a name="thanks-to-our-community-contributors"></a>感謝我們的社群參與者
* @atul-ram，更新 Get-AzDelegation.md (#13176)
* @dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。 (#13249)
* @kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)
* Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)
* Matthew Burleigh (@mburleigh)
  * 將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet
  * 將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet
  * 將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet
  * 將連結新增至參考的 Cmdlet (#13137)
  * 將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet
  * 將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet

## <a name="480---october-2020"></a>4.8.0 - 2020 年 10 月
#### <a name="azaccounts"></a>Az.Accounts
* 已修正通用程式庫中的日期時間剖析問題 [#13045]

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。
* 針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數

#### <a name="azcompute"></a>Az.Compute
* 已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題
* 已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。 

#### <a name="azdatabricks"></a>Az.Databricks
* 'Az.Databricks' 模組正式發行
* 已新增虛擬網路對等互連的支援

#### <a name="azdatafactory"></a>Az.DataFactory
* 已修正輸出訊息中的錯字

#### <a name="azeventhub"></a>Az.EventHub
* 已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet

#### <a name="azhdinsight"></a>Az.HDInsight
* 已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數
* 已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數
* 已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數
* 已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數
* 已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數
* 已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數

#### <a name="aziothub"></a>Az.IotHub
* 已更新裝置 SDK。

#### <a name="azkeyvault"></a>Az.KeyVault
* 已提供移除屬性 SecretValueText 的詳細日期

#### <a name="azmanagedservices"></a>Az.ManagedServices
* 已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告

#### <a name="azmonitor"></a>Az.Monitor
* 已修正無法隱藏警告訊息的錯誤。 [#12889]
* 在警示規則準則中支援 'SkipMetricValidation' 參數。 藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。

#### <a name="aznetwork"></a>Az.Network
* 已將 Office365 原則新增至 VPNSite 資源
    - 'New-AzO365PolicyProperty'

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已新增工作負載備份的容器名稱驗證。

#### <a name="azrediscache"></a>Az.RedisCache
* 讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗

#### <a name="azsql"></a>Az.Sql
* 已將 BackupStorageRedundancy 新增至下列項目： 
    - 'Restore-AzureRmSqlDatabase'
    - 'New-AzSqlDatabaseCopy'
    - 'New-AzSqlDatabaseSecondary'
* 已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫 
* 已更新 BackupStorageRedundancy 警告訊息名稱

#### <a name="azstorage"></a>Az.Storage
* 儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性
    - 'Update-AzStorageFileServiceProperty'
    - 'Get-AzStorageFileServiceProperty'
* 支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式
    - 'Get-AzRmStorageShare'
* 支援還原已刪除檔案共用
    - 'Restore-AzRmStorageShare'
* 已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。
    - 'Enable-AzStorageBlobDeleteRetentionPolicy'
    - 'Disable-AzStorageBlobDeleteRetentionPolicy'  
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - 'Update-AzStorageBlobServiceProperty'
* 已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]
* 已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]

## <a name="470---september-2020"></a>4.7.0 - 2020 年 9 月
#### <a name="azaccounts"></a>Az.Accounts
* 已格式化即將推出的重大變更訊息
* 已將 Azure.Core 更新為 1.4.1

#### <a name="azaks"></a>Az.Aks
* 已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。 [#12372]
* 已新增對 'New-AzAksCluster' 中附加元件的支援。 [#11239]
* 已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。 [#11239]
* 已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。 [#12371]
* 已將 api 版本更新為 2020-06-01。

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已顯示特定 API 的其他法律條款。

#### <a name="azcompute"></a>Az.Compute
* 已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'
* 適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'
* 已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'
* 已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'
* 已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視
* 已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件
* 已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。 此欄位會顯示虛擬機器執行個體的資源識別碼
* 已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup' 
* 已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 4.11.0

#### <a name="azeventhub"></a>Az.EventHub
* 已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。
* 已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。

#### <a name="azfunctions"></a>Az.Functions
* 已移除在不支援 v2 函式的區域中建立 v2 函式的功能。
* 已取代 PowerShell 6.2。 已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援建立具有自動調整設定的叢集
    - 已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'
* 支援操作叢集的自動調整設定
    - 已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'
    - 已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'
    - 已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'
    - 已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'
    - 已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'

#### <a name="azkeyvault"></a>Az.KeyVault
* 已新增對 RBAC 授權的支援 [#10557]
* 已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]

#### <a name="azkusto"></a>Az.Kusto
* 正式發行 'Az.Kusto' 模組

#### <a name="aznetwork"></a>Az.Network
* [重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞
    - 'New-AzVirtualRouter'： 
        - 已新增 -HostedSubnet 參數來支援 IP 設定子資源
        - 已刪除 -HostedGateway 和 -HostedGatewayId
    - 'Get-AzVirtualRouter'：
        - 已新增訂用帳戶層級參數集
    - 'Remove-AzVirtualRouter'
    - 'Add-AzVirtualRouterPeer'
    - 'Get-AzVirtualRouterPeer'
    - 'Remove-AzVirtualRouterPeer'
* 已新增 Azure 快速路由連接埠的 Cmdlet
    - 'New-AzExpressRoutePortLOA'
* 已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源
* 已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。
* 已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出
* 已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]
* 已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'
* 已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。
- 已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。
- 已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。
* 已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。
* 已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。
* 已更新 'Set-AzVirtualNetworkSubnetConfig'
    - 如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已修正工作負載備份項目的刪除狀態。

#### <a name="azresources"></a>Az.Resources
* 已新增 Set-AzRoleAssignment 的遺漏檢查
* 已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數
* 已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更
* 已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 已新增適用於受控叢集和節點類型的 Cmdlet：
    - 'New-AzServiceFabricManagedCluster'
    - 'Get-AzServiceFabricManagedCluster'
    - 'Set-AzServiceFabricManagedCluster'
    - 'Remove-AzServiceFabricManagedCluster'
    - 'Add-AzServiceFabricManagedClusterClientCertificate'
    - 'Remove-AzServiceFabricManagedClusterClientCertificate'
    - 'New-AzServiceFabricManagedNodeType'
    - 'Get-AzServiceFabricManagedNodeType'
    - 'Set-AzServiceFabricManagedNodeType'
    - 'Remove-AzServiceFabricManagedNodeType'
    - 'Add-AzServiceFabricManagedNodeTypeVMExtension'
    - 'Add-AzServiceFabricManagedNodeTypeVMSecret'
    - 'Remove-AzServiceFabricManagedNodeTypeVMExtension'
    - 'Restart-AzServiceFabricManagedNodeTyp'
* 已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。

#### <a name="azsql"></a>Az.Sql
* 已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'
* 已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'
* 已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'
* 已將 Force 參數新增至 'New-AzSqlInstance'
* 已新增受控資料庫記錄重新執行服務的 Cmdlet
    - 'Start-AzSqlInstanceDatabaseLogReplay'
    - 'Get-AzSqlInstanceDatabaseLogReplay'
    - 'Complete-AzSqlInstanceDatabaseLogReplay'
    - 'Stop-AzSqlInstanceDatabaseLogReplay'
* 已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'
* 已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'
* 已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'
* 已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能
* 已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'
* 已更新資料庫 Cmdlet 以支援備份儲存體類型規格
* 已將 Force 參數新增至 'New-AzSqlDatabase'
* 已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告
* 已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject

#### <a name="azstorage"></a>Az.Storage
* 已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]
* 支援時間點還原
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - 'New-AzStorageBlobRangeToRestore'
    - 'Restore-AzStorageBlobRange'
* 支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態 
    - 'Get-AzureRMStorageAccount'
* 已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息
    - 'Get-AzStorageContainerStoredAccessPolicy'
    - 'Set-AzStorageContainerStoredAccessPolicy'
    - 'Set-AzStorageAccountManagementPolicy'
    - 'Get-AzStorageAccountManagementPolicy'
    - 'Add-AzStorageAccountManagementPolicyAction'
    - 'New-AzStorageAccountManagementPolicyRule'
* 已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8

### <a name="thanks-to-our-community-contributors"></a>感謝我們的社群參與者
* Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911) 
* Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807) 
* Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828) 
* Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833) 
* @jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351) 
* @hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784) 
* Joshua Van Daalen (@greenSacrifice)
  * 將 Property 的拼寫更新為 Property (#12821) 
  * 更新 New-AzResourceLock.md 範例 (#12806)
* Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825) 
* @rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)

## <a name="461---august-2020"></a>4.6.1 - 2020 年8 月
#### <a name="azcompute"></a>Az.Compute
* 已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]

## <a name="460---august-2020"></a>4.6.0 - 2020 年8 月
#### <a name="azaccounts"></a>Az.Accounts
* 當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]
* 在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]

#### <a name="azautomation"></a>Az.Automation
* 已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組

#### <a name="azcompute"></a>Az.Compute
* 已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'
* 已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件
* 已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數
* 已新增 'Invoke-AzVmPatchAssessment' Cmdlet

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將遺漏屬性新增至 PSPipelineRun 類別。

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援建立具有主機加密功能的叢集。

#### <a name="azkeyvault"></a>Az.KeyVault
* 已新增打算停用虛刪除的警告訊息
* 已新增打算移除 SecretValueText 屬性的警告訊息

#### <a name="azmaintenance"></a>Az.Maintenance
* 已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'
* 已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet

#### <a name="azmanagedservices"></a>Az.ManagedServices
* 已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告

#### <a name="azmonitor"></a>Az.Monitor
* 已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]
* 已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤

#### <a name="azresources"></a>Az.Resources
* 已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。
* 已建立新的 'Set-AzRoleAssignment' Cmdlet
* 已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果
* 已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果
* 已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果
* 已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和 
* 已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]
* 已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性

#### <a name="azsignalr"></a>Az.SignalR
* 已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤
* 已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet

#### <a name="azstorage"></a>Az.Storage
* 支援的 Blob 查詢加速
    -  'Get-AzStorageBlobQueryResult'
    -  'New-AzStorageBlobQueryConfig'
* 已更新說明檔、新增更多描述及修正錯字
    -  'Start-AzStorageBlobCopy'
    -  'Get-AzDataLakeGen2Item'
* 已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]
    -  'Get-AzStorageBlobContent'
* 支援在儲存體帳戶上設定/取得/移除物件複寫原則
    - 'New-AzStorageObjectReplicationPolicyRule'
    - 'Set-AzStorageObjectReplicationPolicy'
    - 'Get-AzStorageObjectReplicationPolicy'
    - 'Remove-AzStorageObjectReplicationPolicy'
* 支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed
    - 'Update-AzStorageBlobServiceProperty'

## <a name="450---august-2020"></a>4.5.0 - 2020 年 8 月
#### <a name="azaccounts"></a>Az.Accounts
* 已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]
* 已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]
* 訂用帳戶支援的主租用戶和 managedBy 租用戶資訊
* 已更正遙測資料中的模組名稱、版本資訊
* 已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)

#### <a name="azaks"></a>Az.Aks
* 已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。
* 已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。

#### <a name="azapimanagement"></a>Az.ApiManagement
* 已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。
* 已新增新的 'Get-AzApiManagementGateway' Cmdlet。
* 已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。
* 已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。
* 已新增新的 'New-AzApiManagementGateway' Cmdlet。
* 已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。
* 已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。
* 已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。
* 已新增新的 'Remove-AzApiManagementGateway' Cmdlet。
* 已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。
* 已新增新的 'Update-AzApiManagementGateway' Cmdlet。
* 已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已特別將 'Deny' 作為 NetworkRules 預設動作使用。

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援使用傳輸中加密功能建立叢集。
    - 將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'
    - 將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'
* 支援使用私人連結功能建立叢集：
    - 將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'
    - 將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'
* 呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊

#### <a name="aznetwork"></a>Az.Network
* 已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'
* 已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。
* 程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。
* 已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項
* 已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'
* 已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已改善 Azure 備份容器/項目探索體驗。

#### <a name="azresources"></a>Az.Resources
* 已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'
    - 這包括資料模型的所有相關變更

#### <a name="azsql"></a>Az.Sql
* 已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤
* 已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱

#### <a name="azstorage"></a>Az.Storage
* 支援建立具有新權限 x、t 的容器/blob Sas 權杖
    -  'New-AzStorageBlobSASToken'
    -  'New-AzStorageContainerSASToken'
* 支援建立具有新權限 x、t、f 的帳戶 Sas 權杖
    -  'New-AzStorageAccountSASToken'
* 支援取得單一檔案共用使用方式
    - 'Get-AzRmStorageShare'

## <a name="440---july-2020"></a>4.4.0 - 2020 年 7 月
#### <a name="azaccounts"></a>Az.Accounts
* 已新增新的 Cmdlet 'Invoke-AzRestMethod'
* 已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]

#### <a name="azaks"></a>Az.Aks
* 已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* 已移除驗證的專案參考

#### <a name="azautomation"></a>Az.Automation
* 已修正具有 escape 字元的字串無法轉換成 json 物件的問題。

#### <a name="azcompute"></a>Az.Compute
* 在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將全域參數新增至 Data Factory。

#### <a name="azeventgrid"></a>Az.EventGrid
* 已更新為使用 2020-06-01 API 版本。
* 加入新功能：
    - 輸入對應
    - 事件傳遞結構描述
    - 私人連結
    - 雲端事件 V10 結構描述
    - 將服務匯流排主題作為目的地
    - 將 Azure Function 作為目的地
    - WebHook 批次處理
    - 安全 Webhook (AAD 支援)
    - IpFiltering
* 已更新的 Cmdlet：
    - 'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':
        - 新增選擇性參數以支援 webhook 批次處理。
        - 新增選擇性參數以使用 AAD 支援安全的 Wdblook。
        - 為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。
        - 為傳遞結構描述新增選擇性參數。
    - 'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':
        - 新增選擇性參數以支援 IpFiltering。
    - 'New-AzEventGridTopic'/'New-AzEventGridDomain':
        - 新增選擇性參數以支援輸入對應。

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 已更新模組以使用 API 2020-05-01
* 已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。

#### <a name="azmonitor"></a>Az.Monitor
* 已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]

#### <a name="aznetwork"></a>Az.Network
* 已修正 VWan HubVnet 連線中的參數交換
* 為 Azure 網路虛擬設備網站新增了 Cmdlet
    - 'Get-AzVirtualApplianceSite'
    - 'New-AzVirtualApplianceSite'
    - 'Remove-AzVirtualApplianceSite'
    - 'Update-AzVirtualApplianceSite'
    - 'New-AzOffice365PolicyProperty'
* 為 Azure 網路虛擬設備新增了 Cmdlet
    - 'Get-AzNetworkVirtualAppliance'
    - 'New-AzNetworkVirtualAppliance'
    - 'Remove-AzNetworkVirtualAppliance'
    - 'Update-AzNetworkVirtualAppliance'
    - 'Get-AzNetworkVirtualApplianceSku'
    - 'New-AzVirtualApplianceSkuProperty'
* 將應用程式閘道上架至私人連結通用 Cmdlet
* 將 StorageSync 上架至私人連結通用 Cmdlet
* 將 SignalR 上架至私人連結通用 Cmdlet

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已移除驗證的專案參考
* Azure 備份微調的 Cmdlet 有助於文字更精確。
* Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。

#### <a name="azresources"></a>Az.Resources
* 已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。
* 已新增 'Unregister-AzResourceProvider' Cmdlet。

#### <a name="azsql"></a>Az.Sql
* 在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援
* 已修正資料分類 Cmdlet 中的錯誤 (bug)。
* 已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'

#### <a name="azstorage"></a>Az.Storage
* 已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。
* 支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶
    -  'New-AzStorageAccount'
    -  'Set-AzStorageAccount'
* 支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制
    - 'Update-AzStorageBlobServiceProperty'
* 支援 Blob 版本的列出 Blob
    - 'Get-AzStorageBlob'
* 支援取得/移除單一 Blob 快照集或 Blob 版本
    - 'Get-AzStorageBlob'
    - 'Remove-AzStorageBlob'
* 支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道
    - 'Get-AzStorageBlobContent'
    - 'New-AzStorageBlobSASToken'
    - 'Remove-AzStorageBlob'
    - 'Set-AzStorageBlobContent'
    - 'Start-AzStorageBlobCopy'

#### <a name="azstoragesync"></a>Az.StorageSync
* 新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK
* 已新增更新儲存體同步服務 Cmdlet
    - 'Set-AzStorageSyncService'
* 已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。

#### <a name="azwebsites"></a>Az.Websites
* 已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業

## <a name="430---june-2020"></a>4.3.0 - 2020 年 6 月
#### <a name="azaccounts"></a>Az.Accounts
* 預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境
* 更新預先載入的組件 [#12024]、[#11976]
* 已更新 Azure.Core 組件
* 已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]

#### <a name="azaks"></a>Az.Aks
* 透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式

#### <a name="azbatch"></a>Az.Batch
* 已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0
* 新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 支援的顯示帳戶功能。
* 支援修改 PublicNetworkAccess。

#### <a name="azcompute"></a>Az.Compute
* 已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。
* 已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。
* 已將子狀態新增至 VMCustomScriptExtension [#11297]
* 已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。
* 已修正適用於 SAP 的新 VM 擴充功能名稱

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 4.9.0

#### <a name="azeventhub"></a>Az.EventHub
* 已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet

#### <a name="azfunctions"></a>Az.Functions
* 已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援的清單主機和重新開機 HDInsight 叢集的特定主機。

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* 已將 SDK 版本更新為 1.1.0
* 已新增匯出設定和受控識別的支援

#### <a name="azmonitor"></a>Az.Monitor
* 已修正 'Set-AzActivityLogAlert' 的輸入物件參數
* 已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]

#### <a name="aznetwork"></a>Az.Network
* 已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'
* 已新增 Azure FirewallPolicy 的新 Cmdlet
    - 'New-AzFirewallPolicyDnsSetting'
    - 在防火牆原則的網路規則中支援目的地 FQDN
* 已新增對後端位址集區作業的支援
    - 'New-AzLoadBalancerBackendAddressConfig'
    - 'New-AzLoadBalancerBackendAddressPool'
    - 'Set-AzLoadBalancerBackendAddressPool'
    - 'Remove-AzLoadBalancerBackendAddressPool'
    - 'Get-AzLoadBalancerBackendAddressPool'
* 已新增 ' New-AzIpGroup' 的名稱驗證
* 已新增 Azure FirewallPolicy 的新 Cmdlet
    - 'New-AzFirewallPolicyThreatIntelWhitelist'
* 已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。
    - 已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。
    - 已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。
* 已更新 'Update-AzVpnGateway'
    - 已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。
* 已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：
    - 'Reset-AzHubRouter'
* 已根據防火牆原則的最近 Swagger 變更更新下列事項
    - 變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱
    - 已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合
* [重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。
* [重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。
* [重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。
* [重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。
* 已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink
    - 'New-AzApplicationGatewayPrivateLinkConfiguration'
    - 'Get-AzApplicationGatewayPrivateLinkConfiguration'
    - 'New-AzApplicationGatewayPrivateLinkConfiguration'
    - 'Set-AzApplicationGatewayPrivateLinkConfiguration'
    - 'Remove-AzApplicationGatewayPrivateLinkConfiguration'
    - 'New-AzApplicationGatewayPrivateLinkIpConfiguration'
* 已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。
    - 'New-AzVHubRoute'
    - 'New-AzVHubRouteTable'
    - 'Get-AzVHubRouteTable'
    - 'Update-AzVHubRouteTable'
    - 'Remove-AzVHubRouteTable'
* 已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。
    - 'New-AzExpressRouteConnection'
    - 'Set-AzExpressRouteConnection'
    - 'New-AzVirtualHubVnetConnection'
    - 'Update-AzVirtualHubVnetConnection'
    - 'New-AzVpnConnection'
    - 'Update-AzVpnConnection'
    - 'New-AzP2sVpnGateway'
    - 'Update-AzP2sVpnGateway'

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]
* 已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集 
* 已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至
    - 'New-AzOperationalInsightsSavedSearch'
    - 'Set-AzOperationalInsightsSavedSearch'

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure 備份新增了提取 MAB 項目的支援。
* Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'

#### <a name="azresources"></a>Az.Resources
* 已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]
* 已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]
* 已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'
* 已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'
* 已更新 'Test-Az*Deployment' Cmdlet，以顯示更好的錯誤訊息
* 已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息

#### <a name="azsql"></a>Az.Sql
* 已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援
* 已修正資料分類 Cmdlet 中的同步處理問題。
* 支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]

#### <a name="azstorage"></a>Az.Storage
* 支援使用 RequireInfrastructureEncryption 建立儲存體帳戶
    -  'New-AzStorageAccount'
* 已將載入 Azure.Core 的邏輯移至 Az.Accounts

#### <a name="azwebsites"></a>Az.Websites
* 已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)
* 已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'
* 已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)
* 已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)
* 已新增為 Linux 應用程式建立 ASP 的支援
* 已在資源群組中新增複製的例外狀況

## <a name="420---june-2020"></a>4.2.0 - 2020 年 6 月
#### <a name="azaccounts"></a>Az.Accounts
* 已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* 已更新資料平面 Cmdlet 的組件版本

#### <a name="azapimanagement"></a>Az.ApiManagement
* 已更新服務管理 Cmdlet 的組件版本

#### <a name="azbilling"></a>Az.Billing
* 已更新耗用量 Cmdlet 的組件版本

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。 

#### <a name="azdatafactory"></a>Az.DataFactory
* 已更新資料處理站 V2 Cmdlet 的組件版本

#### <a name="azdatashare"></a>Az.DataShare
* ''Az.DataShare'' 模組正式發行

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* ''Az.DesktopVirtualization'' 模組正式發行

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 已將 SDK 升級至 0.21.0
* 已將選用參數新增至 
    - 'New-AzOperationalInsightsSavedSearch'
    - 'Set-AzOperationalInsightsSavedSearch'

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 已更正 'Start-AzPolicyComplianceScan' 的範例 3

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* 已更新 PowerBI Cmdlet 的組件版本

#### <a name="azprivatedns"></a>Az.PrivateDns
* 已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。
* 已更新 SiteRecovery 和備份 Cmdlet 的組件版本

#### <a name="azresources"></a>Az.Resources
* 已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet
* 已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上
* 已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject
* 已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。
* 已更新資源管理員和標記 Cmdlet 的組件版本

#### <a name="azsql"></a>Az.Sql
* 已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'
* 已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'
* 已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet

#### <a name="azstorage"></a>Az.Storage
* 已更新資料平面 Cmdlet 的組件版本

## <a name="410---may-2020"></a>4.1.0 - 2020 年 5 月
### <a name="highlights-since-the-last-release"></a>上次發佈版本之後的更新重點
* 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7
* Az.Functions 正式發行 
* Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本

#### <a name="azaccounts"></a>Az.Accounts
* 已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數
* 已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+

#### <a name="azaks"></a>Az.Aks
* 已將 API 版本升級至 2019-10-01
* 支援使用 Windows 容器建立 AKS
* 已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'

#### <a name="azapimanagement"></a>Az.ApiManagement
* 'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]
* 'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]
* 'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。 PropertyId 參數已重新命名為 NamedValueId。
* 'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。 PropertyId 參數已重新命名為 NamedValueId。 
* 'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。 PropertyId 參數已重新命名為 NamedValueId。
* 'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。 PropertyId 參數已重新命名為 NamedValueId。
* 新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。
* 新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。
* 新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。
* 新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。
* 新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。
* 新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* 新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'
* 已建立 Cmdlet 'Update-AzApplicationInsights'
* 已針對連結的儲存體帳戶建立 Cmdlet

#### <a name="azbatch"></a>Az.Batch
* 已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。
* 已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。
* 已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。
  - 現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。 例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。
* 使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。
* 使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。
  - 'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。 只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。

#### <a name="azcompute"></a>Az.Compute
* 已將 HostId 參數新增至 'Update-AzVM' Cmdlet
* 已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。
* 重大變更
    - 已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。
    - 已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。
    - 已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。
    - 已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。
    - 已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。
    - AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。
* 已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。 

#### <a name="azdatafactory"></a>Az.DataFactory
* 支援受控 IR 中資料流程執行階段屬性的 CRUD。

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet
* 已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet
* 已將規則引擎參考新增至 Front Door 路由規則物件。
* 已將私人連結參數新增至 Front Door 後端物件

#### <a name="azfunctions"></a>Az.Functions
* ''Az.Functions'' 模組正式發行

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援客戶管理的金鑰磁碟加密。

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* 存取原則不再預設為目前的主體

#### <a name="aziothub"></a>Az.IotHub
* 已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。
* 已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]
* 已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。
* 已新增 Cmdlet 來叫用設定計量查詢。
* 管理大規模的 IoT Edge 自動部署。 這些新 Cmdlet 包括：
    - 'Add-AzIotHubDeployment'
    - 'Get-AzIotHubDeployment'
    - 'Remove-AzIotHubDeployment'
    - 'Set-AzIotHubDeployment'
* 已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。
* 已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。

#### <a name="azkeyvault"></a>Az.KeyVault
* 已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'
* 建立金鑰保存庫時，依預設會啟用虛刪除
* 在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具
* 已新增攜帶您自己的金鑰 (BYOK) 的支援
    - 'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰
    - 'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰
* 已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分

#### <a name="azmonitor"></a>Az.Monitor
* 已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]
* 計量警示 V2 支援 WebTest 可用性準則
    - 'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項
    - 'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則
* 已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]
* 已移除 PSEventData 中定義的備援屬性 [#11353]
* 已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'

#### <a name="aznetwork"></a>Az.Network
* 已新增重大變更屬性，以通知區域預設行為將會變更
    - 'New-AzPublicIpAddress'
    - 'New-AzPublicIpPrefix'
    - 'New-AzLoadBalancerFrontendIpConfig'
* 已新增最上層資源 SecurityPartnerProvider 的支援
    - 已新增新的 Cmdlet：
        - New-AzSecurityPartnerProvider
        - Remove-AzSecurityPartnerProvider
        - Get-AzSecurityPartnerProvider
        - Set-AzSecurityPartnerProvider
* 已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'
* 已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型
* 已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。
    - 'New-AzVirtualWan'
    - 'Update-AzVirtualWan'
* 已新增 Cmdlet 來支援私人端點的 DNS 區域群組
    - 'New-AzPrivateDnsZoneConfig'
    - 'Get-AzPrivateDnsZoneGroup'
    - 'New-AzPrivateDnsZoneGroup'
    - 'Set-AzPrivateDnsZoneGroup'
    - 'Remove-AzPrivateDnsZoneGroup'
* 已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'
* 已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'
    - 已更新 Cmdlet：
        - New-AzFirewall

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 已更新舊版程式碼以套用新產生的 SDK
* 由於已取代 API，刪除了 Cmdlet
    - 'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')
    - 'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')
    - 'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')
* 已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數
* 已針對連結的儲存體帳戶建立 Cmdlet
* 已針對叢集和連結服務建立 Cmdlet

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。
* Azure Site Recovery 已將區域的支援新增至區域複本。
* Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。
* Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。
* 已針對站台復原服務新增保存庫認證檔的私人端點。

#### <a name="azresources"></a>Az.Resources
* 已新增有關在建立新角色定義時檢視延遲的訊息警告
* 已變更原則 Cmdlet 以輸出強型別物件
* 已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]
* 已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]
* 已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'
* 已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'
   - Alias:'Get-AzSubscriptionDeploymentWhatIf'
* 已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果
* 已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息
* 已新增為部署失敗顯示已改善錯誤訊息的功能
* 已新增針對部署失敗記錄的 correlationId
* 已將 'error' 屬性新增至部署指令碼輸出
* 已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'
* 當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例
* 已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded
* 已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：
    - 'New-AzDeployment'
    - 'New-AzManagementGroupDeployment'
    - 'New-AzResourceGroupDeployment'
    - 'New-AzTenantDeployment'

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋

#### <a name="azsql"></a>Az.Sql
* 增強下列項目的效能：
    - 'Set-AzSqlDatabaseSensitivityClassification'
    - 'Set-AzSqlInstanceDatabaseSensitivityClassification'
    - 'Remove-AzSqlDatabaseSensitivityClassification'
    - 'Remove-AzSqlInstanceDatabaseSensitivityClassification'
    - 'Enable-AzSqlDatabaseSensitivityRecommendation'
    - 'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'
    - 'Disable-AzSqlDatabaseSensitivityRecommendation'
    - 'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'
* 已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證
* 在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。

#### <a name="azstorage"></a>Az.Storage
* 已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'
* 使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目
    - 'Set-AzStorageAccount'
* 已修正由於管道無法移除 Azure 檔案目錄的問題
    - 'Remove-AzStorageDirectory'
* 已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。
    - 'Update-AzStorageAccountNetworkRuleSet'
    - 'Get-AzStorageAccountNetworkRuleSet'
* 已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗
    - 'Add-AzStorageAccountNetworkRule'
* 已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7
* 已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出
    - 'Get-AzDataLakeGen2ChildItem'
* 已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶
    -  'New-AzStorageAccount'
    -  'Set-AzStorageAccount'
* 支援新增或列出儲存體帳戶的 Kerberos 金鑰
    -  'New-AzStorageAccountKey'
    -  'Get-AzStorageAccountKey'
* 支援容錯移轉儲存體帳戶
    - 'Invoke-AzStorageAccountFailover'
* 已更新 'Get-AzStorageBlobCopyState' 的說明
* 已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明
* 已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet
* 已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性
    - 'Get-AzStorageFile'
    - 'Remove-AzStorageFile'
    - 'Get-AzStorageFileContent'
    - 'Set-AzStorageFileContent'
    - 'Start-AzStorageFileCopy'
* 已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性
    - 'New-AzStorageDirectory'
    - 'Remove-AzStorageDirectory'
* 已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性
    - 'Get-AzStorageShare'
    - 'New-AzStorageShare'
    - 'Remove-AzStorageShare'
* 已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性
    - 'Set-AzStorageShareQuota'

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* 已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱

#### <a name="azwebsites"></a>Az.Websites
* 已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。

## <a name="380---april-2020"></a>3.8.0 - 2020 年 4 月
### <a name="highlights-since-the-last-release"></a>上次發佈版本之後的更新重點
* Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7

#### <a name="azaccounts"></a>Az.Accounts
* 更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]

#### <a name="azapimanagement"></a>Az.ApiManagement
* 在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知
* 'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數

#### <a name="azcdn"></a>Az.Cdn
* 已修正 ChinaCDN 相關的定價 SKU 顯示

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 支援身分識別、加密、UserOwnedStorage

#### <a name="azcompute"></a>Az.Compute
* 已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。
* 具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。

#### <a name="aziothub"></a>Az.IotHub
* 管理 IoT 裝置對應項設定，新的 Cmdlet 包括：
    - 'Get-AzIotHubDeviceTwin'
    - 'Update-AzIotHubDeviceTwin'
* 已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。
* 管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：
    - 'Get-AzIotHubModuleTwin'
    - 'Update-AzIotHubModuleTwin'
* 大規模管理 IoT 自動裝置管理設定。 這些新 Cmdlet 包括：
    - 'Add-AzIotHubConfiguration'
    - 'Get-AzIotHubConfiguration'
    - 'Remove-AzIotHubConfiguration'
    - 'Set-AzIotHubConfiguration'
* 已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。

#### <a name="azkeyvault"></a>Az.KeyVault
* 已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'
* 已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]
* 已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]
* 已將支援新增至私人端點

#### <a name="azmaintenance"></a>Az.Maintenance
* 發行用於 GA 的維護 Cmdlet 版本

#### <a name="azmonitor"></a>Az.Monitor
* 已新增私人連結範圍的 Cmdlet
    - 'Get-AzInsightsPrivateLinkScope'
    - 'Remove-AzInsightsPrivateLinkScope'
    - 'New-AzInsightsPrivateLinkScope'
    - 'Update-AzInsightsPrivateLinkScope'
    - 'Get-AzInsightsPrivateLinkScopedResource'
    - 'New-AzInsightsPrivateLinkScopedResource'
    - 'Remove-AzInsightsPrivateLinkScopedResource'

#### <a name="aznetwork"></a>Az.Network
* 已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。
    - 'New-AzVirtualNetworkGateway'
    - 'Set-AzVirtualNetworkGateway'
    - 'New-AzVirtualNetworkGatewayConnection'
    - 'Set-AzVirtualNetworkGatewayConnection'
* 已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites
    - 'New-AzLocalNetworkGateway'
    - 'New-AzVpnSiteLink'
* 已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)
    - 已新增 'Set-AzExpressRouteCircuitConnectionConfig'
        - 允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties
    - 已更新 'Add-AzExpressRouteCircuitConnectionConfig'
        - 已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列
* 已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet
* 已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性

#### <a name="azsql"></a>Az.Sql
* 已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet
* 支援對 VNet 中的儲存體帳戶進行稽核。

#### <a name="azstorage"></a>Az.Storage
* 在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知
* 建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS
    - 'New-AzStorageAccount'
    - 'Set-AzStorageAccount'
* 支援 DataLake Gen2
    - 'New-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2ChildItem'
    - 'Move-AzDataLakeGen2Item'
    - 'Set-AzDataLakeGen2ItemAclObject'
    - 'Update-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2ItemContent'
    - 'Remove-AzDataLakeGen2Item'

## <a name="0100-preview---april-2020"></a>0.10.0-preview - 2020 年 4 月
### <a name="general"></a>一般
* Az 模組現已在 Azure Stack Hub 中提供預覽。 此模組具有 Linux 和 macOs 的跨平台相容性。 Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)
* Az 模組支援 2019-03-01-hybrid 設定檔：
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* 已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub
* 命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az
* 您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結

## <a name="370---march-2020"></a>3.7.0 - 2020 年 3 月
#### <a name="azaccounts"></a>Az.Accounts
* 已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]

#### <a name="azcompute"></a>Az.Compute
* 已將下列參數新增至 'New-AzDiskConfig' Cmdlet：
    - DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference
* 允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。
* 已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。 [#11354]
* 已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet
    - 'Set-AzVMAEMExtension'
    - 'Get-AzVMAEMExtension'
    - 'Remove-AzVMAEMExtension'
    - 'Update-AzVMAEMExtension'
* 已修正說明文件範例中的錯誤
* 以表格格式顯示 VM PowerState 的確切字串值。
* 'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。 [#11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* 已將 ADF .Net SDK 版本更新為 4.8.0
* 已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述
* 已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項

#### <a name="azhdinsight"></a>Az.HDInsight
* 支援在建立叢集時指定支援的最低 TLS 版本。

#### <a name="aziothub"></a>Az.IotHub
* 已新增管理每一部裝置的分散式設定支援。 這些新 Cmdlet 包括：
    - 'Get-AzIotHubDistributedTracing'
    - 'Set-AzIotHubDistributedTracing'

#### <a name="azkeyvault"></a>Az.KeyVault
* 已將中斷性變更屬性新增至 'New-AzKeyVault'

#### <a name="azmonitor"></a>Az.Monitor
* 已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件

#### <a name="aznetwork"></a>Az.Network
* 已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections
    - 'New-AzVirtualHubVnetConnection'
    - 'Update-AzVirtualHubVnetConnection'
    - 'New-AzVirtualHub'
    - 'Update-AzVirtualHub'
* 已移除 SQL 管理 SDK 相依性

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 改善錯誤訊息

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。
* 已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視
* Azure 備份已新增針對失敗項目重試原則更新的支援。
* Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。
* Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援
* Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援

#### <a name="azresources"></a>Az.Resources
* 已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]
* 已新增對於錯誤案例的 correlationId 記錄
* 小型文件變更為 'Get-AzResourceLock'。 已新增範例。
* 已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]
* 已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet

#### <a name="azsql"></a>Az.Sql
* 已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'
* 已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'
* 已儲存在資料庫中分類資料行時的敏感度等級。

#### <a name="azsupport"></a>Az.Support
* 'Az.Support' 模組的一般可用性

#### <a name="azwebsites"></a>Az.Websites
* 已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援
    - 'Get-AzWebAppTrafficRouting'
    - 'Update-AzWebAppTrafficRouting'
    - 'Add-AzWebAppTrafficRouting'
    - 'Remove-AzWebAppTrafficRouting'

## <a name="361---march-2020"></a>3.6.1 - 2020 年 3 月
#### <a name="azaccounts"></a>Az.Accounts
* 在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]
* 在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]
* 已在 UserAgent 中新增 Az 版本

#### <a name="azapimanagement"></a>Az.ApiManagement
* 已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]
* 'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]
* 'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援
* 'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。

#### <a name="aziothub"></a>Az.IotHub
* 已新增在 IoT 中樞中管理裝置的支援。 這些新 Cmdlet 包括：
    - 'Add-AzIotHubDevice'
    - 'Get-AzIotHubDevice'
    - 'Remove-AzIotHubDevice'
    - 'Set-AzIotHubDevice'
* 已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。 這些新 Cmdlet 包括：
    - 'Add-AzIotHubModule'
    - 'Get-AzIotHubModule'
    - 'Remove-AzIotHubModule'
    - 'Set-AzIotHubModule'
* 已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。
* 已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。
* 已新增可取得/設定 IoT 裝置父系裝置的支援。 這些新 Cmdlet 包括：
    - 'Get-AzIotHubDeviceParent'
    - 'Set-AzIotHubDeviceParent'
* 已新增可管理裝置父子關聯性的支援。

#### <a name="azmonitor"></a>Az.Monitor
* 已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]

#### <a name="aznetwork"></a>Az.Network
* 已更新 Sql Management SDK。
* 已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。
    - 將欄位 ActionsRequired 對應至 ActionRequired。
* 已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'

#### <a name="azresources"></a>Az.Resources
* 已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)
* 已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]
* 已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]
* 已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]
* 已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)
* 已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性
* 已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選
* 已擴充標籤 Cmdlet 以接受 -ResourceId
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* 已新增標籤 Cmdlet
    - Update-AzTag -ResourceId
* 從 SDK 3.3.0 引進 ScopedDeployment

#### <a name="azsql"></a>Az.Sql
* 已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'
* 已針對受控資料庫新增對於長期保留備份設定的支援
    - 在受控資料庫上取得/設定 LTR 原則
    - 依受控資料庫、受控執行個體或位置取得 LTR 備份
    - 移除 LTR 備份
    - 還原 LTR 備份以建立新的受控資料庫
* 已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer
* 已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance
* 已提高適用於 Az.Network 的 SQL SDK 版本

#### <a name="azstorage"></a>Az.Storage
* 已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite
    - 'Set-AzRmStorageContainerImmutabilityPolicy'
* 已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息
    - 'New-AzStorageTable'
    - 'Get-AzStorageTable'

#### <a name="azwebsites"></a>Az.Websites
* 已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數
* 將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet
* 已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業
* 已將存取限制套用至不同資源群組中的 WebApp/函式
* 已修正為 WebAppSlots 設定自訂主機名稱的問題

## <a name="350---february-2020"></a>3.5.0 - 2020 年 2 月
### <a name="highlights-since-the-last-major-release"></a>上次發佈主要版本之後的更新重點
* 更新用戶端遙測。
* Az.IotHub 已新增 Cmdlet 來支援裝置管理。
* Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。

#### <a name="azaccounts"></a>Az.Accounts
* 已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料

#### <a name="azautomation"></a>Az.Automation
* 已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 已將 SDK 更新至 7.0
* 已改善伺服器回應空白主體時的錯誤訊息

#### <a name="azcompute"></a>Az.Compute
* 已允許 ProximityPlacementGroupId 在更新期間為空白值

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義

#### <a name="aziothub"></a>Az.IotHub
* 已新增在 IoT 中樞中管理裝置的支援。 這些新 Cmdlet 包括：
    - 'Add-AzIotHubDevice'
    - 'Get-AzIotHubDevice'
    - 'Remove-AzIotHubDevice'
    - 'Set-AzIotHubDevice'

#### <a name="azkeyvault"></a>Az.KeyVault
* 已修正 Add-AzKeyVaultKey.md 的重複文字

#### <a name="azmonitor"></a>Az.Monitor
* 已修正 Get-AzLog Cmdlet 的描述。
* 已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。
    - 使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。

#### <a name="aznetwork"></a>Az.Network
* 已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。
* 已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。
* 已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。
* 支援 VNet 防火牆上的 Azure 防火牆原則
    - 未新增任何 Cmdlet。 放寬 VNet 防火牆上的防火牆原則限制

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 已為 SQL Database 新增「還原為檔案」支援。

#### <a name="azresources"></a>Az.Resources
* 已重構範本部署 Cmdlet
    - 已新增用於在管理群組上管理部署的 Cmdlet：*-AzManagementGroupDeployment
    - 已新增用於在租用戶範圍上管理部署的 Cmdlet：*-AzTenantDeployment
    - 已重構 *-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作
    - 為 *-AzDeployment Cmdlet 建立別名 *-AzSubscriptionDeployment
* 已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'
* 已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。
* 已重新產生說明檔

#### <a name="azsql"></a>Az.Sql
* 已在受控執行個體上新增跨訂用帳戶的時間點還原支援。
* 已新增變更現有 SQL 受控執行個體硬體世代的支援
* 已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* 已新增用於可用性群組接聽程式的 Cmdlet

#### <a name="azstoragesync"></a>Az.StorageSync
* 已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。

## <a name="340---february-2020"></a>3.4.0 - 2020 年 2 月
### <a name="highlights-since-the-last-major-release"></a>上次發佈主要版本之後的更新重點
* Az.CosmosDB 初始版本 0.1.0 已發行
* Az.Network ConnectionMonitor V2 支援已新增

#### <a name="azaccounts"></a>Az.Accounts
* 當 AzureRmContext.json 無法使用時，停用內容自動儲存
* 將 Azure Powershell Common 的參考更新至 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct**
  - https://github.com/Azure/azure-powershell/issues/10472 的修正文件
* **Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl

#### <a name="azcompute"></a>Az.Compute
* 將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。
* 新增 Update-AzDiskEncryptionSet Cmdlet
* 將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：
    - New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig
* 將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。

#### <a name="azdatafactory"></a>Az.DataFactory
* 將 ADF .Net SDK 版本更新為 4.7.0

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* 新增資源的 LIST 作業
* 新增執行健康情況檢查步驟作業的功能

#### <a name="azhdinsight"></a>Az.HDInsight
* 修正 New-AzHDInsightCluster 的文件錯誤。

#### <a name="azkeyvault"></a>Az.KeyVault
* 將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。

#### <a name="aznetwork"></a>Az.Network
* 新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。
* 新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP
    - 更新了 New-AzFirewall Cmdlet：
        - 已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)
        - 已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'
* 已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。
* 已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。
* 已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援
    - 已新增新的 Cmdlet：
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - 使用選擇性參數 UrlConfiguration 更新的 Cmdlet
        - New-AzApplicationGatewayRewriteRuleActionSet
* 新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 支援在決定要補救的資源之前，評估合規性
    - 將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation
* 新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源
* 已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 支援移除已複寫的磁碟。
* Azure 備份在建立復原服務保存庫時新增了新增標記的支援。

#### <a name="azresources"></a>Az.Resources
* 以內容訂閱的預設值，讓 *-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性
* 新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例

#### <a name="azsql"></a>Az.Sql
修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。

#### <a name="azstorage"></a>Az.Storage
* 支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype
    - New-AzStorageAccount
* 在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId
* 修正 Cmdlet Start-AzStorageBlobCopy 的範例 6

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性
* 修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題

## <a name="330---january-2020"></a>3.3.0 - 2020 年 1 月
#### <a name="azaccounts"></a>Az.Accounts
* 已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數

#### <a name="azcdn"></a>Az.Cdn
* 在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料

#### <a name="azcompute"></a>Az.Compute
* 修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* 修正了 New-AzContainerGroup 範例所使用的參數名稱

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* 新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'
  - 取得 Edge 儲存體容器
* 新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'
  - 建立新的 Edge 儲存體容器
* 新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'
  - 移除 Edge 儲存體容器
* 新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'
  - 用來重新整理 Edge 儲存體容器資料的叫用動作
* 新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'
  - 取得 Edge 儲存體帳戶
* 新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'
  - 建立新的 Edge 儲存體帳戶
* 新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'
  - 移除 Edge 儲存體帳戶
* 叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'
  - 用來重新整理共用資料的叫用動作
* 新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'
  - 設定 az databoxedge 儲存體帳戶憑證

#### <a name="azdatafactory"></a>Az.DataFactory
* 新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性
* 將 ADF .Net SDK 版本更新為 4.6.0
* 為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* 移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結

#### <a name="azeventhub"></a>Az.EventHub
* 問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace

#### <a name="azhdinsight"></a>Az.HDInsight
* 修正 Invoke-AzHDInsightHiveJob.md 錯誤。

#### <a name="azmachinelearning"></a>Az.MachineLearning
* 由於不再提供 MachineLearningCompute，已移除下列 Cmdlet
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* 將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。
* Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。
* Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。
* Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。

#### <a name="azresources"></a>Az.Resources
* 修正 'Remove-AzTag' 說明文件中的錯誤。

#### <a name="azsql"></a>Az.Sql
* 修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。
* 修正建立 SQL 執行個體容錯移轉群組時的錯誤

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* 將 DR 新增為新的有效授權類型

#### <a name="azstorage"></a>Az.Storage
* 在後續版本中新增 DefaultAction 值變更的重大變更警告訊息
    - Update-AzStorageAccountNetworkRuleSet
* 使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 - 2019 年 12 月

### <a name="general"></a>一般
* 更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑

#### <a name="azaccounts"></a>Az.Accounts
* 針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent
* 當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息

#### <a name="azbatch"></a>Az.Batch
* 修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。

#### <a name="azdatafactory"></a>Az.DataFactory
* 將 ADF .Net SDK 版本更新為 4.5.0

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 已新增 WAF 受控規則排除支援
* 在自動完成中新增 SocketAddr

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* 例外狀況處理

#### <a name="azkeyvault"></a>Az.KeyVault
* 已修正存取可能未設定的值時發生的錯誤
* 橢圓曲線密碼編譯憑證管理
    - 已新增為憑證原則指定 Curve 的支援

#### <a name="azmonitor"></a>Az.Monitor
* 在 Add Diagnostic Settings 命令中新增選用的引數。 如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為 專用，資料類型)

#### <a name="aznetwork"></a>Az.Network
* 在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。

#### <a name="azresources"></a>Az.Resources
* 修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。
* 更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。

#### <a name="azsql"></a>Az.Sql
* 已將弱點評估自動啟用中的儲存體建立升級為 StorageV2

#### <a name="azstorage"></a>Az.Storage
* 支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* 支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖
    - Revoke-AzStorageAccountUserDelegationKeys
* 升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。
* 針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* 在參數 'Quota' 中新增參數別名 'QuotaGiB'
    - Set-AzStorageShareQuota
* 修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 - 2019 年 11 月
### <a name="highlights-since-the-last-major-release"></a>上次發佈主要版本之後的更新重點
* 已發佈 Az.DataBoxEdge 1.0.0
* 已發佈 Az.SqlVirtualMachine 1.0.0

#### <a name="azcompute"></a>Az.Compute
* VM Reapply 功能
    - 將 Reapply 參數新增到 Set-AzVM Cmdlet
* VM 擴展集 AutomaticRepairs 功能：
    - 將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss
* 適用於 New-AzVM 的跨租用戶資源庫映像支援
* 將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式
* 將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet
* 將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性
* 將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet
* 將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet
* 將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* 已新增 Cmdlet `Get-AzDataBoxEdgeOrder`
    - 取得訂單
* 已新增 Cmdlet `New-AzDataBoxEdgeOrder`
    - 建立新訂單
* 已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`
    - 移除訂單
* Cmdlet `New-AzDataBoxEdgeShare` 中的變更
    - 立即建立本機共用
* 已新增 Cmdlet `Set-AzDataBoxEdgeRole`
    - IotRole 現在對應到共用
* 已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`
    - 在裝置上叫用掃描更新、下載更新並安裝更新
* 已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`
    - 取得觸發程序的相關資訊
* 已新增 Cmdlet `New-AzDataBoxEdgeTrigger`
    - 建立新的觸發程序
* 已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`
    - 移除觸發程序

#### <a name="azdatafactory"></a>Az.DataFactory
* 將 ADF .Net SDK 版本更新為 4.4.0
* 為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件

#### <a name="azeventhub"></a>Az.EventHub
* 修正 10301 的問題：修正 SAS 權杖日期格式

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject
* 將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject
* 新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* 變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。

#### <a name="azprivatedns"></a>Az.PrivateDns
* 已將 PrivateDns .net SDK 更新為 1.0.0 版

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 支援在啟用保護時選取磁碟類型。
* Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。
* Azure 備份 SQL 還原支援接受 filestream DB.

#### <a name="azrediscache"></a>Az.RedisCache
* 已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。 此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。
* 已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證

#### <a name="azresources"></a>Az.Resources
- 更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。
- 更新了建立原則定義說明範例
- 修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。
- 修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。
- 將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。

#### <a name="azsql"></a>Az.Sql
* 新增了對 ReadReplicaCount 資料庫的支援。
* 修正了未設定區域備援時的 Set-AzSqlDatabase

## <a name="300---november-2019"></a>3.0.0 - 2019 年 11 月
### <a name="general"></a>一般
* 已發行 Az.PrivateDns 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* 為 'Resolve-Error' 別名新增了淘汰訊息。

#### <a name="azadvisor"></a>Az.Advisor
* 已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。

#### <a name="azbatch"></a>Az.Batch
* 已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。 另外還有新的 `LowPriorityCoreQuota`。
  - 這會影響 **Get-AzBatchAccount** 。
* **New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。
* 新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。 這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask** 。
  - 除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：
    - `AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。
    - `StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。
* 已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。
  - 您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。 例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。
* 將 **Get-AzBatchApplicationPackage** 、 **New-AzBatchApplicationPackage** 、 **Remove-AzBatchApplicationPackage** 、 **Get-AzBatchApplication** 、 **New-AzBatchApplication** 、 **Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。
  - `ApplicationId` 現在是 `ApplicationName` 的別名。
* 已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。
* 已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。
* 已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。
* 已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。
* 已移除 **AzBatchPoolOSVersion** 。 不再支援此作業。
* 已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。
* 已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。
* 已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。
* 已移除 **AzBatchNodeAgentSku** ，並以 **AzBatchSupportedImage** 取代。
  - **AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。
  - 系統現在也會傳回新的未驗證映像。 此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。
* 新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。
* 現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。 這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。
* 執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。 這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。
* 新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。 如此可確保集區中的節點將會有來自清單使用者所提供的 IP。
* 未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。
* 未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。

#### <a name="azcdn"></a>Az.Cdn
* 已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。
* 已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。

#### <a name="azcompute"></a>Az.Compute
* 磁碟加密集功能
    - 新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
    - DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig
* 將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig
* 將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定
* 將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet
* 重大變更
    - 上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB
    - 在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id

#### <a name="azdatafactory"></a>Az.DataFactory
* 將 ADF .Net SDK 版本更新為 4.3.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* 更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式
* 避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。
* 在 adlsclient 中公開每個要求超時設定
* 修正傳遞原始 syncflag 以進行 badoffset 復原
* 修正 EnumerateDirectory 以在檢查回應後取得接續權杖
* 修正 Concat 錯誤 (bug)

#### <a name="azfrontdoor"></a>Az.FrontDoor
* 修正了多個模組中的各種錯字問題

#### <a name="azhdinsight"></a>Az.HDInsight
* 修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。
* 將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。
* 已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0
* 已移除五個 Cmdlet：
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* 新增了三個 Cmdlet：
    - Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。
    - Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。
    - Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。
* 修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。
* 已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。
* 將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。
* 已變更下列 Cmdlet 的輸出類型：
*  - 已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。
*  - 已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。
*  - 已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。
* 已新增一些狀況測試案例。
* 移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.

#### <a name="aziothub"></a>Az.IotHub
* 重大變更：
    - Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。
    - 已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。
    - Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。
    - 已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。
    - 已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。
    - 已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。
    - Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。
    - Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。
    - Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。
    - 已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。
    - Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。
    - 已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。
* Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。
* Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。
* Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。
* Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。
* Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。
* Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。
* Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。
* 已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試

#### <a name="azresources"></a>Az.Resources
* 將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2

#### <a name="aznetwork"></a>Az.Network
* 變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。
    - 已更新 Cmdlet：
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* 為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。
    - 新的 cmdlet：
        - Get-AzPrivateLinkResource
* 新增功能 Proxy Protocol V2 的新欄位和參數。
    - 在 PrivateLinkService 中新增屬性 EnableProxyProtocol
    - 在 PrivateEndpointConnection 中新增屬性 LinkIdentifier
    - 更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。
* 修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述
* 新增 Cmdlet 以支援 Azure 防火牆原則
* 為 VirtualHub的子資源 RouteTables 新增支援
    - 已新增新的 Cmdlet：
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* 新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援
    - 已更新 Cmdlet 中的選用參數 -RewriteRuleSet：
        - New-AzVirtualHub：新增了參數 SKU
        - Update-AzVirtualHub：新增了參數 SKU
        - New-AzVirtualWan：新增了參數 VirtualWANType
        - Update-AzVirtualWan：新增了參數 VirtualWANType
* 為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援
    - 已新增新的 Cmdlet：
        - Update-AzureRmVirtualHubVnetConnection
    - 已更新 Cmdlet 中的選用參數 -RewriteRuleSet：
        - New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity
        - New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity
        - Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity
        - New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity
        - Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity
* 新增設定 TopLevel WebApplicationFirewall 原則的支援
    - 已新增新的 Cmdlet：
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - 已更新 Cmdlet 中的選用參數 -RewriteRuleSet：
        - New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule
* 已在 CustomRule 上新增對 Geo-Match 運算子的支援
    - 已將 GeoMatch 新增至 FirewallCondition 上的運算子
* 已新增 perListener 和 perSite 防火牆原則的支援
    - 已更新 Cmdlet 中的選用參數 -RewriteRuleSet：
        - New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId
        - New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId
* 將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫
* 支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN
* 為 IpGroup的上層資源 RouteTables 新增支援
    - 已新增新的 Cmdlet：
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。

#### <a name="azsql"></a>Az.Sql
* 已新增在受控執行個體上還原已卸載之資料庫的支援。
* 已從程式碼中淘汰舊版的審核 Cmdlet。
* 移除了已淘汰的別名：
* Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)
* Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)
* 移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet
* 移除已淘汰的弱點評估設定 Cmdlet 的別名
* 淘汰進階威脅偵測設定 Cmdlet
* 在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。

#### <a name="azstorage"></a>Az.Storage
* 支援在建立或更新儲存體帳戶時啟用大型檔案共用
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* 當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

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
* 已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* 針對接收器使用已啟用的一般警示結構描述。 這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器
* Webhooks 現在支援 Azure Active Directory 驗證。

#### <a name="aznetwork"></a>Az.Network
* 新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。
* 已在虛擬網路閘道連線新增了流量選取器的支援
    - 已新增新的 Cmdlet：
        - New-AzureRmTrafficSelectorPolicy
    - 已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
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
   - **ActionGroups** 要求的 api-version 現在為 **2019-06-01** ，之前為 **2018-03-01** 。 已針對此項變更新增多個案例測試。
   - **EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。 目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。 **注意** ：這是暫時性的變更，必須由警示小組驗證。
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
* 修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題
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
* 已更新 Cmdlet **New-AzApiManagement** ，用以管理 ApiManagement 服務
    - 已加入新的「使用量」SKU 的支援
    - 已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援
    - 新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。 這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。
    - 已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。
* 已更新 Cmdlet **Get-AzApiManagementSsoToken** ，以使用 'PsApiManagement' 物件作為輸入
* 已更新 Cmdlet 以顯示內嵌錯誤訊息
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]
* 已更新 Cmdlet **Export-AzApiManagementApi** ，以採用 'OpenApi 3.0' 格式匯出 API
* 已更新 Cmdlet **Import-AzApiManagementApi**
    - 以從 'OpenApi 3.0' 文件規格匯入 API
    - 以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。
    - 以覆寫任何文件中指定的 'ServiceUrl' 屬性。
* 已更新 Cmdlet **Get-AzApiManagementPolicy** ，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則
* 已更新 Cmdlet **Set-AzApiManagementPolicy** ，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則
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
