---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062134"
---
## <a name="300---november-2019"></a><span data-ttu-id="5d538-103">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="5d538-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="5d538-104">一般</span><span class="sxs-lookup"><span data-stu-id="5d538-104">General</span></span>
* <span data-ttu-id="5d538-105">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5d538-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d538-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-106">Az.Accounts</span></span>
* <span data-ttu-id="5d538-107">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="5d538-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5d538-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5d538-108">Az.Advisor</span></span>
* <span data-ttu-id="5d538-109">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="5d538-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d538-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d538-110">Az.Batch</span></span>
* <span data-ttu-id="5d538-111">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="5d538-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="5d538-112">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="5d538-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="5d538-113">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="5d538-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="5d538-114">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="5d538-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="5d538-115">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="5d538-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="5d538-116">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="5d538-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="5d538-117">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="5d538-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="5d538-118">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="5d538-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="5d538-119">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="5d538-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="5d538-120">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d538-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5d538-121">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="5d538-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="5d538-122">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="5d538-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="5d538-123">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="5d538-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5d538-124">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="5d538-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="5d538-125">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d538-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="5d538-126">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="5d538-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="5d538-127">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="5d538-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="5d538-128">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d538-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="5d538-129">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="5d538-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="5d538-130">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="5d538-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="5d538-131">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="5d538-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5d538-132">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="5d538-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5d538-133">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="5d538-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="5d538-134">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="5d538-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="5d538-135">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="5d538-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="5d538-136">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="5d538-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="5d538-137">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5d538-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="5d538-138">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5d538-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="5d538-139">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="5d538-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="5d538-140">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="5d538-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="5d538-141">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="5d538-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="5d538-142">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="5d538-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="5d538-143">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="5d538-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="5d538-144">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="5d538-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="5d538-145">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="5d538-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="5d538-146">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="5d538-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d538-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d538-147">Az.Cdn</span></span>
* <span data-ttu-id="5d538-148">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="5d538-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="5d538-149">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="5d538-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-150">Az.Compute</span></span>
* <span data-ttu-id="5d538-151">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="5d538-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="5d538-152">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5d538-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="5d538-153">DiskEncryptionSetId 參數已新增至下列 Cmdlet：Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5d538-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="5d538-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5d538-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="5d538-155">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5d538-156">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="5d538-157">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="5d538-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="5d538-158">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="5d538-159">重大變更</span><span class="sxs-lookup"><span data-stu-id="5d538-159">Breaking changes</span></span>
    - <span data-ttu-id="5d538-160">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5d538-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="5d538-161">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="5d538-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-162">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-163">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="5d538-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-165">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="5d538-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="5d538-166">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5d538-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="5d538-167">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="5d538-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="5d538-168">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="5d538-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="5d538-169">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="5d538-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="5d538-170">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="5d538-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d538-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d538-171">Az.FrontDoor</span></span>
* <span data-ttu-id="5d538-172">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="5d538-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d538-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d538-173">Az.HDInsight</span></span>
* <span data-ttu-id="5d538-174">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="5d538-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="5d538-175">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="5d538-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="5d538-176">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="5d538-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="5d538-177">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="5d538-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5d538-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5d538-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5d538-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5d538-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5d538-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5d538-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d538-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="5d538-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d538-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="5d538-183">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="5d538-184">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="5d538-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5d538-185">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="5d538-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5d538-186">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="5d538-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="5d538-187">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="5d538-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="5d538-188">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="5d538-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="5d538-189">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="5d538-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="5d538-190">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="5d538-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="5d538-191">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="5d538-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="5d538-192">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="5d538-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="5d538-193">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="5d538-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="5d538-194">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="5d538-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="5d538-195">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="5d538-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-196">Az.IotHub</span></span>
* <span data-ttu-id="5d538-197">重大變更：</span><span class="sxs-lookup"><span data-stu-id="5d538-197">Breaking changes:</span></span>
    - <span data-ttu-id="5d538-198">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="5d538-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d538-199">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="5d538-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5d538-200">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="5d538-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d538-201">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="5d538-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5d538-202">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="5d538-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="5d538-203">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="5d538-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="5d538-204">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="5d538-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="5d538-205">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="5d538-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="5d538-206">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="5d538-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d538-207">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="5d538-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5d538-208">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="5d538-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d538-209">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="5d538-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-211">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="5d538-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-212">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="5d538-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="5d538-213">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="5d538-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="5d538-214">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="5d538-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-215">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="5d538-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-216">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="5d538-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-217">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d538-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-218">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-219">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="5d538-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-220">Az.Resources</span></span>
* <span data-ttu-id="5d538-221">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="5d538-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-222">Az.Network</span></span>
* <span data-ttu-id="5d538-223">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="5d538-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="5d538-224">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d538-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5d538-230">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="5d538-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="5d538-231">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-231">New cmdlet:</span></span>
        - <span data-ttu-id="5d538-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5d538-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="5d538-233">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="5d538-234">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="5d538-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="5d538-235">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="5d538-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="5d538-236">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="5d538-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="5d538-237">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="5d538-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="5d538-238">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="5d538-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="5d538-239">為 VirtualHub 的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="5d538-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="5d538-240">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-240">New cmdlets added:</span></span>
        - <span data-ttu-id="5d538-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="5d538-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="5d538-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d538-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5d538-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d538-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5d538-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d538-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5d538-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5d538-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="5d538-246">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="5d538-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="5d538-247">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="5d538-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d538-248">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="5d538-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5d538-249">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="5d538-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5d538-250">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="5d538-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="5d538-251">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="5d538-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="5d538-252">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="5d538-253">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-253">New cmdlets added:</span></span>
        - <span data-ttu-id="5d538-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="5d538-255">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="5d538-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d538-256">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d538-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d538-257">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d538-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d538-258">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d538-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d538-259">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d538-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d538-260">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d538-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="5d538-261">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="5d538-262">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-262">New cmdlets added:</span></span>
        - <span data-ttu-id="5d538-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="5d538-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="5d538-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="5d538-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="5d538-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="5d538-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="5d538-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="5d538-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="5d538-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="5d538-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="5d538-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="5d538-269">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="5d538-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d538-270">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5d538-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="5d538-271">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="5d538-272">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="5d538-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="5d538-273">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="5d538-274">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="5d538-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d538-275">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5d538-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="5d538-276">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5d538-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="5d538-277">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="5d538-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="5d538-278">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="5d538-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="5d538-279">為 IpGroup 的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="5d538-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="5d538-280">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-280">New cmdlets added:</span></span>
        - <span data-ttu-id="5d538-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="5d538-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="5d538-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="5d538-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-286">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="5d538-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-287">Az.Sql</span></span>
