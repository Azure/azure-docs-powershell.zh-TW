---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537115"
---
## <a name="310---november-2019"></a><span data-ttu-id="411c6-103">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="411c6-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="411c6-104">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="411c6-104">Highlights since the last major release</span></span>
* <span data-ttu-id="411c6-105">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="411c6-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="411c6-106">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="411c6-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-107">Az.Compute</span></span>
* <span data-ttu-id="411c6-108">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="411c6-108">VM Reapply feature</span></span>
    - <span data-ttu-id="411c6-109">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="411c6-110">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="411c6-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="411c6-111">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="411c6-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="411c6-112">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="411c6-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="411c6-113">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="411c6-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="411c6-114">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="411c6-115">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="411c6-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="411c6-116">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="411c6-117">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="411c6-118">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="411c6-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="411c6-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="411c6-120">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="411c6-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="411c6-121">取得訂單</span><span class="sxs-lookup"><span data-stu-id="411c6-121">Get the Order</span></span>
* <span data-ttu-id="411c6-122">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="411c6-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="411c6-123">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="411c6-123">Create new Order</span></span>
* <span data-ttu-id="411c6-124">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="411c6-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="411c6-125">移除訂單</span><span class="sxs-lookup"><span data-stu-id="411c6-125">Remove the Order</span></span>
* <span data-ttu-id="411c6-126">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="411c6-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="411c6-127">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="411c6-127">Now creates Local Share</span></span>
* <span data-ttu-id="411c6-128">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="411c6-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="411c6-129">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="411c6-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="411c6-130">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="411c6-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="411c6-131">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="411c6-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="411c6-132">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="411c6-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="411c6-133">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="411c6-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="411c6-134">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="411c6-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="411c6-135">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="411c6-135">Create new Triggers</span></span>
* <span data-ttu-id="411c6-136">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="411c6-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="411c6-137">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="411c6-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-138">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-139">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="411c6-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="411c6-140">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="411c6-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-142">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="411c6-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="411c6-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="411c6-143">Az.EventHub</span></span>
* <span data-ttu-id="411c6-144">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="411c6-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="411c6-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="411c6-145">Az.FrontDoor</span></span>
* <span data-ttu-id="411c6-146">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="411c6-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="411c6-147">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="411c6-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="411c6-148">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="411c6-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="411c6-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="411c6-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-150">Az.Network</span></span>
* <span data-ttu-id="411c6-151">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="411c6-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="411c6-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="411c6-152">Az.PrivateDns</span></span>
* <span data-ttu-id="411c6-153">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="411c6-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-155">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="411c6-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="411c6-156">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="411c6-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="411c6-157">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="411c6-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="411c6-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="411c6-158">Az.RedisCache</span></span>
* <span data-ttu-id="411c6-159">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="411c6-160">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="411c6-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="411c6-161">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="411c6-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-162">Az.Resources</span></span>
- <span data-ttu-id="411c6-163">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="411c6-164">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="411c6-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="411c6-165">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="411c6-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="411c6-166">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="411c6-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="411c6-167">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="411c6-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-168">Az.Sql</span></span>
* <span data-ttu-id="411c6-169">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="411c6-170">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="411c6-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="411c6-171">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="411c6-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="411c6-172">一般</span><span class="sxs-lookup"><span data-stu-id="411c6-172">General</span></span>
* <span data-ttu-id="411c6-173">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="411c6-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="411c6-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-174">Az.Accounts</span></span>
* <span data-ttu-id="411c6-175">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="411c6-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="411c6-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="411c6-176">Az.Advisor</span></span>
* <span data-ttu-id="411c6-177">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="411c6-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="411c6-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="411c6-178">Az.Batch</span></span>
* <span data-ttu-id="411c6-179">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="411c6-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="411c6-180">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="411c6-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="411c6-181">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="411c6-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="411c6-182">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="411c6-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="411c6-183">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="411c6-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="411c6-184">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="411c6-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="411c6-185">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="411c6-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="411c6-186">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="411c6-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="411c6-187">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="411c6-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="411c6-188">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="411c6-189">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="411c6-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="411c6-190">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="411c6-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="411c6-191">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="411c6-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="411c6-192">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="411c6-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="411c6-193">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="411c6-194">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="411c6-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="411c6-195">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="411c6-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="411c6-196">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="411c6-197">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="411c6-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="411c6-198">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="411c6-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="411c6-199">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="411c6-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="411c6-200">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="411c6-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="411c6-201">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="411c6-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="411c6-202">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="411c6-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="411c6-203">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="411c6-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="411c6-204">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="411c6-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="411c6-205">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="411c6-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="411c6-206">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="411c6-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="411c6-207">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="411c6-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="411c6-208">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="411c6-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="411c6-209">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="411c6-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="411c6-210">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="411c6-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="411c6-211">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="411c6-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="411c6-212">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="411c6-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="411c6-213">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="411c6-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="411c6-214">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="411c6-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="411c6-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="411c6-215">Az.Cdn</span></span>
* <span data-ttu-id="411c6-216">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="411c6-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="411c6-217">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="411c6-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-218">Az.Compute</span></span>
* <span data-ttu-id="411c6-219">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="411c6-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="411c6-220">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="411c6-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="411c6-221">DiskEncryptionSetId 參數已新增至下列 Cmdlet：Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="411c6-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="411c6-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="411c6-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="411c6-223">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="411c6-224">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="411c6-225">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="411c6-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="411c6-226">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="411c6-227">重大變更</span><span class="sxs-lookup"><span data-stu-id="411c6-227">Breaking changes</span></span>
    - <span data-ttu-id="411c6-228">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="411c6-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="411c6-229">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="411c6-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-230">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-231">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="411c6-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-233">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="411c6-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="411c6-234">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="411c6-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="411c6-235">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="411c6-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="411c6-236">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="411c6-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="411c6-237">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="411c6-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="411c6-238">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="411c6-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="411c6-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="411c6-239">Az.FrontDoor</span></span>
* <span data-ttu-id="411c6-240">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="411c6-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="411c6-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="411c6-241">Az.HDInsight</span></span>
* <span data-ttu-id="411c6-242">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="411c6-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="411c6-243">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="411c6-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="411c6-244">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="411c6-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="411c6-245">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="411c6-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="411c6-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="411c6-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="411c6-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="411c6-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="411c6-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="411c6-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="411c6-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="411c6-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="411c6-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="411c6-251">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="411c6-252">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="411c6-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="411c6-253">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="411c6-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="411c6-254">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="411c6-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="411c6-255">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="411c6-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="411c6-256">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="411c6-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="411c6-257">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="411c6-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="411c6-258">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="411c6-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="411c6-259">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="411c6-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="411c6-260">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="411c6-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="411c6-261">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="411c6-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="411c6-262">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="411c6-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="411c6-263">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="411c6-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-264">Az.IotHub</span></span>
* <span data-ttu-id="411c6-265">重大變更：</span><span class="sxs-lookup"><span data-stu-id="411c6-265">Breaking changes:</span></span>
    - <span data-ttu-id="411c6-266">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="411c6-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="411c6-267">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="411c6-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="411c6-268">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="411c6-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="411c6-269">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="411c6-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="411c6-270">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="411c6-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="411c6-271">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="411c6-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="411c6-272">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="411c6-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="411c6-273">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="411c6-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="411c6-274">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="411c6-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="411c6-275">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="411c6-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="411c6-276">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="411c6-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="411c6-277">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="411c6-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-279">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="411c6-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-280">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="411c6-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="411c6-281">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="411c6-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="411c6-282">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="411c6-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-283">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="411c6-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-284">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="411c6-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-285">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="411c6-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-286">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-287">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="411c6-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-288">Az.Resources</span></span>
