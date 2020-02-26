---
title: Az 3.0.0 的移轉指南
description: 本移轉指南包含在 Az 3.0 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: e88752e0c997efc4f49161e358072803cb63450a
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477724"
---
# <a name="migration-guide-for-az-300"></a>Az 3.0.0 的移轉指南

本文件說明 Az 2.0.0 與 3.0.0 版之間的變更

<!-- TOC -->

- [Az 3.0.0 的移轉指南](#migration-guide-for-az-300)
  - [Batch](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [與舊版 `Az.Resources`](#previous-version-incompatibility-with-azresources-module) 不相容
  - [計算](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [HDInsight](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [IotHub](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [RecoveryServices](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [資源](#resources)
    - [與舊版 `Az.Batch`](#previous-version-incompatibility-with-azbatch-module) 不相容
  - [ServiceFabric](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [Sql](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a>Batch

### `Get-AzBatchNodeAgentSku`
- 已移除 `Get-AzBatchNodeAgentSku`，並以 `Get-AzBatchSupportedImage` 取代。
- `Get-AzBatchSupportedImage` 會傳回與 `Get-AzBatchNodeAgentSku` 相同的資料，但格式較易懂。
- 系統現在也會傳回新的未驗證映像。 此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。

#### <a name="before"></a>之前
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a>After
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a>與 Az. Resources 模組的舊版不相容
‘Az.Batch’ 模組的 2.0.1 版本與 ‘Az.Resources’ 模組的舊版 (1.7.0 或更早版本) 不相容。  這會導致在匯入 ‘Az.Batch’ 模組的 2.0.1 版本時，無法匯入 ‘Az.Resources’ 模組的 1.7.0 版本。  要修正此問題，只要將 ‘Az.Resources’ 模組更新為 1.7.1 或更高版本，或只安裝最新版的 ‘Az’ 模組即可。

## <a name="compute"></a>計算

### `New-AzDiskConfig`
上傳 CreateOption 時，已使用 `UploadSizeInBytes` 參數而非 `New-AzDiskConfig` 的 `DiskSizeGB`

#### <a name="before"></a>之前
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a>After
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a>HDInsight

### `Get-AzHDInsightJobOutput`
- 已更新 `Get-AzHDInsightJobOutput` Cmdlet 以支援對儲存體金鑰的細微角色型存取。
- 具有 HDInsight 叢集操作員、參與者或擁有者角色的使用者將不受影響。
- 具有讀者角色的使用者將必須明確指定 `DefaultStorageAccountKey` 參數。

#### <a name="before"></a>之前
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a>After
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
Cmdlet `Add-AzHDInsightConfigValue` 已移除 `Add-AzHDInsightConfigValues` 的別名。

#### <a name="before"></a>之前
使用已淘汰的別名
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a>After
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
已新增新的 `Disable-AzHDInsightMonitoring` Cmdlet。 使用此 Cmdlet 來停用 HDInsight 叢集中的監視 (取代 `Disable-AzHDInsightOperationsManagementSuite` 和 `Disable-AzHDInsightOMS`)。

#### <a name="before"></a>之前
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a>After
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
已新增新的 `Enable-AzHDInsightMonitoring` Cmdlet。 使用此 Cmdlet 來啟用 HDInsight 叢集中的監視 (取代 `Enable-AzHDInsightOperationsManagementSuite` 和 `Enable-AzHDInsightOMS`)。

#### <a name="before"></a>之前
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a>After
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
已新增新的 `Get-AzHDInsightMonitoring` Cmdlet。 使用此 Cmdlet 取得Azure HDInsight 叢集中的安裝監視狀態 (取代 `Get-AzHDInsightOperationsManagementSuite` 和 `Get-AzHDInsightOMS`)。

#### <a name="before"></a>之前
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a>After
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
Cmdlet `Get-HDInsightProperty` 已移除 `Get-AzHDInsightProperties` 的別名。

#### <a name="before"></a>之前
使用已淘汰的別名
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a>After
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
已移除 `Grant-AzHDInsightRdpServicesAccess` 和 `Revoke-AzHDInsightRdpServicesAccess` Cmdlet。 因為不支援使用 Windows OS 類型的叢集，所以不再需要這些項目。 請改為使用 Linux OS 類型來建立叢集。

### `Remove-AzHDInsightCluster`
`Remove-AzHDInsightCluster` 的輸出類型從 `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` 變更為 `bool`。

#### <a name="before"></a>之前
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a>After
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
Cmdlet 已淘汰， 且沒有取代項目。

### `Set-AzHDInsightGatewayCredential`
`Set-AzHDInsightGatewayCredential` 的輸出類型從 `HttpConnectivitySettings` 變更為 `AzureHDInsightGatewaySettings`。



## <a name="iothub"></a>IotHub

### `New-AzIotHubImportDevices`
已移除別名；請改用 `New-AzIotHubImportDevice`。

#### <a name="before"></a>之前
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a>After
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
已移除別名；請改用 `New-AzIotHubExportDevice`。

#### <a name="before"></a>之前
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a>After
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
參數 `EventHubEndPointName` 已淘汏且沒有取代項目。因為 IotHub 只有一個內建 endpoint("events")，無法處理系統和裝置訊息。

#### <a name="before"></a>之前
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a>After
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
參數 `EventHubEndPointName` 已淘汏且沒有取代項目。因為 IotHub 只有一個內建 endpoint("events")，無法處理系統和裝置訊息。

#### <a name="before"></a>之前
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a>After
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
參數 `EventHubEndPointName` 已淘汏且沒有取代項目。因為 IotHub 只有一個內建 endpoint("events")，無法處理系統和裝置訊息。

#### <a name="before"></a>之前
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a>After
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
參數 `OperationsMonitoringProperties` 已淘汏且沒有取代項目。因為 IotHub 不再使用內建 endpoint("operationsMonitoringEvents")。



## <a name="recoveryservices"></a>RecoveryServices

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
`ASRRecoveryPlanGroup.ReplicationProtectedItems`、`ASRRecoveryPlanGroup.StartGroupActions` 和 `ASRRecoveryPlanGroup.EndGroupActions` 已從輸出中移除。

### `Get-AzRecoveryServicesAsrRecoveryPlan`
`ASRRecoveryPlanGroup.ReplicationProtectedItems`、`ASRRecoveryPlanGroup.StartGroupActions` 和 `ASRRecoveryPlanGroup.EndGroupActions` 已從輸出中移除。

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
參數 IncludeDiskId已變更為直接支援寫入 Azure Site Recovery 中的受控磁碟。

#### <a name="before"></a>之前
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a>After
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a>資源

### <a name="previous-version-incompatibility-with-azbatch-module"></a>與 Az.Batch 模組的舊版不相容
‘Az.Resources’ 模組的1.7.1 版本與 ‘Az.Batch’ 模組的舊版 (1.1.2 或更早版本) 不相容。  這會導致在匯入 ‘Az.Resources’ 模組的 1.7.1 版本時，無法匯入 ‘Az.Batch’ 模組的 1.1.2 版本。  要修正此問題，請將 ‘Az.Batch’ 模組更新為 2.0.1 或更高版本，或只安裝最新版的 ‘Az’ 模組即可。

## <a name="servicefabric"></a>ServiceFabric

### `Add-ServiceFabricApplicationCertificate`
已移除 `Add-ServiceFabricApplicationCertificate`，因為 `Add-AzVmssSecret` 涵蓋此案例。

#### <a name="before"></a>之前
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a>After
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a>Sql

### `Get-AzSqlDatabaseSecureConnectionPolicy`
請注意，安全連線已被取代，因此會移除命令。 請使用 Azure 入口網站中的 SQL 資料庫刀鋒視窗來檢視連接字串

### `Get-AzSqlDatabaseIndexRecommendations`
已移除 `Get-AzSqlDatabaseIndexRecommendations` 別名。 請改用 `Get-AzSqlDatabaseIndexRecommendation`。

### `Get-AzSqlDatabaseRestorePoints`
已移除 `Get-AzSqlDatabaseRestorePoints` 別名。 請改用 `Get-AzSqlDatabaseRestorePoint`。

### `Get-AzSqlDatabaseAuditing`
- Cmdlet `Get-AzSqlDatabaseAudit` 已取代此 Cmdlet。
- 輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel'，並移除了屬性 `AuditState` 和 `StorageAccountName`。 和 `StorageAccountSubscriptionId`。  指令碼可以從新的 `StorageAccountResourceId` 屬性取得儲存體帳戶資訊。

#### <a name="before"></a>之前
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a>After
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- Cmdlet `Set-AzSqlDatabaseAudit` 已取代此 Cmdlet。
- 輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'bool'

#### <a name="before"></a>之前
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- Cmdlet `Get-AzSqlServerAudit` 已取代此 Cmdlet。
- 輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'，  並移除了屬性 `AuditState`、`StorageAccountName` 和 `StorageAccountSubscriptionId`。  使用 `StorageAccountName` 和 `StorageAccountSubscriptionId` 屬性的指令碼可從新的 `StorageAccountResourceId` 屬性取出此資訊。

#### <a name="before"></a>之前
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a>After
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- Cmdlet `Set-AzSqlServerAudit` 已取代此 Cmdlet。
- 輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'bool'

#### <a name="before"></a>之前
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a>After
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` 已由 `Get-AzSqlServerAdvancedThreatProtectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a>After
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` 已由 `Clear-AzSqlServerAdvancedThreatProtectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` 已由 `Update-AzSqlServerAdvancedThreatProtectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>After
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` 已由 `Get-AzSqlDatabaseAdvancedThreatProtectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` 已由 `Update-AzSqlDatabaseAdvancedThreatProtectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>After
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` 已由 `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` 已由 `Update-AzSqlDatabaseVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>After
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` 已由 `Get-AzSqlDatabaseVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` 已由 `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>After
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` 已由 `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` 已由 `Update-AzSqlInstanceVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>After
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` 已由 `Get-AzSqlInstanceVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlInstanceVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` 已由 `Update-AzSqlServerVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>After
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` 已由 `Get-AzSqlServerVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlServerVulnerabilityAssessmentSetting` 取代

#### <a name="before"></a>之前
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` 已刪除，且沒有取代的 Cmdlet

### `Get-AzSqlServerThreatDetectionPolicy`
Cmdlet `Get-AzSqlServerThreatDetectionPolicy` 已由 `Get-AzSqlServerThreatDetectionSetting` 取代

#### <a name="before"></a>之前
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a>After
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` 已由 `Clear-AzSqlServerThreatDetectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
Cmdlet `Set-AzSqlServerThreatDetectionPolicy` 已由 `Update-AzSqlServerThreatDetectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>After
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` 已由 `Get-AzSqlDatabaseThreatDetectionSetting` 取代

#### <a name="before"></a>之前
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a>After
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` 已由 `Update-AzSqlDatabaseThreatDetectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>After
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` 已由 `Clear-AzSqlDatabaseThreatDetectionSetting` 取代

#### <a name="before"></a>之前
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a>After
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