* <span data-ttu-id="5d538-288">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="5d538-289">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="5d538-290">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="5d538-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="5d538-291">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="5d538-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="5d538-292">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="5d538-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="5d538-293">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5d538-294">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="5d538-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="5d538-295">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="5d538-296">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="5d538-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-297">Az.Storage</span></span>
* <span data-ttu-id="5d538-298">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="5d538-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="5d538-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5d538-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5d538-301">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="5d538-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="5d538-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d538-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="5d538-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d538-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="5d538-304">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="5d538-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="5d538-305">一般</span><span class="sxs-lookup"><span data-stu-id="5d538-305">General</span></span>
* <span data-ttu-id="5d538-306">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="5d538-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d538-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-307">Az.Accounts</span></span>
* <span data-ttu-id="5d538-308">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="5d538-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d538-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-309">Az.ApiManagement</span></span>
* <span data-ttu-id="5d538-310">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="5d538-311">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-312">Az.Automation</span></span>
* <span data-ttu-id="5d538-313">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="5d538-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d538-314">Az.Batch</span></span>
* <span data-ttu-id="5d538-315">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="5d538-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-316">Az.Compute</span></span>
* <span data-ttu-id="5d538-317">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="5d538-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5d538-318">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="5d538-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="5d538-319">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="5d538-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="5d538-320">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="5d538-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-321">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-322">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="5d538-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="5d538-323">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="5d538-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="5d538-324">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="5d538-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-326">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="5d538-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5d538-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5d538-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="5d538-328">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5d538-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="5d538-329">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="5d538-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="5d538-330">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="5d538-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="5d538-331">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="5d538-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-332">Az.IotHub</span></span>
* <span data-ttu-id="5d538-333">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="5d538-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="5d538-334">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d538-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="5d538-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-335">Az.Monitor</span></span>
* <span data-ttu-id="5d538-336">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5d538-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="5d538-337">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="5d538-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="5d538-338">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="5d538-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="5d538-339">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5d538-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-340">Az.Network</span></span>
* <span data-ttu-id="5d538-341">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="5d538-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="5d538-342">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="5d538-343">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-343">New cmdlets added:</span></span>
        - <span data-ttu-id="5d538-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="5d538-345">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5d538-346">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="5d538-347">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="5d538-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d538-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d538-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5d538-351">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="5d538-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="5d538-352">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="5d538-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="5d538-353">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="5d538-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="5d538-354">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="5d538-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d538-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d538-355">Az.RedisCache</span></span>
* <span data-ttu-id="5d538-356">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="5d538-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-357">Az.Sql</span></span>
* <span data-ttu-id="5d538-358">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-359">Az.Storage</span></span>
* <span data-ttu-id="5d538-360">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="5d538-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="5d538-361">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="5d538-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5d538-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5d538-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="5d538-363">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="5d538-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5d538-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d538-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d538-365">Az.StorageSync</span></span>
* <span data-ttu-id="5d538-366">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="5d538-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-367">Az.Websites</span></span>
* <span data-ttu-id="5d538-368">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="5d538-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="5d538-369">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="5d538-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5d538-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-370">Az.ApiManagement</span></span>
* <span data-ttu-id="5d538-371">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="5d538-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="5d538-372">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="5d538-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="5d538-373">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="5d538-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-374">Az.Automation</span></span>
* <span data-ttu-id="5d538-375">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="5d538-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="5d538-376">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="5d538-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="5d538-377">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5d538-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-378">Az.Compute</span></span>
* <span data-ttu-id="5d538-379">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="5d538-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="5d538-380">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="5d538-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5d538-381">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="5d538-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="5d538-382">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="5d538-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="5d538-383">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="5d538-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="5d538-384">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="5d538-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="5d538-385">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5d538-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="5d538-386">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="5d538-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="5d538-387">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-388">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-389">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5d538-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="5d538-390">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="5d538-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d538-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d538-391">Az.HDInsight</span></span>
* <span data-ttu-id="5d538-392">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="5d538-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-393">Az.IotHub</span></span>
* <span data-ttu-id="5d538-394">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="5d538-395">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="5d538-396">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="5d538-396">New cmdlets are:</span></span>
    - <span data-ttu-id="5d538-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d538-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5d538-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d538-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5d538-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d538-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5d538-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d538-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d538-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-401">Az.Monitor</span></span>
* <span data-ttu-id="5d538-402">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="5d538-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="5d538-403">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="5d538-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="5d538-404">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="5d538-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="5d538-405">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="5d538-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="5d538-406">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="5d538-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="5d538-407">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="5d538-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="5d538-408">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="5d538-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="5d538-409">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="5d538-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="5d538-410">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="5d538-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5d538-411">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="5d538-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="5d538-412">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="5d538-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5d538-413">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="5d538-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="5d538-414">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="5d538-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="5d538-415">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="5d538-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="5d538-416">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="5d538-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="5d538-417">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="5d538-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="5d538-418">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="5d538-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="5d538-419">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="5d538-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="5d538-420">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="5d538-421">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="5d538-421">Overall improved help files</span></span>
* <span data-ttu-id="5d538-422">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="5d538-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-423">Az.Network</span></span>
* <span data-ttu-id="5d538-424">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="5d538-425">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5d538-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="5d538-426">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="5d538-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="5d538-427">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="5d538-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="5d538-428">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="5d538-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="5d538-429">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="5d538-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="5d538-430">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="5d538-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="5d538-431">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="5d538-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="5d538-432">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="5d538-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="5d538-433">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="5d538-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="5d538-434">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="5d538-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="5d538-435">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="5d538-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="5d538-436">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-436">New cmdlets</span></span>
        - <span data-ttu-id="5d538-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5d538-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="5d538-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="5d538-439">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d538-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5d538-440">New-VpnSite</span></span>
        - <span data-ttu-id="5d538-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5d538-441">Update-VpnSite</span></span>
        - <span data-ttu-id="5d538-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-442">New-VpnConnection</span></span>
        - <span data-ttu-id="5d538-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-443">Update-VpnConnection</span></span>