* <span data-ttu-id="411c6-289">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="411c6-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-290">Az.Network</span></span>
* <span data-ttu-id="411c6-291">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="411c6-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="411c6-292">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="411c6-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="411c6-298">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="411c6-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="411c6-299">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-299">New cmdlet:</span></span>
        - <span data-ttu-id="411c6-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="411c6-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="411c6-301">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="411c6-302">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="411c6-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="411c6-303">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="411c6-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="411c6-304">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="411c6-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="411c6-305">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="411c6-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="411c6-306">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="411c6-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="411c6-307">為 VirtualHub 的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="411c6-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="411c6-308">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-308">New cmdlets added:</span></span>
        - <span data-ttu-id="411c6-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="411c6-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="411c6-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="411c6-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="411c6-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="411c6-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="411c6-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="411c6-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="411c6-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="411c6-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="411c6-314">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="411c6-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="411c6-315">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="411c6-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="411c6-316">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="411c6-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="411c6-317">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="411c6-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="411c6-318">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="411c6-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="411c6-319">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="411c6-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="411c6-320">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="411c6-321">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-321">New cmdlets added:</span></span>
        - <span data-ttu-id="411c6-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="411c6-323">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="411c6-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="411c6-324">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="411c6-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="411c6-325">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="411c6-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="411c6-326">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="411c6-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="411c6-327">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="411c6-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="411c6-328">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="411c6-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="411c6-329">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="411c6-330">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-330">New cmdlets added:</span></span>
        - <span data-ttu-id="411c6-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="411c6-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="411c6-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="411c6-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="411c6-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="411c6-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="411c6-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="411c6-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="411c6-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="411c6-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="411c6-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="411c6-337">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="411c6-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="411c6-338">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="411c6-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="411c6-339">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="411c6-340">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="411c6-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="411c6-341">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="411c6-342">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="411c6-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="411c6-343">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="411c6-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="411c6-344">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="411c6-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="411c6-345">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="411c6-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="411c6-346">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="411c6-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="411c6-347">為 IpGroup 的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="411c6-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="411c6-348">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-348">New cmdlets added:</span></span>
        - <span data-ttu-id="411c6-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="411c6-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="411c6-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="411c6-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-354">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="411c6-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-355">Az.Sql</span></span>
* <span data-ttu-id="411c6-356">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="411c6-357">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="411c6-358">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="411c6-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="411c6-359">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="411c6-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="411c6-360">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="411c6-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="411c6-361">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="411c6-362">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="411c6-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="411c6-363">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="411c6-364">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="411c6-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-365">Az.Storage</span></span>
* <span data-ttu-id="411c6-366">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="411c6-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="411c6-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="411c6-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="411c6-369">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="411c6-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="411c6-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="411c6-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="411c6-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="411c6-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="411c6-372">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="411c6-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="411c6-373">一般</span><span class="sxs-lookup"><span data-stu-id="411c6-373">General</span></span>
* <span data-ttu-id="411c6-374">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="411c6-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="411c6-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-375">Az.Accounts</span></span>
* <span data-ttu-id="411c6-376">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="411c6-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="411c6-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-377">Az.ApiManagement</span></span>
* <span data-ttu-id="411c6-378">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="411c6-379">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-380">Az.Automation</span></span>
* <span data-ttu-id="411c6-381">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="411c6-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="411c6-382">Az.Batch</span></span>
* <span data-ttu-id="411c6-383">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="411c6-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-384">Az.Compute</span></span>
* <span data-ttu-id="411c6-385">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="411c6-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="411c6-386">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="411c6-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="411c6-387">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="411c6-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="411c6-388">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="411c6-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-389">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-390">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="411c6-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="411c6-391">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="411c6-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="411c6-392">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="411c6-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-394">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="411c6-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="411c6-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="411c6-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="411c6-396">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="411c6-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="411c6-397">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="411c6-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="411c6-398">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="411c6-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="411c6-399">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="411c6-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-400">Az.IotHub</span></span>
* <span data-ttu-id="411c6-401">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="411c6-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="411c6-402">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="411c6-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="411c6-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-403">Az.Monitor</span></span>
* <span data-ttu-id="411c6-404">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="411c6-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="411c6-405">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="411c6-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="411c6-406">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="411c6-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="411c6-407">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="411c6-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-408">Az.Network</span></span>
* <span data-ttu-id="411c6-409">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="411c6-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="411c6-410">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="411c6-411">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-411">New cmdlets added:</span></span>
        - <span data-ttu-id="411c6-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="411c6-413">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="411c6-414">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="411c6-415">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="411c6-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="411c6-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="411c6-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="411c6-419">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="411c6-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="411c6-420">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="411c6-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="411c6-421">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="411c6-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="411c6-422">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="411c6-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="411c6-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="411c6-423">Az.RedisCache</span></span>
* <span data-ttu-id="411c6-424">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="411c6-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-425">Az.Sql</span></span>
* <span data-ttu-id="411c6-426">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-427">Az.Storage</span></span>
* <span data-ttu-id="411c6-428">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="411c6-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="411c6-429">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="411c6-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="411c6-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="411c6-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="411c6-431">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="411c6-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="411c6-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="411c6-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="411c6-433">Az.StorageSync</span></span>
* <span data-ttu-id="411c6-434">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="411c6-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-435">Az.Websites</span></span>
* <span data-ttu-id="411c6-436">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="411c6-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="411c6-437">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="411c6-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="411c6-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-438">Az.ApiManagement</span></span>
* <span data-ttu-id="411c6-439">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="411c6-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="411c6-440">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="411c6-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="411c6-441">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="411c6-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-442">Az.Automation</span></span>
* <span data-ttu-id="411c6-443">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="411c6-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="411c6-444">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="411c6-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="411c6-445">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="411c6-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-446">Az.Compute</span></span>
* <span data-ttu-id="411c6-447">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="411c6-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="411c6-448">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="411c6-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="411c6-449">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="411c6-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="411c6-450">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="411c6-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="411c6-451">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="411c6-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="411c6-452">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="411c6-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="411c6-453">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="411c6-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="411c6-454">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="411c6-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="411c6-455">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-456">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-457">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="411c6-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="411c6-458">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="411c6-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="411c6-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="411c6-459">Az.HDInsight</span></span>
* <span data-ttu-id="411c6-460">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="411c6-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-461">Az.IotHub</span></span>
* <span data-ttu-id="411c6-462">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="411c6-463">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="411c6-464">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="411c6-464">New cmdlets are:</span></span>
    - <span data-ttu-id="411c6-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="411c6-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="411c6-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="411c6-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="411c6-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="411c6-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="411c6-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="411c6-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="411c6-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-469">Az.Monitor</span></span>
* <span data-ttu-id="411c6-470">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="411c6-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="411c6-471">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="411c6-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="411c6-472">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="411c6-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="411c6-473">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="411c6-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="411c6-474">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="411c6-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="411c6-475">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="411c6-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="411c6-476">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="411c6-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="411c6-477">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="411c6-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="411c6-478">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="411c6-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="411c6-479">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="411c6-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="411c6-480">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="411c6-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="411c6-481">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="411c6-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="411c6-482">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="411c6-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="411c6-483">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="411c6-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="411c6-484">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="411c6-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="411c6-485">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="411c6-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="411c6-486">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="411c6-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="411c6-487">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="411c6-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="411c6-488">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="411c6-489">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="411c6-489">Overall improved help files</span></span>
* <span data-ttu-id="411c6-490">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="411c6-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-491">Az.Network</span></span>
* <span data-ttu-id="411c6-492">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="411c6-493">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="411c6-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="411c6-494">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="411c6-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="411c6-495">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="411c6-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="411c6-496">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="411c6-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="411c6-497">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="411c6-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="411c6-498">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="411c6-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="411c6-499">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="411c6-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="411c6-500">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="411c6-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="411c6-501">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="411c6-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="411c6-502">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="411c6-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="411c6-503">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="411c6-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="411c6-504">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-504">New cmdlets</span></span>
        - <span data-ttu-id="411c6-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="411c6-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="411c6-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="411c6-507">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="411c6-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="411c6-508">New-VpnSite</span></span>
        - <span data-ttu-id="411c6-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="411c6-509">Update-VpnSite</span></span>
        - <span data-ttu-id="411c6-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-510">New-VpnConnection</span></span>
        - <span data-ttu-id="411c6-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-511">Update-VpnConnection</span></span>
