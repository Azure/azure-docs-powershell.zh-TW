---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: bee7d63c06ab42e920eea750095facddb8f542d8
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534540"
---
# <a name="release-notes"></a>版本資訊

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

這是此版本中對 Azure PowerShell 所做的變更清單。

## <a name="20170925---version-440"></a>2017.09.25 - 版本 4.4.0
* AnalysisServices
  * 新增資料平面 commandlet，以允許將資料庫從讀寫執行個體同步處理至唯讀執行個體
    - 已包含 commandlet 的說明檔
    - 已新增記憶體內部測試和情節測試 (僅限即時)
  * 已修正 Add-AzureAsAccount commandlet 中的錯誤
* 自動化
  * 已修正先前版本中已修正過的 Cmdlet 說明文件。
  * 已新增 4 個新的 cmdlet 來支援 DSC 節點設定的分段推出。
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * 整合認知服務管理 SDK 2.0.0 版。
  * Get-AzureRmCognitiveServicesAccount 現在可正確支援分頁。
* 計算
  * 執行命令功能：
    - 新的 cmdlet：'Invoke-AzureRmVMRunCommand' 可叫用 VM 上的執行命令
    - 新的 cmdlet：'Get-AzureRmVMRunCommandDocument' 會顯示可用的執行命令文件
  * 將 'StorageAccountType' 參數新增至 Set-AzureRmDataDisk
  * 可用性區域支援虛擬機器、VM 擴展集和磁碟
    - 新的 參數：'Zone' 已新增至 New-AzureRmVM、New-AzureRmVMConfig、New-AzureRmVmssConfig、New-AzureRmDiskConfig
  * VM 擴展集輪流升級功能：
    - 新的 cmdlet：'Start-AzureRmVmssRollingOSUpgrade' 會叫用 VM 擴展集的 OS 輪流升級
    - 新的 cmdlet：'Set-AzureRmVmssRollingUpgradePolicy' 會設定 VM 擴展集輪流升級的升級原則。
    - 新的 cmdlet：'Stop-AzureRmVmssRollingUpgrade' 會取消 VM 擴展集的輪流升級
    - 新的 cmdlet：'Get-AzureRmVmssRollingUpgrade' 會顯示 VM 擴展集輪流升級的狀態。
  * 已針對系統指派的識別引進 AssignIdentity 切換參數。
    - 新的參數：'AssignIdentity' 已新增至 New-AzureRmVMConfig、New-AzureRmVmssConfig 和 Update-AzureRmVM
  * Vmss 磁碟加密功能：
    - 新的 cmdlet：'Set-AzureRmVmssDiskEncryptionExtension' 會啟用 VM 擴展集上的磁碟加密
    - 新的 cmdlet：'Disable-AzureRmVmssDiskEncryption' 會停用 VM 擴展集上的磁碟加密
    - 新的 cmdlet：'Get-AzureRmVmssDiskEncryptionStatus' 會顯示 VM 擴展集的磁碟加密狀態
    - 新的 cmdlet：'Get-AzureRmVmssVMDiskEncryptionStatus' 會顯示 VM 擴展集的磁碟加密狀態
* ContainerInstance
  * 新增 Azure Container 執行個體的 PowerShell Cmdlet
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* 深入解析
  * 新的 cmdlet Disable-AzureRmActivityLogAlert
    - 可停用現有活動記錄警示的新 cmdlet。
    - 也可選擇性地使用這個 Cmdlet 設定標記。
  * 新的 cmdlet Enable-AzureRmActivityLogAlert
    - 可啟用現有活動記錄警示的新 cmdlet。
    - 也可選擇性地使用這個 Cmdlet 設定標記。
  * 新的 cmdlet Get-AzureRmActivityLogAlert
    - 可取出一或多個活動記錄警示的新 cmdlet。
    - 可依名稱、資源群組或訂用帳戶來取出警示。
  * 新的 cmdlet New-AzureRmActionGroup
    - 可在記憶體中建立 ActionGroup 物件的新 cmdlet (不包含要求)。
  * 新的 cmdlet New-AzureRmActivityLogAlertCondition
    - 可在記憶體中建立活動記錄警示分葉條件物件的新 cmdlet (不包含要求)。
  * 新的 cmdlet Set-AzureRmActivityLogAlert
    - 可建立或更新活動記錄警示的新 cmdlet。
  * 新的 cmdlet Remove-AzureRmActivityLogAlert
    - 可移除一個活動記錄警示的新 cmdlet。
  * 新的 cmdlet Set-AzureRmActionGroup
    - 可建立新的或更新現有動作群組的新 cmdlet。
  * 新的 cmdlet Get-AzureRmActionGroup
    - 可取出一或多個動作群組的新 cmdlet。
    - 可依名稱、資源群組或訂用帳戶來取出動作群組。
  * 新的 cmdlet Remove-AzureRmActionGroup
    - 可移除一個動作群組的新 cmdlet。
  * 新的 cmdlet New-AzureRmActionGroupReceiver
    - 可在記憶體中建立新動作群組的新 cmdlet。