* <span data-ttu-id="5d538-444">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-446">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="5d538-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="5d538-447">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="5d538-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-448">Az.Resources</span></span>
* <span data-ttu-id="5d538-449">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="5d538-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-451">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="5d538-452">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="5d538-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="5d538-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d538-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d538-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5d538-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5d538-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5d538-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5d538-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5d538-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="5d538-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d538-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d538-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d538-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d538-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5d538-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5d538-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5d538-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5d538-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5d538-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="5d538-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d538-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d538-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5d538-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5d538-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5d538-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5d538-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="5d538-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="5d538-466">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="5d538-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5d538-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5d538-467">Az.SignalR</span></span>
* <span data-ttu-id="5d538-468">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-469">Az.Sql</span></span>
* <span data-ttu-id="5d538-470">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="5d538-471">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="5d538-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="5d538-472">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="5d538-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="5d538-473">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="5d538-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="5d538-474">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="5d538-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-475">Az.Storage</span></span>
* <span data-ttu-id="5d538-476">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5d538-477">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="5d538-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="5d538-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d538-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="5d538-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d538-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="5d538-480">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="5d538-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d538-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="5d538-482">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="5d538-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="5d538-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d538-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5d538-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d538-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5d538-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d538-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5d538-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d538-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-487">Az.Websites</span></span>
* <span data-ttu-id="5d538-488">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="5d538-489">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="5d538-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="5d538-490">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="5d538-491">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="5d538-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="5d538-492">一般</span><span class="sxs-lookup"><span data-stu-id="5d538-492">General</span></span>
* <span data-ttu-id="5d538-493">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="5d538-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d538-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-494">Az.Accounts</span></span>
* <span data-ttu-id="5d538-495">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="5d538-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5d538-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5d538-496">Az.Aks</span></span>
* <span data-ttu-id="5d538-497">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="5d538-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="5d538-498">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="5d538-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d538-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-499">Az.ApiManagement</span></span>
* <span data-ttu-id="5d538-500">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="5d538-501">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="5d538-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="5d538-502">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="5d538-503">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="5d538-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="5d538-504">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5d538-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d538-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d538-505">Az.Batch</span></span>
* <span data-ttu-id="5d538-506">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="5d538-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d538-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d538-507">Az.Cdn</span></span>
* <span data-ttu-id="5d538-508">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-509">Az.Compute</span></span>
* <span data-ttu-id="5d538-510">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="5d538-511">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="5d538-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="5d538-512">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="5d538-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="5d538-513">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="5d538-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="5d538-514">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5d538-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="5d538-515">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="5d538-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="5d538-516">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="5d538-517">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="5d538-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-518">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-519">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="5d538-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="5d538-520">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="5d538-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="5d538-521">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="5d538-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="5d538-522">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="5d538-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-524">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5d538-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d538-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d538-525">Az.EventHub</span></span>
* <span data-ttu-id="5d538-526">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="5d538-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="5d538-527">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="5d538-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="5d538-528">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="5d538-529">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="5d538-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="5d538-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5d538-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5d538-531">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="5d538-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d538-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-532">Az.Monitor</span></span>
* <span data-ttu-id="5d538-533">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-534">Az.Network</span></span>
* <span data-ttu-id="5d538-535">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="5d538-536">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="5d538-537">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="5d538-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="5d538-538">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="5d538-539">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="5d538-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="5d538-540">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="5d538-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="5d538-541">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="5d538-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d538-543">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="5d538-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="5d538-544">新增了範例</span><span class="sxs-lookup"><span data-stu-id="5d538-544">Added example</span></span>
    - <span data-ttu-id="5d538-545">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="5d538-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="5d538-546">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="5d538-547">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="5d538-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-549">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-550">Az.Resources</span></span>
* <span data-ttu-id="5d538-551">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="5d538-552">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="5d538-553">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="5d538-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="5d538-554">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="5d538-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d538-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d538-555">Az.ServiceBus</span></span>
* <span data-ttu-id="5d538-556">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="5d538-557">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="5d538-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="5d538-558">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="5d538-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-560">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="5d538-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="5d538-561">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="5d538-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="5d538-562">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="5d538-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="5d538-563">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="5d538-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="5d538-564">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="5d538-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="5d538-565">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-566">Az.Sql</span></span>
* <span data-ttu-id="5d538-567">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="5d538-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-568">Az.Storage</span></span>
* <span data-ttu-id="5d538-569">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="5d538-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="5d538-570">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="5d538-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="5d538-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d538-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="5d538-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5d538-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="5d538-573">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="5d538-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="5d538-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5d538-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-575">Az.Websites</span></span>
* <span data-ttu-id="5d538-576">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="5d538-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="5d538-577">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="5d538-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-578">Az.Accounts</span></span>
* <span data-ttu-id="5d538-579">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5d538-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5d538-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5d538-581">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="5d538-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-582">Az.Automation</span></span>
* <span data-ttu-id="5d538-583">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d538-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d538-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d538-585">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-586">Az.Compute</span></span>
* <span data-ttu-id="5d538-587">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="5d538-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5d538-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5d538-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5d538-589">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="5d538-590">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="5d538-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-591">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-592">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5d538-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="5d538-593">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d538-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d538-594">Az.EventHub</span></span>
* <span data-ttu-id="5d538-595">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5d538-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5d538-596">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="5d538-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d538-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d538-597">Az.KeyVault</span></span>
* <span data-ttu-id="5d538-598">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d538-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d538-599">Az.LogicApp</span></span>
* <span data-ttu-id="5d538-600">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="5d538-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="5d538-601">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="5d538-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5d538-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5d538-602">Az.ManagedServices</span></span>
* <span data-ttu-id="5d538-603">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-604">Az.Network</span></span>
* <span data-ttu-id="5d538-605">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="5d538-606">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-606">New cmdlets</span></span>
        - <span data-ttu-id="5d538-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d538-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d538-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d538-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d538-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d538-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5d538-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="5d538-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d538-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="5d538-615">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="5d538-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="5d538-616">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="5d538-617">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="5d538-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="5d538-618">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="5d538-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="5d538-619">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="5d538-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="5d538-620">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="5d538-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="5d538-621">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-621">Updated cmdlets</span></span>
        - <span data-ttu-id="5d538-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d538-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d538-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5d538-625">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="5d538-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5d538-626">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5d538-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="5d538-627">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d538-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5d538-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5d538-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="5d538-631">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="5d538-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="5d538-632">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="5d538-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="5d538-633">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="5d538-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d538-635">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="5d538-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="5d538-636">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="5d538-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-638">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5d538-639">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="5d538-640">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="5d538-641">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5d538-642">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="5d538-643">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5d538-644">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="5d538-645">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5d538-646">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="5d538-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="5d538-647">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="5d538-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-648">Az.Resources</span></span>
- <span data-ttu-id="5d538-649">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="5d538-650">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5d538-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d538-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d538-651">Az.ServiceBus</span></span>
* <span data-ttu-id="5d538-652">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5d538-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5d538-653">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="5d538-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-654">Az.Sql</span></span>
* <span data-ttu-id="5d538-655">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="5d538-656">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="5d538-657">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="5d538-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-658">Az.Storage</span></span>
* <span data-ttu-id="5d538-659">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d538-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d538-660">Az.StorageSync</span></span>
* <span data-ttu-id="5d538-661">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="5d538-662">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="5d538-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-663">Az.Websites</span></span>
* <span data-ttu-id="5d538-664">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="5d538-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="5d538-665">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="5d538-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="5d538-666">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="5d538-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="5d538-667">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="5d538-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-668">Az.Accounts</span></span>
* <span data-ttu-id="5d538-669">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="5d538-670">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="5d538-671">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5d538-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5d538-672">Az.Advisor</span></span>
* <span data-ttu-id="5d538-673">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="5d538-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="5d538-674">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="5d538-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d538-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-675">Az.ApiManagement</span></span>
* <span data-ttu-id="5d538-676">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="5d538-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5d538-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="5d538-678">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="5d538-679">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="5d538-680">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="5d538-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5d538-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="5d538-682">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-683">Az.Automation</span></span>
* <span data-ttu-id="5d538-684">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="5d538-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-685">Az.Compute</span></span>
* <span data-ttu-id="5d538-686">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-687">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-688">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="5d538-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d538-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d538-689">Az.EventGrid</span></span>
* <span data-ttu-id="5d538-690">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-691">Az.IotHub</span></span>
* <span data-ttu-id="5d538-692">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-693">Az.Network</span></span>
* <span data-ttu-id="5d538-694">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="5d538-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="5d538-695">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d538-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d538-697">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="5d538-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="5d538-698">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="5d538-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d538-700">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="5d538-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-702">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="5d538-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-703">Az.Resources</span></span>
    - <span data-ttu-id="5d538-704">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="5d538-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="5d538-705">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="5d538-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="5d538-706">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="5d538-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="5d538-707">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="5d538-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d538-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d538-708">Az.ServiceBus</span></span>