* <span data-ttu-id="411c6-512">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-514">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="411c6-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="411c6-515">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="411c6-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-516">Az.Resources</span></span>
* <span data-ttu-id="411c6-517">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="411c6-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-519">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="411c6-520">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="411c6-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="411c6-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="411c6-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="411c6-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="411c6-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="411c6-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="411c6-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="411c6-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="411c6-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="411c6-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="411c6-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="411c6-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="411c6-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="411c6-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="411c6-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="411c6-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="411c6-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="411c6-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="411c6-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="411c6-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="411c6-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="411c6-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="411c6-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="411c6-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="411c6-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="411c6-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="411c6-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="411c6-534">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="411c6-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="411c6-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="411c6-535">Az.SignalR</span></span>
* <span data-ttu-id="411c6-536">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-537">Az.Sql</span></span>
* <span data-ttu-id="411c6-538">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="411c6-539">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="411c6-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="411c6-540">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="411c6-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="411c6-541">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="411c6-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="411c6-542">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="411c6-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-543">Az.Storage</span></span>
* <span data-ttu-id="411c6-544">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="411c6-545">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="411c6-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="411c6-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="411c6-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="411c6-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="411c6-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="411c6-548">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="411c6-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="411c6-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="411c6-550">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="411c6-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="411c6-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="411c6-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="411c6-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="411c6-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="411c6-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="411c6-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="411c6-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="411c6-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-555">Az.Websites</span></span>
* <span data-ttu-id="411c6-556">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="411c6-557">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="411c6-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="411c6-558">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="411c6-559">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="411c6-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="411c6-560">一般</span><span class="sxs-lookup"><span data-stu-id="411c6-560">General</span></span>
* <span data-ttu-id="411c6-561">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="411c6-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="411c6-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-562">Az.Accounts</span></span>
* <span data-ttu-id="411c6-563">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="411c6-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="411c6-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="411c6-564">Az.Aks</span></span>
* <span data-ttu-id="411c6-565">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="411c6-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="411c6-566">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="411c6-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="411c6-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-567">Az.ApiManagement</span></span>
* <span data-ttu-id="411c6-568">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="411c6-569">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="411c6-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="411c6-570">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="411c6-571">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="411c6-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="411c6-572">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="411c6-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="411c6-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="411c6-573">Az.Batch</span></span>
* <span data-ttu-id="411c6-574">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="411c6-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="411c6-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="411c6-575">Az.Cdn</span></span>
* <span data-ttu-id="411c6-576">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-577">Az.Compute</span></span>
* <span data-ttu-id="411c6-578">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="411c6-579">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="411c6-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="411c6-580">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="411c6-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="411c6-581">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="411c6-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="411c6-582">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="411c6-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="411c6-583">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="411c6-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="411c6-584">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="411c6-585">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="411c6-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-586">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-587">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="411c6-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="411c6-588">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="411c6-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="411c6-589">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="411c6-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="411c6-590">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="411c6-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-592">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="411c6-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="411c6-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="411c6-593">Az.EventHub</span></span>
* <span data-ttu-id="411c6-594">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="411c6-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="411c6-595">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="411c6-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="411c6-596">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="411c6-597">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="411c6-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="411c6-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="411c6-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="411c6-599">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="411c6-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="411c6-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-600">Az.Monitor</span></span>
* <span data-ttu-id="411c6-601">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-602">Az.Network</span></span>
* <span data-ttu-id="411c6-603">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="411c6-604">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="411c6-605">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="411c6-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="411c6-606">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="411c6-607">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="411c6-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="411c6-608">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="411c6-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="411c6-609">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="411c6-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="411c6-611">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="411c6-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="411c6-612">新增了範例</span><span class="sxs-lookup"><span data-stu-id="411c6-612">Added example</span></span>
    - <span data-ttu-id="411c6-613">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="411c6-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="411c6-614">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="411c6-615">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="411c6-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-617">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-618">Az.Resources</span></span>
* <span data-ttu-id="411c6-619">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="411c6-620">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="411c6-621">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="411c6-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="411c6-622">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="411c6-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="411c6-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="411c6-623">Az.ServiceBus</span></span>
* <span data-ttu-id="411c6-624">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="411c6-625">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="411c6-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="411c6-626">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="411c6-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-628">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="411c6-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="411c6-629">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="411c6-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="411c6-630">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="411c6-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="411c6-631">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="411c6-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="411c6-632">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="411c6-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="411c6-633">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-634">Az.Sql</span></span>
* <span data-ttu-id="411c6-635">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="411c6-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-636">Az.Storage</span></span>
* <span data-ttu-id="411c6-637">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="411c6-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="411c6-638">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="411c6-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="411c6-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="411c6-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="411c6-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="411c6-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="411c6-641">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="411c6-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="411c6-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="411c6-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-643">Az.Websites</span></span>
* <span data-ttu-id="411c6-644">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="411c6-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="411c6-645">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="411c6-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-646">Az.Accounts</span></span>
* <span data-ttu-id="411c6-647">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="411c6-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="411c6-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="411c6-649">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="411c6-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-650">Az.Automation</span></span>
* <span data-ttu-id="411c6-651">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="411c6-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="411c6-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="411c6-653">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-654">Az.Compute</span></span>
* <span data-ttu-id="411c6-655">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="411c6-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="411c6-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="411c6-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="411c6-657">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="411c6-658">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="411c6-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-659">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-660">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="411c6-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="411c6-661">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="411c6-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="411c6-662">Az.EventHub</span></span>
* <span data-ttu-id="411c6-663">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="411c6-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="411c6-664">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="411c6-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="411c6-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="411c6-665">Az.KeyVault</span></span>
* <span data-ttu-id="411c6-666">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="411c6-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="411c6-667">Az.LogicApp</span></span>
* <span data-ttu-id="411c6-668">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="411c6-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="411c6-669">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="411c6-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="411c6-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="411c6-670">Az.ManagedServices</span></span>
* <span data-ttu-id="411c6-671">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-672">Az.Network</span></span>
* <span data-ttu-id="411c6-673">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="411c6-674">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-674">New cmdlets</span></span>
        - <span data-ttu-id="411c6-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="411c6-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="411c6-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="411c6-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="411c6-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="411c6-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="411c6-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="411c6-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="411c6-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="411c6-683">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="411c6-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="411c6-684">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="411c6-685">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="411c6-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="411c6-686">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="411c6-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="411c6-687">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="411c6-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="411c6-688">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="411c6-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="411c6-689">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-689">Updated cmdlets</span></span>
        - <span data-ttu-id="411c6-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="411c6-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="411c6-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="411c6-693">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="411c6-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="411c6-694">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="411c6-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="411c6-695">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="411c6-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="411c6-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="411c6-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="411c6-699">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="411c6-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="411c6-700">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="411c6-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="411c6-701">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="411c6-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="411c6-703">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="411c6-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="411c6-704">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="411c6-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-706">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="411c6-707">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="411c6-708">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="411c6-709">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="411c6-710">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="411c6-711">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="411c6-712">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="411c6-713">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="411c6-714">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="411c6-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="411c6-715">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="411c6-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-716">Az.Resources</span></span>
