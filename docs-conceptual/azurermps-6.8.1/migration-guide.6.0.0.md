---
title: Microsoft Azure PowerShell 6.0.0 的重大變更
description: 本移轉指南包含在第 6 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 72a0e9ca8562dc06a1fe2718658172ce9ee20f0e
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383935"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="57b35-103">Microsoft Azure PowerShell 6.0.0 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="57b35-104">本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。</span><span class="sxs-lookup"><span data-stu-id="57b35-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="57b35-105">每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。</span><span class="sxs-lookup"><span data-stu-id="57b35-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="57b35-106">如需深入了解內容，請參閱與每次變更相關聯的提取要求。</span><span class="sxs-lookup"><span data-stu-id="57b35-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="57b35-107">目錄</span><span class="sxs-lookup"><span data-stu-id="57b35-107">Table of Contents</span></span>

- [<span data-ttu-id="57b35-108">一般重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="57b35-109">移至 5.0 所需的最低 PowerShell 版本</span><span class="sxs-lookup"><span data-stu-id="57b35-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="57b35-110">依預設啟用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="57b35-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="57b35-111">移除標記別名</span><span class="sxs-lookup"><span data-stu-id="57b35-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="57b35-112">AzureRM.Compute Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="57b35-113">AzureRM.DataLakeStore Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="57b35-114">AzureRM.Dns Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="57b35-115">AzureRM.Insights Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="57b35-116">AzureRM.KeyVault Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="57b35-117">AzureRM.Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="57b35-118">AzureRM.RedisCache Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="57b35-119">AzureRM.Resources Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="57b35-120">AzureRM.Storage Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="57b35-121">移除的模組</span><span class="sxs-lookup"><span data-stu-id="57b35-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="57b35-122">一般重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="57b35-123">移至 5.0 所需的最低 PowerShell 版本</span><span class="sxs-lookup"><span data-stu-id="57b35-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="57b35-124">以前，Azure PowerShell _至少需要_ PowerShell 版本 3.0，才能執行任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57b35-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="57b35-125">日後，此需求將提升至 PowerShell 版本 5.0。</span><span class="sxs-lookup"><span data-stu-id="57b35-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="57b35-126">如需升級至 PowerShell 5.0 的詳細資訊，請參閱[此表格](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="57b35-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="57b35-127">依預設啟用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="57b35-127">Context autosave enabled by default</span></span>

<span data-ttu-id="57b35-128">內容自動儲存是 Azure 登入資訊的儲存體，可以在全新和不同的 PowerShell 工作階段之間使用。</span><span class="sxs-lookup"><span data-stu-id="57b35-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="57b35-129">如需內容自動儲存的詳細資訊，請參閱[此文件](https://docs.microsoft.com/en-us/powershell/azure/context-persistence)。</span><span class="sxs-lookup"><span data-stu-id="57b35-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="57b35-130">之前，內容自動儲存會依預設停用，這表示在使用者執行 `Enable-AzureRmContextAutosave` Cmdlet 開啟內容持續性之前，系統不會儲存工作階段之間的使用者 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="57b35-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="57b35-131">未來，內容自動儲存將會依預設啟用，這表示若使用者_並未針對已儲存的內容設定自動儲存_，會在他們下次登入時儲存內容。</span><span class="sxs-lookup"><span data-stu-id="57b35-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="57b35-132">使用者可以藉由使用 `Disable-AzureRmContextAutosave` Cmdlet 來選擇退出此功能。</span><span class="sxs-lookup"><span data-stu-id="57b35-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="57b35-133">_注意_：先前已停用內容自動儲存或已啟用內容自動儲存的使用者，以及現有的內容將不會受到此變更影響</span><span class="sxs-lookup"><span data-stu-id="57b35-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="57b35-134">移除標記別名</span><span class="sxs-lookup"><span data-stu-id="57b35-134">Removal of Tags alias</span></span>

<span data-ttu-id="57b35-135">已在多個 Cmdlet 中移除 `Tag` 參數的別名 `Tags`。</span><span class="sxs-lookup"><span data-stu-id="57b35-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="57b35-136">以下是受此影響的模組清單 (以及對應的 Cmdlet)：</span><span class="sxs-lookup"><span data-stu-id="57b35-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="57b35-137">AzureRM.Compute Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="57b35-138">**其他**</span><span class="sxs-lookup"><span data-stu-id="57b35-138">**Miscellaneous**</span></span>
- <span data-ttu-id="57b35-139">在類型 `PSDisk` 和 `PSSnapshot` 中形成巢狀的 SKU 名稱屬性，已分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="57b35-140">在類型 `PSVirtualMachine`、`PSVirtualMachineScaleSet` 和 `PSImage` 中形成巢狀的儲存體帳戶類型，已分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="57b35-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="57b35-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="57b35-142">參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="57b35-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="57b35-144">參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="57b35-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="57b35-146">參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="57b35-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="57b35-148">已移除參數 `Managed` 以支持 `Sku`</span><span class="sxs-lookup"><span data-stu-id="57b35-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="57b35-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="57b35-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="57b35-150">參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="57b35-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="57b35-152">參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="57b35-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="57b35-154">參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="57b35-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="57b35-156">參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="57b35-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="57b35-158">參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="57b35-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="57b35-160">已移除參數 `DisableWAD`</span><span class="sxs-lookup"><span data-stu-id="57b35-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="57b35-161">Windows Azure 診斷預設為停用</span><span class="sxs-lookup"><span data-stu-id="57b35-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="57b35-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="57b35-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="57b35-163">參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="57b35-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="57b35-165">參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="57b35-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="57b35-167">參數 `ManagedDisk` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="57b35-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="57b35-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="57b35-169">參數 `ManagedDiskStorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="57b35-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="57b35-170">AzureRM.DataLakeStore Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="57b35-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="57b35-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="57b35-172">已移除參數 `PerFileThreadCount` 和 `ConcurrentFileCount`。</span><span class="sxs-lookup"><span data-stu-id="57b35-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="57b35-173">未來請使用 `Concurrency` 參數</span><span class="sxs-lookup"><span data-stu-id="57b35-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="57b35-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="57b35-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="57b35-175">已移除參數 `PerFileThreadCount` 和 `ConcurrentFileCount`。</span><span class="sxs-lookup"><span data-stu-id="57b35-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="57b35-176">未來請使用 `Concurrency` 參數</span><span class="sxs-lookup"><span data-stu-id="57b35-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="57b35-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="57b35-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="57b35-178">已移除參數 `Clean`</span><span class="sxs-lookup"><span data-stu-id="57b35-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="57b35-179">AzureRM.Dns Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="57b35-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="57b35-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="57b35-181">已移除參數 `Force`</span><span class="sxs-lookup"><span data-stu-id="57b35-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="57b35-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="57b35-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="57b35-183">已移除參數 `Force`</span><span class="sxs-lookup"><span data-stu-id="57b35-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="57b35-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="57b35-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="57b35-185">已移除參數 `Force`</span><span class="sxs-lookup"><span data-stu-id="57b35-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="57b35-186">AzureRM.Insights Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="57b35-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="57b35-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="57b35-188">已移除參數別名 `AutoscaleProfiles` 和 `Notifications`</span><span class="sxs-lookup"><span data-stu-id="57b35-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="57b35-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="57b35-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="57b35-190">已移除參數別名 `Categories` 和 `Locations`</span><span class="sxs-lookup"><span data-stu-id="57b35-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="57b35-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="57b35-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="57b35-192">已移除參數別名 `Actions`</span><span class="sxs-lookup"><span data-stu-id="57b35-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="57b35-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="57b35-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="57b35-194">已移除參數別名 `Actions`</span><span class="sxs-lookup"><span data-stu-id="57b35-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="57b35-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="57b35-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="57b35-196">已移除參數別名 `MaxRecords` 和 `MaxEvents`</span><span class="sxs-lookup"><span data-stu-id="57b35-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="57b35-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="57b35-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="57b35-198">已移除參數別名 `MetricNames`</span><span class="sxs-lookup"><span data-stu-id="57b35-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="57b35-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="57b35-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="57b35-200">已移除參數別名 `CustomEmails` 和 `SendToServiceOwners`</span><span class="sxs-lookup"><span data-stu-id="57b35-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="57b35-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="57b35-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="57b35-202">已移除參數別名 `Properties`</span><span class="sxs-lookup"><span data-stu-id="57b35-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="57b35-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="57b35-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="57b35-204">已移除參數別名 `CustomEmails`、`SendEmailToSubscriptionCoAdministrators` 和 `Webhooks`</span><span class="sxs-lookup"><span data-stu-id="57b35-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="57b35-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="57b35-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="57b35-206">已移除參數別名 `Rules`、`ScheduleDays`、`ScheduleHours` 和 `ScheduleMinutes`</span><span class="sxs-lookup"><span data-stu-id="57b35-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="57b35-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="57b35-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="57b35-208">已移除參數別名 `Properties`</span><span class="sxs-lookup"><span data-stu-id="57b35-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="57b35-209">AzureRM.KeyVault Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="57b35-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="57b35-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="57b35-211">`CertificatePolicy` 參數已變成強制參數。</span><span class="sxs-lookup"><span data-stu-id="57b35-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="57b35-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="57b35-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="57b35-213">此 Cmdlet 不再接受組成存取權杖的個別參數；相反地，Cmdlet 會取代明確的存取權杖參數，例如 `Service` 或 `Permissions`，並使用泛型 `TemplateUri` 參數，對應至在其他位置定義的範例存取權杖 (假定使用的是儲存體 PowerShell Cmdlet，或是依據儲存體文件手動組成。)此 Cmdlet 會保留 `ValidityPeriod` 參數。</span><span class="sxs-lookup"><span data-stu-id="57b35-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="57b35-214">如需撰寫 Azure 儲存體共用存取權杖的詳細資訊，請分別參閱以下文件頁面：</span><span class="sxs-lookup"><span data-stu-id="57b35-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="57b35-215">[建構服務 SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="57b35-215">[Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="57b35-216">[建構帳戶 SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="57b35-216">[Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="57b35-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="57b35-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="57b35-218">`IssuerProvider` 參數已變成強制參數。</span><span class="sxs-lookup"><span data-stu-id="57b35-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="57b35-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="57b35-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="57b35-220">此 Cmdlet 的輸出已從 `CertificateBundle` 變更為 `PSKeyVaultCertificate`。</span><span class="sxs-lookup"><span data-stu-id="57b35-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="57b35-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="57b35-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="57b35-222">已從 `InputObject` 參數集移除 `ResourceGroupName`，並改為從 `InputObject` 參數的 `ResourceId` 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="57b35-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="57b35-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="57b35-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="57b35-224">已從 `PermissionsToKeys`、`PermissionsToSecrets` 和 `PermissionsToCertificates` 中移除 `all` 權限。</span><span class="sxs-lookup"><span data-stu-id="57b35-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="57b35-225">**一般**</span><span class="sxs-lookup"><span data-stu-id="57b35-225">**General**</span></span>
- <span data-ttu-id="57b35-226">已從已啟用 `InputObject` 管線的所有 Cmdlet 中移除 `ValueFromPipelineByPropertyName` 屬性。</span><span class="sxs-lookup"><span data-stu-id="57b35-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="57b35-227">受影響的 Cmdlet 為：</span><span class="sxs-lookup"><span data-stu-id="57b35-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="57b35-228">已從所有 Cmdlet 中移除 `ConfirmImpact` 層級。</span><span class="sxs-lookup"><span data-stu-id="57b35-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="57b35-229">受影響的 Cmdlet 為：</span><span class="sxs-lookup"><span data-stu-id="57b35-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="57b35-230">`IKeyVaultDataServiceClient` 已更新，使得所有憑證作業會傳回 PSTypes 而不是 SDK 類型。</span><span class="sxs-lookup"><span data-stu-id="57b35-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="57b35-231">其中包括：</span><span class="sxs-lookup"><span data-stu-id="57b35-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="57b35-232">AzureRM.Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="57b35-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="57b35-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="57b35-234">已移除參數 `ProbeEnabled`</span><span class="sxs-lookup"><span data-stu-id="57b35-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="57b35-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="57b35-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="57b35-236">已移除參數別名 `AlloowGatewayTransit`</span><span class="sxs-lookup"><span data-stu-id="57b35-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="57b35-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="57b35-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="57b35-238">已移除參數 `ProbeEnabled`</span><span class="sxs-lookup"><span data-stu-id="57b35-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="57b35-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="57b35-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="57b35-240">已移除參數 `ProbeEnabled`</span><span class="sxs-lookup"><span data-stu-id="57b35-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="57b35-241">AzureRM.RedisCache Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="57b35-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="57b35-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="57b35-243">已移除參數 `Subnet` 和 `VirtualNetwork` 以支持 `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="57b35-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="57b35-244">已移除參數 `RedisVersion`</span><span class="sxs-lookup"><span data-stu-id="57b35-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="57b35-245">已移除參數 `MaxMemoryPolicy` 以支持 `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="57b35-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="57b35-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="57b35-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="57b35-247">已移除參數 `MaxMemoryPolicy` 以支持 `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="57b35-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="57b35-248">AzureRM.Resources Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="57b35-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="57b35-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="57b35-250">已移除此 Cmdlet，並將功能移至 `Get-AzureRmResource`</span><span class="sxs-lookup"><span data-stu-id="57b35-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="57b35-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="57b35-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="57b35-252">已移除此 Cmdlet，並將功能移至 `Get-AzureRmResourceGroup`</span><span class="sxs-lookup"><span data-stu-id="57b35-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="57b35-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="57b35-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="57b35-254">已移除參數 `AtScopeAndBelow`。</span><span class="sxs-lookup"><span data-stu-id="57b35-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="57b35-255">AzureRM.Storage Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="57b35-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="57b35-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="57b35-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="57b35-257">已移除參數 `EnableEncryptionService`</span><span class="sxs-lookup"><span data-stu-id="57b35-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="57b35-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="57b35-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="57b35-259">已移除參數 `EnableEncryptionService` 和 `DisableEncryptionService`</span><span class="sxs-lookup"><span data-stu-id="57b35-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="57b35-260">移除的模組</span><span class="sxs-lookup"><span data-stu-id="57b35-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="57b35-261">伺服器管理工具服務已在[去年淘汰](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)；因此，SMT 的對應模組 `AzureRM.ServerManagement`已從 `AzureRM` 移除，並將在日後停止傳送。</span><span class="sxs-lookup"><span data-stu-id="57b35-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="57b35-262">已由 `AzureRM.RecoveryServices.SiteRecovery` 取代的 `AzureRM.SiteRecovery` 模組，是 `AzureRM.SiteRecovery` 模組的功能超集，並包含一組新的對等 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57b35-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="57b35-263">您可以在下方找到從舊到新 Cmdlet 對應的完整清單：</span><span class="sxs-lookup"><span data-stu-id="57b35-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="57b35-264">已取代的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57b35-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="57b35-265">對等的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57b35-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="57b35-266">別名</span><span class="sxs-lookup"><span data-stu-id="57b35-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