* <span data-ttu-id="5d538-709">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="5d538-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-710">Az.Sql</span></span>
* <span data-ttu-id="5d538-711">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="5d538-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="5d538-712">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="5d538-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="5d538-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5d538-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5d538-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5d538-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5d538-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5d538-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5d538-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5d538-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5d538-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5d538-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5d538-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5d538-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="5d538-719">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="5d538-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-720">Az.Storage</span></span>
* <span data-ttu-id="5d538-721">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="5d538-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="5d538-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5d538-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="5d538-723">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="5d538-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="5d538-724">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="5d538-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="5d538-725">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="5d538-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="5d538-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5d538-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5d538-728">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="5d538-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="5d538-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d538-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="5d538-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d538-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d538-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d538-731">Az.StorageSync</span></span>
* <span data-ttu-id="5d538-732">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="5d538-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="5d538-733">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="5d538-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-734">Az.Accounts</span></span>
* <span data-ttu-id="5d538-735">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="5d538-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="5d538-736">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="5d538-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="5d538-737">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="5d538-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="5d538-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5d538-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="5d538-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5d538-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-740">Az.Compute</span></span>
* <span data-ttu-id="5d538-741">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="5d538-742">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="5d538-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5d538-743">Az.Dns</span></span>
* <span data-ttu-id="5d538-744">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="5d538-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d538-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d538-745">Az.EventGrid</span></span>
* <span data-ttu-id="5d538-746">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5d538-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="5d538-747">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-747">New cmdlets:</span></span>
    - <span data-ttu-id="5d538-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5d538-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5d538-749">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="5d538-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5d538-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5d538-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5d538-751">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="5d538-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="5d538-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5d538-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5d538-753">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="5d538-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5d538-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5d538-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5d538-755">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="5d538-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5d538-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5d538-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5d538-757">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="5d538-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="5d538-758">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="5d538-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5d538-759">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="5d538-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="5d538-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5d538-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="5d538-761">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="5d538-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="5d538-762">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="5d538-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5d538-763">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="5d538-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="5d538-764">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="5d538-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="5d538-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="5d538-766">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d538-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5d538-767">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d538-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5d538-768">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="5d538-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="5d538-769">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="5d538-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="5d538-770">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="5d538-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="5d538-771">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="5d538-772">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="5d538-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="5d538-773">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="5d538-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="5d538-774">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="5d538-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="5d538-775">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="5d538-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="5d538-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5d538-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="5d538-777">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d538-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="5d538-778">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d538-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d538-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d538-779">Az.FrontDoor</span></span>
* <span data-ttu-id="5d538-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5d538-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="5d538-781">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="5d538-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="5d538-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="5d538-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="5d538-783">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="5d538-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-784">Az.Network</span></span>
* <span data-ttu-id="5d538-785">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="5d538-786">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-786">New cmdlets</span></span>
        - <span data-ttu-id="5d538-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5d538-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="5d538-788">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5d538-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="5d538-789">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-789">New cmdlets</span></span> 
        - <span data-ttu-id="5d538-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5d538-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="5d538-791">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d538-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="5d538-792">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-792">New cmdlets</span></span> 
        - <span data-ttu-id="5d538-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d538-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="5d538-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d538-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d538-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d538-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d538-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="5d538-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5d538-798">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d538-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="5d538-799">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-799">New cmdlets</span></span>
        - <span data-ttu-id="5d538-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d538-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d538-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d538-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d538-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d538-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d538-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5d538-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="5d538-804">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="5d538-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="5d538-805">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="5d538-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="5d538-806">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="5d538-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="5d538-807">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="5d538-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="5d538-808">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="5d538-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="5d538-809">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="5d538-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="5d538-810">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="5d538-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="5d538-811">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="5d538-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="5d538-812">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="5d538-813">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="5d538-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="5d538-814">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="5d538-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="5d538-815">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="5d538-816">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5d538-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="5d538-817">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="5d538-818">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5d538-819">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="5d538-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="5d538-820">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="5d538-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="5d538-821">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="5d538-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="5d538-822">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="5d538-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="5d538-823">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="5d538-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="5d538-824">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="5d538-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5d538-825">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="5d538-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5d538-826">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="5d538-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d538-828">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="5d538-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-829">Az.Resources</span></span>