- <span data-ttu-id="411c6-717">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="411c6-718">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="411c6-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="411c6-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="411c6-719">Az.ServiceBus</span></span>
* <span data-ttu-id="411c6-720">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="411c6-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="411c6-721">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="411c6-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-722">Az.Sql</span></span>
* <span data-ttu-id="411c6-723">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="411c6-724">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="411c6-725">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="411c6-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-726">Az.Storage</span></span>
* <span data-ttu-id="411c6-727">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="411c6-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="411c6-728">Az.StorageSync</span></span>
* <span data-ttu-id="411c6-729">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="411c6-730">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="411c6-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-731">Az.Websites</span></span>
* <span data-ttu-id="411c6-732">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="411c6-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="411c6-733">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="411c6-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="411c6-734">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="411c6-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="411c6-735">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="411c6-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-736">Az.Accounts</span></span>
* <span data-ttu-id="411c6-737">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="411c6-738">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="411c6-739">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="411c6-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="411c6-740">Az.Advisor</span></span>
* <span data-ttu-id="411c6-741">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="411c6-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="411c6-742">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="411c6-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="411c6-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-743">Az.ApiManagement</span></span>
* <span data-ttu-id="411c6-744">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="411c6-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="411c6-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="411c6-746">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="411c6-747">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="411c6-748">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="411c6-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="411c6-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="411c6-750">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-751">Az.Automation</span></span>
* <span data-ttu-id="411c6-752">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="411c6-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-753">Az.Compute</span></span>
* <span data-ttu-id="411c6-754">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-755">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-756">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="411c6-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="411c6-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="411c6-757">Az.EventGrid</span></span>
* <span data-ttu-id="411c6-758">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-759">Az.IotHub</span></span>
* <span data-ttu-id="411c6-760">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-761">Az.Network</span></span>
* <span data-ttu-id="411c6-762">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="411c6-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="411c6-763">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="411c6-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="411c6-765">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="411c6-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="411c6-766">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="411c6-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="411c6-768">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="411c6-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-770">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="411c6-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-771">Az.Resources</span></span>
    - <span data-ttu-id="411c6-772">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="411c6-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="411c6-773">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="411c6-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="411c6-774">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="411c6-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="411c6-775">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="411c6-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="411c6-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="411c6-776">Az.ServiceBus</span></span>
* <span data-ttu-id="411c6-777">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="411c6-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-778">Az.Sql</span></span>
* <span data-ttu-id="411c6-779">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="411c6-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="411c6-780">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="411c6-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="411c6-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="411c6-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="411c6-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="411c6-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="411c6-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="411c6-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="411c6-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="411c6-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="411c6-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="411c6-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="411c6-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="411c6-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="411c6-787">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="411c6-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-788">Az.Storage</span></span>
* <span data-ttu-id="411c6-789">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="411c6-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="411c6-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="411c6-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="411c6-791">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="411c6-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="411c6-792">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="411c6-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="411c6-793">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="411c6-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="411c6-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="411c6-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="411c6-796">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="411c6-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="411c6-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="411c6-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="411c6-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="411c6-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="411c6-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="411c6-799">Az.StorageSync</span></span>
* <span data-ttu-id="411c6-800">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="411c6-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="411c6-801">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="411c6-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-802">Az.Accounts</span></span>
* <span data-ttu-id="411c6-803">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="411c6-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="411c6-804">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="411c6-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="411c6-805">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="411c6-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="411c6-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="411c6-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="411c6-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="411c6-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-808">Az.Compute</span></span>
* <span data-ttu-id="411c6-809">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="411c6-810">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="411c6-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="411c6-811">Az.Dns</span></span>
* <span data-ttu-id="411c6-812">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="411c6-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="411c6-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="411c6-813">Az.EventGrid</span></span>
* <span data-ttu-id="411c6-814">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="411c6-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="411c6-815">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-815">New cmdlets:</span></span>
    - <span data-ttu-id="411c6-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="411c6-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="411c6-817">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="411c6-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="411c6-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="411c6-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="411c6-819">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="411c6-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="411c6-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="411c6-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="411c6-821">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="411c6-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="411c6-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="411c6-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="411c6-823">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="411c6-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="411c6-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="411c6-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="411c6-825">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="411c6-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="411c6-826">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="411c6-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="411c6-827">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="411c6-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="411c6-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="411c6-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="411c6-829">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="411c6-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="411c6-830">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="411c6-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="411c6-831">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="411c6-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="411c6-832">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="411c6-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="411c6-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="411c6-834">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="411c6-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="411c6-835">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="411c6-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="411c6-836">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="411c6-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="411c6-837">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="411c6-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="411c6-838">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="411c6-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="411c6-839">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="411c6-840">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="411c6-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="411c6-841">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="411c6-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="411c6-842">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="411c6-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="411c6-843">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="411c6-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="411c6-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="411c6-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="411c6-845">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="411c6-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="411c6-846">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="411c6-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="411c6-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="411c6-847">Az.FrontDoor</span></span>
* <span data-ttu-id="411c6-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="411c6-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="411c6-849">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="411c6-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="411c6-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="411c6-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="411c6-851">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="411c6-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-852">Az.Network</span></span>
* <span data-ttu-id="411c6-853">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="411c6-854">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-854">New cmdlets</span></span>
        - <span data-ttu-id="411c6-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="411c6-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="411c6-856">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="411c6-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="411c6-857">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-857">New cmdlets</span></span> 
        - <span data-ttu-id="411c6-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="411c6-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="411c6-859">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="411c6-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="411c6-860">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-860">New cmdlets</span></span> 
        - <span data-ttu-id="411c6-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="411c6-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="411c6-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="411c6-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="411c6-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="411c6-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="411c6-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="411c6-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="411c6-866">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="411c6-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="411c6-867">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-867">New cmdlets</span></span>
        - <span data-ttu-id="411c6-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="411c6-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="411c6-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="411c6-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="411c6-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="411c6-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="411c6-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="411c6-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="411c6-872">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="411c6-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="411c6-873">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="411c6-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="411c6-874">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="411c6-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="411c6-875">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="411c6-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="411c6-876">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="411c6-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="411c6-877">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="411c6-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="411c6-878">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="411c6-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="411c6-879">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="411c6-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="411c6-880">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="411c6-881">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="411c6-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="411c6-882">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="411c6-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="411c6-883">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="411c6-884">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="411c6-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="411c6-885">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="411c6-886">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="411c6-887">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="411c6-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="411c6-888">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="411c6-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="411c6-889">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="411c6-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="411c6-890">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="411c6-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="411c6-891">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="411c6-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="411c6-892">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="411c6-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="411c6-893">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="411c6-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="411c6-894">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="411c6-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="411c6-896">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="411c6-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-897">Az.Resources</span></span>
