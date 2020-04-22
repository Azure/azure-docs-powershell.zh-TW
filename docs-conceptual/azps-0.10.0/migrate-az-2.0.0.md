---
title: Az 2.0.0 的移轉指南
description: 本移轉指南包含在 Az 2.0 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 133769c09f74e1d0d90eff0c6c4bdbb90d1ebe24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445487"
---
# <a name="migration-guide-for-az-200"></a>Az 2.0.0 的移轉指南

本文件說明 Az 1.0.0 與 2.0.0 版之間的變更 

## <a name="table-of-contents"></a>目錄
- [模組的重大變更](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>模組的重大變更

### <a name="azcompute"></a>Az.Compute

- 已從 `New-AzAvailabilitySet` 和 `Update-AzAvailabilitySet` Cmdlet 中移除 `Managed` 參數，而改用 ```Sku = Aligned```

  #### <a name="before"></a>之前

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- 為求一致，已從 `Update-AzImage` 中的 'ByName' 和 'ByResourceId' 參數集移除 `Image` 參數 
  
  #### <a name="before"></a>之前

  請注意，下列程式碼可運作，但由於未使用傳入的 ImageName，因此移除此參數並沒有功能上的影響。

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- 為求一致，已從 `Restart-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數
  
  #### <a name="before"></a>之前

  請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- 為求一致，已從 `Start-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數
  
  #### <a name="before"></a>之前

  請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- 為求一致，已從 `Stop-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數
  
  #### <a name="before"></a>之前

  請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- 為求一致，已從 `Remove-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數
  
  #### <a name="before"></a>之前

  請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>After

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- 為求一致，已從 `Set-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數
  
  #### <a name="before"></a>之前

  請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- 為求一致，已從 `Save-AzVMImage` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數 
  
  #### <a name="before"></a>之前
  請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>After
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- 已新增 ProtectionPolicy 屬性，以將 `ProtectFromScaleIn` 屬性封裝在 `PSVirtualMachineScaleSetVM` 中

  #### <a name="before"></a>之前

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- 已新增 ```EncryptionSettingsCollection``` 屬性，以將 `EncryptionSettings` 屬性含括在 `PSDisk` 中

  #### <a name="before"></a>之前

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- 已新增 ```EncryptionSettingsCollection``` 屬性，以將 `EncryptionSettings` 屬性含括在 `PSSnapshot` 中

  #### <a name="before"></a>之前

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- 已從 `PSVirtualMachineScaleSet` 中移除 `VirtualMachineProfile` 屬性

  #### <a name="before"></a>之前

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- Cmdlet `Set-AzVMBootDiagnostic` 已移除 `Set-AzVMBootDiagnostics` 的別名

  #### <a name="before"></a>之前

  使用已淘汰的別名

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- Cmdlet `Export-AzLogAnalyticThrottledRequest` 已移除 `Export-AzLogAnalyticThrottledRequests` 的別名

  #### <a name="before"></a>之前

  使用已淘汰的別名

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>After

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- 已移除 `Grant-AzHDInsightHttpServicesAccess` 和 `Revoke-AzHDInsightHttpServicesAccess` Cmdlet。 由於所有 HDInsight 叢集上一律會啟用 HTTP 存取，因此不再需要這些項目。
- 已新增 `Set-AzHDInsightGatewayCredential` Cmdlet。 使用此 Cmdlet 可變更閘道 HTTP 使用者名稱和密碼 (取代 `Grant-AzHDInsightHttpServicesAccess`)。
- 已更新 `Get-AzHDInsightJobOutput` Cmdlet 以支援對儲存體金鑰的細微角色型存取。
    - 具有 HDInsight 叢集操作員、參與者或擁有者角色的使用者將不受影響。
    - 具有讀者角色的使用者將必須明確指定 `DefaultStorageAccountKey` 參數。

如需這些角色型存取權變更的詳細資訊，請參閱 [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)

  #### <a name="before"></a>之前

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>使用者僅具有 Cmdlet Get-AzHDInsightJobOutput 的讀者角色

  ####  <a name="before"></a>之前

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>After

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- 從 Blob、佇列和檔案 Cmdlet 傳回的類型已將其命名空間從 `Microsoft.WindowsAzure.Storage` 變更為 `Microsoft.Azure.Storage`。  雖然根據重大變更原則，這不是技術上的重大變更，但可能需要對使用儲存體 .Net SDK 方法的程式碼進行某些變更，才能與這些 Cmdlet 傳回的物件互動。

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>範例 1：將訊息新增至佇列 (變更 CloudQueueMessage 物件命名空間)

  之前： 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  之後：

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>範例 2：使用 AccessCondition 擷取 Blob/檔案屬性 (變更 AccessCondition 物件命名空間)

  之前： 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  之後：

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- 雖然並非技術上的重大變更，但在 `New/Get/Set-AzStorageAccount` 變更所傳回的儲存體帳戶中，您會發現其 Sku.Name 屬性的輸出有如下的差異。 (經過變更後，輸出和輸入的 SkuName 會相對應。)
  - "StandardLRS" -> "Standard_LRS";
  - "StandardGRS" -> "Standard_GRS";
  - "StandardRAGRS" -> "Standard_RAGRS";
  - "StandardZRS" -> "Standard_ZRS";
  - "PremiumLRS" -> "Premium_LRS";

- 在建立儲存體帳戶時未指定種類的預設服務行為已變更。  在舊版中，在建立儲存體帳戶時若未指定 `Kind`，將會使用 `Storage` 種類的儲存體帳戶，而新版本的預設 `Kind` 值則為 `StorageV2`。 如果您需要建立 'Storage' 種類的 V1 儲存體帳戶，請新增參數 '-Kind Storage'

  #### <a name="example--create-a-storage-account-default-kind-change"></a>範例：建立儲存體帳戶 (預設種類變更)  

  之前：

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  之後：

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