* <span data-ttu-id="5d538-830">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="5d538-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="5d538-831">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5d538-832">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5d538-833">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="5d538-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-835">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-836">Az.Sql</span></span>
* <span data-ttu-id="5d538-837">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="5d538-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="5d538-838">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="5d538-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="5d538-839">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="5d538-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="5d538-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d538-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5d538-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d538-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5d538-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d538-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5d538-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5d538-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="5d538-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5d538-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-845">Az.Storage</span></span>
* <span data-ttu-id="5d538-846">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="5d538-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="5d538-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="5d538-848">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="5d538-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="5d538-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-850">Az.Websites</span></span>
* <span data-ttu-id="5d538-851">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="5d538-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="5d538-852">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5d538-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="5d538-853">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="5d538-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="5d538-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d538-854">Az.Cdn</span></span>
* <span data-ttu-id="5d538-855">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="5d538-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-856">Az.Compute</span></span>
* <span data-ttu-id="5d538-857">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="5d538-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="5d538-858">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5d538-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d538-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d538-859">Az.EventHub</span></span>
* <span data-ttu-id="5d538-860">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="5d538-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="5d538-861">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d538-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-862">Az.Network</span></span>
* <span data-ttu-id="5d538-863">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="5d538-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="5d538-864">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="5d538-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d538-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d538-866">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="5d538-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-868">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="5d538-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d538-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d538-869">Az.ServiceBus</span></span>
* <span data-ttu-id="5d538-870">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d538-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-872">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="5d538-873">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="5d538-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-874">Az.Sql</span></span>
* <span data-ttu-id="5d538-875">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="5d538-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="5d538-876">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5d538-877">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="5d538-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="5d538-878">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-879">Az.Websites</span></span>
* <span data-ttu-id="5d538-880">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="5d538-881">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="5d538-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5d538-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-882">Az.ApiManagement</span></span>
* <span data-ttu-id="5d538-883">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="5d538-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="5d538-884">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="5d538-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="5d538-885">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="5d538-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="5d538-886">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="5d538-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="5d538-887">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="5d538-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="5d538-888">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="5d538-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="5d538-889">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="5d538-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="5d538-890">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="5d538-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="5d538-891">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="5d538-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="5d538-892">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="5d538-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="5d538-893">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="5d538-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="5d538-894">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="5d538-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="5d538-895">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="5d538-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="5d538-896">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="5d538-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="5d538-897">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="5d538-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="5d538-898">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="5d538-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="5d538-899">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="5d538-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="5d538-900">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="5d538-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="5d538-901">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="5d538-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="5d538-902">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="5d538-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="5d538-903">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="5d538-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="5d538-904">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="5d538-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="5d538-905">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="5d538-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="5d538-906">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="5d538-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="5d538-907">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="5d538-908">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="5d538-909">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="5d538-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="5d538-910">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="5d538-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="5d538-911">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="5d538-912">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="5d538-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="5d538-913">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="5d538-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="5d538-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="5d538-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="5d538-915">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="5d538-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="5d538-916">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5d538-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5d538-917">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="5d538-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="5d538-918">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d538-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="5d538-919">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d538-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="5d538-920">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="5d538-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="5d538-921">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="5d538-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="5d538-922">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5d538-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="5d538-923">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="5d538-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5d538-924">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="5d538-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5d538-925">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="5d538-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="5d538-926">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="5d538-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5d538-927">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5d538-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5d538-928">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="5d538-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5d538-929">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="5d538-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="5d538-930">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="5d538-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5d538-931">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="5d538-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="5d538-932">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="5d538-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="5d538-933">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="5d538-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="5d538-934">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="5d538-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="5d538-935">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="5d538-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="5d538-936">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="5d538-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="5d538-937">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="5d538-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="5d538-938">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="5d538-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="5d538-939">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5d538-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5d538-940">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="5d538-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5d538-941">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="5d538-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5d538-942">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5d538-943">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5d538-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5d538-944">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="5d538-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5d538-945">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="5d538-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5d538-946">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5d538-947">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="5d538-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="5d538-948">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="5d538-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="5d538-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="5d538-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="5d538-950">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="5d538-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="5d538-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="5d538-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="5d538-952">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5d538-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="5d538-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="5d538-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="5d538-954">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5d538-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="5d538-955">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="5d538-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="5d538-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="5d538-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="5d538-957">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="5d538-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="5d538-958">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5d538-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="5d538-959">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="5d538-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-960">Az.Automation</span></span>
* <span data-ttu-id="5d538-961">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="5d538-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="5d538-962">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="5d538-963">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="5d538-964">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="5d538-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="5d538-965">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="5d538-966">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="5d538-967">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="5d538-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-968">Az.Compute</span></span>
* <span data-ttu-id="5d538-969">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="5d538-970">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="5d538-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-972">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="5d538-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d538-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-973">Az.Monitor</span></span>
* <span data-ttu-id="5d538-974">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-975">Az.Network</span></span>
* <span data-ttu-id="5d538-976">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="5d538-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="5d538-977">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d538-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d538-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="5d538-979">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="5d538-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-980">Az.Resources</span></span>
* <span data-ttu-id="5d538-981">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="5d538-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-982">Az.Sql</span></span>
* <span data-ttu-id="5d538-983">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="5d538-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="5d538-984">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="5d538-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-985">Az.Accounts</span></span>
* <span data-ttu-id="5d538-986">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="5d538-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d538-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d538-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d538-988">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="5d538-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="5d538-989">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d538-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-990">Az.Compute</span></span>
* <span data-ttu-id="5d538-991">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="5d538-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="5d538-992">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="5d538-993">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="5d538-994">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="5d538-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="5d538-995">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="5d538-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="5d538-996">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5d538-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="5d538-997">重大變更</span><span class="sxs-lookup"><span data-stu-id="5d538-997">Breaking changes</span></span>
    - <span data-ttu-id="5d538-998">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="5d538-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="5d538-999">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="5d538-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5d538-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5d538-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="5d538-1001">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="5d538-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5d538-1002">Az.Dns</span></span>
* <span data-ttu-id="5d538-1003">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="5d538-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="5d538-1004">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="5d538-1005">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="5d538-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d538-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d538-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="5d538-1007">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="5d538-1008">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="5d538-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="5d538-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d538-1009">Az.HDInsight</span></span>
* <span data-ttu-id="5d538-1010">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="5d538-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d538-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="5d538-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d538-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5d538-1013">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d538-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5d538-1014">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="5d538-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="5d538-1015">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d538-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="5d538-1016">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="5d538-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d538-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-1017">Az.Monitor</span></span>
* <span data-ttu-id="5d538-1018">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="5d538-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="5d538-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5d538-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="5d538-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5d538-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="5d538-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5d538-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="5d538-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5d538-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="5d538-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5d538-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="5d538-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5d538-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="5d538-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d538-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d538-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d538-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d538-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d538-1030">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5d538-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="5d538-1031">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1032">Az.Network</span></span>
* <span data-ttu-id="5d538-1033">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="5d538-1034">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1034">New cmdlets</span></span>
        - <span data-ttu-id="5d538-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d538-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="5d538-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d538-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="5d538-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d538-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="5d538-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d538-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="5d538-1039">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="5d538-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5d538-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="5d538-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5d538-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="5d538-1042">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="5d538-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="5d538-1043">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="5d538-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="5d538-1044">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="5d538-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d538-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d538-1046">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5d538-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="5d538-1047">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="5d538-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="5d538-1048">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="5d538-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-1050">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="5d538-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="5d538-1051">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="5d538-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="5d538-1052">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="5d538-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="5d538-1053">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="5d538-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="5d538-1054">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="5d538-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="5d538-1055">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="5d538-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="5d538-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5d538-1056">Az.Relay</span></span>
* <span data-ttu-id="5d538-1057">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d538-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d538-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="5d538-1059">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1060">Az.Storage</span></span>
* <span data-ttu-id="5d538-1061">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="5d538-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="5d538-1062">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="5d538-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="5d538-1063">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="5d538-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="5d538-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="5d538-1065">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="5d538-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="5d538-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="5d538-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="5d538-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1069">Az.Websites</span></span>
* <span data-ttu-id="5d538-1070">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="5d538-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="5d538-1071">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="5d538-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="5d538-1072">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d538-1073">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="5d538-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="5d538-1074">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="5d538-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="5d538-1075">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5d538-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5d538-1076">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5d538-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5d538-1077">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5d538-1078">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="5d538-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d538-1079">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5d538-1080">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d538-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1081">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1082">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="5d538-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d538-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d538-1083">Az.Batch</span></span>
* <span data-ttu-id="5d538-1084">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d538-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d538-1085">Az.Cdn</span></span>
* <span data-ttu-id="5d538-1086">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d538-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d538-1088">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1089">Az.Compute</span></span>
* <span data-ttu-id="5d538-1090">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5d538-1091">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d538-1092">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="5d538-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-1093">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-1094">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="5d538-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-1096">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d538-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d538-1097">Az.EventGrid</span></span>
* <span data-ttu-id="5d538-1098">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d538-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d538-1099">Az.EventHub</span></span>
* <span data-ttu-id="5d538-1100">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="5d538-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d538-1101">Az.HDInsight</span></span>
* <span data-ttu-id="5d538-1102">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-1103">Az.IotHub</span></span>
* <span data-ttu-id="5d538-1104">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d538-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d538-1105">Az.KeyVault</span></span>
* <span data-ttu-id="5d538-1106">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d538-1107">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="5d538-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5d538-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5d538-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="5d538-1109">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5d538-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5d538-1110">Az.Media</span></span>
* <span data-ttu-id="5d538-1111">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d538-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-1112">Az.Monitor</span></span>
  * <span data-ttu-id="5d538-1113">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5d538-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5d538-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5d538-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5d538-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5d538-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5d538-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5d538-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5d538-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5d538-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5d538-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5d538-1119">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="5d538-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1120">Az.Network</span></span>