* KeyVault
  * 可支援 KeyVault 憑證 soft-delete 的新/更新 cmdlet
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* 網路
  * 已將端點服務的支援新增至虛擬網路子網路
    - 更新了 Add-AzureRmVirtualSubnetConfig：已新增選用參數 -ServiceEndpoint
    - 更新了 New-AzureRmVirtualSubnetConfig：已新增選用參數 -ServiceEndpoint
    - 更新了 Set-AzureRmVirtualSubnetConfig：已新增選用參數 -ServiceEndpoint
  * 已新增可列出位置中可用端點服務的 cmdlet
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * 已將可設定以 RADIUS 作為基礎的外部 P2S 驗證新增至下列 commandlet
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * 已新增可允許產生以 RADIUS 作為基礎的外部 P2S 之 VpnProfiles 的 cmdlet
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * 已將 SKU 參數的支援新增至公用 IP 位址與 Load Balancer
    - 更新了 New-AzureRMLoadBalancer：已新增選用參數 -Sku
    - 更新了 New-AzureRMPublicIpAddress：已新增選用參數 -Sku
  * 已將 DisableOutboundSNAT 的支援新增至 Load Balancer 規則
    - 更新了 New-AzureRMLoadBalancerRuleConfig：已新增選用參數 DisableOutboundSNAT
    - 更新了 Add-AzureRMLoadBalancerRuleConfig：已新增選用參數 DisableOutboundSNAT
    - 更新了 Set-AzureRMLoadBalancerRuleConfig：已新增選用參數 DisableOutboundSNAT
  * 已新增 IkeV2 P2S 的支援
    - 更新了 New-AzureRmVirtualNetworkGateway：已將選用參數 -VpnClientProtocol 預設新增至 [ "SSTP", "IkeV2" ]
    - 更新了 Set-AzureRmVirtualNetworkGateway：已新增選用參數 -VpnClientProtocol
  * 已在網路安全性規則和有效網路安全性規則中新增多重值規則的支援
    - 更新了 Add-AzureRmNetworkSecurityRuleConfig：已更新 SourcePortRange、DestinationPortRange、SourceAddressPrefix 參數以接受字串清單
    - 更新了 New-AzureRmNetworkSecurityRuleConfig：已更新 SourcePortRange、DestinationPortRange、SourceAddressPrefix 參數以接受字串清單
    - 更新了 Set-AzureRmNetworkSecurityRuleConfig：已更新 SourcePortRange、DestinationPortRange、SourceAddressPrefix 參數以接受字串清單
    - 更新了 Add-AzureRmNetworkSecurityRuleConfig：已更新 SourcePortRange、DestinationPortRange、SourceAddressPrefix 參數以接受字串清單
    - 更新了 New-AzureRmNetworkSecurityGroup：已更新 SecurityRules 參數以接受 SourcePortRange、DestinationPortRange、SourceAddressPrefix 參數，這些是 PSSecurityRule 物件中的字串清單
    - 更新了 Get-AzureRmEffectiveNetworkSecurityGroup：已新增 TagMap 參數
    - 更新了 Get-AzureRmEffectiveNetworkSecurityGroup：已使用 SourcePortRange、DestinationPortRange、SourceAddressPrefix 參數更新傳回的 PSEffectiveSecurityRule 物件，這些是字串清單。
  * 已新增虛擬網路 DDoS 保護的支援
    - 更新了 New-AzureRmVirtualNetwork：已新增切換參數 EnableDDoSProtection 和 EnableVmProtection
    - 已新增 PSVirtualNetwork 物件中的 EnableDDoSProtection 和 EnableVmProtection 屬性
  * 已新增高可用內部 Load Balancer 的支援
    - 更新了 Add-AzureRmLoadBalancerRuleConfig：已將 All 新增為通訊協定參數可接受的值
    - 更新了 New-AzureRmLoadBalancerRuleConfig：已將 All 新增為通訊協定參數可接受的值
    - 更新了 Set-AzureRmLoadBalancerRuleConfig：已將 All 新增為通訊協定參數可接受的值
  * 已新增應用程式安全性群組的支援
    - 已新增 New-AzureRmApplicationSecurityGroup
    - 已新增 Get-AzureRmApplicationSecurityGroup
    - 已新增 Remove-AzureRmApplicationSecurityGroup
    - 更新了 New-AzureRmNetworkInterface：已新增 ApplicationSecurityGroup 和 ApplicationSecurityGroupId 選擇性參數
    - 更新了 New-AzureRmNetworkInterfaceIpConfig：已新增 ApplicationSecurityGroup 和 ApplicationSecurityGroupId 選擇性參數
    - 更新了 Add-AzureRmNetworkInterfaceIpConfig：已新增 ApplicationSecurityGroup 和 ApplicationSecurityGroupId 選擇性參數
    - 更新了 Set-AzureRmNetworkInterfaceIpConfig：已新增 ApplicationSecurityGroup 和 ApplicationSecurityGroupId 選擇性參數
    - 更新了 New-AzureRmNetworkSecurityRuleConfig：已新增 SourceApplicationSecurityGroup、SourceApplicationSecurityGroupId、DestinationApplicationSecurityGroup 和 DestinationApplicationSecurityGroupId 選擇性參數
    - 更新了 Add-AzureRmNetworkSecurityRuleConfig：已新增 SourceApplicationSecurityGroup、SourceApplicationSecurityGroupId、DestinationApplicationSecurityGroup 和 DestinationApplicationSecurityGroupId 選擇性參數
    - 更新了 Set-AzureRmNetworkSecurityRuleConfig：已新增 SourceApplicationSecurityGroup、SourceApplicationSecurityGroupId、DestinationApplicationSecurityGroup 和 DestinationApplicationSecurityGroupId 選擇性參數
  * 已新增 VpnDeviceConfiguration 指令碼的新命令
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* 設定檔
  * AzureRm cmdlet 的 Start-Job 支援。
    * 所有 AzureRmCmdlet 都會新增 -AzureRmContext 參數，可接受內容 (Context cmdlet 的輸出)。
      - 內容持續性「已停用」之作業的常見模式：`Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - 內容持續性「已啟用」之作業的常見模式：`Start-Job {New-AzureRmVM [... other parameters]}`
  * 在工作階段之間保存登入資訊，新的 Cmdlet：
    - Enable-AzureRmContextAutosave - 啟用工作階段之間的認證持續性。
    - Disable-AzureRmContextAutosave - 停用工作階段之間的認證持續性。
  * 管理內容資訊，新的 cmdlet
    - Select-AzureRmContext - 選取作用中的命名內容。
    - Rename-AzureRmContext - 將現有內容重新命名以方便參考。
    - Remove-AzureRmContext - 將現有的內容移除。
    - Remove-AzureRmAccount - 將與帳戶相關聯的所有認證、訂用帳戶和租用戶移除。
  * 管理內容資訊，Cmdlet 變更：
    - 已將 Scope = (Process | CurrentUser) 新增至變更認證的所有 Cmdlet
    - Get-AzureRmContext - 已新增 ListAvailable 參數以列出所有儲存的內容
* 資源
  * 新增 PolicySetDefinition Cmdlet
    - 可建立原則集合定義的 New-AzureRmPolicySetDefinition Cmdlet
    - 可列出所有原則集合定義或可取得特定原則集合定義的 Get-AzureRmPolicySetDefinition Cmdlet
    - 可刪除原則集合定義的 Remove-AzureRmPolicySetDefinition Cmdlet
    - 可更新現有原則集合定義的 Set-AzureRmPolicySetDefinition Cmdlet
  * 將 -PolicySetDefinition、-Sku 和 -NotScope 參數新增至 New-AzureRmPolicyAssignment 和 Set-AzureRmPolicyAssignment Cmdlet
  * 將要傳入原則 URL 的支援新增至 New-AzureRmPolicyDefinition and Set-AzureRmPolicyDefinition Cmdlet
  * 將 -Mode 參數新增至 New-AzureRmPolicyDefinition Cmdlet
  * 使用 PSRoleAssignment 物件來新增移除 Roleassignment 的支援
    - 使用者現在可以使用 PSRoleassignmnet inputobject 搭配 Remove-AzureRMRoleAssignment commandlet 來移除 roleassignment。
  * 新增 ManagedApplication Cmdlet
    - 可建立受控應用程式的 New-AzureRmManagedApplication Cmdlet
    - 可列出訂用帳戶下所有受控應用程式或可取得特定受控應用程式的 Get-AzureRmManagedApplication Cmdlet
    - 可刪除受控應用程式的 Remove-AzureRmManagedApplication Cmdlet
    - 可更新現有受控應用程式的 Set-AzureRmManagedApplication Cmdlet
  * 新增 ManagedApplicationDefinition Cmdlet
    - 可使用 ZIP 檔案 URI 或使用 mainTemplate 與 createUiDefinition json 檔案建立受控應用程式定義的 New-AzureRmManagedApplicationDefinition Cmdlet
    - 可列出資源群組下所有受控應用程式定義或可取得特定受控應用程式的 Get-AzureRmManagedApplicationDefinition Cmdlet
    - 可刪除受控應用程式定義的 Remove-AzureRmManagedApplicationDefinition Cmdlet
    - 可更新現有受控應用程式定義的 Set-AzureRmManagedApplicationDefinition Cmdlet
* Sql
  * 新增虛擬網路規則的支援
    - 新增 Get-AzureRmSqlServerVirtualNetworkRule Cmdlet，可依 Azure SQL Server 中特定的規則名稱或虛擬網路規則的清單取得虛擬網路規則。
    - 新增 Set-AzureRmSqlServerVirtualNetworkRule Cmdlet，可變更規則指向的虛擬網路。
    - 新增 Remove-AzureRmSqlServerVirtualNetworkRule Cmdlet，可移除 Azure SQL Server 的虛擬網路規則。
    - 新增 New-AzureRmSqlServerVirtualNetworkRule Cmdlet，可建立新的 Azure SQL Server 虛擬網路規則。
* 網站
  * 新增 App Service 方案的 PremiumV2 層
* Azure.Storage
  * 升級至 Azure 儲存體用戶端程式庫 8.4.0 及 Azure 儲存體資料移動程式庫 0.6.1
  * 在上傳和複製 Blob API 中新增 PremiumPageBlobTier 支援
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * 縮小 AzureStorageContainer、AzureStorageBlob、AzureStorageQueue、AzureStorageTable 之主控台輸出格式的搜尋範圍
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 - 版本 4.3.1
  * 更新以修正組件簽署問題

## <a name="20170807---version-430"></a>2017.08.07 - 版本 4.3.0
* AnalysisServices
  * 修正了 Set-AzureRmAnalysisServciesServer 中的錯誤 (bug)
    - 若未提供管理員，會移除管理員。
  * 在 New-AzureRmAnalysisServicesServer 與 Set-AzureRmAnalysisServicesServer 中新增了 BackupBlobContainerUri
    - 啟用此功能可設定/停用用於備份/還原 Azure Analysis Services 伺服器的備份 BLOb 容器
  * 更新了 New-AzureRmAnalysisServicesServer 與 Set-AzureRmAnalysisServicesServer 中的 Sku 查閱功能
    - 將硬式編碼的 Sku 變更為動態查閱。
  * 新增 Add-AzureAnalysisServicesAccount 以支援透過服務主體登入
* 自動化
  * 變更了 AutomationDSC* Cmdlet，現可從 100 多筆記錄中提取資料
  * 解決了 Verbose 串流在呼叫某些自動化 Cmdlet (例如 Get-AzureRmAutomationVariable、Get-AzureRmAutomationJob) 後，停止運作的問題。
  * 支援在 StartAzureAutomationDscCompilationJob 與 ImportAzureAutomationDscNodeConfiguration 中新增的 NodeConfiguration 組建版本設定
  * 修正現有問題的錯誤 (bug) - 修正別名問題 #3775，以及修正 runOn 別名和 HybridWorkers 的支援。
* 計算
  * Set-AzureRmVMAEMExtension：針對新的進階磁碟大小新增支援
  * Set-AzureRmVMAEMExtension：新增 M 系列的支援
  * 將 ForceUpdateTag 參數新增至 Add-AzureRmVmssExtension
  * 將 Primary 參數新增至 New-AzureRmVmssIpConfig
  * 將 EnableAcceleratedNetworking 參數新增至 Add-AzureRmVmssNetworkInterfaceConfig
  * 將 InstanceId 新增至 Set-AzureRmVmss
  * 對 Get-AzureRmVM -Status 輸出公開 MaintenanceRedeployStatus
  * 對 Get-AzureRmComputeResourceSku 的表格格式公開限制與功能
* DataLakeStore
  * 修正此問題： https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * 為 NamespaceAttributes 新增了 ResourceGroup 屬性
    - 「ResourceGroup」獲得命名空間所在資源群組的名稱
  * 更新了可以在執行用於操作 AuthorizationRule 的命名空間與 EventHub 的參數集時使用的 Cmdlet
    - New-AzureRmEventHubAuthorizationRule - 將新的 AuthorizationRule 新增至現有的命名空間或 EventHub 。
    - Get-AzureRmEventHubAuthorizationRule - 取得現有命名空間或 EventHub 的 AuthorizationRule/AuthorizationRule 清單。
    - Set-AzureRmEventHubAuthorizationRule - 更新 EventHub 或命名空間現有 AuthorizationRule 的屬性。
    - Remove-AzureRmEventHubAuthorizationRule - 刪除現有命名空間或 EventHub 的現有 AuthorizationRule。
    - New-AzureRmEventHubKey - 為現有命名空間或 EventHub 的 AuthorizationRule 產生新的主要/次要索引鍵。
    - Get-AzureRmEventHubKey - 為現有命名空間或 EventHub 的 AuthorizationRule 取得主要/次要索引鍵。
* 網路
    * 新增了 IPv6 支援與新的選擇性參數 -PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig：
      * Set-AzureRmExpressRouteCircuitPeeringConfig：已新增 IPv6 支援。 新增了新的選擇性參數
      * Remove-AzureRmExpressRouteCircuitPeeringConfig：已新增 IPv6 支援。 新增了新的選擇性參數
    * 將參數 -ProbeEnabled 標示為已淘汰
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* 設定檔
    * 資料收集功能依預設啟用。 Microsoft 會收集使用資料來改善使用者體驗。 資料為匿名，且不包含命令列引數值。
      - 使用 Disable-AzureRmDataCollection Cmdlet 可將該功能關閉
      - 使用 Enable-AzureRmDataCollection Cmdlet 可將該功能開啟
* 資源
    * 新增在將要求傳送到 ARM 之前，對下列 roledefinition 與 roleassignment Commandlet 提供的驗證範圍支援
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * 為命名空間、佇列與主題新增了以下新的 Commandlet。 授權規則作業是根據參數集而執行。
    - New-AzureRmServiceBusAuthorizationRule - 將新的 AuthorizationRule 新增至現有的 ServiceBus 命名空間/佇列/主題。
    - Get-AzureRmServiceBusAuthorizationRule - 取得現有 ServiceBus 命名空間/佇列/主題的 AuthorizationRule/AuthorizationRule 清單。
    - Set-AzureRmServiceBusAuthorizationRule - 更新 Servicebus 命名空間/佇列/主題現有 AuthorizationRule 的屬性。
    - New-AzureRmServiceBusKey - 為現有 ServiceBus 命名空間/佇列/主題的 AuthorizationRule 產生新的主要/次要索引鍵。
    - Get-AzureRmServiceBusKey - 取得現有 ServiceBus 命名空間/佇列/主題的 AuthorizationRule 的主要/次要索引鍵。
    - Remove-AzureRmServiceBusNamespaceAuthorizationRule - 刪除 ServiceBus 命名空間/佇列/主題的現有 AuthorizationRule。
  * 新增了資源群組屬性至 NamespceAttributes

* Sql
    * 更新 Set-AzureRmSqlServerTransparentDataEncryptionProtector，以在加密保護裝置類型設為 AzureKeyVault 時，顯示警告並要求確認
    * 為稽核設定新增更新的 Cmdlet
      - Get-AzureRmSqlDatabaseAuditing Cmdlet，此 Cmdlet 可取得 Azure SQL 資料庫的稽核設定。
      - Get-AzureRmSqlServerAuditing Cmdlet，此 Cmdlet 可取得 Azure SQL 伺服器的稽核設定。
      - Set-AzureRmSqlDatabaseAuditing Cmdlet，此 Cmdlet 可變更 Azure SQL 資料庫的稽核設定。
      - Set-AzureRmSqlServerAuditing Cmdlet，此 Cmdlet 可變更 Azure SQL 伺服器的稽核設定。
    * 淘汰現有的稽核原則 Cmdlet
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Update-AzureRmSqlSyncGroup 的結構描述檔案剖析現在不區分大小寫。
* 儲存體
    * 為資源模式儲存體帳戶 Cmdlet 新增 NeworkRule 支援
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17 - 版本 4.2.1
* 計算
  - 修正 VM 磁碟和 VM 磁碟快照集建立和更新 Cmdlet 的問題，(連結) [<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* 設定檔
  - 修正 RDFE 中非互動使用者驗證問題 (連結) [<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - 修正非互動使用者驗證問題 (連結) [<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.7.11 - 版本 4.2.0
* AnalysisServices
    * 新增資料平面 API
        - 引進用以擷取 AS 伺服器記錄檔 Export-AzureAnalysisServicesInstanceLog 的 API
* 自動化
    * 針對 New-AzureRmAutomationSchedule，正確設定每週和每月排程的 TimeZone 值
        - 在此問題中可找到詳細資訊： https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - 新增 Get-AzureBatchJobPreparationAndReleaseTaskStatus cmdlet。
    - 將位元組範圍的開始與結束加入 Get-AzureBatchNodeFileContent 參數。
* CognitiveServices
    * 整合認知服務管理 SDK 1.0.0 版。
    * 修正帳戶名稱長度檢查錯誤。
* 計算
    * 儲存體帳戶類型支援映像磁碟：
        - 「StorageAccountType」參數已加入 Set-AzureRmImageOsDisk 和 Add-AzureRmImageDataDisk
    * 採用 Vmss IP 組態的 PrivateIP 和 PublicIP 功能：
        - 「PrivateIPAddressVersion」、「PublicIPAddressConfigurationName」、「PublicIPAddressConfigurationIdleTimeoutInMinutes」、「DnsSetting」名稱已加入 New-AzureRmVmssIpConfig
        - 指定 IPv4 或 IPv6 的「PrivateIPAddressVersion」參數已加入 New-AzureRmVmssIpConfig
    * 效能維護功能：
        - 「PerformMaintenance」切換參數已加入 Restart-AzureRmVM。
        - Get-AzureRmVM -Status 會顯示特定 VM 的效能維護資訊
    * 虛擬機器身分識別功能：
        - 「IdentityType」參數已加入 New-AzureRmVMConfig 和 UpdateAzureRmVM
        - Get-AzureRmVM 顯示特定 VM 的身分識別資訊
    * Vmss 身分識別功能：
        - 「IdentityType」參數已加入 New-AzureRmVmssConfig
        - Get-AzureRmVmss 顯示特定 Vmss 的身分識別資訊
    * Vmss 開機診斷功能：
        - 設定 Vmss 物件開機診斷的新 Cmdlet：Set-AzureRmVmssBootDiagnostics
        - 「BootDiagnostic」參數已加入 New-AzureRmVmssConfig
    * Vmss LicenseType 功能：
        - 「LicenseType」參數已加入 New-AzureRmVmssConfig
    * RecoveryPolicyMode 支援：
        - 「RecoveryPolicyMode」參數已加入 New-AzureRmVmssConfig
    * 計算資源 Sku 功能：
        - 新 Cmdlet「Get-AzureRmComputeResourceSku」列出所有計算資源 sku
* DataFactories
    * 取代 New-AzureRmDataFactoryGatewayKey
    * 加入 New-AzureRmDataFactoryGatewayAuthKey 和 Get-AzureRmDataFactoryGatewayAuthKey，推出閘道驗證金鑰功能
* DataLakeAnalytics
    * 透過下列命令，加入計算原則 CRUD 支援：
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * 新增支援作業關係中繼資料，協助處理週期性作業和作業流程。 已更新或新增下列命令：
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * 針對作業和目錄 API 更新 Token 對象，以使用正確的 Data Lake 特定對象，而非 Azure 資源對象。
* DataLakeStore
    * 新增支援在 Set-AzureRMDataLakeStoreAccount Cmdlet 由使用者管理 KeyVault 金鑰輪替
    * 新增生活品質更新，在新增使用者管理的 KeyVault 或金鑰輪替時，自動觸發 `enableKeyVault` 呼叫。
    * 針對作業和目錄 API 更新 Token 對象，以使用正確的 Data Lake 特定對象，而非 Azure 資源對象。
    * 已修正錯誤，該錯誤會使用下列 Cmdlet 限制建立/附加檔案的大小：
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* Dns
    * 針對 Get-AzureRmDnsZone 修正管線情節中的錯誤
        - 如需詳細資訊，請參閱： https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * 新增支援以啟用/停用 Operations Management Suite (OMS)
    * 新的 Cmdlet
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * 加入新的參數，將 Spark 自訂設定設為 Add-AzureRmHDInsightConfigValues
        - Spark 1.6 適用的參數 SparkDefaults 和 SparkThriftConf
        - Spark 2.0 適用的參數 Spark2Defaults 和 Spark2ThriftConf
* 深入解析
    * 問題 #4215 (變更要求) 移除 Get-AzureRmLog Cmdlet 的 15 天期間限制。 此外亦小幅變更了單元測試名稱。
    * 已針對 Get-AzureRmLog 修正問題 #3957
        - 問題 1：後端傳回的記錄，每頁 200 筆，透過接續 Token 連結下一頁。 客戶會看到 Cmdlet 只傳回 200 筆記錄，但確知應還有更多記錄。 除非 MaxEvents 小於 200，否則不論客戶設定的值為何，都會發生這種情形。
        - 問題 2：文件包含不正確的 Cmdlet 相關資料，例如：預設期間是 1 小時。
        - 修正問題 1：Cmdlet 現在會遵循後端傳回的接續 Token，直到達到 MaxEvents 或集合的結束為止。<br>MaxEvents 的預設值為 1000，最大值為 100000。 凡 MaxEvents 值小於 1 都會忽略，並改為使用預設值。 這些值和行為並未變更，現在都已正確地記錄。<br>由於 Cmdlet 名稱未說明相關事件，而只提供了記錄，因此已新增 MaxEvents 別名 -MaxRecords-。
        - 修正問題 2：文件包含正確及更詳細的資訊：新的別名、正確的期間、正確的預設值、最小值和最大值。
* KeyVault
    * 將 -UserPrincipalName 指定到 Set-AzureRMKeyVaultAccessPolicy 和 Remove-AzureRMKeyVaultAccessPolicy Cmdlet 時，請從目錄查詢中移除電子郵件地址。
      - 兩個 Cmdlet 現在會有適當的 -EmailAddress 參數，在需要查詢電子郵件地址時可供使用，而不使用 -UserPrincipalName 參數。  如果目錄中有多個相符的電子郵件地址，則此 Cmdlet 的電子郵件地址將會失效。
* 網路
    * New-AzureRmIpsecPolicy：SALifeTimeSeconds 和 SADataSizeKilobytes 不再是必要參數
        - SALifeTimeSeconds 預設值為 27000 秒
        - SADataSizeKilobytes 預設值為 102400000 KB
    * 使用 ssl 原則，並在應用程式閘道列出所有 ssl 選項 api，以新增支援自訂加密套件設定
        - 新增選擇性參數 -PolicyType、-PolicyName、-MinProtocolVersion、-Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - 已新增 Get-AzureRmApplicationGatewayAvailableSslOptions (別名：List-AzureRmApplicationGatewayAvailableSslOptions)
        - 已新增 Get-AzureRmApplicationGatewaySslPredefinedPolicy (別名：List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * 應用程式閘道中新增重新導向支援
        - 新增 Add-AzureRmApplicationGatewayRedirectConfiguration
        - 新增 Get-AzureRmApplicationGatewayRedirectConfiguration
        - 新增 New-AzureRmApplicationGatewayRedirectConfiguration
        - 新增 Remove-AzureRmApplicationGatewayRedirectConfiguration
        - 新增 Set-AzureRmApplicationGatewayRedirectConfiguration
        - 新增選擇性參數 -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - 新增選擇性參數-DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - 新增選擇性參數 -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - 新增選擇性參數 -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * 在應用程式閘道中新增支援 azure 網站
        - 新增 New-AzureRmApplicationGatewayProbeHealthResponseMatch
        - 新增選擇性參數 -PickHostNameFromBackendHttpSettings、-MinServers、-Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - 新增選擇性參數 -PickHostNameFromBackendAddress、-AffinityCookieName、-ProbeEnabled、-Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * 更新 Get-AzureRmPublicIPaddress，以擷取透過 VM 擴展集建立的 publicipaddress 資源
    * 新增 Cmdlet 取得虛擬網路的目前使用情形
        - Get-AzureRmVirtualNetworkUsageList
* 設定檔
    * 修正使用 Import-AzureRmContext 或 Save-AzureRmContext 時的錯誤
        - 在此問題中可找到詳細資訊： https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * 推出新的 Azure Site Recovery 作業模組。
        - 所有 Cmdlet 的開頭均為 AzureRmRecoveryServicesAsr*
* Sql
    * 將資料同步 PowerShell Cmdlet 加入 AzureRM.Sql
    * 更新 AzureRmSqlServer Cmdlet 以使用新的 REST API 版本，避免建立伺服器時發生逾時。
    * 已取代的伺服器升級 Cmdlet，因為舊的伺服器版本 (2.0) 已經不存在。
    * 將新的選擇性切換參數「AssignIdentity」加入 New-AzureRmSqlServer 和 Set-AzureRmSqlServer Cmdlet，以支援佈建 SQL 伺服器資源的資源身分識別
    * 參數 ResourceGroupName 現在是 Get-AzureRmSqlServer 的選擇性項目
        - 在下列問題中可找到詳細資訊： https://github.com/Azure/azure-powershell/issues/635
* ExpressRoute 的 ServiceManagement：
    * 更新 New-AzureBgpPeering Cmdlet，新增下列選項：
        - PeerAddressType：可指定「IPv4」或「IPv6」的值，以建立對應位址系列類型的 BGP 對等互連
    * 更新 Set-AzureBgpPeering Cmdlet，新增下列選項：
        - PeerAddressType：可指定「IPv4」或「IPv6」的值，以更新對應位址系列類型的 BGP 對等互連
    * 更新 Remove-AzureBgpPeering Cmdlet，新增下列選項：
        - PeerAddressType：可指定「IPv4」、「IPv6」或所有的值，以移除對應位址系列類型或所有的 BGP 對等互連

## <a name="20170607---version-410"></a>2017.06.07 - 版本 4.1.0
* AnalysisServices
    * 新增的 SKU：B1、B2、S0
    * 新增相應增加/減少支援
* CognitiveServices
    * 更新在建立認知服務資源時的授權合約詳細顯示內容
* 計算
    * 針對具有多個受控磁碟的虛擬機器，修正 Test-AzureRmVMAEMExtension
    * 已更新 Set-AzureRmVMAEMExtension：新增進階受控磁碟的快取資訊
    * Add-AzureRmVhd：VHD 大小限制已增加至 4TB。
    * Stop-AzureRmVM：釐清 STayProvisioned 參數的文件
    * New-AzureRmDiskUpdateConfig
      * 已取代的參數 CreateOption、StorageAccountId、ImageReference、SourceUri、SourceResourceId
    * Set-AzureRmDiskUpdateImageReference：已取代的 Cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * 已取代的參數 CreateOption、StorageAccountId、ImageReference、SourceUri、SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference：已取代的 Cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * 啟用 DataLake 存放區的 KeyVault 受控加密
* DevTestLabs
    * 更新 Cmdlet 以處理目前和更新的 DevTest Labs API 版本。
* IotHub
    * 新增 IoTHub Cmdlet 的路由支援
* KeyVault
  * 新的 Cmdlet，可支援 KeyVault 受控儲存體帳戶金鑰
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* 網路
    * Get-AzureRmNetworkUsage：新的 Cmdlet，可顯示網路使用量和容量詳細資料
    * 新增 VirtualNetworkGateways 的 GatewaySku 選項
        * VpnGw1、VpnGw2、VpnGw3 是針對 Vpn 閘道新增的 Sku
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * 固定說明範例
* NotificationHubs
    * 針對新 API 的 NotificationHubs Cmdlet 進行透明更新
* 設定檔
    * Resolve-AzureRmError
      * 新的 Cmdlet，可顯示詳細錯誤和 Cmdlet 產生的例外狀況，包括伺服器要求/回應資料
    * Send-Feedback
      * 啟用傳送意見反應而無須登入
    * Get-AzureRmSubscription
      * 修正擷取 CSP 訂用帳戶時的錯誤
* 資源
    * 已修正問題，其中若 roleassignments 的數字大於 1000，Get-AzureRMRoleAssignment 會導致錯誤的要求
        * 現在即使要傳回的 roleassignments 大於 1000，使用者仍可使用 Get-AzureRMRoleAssignment
* Sql
    * Restore-AzureRmSqlDatabase：更新文件範例
* 儲存體
    * 在資源模式的儲存體帳戶 Cmdlet，新增 AssignIdentity 設定支援
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * 在資源模式的儲存體帳戶 Cmdlet，新增客戶金鑰支援
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * 新監視器設定「MonitorIntervalInSeconds」、「MonitorTimeoutInSeconds」、「MonitorToleratedNumberOfFailures」
    * 新監視器通訊協定「TCP」
* ServiceManagement
    * Add-AzureVhd：VHD 大小限制已增加至 4TB。
    * New-AzureBGPPeering：支援 LegacyMode
* Azure.Storage
    * 針對可接受萬用字元的參數更新說明，並更新 StorageContext 類型

## <a name="20170523---version-402"></a>2017.05.23 - 版本 4.0.2
* 設定檔
    * Add-AzureRmAccount
      * 新增 `-EnvironmentName` 參數別名，以便回溯相容於 AzureRM.profile 的 2.x 版本

## <a name="20170512---version-401"></a>2017.05.12 - 版本 4.0.1
 * 修正離線案例中 New-AzureStorageContext 的問題： https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 - 版本 4.0.0


* 此版本包含重大變更。 如需變更詳細資料和對現有指令碼的影響，請參閱[移轉指南 (英文)](https://aka.ms/azps-migration-guide)。
* ApiManagement
  - 新增在 New-AzureRmApiManagementGroup 中設定外部群組的支援。
* 計費
  - 新的 Get-AzureRmBillingPeriod Cmdlet
    + 用來擷取 Azure 訂用帳戶計費週期的 Cmdlet。
  - 更新 Get-AzureRmBillingInvoice Cmdlet
  - 新的 BillingPeriodNames 屬性
  - 在清單檢視中輸出
* 計算
  - 已更新 Set-AzureRmVMAEMExtension 和 Test-AzureRmVMAEMExtension Cmdlet，以支援進階受控磁碟
  - 適用於 IaaS VM 和失敗時還原的備份加密設定
  - ChefServiceInterval 選項現已重新命名為 ChefDaemonInterval。 但舊選項將繼續運作。
  - 移除 PS VM 物件中重複的 DataDiskNames 和 NetworkInterfaceIDs 屬性。
  - 使個別位於 Remove-AzureRmVMDataDisk 和 Remove-AzureRmVMNetworkInterface 中的 DataDiskNames 和 NetworkInterfaceIDs 參數成為選擇性。
  - 修正 Get Cmdlet 傳回清單物件時的管線問題。
  - 已重新命名和 RDFE Cmdlet 衝突的 Cmdlet。 如需詳細資料，請參閱問題 https://github.com/Azure/azure-powershell/issues/2917
    + `New-AzureVMSqlServerAutoBackupConfig` 已重新命名為 `New-AzureRmVMSqlServerAutoBackupConfig`
    + `New-AzureVMSqlServerAutoPatchingConfig` 已重新命名為 `New-AzureRmVMSqlServerAutoPatchingConfig`
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` 已重新命名為 `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* 耗用量
  - 新的 Get-AzureRmConsumptionUsageDetail Cmdlet
    + 用於擷取訂用帳戶使用量詳細資料的 Cmdlet。
* ContainerRegistry
  - 新增 Azure Container Registry 的 PowerShell Cmdlet
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - 新增取得和列出目錄套件的支援
  - 新增從更深層的上階列出下列目錄項目的支援：
    + 資料表
    + TVF
    + 檢視
    + 統計資料
* DataLakeStore
  - 對於 `Import-AzureRMDataLakeStoreItem` 和 `Export-AzureRMDataLakeStoreItem`，預設已停用追蹤記錄以改善效能。 如果需要追蹤記錄，請使用 `-DiagnosticLogLevel` 和 `-DiagnosticLogPath` 參數
  - 已修正將大量的小型檔案上傳到 ADLS 時偶爾會導致 PowerShell 當機的問題。
* EventHub
  - 錯誤修正：
    + 修正 Set-AzureRmEventHubNamespace Cmdlet 錯誤 - 'Tier' 不能為 Null，而必須是 'SkuName'
    + Set-AzureRmEventHub - 修正更新 EventHub 時的「物件參考未設定成物件的執行個體」錯誤
* 深入解析
  - Add-AzureRm*AlertRule
    + 傳回單一物件︰newResource、statusCode、requestId
  - Get-AzureRmAlertRule
    + 現在會對輸出進行列舉，而不是將它視為單一物件。 它的類型並未變更，仍然是清單。
  - Remove-AzureRmAlertRule
    + statusCode 會遵循要求所傳回的狀態碼，先前一律是「良好」。
  - Add-AzureRmAutoscaleSetting
    + 現在會傳回包含 statusCode、requestId，以及最近所建立/更新資源的單一物件 (而非先前的清單)。
    + 狀態碼會遵循要求所傳回的狀態，先前一律是「良好」。
  - New-AzureRmAutoscaleRule
    + 已擴充 ScaleActionType 參數，現在它會接收下列值：ChangeCount、PercentChangeCount 和 ExactCount。
  - Remove-AzureRmAutoscaleSetting
    + 輸出中的 statusCode 會遵循要求所傳回的 statusCode。 先前一律是「良好」。
  - Get-AzureRMLogProfile
    + 現在會對輸出進行列舉。 先前是將它視為單一物件。 輸出的類型仍為先前的清單。
  - Remove-AzureRmLogProfile
    + 已實作 PassThru 參數。
  - 計量 API
    + SDK 現在會從 MDM 擷取計量。
  - Get-AzureRmMetricDefinition
    + 輸出仍是清單，但清單的結構已變更。
  - Get-AzureRmMetric
    + 呼叫已變更。 新的語法為：Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + 輸出是清單，但其元素的結構已變更。
* KeyVault
  - 新增備份/還原 KeyVault 密碼的支援
    + 可以對密碼進行備份和還原，以符合目前對於金鑰所支援的功能

  - 金鑰和密碼的備份 Cmdlet 現在接受以對應的物件做為輸入參數
    + 呼叫端可鏈結擷取和備份作業：Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - 備份 Cmdlet 現在支援用於覆寫現有檔案的 -Force 參數
    + 請注意，嘗試覆寫現有檔案將不再會擲回，而是改為提示使用者選擇繼續的方式。
* LogicApp
  - 交換控制編號災害復原 Cmdlet 的新參數︰
    + 用於指定相關控制編號的選擇性 -AgreementType 參數 ("X12" 或 "Edifact")
* MachineLearning
  - 使用新版的 Azure Machine Learning .Net SDK，並新增 Cmdlet
    + Add-AzureRmMlWebServiceRegionalProperty
  - 說明文字中的次要措辭修正。
* 網路
  - 已新增 Test-AzureRmNetworkWatcherConnectivity Cmdlet
    + 傳回指定來源 VM 和目的地的連線資訊
    + 如果無法建立來源與目的地之間的連線，此 Cmdlet 會傳回問題的詳細資料
* 設定檔
  - 已新增 'Send-Feedback' Cmdlet︰可讓使用者起始一組提示，以傳送意見反應給 Azure PowerShell 小組。
  - 已移除下列別名，因為它們與 Azure 模組中現有的 Cmdlet 名稱衝突︰
    + `Enable-AzureDataCollection` (受 `Enable-AzureRmDataCollection` 支援)
    + `Disable-AzureDataCollection` (受 `Disable-AzureRmDataCollection` 支援)
* 轉送
  - 新增 Azure 轉送適用的 Cmdlet，方便使用者建立和管理所有 Azure 轉送資源。
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* 資源
  - 支援適用於 AzureRmResourceGroupDeployment 的跨資源群組部署
    + 使用者現在可以使用巢狀部署以部署至不同的資源群組。
* ServiceBus

  - 錯誤 (bug) 修正：ServiceBus 佇列物件屬性值已設為 Null，該物件是做為 Set-AzureRmServiceBusQueue Cmdlet 中的輸入參數使用以更新佇列。
    - 受影響的屬性包括 LockDuration、EntityAvailabilityStatus、DuplicateDetectionHistoryTimeWindow、MaxDeliveryCount 和 MessageCount
* ServiceFabric

  - 已新增適用於 Service Fabric 的 Cmdlet
    + Add-AzureRmServiceFabricApplicationCertificate       新增將做為應用程式憑證使用的憑證
    + Add-AzureRmServiceFabricClientCertificate       在叢集設定新增用於用戶端驗證的一般名稱或指紋
    + Add-AzureRmServiceFabricClusterCertificate       在叢集新增次要叢集憑證以更換現有的憑證
    + Add-AzureRmServiceFabricNodes       在叢集新增特定節點類型的節點/VM
    + Add-AzureRmServiceFabricNodeType       在現有叢集新增節點類型/VM
    + Get-AzureRmServiceFabricCluster       取得叢集資源的詳細資料
    + New-AzureRmServiceFabricCluster 建立新的 ServiceFabric 叢集。 此命令有許多的多載，可涵蓋各種案例
    + Remove-AzureRmServiceFabricClientCertificate       移除某個用戶端憑證以防止將它用於存取叢集
    + Remove-AzureRmServiceFabricClusterCertificate       移除某個用戶端憑證以防止將它用於叢集安全性
    + Remove-AzureRmServiceFabricNodes       自叢集中移除特定節點類型的節點
    + Remove-AzureRmServiceFabricNodeType       自叢集中移除某個節點類型
    + Remove-AzureRmServiceFabricSettings       自叢集中移除一或多個 ServiceFabric 設定
    + Set-AzureRmServiceFabricSettings       新增或更新叢集的一或多個 ServiceFabric 設定
    + Set-AzureRmServiceFabricUpgradeType       變更叢集的 ServiceFabric 升級類型
    + Update-AzureRmServiceFabricDurability       變更叢集的持久性層
    + Update-AzureRmServiceFabricReliability       變更叢集的可靠性層
* Sql
  - 已將 -SampleName 參數新增至 New-AzureRmSqlDatabase
  - 更新容錯移轉群組 Cmdlet
  - 移除 'Tag' 參數
  - 從 Remove-AzureRmSqlDatabaseFailoverGroup Cmdlet 中移除 'PartnerResourceGroupName' 和 'PartnerServerName' 參數
  - 將 'GracePeriodWithDataLossHours' 參數新增至 New- 和 Set- Cmdlet，此參數最終會取代 'GracePeriodWithDataLossHour'
  - 文件已增補並更新
  - 變更傳回物件的格式，並修正欄位有時不會填入的錯誤
  - 將 'DatabaseNames' 和 'PartnerLocation' 屬性新增至容錯移轉群組物件
  - 修正造成 Switch- Cmdlet 立即傳回 (而非等待作業完成後再傳回) 的錯誤
  - 修正使用高寬限期值時的整數溢位錯誤
  - 在提供的值比 1 小時的下限還要低的情況下，將寬限期調整為 1 小時
  - 從 Set-AzureRmSqlDatabaseThreatDetectionPolicy Cmdlet 和 Set-AzureRmSqlServerThreatDetectionPolicy Cmdlet 之 "ExcludedDetectionType" 參數的可接受值中移除 "Usage_Anomaly"。
* 儲存體
  - 將 SRP SDK 升級至 6.3.0
  - New/Set-AzureRmStorageAccount：新增參數以支援 EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount：傳回的儲存體帳戶包含新的 EnableHttpsTrafficOnly 屬性
* Azure.Storage
  - 升級至 Azure 儲存體用戶端程式庫 8.1.1 及 Azure 儲存體資料移動程式庫 0.5.1
  - 新增 Cmdlet 以支援 Blob 增量複製功能
