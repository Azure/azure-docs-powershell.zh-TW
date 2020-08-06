---
title: Az 2.0.0 的移轉指南
description: 本移轉指南包含在 Az 2.0 版發行中對 Azure PowerShell 進行重大變更的清單。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 91362f3cc6b35e96a543c1304fb55acbf373d291
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566152"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="5213f-103">Az 2.0.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="5213f-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="5213f-104">本文件說明 Az 1.0.0 與 2.0.0 版之間的變更</span><span class="sxs-lookup"><span data-stu-id="5213f-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="5213f-105">目錄</span><span class="sxs-lookup"><span data-stu-id="5213f-105">Table of Contents</span></span>
- [<span data-ttu-id="5213f-106">模組的重大變更</span><span class="sxs-lookup"><span data-stu-id="5213f-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="5213f-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5213f-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="5213f-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5213f-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="5213f-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5213f-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="5213f-110">模組的重大變更</span><span class="sxs-lookup"><span data-stu-id="5213f-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="5213f-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5213f-111">Az.Compute</span></span>

- <span data-ttu-id="5213f-112">已從 `New-AzAvailabilitySet` 和 `Update-AzAvailabilitySet` Cmdlet 中移除 `Managed` 參數，而改用 ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="5213f-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-113">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-114">After</span><span class="sxs-lookup"><span data-stu-id="5213f-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="5213f-115">為求一致，已從 `Update-AzImage` 中的 'ByName' 和 'ByResourceId' 參數集移除 `Image` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="5213f-116">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-116">Before</span></span>

  <span data-ttu-id="5213f-117">請注意，下列程式碼可運作，但由於未使用傳入的 ImageName，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-118">After</span><span class="sxs-lookup"><span data-stu-id="5213f-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="5213f-119">為求一致，已從 `Restart-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="5213f-120">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-120">Before</span></span>

  <span data-ttu-id="5213f-121">請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-122">After</span><span class="sxs-lookup"><span data-stu-id="5213f-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="5213f-123">為求一致，已從 `Start-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="5213f-124">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-124">Before</span></span>

  <span data-ttu-id="5213f-125">請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-126">After</span><span class="sxs-lookup"><span data-stu-id="5213f-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="5213f-127">為求一致，已從 `Stop-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="5213f-128">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-128">Before</span></span>

  <span data-ttu-id="5213f-129">請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-130">After</span><span class="sxs-lookup"><span data-stu-id="5213f-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="5213f-131">為求一致，已從 `Remove-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="5213f-132">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-132">Before</span></span>

  <span data-ttu-id="5213f-133">請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-134">After</span><span class="sxs-lookup"><span data-stu-id="5213f-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="5213f-135">為求一致，已從 `Set-AzVM` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="5213f-136">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-136">Before</span></span>

  <span data-ttu-id="5213f-137">請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-138">After</span><span class="sxs-lookup"><span data-stu-id="5213f-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="5213f-139">為求一致，已從 `Save-AzVMImage` 中的 'ByObject' 和 'ByResourceId' 參數集移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="5213f-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="5213f-140">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-140">Before</span></span>
  <span data-ttu-id="5213f-141">請注意，下列程式碼可運作，但由於未使用傳入的 Name，因此移除此參數並沒有功能上的影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="5213f-142">After</span><span class="sxs-lookup"><span data-stu-id="5213f-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="5213f-143">已新增 ProtectionPolicy 屬性，以將 `ProtectFromScaleIn` 屬性封裝在 `PSVirtualMachineScaleSetVM` 中</span><span class="sxs-lookup"><span data-stu-id="5213f-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-144">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-145">After</span><span class="sxs-lookup"><span data-stu-id="5213f-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="5213f-146">已新增 ```EncryptionSettingsCollection``` 屬性，以將 `EncryptionSettings` 屬性含括在 `PSDisk` 中</span><span class="sxs-lookup"><span data-stu-id="5213f-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-147">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-147">Before</span></span>

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

  #### <a name="after"></a><span data-ttu-id="5213f-148">After</span><span class="sxs-lookup"><span data-stu-id="5213f-148">After</span></span>

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

- <span data-ttu-id="5213f-149">已新增 ```EncryptionSettingsCollection``` 屬性，以將 `EncryptionSettings` 屬性含括在 `PSSnapshot` 中</span><span class="sxs-lookup"><span data-stu-id="5213f-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-150">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-150">Before</span></span>

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

  #### <a name="after"></a><span data-ttu-id="5213f-151">After</span><span class="sxs-lookup"><span data-stu-id="5213f-151">After</span></span>

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

- <span data-ttu-id="5213f-152">已從 `PSVirtualMachineScaleSet` 中移除 `VirtualMachineProfile` 屬性</span><span class="sxs-lookup"><span data-stu-id="5213f-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-153">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-154">After</span><span class="sxs-lookup"><span data-stu-id="5213f-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="5213f-155">Cmdlet `Set-AzVMBootDiagnostic` 已移除 `Set-AzVMBootDiagnostics` 的別名</span><span class="sxs-lookup"><span data-stu-id="5213f-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-156">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-156">Before</span></span>

  <span data-ttu-id="5213f-157">使用已淘汰的別名</span><span class="sxs-lookup"><span data-stu-id="5213f-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-158">After</span><span class="sxs-lookup"><span data-stu-id="5213f-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="5213f-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` 已移除 `Export-AzLogAnalyticThrottledRequests` 的別名</span><span class="sxs-lookup"><span data-stu-id="5213f-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-160">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-160">Before</span></span>

  <span data-ttu-id="5213f-161">使用已淘汰的別名</span><span class="sxs-lookup"><span data-stu-id="5213f-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-162">After</span><span class="sxs-lookup"><span data-stu-id="5213f-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="5213f-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5213f-163">Az.HDInsight</span></span>

- <span data-ttu-id="5213f-164">已移除 `Grant-AzHDInsightHttpServicesAccess` 和 `Revoke-AzHDInsightHttpServicesAccess` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5213f-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="5213f-165">由於所有 HDInsight 叢集上一律會啟用 HTTP 存取，因此不再需要這些項目。</span><span class="sxs-lookup"><span data-stu-id="5213f-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="5213f-166">已新增 `Set-AzHDInsightGatewayCredential` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5213f-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="5213f-167">使用此 Cmdlet 可變更閘道 HTTP 使用者名稱和密碼 (取代 `Grant-AzHDInsightHttpServicesAccess`)。</span><span class="sxs-lookup"><span data-stu-id="5213f-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="5213f-168">已更新 `Get-AzHDInsightJobOutput` Cmdlet 以支援對儲存體金鑰的細微角色型存取。</span><span class="sxs-lookup"><span data-stu-id="5213f-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="5213f-169">具有 HDInsight 叢集操作員、參與者或擁有者角色的使用者將不受影響。</span><span class="sxs-lookup"><span data-stu-id="5213f-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="5213f-170">具有讀者角色的使用者將必須明確指定 `DefaultStorageAccountKey` 參數。</span><span class="sxs-lookup"><span data-stu-id="5213f-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="5213f-171">如需這些角色型存取權變更的詳細資訊，請參閱 [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="5213f-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="5213f-172">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-173">After</span><span class="sxs-lookup"><span data-stu-id="5213f-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="5213f-174">使用者僅具有 Cmdlet Get-AzHDInsightJobOutput 的讀者角色</span><span class="sxs-lookup"><span data-stu-id="5213f-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="5213f-175">之前</span><span class="sxs-lookup"><span data-stu-id="5213f-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="5213f-176">After</span><span class="sxs-lookup"><span data-stu-id="5213f-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="5213f-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5213f-177">Az.Storage</span></span>

- <span data-ttu-id="5213f-178">從 Blob、佇列和檔案 Cmdlet 傳回的類型已將其命名空間從 `Microsoft.WindowsAzure.Storage` 變更為 `Microsoft.Azure.Storage`。</span><span class="sxs-lookup"><span data-stu-id="5213f-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="5213f-179">雖然根據重大變更原則，這不是技術上的重大變更，但可能需要對使用儲存體 .Net SDK 方法的程式碼進行某些變更，才能與這些 Cmdlet 傳回的物件互動。</span><span class="sxs-lookup"><span data-stu-id="5213f-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="5213f-180">範例 1：將訊息新增至佇列 (變更 CloudQueueMessage 物件命名空間)</span><span class="sxs-lookup"><span data-stu-id="5213f-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="5213f-181">之前：</span><span class="sxs-lookup"><span data-stu-id="5213f-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="5213f-182">之後：</span><span class="sxs-lookup"><span data-stu-id="5213f-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="5213f-183">範例 2：使用 AccessCondition 擷取 Blob/檔案屬性 (變更 AccessCondition 物件命名空間)</span><span class="sxs-lookup"><span data-stu-id="5213f-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="5213f-184">之前：</span><span class="sxs-lookup"><span data-stu-id="5213f-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="5213f-185">之後：</span><span class="sxs-lookup"><span data-stu-id="5213f-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="5213f-186">雖然並非技術上的重大變更，但在 `New/Get/Set-AzStorageAccount` 變更所傳回的儲存體帳戶中，您會發現其 Sku.Name 屬性的輸出有如下的差異。</span><span class="sxs-lookup"><span data-stu-id="5213f-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="5213f-187">(經過變更後，輸出和輸入的 SkuName 會相對應。)</span><span class="sxs-lookup"><span data-stu-id="5213f-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="5213f-188">"StandardLRS" -> "Standard_LRS";</span><span class="sxs-lookup"><span data-stu-id="5213f-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="5213f-189">"StandardGRS" -> "Standard_GRS";</span><span class="sxs-lookup"><span data-stu-id="5213f-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="5213f-190">"StandardRAGRS" -> "Standard_RAGRS";</span><span class="sxs-lookup"><span data-stu-id="5213f-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="5213f-191">"StandardZRS" -> "Standard_ZRS";</span><span class="sxs-lookup"><span data-stu-id="5213f-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="5213f-192">"PremiumLRS" -> "Premium_LRS";</span><span class="sxs-lookup"><span data-stu-id="5213f-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="5213f-193">在建立儲存體帳戶時未指定種類的預設服務行為已變更。</span><span class="sxs-lookup"><span data-stu-id="5213f-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="5213f-194">在舊版中，在建立儲存體帳戶時若未指定 `Kind`，將會使用 `Storage` 種類的儲存體帳戶，而新版本的預設 `Kind` 值則為 `StorageV2`。</span><span class="sxs-lookup"><span data-stu-id="5213f-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="5213f-195">如果您需要建立 'Storage' 種類的 V1 儲存體帳戶，請新增參數 '-Kind Storage'</span><span class="sxs-lookup"><span data-stu-id="5213f-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="5213f-196">範例：建立儲存體帳戶 (預設種類變更)</span><span class="sxs-lookup"><span data-stu-id="5213f-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="5213f-197">之前：</span><span class="sxs-lookup"><span data-stu-id="5213f-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="5213f-198">之後：</span><span class="sxs-lookup"><span data-stu-id="5213f-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