* <span data-ttu-id="411c6-898">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="411c6-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="411c6-899">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="411c6-900">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="411c6-901">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="411c6-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-903">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-904">Az.Sql</span></span>
* <span data-ttu-id="411c6-905">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="411c6-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="411c6-906">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="411c6-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="411c6-907">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="411c6-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="411c6-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="411c6-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="411c6-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="411c6-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="411c6-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="411c6-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="411c6-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="411c6-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="411c6-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="411c6-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-913">Az.Storage</span></span>
* <span data-ttu-id="411c6-914">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="411c6-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="411c6-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="411c6-916">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="411c6-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="411c6-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-918">Az.Websites</span></span>
* <span data-ttu-id="411c6-919">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="411c6-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="411c6-920">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="411c6-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="411c6-921">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="411c6-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="411c6-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="411c6-922">Az.Cdn</span></span>
* <span data-ttu-id="411c6-923">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="411c6-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-924">Az.Compute</span></span>
* <span data-ttu-id="411c6-925">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="411c6-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="411c6-926">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="411c6-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="411c6-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="411c6-927">Az.EventHub</span></span>
* <span data-ttu-id="411c6-928">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="411c6-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="411c6-929">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411c6-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-930">Az.Network</span></span>
* <span data-ttu-id="411c6-931">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="411c6-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="411c6-932">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="411c6-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="411c6-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="411c6-934">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="411c6-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-936">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="411c6-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="411c6-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="411c6-937">Az.ServiceBus</span></span>
* <span data-ttu-id="411c6-938">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411c6-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-940">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="411c6-941">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="411c6-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-942">Az.Sql</span></span>
* <span data-ttu-id="411c6-943">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="411c6-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="411c6-944">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="411c6-945">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="411c6-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="411c6-946">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-947">Az.Websites</span></span>
* <span data-ttu-id="411c6-948">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="411c6-949">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="411c6-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="411c6-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-950">Az.ApiManagement</span></span>
* <span data-ttu-id="411c6-951">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="411c6-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="411c6-952">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="411c6-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="411c6-953">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="411c6-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="411c6-954">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="411c6-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="411c6-955">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="411c6-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="411c6-956">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="411c6-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="411c6-957">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="411c6-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="411c6-958">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="411c6-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="411c6-959">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="411c6-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="411c6-960">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="411c6-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="411c6-961">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="411c6-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="411c6-962">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="411c6-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="411c6-963">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="411c6-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="411c6-964">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="411c6-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="411c6-965">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="411c6-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="411c6-966">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="411c6-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="411c6-967">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="411c6-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="411c6-968">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="411c6-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="411c6-969">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="411c6-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="411c6-970">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="411c6-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="411c6-971">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="411c6-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="411c6-972">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="411c6-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="411c6-973">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="411c6-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="411c6-974">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="411c6-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="411c6-975">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="411c6-976">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="411c6-977">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="411c6-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="411c6-978">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="411c6-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="411c6-979">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="411c6-980">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="411c6-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="411c6-981">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="411c6-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="411c6-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="411c6-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="411c6-983">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="411c6-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="411c6-984">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="411c6-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="411c6-985">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="411c6-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="411c6-986">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="411c6-987">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="411c6-988">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="411c6-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="411c6-989">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="411c6-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="411c6-990">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="411c6-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="411c6-991">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="411c6-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="411c6-992">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="411c6-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="411c6-993">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="411c6-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="411c6-994">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="411c6-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="411c6-995">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="411c6-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="411c6-996">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="411c6-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="411c6-997">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="411c6-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="411c6-998">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="411c6-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="411c6-999">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="411c6-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="411c6-1000">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="411c6-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="411c6-1001">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="411c6-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="411c6-1002">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="411c6-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="411c6-1003">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="411c6-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="411c6-1004">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="411c6-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="411c6-1005">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="411c6-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="411c6-1006">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="411c6-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="411c6-1007">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="411c6-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="411c6-1008">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="411c6-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="411c6-1009">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="411c6-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="411c6-1010">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="411c6-1011">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="411c6-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="411c6-1012">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="411c6-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="411c6-1013">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="411c6-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="411c6-1014">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="411c6-1015">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="411c6-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="411c6-1016">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="411c6-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="411c6-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="411c6-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="411c6-1018">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="411c6-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="411c6-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="411c6-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="411c6-1020">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="411c6-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="411c6-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="411c6-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="411c6-1022">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="411c6-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="411c6-1023">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="411c6-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="411c6-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="411c6-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="411c6-1025">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="411c6-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="411c6-1026">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="411c6-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="411c6-1027">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="411c6-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1028">Az.Automation</span></span>
* <span data-ttu-id="411c6-1029">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="411c6-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="411c6-1030">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="411c6-1031">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="411c6-1032">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="411c6-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="411c6-1033">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="411c6-1034">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="411c6-1035">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="411c6-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1036">Az.Compute</span></span>
* <span data-ttu-id="411c6-1037">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="411c6-1038">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="411c6-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1040">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="411c6-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="411c6-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-1041">Az.Monitor</span></span>
* <span data-ttu-id="411c6-1042">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1043">Az.Network</span></span>
* <span data-ttu-id="411c6-1044">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="411c6-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="411c6-1045">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="411c6-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="411c6-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="411c6-1047">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="411c6-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1048">Az.Resources</span></span>
* <span data-ttu-id="411c6-1049">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="411c6-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1050">Az.Sql</span></span>
* <span data-ttu-id="411c6-1051">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="411c6-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="411c6-1052">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1053">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1054">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="411c6-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="411c6-1056">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="411c6-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="411c6-1057">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="411c6-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1058">Az.Compute</span></span>
* <span data-ttu-id="411c6-1059">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="411c6-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="411c6-1060">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="411c6-1061">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="411c6-1062">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="411c6-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="411c6-1063">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="411c6-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="411c6-1064">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="411c6-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="411c6-1065">重大變更</span><span class="sxs-lookup"><span data-stu-id="411c6-1065">Breaking changes</span></span>
    - <span data-ttu-id="411c6-1066">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="411c6-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="411c6-1067">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="411c6-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="411c6-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="411c6-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="411c6-1069">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="411c6-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="411c6-1070">Az.Dns</span></span>
* <span data-ttu-id="411c6-1071">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="411c6-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="411c6-1072">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="411c6-1073">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="411c6-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="411c6-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="411c6-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="411c6-1075">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="411c6-1076">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="411c6-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="411c6-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="411c6-1077">Az.HDInsight</span></span>
* <span data-ttu-id="411c6-1078">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="411c6-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="411c6-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="411c6-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="411c6-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="411c6-1081">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="411c6-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="411c6-1082">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="411c6-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="411c6-1083">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="411c6-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="411c6-1084">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="411c6-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="411c6-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-1085">Az.Monitor</span></span>
* <span data-ttu-id="411c6-1086">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="411c6-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="411c6-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="411c6-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="411c6-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="411c6-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="411c6-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="411c6-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="411c6-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="411c6-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="411c6-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="411c6-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="411c6-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="411c6-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="411c6-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="411c6-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="411c6-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="411c6-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="411c6-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="411c6-1098">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="411c6-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="411c6-1099">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1100">Az.Network</span></span>
* <span data-ttu-id="411c6-1101">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="411c6-1102">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1102">New cmdlets</span></span>
        - <span data-ttu-id="411c6-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="411c6-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="411c6-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="411c6-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="411c6-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="411c6-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="411c6-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="411c6-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="411c6-1107">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="411c6-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="411c6-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="411c6-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="411c6-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="411c6-1110">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="411c6-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="411c6-1111">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="411c6-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="411c6-1112">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="411c6-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="411c6-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="411c6-1114">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="411c6-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="411c6-1115">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="411c6-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="411c6-1116">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="411c6-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-1118">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="411c6-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="411c6-1119">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="411c6-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="411c6-1120">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="411c6-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="411c6-1121">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="411c6-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="411c6-1122">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="411c6-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="411c6-1123">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="411c6-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="411c6-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="411c6-1124">Az.Relay</span></span>
* <span data-ttu-id="411c6-1125">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="411c6-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="411c6-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="411c6-1127">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1128">Az.Storage</span></span>
* <span data-ttu-id="411c6-1129">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="411c6-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="411c6-1130">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="411c6-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="411c6-1131">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="411c6-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="411c6-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="411c6-1133">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="411c6-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="411c6-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="411c6-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="411c6-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1137">Az.Websites</span></span>
* <span data-ttu-id="411c6-1138">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="411c6-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="411c6-1139">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="411c6-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="411c6-1140">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="411c6-1141">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="411c6-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="411c6-1142">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="411c6-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="411c6-1143">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="411c6-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="411c6-1144">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="411c6-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="411c6-1145">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="411c6-1146">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="411c6-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="411c6-1147">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="411c6-1148">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="411c6-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1149">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1150">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="411c6-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="411c6-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="411c6-1151">Az.Batch</span></span>
* <span data-ttu-id="411c6-1152">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="411c6-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="411c6-1153">Az.Cdn</span></span>
* <span data-ttu-id="411c6-1154">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="411c6-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="411c6-1156">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1157">Az.Compute</span></span>
* <span data-ttu-id="411c6-1158">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="411c6-1159">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="411c6-1160">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="411c6-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-1161">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-1162">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="411c6-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1164">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="411c6-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="411c6-1165">Az.EventGrid</span></span>
* <span data-ttu-id="411c6-1166">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="411c6-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="411c6-1167">Az.EventHub</span></span>
* <span data-ttu-id="411c6-1168">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="411c6-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="411c6-1169">Az.HDInsight</span></span>
* <span data-ttu-id="411c6-1170">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-1171">Az.IotHub</span></span>
* <span data-ttu-id="411c6-1172">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="411c6-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="411c6-1173">Az.KeyVault</span></span>
* <span data-ttu-id="411c6-1174">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="411c6-1175">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="411c6-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="411c6-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="411c6-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="411c6-1177">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="411c6-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="411c6-1178">Az.Media</span></span>
* <span data-ttu-id="411c6-1179">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="411c6-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-1180">Az.Monitor</span></span>
  * <span data-ttu-id="411c6-1181">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="411c6-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="411c6-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="411c6-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="411c6-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="411c6-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="411c6-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="411c6-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="411c6-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="411c6-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="411c6-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="411c6-1187">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="411c6-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1188">Az.Network</span></span>