* <span data-ttu-id="5d538-1121">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d538-1122">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="5d538-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5d538-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5d538-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="5d538-1124">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d538-1126">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5d538-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5d538-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5d538-1128">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-1130">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d538-1131">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="5d538-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5d538-1132">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="5d538-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5d538-1133">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="5d538-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d538-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d538-1134">Az.RedisCache</span></span>
* <span data-ttu-id="5d538-1135">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1136">Az.Resources</span></span>
* <span data-ttu-id="5d538-1137">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="5d538-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1138">Az.Sql</span></span>
* <span data-ttu-id="5d538-1139">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="5d538-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5d538-1140">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d538-1141">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="5d538-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5d538-1142">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="5d538-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5d538-1143">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="5d538-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5d538-1144">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5d538-1145">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="5d538-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1146">Az.Websites</span></span>
* <span data-ttu-id="5d538-1147">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="5d538-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5d538-1148">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d538-1149">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="5d538-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5d538-1150">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d538-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5d538-1151">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d538-1152">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="5d538-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="5d538-1153">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="5d538-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="5d538-1154">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5d538-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5d538-1155">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5d538-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5d538-1156">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5d538-1157">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="5d538-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d538-1158">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5d538-1159">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d538-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1160">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1161">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="5d538-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d538-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d538-1163">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="5d538-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5d538-1164">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="5d538-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-1165">Az.Automation</span></span>
* <span data-ttu-id="5d538-1166">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="5d538-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5d538-1167">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="5d538-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5d538-1168">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="5d538-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1169">Az.Compute</span></span>
* <span data-ttu-id="5d538-1170">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5d538-1171">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="5d538-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="5d538-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="5d538-1173">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="5d538-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-1174">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-1175">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="5d538-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5d538-1176">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1177">Az.Resources</span></span>
* <span data-ttu-id="5d538-1178">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="5d538-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5d538-1179">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="5d538-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5d538-1180">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="5d538-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5d538-1181">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5d538-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5d538-1182">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="5d538-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5d538-1183">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5d538-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1184">Az.Sql</span></span>
* <span data-ttu-id="5d538-1185">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="5d538-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1186">Az.Storage</span></span>
* <span data-ttu-id="5d538-1187">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="5d538-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5d538-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d538-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="5d538-1189">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="5d538-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5d538-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5d538-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5d538-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5d538-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5d538-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5d538-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5d538-1194">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5d538-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d538-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5d538-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d538-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5d538-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d538-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5d538-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d538-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5d538-1199">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d538-1200">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="5d538-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="5d538-1201">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="5d538-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="5d538-1202">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5d538-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5d538-1203">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5d538-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5d538-1204">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5d538-1205">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="5d538-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d538-1206">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5d538-1207">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-1208">Az.Automation</span></span>
* <span data-ttu-id="5d538-1209">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="5d538-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5d538-1210">動態分組</span><span class="sxs-lookup"><span data-stu-id="5d538-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="5d538-1211">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="5d538-1211">Pre-Post script</span></span>
    * <span data-ttu-id="5d538-1212">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="5d538-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1213">Az.Compute</span></span>
