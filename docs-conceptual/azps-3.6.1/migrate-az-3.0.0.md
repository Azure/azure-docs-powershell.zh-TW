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
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2020
ms.locfileid: "79035680"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="7883b-103">Az 3.0.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="7883b-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="7883b-104">本文件說明 Az 2.0.0 與 3.0.0 版之間的變更</span><span class="sxs-lookup"><span data-stu-id="7883b-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="7883b-105">Az 3.0.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="7883b-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="7883b-106">Batch</span><span class="sxs-lookup"><span data-stu-id="7883b-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - <span data-ttu-id="7883b-107">[與舊版 `Az.Resources`](#previous-version-incompatibility-with-azresources-module) 不相容</span><span class="sxs-lookup"><span data-stu-id="7883b-107">[Incompatibility with previous versions of `Az.Resources`](#previous-version-incompatibility-with-azresources-module)</span></span>
  - [<span data-ttu-id="7883b-108">計算</span><span class="sxs-lookup"><span data-stu-id="7883b-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="7883b-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7883b-109">HDInsight</span></span>](#hdinsight)
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
  - [<span data-ttu-id="7883b-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="7883b-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="7883b-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7883b-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="7883b-112">資源</span><span class="sxs-lookup"><span data-stu-id="7883b-112">Resources</span></span>](#resources)
    - <span data-ttu-id="7883b-113">[與舊版 `Az.Batch`](#previous-version-incompatibility-with-azbatch-module) 不相容</span><span class="sxs-lookup"><span data-stu-id="7883b-113">[Incompatibility with previous versions of `Az.Batch`](#previous-version-incompatibility-with-azbatch-module)</span></span>
  - [<span data-ttu-id="7883b-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7883b-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="7883b-115">Sql</span><span class="sxs-lookup"><span data-stu-id="7883b-115">Sql</span></span>](#sql)
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


## <a name="batch"></a><span data-ttu-id="7883b-116">Batch</span><span class="sxs-lookup"><span data-stu-id="7883b-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="7883b-117">已移除 `Get-AzBatchNodeAgentSku`，並以 `Get-AzBatchSupportedImage` 取代。</span><span class="sxs-lookup"><span data-stu-id="7883b-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="7883b-118">`Get-AzBatchSupportedImage` 會傳回與 `Get-AzBatchNodeAgentSku` 相同的資料，但格式較易懂。</span><span class="sxs-lookup"><span data-stu-id="7883b-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="7883b-119">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="7883b-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="7883b-120">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7883b-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-121">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="7883b-122">After</span><span class="sxs-lookup"><span data-stu-id="7883b-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="7883b-123">與 Az. Resources 模組的舊版不相容</span><span class="sxs-lookup"><span data-stu-id="7883b-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="7883b-124">‘Az.Batch’ 模組的 2.0.1 版本與 ‘Az.Resources’ 模組的舊版 (1.7.0 或更早版本) 不相容。</span><span class="sxs-lookup"><span data-stu-id="7883b-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="7883b-125">這會導致在匯入 ‘Az.Batch’ 模組的 2.0.1 版本時，無法匯入 ‘Az.Resources’ 模組的 1.7.0 版本。</span><span class="sxs-lookup"><span data-stu-id="7883b-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="7883b-126">要修正此問題，只要將 ‘Az.Resources’ 模組更新為 1.7.1 或更高版本，或只安裝最新版的 ‘Az’ 模組即可。</span><span class="sxs-lookup"><span data-stu-id="7883b-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="7883b-127">計算</span><span class="sxs-lookup"><span data-stu-id="7883b-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="7883b-128">上傳 CreateOption 時，已使用 `UploadSizeInBytes` 參數而非 `New-AzDiskConfig` 的 `DiskSizeGB`</span><span class="sxs-lookup"><span data-stu-id="7883b-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-129">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="7883b-130">After</span><span class="sxs-lookup"><span data-stu-id="7883b-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="7883b-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7883b-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="7883b-132">已更新 `Get-AzHDInsightJobOutput` Cmdlet 以支援對儲存體金鑰的細微角色型存取。</span><span class="sxs-lookup"><span data-stu-id="7883b-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="7883b-133">具有 HDInsight 叢集操作員、參與者或擁有者角色的使用者將不受影響。</span><span class="sxs-lookup"><span data-stu-id="7883b-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="7883b-134">具有讀者角色的使用者將必須明確指定 `DefaultStorageAccountKey` 參數。</span><span class="sxs-lookup"><span data-stu-id="7883b-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-135">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="7883b-136">After</span><span class="sxs-lookup"><span data-stu-id="7883b-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="7883b-137">Cmdlet `Add-AzHDInsightConfigValue` 已移除 `Add-AzHDInsightConfigValues` 的別名。</span><span class="sxs-lookup"><span data-stu-id="7883b-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-138">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-138">Before</span></span>
<span data-ttu-id="7883b-139">使用已淘汰的別名</span><span class="sxs-lookup"><span data-stu-id="7883b-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="7883b-140">After</span><span class="sxs-lookup"><span data-stu-id="7883b-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="7883b-141">已新增新的 `Disable-AzHDInsightMonitoring` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="7883b-142">使用此 Cmdlet 來停用 HDInsight 叢集中的監視 (取代 `Disable-AzHDInsightOperationsManagementSuite` 和 `Disable-AzHDInsightOMS`)。</span><span class="sxs-lookup"><span data-stu-id="7883b-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-143">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="7883b-144">After</span><span class="sxs-lookup"><span data-stu-id="7883b-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="7883b-145">已新增新的 `Enable-AzHDInsightMonitoring` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="7883b-146">使用此 Cmdlet 來啟用 HDInsight 叢集中的監視 (取代 `Enable-AzHDInsightOperationsManagementSuite` 和 `Enable-AzHDInsightOMS`)。</span><span class="sxs-lookup"><span data-stu-id="7883b-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-147">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="7883b-148">After</span><span class="sxs-lookup"><span data-stu-id="7883b-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="7883b-149">已新增新的 `Get-AzHDInsightMonitoring` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="7883b-150">使用此 Cmdlet 取得Azure HDInsight 叢集中的安裝監視狀態 (取代 `Get-AzHDInsightOperationsManagementSuite` 和 `Get-AzHDInsightOMS`)。</span><span class="sxs-lookup"><span data-stu-id="7883b-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-151">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="7883b-152">After</span><span class="sxs-lookup"><span data-stu-id="7883b-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="7883b-153">Cmdlet `Get-HDInsightProperty` 已移除 `Get-AzHDInsightProperties` 的別名。</span><span class="sxs-lookup"><span data-stu-id="7883b-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-154">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-154">Before</span></span>
<span data-ttu-id="7883b-155">使用已淘汰的別名</span><span class="sxs-lookup"><span data-stu-id="7883b-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="7883b-156">After</span><span class="sxs-lookup"><span data-stu-id="7883b-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="7883b-157">已移除 `Grant-AzHDInsightRdpServicesAccess` 和 `Revoke-AzHDInsightRdpServicesAccess` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="7883b-158">因為不支援使用 Windows OS 類型的叢集，所以不再需要這些項目。</span><span class="sxs-lookup"><span data-stu-id="7883b-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="7883b-159">請改為使用 Linux OS 類型來建立叢集。</span><span class="sxs-lookup"><span data-stu-id="7883b-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="7883b-160">`Remove-AzHDInsightCluster` 的輸出類型從 `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` 變更為 `bool`。</span><span class="sxs-lookup"><span data-stu-id="7883b-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-161">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="7883b-162">After</span><span class="sxs-lookup"><span data-stu-id="7883b-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="7883b-163">Cmdlet 已淘汰，</span><span class="sxs-lookup"><span data-stu-id="7883b-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="7883b-164">且沒有取代項目。</span><span class="sxs-lookup"><span data-stu-id="7883b-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="7883b-165">`Set-AzHDInsightGatewayCredential` 的輸出類型從 `HttpConnectivitySettings` 變更為 `AzureHDInsightGatewaySettings`。</span><span class="sxs-lookup"><span data-stu-id="7883b-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="7883b-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="7883b-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="7883b-167">已移除別名；請改用 `New-AzIotHubImportDevice`。</span><span class="sxs-lookup"><span data-stu-id="7883b-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-168">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="7883b-169">After</span><span class="sxs-lookup"><span data-stu-id="7883b-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="7883b-170">已移除別名；請改用 `New-AzIotHubExportDevice`。</span><span class="sxs-lookup"><span data-stu-id="7883b-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-171">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="7883b-172">After</span><span class="sxs-lookup"><span data-stu-id="7883b-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="7883b-173">參數 `EventHubEndPointName` 已淘汏且沒有取代項目。因為 IotHub 只有一個內建 endpoint("events")，無法處理系統和裝置訊息。</span><span class="sxs-lookup"><span data-stu-id="7883b-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-174">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="7883b-175">After</span><span class="sxs-lookup"><span data-stu-id="7883b-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="7883b-176">參數 `EventHubEndPointName` 已淘汏且沒有取代項目。因為 IotHub 只有一個內建 endpoint("events")，無法處理系統和裝置訊息。</span><span class="sxs-lookup"><span data-stu-id="7883b-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-177">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="7883b-178">After</span><span class="sxs-lookup"><span data-stu-id="7883b-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="7883b-179">參數 `EventHubEndPointName` 已淘汏且沒有取代項目。因為 IotHub 只有一個內建 endpoint("events")，無法處理系統和裝置訊息。</span><span class="sxs-lookup"><span data-stu-id="7883b-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-180">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="7883b-181">After</span><span class="sxs-lookup"><span data-stu-id="7883b-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="7883b-182">參數 `OperationsMonitoringProperties` 已淘汏且沒有取代項目。因為 IotHub 不再使用內建 endpoint("operationsMonitoringEvents")。</span><span class="sxs-lookup"><span data-stu-id="7883b-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="7883b-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7883b-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="7883b-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`、`ASRRecoveryPlanGroup.StartGroupActions` 和 `ASRRecoveryPlanGroup.EndGroupActions` 已從輸出中移除。</span><span class="sxs-lookup"><span data-stu-id="7883b-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="7883b-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`、`ASRRecoveryPlanGroup.StartGroupActions` 和 `ASRRecoveryPlanGroup.EndGroupActions` 已從輸出中移除。</span><span class="sxs-lookup"><span data-stu-id="7883b-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="7883b-186">參數 IncludeDiskId已變更為直接支援寫入 Azure Site Recovery 中的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="7883b-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-187">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="7883b-188">After</span><span class="sxs-lookup"><span data-stu-id="7883b-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="7883b-189">資源</span><span class="sxs-lookup"><span data-stu-id="7883b-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="7883b-190">與 Az.Batch 模組的舊版不相容</span><span class="sxs-lookup"><span data-stu-id="7883b-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="7883b-191">‘Az.Resources’ 模組的1.7.1 版本與 ‘Az.Batch’ 模組的舊版 (1.1.2 或更早版本) 不相容。</span><span class="sxs-lookup"><span data-stu-id="7883b-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="7883b-192">這會導致在匯入 ‘Az.Resources’ 模組的 1.7.1 版本時，無法匯入 ‘Az.Batch’ 模組的 1.1.2 版本。</span><span class="sxs-lookup"><span data-stu-id="7883b-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="7883b-193">要修正此問題，請將 ‘Az.Batch’ 模組更新為 2.0.1 或更高版本，或只安裝最新版的 ‘Az’ 模組即可。</span><span class="sxs-lookup"><span data-stu-id="7883b-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="7883b-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7883b-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="7883b-195">已移除 `Add-ServiceFabricApplicationCertificate`，因為 `Add-AzVmssSecret` 涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="7883b-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-196">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="7883b-197">After</span><span class="sxs-lookup"><span data-stu-id="7883b-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="7883b-198">Sql</span><span class="sxs-lookup"><span data-stu-id="7883b-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="7883b-199">請注意，安全連線已被取代，因此會移除命令。</span><span class="sxs-lookup"><span data-stu-id="7883b-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="7883b-200">請使用 Azure 入口網站中的 SQL 資料庫刀鋒視窗來檢視連接字串</span><span class="sxs-lookup"><span data-stu-id="7883b-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="7883b-201">已移除 `Get-AzSqlDatabaseIndexRecommendations` 別名。</span><span class="sxs-lookup"><span data-stu-id="7883b-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="7883b-202">請改用 `Get-AzSqlDatabaseIndexRecommendation`。</span><span class="sxs-lookup"><span data-stu-id="7883b-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="7883b-203">已移除 `Get-AzSqlDatabaseRestorePoints` 別名。</span><span class="sxs-lookup"><span data-stu-id="7883b-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="7883b-204">請改用 `Get-AzSqlDatabaseRestorePoint`。</span><span class="sxs-lookup"><span data-stu-id="7883b-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="7883b-205">Cmdlet `Get-AzSqlDatabaseAudit` 已取代此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="7883b-206">輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel'，並移除了屬性 `AuditState` 和 `StorageAccountName`。</span><span class="sxs-lookup"><span data-stu-id="7883b-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="7883b-207">和 `StorageAccountSubscriptionId`。</span><span class="sxs-lookup"><span data-stu-id="7883b-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="7883b-208">指令碼可以從新的 `StorageAccountResourceId` 屬性取得儲存體帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="7883b-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-209">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-209">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-210">After</span><span class="sxs-lookup"><span data-stu-id="7883b-210">After</span></span>
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
- <span data-ttu-id="7883b-211">Cmdlet `Set-AzSqlDatabaseAudit` 已取代此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="7883b-212">輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'bool'</span><span class="sxs-lookup"><span data-stu-id="7883b-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-213">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-214">After</span><span class="sxs-lookup"><span data-stu-id="7883b-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="7883b-215">Cmdlet `Get-AzSqlServerAudit` 已取代此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="7883b-216">輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'，</span><span class="sxs-lookup"><span data-stu-id="7883b-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="7883b-217">並移除了屬性 `AuditState`、`StorageAccountName` 和 `StorageAccountSubscriptionId`。</span><span class="sxs-lookup"><span data-stu-id="7883b-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="7883b-218">使用 `StorageAccountName` 和 `StorageAccountSubscriptionId` 屬性的指令碼可從新的 `StorageAccountResourceId` 屬性取出此資訊。</span><span class="sxs-lookup"><span data-stu-id="7883b-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-219">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-219">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-220">After</span><span class="sxs-lookup"><span data-stu-id="7883b-220">After</span></span>
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
- <span data-ttu-id="7883b-221">Cmdlet `Set-AzSqlServerAudit` 已取代此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7883b-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="7883b-222">輸出類型正在從現有的類型 :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' 變更為新類型：'bool'</span><span class="sxs-lookup"><span data-stu-id="7883b-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-223">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="7883b-224">After</span><span class="sxs-lookup"><span data-stu-id="7883b-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="7883b-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` 已由 `Get-AzSqlServerAdvancedThreatProtectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-226">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="7883b-227">After</span><span class="sxs-lookup"><span data-stu-id="7883b-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="7883b-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` 已由 `Clear-AzSqlServerAdvancedThreatProtectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-229">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="7883b-230">After</span><span class="sxs-lookup"><span data-stu-id="7883b-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="7883b-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` 已由 `Update-AzSqlServerAdvancedThreatProtectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-232">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="7883b-233">After</span><span class="sxs-lookup"><span data-stu-id="7883b-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="7883b-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` 已由 `Get-AzSqlDatabaseAdvancedThreatProtectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-235">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-236">After</span><span class="sxs-lookup"><span data-stu-id="7883b-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="7883b-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` 已由 `Update-AzSqlDatabaseAdvancedThreatProtectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-238">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="7883b-239">After</span><span class="sxs-lookup"><span data-stu-id="7883b-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="7883b-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` 已由 `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-241">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-242">After</span><span class="sxs-lookup"><span data-stu-id="7883b-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` 已由 `Update-AzSqlDatabaseVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-244">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-244">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-245">After</span><span class="sxs-lookup"><span data-stu-id="7883b-245">After</span></span>
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
<span data-ttu-id="7883b-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` 已由 `Get-AzSqlDatabaseVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-247">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-248">After</span><span class="sxs-lookup"><span data-stu-id="7883b-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-250">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-251">After</span><span class="sxs-lookup"><span data-stu-id="7883b-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` 已由 `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-253">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-253">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-254">After</span><span class="sxs-lookup"><span data-stu-id="7883b-254">After</span></span>
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
<span data-ttu-id="7883b-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` 已由 `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-256">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-257">After</span><span class="sxs-lookup"><span data-stu-id="7883b-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-259">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-260">After</span><span class="sxs-lookup"><span data-stu-id="7883b-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` 已由 `Update-AzSqlInstanceVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-262">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-262">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-263">After</span><span class="sxs-lookup"><span data-stu-id="7883b-263">After</span></span>
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
<span data-ttu-id="7883b-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` 已由 `Get-AzSqlInstanceVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-265">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-266">After</span><span class="sxs-lookup"><span data-stu-id="7883b-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlInstanceVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-268">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-269">After</span><span class="sxs-lookup"><span data-stu-id="7883b-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` 已由 `Update-AzSqlServerVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-271">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-271">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-272">After</span><span class="sxs-lookup"><span data-stu-id="7883b-272">After</span></span>
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
<span data-ttu-id="7883b-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` 已由 `Get-AzSqlServerVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-274">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-275">After</span><span class="sxs-lookup"><span data-stu-id="7883b-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="7883b-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` 已由 `Clear-AzSqlServerVulnerabilityAssessmentSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-277">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-278">After</span><span class="sxs-lookup"><span data-stu-id="7883b-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="7883b-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` 已刪除，且沒有取代的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7883b-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="7883b-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` 已由 `Get-AzSqlServerThreatDetectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-281">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-281">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-282">After</span><span class="sxs-lookup"><span data-stu-id="7883b-282">After</span></span>
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
<span data-ttu-id="7883b-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` 已由 `Clear-AzSqlServerThreatDetectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-284">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="7883b-285">After</span><span class="sxs-lookup"><span data-stu-id="7883b-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="7883b-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` 已由 `Update-AzSqlServerThreatDetectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-287">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="7883b-288">After</span><span class="sxs-lookup"><span data-stu-id="7883b-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="7883b-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` 已由 `Get-AzSqlDatabaseThreatDetectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-290">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-290">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="7883b-291">After</span><span class="sxs-lookup"><span data-stu-id="7883b-291">After</span></span>
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
<span data-ttu-id="7883b-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` 已由 `Update-AzSqlDatabaseThreatDetectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-293">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="7883b-294">After</span><span class="sxs-lookup"><span data-stu-id="7883b-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="7883b-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` 已由 `Clear-AzSqlDatabaseThreatDetectionSetting` 取代</span><span class="sxs-lookup"><span data-stu-id="7883b-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="7883b-296">之前</span><span class="sxs-lookup"><span data-stu-id="7883b-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="7883b-297">After</span><span class="sxs-lookup"><span data-stu-id="7883b-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
