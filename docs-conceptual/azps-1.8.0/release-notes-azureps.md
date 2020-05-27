---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 287e9e1f066d0768e7f572ca7f5f2ee2b78931d9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386964"
---
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