* <span data-ttu-id="411c6-1189">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="411c6-1190">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="411c6-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="411c6-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="411c6-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="411c6-1192">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="411c6-1194">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="411c6-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="411c6-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="411c6-1196">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-1198">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="411c6-1199">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="411c6-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="411c6-1200">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="411c6-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="411c6-1201">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="411c6-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="411c6-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="411c6-1202">Az.RedisCache</span></span>
* <span data-ttu-id="411c6-1203">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1204">Az.Resources</span></span>
* <span data-ttu-id="411c6-1205">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="411c6-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1206">Az.Sql</span></span>
* <span data-ttu-id="411c6-1207">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="411c6-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="411c6-1208">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="411c6-1209">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="411c6-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="411c6-1210">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="411c6-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="411c6-1211">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="411c6-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="411c6-1212">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="411c6-1213">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="411c6-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1214">Az.Websites</span></span>
* <span data-ttu-id="411c6-1215">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="411c6-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="411c6-1216">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="411c6-1217">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="411c6-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="411c6-1218">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="411c6-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="411c6-1219">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="411c6-1220">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="411c6-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="411c6-1221">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="411c6-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="411c6-1222">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="411c6-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="411c6-1223">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="411c6-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="411c6-1224">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="411c6-1225">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="411c6-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="411c6-1226">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="411c6-1227">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="411c6-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1228">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1229">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="411c6-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="411c6-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="411c6-1231">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="411c6-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="411c6-1232">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="411c6-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1233">Az.Automation</span></span>
* <span data-ttu-id="411c6-1234">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="411c6-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="411c6-1235">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="411c6-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="411c6-1236">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="411c6-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1237">Az.Compute</span></span>
* <span data-ttu-id="411c6-1238">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="411c6-1239">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="411c6-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="411c6-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="411c6-1241">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="411c6-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-1242">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-1243">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="411c6-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="411c6-1244">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1245">Az.Resources</span></span>
* <span data-ttu-id="411c6-1246">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="411c6-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="411c6-1247">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="411c6-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="411c6-1248">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="411c6-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="411c6-1249">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="411c6-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="411c6-1250">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="411c6-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="411c6-1251">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="411c6-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1252">Az.Sql</span></span>
* <span data-ttu-id="411c6-1253">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="411c6-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1254">Az.Storage</span></span>
* <span data-ttu-id="411c6-1255">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="411c6-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="411c6-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="411c6-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="411c6-1257">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="411c6-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="411c6-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="411c6-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="411c6-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="411c6-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="411c6-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="411c6-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="411c6-1262">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="411c6-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="411c6-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="411c6-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="411c6-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="411c6-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="411c6-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="411c6-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="411c6-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="411c6-1267">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="411c6-1268">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="411c6-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="411c6-1269">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="411c6-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="411c6-1270">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="411c6-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="411c6-1271">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="411c6-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="411c6-1272">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="411c6-1273">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="411c6-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="411c6-1274">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="411c6-1275">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1276">Az.Automation</span></span>
* <span data-ttu-id="411c6-1277">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="411c6-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="411c6-1278">動態分組</span><span class="sxs-lookup"><span data-stu-id="411c6-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="411c6-1279">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="411c6-1279">Pre-Post script</span></span>
    * <span data-ttu-id="411c6-1280">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="411c6-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1281">Az.Compute</span></span>