* <span data-ttu-id="5d538-1214">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5d538-1215">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="5d538-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d538-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d538-1216">Az.KeyVault</span></span>
* <span data-ttu-id="5d538-1217">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1218">Az.Network</span></span>
* <span data-ttu-id="5d538-1219">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5d538-1220">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="5d538-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-1222">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="5d538-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5d538-1223">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1224">Az.Resources</span></span>
* <span data-ttu-id="5d538-1225">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5d538-1226">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="5d538-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1227">Az.Sql</span></span>
* <span data-ttu-id="5d538-1228">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="5d538-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1229">Az.Storage</span></span>
* <span data-ttu-id="5d538-1230">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="5d538-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5d538-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5d538-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5d538-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5d538-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5d538-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5d538-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5d538-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5d538-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1237">Az.Websites</span></span>
* <span data-ttu-id="5d538-1238">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="5d538-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="5d538-1239">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1240">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1241">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5d538-1242">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-1243">Az.Automation</span></span>
* <span data-ttu-id="5d538-1244">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5d538-1245">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5d538-1246">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="5d538-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d538-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d538-1247">Az.Cdn</span></span>
* <span data-ttu-id="5d538-1248">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1249">Az.Compute</span></span>
* <span data-ttu-id="5d538-1250">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-1251">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-1252">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="5d538-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d538-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d538-1253">Az.LogicApp</span></span>
* <span data-ttu-id="5d538-1254">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="5d538-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1255">Az.Network</span></span>
* <span data-ttu-id="5d538-1256">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-1258">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5d538-1259">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="5d538-1259">SDK Update</span></span>
* <span data-ttu-id="5d538-1260">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="5d538-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5d538-1261">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="5d538-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1262">Az.Resources</span></span>
* <span data-ttu-id="5d538-1263">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5d538-1264">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="5d538-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5d538-1265">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5d538-1266">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="5d538-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5d538-1267">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5d538-1268">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="5d538-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1269">Az.Sql</span></span>
* <span data-ttu-id="5d538-1270">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="5d538-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5d538-1271">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="5d538-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1272">Az.Storage</span></span>
* <span data-ttu-id="5d538-1273">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d538-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5d538-1274">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5d538-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d538-1276">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-1277">Az.Automation</span></span>
* <span data-ttu-id="5d538-1278">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="5d538-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5d538-1279">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5d538-1280">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="5d538-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d538-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d538-1282">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="5d538-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1283">Az.Compute</span></span>
* <span data-ttu-id="5d538-1284">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5d538-1285">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="5d538-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5d538-1286">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5d538-1287">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="5d538-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-1289">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d538-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d538-1290">Az.EventHub</span></span>
* <span data-ttu-id="5d538-1291">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="5d538-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="5d538-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d538-1292">Az.KeyVault</span></span>
* <span data-ttu-id="5d538-1293">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="5d538-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d538-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d538-1294">Az.LogicApp</span></span>
* <span data-ttu-id="5d538-1295">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="5d538-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5d538-1296">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="5d538-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5d538-1297">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5d538-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d538-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5d538-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d538-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5d538-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d538-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5d538-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d538-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5d538-1302">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5d538-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d538-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5d538-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d538-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5d538-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d538-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5d538-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d538-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5d538-1307">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="5d538-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d538-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-1308">Az.Monitor</span></span>
* <span data-ttu-id="5d538-1309">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="5d538-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1310">Az.Network</span></span>
* <span data-ttu-id="5d538-1311">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d538-1313">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5d538-1314">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="5d538-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="5d538-1315">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="5d538-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="5d538-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1316">Az.Resources</span></span>
* <span data-ttu-id="5d538-1317">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5d538-1318">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5d538-1319">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5d538-1320">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="5d538-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1321">Az.Sql</span></span>
* <span data-ttu-id="5d538-1322">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5d538-1323">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="5d538-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1324">Az.Websites</span></span>
* <span data-ttu-id="5d538-1325">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5d538-1326">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1327">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1328">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5d538-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d538-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="5d538-1330">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="5d538-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1331">Az.Compute</span></span>
* <span data-ttu-id="5d538-1332">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5d538-1333">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="5d538-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5d538-1334">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="5d538-1336">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="5d538-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1337">Az.Resources</span></span>
* <span data-ttu-id="5d538-1338">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="5d538-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="5d538-1339">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5d538-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5d538-1340">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="5d538-1341">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5d538-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1342">Az.Sql</span></span>
* <span data-ttu-id="5d538-1343">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d538-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5d538-1344">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5d538-1345">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="5d538-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5d538-1346">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1347">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1348">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="5d538-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d538-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d538-1350">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="5d538-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d538-1352">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="5d538-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5d538-1353">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1354">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1355">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="5d538-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d538-1356">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d538-1357">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="5d538-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5d538-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5d538-1358">Az.Aks</span></span>
* <span data-ttu-id="5d538-1359">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d538-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-1360">Az.Automation</span></span>
* <span data-ttu-id="5d538-1361">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5d538-1362">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d538-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d538-1363">Az.Cdn</span></span>
* <span data-ttu-id="5d538-1364">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1365">Az.Compute</span></span>
* <span data-ttu-id="5d538-1366">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5d538-1367">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5d538-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5d538-1368">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="5d538-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5d538-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5d538-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5d538-1370">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d538-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d538-1371">Az.DataFactory</span></span>
* <span data-ttu-id="5d538-1372">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="5d538-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-1374">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5d538-1375">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="5d538-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5d538-1376">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-1377">Az.IotHub</span></span>
* <span data-ttu-id="5d538-1378">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d538-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d538-1379">Az.KeyVault</span></span>
* <span data-ttu-id="5d538-1380">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1381">Az.Network</span></span>
* <span data-ttu-id="5d538-1382">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1383">Az.Resources</span></span>
* <span data-ttu-id="5d538-1384">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5d538-1385">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5d538-1386">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="5d538-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5d538-1387">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5d538-1388">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5d538-1389">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5d538-1390">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="5d538-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-1392">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="5d538-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5d538-1393">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5d538-1393">Fix some error messages.</span></span>
* <span data-ttu-id="5d538-1394">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5d538-1395">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5d538-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5d538-1396">Az.SignalR</span></span>
* <span data-ttu-id="5d538-1397">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1398">Az.Sql</span></span>
* <span data-ttu-id="5d538-1399">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d538-1400">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="5d538-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5d538-1401">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5d538-1402">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="5d538-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1403">Az.Storage</span></span>
* <span data-ttu-id="5d538-1404">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d538-1405">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="5d538-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5d538-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5d538-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5d538-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5d538-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5d538-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5d538-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="5d538-1409">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1410">Az.Websites</span></span>
* <span data-ttu-id="5d538-1411">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d538-1412">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="5d538-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5d538-1413">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="5d538-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5d538-1414">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d538-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1415">Az.Accounts</span></span>
* <span data-ttu-id="5d538-1416">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5d538-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1417">Az.Compute</span></span>
* <span data-ttu-id="5d538-1418">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="5d538-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5d538-1419">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="5d538-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5d538-1420">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-1422">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5d538-1423">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="5d538-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d538-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d538-1424">Az.EventGrid</span></span>
* <span data-ttu-id="5d538-1425">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5d538-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5d538-1426">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="5d538-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5d538-1427">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="5d538-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5d538-1428">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="5d538-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5d538-1429">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="5d538-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5d538-1430">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="5d538-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5d538-1431">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="5d538-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5d538-1432">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="5d538-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5d538-1433">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="5d538-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5d538-1434">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="5d538-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="5d538-1435">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="5d538-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5d538-1436">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="5d538-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d538-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d538-1437">Az.IotHub</span></span>
* <span data-ttu-id="5d538-1438">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="5d538-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d538-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d538-1439">Az.LogicApp</span></span>
* <span data-ttu-id="5d538-1440">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1441">Az.Resources</span></span>
* <span data-ttu-id="5d538-1442">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5d538-1443">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="5d538-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5d538-1444">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="5d538-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5d538-1445">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5d538-1446">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="5d538-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5d538-1447">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="5d538-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5d538-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5d538-1448">Az.SignalR</span></span>
* <span data-ttu-id="5d538-1449">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1450">Az.Sql</span></span>
* <span data-ttu-id="5d538-1451">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="5d538-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d538-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1452">Az.Storage</span></span>
* <span data-ttu-id="5d538-1453">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5d538-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d538-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="5d538-1455">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="5d538-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5d538-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5d538-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1457">Az.Websites</span></span>
* <span data-ttu-id="5d538-1458">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="5d538-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5d538-1459">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5d538-1460">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5d538-1461">一般</span><span class="sxs-lookup"><span data-stu-id="5d538-1461">General</span></span>

- <span data-ttu-id="5d538-1462">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="5d538-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="5d538-1463">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="5d538-1463">Online help for each module</span></span>
- <span data-ttu-id="5d538-1464">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="5d538-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5d538-1465">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5d538-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1466">Az.Accounts</span></span>
- <span data-ttu-id="5d538-1467">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="5d538-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="5d538-1468">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="5d538-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5d538-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="5d538-1470">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="5d538-1470">Fixes for #7002</span></span>
- <span data-ttu-id="5d538-1471">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5d538-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d538-1472">Az.Batch</span></span>
- <span data-ttu-id="5d538-1473">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="5d538-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5d538-1474">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="5d538-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5d538-1475">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5d538-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5d538-1476">Az.Billing</span></span>
- <span data-ttu-id="5d538-1477">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5d538-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="5d538-1479">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="5d538-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5d538-1480">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="5d538-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5d538-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="5d538-1482">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5d538-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5d538-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5d538-1484">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="5d538-1486">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5d538-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d538-1487">Az.Monitor</span></span>
- <span data-ttu-id="5d538-1488">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5d538-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d538-1489">Az.KeyVault</span></span>
- <span data-ttu-id="5d538-1490">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="5d538-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5d538-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5d538-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="5d538-1492">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5d538-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5d538-1493">Az.Media</span></span>
- <span data-ttu-id="5d538-1494">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="5d538-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5d538-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1495">Az.Network</span></span>
<span data-ttu-id="5d538-1496">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5d538-1497">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5d538-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="5d538-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d538-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d538-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d538-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d538-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d538-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5d538-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5d538-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d538-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5d538-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d538-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5d538-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d538-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5d538-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5d538-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5d538-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5d538-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5d538-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5d538-1512">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5d538-1513">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5d538-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d538-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5d538-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d538-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5d538-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d538-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5d538-1517">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5d538-1518">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5d538-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="5d538-1520">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5d538-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5d538-1521">Az.Profile</span></span>
- <span data-ttu-id="5d538-1522">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d538-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="5d538-1524">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5d538-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1525">Az.Resources</span></span>
- <span data-ttu-id="5d538-1526">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5d538-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="5d538-1528">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="5d538-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5d538-1529">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5d538-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5d538-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="5d538-1531">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="5d538-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5d538-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1532">Az.Sql</span></span>
- <span data-ttu-id="5d538-1533">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="5d538-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5d538-1534">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5d538-1535">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5d538-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1536">Az.Storage</span></span>
- <span data-ttu-id="5d538-1537">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5d538-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1538">Az.Websites</span></span>
- <span data-ttu-id="5d538-1539">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5d538-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5d538-1540">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5d538-1541">一般</span><span class="sxs-lookup"><span data-stu-id="5d538-1541">General</span></span>

