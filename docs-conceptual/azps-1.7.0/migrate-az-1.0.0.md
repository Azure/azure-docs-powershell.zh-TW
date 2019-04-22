---
title: Microsoft Azure PowerShell Az 1.0.0 的重大變更
description: 本移轉指南包含在 Az 第 1 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59363990"
---
# <a name="migration-guide-for-az-100"></a>Az 1.0.0 的移轉指南

本文件說明 6.x 版 AzureRM 和 Az 1.0.0 版之間的變更。

## <a name="table-of-contents"></a>目錄
- [一般重大變更](#general-breaking-changes)
  - [Cmdlet 名詞前置詞的變更](#cmdlet-noun-prefix-changes)
  - [模組名稱的變更](#module-name-changes)
  - [移除的模組](#removed-modules)
  - [Windows PowerShell 5.1 和 .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [使用 PSCredential 暫時移除使用者登入](#temporary-removal-of-user-login-using-pscredential)
  - [預設使用裝置程式碼登入，而非網頁瀏覽器提示](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [模組的重大變更](#module-breaking-changes)
  - [Az.ApiManagement (先前是 AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (先前是 AzureRM.Billing、AzureRM.Consumption 和 AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (先前是 AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (先前是 AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (先前是 AzureRM.DataFactories 和 AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (先前是 AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (先前是 AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (先前是 AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (先前是 AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (先前是 AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (先前是 AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (先前是 AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (先前是 AzureRM.RecoveryServices、AzureRM.RecoveryServices.Backup 和 AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (先前是 AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (先前是 AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (先前是 AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (先前是 Azure.Storage 和 AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (先前是 AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>一般重大變更
### <a name="cmdlet-noun-prefix-changes"></a>Cmdlet 名詞前置詞的變更
在 AzureRM 中，Cmdlet 使用 'AzureRM' 或 'Azure' 作為名詞前置詞。  Az 則將 Cmndlet 名稱予以簡化和標準化，讓所有 Cmdlet皆使用 'Az' 作為其 Cmdlet 名詞前置詞。 例如︰
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

已變更為
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

為了讓您更輕鬆地轉為使用這些新的 Cmdlet 名稱，Az 會引進兩個新的 Cmdlet，這兩者分別是 ```Enable-AzureRmAlias``` 和 ```Disable-AzureRmAlias```。  ```Enable-AzureRmAlias``` 會將別名從 AzureRM 中較舊的 Cmdlet 名稱，改建立為較新的 Az Cmdlet 名稱。  此 Cmdlet 可讓您在目前的工作階段中建立別名，而您也可以藉由變更使用者或機器的設定檔，在所有工作階段建立別名。 

例如，下列的 AzureRM 指令碼：
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

只要使用 ```Enable-AzureRmAlias``` 稍做變更即可執行：
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

執行 ```Enable-AzureRmAlias -Scope CurrentUser``` 會對所有已開啟的 PowerShell 工作階段啟用別名，因此在執行此 Cmdlet 之後，就完全不需要變更這類指令碼：
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

如需如何使用別名 Cmdlet 的完整詳細資訊，請從 PowerShell 提示字元執行 ```Get-Help -Online Enable-AzureRmAlias```。

```Disable-AzureRmAlias``` 會移除 ```Enable-AzureRmAlias``` 所建立的 AzureRM Cmdlet 別名。  如需完整的詳細資訊，請從 PowerShell 提示字元執行 ```Get-Help -Online Disable-AzureRmAlias```。

### <a name="module-name-changes"></a>模組名稱的變更
- 模組名稱已從 `AzureRM.*` 變更為 `Az.*`，但下列模組除外：
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

模組名稱的變更表示，只要指令碼使用 ```#Requires``` 或 ```Import-Module``` 來載入特定模組，就需要進行變更，以改為使用新的模組。

#### <a name="migrating-requires-statements"></a>遷移 #Requires 陳述式
使用 #Requires 來宣告 AzureRM 模組相依性的指令碼，應更新為使用新的模組名稱
```powershell
#Requires -Module AzureRM.Compute
```

應變更為
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>遷移 Import-Module 陳述式
使用 ```Import-Module``` 來載入 AzureRM 模組的指令碼，必須加以更新以反映新的模組名稱。
```powershell
Import-Module -Name AzureRM.Compute
```

應變更為
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>遷移完整的 Cmdlet 叫用
使用模組完整 Cmdlet 叫用的指令碼，例如
```powershell
AzureRM.Compute\Get-AzureRmVM
```

應變更為使用新的模組和 Cmdlet 名稱
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>遷移模組資訊清單相依性
透過模組資訊清單 (.psd1) 檔案來表達 AzureRM 模組相依性的模組，必須更新其 'RequiredModules' 區段中的模組名稱

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

應變更為

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>移除的模組
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

不再支援這些服務的工具。  建議客戶一有空就立刻遷移至替代服務。

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 和 .NET 4.7.2
- 若要搭配使用 Az 和 Windows PowerShell 5.1，則必須安裝 .NET 4.7.2。 不過，搭配使用 Az 和 PowerShell Core 則不需要 .NET 4.7.2。 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>使用 PSCredential 暫時移除使用者登入
- 由於 .NET Standard 的驗證流程有變，我們暫時移除透過 PSCredential 來登入使用者的功能。 這項功能會在 2019 年 1 月 15 日版本的 Windows PowerShell 5.1 重新引進。 [此問題](https://github.com/Azure/azure-powershell/issues/7430)中會有這方面的詳細討論。

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>預設使用裝置程式碼登入，而非網頁瀏覽器提示
- 由於 .NET Standard 的驗證流程有變，我們會在互動式登入期間使用裝置登入作為預設的登入流程。 在 2019 年 1 月 15 日的版本中，會重新引進透過網頁瀏覽器來登入的功能，來作為 Windows PowerShell 5.1 的預設登入功能。 屆時，使用者將能夠使用切換參數來選擇裝置登入功能。

## <a name="module-breaking-changes"></a>模組的重大變更

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (先前是 AzureRM.ApiManagement)
- 即將移除下列 Cmdlet：
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - 請改為使用 **Set-AzApiManagement** Cmdlet 來設定這些屬性
- 已移除下列屬性
  - 已從 `PsApiManagementContext` 移除 `PsApiManagementHostnameConfiguration` 類型的 `PortalHostnameConfiguration`、`ProxyHostnameConfiguration`、`ManagementHostnameConfiguration` 和 `ScmHostnameConfiguration` 屬性。 請改為使用 `PsApiManagementCustomHostNameConfiguration` 類型的 `PortalCustomHostnameConfiguration`、`ProxyCustomHostnameConfiguration`、`ManagementCustomHostnameConfiguration` 和 `ScmCustomHostnameConfiguration`。
  - 已從 PsApiManagementContext 移除 `StaticIPs` 屬性。 此屬性已分割為 `PublicIPAddresses` 和 `PrivateIPAddresses`。
  - 已從 New-AzureApiManagementVirtualNetwork Cmdlet 移除必要的 `Location` 屬性。

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (先前是 AzureRM.Billing、AzureRM.Consumption 和 AzureRM.UsageAggregates)
- 已從 `Get-AzConsumptionUsageDetail` Cmdlet 移除 `InvoiceName` 參數。  指令碼必須針對發票使用其他身分識別參數。

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (先前是 AzureRM.CognitiveServices)
- 已從 `Get-AzCognitiveServicesAccountSkus` Cmdlet 移除 `GetSkusWithAccountParamSetName` 參數集。  您必須依帳戶類型和位置來取得 SKU，而非使用 ResourceGroupName 和帳戶名稱來取得。

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (先前是 AzureRM.Compute)
- 已從 `PSVirtualMachine` 和 `PSVirtualMachineScaleSet` 物件中的 `Identity` 屬性移除 `IdentityIds`。指令碼不應再使用這個欄位的值來決定處理方式。
- `PSVirtualMachineScaleSetVM` 物件的 `InstanceView` 屬性，其類型已從 `VirtualMachineInstanceView` 變更為 `VirtualMachineScaleSetVMInstanceView`
- 已從 `UpgradePolicy` 屬性移除 `AutoOSUpgradePolicy` 和 `AutomaticOSUpgrade` 屬性
- `PSSnapshotUpdate` 物件中的 `Sku` 屬性，其類型已從 `DiskSku` 變更為 `SnapshotSku`
- 已從 `Add-AzVMDataDisk` Cmdlet 移除 `VmScaleSetVMParameterSet`，您無法再將資料磁碟個別地新增至擴展集 VM。

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (先前是 AzureRM.DataFactories 和 AzureRM.DataFactoryV2)
- `GatewayName` 已成為 `New-AzDataFactoryEncryptValue` Cmdlet 的必要參數
- 已移除 `New-AzDataFactoryGatewayKey` Cmdlet
- 已從 `Get-AzDataFactoryV2ActivityRun` Cmdlet 移除 `LinkedServiceName` 參數。指令碼不應再使用這個欄位的值來決定處理方式。

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (先前是 AzureRM.DataLakeAnalytics)
- 已移除淘汰的 Cmdlet：`New-AzDataLakeAnalyticsCatalogSecret`、`Remove-AzDataLakeAnalyticsCatalogSecret` 和 `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (先前是 AzureRM.DataLakeStore)
- 下列 Cmdlet 已將 `Encoding` 參數的類型從 `FileSystemCmdletProviderEncoding` 變更為 `System.Text.Encoding`。 這項變更會移除編碼值 `String` 和 `Oem`。 其他所有先前的編碼值則會保留。
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- 已從 `New-AzDataLakeStoreAccount` 和 `Set-AzDataLakeStoreAccount` Cmdlet 移除淘汰的 `Tags` 屬性別名

  使用下列 Cmdlet 的指令碼
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  應變更為
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- 已從 ```PSDataLakeStoreAccountBasic``` 物件移除淘汰的 ```Identity```、```EncryptionState```、```EncrypotionProvisioningState```、```EncryptionConfig```、```FirewallState```、```FirewallRules```、```VirtualNetworkRules```、```TrustedIdProviderState```、```TrustedIdProviders```、```DefaultGroup```、```NewTier```、```CurrentTier```、```FirewallAllowAzureIps``` 屬性。  指令碼若使用 ```Get-AzDataLakeStoreAccount``` 所傳回的 ```PSDatalakeStoreAccount```，則不應參考這些屬性。

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (先前是 AzureRM.KeyVault)
- 已從 `PSKeyVaultKeyAttributes`、`PSKeyVaultKeyIdentityItem` 和 `PSKeyVaultSecretAttributes` 物件移除 `PurgeDisabled` 屬性。指令碼不應再參考 ```PurgeDisabled``` 屬性來決定處理方式。

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (先前是 AzureRM.Media)
- 已從 `New-AzMediaService` Cmdlet 移除淘汰的 `Tags` 屬性別名。使用下列 Cmdlet 的指令碼
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  應變更為
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (先前是 AzureRM.Insights)
- 已從 `Set-AzDiagnosticSetting` Cmdlet 移除複數名稱 `Categories` 和 `Timegrains` 參數，以便支援單一參數名稱。使用下列 Cmdlet 的指令碼
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  應變更為
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (先前是 AzureRM.Network)
- 已從 `Get-AzServiceEndpointPolicyDefinition` Cmdlet 移除淘汰的 `ResourceId` 參數
- 已從 `PSVirtualNetwork` 物件移除淘汰的 `EnableVmProtection` 屬性
- 已移除淘汰的 `Set-AzVirtualNetworkGatewayVpnClientConfig` Cmdlet
  
指令碼不應再根據這些欄位的值來決定處理方式。

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (先前是 AzureRM.OperationalInsights)
- 已移除 `Get-AzOperationalInsightsDataSource` 的預設參數集，由 `ByWorkspaceNameByKind` 成為預設參數集

  使用下列 Cmdlet 來列出資料來源的指令碼
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  應變更為指定某個種類
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (先前是 AzureRM.RecoveryServices、AzureRM.RecoveryServices.Backup 和 AzureRM.RecoveryServices.SiteRecovery)
- 已從 `New/Set-AzRecoveryServicesAsrPolicy` Cmdlet 移除 `Encryption` 參數
- `TargetStorageAccountName` 現在是 `Restore-AzRecoveryServicesBackupItem` Cmdlet 中用於還原受控磁碟的必要參數
- 已在 `Restore-AzRecoveryServicesBackupItem` Cmdlet 中移除 `StorageAccountName` 和 `StorageAccountResourceGroupName` 參數
- 已在 `Get-AzRecoveryServicesBackupContainer` Cmdlet 中移除 `Name` 參數

### <a name="azresources-previously-azurermresources"></a>Az.Resources (先前是 AzureRM.Resources)
- 已從 `New/Set-AzPolicyAssignment` Cmdlet 移除 `Sku` 參數
- 已從 `New-AzADServicePrincipal` 和 `New-AzADSpCredential` Cmdlet 移除 `Password` 參數。密碼會自動產生，提供密碼的指令碼：
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  應變更為從輸出擷取密碼：
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (先前是 AzureRM.ServiceFabric)
- 已變更下列 Cmdlet 的傳回類型：
  - 已移除 `ApplicationHealthPolicy` 類型的 `SerivceTypeHealthPolicies` 屬性。
  - 已移除 `ClusterUpgradeDeltaHealthPolicy` 類型的 `ApplicationHealthPolicies` 屬性。
  - 已移除 `ClusterUpgradePolicy` 類型的 `OverrideUserUpgradePolicy` 屬性。
  - 這些變更會影響下列 Cmdlet：
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (previously AzureRM.Sql)
- 已從 `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` Cmdlet 移除 `State` 和 `ResourceId` 參數
- 已移除淘汰的 Cmdlet：`Get/Set-AzSqlServerBackupLongTermRetentionVault`、`Get/Start/Stop-AzSqlServerUpgrade`、`Get/Set-AzSqlDatabaseAuditingPolicy`、`Get/Set-AzSqlServerAuditingPolicy`、`Remove-AzSqlDatabaseAuditing`、`Remove-AzSqlServerAuditing`
- 已從 `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` Cmdlet 移除淘汰的 `Current` 參數
- 已從 `Get-AzSqlServerServiceObjective` Cmdlet 移除淘汰的 `DatabaseName` 參數
- 已從 `Set-AzSqlDatabaseDataMaskingPolicy` Cmdlet 移除淘汰的 `PrivilegedLogin` 參數

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (先前是 Azure.Storage 和 AzureRM.Storage)
- 為了支援建立僅具有儲存體帳戶名稱的 Oauth 儲存體內容，預設參數集已變更為 `OAuthParameterSet`
  - 範例： `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- `Location` 已成為 `Get-AzStorageUsage` Cmdlet 的必要參數
- 儲存體 API 方法現在會使用以工作為基礎的非同步模式 (TAP)，而非使用同步 API 呼叫。
#### <a name="1-blob-snapshot"></a>1.Blob 快照集
##### <a name="before"></a>之前：
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>之後︰
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2.共用快照集
##### <a name="before"></a>之前：
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>之後︰
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3.取消刪除虛刪除的 Blob
##### <a name="before"></a>之前：
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>之後︰
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4.設定 Blob 層
##### <a name="before"></a>之前：
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>之後︰
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (先前是 AzureRM.Websites)
- 已從 `PSAppServicePlan`、`PSCertificate`、`PSCloningInfo` 和 `PSSite` 物件移除淘汰的屬性