* <span data-ttu-id="411c6-1282">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="411c6-1283">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="411c6-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="411c6-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="411c6-1284">Az.KeyVault</span></span>
* <span data-ttu-id="411c6-1285">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1286">Az.Network</span></span>
* <span data-ttu-id="411c6-1287">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="411c6-1288">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="411c6-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-1290">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="411c6-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="411c6-1291">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1292">Az.Resources</span></span>
* <span data-ttu-id="411c6-1293">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="411c6-1294">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="411c6-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1295">Az.Sql</span></span>
* <span data-ttu-id="411c6-1296">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="411c6-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1297">Az.Storage</span></span>
* <span data-ttu-id="411c6-1298">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="411c6-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="411c6-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="411c6-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="411c6-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="411c6-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="411c6-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="411c6-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="411c6-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="411c6-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1305">Az.Websites</span></span>
* <span data-ttu-id="411c6-1306">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="411c6-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="411c6-1307">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1308">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1309">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="411c6-1310">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1311">Az.Automation</span></span>
* <span data-ttu-id="411c6-1312">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="411c6-1313">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="411c6-1314">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="411c6-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="411c6-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="411c6-1315">Az.Cdn</span></span>
* <span data-ttu-id="411c6-1316">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1317">Az.Compute</span></span>
* <span data-ttu-id="411c6-1318">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-1319">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-1320">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="411c6-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="411c6-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="411c6-1321">Az.LogicApp</span></span>
* <span data-ttu-id="411c6-1322">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="411c6-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1323">Az.Network</span></span>
* <span data-ttu-id="411c6-1324">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-1326">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="411c6-1327">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="411c6-1327">SDK Update</span></span>
* <span data-ttu-id="411c6-1328">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="411c6-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="411c6-1329">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="411c6-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1330">Az.Resources</span></span>
* <span data-ttu-id="411c6-1331">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="411c6-1332">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="411c6-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="411c6-1333">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="411c6-1334">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="411c6-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="411c6-1335">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="411c6-1336">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="411c6-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1337">Az.Sql</span></span>
* <span data-ttu-id="411c6-1338">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="411c6-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="411c6-1339">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="411c6-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1340">Az.Storage</span></span>
* <span data-ttu-id="411c6-1341">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="411c6-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="411c6-1342">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="411c6-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="411c6-1344">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1345">Az.Automation</span></span>
* <span data-ttu-id="411c6-1346">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="411c6-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="411c6-1347">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="411c6-1348">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="411c6-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="411c6-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="411c6-1350">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="411c6-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1351">Az.Compute</span></span>
* <span data-ttu-id="411c6-1352">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="411c6-1353">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="411c6-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="411c6-1354">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="411c6-1355">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="411c6-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1357">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="411c6-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="411c6-1358">Az.EventHub</span></span>
* <span data-ttu-id="411c6-1359">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="411c6-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="411c6-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="411c6-1360">Az.KeyVault</span></span>
* <span data-ttu-id="411c6-1361">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="411c6-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="411c6-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="411c6-1362">Az.LogicApp</span></span>
* <span data-ttu-id="411c6-1363">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="411c6-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="411c6-1364">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="411c6-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="411c6-1365">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="411c6-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="411c6-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="411c6-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="411c6-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="411c6-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="411c6-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="411c6-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="411c6-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="411c6-1370">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="411c6-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="411c6-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="411c6-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="411c6-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="411c6-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="411c6-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="411c6-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="411c6-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="411c6-1375">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="411c6-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="411c6-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-1376">Az.Monitor</span></span>
* <span data-ttu-id="411c6-1377">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="411c6-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1378">Az.Network</span></span>
* <span data-ttu-id="411c6-1379">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="411c6-1381">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="411c6-1382">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="411c6-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="411c6-1383">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="411c6-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="411c6-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1384">Az.Resources</span></span>
* <span data-ttu-id="411c6-1385">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="411c6-1386">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="411c6-1387">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="411c6-1388">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="411c6-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1389">Az.Sql</span></span>
* <span data-ttu-id="411c6-1390">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="411c6-1391">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="411c6-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1392">Az.Websites</span></span>
* <span data-ttu-id="411c6-1393">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="411c6-1394">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1395">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1396">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="411c6-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="411c6-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="411c6-1398">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="411c6-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1399">Az.Compute</span></span>
* <span data-ttu-id="411c6-1400">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="411c6-1401">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="411c6-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="411c6-1402">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="411c6-1404">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="411c6-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1405">Az.Resources</span></span>
* <span data-ttu-id="411c6-1406">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="411c6-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="411c6-1407">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="411c6-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="411c6-1408">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="411c6-1409">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="411c6-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1410">Az.Sql</span></span>
* <span data-ttu-id="411c6-1411">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="411c6-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="411c6-1412">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="411c6-1413">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="411c6-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="411c6-1414">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1415">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1416">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="411c6-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="411c6-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="411c6-1418">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="411c6-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="411c6-1420">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="411c6-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="411c6-1421">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1422">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1423">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="411c6-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="411c6-1424">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="411c6-1425">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="411c6-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="411c6-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="411c6-1426">Az.Aks</span></span>
* <span data-ttu-id="411c6-1427">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="411c6-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1428">Az.Automation</span></span>
* <span data-ttu-id="411c6-1429">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="411c6-1430">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="411c6-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="411c6-1431">Az.Cdn</span></span>
* <span data-ttu-id="411c6-1432">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1433">Az.Compute</span></span>
* <span data-ttu-id="411c6-1434">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="411c6-1435">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="411c6-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="411c6-1436">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="411c6-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="411c6-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="411c6-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="411c6-1438">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="411c6-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="411c6-1439">Az.DataFactory</span></span>
* <span data-ttu-id="411c6-1440">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="411c6-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1442">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="411c6-1443">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="411c6-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="411c6-1444">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-1445">Az.IotHub</span></span>
* <span data-ttu-id="411c6-1446">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="411c6-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="411c6-1447">Az.KeyVault</span></span>
* <span data-ttu-id="411c6-1448">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1449">Az.Network</span></span>
* <span data-ttu-id="411c6-1450">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1451">Az.Resources</span></span>
* <span data-ttu-id="411c6-1452">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="411c6-1453">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="411c6-1454">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="411c6-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="411c6-1455">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="411c6-1456">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="411c6-1457">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="411c6-1458">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="411c6-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-1460">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="411c6-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="411c6-1461">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="411c6-1461">Fix some error messages.</span></span>
* <span data-ttu-id="411c6-1462">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="411c6-1463">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="411c6-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="411c6-1464">Az.SignalR</span></span>
* <span data-ttu-id="411c6-1465">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1466">Az.Sql</span></span>
* <span data-ttu-id="411c6-1467">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="411c6-1468">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="411c6-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="411c6-1469">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="411c6-1470">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="411c6-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1471">Az.Storage</span></span>
* <span data-ttu-id="411c6-1472">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="411c6-1473">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="411c6-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="411c6-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="411c6-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="411c6-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="411c6-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="411c6-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="411c6-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="411c6-1477">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1478">Az.Websites</span></span>
* <span data-ttu-id="411c6-1479">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="411c6-1480">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="411c6-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="411c6-1481">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="411c6-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="411c6-1482">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="411c6-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1483">Az.Accounts</span></span>
* <span data-ttu-id="411c6-1484">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="411c6-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1485">Az.Compute</span></span>
* <span data-ttu-id="411c6-1486">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="411c6-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="411c6-1487">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="411c6-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="411c6-1488">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1490">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="411c6-1491">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="411c6-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="411c6-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="411c6-1492">Az.EventGrid</span></span>
* <span data-ttu-id="411c6-1493">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="411c6-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="411c6-1494">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="411c6-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="411c6-1495">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="411c6-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="411c6-1496">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="411c6-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="411c6-1497">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="411c6-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="411c6-1498">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="411c6-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="411c6-1499">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="411c6-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="411c6-1500">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="411c6-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="411c6-1501">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="411c6-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="411c6-1502">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="411c6-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="411c6-1503">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="411c6-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="411c6-1504">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="411c6-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="411c6-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="411c6-1505">Az.IotHub</span></span>
* <span data-ttu-id="411c6-1506">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="411c6-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="411c6-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="411c6-1507">Az.LogicApp</span></span>
* <span data-ttu-id="411c6-1508">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1509">Az.Resources</span></span>
* <span data-ttu-id="411c6-1510">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="411c6-1511">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="411c6-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="411c6-1512">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="411c6-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="411c6-1513">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="411c6-1514">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="411c6-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="411c6-1515">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="411c6-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="411c6-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="411c6-1516">Az.SignalR</span></span>
* <span data-ttu-id="411c6-1517">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1518">Az.Sql</span></span>
* <span data-ttu-id="411c6-1519">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="411c6-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="411c6-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1520">Az.Storage</span></span>
* <span data-ttu-id="411c6-1521">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="411c6-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="411c6-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="411c6-1523">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="411c6-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="411c6-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="411c6-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1525">Az.Websites</span></span>
* <span data-ttu-id="411c6-1526">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="411c6-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="411c6-1527">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="411c6-1528">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="411c6-1529">一般</span><span class="sxs-lookup"><span data-stu-id="411c6-1529">General</span></span>

- <span data-ttu-id="411c6-1530">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="411c6-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="411c6-1531">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="411c6-1531">Online help for each module</span></span>
- <span data-ttu-id="411c6-1532">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="411c6-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="411c6-1533">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="411c6-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1534">Az.Accounts</span></span>
- <span data-ttu-id="411c6-1535">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="411c6-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="411c6-1536">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="411c6-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="411c6-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="411c6-1538">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="411c6-1538">Fixes for #7002</span></span>
- <span data-ttu-id="411c6-1539">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="411c6-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="411c6-1540">Az.Batch</span></span>
- <span data-ttu-id="411c6-1541">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="411c6-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="411c6-1542">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="411c6-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="411c6-1543">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="411c6-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="411c6-1544">Az.Billing</span></span>
- <span data-ttu-id="411c6-1545">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="411c6-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="411c6-1547">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="411c6-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="411c6-1548">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="411c6-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="411c6-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="411c6-1550">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="411c6-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="411c6-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="411c6-1552">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="411c6-1554">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="411c6-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="411c6-1555">Az.Monitor</span></span>
- <span data-ttu-id="411c6-1556">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="411c6-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="411c6-1557">Az.KeyVault</span></span>
- <span data-ttu-id="411c6-1558">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="411c6-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="411c6-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="411c6-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="411c6-1560">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="411c6-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="411c6-1561">Az.Media</span></span>
- <span data-ttu-id="411c6-1562">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="411c6-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="411c6-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1563">Az.Network</span></span>
<span data-ttu-id="411c6-1564">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="411c6-1565">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="411c6-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="411c6-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="411c6-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="411c6-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="411c6-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="411c6-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="411c6-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="411c6-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="411c6-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="411c6-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="411c6-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c6-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="411c6-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="411c6-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="411c6-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="411c6-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="411c6-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="411c6-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="411c6-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="411c6-1580">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="411c6-1581">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="411c6-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="411c6-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="411c6-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="411c6-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="411c6-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="411c6-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="411c6-1585">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="411c6-1586">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="411c6-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="411c6-1588">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="411c6-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="411c6-1589">Az.Profile</span></span>
- <span data-ttu-id="411c6-1590">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="411c6-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="411c6-1592">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="411c6-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1593">Az.Resources</span></span>
- <span data-ttu-id="411c6-1594">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="411c6-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="411c6-1596">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="411c6-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="411c6-1597">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="411c6-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="411c6-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="411c6-1599">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="411c6-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="411c6-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1600">Az.Sql</span></span>
- <span data-ttu-id="411c6-1601">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="411c6-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="411c6-1602">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="411c6-1603">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="411c6-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1604">Az.Storage</span></span>
- <span data-ttu-id="411c6-1605">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="411c6-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1606">Az.Websites</span></span>
- <span data-ttu-id="411c6-1607">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="411c6-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="411c6-1608">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="411c6-1609">一般</span><span class="sxs-lookup"><span data-stu-id="411c6-1609">General</span></span>

