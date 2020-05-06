---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eecd66ddf433cc2543ceeaef1519d69179f2f099
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534462"
---
# <a name="release-notes"></a>版本資訊

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

這是此版本中對 Azure PowerShell 所做的變更清單。

---
## <a name="6130---november-2018"></a>6.13.0 - 2018 年 11 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 更新通用程式碼，以使用最新版 ClientRuntime

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 針對類型對應問題更新相依性

#### <a name="azurermautomation"></a>AzureRM.Automation
* 以 Swagger 為基礎的 Azure 自動化 Cmdlet
* 已新增更新管理 Cmdlet
* 已新增原始檔控制 Cmdlet
* 已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet
* 已修正 DSC 註冊節點命令

#### <a name="azurermcompute"></a>AzureRM.Compute
* 已修正 SystemAssigned 身分識別的身份識別問題
* 針對類型對應問題更新相依性

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 針對類型對應問題更新相依性

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* 更新市集 Cmdlet 的範例描述

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError
* 已將 ICMP 加回支援的 AzureFirewall 網路通訊協定
* 更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。 
* 修正 VirtualNetwork 對應中的記憶體使用量問題

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 提供修正程式以修改受保護的檔案共用原則。
* 已將原則時區轉換為大寫。

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例
* 針對類型對應問題更新相依性

#### <a name="azurermrelay"></a>AzureRM.Relay
* 已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。

#### <a name="azurermresources"></a>AzureRM.Resources
* 更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件
* 新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例
* 修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 針對即將推出的重大變更新增取代資訊

#### <a name="azurermsql"></a>AzureRM.Sql
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

## <a name="6120---november-2018"></a>6.12.0 - 2018 年 11 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 更新通用程式碼，以使用最新版 ClientRuntime
* 將 Cmdlet Connect-AzureRmAccount 中的 param TenantId 重新命名為 Tenant 並新增 TenantId 的別名
* 更新 Connect-AzureRmAccount 的 TenantId 說明
* 修正提供租用戶網域時登入失敗的錯誤訊息
    - https://github.com/Azure/azure-powershell/issues/6936
* 修正租用戶中無訂用帳戶之帳戶內容衝突的問題
    - https://github.com/Azure/azure-powershell/issues/7453
* 修正使用 MSI 時 DataLake 端點的問題
    - https://github.com/Azure/azure-powershell/issues/7462
* 修正若未連線，'Disconnect-AzureRmAccount' 會擲出錯誤的問題
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* 已將 Cmdlet DLL 檔案名稱重新命名為 Microsoft.Azure.Commands.Automation.dll

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 新增 Get-AzureRmCognitiveServicesAccountSkus 作業。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 新增 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk Cmdlet
* Get-AzureRmVMImage 顯示 AutomaticOSUpgradeProperties
* 已修正 SetAzureRmVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 將 DataLake 套件更新為 1.1.10。
* 將預設並行新增至多執行作業。

#### <a name="azurerminsights"></a>AzureRM.Insights
* 已修正問題 #7267 (自動調整區域)
    - 建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。
* 已修正問題 #7513 [Insights] Set-AzureRMDiagnosticSetting 在建立設定時需要明確的類別規格
    - 目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已將 PeeringType 變更為下列 Cmdlet 的必要參數：-
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 已新增原則修復 Cmdlet

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 已新增在復原服務中共用 Azure 檔案的支援。

