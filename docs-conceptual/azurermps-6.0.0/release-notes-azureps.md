---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911998"
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

---

## <a name="600---may-2018"></a>6.0.0 - 2018 年 5 月

### <a name="general"></a>一般
* 將模組的最小相依性設定為 PowerShell 5.0

### <a name="azurestorage"></a>Azure.Storage
* 支援做為儲存體 Blob 容器名稱
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* 修正此問題：某些儲存體 Cmdlet 失敗輸出未包含詳細的失敗資訊

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermautomation"></a>AzureRM.Automation
* 從 Cmdlet 移除取代的 'Tags' 別名
    - 'Set-AzureRmAutomationRunbook'

### <a name="azurermbatch"></a>AzureRM.Batch
* 已更新 New-AzureBatchPool 文件以移除取代的範例

### <a name="azurermcdn"></a>AzureRM.Cdn
* 推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVm' 和 'New-AzureRmVmss' 支援參數的詳細資訊輸出
* 'New-AzureRmVm' 和 'New-AzureRmVmss' (簡單參數集) 支援將使用者定義和 (或) 系統定義的身分識別指派至虛擬機器。
* VMSS 重新部署和執行維護功能
    -  將新的切換參數 -Redeploy 和 -PerformMaintenance 新增至 'Set-AzureRmVmss' 和 'Set-AzureRmVmssVM'
* 將 DisableVMAgent 切換參數新增至 'Set-AzureRmVMOperatingSystem' Cmdlet
* 'New-AzureRmVm' 和 'New-AzureRmVmss' (簡單參數集全) 支援 'Win10' 映像。
* 已新增 'Repair-AzureRmVmssServiceFabricUpdateDomain' Cmdlet。
* 推出多項重大變更
    - 如需詳細資料，請參閱移轉指南
* 'Set-AzureRmVmDiskEncryptionExtension' 讓 AAD 參數成為選用

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 從 Cmdlet 移除取代的 'Tags' 別名
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已將 ADF .Net SDK 更新為版本 0.7.0-preview，包含以下變更：
    - 已在 ExecuteSSISPackage 活動上新增執行參數和連線管理員屬性
    - 已更新 PostgreSql、MySql 連結服務，以使用完整的連接字串，而不是伺服器、資料庫、結構描述、使用者名稱和密碼
    - 已從 DB2 連結服務中移除結構描述
    - 已從 Teradata 連結服務中移除結構描述屬性
    - 已新增 Responsys 的 LinkedService、Dataset、CopySource

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 從 Cmdlet 移除取代的 'Tags' 別名
    - 'New-AzureRmDataLakeAnalyticsAccount'
    - 'Set-AzureRmDataLakeAnalyticsAccount'

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 對 Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的遞迴 Acl 變更新增新的功能
* 新增 Cmdlet 以擷取目錄下的內容摘要
* 新增 Cmdlet 以擷取磁碟使用量和 ACL 傾印
* 將 Set-AzureRmDataLakeStoreItemAcl 布林的傳回類型更正為 IEnumerable<DataLakeStoreItemAce>
* 將 Set-AzureRmDataLakeStoreItemAclEntry 布林的傳回類型更正為 IEnumerable<DataLakeStoreItemAce>
* Export-AzureRmDataLakeStoreItem、Import-AzureRmDataLakeStoreItem、Remove-AzureRmDataLakeStoreItem 的重大變更

### <a name="azurermdns"></a>AzureRM.Dns
* 推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermeventhub"></a>AzureRM.EventHub
* 更新 Cmdlet 的說明，加上遺漏的範例

### <a name="azurerminsights"></a>AzureRM.Insights
* 已推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermiothub"></a>AzureRM.IotHub
* 啟用 IotHub 的標記和基本 SKU

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 支援管線案例的重大變更
* 新增新的 Cmdlet：Backup/Restore-AzureKeyVaultManagedStorageAccount、Backup/Restore-AzureKeyVaultCertificate、Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval 和 Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 從 Cmdlet 移除取代的 'Tags' 別名
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* 從 Cmdlet 移除取代的 'Tags' 別名
    - 'Set-AzureRmMediaService'

### <a name="azurermnetwork"></a>AzureRM.Network
* 針對 DDoS 保護計劃資源新增支援
* 已推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermprofile"></a>AzureRM.Profile
* 依預設啟用內容自動儲存
* 將 USGovernmentOperationalInsightsEndpoint 和 USGovernmentOperationalInsightsEndpointResourceId 屬性新增至適用於 US Gov 的 Azure 環境中。

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 已修正 SiteRecovery 案例中的驗證標頭

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 已推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermresources"></a>AzureRM.Resources
* 從 Get-AzureRmRoledefinition 呼叫中移除已淘汰的參數 -AtScopeAndBelow
* 在 Get-AzureRmRoleAssignment 結果中納入指派給已刪除的使用者/群組/服務主體
* 針對範圍和資源類型新增 Tab 完成器
* 新增用於建立服務主體的便利 Cmdlet
* 合併 Get-AzureRmResource 的 Get- 和 Find- 功能
* 新增 AD Cmdlet：
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 更新預設的 Linux 映像版本 SKU
  - NewAzureServiceFabricCluster.cs 預設 UbuntuServer1604 SKU 更新

### <a name="azurermstorage"></a>AzureRM.Storage
* 已推出多項重大變更
    - 如需詳細資訊，請參閱移轉指南

### <a name="azurermwebsites"></a>AzureRM.Websites
* 升級至最新版本的網站 SDK
* 已新增 Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot 的 -AssignIdentity 和 -Httpsonly 屬性
* 已新增兩個新的 Cmdlet：Get-AzureRmWebAppSnapshots 和 Restore-AzureRmWebAppSnapshot