* <span data-ttu-id="411c6-1610">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="411c6-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="411c6-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1611">Az.Compute</span></span>

* <span data-ttu-id="411c6-1612">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="411c6-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="411c6-1614">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="411c6-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="411c6-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="411c6-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="411c6-1616">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="411c6-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="411c6-1617">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="411c6-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="411c6-1618">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="411c6-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="411c6-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="411c6-1620">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="411c6-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="411c6-1621">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="411c6-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="411c6-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1622">Az.Resources</span></span>

* <span data-ttu-id="411c6-1623">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="411c6-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="411c6-1624">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="411c6-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="411c6-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1625">Az.Sql</span></span>

* <span data-ttu-id="411c6-1626">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="411c6-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="411c6-1627">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="411c6-1628">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="411c6-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="411c6-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1629">Az.Storage</span></span>

* <span data-ttu-id="411c6-1630">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="411c6-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="411c6-1631">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="411c6-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="411c6-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="411c6-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="411c6-1633">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="411c6-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="411c6-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="411c6-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="411c6-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="411c6-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="411c6-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1636">Az.Websites</span></span>

* <span data-ttu-id="411c6-1637">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="411c6-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="411c6-1638">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="411c6-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="411c6-1639">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="411c6-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="411c6-1640">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="411c6-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="411c6-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="411c6-1642">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="411c6-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="411c6-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="411c6-1643">Az.Automation</span></span>
* <span data-ttu-id="411c6-1644">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="411c6-1645">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="411c6-1646">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="411c6-1647">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="411c6-1648">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="411c6-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="411c6-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1649">Az.Compute</span></span>
* <span data-ttu-id="411c6-1650">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="411c6-1651">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="411c6-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="411c6-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="411c6-1653">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="411c6-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="411c6-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="411c6-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="411c6-1655">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="411c6-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="411c6-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1656">Az.Network</span></span>
* <span data-ttu-id="411c6-1657">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="411c6-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="411c6-1658">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="411c6-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="411c6-1659">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="411c6-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="411c6-1660">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="411c6-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="411c6-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="411c6-1662">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="411c6-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="411c6-1663">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="411c6-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="411c6-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="411c6-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="411c6-1665">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="411c6-1666">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="411c6-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="411c6-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="411c6-1667">Az.Relay</span></span>
* <span data-ttu-id="411c6-1668">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="411c6-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="411c6-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1669">Az.Resources</span></span>
* <span data-ttu-id="411c6-1670">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="411c6-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="411c6-1671">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="411c6-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="411c6-1672">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="411c6-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="411c6-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-1674">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="411c6-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="411c6-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1675">Az.Sql</span></span>
* <span data-ttu-id="411c6-1676">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="411c6-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="411c6-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="411c6-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="411c6-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="411c6-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="411c6-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="411c6-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="411c6-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="411c6-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="411c6-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="411c6-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="411c6-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="411c6-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="411c6-1685">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="411c6-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="411c6-1686">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="411c6-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="411c6-1687">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="411c6-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="411c6-1688">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="411c6-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="411c6-1689">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="411c6-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="411c6-1690">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="411c6-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="411c6-1691">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="411c6-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="411c6-1692">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="411c6-1693">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="411c6-1694">一般</span><span class="sxs-lookup"><span data-stu-id="411c6-1694">General</span></span>
* <span data-ttu-id="411c6-1695">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="411c6-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="411c6-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="411c6-1696">Az.Profile</span></span>
* <span data-ttu-id="411c6-1697">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="411c6-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="411c6-1698">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="411c6-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="411c6-1699">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="411c6-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="411c6-1700">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="411c6-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="411c6-1701">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="411c6-1702">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="411c6-1703">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="411c6-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="411c6-1705">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="411c6-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1706">Az.Compute</span></span>
* <span data-ttu-id="411c6-1707">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="411c6-1708">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="411c6-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="411c6-1709">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1711">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="411c6-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="411c6-1712">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="411c6-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="411c6-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="411c6-1713">Az.Insights</span></span>
* <span data-ttu-id="411c6-1714">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="411c6-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="411c6-1715">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="411c6-1716">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="411c6-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="411c6-1717">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="411c6-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1718">Az.Network</span></span>
* <span data-ttu-id="411c6-1719">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="411c6-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="411c6-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="411c6-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="411c6-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="411c6-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="411c6-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="411c6-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="411c6-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="411c6-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="411c6-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="411c6-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="411c6-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="411c6-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="411c6-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="411c6-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="411c6-1727">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1728">Az.Resources</span></span>
* <span data-ttu-id="411c6-1729">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="411c6-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="411c6-1730">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="411c6-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="411c6-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="411c6-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="411c6-1732">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="411c6-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="411c6-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="411c6-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="411c6-1734">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="411c6-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="411c6-1735">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="411c6-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="411c6-1736">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="411c6-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="411c6-1737">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="411c6-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="411c6-1738">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="411c6-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="411c6-1739">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="411c6-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="411c6-1740">Az.Profile</span></span>
* <span data-ttu-id="411c6-1741">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="411c6-1742">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="411c6-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1743">Az.Compute</span></span>
* <span data-ttu-id="411c6-1744">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="411c6-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="411c6-1745">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="411c6-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="411c6-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="411c6-1747">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="411c6-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="411c6-1748">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="411c6-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="411c6-1749">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="411c6-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="411c6-1750">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="411c6-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="411c6-1751">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="411c6-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1752">Az.Network</span></span>
* <span data-ttu-id="411c6-1753">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="411c6-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="411c6-1754">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="411c6-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1755">Az.Resources</span></span>
* <span data-ttu-id="411c6-1756">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="411c6-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="411c6-1757">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="411c6-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="411c6-1758">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="411c6-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="411c6-1759">Azure.Storage</span></span>
* <span data-ttu-id="411c6-1760">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="411c6-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="411c6-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="411c6-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="411c6-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="411c6-1763">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="411c6-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="411c6-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="411c6-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="411c6-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="411c6-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="411c6-1766">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="411c6-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="411c6-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="411c6-1767">Az.Compute</span></span>
* <span data-ttu-id="411c6-1768">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="411c6-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="411c6-1769">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="411c6-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="411c6-1770">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="411c6-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="411c6-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="411c6-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="411c6-1772">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="411c6-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="411c6-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="411c6-1773">Az.Network</span></span>
* <span data-ttu-id="411c6-1774">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="411c6-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="411c6-1775">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1775">new cmdlets added</span></span>
    - <span data-ttu-id="411c6-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="411c6-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="411c6-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="411c6-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="411c6-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="411c6-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="411c6-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="411c6-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="411c6-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="411c6-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="411c6-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="411c6-1782">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="411c6-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="411c6-1783">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="411c6-1784">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="411c6-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="411c6-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="411c6-1785">Az.RedisCache</span></span>
* <span data-ttu-id="411c6-1786">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="411c6-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="411c6-1787">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="411c6-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="411c6-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="411c6-1788">Az.Resources</span></span>
* <span data-ttu-id="411c6-1789">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="411c6-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="411c6-1790">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="411c6-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="411c6-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="411c6-1791">Az.Sql</span></span>
* <span data-ttu-id="411c6-1792">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="411c6-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="411c6-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="411c6-1793">Az.Websites</span></span>
* <span data-ttu-id="411c6-1794">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="411c6-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="411c6-1795">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="411c6-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="411c6-1796">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="411c6-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="411c6-1797">初始版本</span><span class="sxs-lookup"><span data-stu-id="411c6-1797">Initial Release</span></span>