#### <a name="azurermresources"></a>AzureRM.Resources
* 修正 https://github.com/Azure/azure-powershell/issues/7402
    - 允許使用 'Get-AzureRmResource' 的 '-ResourceId' 參數列出資源

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 修正將憑證新增至 Linux Vmss。
* 修正 'Add-AzureRmServiceFabricClusterCertificate'
    - 使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。
    - 正確顯示例外狀況 (Azure/service-fabric-issues#1054)。
* 修正 'Update-AzureRmServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。

## <a name="6110---october-2018"></a>6.11.0 - 2018 年 10 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 修正 CloudShell 中 Get-AzureRmSubscription 的問題
* 更新通用程式碼，以使用最新版 ClientRuntime

#### <a name="azurermbackup"></a>AzureRM.Backup
* 淘汰的 Azure 備份 Cmdlet。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzureRmVm' 的簡單參數集合時，將會開啟加速的網路
* 已將 ResourceName 引數完成器新增至所有 Cmdlet。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 新增虛擬網路規則的支援
    - Get-AzureRmDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 虛擬網路規則。
    - Add-AzureRmDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。
    - Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帳戶中修改指定的虛擬網路規則。
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 虛擬網路規則。

#### <a name="azurermnetwork"></a>AzureRM.Network
* 更新 Cmdlet Test-AzureRmNetworkWatcherConnectivity，將通訊協定值傳遞至後端。
* 已將 ResourceName 引數完成器新增至所有 Cmdlet。

#### <a name="azurermresources"></a>AzureRM.Resources
* 修正當 Get-AzureRMRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。 也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。

## <a name="6100---october-2018"></a>6.10.0 - 2018 年 10 月
#### <a name="azurestorage"></a>Azure.Storage
* 修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 在沒有現有帳戶的情況下支援 Get-AzureRmCognitiveServicesAccountSkus。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 修正 Get-AzureRmVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果
* 已將 'SimpleParameterSet' 的範例新增到 New-AzureRmVmss Cmdlet 說明中。
* 已修正 Azure 磁碟加密進度訊息中的錯字

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已將 ADF .Net SDK 版本更新為 2.3.0。

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已新增 NetworkProfile 功能。 已新增新的 Cmdlet
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* 已在子網路模型中新增服務關聯連結
* 已新增 New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap 和 Remove-AzureRmVirtualNetworkTap Cmdlet
* 已新增 Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig 和 Remove-AzureRmNEtworkInterfaceTapConfig Cmdlet

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 日後允許任何字串做為 Size 參數。 在 P5 PSArgumentCompleter 快顯視窗中新增 P5

#### <a name="azurermresources"></a>AzureRM.Resources
* 將遺漏的 -Mode 參數新增至 Set-AzureRmPolicyDefinition
* 修正 Get-AzureRmProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業

#### <a name="azurermsql"></a>AzureRM.Sql
* 已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題

#### <a name="azurermstorage"></a>AzureRM.Storage
* 支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL
* 新 Cmdlet New-AzureRMWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段

## <a name="690---september-2018"></a>6.9.0 - 2018 年 9 月
#### <a name="general"></a>一般
* 已將 AzureRM.SignalR 新增至 AzureRM 彙總模組

#### <a name="azurermprofile"></a>AzureRM.Profile
* 儲存體通用程式碼的小幅變更
* 已更新說明檔以包含完整的參數類型。
* 已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集 

#### <a name="azurestorage"></a>Azure.Storage
* 支援使用 OAuth 建立儲存體內容。 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 已在 CDN 定價 SKU 中新增 Standard_Microsoft。 

#### <a name="azurermcompute"></a>AzureRM.Compute
* 將金鑰保存庫和儲存體上的相依性移至一般相依性
* 對 AEM Cmdlet 新增更多的虛擬機器大小支援
* 將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig
* 將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt
* 新增 Invoke-AzureRmVmssVMRunCommand Cmdlet

#### <a name="azurermdns"></a>AzureRM.Dns
* 已新增建立 DNS 記錄時的別名記錄支援

#### <a name="azurerminsights"></a>AzureRM.Insights
* 已修正問題 #6833 和 #7102 (診斷設定區域)
    - 建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')
    - 以類別建立診斷設定的問題
* 已新增計量時間粒紋參數的取代訊息
    - Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效

#### <a name="azurermnetwork"></a>AzureRM.Network
* LoadBalancer Cmdlet 的變更
  - LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數
  - LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數
  - LoadBalancerRuleConfig：已新增 EnableTcpReset 參數
  - LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援
* 已為新 LoadBalancer 的子資源 OutboundRule 新增命令
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* 已為 PSNetworkInterface 新增 HostedWorkloads 屬性
* 已為以下功能新增 Cmdlet：由 ARM 支援的 Azure 防火牆
  - 已新增 Get-AzureRmFirewall
  - 已新增 Set-AzureRmFirewall
  - 已新增 New-AzureRmFirewall
  - 已新增 Remove-AzureRmFirewall
  - 已新增 New-AzureRmFirewallApplicationRuleCollection
  - 已新增 New-AzureRmFirewallApplicationRule
  - 已新增 New-AzureRmFirewallNatRuleCollection
  - 已新增 New-AzureRmFirewallNatRule
  - 已新增 New-AzureRmFirewallNetworkRuleCollection
  - 已新增 New-AzureRmFirewallNetworkRule
* 已在應用程式閘道中新增受信任根憑證和自動調整組態的支援
  - 已新增的 Cmdlet：
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - 已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - 已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* 為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet
* 已在子網路中新增多個位址前置詞的支援。 已更新的 Cmdlet：
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* 為子網路委派新增 Cmdlet。
  - New-AzureRmDelegation：建立可新增至子網路的新委派
  - Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱
  - Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 支援受控磁碟

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 已更新深入解析相依性。

#### <a name="azurermresources"></a>AzureRM.Resources
* 使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment
    - 使用新參數新增 OnErrorDeployment 的支援。
* 支援原則指派上的受控識別。
* 以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數
* 新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已修正問題 #7161

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* 將 SKU 名稱更新為 Free_F1 和 Standard_S1
* 將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。

#### <a name="azurermstorage"></a>AzureRM.Storage
* 在 AzureRm.Storage 中支援不變原則 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已新增兩個 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp
* New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案
* New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式

## <a name="681---august-2018"></a>6.8.1 - 2018 年 8 月
#### <a name="general"></a>一般
* 已修正未設定預設資源群組的問題。
* 已更新通用執行階段組件

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 已修正未設定預設資源群組的問題。
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6603
    - Import-AzureRmApiManagementApi 和 *-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6879
    - CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。 已藉由升級至 4.0.4-preview NuGet 而修正
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6853
    - 已修正依產品名稱搜尋的 Odata 篩選條件
* 已修正的問題 https://github.com/Azure/azure-powershell/issues/6814
    - 已修正依 API 名稱搜尋的 Odata 篩選條件
* 已新增對 AzureMonitor 記錄器的支援


#### <a name="azurermcompute"></a>AzureRM.Compute
* 已修正在錯誤輸出中遺漏目標的問題。
* 已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題
* 已修正未設定預設資源群組的問題。
* 修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已將預設的 Cmdlet 輸出表示法變更為資料表檢視

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤


#### <a name="azurermresources"></a>AzureRM.Resources
* 已修正從 MarketPlace 建立受控應用程式發生的問題。

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已修正的問題
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 已新增對 MultiValue 路由方法的支援
    - 為 MultiValue 路由新增 'MaxReturn' 參數
* 已新增對子網路路由方法的支援
    - 支援端點中的 IP 位址範圍 (子網路)
* 已新增對設定檔中自訂標頭的支援
* 已新增對設定檔中預期狀態碼的支援
* 已新增對端點中自訂標頭的支援

## <a name="680---august-2018"></a>6.8.0 - 2018 年 8 月
#### <a name="general"></a>一般
* 已修正未設定預設資源群組的問題。

#### <a name="azurermprofile"></a>AzureRM.Profile
* 已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖

#### <a name="azurermcompute"></a>AzureRM.Compute
* 已修正在錯誤輸出中遺漏目標的問題。
* 已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題
* 修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China

#### <a name="azurermiothub"></a>AzureRM.IotHub
* 修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已將預設模式表示法變更為資料表檢視

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤

#### <a name="azurermresources"></a>AzureRM.Resources
* 已修正從 MarketPlace 建立受控應用程式發生的問題。

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 修正問題
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 支援 MultiValue 路由方法
    - 為 MultiValue 路由新增 'MaxReturn' 參數
* 支援子網路路由方法
    - 支援端點中的 IP 位址範圍 (子網路)
* 支援設定檔中的自訂標頭
* 支援設定檔中的預期狀態碼
* 支援端點中的自訂標頭

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已修正未正確設定預設資源群組的問題。

## <a name="670---august-2018"></a>6.7.0 - 2018 年 8 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 已更新至最新版本的 Azure ClientRuntime。
* 將使用者識別碼新增至預設內容名稱，以避免內容發生衝突
    - https://github.com/Azure/azure-powershell/issues/6489
* 修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題
* 允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* 移除 Azure 檔案共用 5TB 的配額限制
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermautomation"></a>AzureRM.Automation
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermbackup"></a>AzureRM.Backup
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermbatch"></a>AzureRM.Batch
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermbilling"></a>AzureRM.Billing
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 已更新至最新版本的 Azure ClientRuntime。
* 將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig
* 若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。
* 修正 Save-AzureRmVMImage 中的參數描述
* 修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問
* 更新 Set-AzureRmDataLakeStoreItemAcl 範例
* 已更新至最新版本的 Azure ClientRuntime。
* 更新 Set-AzureRmDataLakeStoreItemAclEntry 範例

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermdns"></a>AzureRM.Dns
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurerminsights"></a>AzureRM.Insights
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermiothub"></a>AzureRM.IotHub
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermmedia"></a>AzureRM.Media
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已新增 Set-AzureRmLocalNetworkGateway 範例
* 已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述
* 已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例
* 已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例
* 已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例
* 已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例
* 已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage
* 已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。 命令會傳回受指定原則識別碼保護的備份項目清單。
* 已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。
* 已更新至最新版本的 Azure ClientRuntime。
* 已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。 受控磁碟還原的資源群組。 適用於具有受控磁碟的 VM 備份。

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermrelay"></a>AzureRM.Relay
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermresources"></a>AzureRM.Resources
* 支援在訂用帳戶範圍部署範本。 新增新的 Cmdlet：
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* 修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題
    - https://github.com/Azure/azure-powershell/issues/5705
* 修正 New-AzureRmResourceGroupDeployment 中的範例
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermsql"></a>AzureRM.Sql
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermstorage"></a>AzureRM.Storage
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermtags"></a>AzureRM.Tags
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* 已更新至最新版本的 Azure ClientRuntime。

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已更新至最新版本的 Azure ClientRuntime。

## <a name="660---july-2018"></a>6.6.0 - 2018 年 7 月
#### <a name="general"></a>一般
* 已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。

#### <a name="azurermprofile"></a>AzureRM.Profile
* 已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。
* 已將 ps1xml 類型新增至 Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* 已新增從 DefaultProfile 取得儲存體內容的支援
* 已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。

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
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

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