* <span data-ttu-id="5d538-1542">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="5d538-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5d538-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1543">Az.Compute</span></span>

* <span data-ttu-id="5d538-1544">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="5d538-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="5d538-1546">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="5d538-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5d538-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d538-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="5d538-1548">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="5d538-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="5d538-1549">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="5d538-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5d538-1550">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="5d538-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5d538-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="5d538-1552">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="5d538-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5d538-1553">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="5d538-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5d538-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1554">Az.Resources</span></span>

* <span data-ttu-id="5d538-1555">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5d538-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5d538-1556">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="5d538-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5d538-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1557">Az.Sql</span></span>

* <span data-ttu-id="5d538-1558">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="5d538-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5d538-1559">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5d538-1560">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="5d538-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5d538-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1561">Az.Storage</span></span>

* <span data-ttu-id="5d538-1562">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="5d538-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5d538-1563">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="5d538-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5d538-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5d538-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5d538-1565">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="5d538-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="5d538-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5d538-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5d538-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5d538-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5d538-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1568">Az.Websites</span></span>

* <span data-ttu-id="5d538-1569">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5d538-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="5d538-1570">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="5d538-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5d538-1571">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="5d538-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5d538-1572">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5d538-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d538-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="5d538-1574">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="5d538-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5d538-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d538-1575">Az.Automation</span></span>
* <span data-ttu-id="5d538-1576">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5d538-1577">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5d538-1578">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5d538-1579">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5d538-1580">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="5d538-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5d538-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1581">Az.Compute</span></span>
* <span data-ttu-id="5d538-1582">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5d538-1583">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="5d538-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5d538-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="5d538-1585">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="5d538-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5d538-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5d538-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5d538-1587">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="5d538-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5d538-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1588">Az.Network</span></span>
* <span data-ttu-id="5d538-1589">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5d538-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5d538-1590">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="5d538-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5d538-1591">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="5d538-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="5d538-1592">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5d538-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5d538-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5d538-1594">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="5d538-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5d538-1595">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="5d538-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5d538-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5d538-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5d538-1597">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5d538-1598">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="5d538-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5d538-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5d538-1599">Az.Relay</span></span>
* <span data-ttu-id="5d538-1600">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="5d538-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5d538-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1601">Az.Resources</span></span>
* <span data-ttu-id="5d538-1602">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="5d538-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5d538-1603">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="5d538-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5d538-1604">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="5d538-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5d538-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-1606">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="5d538-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5d538-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1607">Az.Sql</span></span>
* <span data-ttu-id="5d538-1608">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5d538-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d538-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d538-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d538-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d538-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d538-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d538-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5d538-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d538-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5d538-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d538-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5d538-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d538-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5d538-1617">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="5d538-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5d538-1618">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="5d538-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5d538-1619">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="5d538-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5d538-1620">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="5d538-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5d538-1621">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="5d538-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5d538-1622">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="5d538-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5d538-1623">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="5d538-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5d538-1624">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5d538-1625">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5d538-1626">一般</span><span class="sxs-lookup"><span data-stu-id="5d538-1626">General</span></span>
* <span data-ttu-id="5d538-1627">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="5d538-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5d538-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5d538-1628">Az.Profile</span></span>
* <span data-ttu-id="5d538-1629">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5d538-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5d538-1630">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="5d538-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5d538-1631">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="5d538-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5d538-1632">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="5d538-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5d538-1633">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5d538-1634">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5d538-1635">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d538-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d538-1637">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="5d538-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1638">Az.Compute</span></span>
* <span data-ttu-id="5d538-1639">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5d538-1640">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="5d538-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5d538-1641">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-1643">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="5d538-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5d538-1644">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="5d538-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5d538-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5d538-1645">Az.Insights</span></span>
* <span data-ttu-id="5d538-1646">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="5d538-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5d538-1647">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5d538-1648">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="5d538-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5d538-1649">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="5d538-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1650">Az.Network</span></span>
* <span data-ttu-id="5d538-1651">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="5d538-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5d538-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d538-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5d538-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5d538-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5d538-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5d538-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5d538-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5d538-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5d538-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d538-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5d538-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5d538-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d538-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d538-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d538-1659">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1660">Az.Resources</span></span>
* <span data-ttu-id="5d538-1661">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5d538-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5d538-1662">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="5d538-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d538-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d538-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="5d538-1664">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="5d538-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d538-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d538-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d538-1666">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="5d538-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5d538-1667">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="5d538-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5d538-1668">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="5d538-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5d538-1669">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="5d538-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5d538-1670">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="5d538-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5d538-1671">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5d538-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5d538-1672">Az.Profile</span></span>
* <span data-ttu-id="5d538-1673">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5d538-1674">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5d538-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1675">Az.Compute</span></span>
* <span data-ttu-id="5d538-1676">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="5d538-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5d538-1677">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d538-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d538-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d538-1679">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="5d538-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5d538-1680">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="5d538-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5d538-1681">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d538-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5d538-1682">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="5d538-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5d538-1683">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="5d538-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1684">Az.Network</span></span>
* <span data-ttu-id="5d538-1685">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="5d538-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5d538-1686">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d538-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1687">Az.Resources</span></span>
* <span data-ttu-id="5d538-1688">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="5d538-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5d538-1689">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="5d538-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5d538-1690">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5d538-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5d538-1691">Azure.Storage</span></span>
* <span data-ttu-id="5d538-1692">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5d538-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5d538-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5d538-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5d538-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5d538-1695">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="5d538-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5d538-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5d538-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="5d538-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d538-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d538-1698">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="5d538-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d538-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d538-1699">Az.Compute</span></span>
* <span data-ttu-id="5d538-1700">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="5d538-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5d538-1701">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="5d538-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5d538-1702">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="5d538-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5d538-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5d538-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5d538-1704">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="5d538-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d538-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d538-1705">Az.Network</span></span>
* <span data-ttu-id="5d538-1706">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="5d538-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5d538-1707">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1707">new cmdlets added</span></span>
    - <span data-ttu-id="5d538-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d538-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d538-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d538-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d538-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d538-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d538-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d538-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d538-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5d538-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d538-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5d538-1714">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="5d538-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5d538-1715">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5d538-1716">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d538-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d538-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d538-1717">Az.RedisCache</span></span>
* <span data-ttu-id="5d538-1718">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="5d538-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5d538-1719">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="5d538-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d538-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d538-1720">Az.Resources</span></span>
* <span data-ttu-id="5d538-1721">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5d538-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5d538-1722">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="5d538-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d538-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d538-1723">Az.Sql</span></span>
* <span data-ttu-id="5d538-1724">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="5d538-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d538-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d538-1725">Az.Websites</span></span>
* <span data-ttu-id="5d538-1726">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="5d538-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5d538-1727">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="5d538-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5d538-1728">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="5d538-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5d538-1729">初始版本</span><span class="sxs-lookup"><span data-stu-id="5d538-1729">Initial Release</span></span>
