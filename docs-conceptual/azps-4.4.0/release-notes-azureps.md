---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/14/2020
ms.locfileid: "86381814"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="11b0c-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="11b0c-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="11b0c-104">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-105">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-106">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="11b0c-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="11b0c-107">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="11b0c-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="11b0c-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11b0c-108">Az.Aks</span></span>
* <span data-ttu-id="11b0c-109">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="11b0c-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11b0c-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="11b0c-111">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="11b0c-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-112">Az.Automation</span></span>
* <span data-ttu-id="11b0c-113">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-114">Az.Compute</span></span>
* <span data-ttu-id="11b0c-115">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="11b0c-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-116">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-117">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="11b0c-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11b0c-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11b0c-118">Az.EventGrid</span></span>
* <span data-ttu-id="11b0c-119">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="11b0c-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="11b0c-120">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="11b0c-120">Added new features:</span></span>
    - <span data-ttu-id="11b0c-121">輸入對應</span><span class="sxs-lookup"><span data-stu-id="11b0c-121">Input mapping</span></span>
    - <span data-ttu-id="11b0c-122">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="11b0c-123">私人連結</span><span class="sxs-lookup"><span data-stu-id="11b0c-123">Private Link</span></span>
    - <span data-ttu-id="11b0c-124">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="11b0c-125">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="11b0c-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="11b0c-126">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="11b0c-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="11b0c-127">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-127">WebHook Batching</span></span>
    - <span data-ttu-id="11b0c-128">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="11b0c-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="11b0c-129">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="11b0c-129">IpFiltering</span></span>
* <span data-ttu-id="11b0c-130">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="11b0c-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="11b0c-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="11b0c-132">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="11b0c-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="11b0c-133">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="11b0c-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="11b0c-134">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="11b0c-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="11b0c-135">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="11b0c-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="11b0c-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="11b0c-137">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="11b0c-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="11b0c-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="11b0c-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="11b0c-139">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="11b0c-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-140">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-141">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="11b0c-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="11b0c-142">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-143">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-144">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="11b0c-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-145">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-146">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="11b0c-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-147">Az.Network</span></span>
* <span data-ttu-id="11b0c-148">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="11b0c-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="11b0c-149">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="11b0c-150">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="11b0c-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="11b0c-151">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="11b0c-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="11b0c-152">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="11b0c-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="11b0c-153">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="11b0c-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="11b0c-154">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="11b0c-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="11b0c-155">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="11b0c-156">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="11b0c-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="11b0c-157">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="11b0c-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="11b0c-158">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="11b0c-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="11b0c-159">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="11b0c-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="11b0c-160">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="11b0c-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="11b0c-161">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="11b0c-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="11b0c-162">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="11b0c-163">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="11b0c-164">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-166">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="11b0c-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="11b0c-167">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="11b0c-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="11b0c-168">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-169">Az.Resources</span></span>
* <span data-ttu-id="11b0c-170">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="11b0c-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="11b0c-171">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-172">Az.Sql</span></span>
* <span data-ttu-id="11b0c-173">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="11b0c-174">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="11b0c-175">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="11b0c-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-176">Az.Storage</span></span>
* <span data-ttu-id="11b0c-177">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="11b0c-178">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="11b0c-179">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="11b0c-180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="11b0c-181">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="11b0c-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="11b0c-182">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="11b0c-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="11b0c-183">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="11b0c-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="11b0c-184">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="11b0c-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="11b0c-185">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="11b0c-186">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="11b0c-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="11b0c-187">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="11b0c-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="11b0c-188">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="11b0c-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="11b0c-189">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="11b0c-190">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="11b0c-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="11b0c-191">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="11b0c-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="11b0c-192">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="11b0c-193">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="11b0c-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11b0c-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11b0c-194">Az.StorageSync</span></span>
* <span data-ttu-id="11b0c-195">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="11b0c-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="11b0c-196">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="11b0c-197">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="11b0c-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="11b0c-198">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-199">Az.Websites</span></span>
* <span data-ttu-id="11b0c-200">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="11b0c-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="11b0c-201">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-202">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-203">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="11b0c-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="11b0c-204">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="11b0c-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="11b0c-205">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="11b0c-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="11b0c-206">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="11b0c-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="11b0c-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11b0c-207">Az.Aks</span></span>
* <span data-ttu-id="11b0c-208">透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="11b0c-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-209">Az.Batch</span></span>
* <span data-ttu-id="11b0c-210">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="11b0c-211">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-213">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="11b0c-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="11b0c-214">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="11b0c-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-215">Az.Compute</span></span>
* <span data-ttu-id="11b0c-216">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="11b0c-217">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="11b0c-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="11b0c-218">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="11b0c-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="11b0c-219">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="11b0c-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="11b0c-220">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-221">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-222">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-223">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-224">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="11b0c-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="11b0c-225">Az.Functions</span></span>
* <span data-ttu-id="11b0c-226">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-227">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-228">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="11b0c-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="11b0c-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="11b0c-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="11b0c-230">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="11b0c-231">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-232">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-233">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="11b0c-234">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="11b0c-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-235">Az.Network</span></span>
* <span data-ttu-id="11b0c-236">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="11b0c-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="11b0c-237">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="11b0c-238">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="11b0c-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="11b0c-239">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="11b0c-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="11b0c-240">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="11b0c-241">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="11b0c-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="11b0c-242">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="11b0c-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="11b0c-243">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="11b0c-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="11b0c-244">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="11b0c-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="11b0c-245">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="11b0c-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="11b0c-246">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="11b0c-247">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="11b0c-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="11b0c-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="11b0c-249">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="11b0c-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="11b0c-250">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="11b0c-251">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="11b0c-252">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="11b0c-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="11b0c-253">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="11b0c-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="11b0c-254">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="11b0c-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="11b0c-255">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="11b0c-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="11b0c-256">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="11b0c-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="11b0c-257">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="11b0c-258">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="11b0c-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="11b0c-259">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="11b0c-260">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="11b0c-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="11b0c-261">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="11b0c-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="11b0c-262">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="11b0c-263">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="11b0c-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="11b0c-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="11b0c-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="11b0c-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="11b0c-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="11b0c-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="11b0c-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="11b0c-270">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="11b0c-271">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="11b0c-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="11b0c-272">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="11b0c-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="11b0c-273">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="11b0c-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="11b0c-274">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="11b0c-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="11b0c-275">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="11b0c-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="11b0c-276">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="11b0c-277">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="11b0c-278">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="11b0c-279">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="11b0c-280">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="11b0c-281">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="11b0c-282">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="11b0c-283">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="11b0c-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="11b0c-284">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="11b0c-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-286">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="11b0c-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="11b0c-287">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="11b0c-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="11b0c-288">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="11b0c-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="11b0c-289">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="11b0c-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="11b0c-290">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="11b0c-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-292">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="11b0c-293">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="11b0c-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-294">Az.Resources</span></span>
* <span data-ttu-id="11b0c-295">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="11b0c-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="11b0c-296">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="11b0c-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="11b0c-297">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="11b0c-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="11b0c-298">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="11b0c-299">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="11b0c-300">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-301">Az.Sql</span></span>
* <span data-ttu-id="11b0c-302">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="11b0c-303">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="11b0c-304">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="11b0c-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-305">Az.Storage</span></span>
* <span data-ttu-id="11b0c-306">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="11b0c-307">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="11b0c-308">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-309">Az.Websites</span></span>
* <span data-ttu-id="11b0c-310">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="11b0c-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="11b0c-311">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="11b0c-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="11b0c-312">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="11b0c-313">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="11b0c-314">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="11b0c-315">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="11b0c-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="11b0c-316">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-317">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-318">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="11b0c-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11b0c-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="11b0c-320">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-321">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-322">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="11b0c-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11b0c-323">Az.Billing</span></span>
* <span data-ttu-id="11b0c-324">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-326">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="11b0c-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-327">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-328">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="11b0c-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-329">Az.DataShare</span></span>
* <span data-ttu-id="11b0c-330">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="11b0c-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="11b0c-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="11b0c-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="11b0c-332">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="11b0c-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-334">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="11b0c-335">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="11b0c-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="11b0c-336">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="11b0c-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="11b0c-337">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="11b0c-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-339">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="11b0c-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="11b0c-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="11b0c-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="11b0c-341">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="11b0c-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="11b0c-342">Az.PrivateDns</span></span>
* <span data-ttu-id="11b0c-343">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="11b0c-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-345">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="11b0c-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="11b0c-346">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-347">Az.Resources</span></span>
* <span data-ttu-id="11b0c-348">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="11b0c-349">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="11b0c-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="11b0c-350">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="11b0c-351">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="11b0c-352">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-353">Az.Sql</span></span>
* <span data-ttu-id="11b0c-354">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="11b0c-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="11b0c-355">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="11b0c-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="11b0c-356">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-357">Az.Storage</span></span>
* <span data-ttu-id="11b0c-358">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="11b0c-359">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="11b0c-360">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-360">Highlights since the last release</span></span>
* <span data-ttu-id="11b0c-361">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="11b0c-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="11b0c-362">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="11b0c-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="11b0c-363">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-364">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-365">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="11b0c-366">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="11b0c-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="11b0c-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11b0c-367">Az.Aks</span></span>
* <span data-ttu-id="11b0c-368">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="11b0c-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="11b0c-369">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="11b0c-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="11b0c-370">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="11b0c-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-371">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-372">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="11b0c-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="11b0c-373">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="11b0c-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="11b0c-374">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="11b0c-375">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="11b0c-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="11b0c-376">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="11b0c-377">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="11b0c-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="11b0c-378">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="11b0c-379">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="11b0c-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="11b0c-380">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="11b0c-381">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="11b0c-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="11b0c-382">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="11b0c-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="11b0c-383">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="11b0c-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="11b0c-384">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="11b0c-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="11b0c-385">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="11b0c-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="11b0c-386">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="11b0c-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="11b0c-387">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="11b0c-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="11b0c-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="11b0c-389">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="11b0c-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="11b0c-390">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="11b0c-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="11b0c-391">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-392">Az.Batch</span></span>
* <span data-ttu-id="11b0c-393">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="11b0c-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="11b0c-394">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="11b0c-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="11b0c-395">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="11b0c-396">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="11b0c-397">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="11b0c-398">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="11b0c-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="11b0c-399">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="11b0c-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="11b0c-400">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="11b0c-401">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-402">Az.Compute</span></span>
* <span data-ttu-id="11b0c-403">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="11b0c-404">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="11b0c-405">重大變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-405">Breaking changes</span></span>
    - <span data-ttu-id="11b0c-406">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="11b0c-407">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="11b0c-408">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="11b0c-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="11b0c-409">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="11b0c-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="11b0c-410">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="11b0c-411">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="11b0c-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="11b0c-412">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="11b0c-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-413">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-414">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="11b0c-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-415">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-416">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="11b0c-417">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="11b0c-418">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="11b0c-419">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="11b0c-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="11b0c-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="11b0c-420">Az.Functions</span></span>
* <span data-ttu-id="11b0c-421">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="11b0c-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-422">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-423">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="11b0c-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="11b0c-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="11b0c-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="11b0c-425">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="11b0c-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-426">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-427">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="11b0c-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="11b0c-428">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="11b0c-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="11b0c-429">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="11b0c-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="11b0c-430">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="11b0c-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="11b0c-431">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="11b0c-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="11b0c-432">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-432">New cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-433">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="11b0c-434">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="11b0c-435">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="11b0c-436">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="11b0c-437">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="11b0c-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="11b0c-438">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="11b0c-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-439">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-440">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="11b0c-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="11b0c-441">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="11b0c-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="11b0c-442">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="11b0c-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="11b0c-443">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="11b0c-444">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="11b0c-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="11b0c-445">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="11b0c-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="11b0c-446">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="11b0c-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-447">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-448">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="11b0c-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="11b0c-449">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="11b0c-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="11b0c-450">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="11b0c-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="11b0c-451">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="11b0c-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="11b0c-452">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="11b0c-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="11b0c-453">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="11b0c-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="11b0c-454">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="11b0c-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-455">Az.Network</span></span>
* <span data-ttu-id="11b0c-456">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="11b0c-457">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="11b0c-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="11b0c-458">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="11b0c-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="11b0c-459">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="11b0c-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="11b0c-460">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="11b0c-461">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-461">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-462">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="11b0c-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="11b0c-463">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="11b0c-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="11b0c-464">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="11b0c-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="11b0c-465">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="11b0c-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="11b0c-466">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="11b0c-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="11b0c-467">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="11b0c-468">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="11b0c-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="11b0c-469">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="11b0c-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="11b0c-470">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="11b0c-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="11b0c-471">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="11b0c-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="11b0c-472">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="11b0c-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="11b0c-473">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="11b0c-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="11b0c-474">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="11b0c-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="11b0c-475">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="11b0c-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="11b0c-476">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="11b0c-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="11b0c-477">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="11b0c-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="11b0c-478">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="11b0c-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="11b0c-479">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="11b0c-480">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="11b0c-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-482">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="11b0c-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="11b0c-483">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="11b0c-484">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="11b0c-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="11b0c-485">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="11b0c-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="11b0c-486">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="11b0c-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="11b0c-487">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="11b0c-488">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="11b0c-489">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-491">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="11b0c-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="11b0c-492">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="11b0c-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="11b0c-493">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="11b0c-494">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="11b0c-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="11b0c-495">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="11b0c-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-496">Az.Resources</span></span>
* <span data-ttu-id="11b0c-497">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="11b0c-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="11b0c-498">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="11b0c-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="11b0c-499">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="11b0c-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="11b0c-500">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="11b0c-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="11b0c-501">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="11b0c-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="11b0c-502">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="11b0c-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="11b0c-503">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="11b0c-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="11b0c-504">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="11b0c-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="11b0c-505">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="11b0c-506">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="11b0c-507">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="11b0c-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="11b0c-508">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="11b0c-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="11b0c-509">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="11b0c-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="11b0c-510">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="11b0c-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="11b0c-511">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="11b0c-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="11b0c-512">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="11b0c-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="11b0c-513">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="11b0c-514">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="11b0c-515">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="11b0c-516">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="11b0c-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-518">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="11b0c-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-519">Az.Sql</span></span>
* <span data-ttu-id="11b0c-520">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="11b0c-520">Enhance performance of:</span></span>
    - <span data-ttu-id="11b0c-521">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="11b0c-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="11b0c-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="11b0c-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="11b0c-523">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="11b0c-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="11b0c-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="11b0c-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="11b0c-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="11b0c-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="11b0c-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="11b0c-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="11b0c-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="11b0c-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="11b0c-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="11b0c-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="11b0c-529">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="11b0c-530">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="11b0c-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-531">Az.Storage</span></span>
* <span data-ttu-id="11b0c-532">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="11b0c-533">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="11b0c-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="11b0c-534">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="11b0c-535">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="11b0c-536">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="11b0c-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="11b0c-537">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="11b0c-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="11b0c-538">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="11b0c-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="11b0c-539">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="11b0c-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="11b0c-540">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="11b0c-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="11b0c-541">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="11b0c-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="11b0c-542">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="11b0c-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="11b0c-543">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="11b0c-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="11b0c-544">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="11b0c-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="11b0c-545">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="11b0c-546">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="11b0c-547">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="11b0c-548">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="11b0c-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="11b0c-549">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="11b0c-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="11b0c-550">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="11b0c-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="11b0c-551">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="11b0c-552">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="11b0c-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="11b0c-553">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="11b0c-554">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="11b0c-555">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="11b0c-556">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="11b0c-557">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="11b0c-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="11b0c-558">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="11b0c-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="11b0c-559">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="11b0c-560">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="11b0c-561">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="11b0c-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="11b0c-562">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="11b0c-563">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="11b0c-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="11b0c-564">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="11b0c-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="11b0c-565">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="11b0c-566">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="11b0c-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="11b0c-567">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="11b0c-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="11b0c-568">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="11b0c-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="11b0c-569">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="11b0c-570">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="11b0c-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="11b0c-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="11b0c-571">Az.TrafficManager</span></span>
* <span data-ttu-id="11b0c-572">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-573">Az.Websites</span></span>
* <span data-ttu-id="11b0c-574">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="11b0c-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="11b0c-575">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="11b0c-576">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-576">Highlights since the last release</span></span>
* <span data-ttu-id="11b0c-577">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="11b0c-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-578">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-579">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="11b0c-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-580">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-581">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="11b0c-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="11b0c-582">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-583">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-584">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="11b0c-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-586">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="11b0c-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-587">Az.Compute</span></span>
* <span data-ttu-id="11b0c-588">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="11b0c-589">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="11b0c-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-590">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-591">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-592">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="11b0c-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="11b0c-593">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="11b0c-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="11b0c-594">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="11b0c-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="11b0c-595">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-596">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="11b0c-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="11b0c-597">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="11b0c-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="11b0c-598">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="11b0c-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="11b0c-599">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-599">New cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-600">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="11b0c-601">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="11b0c-602">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="11b0c-603">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="11b0c-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="11b0c-604">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="11b0c-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-605">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-606">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="11b0c-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="11b0c-607">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="11b0c-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="11b0c-608">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="11b0c-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="11b0c-609">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="11b0c-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="11b0c-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="11b0c-610">Az.Maintenance</span></span>
* <span data-ttu-id="11b0c-611">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-612">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-613">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="11b0c-614">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="11b0c-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="11b0c-615">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="11b0c-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="11b0c-616">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="11b0c-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="11b0c-617">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="11b0c-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="11b0c-618">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="11b0c-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="11b0c-619">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="11b0c-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="11b0c-620">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="11b0c-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-621">Az.Network</span></span>
* <span data-ttu-id="11b0c-622">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="11b0c-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="11b0c-623">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="11b0c-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="11b0c-624">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="11b0c-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="11b0c-625">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="11b0c-626">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="11b0c-627">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="11b0c-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="11b0c-628">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="11b0c-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="11b0c-629">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="11b0c-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="11b0c-630">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="11b0c-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="11b0c-631">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="11b0c-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="11b0c-632">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="11b0c-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="11b0c-633">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="11b0c-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="11b0c-634">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="11b0c-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="11b0c-635">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="11b0c-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="11b0c-636">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="11b0c-637">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-639">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="11b0c-640">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="11b0c-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-642">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="11b0c-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-643">Az.Sql</span></span>
* <span data-ttu-id="11b0c-644">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="11b0c-645">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="11b0c-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-646">Az.Storage</span></span>
* <span data-ttu-id="11b0c-647">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="11b0c-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="11b0c-648">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="11b0c-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="11b0c-649">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="11b0c-650">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="11b0c-651">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="11b0c-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="11b0c-652">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="11b0c-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="11b0c-653">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="11b0c-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="11b0c-654">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="11b0c-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="11b0c-655">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="11b0c-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="11b0c-656">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="11b0c-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="11b0c-657">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="11b0c-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="11b0c-658">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="11b0c-659">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="11b0c-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="11b0c-660">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="11b0c-661">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-661">General</span></span>
* <span data-ttu-id="11b0c-662">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="11b0c-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="11b0c-663">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="11b0c-664">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="11b0c-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="11b0c-665">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="11b0c-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="11b0c-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11b0c-666">Az.Billing</span></span>
  - <span data-ttu-id="11b0c-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-667">Az.Compute</span></span>
  - <span data-ttu-id="11b0c-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="11b0c-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="11b0c-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-669">Az.EventHub</span></span>
  - <span data-ttu-id="11b0c-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-670">Az.IotHub</span></span>
  - <span data-ttu-id="11b0c-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-671">Az.KeyVault</span></span>
  - <span data-ttu-id="11b0c-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-672">Az.Monitor</span></span>
  - <span data-ttu-id="11b0c-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-673">Az.Network</span></span>
  - <span data-ttu-id="11b0c-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-674">Az.Resources</span></span>
  - <span data-ttu-id="11b0c-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-675">Az.Storage</span></span>
  - <span data-ttu-id="11b0c-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-676">Az.Websites</span></span>
* <span data-ttu-id="11b0c-677">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="11b0c-678">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="11b0c-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="11b0c-679">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="11b0c-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="11b0c-680">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-681">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-682">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="11b0c-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-683">Az.Compute</span></span>
* <span data-ttu-id="11b0c-684">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="11b0c-685">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="11b0c-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="11b0c-686">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="11b0c-687">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="11b0c-688">[#11354]</span><span class="sxs-lookup"><span data-stu-id="11b0c-688">[#11354]</span></span>
* <span data-ttu-id="11b0c-689">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="11b0c-690">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="11b0c-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="11b0c-691">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="11b0c-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="11b0c-692">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="11b0c-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="11b0c-693">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="11b0c-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="11b0c-694">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="11b0c-695">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="11b0c-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="11b0c-696">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="11b0c-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="11b0c-697">[#11257]</span><span class="sxs-lookup"><span data-stu-id="11b0c-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-698">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-699">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="11b0c-700">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="11b0c-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-702">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="11b0c-703">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="11b0c-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-704">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-705">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="11b0c-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-706">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-707">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="11b0c-708">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-709">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="11b0c-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="11b0c-710">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="11b0c-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-711">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-712">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="11b0c-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-713">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-714">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-715">Az.Network</span></span>
* <span data-ttu-id="11b0c-716">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="11b0c-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="11b0c-717">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="11b0c-718">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="11b0c-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="11b0c-719">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="11b0c-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="11b0c-720">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="11b0c-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="11b0c-721">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="11b0c-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-723">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-725">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="11b0c-726">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="11b0c-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="11b0c-727">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="11b0c-728">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="11b0c-729">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="11b0c-730">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-731">Az.Resources</span></span>
* <span data-ttu-id="11b0c-732">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="11b0c-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="11b0c-733">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="11b0c-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="11b0c-734">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="11b0c-735">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-735">Added example.</span></span>
* <span data-ttu-id="11b0c-736">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="11b0c-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="11b0c-737">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-738">Az.Sql</span></span>
* <span data-ttu-id="11b0c-739">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="11b0c-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="11b0c-740">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="11b0c-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="11b0c-741">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="11b0c-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="11b0c-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="11b0c-742">Az.Support</span></span>
* <span data-ttu-id="11b0c-743">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="11b0c-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-744">Az.Websites</span></span>
* <span data-ttu-id="11b0c-745">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="11b0c-746">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="11b0c-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="11b0c-747">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="11b0c-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="11b0c-748">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="11b0c-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="11b0c-749">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="11b0c-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="11b0c-750">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-751">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-752">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="11b0c-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="11b0c-753">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="11b0c-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="11b0c-754">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-755">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-756">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="11b0c-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="11b0c-757">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="11b0c-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="11b0c-758">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="11b0c-759">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="11b0c-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-761">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="11b0c-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-762">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-763">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="11b0c-764">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-765">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="11b0c-766">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="11b0c-767">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="11b0c-768">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="11b0c-769">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="11b0c-770">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-771">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="11b0c-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="11b0c-772">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="11b0c-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="11b0c-773">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="11b0c-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="11b0c-774">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="11b0c-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="11b0c-775">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="11b0c-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="11b0c-776">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="11b0c-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="11b0c-777">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="11b0c-778">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-779">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="11b0c-780">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="11b0c-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="11b0c-781">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-782">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-783">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="11b0c-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-784">Az.Network</span></span>
* <span data-ttu-id="11b0c-785">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="11b0c-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="11b0c-786">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="11b0c-787">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="11b0c-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="11b0c-788">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-789">Az.Resources</span></span>
* <span data-ttu-id="11b0c-790">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="11b0c-791">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="11b0c-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="11b0c-792">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="11b0c-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="11b0c-793">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="11b0c-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="11b0c-794">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="11b0c-795">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="11b0c-796">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="11b0c-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="11b0c-797">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b0c-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="11b0c-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b0c-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="11b0c-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b0c-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="11b0c-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b0c-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="11b0c-801">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="11b0c-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b0c-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="11b0c-803">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="11b0c-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-804">Az.Sql</span></span>
* <span data-ttu-id="11b0c-805">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="11b0c-806">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="11b0c-807">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="11b0c-808">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="11b0c-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="11b0c-809">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="11b0c-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="11b0c-810">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="11b0c-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="11b0c-811">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="11b0c-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="11b0c-812">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="11b0c-813">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-814">Az.Storage</span></span>
* <span data-ttu-id="11b0c-815">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="11b0c-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="11b0c-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="11b0c-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="11b0c-817">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="11b0c-818">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="11b0c-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="11b0c-819">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="11b0c-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-820">Az.Websites</span></span>
* <span data-ttu-id="11b0c-821">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="11b0c-822">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="11b0c-823">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="11b0c-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="11b0c-824">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="11b0c-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="11b0c-825">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="11b0c-826">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11b0c-827">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-827">Highlights since the last major release</span></span>
* <span data-ttu-id="11b0c-828">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="11b0c-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="11b0c-829">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="11b0c-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="11b0c-830">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-831">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-832">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="11b0c-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-833">Az.Automation</span></span>
* <span data-ttu-id="11b0c-834">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-836">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="11b0c-837">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-838">Az.Compute</span></span>
* <span data-ttu-id="11b0c-839">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="11b0c-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-840">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-841">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="11b0c-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-842">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-843">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="11b0c-844">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-845">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="11b0c-846">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="11b0c-847">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="11b0c-848">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="11b0c-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-849">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-850">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="11b0c-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-851">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-852">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="11b0c-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="11b0c-853">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="11b0c-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="11b0c-854">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-855">Az.Network</span></span>
* <span data-ttu-id="11b0c-856">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="11b0c-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="11b0c-857">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="11b0c-858">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="11b0c-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="11b0c-859">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="11b0c-860">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-860">No new cmdlets are added.</span></span> <span data-ttu-id="11b0c-861">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="11b0c-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-863">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-864">Az.Resources</span></span>
* <span data-ttu-id="11b0c-865">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="11b0c-866">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="11b0c-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="11b0c-867">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="11b0c-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="11b0c-868">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="11b0c-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="11b0c-869">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="11b0c-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="11b0c-870">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="11b0c-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="11b0c-871">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="11b0c-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="11b0c-872">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="11b0c-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-873">Az.Sql</span></span>
* <span data-ttu-id="11b0c-874">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="11b0c-875">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="11b0c-876">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="11b0c-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="11b0c-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="11b0c-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="11b0c-878">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11b0c-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11b0c-879">Az.StorageSync</span></span>
* <span data-ttu-id="11b0c-880">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="11b0c-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="11b0c-881">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11b0c-882">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-882">Highlights since the last major release</span></span>
* <span data-ttu-id="11b0c-883">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="11b0c-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="11b0c-884">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="11b0c-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-885">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-886">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="11b0c-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="11b0c-887">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="11b0c-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-888">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-889">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="11b0c-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="11b0c-890">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="11b0c-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="11b0c-891">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="11b0c-892">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="11b0c-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-893">Az.Compute</span></span>
* <span data-ttu-id="11b0c-894">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="11b0c-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="11b0c-895">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="11b0c-896">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="11b0c-897">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="11b0c-898">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-899">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-900">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="11b0c-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="11b0c-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="11b0c-902">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="11b0c-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="11b0c-903">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-904">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-905">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="11b0c-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-906">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-907">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="11b0c-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-908">Az.Network</span></span>
* <span data-ttu-id="11b0c-909">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="11b0c-910">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="11b0c-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="11b0c-911">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="11b0c-912">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="11b0c-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="11b0c-913">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="11b0c-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="11b0c-914">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="11b0c-915">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="11b0c-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="11b0c-916">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="11b0c-917">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-917">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b0c-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="11b0c-919">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="11b0c-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="11b0c-921">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-923">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="11b0c-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="11b0c-924">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="11b0c-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="11b0c-925">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="11b0c-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="11b0c-926">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="11b0c-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-928">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="11b0c-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="11b0c-929">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-930">Az.Resources</span></span>
* <span data-ttu-id="11b0c-931">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="11b0c-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="11b0c-932">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-933">Az.Sql</span></span>
<span data-ttu-id="11b0c-934">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="11b0c-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-935">Az.Storage</span></span>
* <span data-ttu-id="11b0c-936">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="11b0c-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="11b0c-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="11b0c-938">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="11b0c-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="11b0c-939">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="11b0c-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-940">Az.Websites</span></span>
* <span data-ttu-id="11b0c-941">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="11b0c-942">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="11b0c-943">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-944">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-945">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-946">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-947">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="11b0c-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-948">Az.Compute</span></span>
* <span data-ttu-id="11b0c-949">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="11b0c-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="11b0c-951">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="11b0c-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="11b0c-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="11b0c-953">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="11b0c-954">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="11b0c-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="11b0c-955">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="11b0c-956">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="11b0c-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="11b0c-957">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="11b0c-958">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="11b0c-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="11b0c-959">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="11b0c-960">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="11b0c-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="11b0c-961">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="11b0c-962">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="11b0c-963">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="11b0c-964">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="11b0c-965">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="11b0c-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="11b0c-966">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="11b0c-967">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="11b0c-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="11b0c-968">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="11b0c-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="11b0c-969">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="11b0c-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="11b0c-970">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="11b0c-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-971">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-972">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="11b0c-973">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="11b0c-974">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="11b0c-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="11b0c-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="11b0c-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="11b0c-976">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="11b0c-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-977">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-978">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="11b0c-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-979">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-980">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="11b0c-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="11b0c-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11b0c-981">Az.MachineLearning</span></span>
* <span data-ttu-id="11b0c-982">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="11b0c-983">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="11b0c-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="11b0c-984">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="11b0c-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="11b0c-985">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="11b0c-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="11b0c-986">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="11b0c-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="11b0c-987">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="11b0c-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="11b0c-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="11b0c-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="11b0c-989">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="11b0c-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-990">Az.Network</span></span>
* <span data-ttu-id="11b0c-991">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="11b0c-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-993">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="11b0c-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="11b0c-994">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="11b0c-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="11b0c-995">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="11b0c-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="11b0c-996">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="11b0c-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-997">Az.Resources</span></span>
* <span data-ttu-id="11b0c-998">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="11b0c-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-999">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1000">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="11b0c-1001">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="11b0c-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="11b0c-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="11b0c-1003">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1004">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1005">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="11b0c-1006">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="11b0c-1007">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="11b0c-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="11b0c-1008">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="11b0c-1009">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="11b0c-1010">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-1010">General</span></span>
* <span data-ttu-id="11b0c-1011">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="11b0c-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1012">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1013">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="11b0c-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="11b0c-1014">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-1015">Az.Batch</span></span>
* <span data-ttu-id="11b0c-1016">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1017">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1018">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-1020">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="11b0c-1021">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="11b0c-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="11b0c-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="11b0c-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="11b0c-1023">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-1024">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-1025">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="11b0c-1026">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="11b0c-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="11b0c-1027">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1028">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-1029">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="11b0c-1030">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="11b0c-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="11b0c-1031">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1032">Az.Network</span></span>
* <span data-ttu-id="11b0c-1033">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1034">Az.Resources</span></span>
* <span data-ttu-id="11b0c-1035">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="11b0c-1036">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1037">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1038">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="11b0c-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1039">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1040">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="11b0c-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="11b0c-1041">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="11b0c-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="11b0c-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="11b0c-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="11b0c-1043">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="11b0c-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="11b0c-1044">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="11b0c-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="11b0c-1045">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="11b0c-1046">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="11b0c-1047">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="11b0c-1048">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="11b0c-1049">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="11b0c-1050">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="11b0c-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="11b0c-1051">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="11b0c-1052">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="11b0c-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="11b0c-1053">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11b0c-1054">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="11b0c-1055">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="11b0c-1056">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1057">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1058">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="11b0c-1059">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="11b0c-1060">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="11b0c-1061">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11b0c-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="11b0c-1062">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="11b0c-1063">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="11b0c-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="11b0c-1064">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="11b0c-1065">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="11b0c-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="11b0c-1066">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="11b0c-1067">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="11b0c-1068">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="11b0c-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="11b0c-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="11b0c-1070">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="11b0c-1071">取得訂單</span><span class="sxs-lookup"><span data-stu-id="11b0c-1071">Get the Order</span></span>
* <span data-ttu-id="11b0c-1072">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="11b0c-1073">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="11b0c-1073">Create new Order</span></span>
* <span data-ttu-id="11b0c-1074">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="11b0c-1075">移除訂單</span><span class="sxs-lookup"><span data-stu-id="11b0c-1075">Remove the Order</span></span>
* <span data-ttu-id="11b0c-1076">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="11b0c-1077">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="11b0c-1077">Now creates Local Share</span></span>
* <span data-ttu-id="11b0c-1078">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="11b0c-1079">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="11b0c-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="11b0c-1080">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="11b0c-1081">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="11b0c-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="11b0c-1082">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="11b0c-1083">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="11b0c-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="11b0c-1084">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="11b0c-1085">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="11b0c-1085">Create new Triggers</span></span>
* <span data-ttu-id="11b0c-1086">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="11b0c-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="11b0c-1087">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="11b0c-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1088">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1089">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="11b0c-1090">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-1092">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1093">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-1094">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="11b0c-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-1096">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="11b0c-1097">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="11b0c-1098">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="11b0c-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="11b0c-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1100">Az.Network</span></span>
* <span data-ttu-id="11b0c-1101">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="11b0c-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="11b0c-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="11b0c-1103">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="11b0c-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1105">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="11b0c-1106">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="11b0c-1107">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="11b0c-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11b0c-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11b0c-1108">Az.RedisCache</span></span>
* <span data-ttu-id="11b0c-1109">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="11b0c-1110">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="11b0c-1111">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1112">Az.Resources</span></span>
- <span data-ttu-id="11b0c-1113">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="11b0c-1114">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="11b0c-1115">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="11b0c-1116">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="11b0c-1117">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1118">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1119">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="11b0c-1120">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="11b0c-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="11b0c-1121">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="11b0c-1122">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-1122">General</span></span>
* <span data-ttu-id="11b0c-1123">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1124">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1125">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="11b0c-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1126">Az.Advisor</span></span>
* <span data-ttu-id="11b0c-1127">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-1128">Az.Batch</span></span>
* <span data-ttu-id="11b0c-1129">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="11b0c-1130">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="11b0c-1131">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="11b0c-1132">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="11b0c-1133">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="11b0c-1134">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="11b0c-1135">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="11b0c-1136">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="11b0c-1137">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="11b0c-1138">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="11b0c-1139">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="11b0c-1140">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="11b0c-1141">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="11b0c-1142">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="11b0c-1143">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="11b0c-1144">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="11b0c-1145">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="11b0c-1146">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="11b0c-1147">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="11b0c-1148">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="11b0c-1149">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="11b0c-1150">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="11b0c-1151">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="11b0c-1152">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="11b0c-1153">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="11b0c-1154">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="11b0c-1155">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="11b0c-1156">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="11b0c-1157">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="11b0c-1158">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="11b0c-1159">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="11b0c-1160">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="11b0c-1161">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="11b0c-1162">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="11b0c-1163">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="11b0c-1164">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-1165">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-1166">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="11b0c-1167">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1168">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1169">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="11b0c-1170">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="11b0c-1171">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="11b0c-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="11b0c-1172">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11b0c-1173">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="11b0c-1174">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="11b0c-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="11b0c-1175">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="11b0c-1176">重大變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-1176">Breaking changes</span></span>
    - <span data-ttu-id="11b0c-1177">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="11b0c-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="11b0c-1178">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="11b0c-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1179">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1180">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-1182">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="11b0c-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="11b0c-1183">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="11b0c-1184">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="11b0c-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="11b0c-1185">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="11b0c-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="11b0c-1186">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="11b0c-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="11b0c-1187">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-1189">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-1190">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-1191">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="11b0c-1192">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="11b0c-1193">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="11b0c-1194">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="11b0c-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="11b0c-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="11b0c-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="11b0c-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="11b0c-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="11b0c-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="11b0c-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11b0c-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="11b0c-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11b0c-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="11b0c-1200">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="11b0c-1201">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="11b0c-1202">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="11b0c-1203">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="11b0c-1204">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="11b0c-1205">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="11b0c-1206">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="11b0c-1207">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="11b0c-1208">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="11b0c-1209">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="11b0c-1210">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="11b0c-1211">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="11b0c-1212">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="11b0c-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1213">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-1214">重大變更：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1214">Breaking changes:</span></span>
    - <span data-ttu-id="11b0c-1215">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11b0c-1216">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="11b0c-1217">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11b0c-1218">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="11b0c-1219">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="11b0c-1220">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="11b0c-1221">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="11b0c-1222">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="11b0c-1223">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11b0c-1224">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="11b0c-1225">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11b0c-1226">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1228">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-1229">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="11b0c-1230">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="11b0c-1231">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-1232">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-1233">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-1234">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-1235">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-1236">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="11b0c-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1237">Az.Resources</span></span>
* <span data-ttu-id="11b0c-1238">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="11b0c-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1239">Az.Network</span></span>
* <span data-ttu-id="11b0c-1240">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="11b0c-1241">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="11b0c-1242">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1243">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1244">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1245">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="11b0c-1247">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="11b0c-1248">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1248">New cmdlet:</span></span>
        - <span data-ttu-id="11b0c-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="11b0c-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="11b0c-1250">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="11b0c-1251">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="11b0c-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="11b0c-1252">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="11b0c-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="11b0c-1253">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="11b0c-1254">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="11b0c-1255">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="11b0c-1256">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="11b0c-1257">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="11b0c-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="11b0c-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="11b0c-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="11b0c-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="11b0c-1263">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="11b0c-1264">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11b0c-1265">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="11b0c-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="11b0c-1266">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="11b0c-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="11b0c-1267">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="11b0c-1268">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="11b0c-1269">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="11b0c-1270">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="11b0c-1272">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11b0c-1273">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="11b0c-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11b0c-1274">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="11b0c-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11b0c-1275">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="11b0c-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11b0c-1276">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="11b0c-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11b0c-1277">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="11b0c-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="11b0c-1278">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="11b0c-1279">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="11b0c-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="11b0c-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="11b0c-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="11b0c-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="11b0c-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="11b0c-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="11b0c-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="11b0c-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="11b0c-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="11b0c-1286">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11b0c-1287">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="11b0c-1288">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="11b0c-1289">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="11b0c-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="11b0c-1290">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="11b0c-1291">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11b0c-1292">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="11b0c-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="11b0c-1293">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="11b0c-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="11b0c-1294">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="11b0c-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="11b0c-1295">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="11b0c-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="11b0c-1296">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="11b0c-1297">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="11b0c-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="11b0c-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="11b0c-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-1303">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1304">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1305">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="11b0c-1306">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="11b0c-1307">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="11b0c-1308">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="11b0c-1309">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="11b0c-1310">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="11b0c-1311">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="11b0c-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="11b0c-1312">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="11b0c-1313">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1314">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1315">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="11b0c-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="11b0c-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="11b0c-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="11b0c-1318">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="11b0c-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="11b0c-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11b0c-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="11b0c-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11b0c-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="11b0c-1321">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="11b0c-1322">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-1322">General</span></span>
* <span data-ttu-id="11b0c-1323">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1324">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1325">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-1327">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="11b0c-1328">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-1329">Az.Automation</span></span>
* <span data-ttu-id="11b0c-1330">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-1331">Az.Batch</span></span>
* <span data-ttu-id="11b0c-1332">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1333">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1334">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="11b0c-1335">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="11b0c-1336">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="11b0c-1337">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1338">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1339">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="11b0c-1340">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="11b0c-1341">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-1343">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="11b0c-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="11b0c-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="11b0c-1345">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="11b0c-1346">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="11b0c-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="11b0c-1347">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="11b0c-1348">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1349">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-1350">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="11b0c-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="11b0c-1351">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="11b0c-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1352">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-1353">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="11b0c-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="11b0c-1354">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="11b0c-1355">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="11b0c-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="11b0c-1356">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1357">Az.Network</span></span>
* <span data-ttu-id="11b0c-1358">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="11b0c-1359">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="11b0c-1360">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-1361">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="11b0c-1362">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="11b0c-1363">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="11b0c-1364">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="11b0c-1365">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11b0c-1366">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11b0c-1367">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="11b0c-1368">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="11b0c-1369">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="11b0c-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="11b0c-1370">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="11b0c-1371">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11b0c-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11b0c-1372">Az.RedisCache</span></span>
* <span data-ttu-id="11b0c-1373">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="11b0c-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1374">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1375">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1376">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1377">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="11b0c-1378">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="11b0c-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="11b0c-1379">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="11b0c-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="11b0c-1380">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="11b0c-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="11b0c-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11b0c-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11b0c-1382">Az.StorageSync</span></span>
* <span data-ttu-id="11b0c-1383">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-1384">Az.Websites</span></span>
* <span data-ttu-id="11b0c-1385">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="11b0c-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="11b0c-1386">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-1388">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="11b0c-1389">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="11b0c-1390">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-1391">Az.Automation</span></span>
* <span data-ttu-id="11b0c-1392">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="11b0c-1393">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="11b0c-1394">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1395">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1396">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="11b0c-1397">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11b0c-1398">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="11b0c-1399">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="11b0c-1400">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="11b0c-1401">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="11b0c-1402">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="11b0c-1403">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="11b0c-1404">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1405">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1406">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="11b0c-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="11b0c-1407">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="11b0c-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-1408">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-1409">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1410">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-1411">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="11b0c-1412">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="11b0c-1413">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="11b0c-1414">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11b0c-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11b0c-1415">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11b0c-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11b0c-1416">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11b0c-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11b0c-1417">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11b0c-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1418">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-1419">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="11b0c-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="11b0c-1420">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="11b0c-1421">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="11b0c-1422">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="11b0c-1423">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="11b0c-1424">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="11b0c-1425">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="11b0c-1426">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="11b0c-1427">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="11b0c-1428">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="11b0c-1429">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="11b0c-1430">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="11b0c-1431">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="11b0c-1432">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="11b0c-1433">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="11b0c-1434">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="11b0c-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="11b0c-1435">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="11b0c-1436">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="11b0c-1437">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="11b0c-1438">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="11b0c-1438">Overall improved help files</span></span>
* <span data-ttu-id="11b0c-1439">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1440">Az.Network</span></span>
* <span data-ttu-id="11b0c-1441">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="11b0c-1442">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="11b0c-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="11b0c-1443">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="11b0c-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="11b0c-1444">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="11b0c-1445">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="11b0c-1446">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="11b0c-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="11b0c-1447">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="11b0c-1448">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="11b0c-1449">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="11b0c-1450">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="11b0c-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="11b0c-1451">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="11b0c-1452">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="11b0c-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="11b0c-1453">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1453">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-1454">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="11b0c-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="11b0c-1455">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="11b0c-1456">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="11b0c-1457">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="11b0c-1457">New-VpnSite</span></span>
        - <span data-ttu-id="11b0c-1458">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="11b0c-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="11b0c-1459">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="11b0c-1460">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="11b0c-1461">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1463">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="11b0c-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="11b0c-1464">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="11b0c-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1465">Az.Resources</span></span>
* <span data-ttu-id="11b0c-1466">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-1468">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="11b0c-1469">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="11b0c-1470">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11b0c-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11b0c-1471">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11b0c-1472">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11b0c-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11b0c-1473">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="11b0c-1474">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11b0c-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11b0c-1475">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11b0c-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11b0c-1476">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11b0c-1477">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11b0c-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11b0c-1478">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="11b0c-1479">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11b0c-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11b0c-1480">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11b0c-1481">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11b0c-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11b0c-1482">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="11b0c-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="11b0c-1483">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11b0c-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11b0c-1484">Az.SignalR</span></span>
* <span data-ttu-id="11b0c-1485">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1486">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1487">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="11b0c-1488">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="11b0c-1489">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="11b0c-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="11b0c-1490">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="11b0c-1491">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1492">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1493">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="11b0c-1494">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="11b0c-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="11b0c-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="11b0c-1497">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="11b0c-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="11b0c-1499">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="11b0c-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="11b0c-1500">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11b0c-1501">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11b0c-1502">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11b0c-1503">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11b0c-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-1504">Az.Websites</span></span>
* <span data-ttu-id="11b0c-1505">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="11b0c-1506">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="11b0c-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="11b0c-1507">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="11b0c-1508">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="11b0c-1509">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-1509">General</span></span>
* <span data-ttu-id="11b0c-1510">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1511">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1512">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="11b0c-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11b0c-1513">Az.Aks</span></span>
* <span data-ttu-id="11b0c-1514">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="11b0c-1515">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="11b0c-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-1517">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="11b0c-1518">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="11b0c-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="11b0c-1519">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="11b0c-1520">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="11b0c-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="11b0c-1521">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-1522">Az.Batch</span></span>
* <span data-ttu-id="11b0c-1523">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="11b0c-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-1524">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-1525">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1526">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1527">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="11b0c-1528">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="11b0c-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="11b0c-1529">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="11b0c-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="11b0c-1530">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="11b0c-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="11b0c-1531">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="11b0c-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="11b0c-1532">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="11b0c-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="11b0c-1533">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="11b0c-1534">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1535">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1536">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="11b0c-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="11b0c-1537">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="11b0c-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="11b0c-1538">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="11b0c-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="11b0c-1539">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-1541">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1542">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-1543">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="11b0c-1544">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="11b0c-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="11b0c-1545">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="11b0c-1546">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="11b0c-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="11b0c-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="11b0c-1548">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1549">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-1550">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1551">Az.Network</span></span>
* <span data-ttu-id="11b0c-1552">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="11b0c-1553">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="11b0c-1554">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="11b0c-1555">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="11b0c-1556">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="11b0c-1557">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="11b0c-1558">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-1560">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="11b0c-1561">新增了範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1561">Added example</span></span>
    - <span data-ttu-id="11b0c-1562">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="11b0c-1563">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="11b0c-1564">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1566">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1567">Az.Resources</span></span>
* <span data-ttu-id="11b0c-1568">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="11b0c-1569">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="11b0c-1570">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="11b0c-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="11b0c-1571">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11b0c-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11b0c-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="11b0c-1573">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="11b0c-1574">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="11b0c-1575">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="11b0c-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-1577">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="11b0c-1578">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="11b0c-1579">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="11b0c-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="11b0c-1580">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="11b0c-1581">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="11b0c-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="11b0c-1582">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1583">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1584">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1585">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1586">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="11b0c-1587">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="11b0c-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="11b0c-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="11b0c-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11b0c-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="11b0c-1590">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="11b0c-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="11b0c-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11b0c-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-1592">Az.Websites</span></span>
* <span data-ttu-id="11b0c-1593">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="11b0c-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="11b0c-1594">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1595">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1596">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11b0c-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="11b0c-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="11b0c-1598">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-1599">Az.Automation</span></span>
* <span data-ttu-id="11b0c-1600">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-1602">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1603">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1604">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="11b0c-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="11b0c-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="11b0c-1606">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="11b0c-1607">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="11b0c-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1608">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1609">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="11b0c-1610">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1611">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-1612">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="11b0c-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="11b0c-1613">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-1614">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-1615">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11b0c-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11b0c-1616">Az.LogicApp</span></span>
* <span data-ttu-id="11b0c-1617">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="11b0c-1618">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="11b0c-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="11b0c-1620">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1621">Az.Network</span></span>
* <span data-ttu-id="11b0c-1622">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="11b0c-1623">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1623">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-1624">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11b0c-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11b0c-1625">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11b0c-1626">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1627">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1628">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1629">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11b0c-1630">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="11b0c-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="11b0c-1631">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="11b0c-1632">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="11b0c-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="11b0c-1633">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="11b0c-1634">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="11b0c-1635">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="11b0c-1636">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="11b0c-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="11b0c-1637">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="11b0c-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="11b0c-1638">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="11b0c-1639">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11b0c-1640">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11b0c-1641">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="11b0c-1642">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="11b0c-1643">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="11b0c-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="11b0c-1644">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="11b0c-1645">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="11b0c-1646">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="11b0c-1647">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="11b0c-1648">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="11b0c-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="11b0c-1649">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="11b0c-1650">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-1652">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="11b0c-1653">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1655">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="11b0c-1656">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="11b0c-1657">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="11b0c-1658">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="11b0c-1659">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="11b0c-1660">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="11b0c-1661">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="11b0c-1662">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="11b0c-1663">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="11b0c-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="11b0c-1664">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1665">Az.Resources</span></span>
- <span data-ttu-id="11b0c-1666">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="11b0c-1667">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="11b0c-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11b0c-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11b0c-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="11b0c-1669">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="11b0c-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="11b0c-1670">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1671">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1672">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="11b0c-1673">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="11b0c-1674">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1675">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1676">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11b0c-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11b0c-1677">Az.StorageSync</span></span>
* <span data-ttu-id="11b0c-1678">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="11b0c-1679">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="11b0c-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-1680">Az.Websites</span></span>
* <span data-ttu-id="11b0c-1681">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="11b0c-1682">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="11b0c-1683">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="11b0c-1684">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1685">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1686">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="11b0c-1687">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="11b0c-1688">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="11b0c-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1689">Az.Advisor</span></span>
* <span data-ttu-id="11b0c-1690">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="11b0c-1691">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="11b0c-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-1693">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="11b0c-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="11b0c-1695">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="11b0c-1696">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="11b0c-1697">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="11b0c-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="11b0c-1699">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-1700">Az.Automation</span></span>
* <span data-ttu-id="11b0c-1701">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1702">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1703">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-1704">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-1705">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11b0c-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11b0c-1706">Az.EventGrid</span></span>
* <span data-ttu-id="11b0c-1707">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1708">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-1709">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1710">Az.Network</span></span>
* <span data-ttu-id="11b0c-1711">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="11b0c-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="11b0c-1712">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-1714">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="11b0c-1715">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="11b0c-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-1717">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1719">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="11b0c-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1720">Az.Resources</span></span>
    - <span data-ttu-id="11b0c-1721">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="11b0c-1722">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="11b0c-1723">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="11b0c-1724">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="11b0c-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11b0c-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11b0c-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="11b0c-1726">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="11b0c-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1727">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1728">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="11b0c-1729">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="11b0c-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11b0c-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11b0c-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11b0c-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11b0c-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11b0c-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11b0c-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11b0c-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="11b0c-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11b0c-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="11b0c-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11b0c-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="11b0c-1736">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="11b0c-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1737">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1738">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="11b0c-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11b0c-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="11b0c-1740">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="11b0c-1741">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="11b0c-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="11b0c-1742">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="11b0c-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="11b0c-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="11b0c-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="11b0c-1745">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="11b0c-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="11b0c-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11b0c-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="11b0c-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11b0c-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11b0c-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11b0c-1748">Az.StorageSync</span></span>
* <span data-ttu-id="11b0c-1749">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="11b0c-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="11b0c-1750">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-1751">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-1752">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="11b0c-1753">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="11b0c-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="11b0c-1754">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="11b0c-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11b0c-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="11b0c-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="11b0c-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1757">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1758">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="11b0c-1759">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="11b0c-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="11b0c-1760">Az.Dns</span></span>
* <span data-ttu-id="11b0c-1761">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11b0c-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11b0c-1762">Az.EventGrid</span></span>
* <span data-ttu-id="11b0c-1763">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="11b0c-1764">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1764">New cmdlets:</span></span>
    - <span data-ttu-id="11b0c-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11b0c-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11b0c-1766">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11b0c-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11b0c-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11b0c-1768">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="11b0c-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11b0c-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11b0c-1770">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11b0c-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="11b0c-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="11b0c-1772">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11b0c-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="11b0c-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="11b0c-1774">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="11b0c-1775">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="11b0c-1776">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="11b0c-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="11b0c-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="11b0c-1778">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="11b0c-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="11b0c-1779">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="11b0c-1780">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="11b0c-1781">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="11b0c-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="11b0c-1783">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="11b0c-1784">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="11b0c-1785">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="11b0c-1786">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="11b0c-1787">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="11b0c-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="11b0c-1788">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="11b0c-1789">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="11b0c-1790">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="11b0c-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="11b0c-1791">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="11b0c-1792">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="11b0c-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="11b0c-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="11b0c-1794">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="11b0c-1795">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="11b0c-1798">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="11b0c-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="11b0c-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="11b0c-1800">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="11b0c-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1801">Az.Network</span></span>
* <span data-ttu-id="11b0c-1802">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="11b0c-1803">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1803">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="11b0c-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="11b0c-1805">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="11b0c-1806">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1806">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="11b0c-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="11b0c-1808">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="11b0c-1809">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1809">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11b0c-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11b0c-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11b0c-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11b0c-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="11b0c-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="11b0c-1815">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11b0c-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="11b0c-1816">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1816">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11b0c-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11b0c-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11b0c-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11b0c-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11b0c-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11b0c-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="11b0c-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="11b0c-1821">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="11b0c-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="11b0c-1822">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="11b0c-1823">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="11b0c-1824">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="11b0c-1825">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="11b0c-1826">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="11b0c-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="11b0c-1827">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="11b0c-1828">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="11b0c-1829">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="11b0c-1830">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="11b0c-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="11b0c-1831">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="11b0c-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="11b0c-1832">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="11b0c-1833">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="11b0c-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="11b0c-1834">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="11b0c-1835">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="11b0c-1836">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="11b0c-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="11b0c-1837">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="11b0c-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="11b0c-1838">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="11b0c-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="11b0c-1839">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="11b0c-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="11b0c-1840">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="11b0c-1841">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="11b0c-1842">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="11b0c-1843">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-1845">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="11b0c-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1846">Az.Resources</span></span>
* <span data-ttu-id="11b0c-1847">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="11b0c-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="11b0c-1848">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="11b0c-1849">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="11b0c-1850">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="11b0c-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-1852">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1853">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1854">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="11b0c-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="11b0c-1855">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="11b0c-1856">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="11b0c-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="11b0c-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11b0c-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11b0c-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11b0c-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11b0c-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11b0c-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11b0c-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11b0c-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="11b0c-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11b0c-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-1862">Az.Storage</span></span>
* <span data-ttu-id="11b0c-1863">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="11b0c-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="11b0c-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="11b0c-1865">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="11b0c-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-1867">Az.Websites</span></span>
* <span data-ttu-id="11b0c-1868">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="11b0c-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="11b0c-1869">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="11b0c-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="11b0c-1870">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="11b0c-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-1871">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-1872">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1873">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1874">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="11b0c-1875">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="11b0c-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-1876">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-1877">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="11b0c-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="11b0c-1878">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b0c-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1879">Az.Network</span></span>
* <span data-ttu-id="11b0c-1880">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="11b0c-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="11b0c-1881">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="11b0c-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-1883">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-1885">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="11b0c-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11b0c-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11b0c-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="11b0c-1887">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b0c-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-1889">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="11b0c-1890">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="11b0c-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1891">Az.Sql</span></span>
* <span data-ttu-id="11b0c-1892">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="11b0c-1893">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="11b0c-1894">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="11b0c-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="11b0c-1895">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-1896">Az.Websites</span></span>
* <span data-ttu-id="11b0c-1897">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="11b0c-1898">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="11b0c-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-1900">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="11b0c-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="11b0c-1901">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="11b0c-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="11b0c-1902">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="11b0c-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="11b0c-1903">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="11b0c-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="11b0c-1904">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="11b0c-1905">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="11b0c-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="11b0c-1906">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="11b0c-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="11b0c-1907">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="11b0c-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="11b0c-1908">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="11b0c-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="11b0c-1909">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="11b0c-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="11b0c-1910">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="11b0c-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="11b0c-1911">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="11b0c-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="11b0c-1912">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="11b0c-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="11b0c-1913">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="11b0c-1914">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="11b0c-1915">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="11b0c-1916">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="11b0c-1917">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="11b0c-1918">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="11b0c-1919">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="11b0c-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="11b0c-1920">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="11b0c-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="11b0c-1921">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="11b0c-1922">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="11b0c-1923">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="11b0c-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="11b0c-1924">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="11b0c-1925">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="11b0c-1926">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="11b0c-1927">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="11b0c-1928">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="11b0c-1929">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="11b0c-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="11b0c-1930">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="11b0c-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="11b0c-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="11b0c-1932">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="11b0c-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="11b0c-1933">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11b0c-1934">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="11b0c-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="11b0c-1935">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="11b0c-1936">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="11b0c-1937">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="11b0c-1938">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="11b0c-1939">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11b0c-1940">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="11b0c-1941">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="11b0c-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="11b0c-1942">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="11b0c-1943">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="11b0c-1944">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11b0c-1945">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="11b0c-1946">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="11b0c-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="11b0c-1947">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="11b0c-1948">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="11b0c-1949">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="11b0c-1950">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="11b0c-1951">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="11b0c-1952">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="11b0c-1953">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="11b0c-1954">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="11b0c-1955">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="11b0c-1956">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="11b0c-1957">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="11b0c-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="11b0c-1958">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="11b0c-1959">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="11b0c-1960">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11b0c-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="11b0c-1961">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="11b0c-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="11b0c-1962">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="11b0c-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="11b0c-1963">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="11b0c-1964">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="11b0c-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="11b0c-1965">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="11b0c-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="11b0c-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="11b0c-1967">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="11b0c-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="11b0c-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="11b0c-1969">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="11b0c-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="11b0c-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="11b0c-1971">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="11b0c-1972">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="11b0c-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="11b0c-1974">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="11b0c-1975">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="11b0c-1976">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="11b0c-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-1977">Az.Automation</span></span>
* <span data-ttu-id="11b0c-1978">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="11b0c-1979">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="11b0c-1980">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="11b0c-1981">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="11b0c-1982">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="11b0c-1983">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="11b0c-1984">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-1985">Az.Compute</span></span>
* <span data-ttu-id="11b0c-1986">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="11b0c-1987">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="11b0c-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-1989">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="11b0c-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-1990">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-1991">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-1992">Az.Network</span></span>
* <span data-ttu-id="11b0c-1993">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="11b0c-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="11b0c-1994">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="11b0c-1995">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="11b0c-1996">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="11b0c-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-1997">Az.Resources</span></span>
* <span data-ttu-id="11b0c-1998">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="11b0c-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-1999">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2000">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="11b0c-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="11b0c-2001">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2002">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2003">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-2005">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="11b0c-2006">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2007">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2008">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="11b0c-2009">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="11b0c-2010">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="11b0c-2011">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="11b0c-2012">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="11b0c-2013">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11b0c-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="11b0c-2014">重大變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-2014">Breaking changes</span></span>
    - <span data-ttu-id="11b0c-2015">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="11b0c-2016">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="11b0c-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="11b0c-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="11b0c-2018">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="11b0c-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="11b0c-2019">Az.Dns</span></span>
* <span data-ttu-id="11b0c-2020">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="11b0c-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="11b0c-2021">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="11b0c-2022">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="11b0c-2024">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="11b0c-2025">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="11b0c-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-2026">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-2027">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="11b0c-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11b0c-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="11b0c-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11b0c-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="11b0c-2030">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11b0c-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="11b0c-2031">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="11b0c-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="11b0c-2032">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="11b0c-2033">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-2034">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-2035">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="11b0c-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="11b0c-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="11b0c-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="11b0c-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="11b0c-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="11b0c-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="11b0c-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="11b0c-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="11b0c-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="11b0c-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="11b0c-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="11b0c-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11b0c-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11b0c-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11b0c-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11b0c-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11b0c-2047">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="11b0c-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="11b0c-2048">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2049">Az.Network</span></span>
* <span data-ttu-id="11b0c-2050">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="11b0c-2051">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2051">New cmdlets</span></span>
        - <span data-ttu-id="11b0c-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11b0c-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="11b0c-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11b0c-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="11b0c-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11b0c-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="11b0c-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11b0c-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="11b0c-2056">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="11b0c-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="11b0c-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="11b0c-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="11b0c-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="11b0c-2059">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="11b0c-2060">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="11b0c-2061">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-2063">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="11b0c-2064">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="11b0c-2065">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-2067">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="11b0c-2068">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="11b0c-2069">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="11b0c-2070">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="11b0c-2071">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="11b0c-2072">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="11b0c-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="11b0c-2073">Az.Relay</span></span>
* <span data-ttu-id="11b0c-2074">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11b0c-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11b0c-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="11b0c-2076">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2077">Az.Storage</span></span>
* <span data-ttu-id="11b0c-2078">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="11b0c-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="11b0c-2079">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="11b0c-2080">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="11b0c-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="11b0c-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="11b0c-2082">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="11b0c-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="11b0c-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="11b0c-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="11b0c-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2086">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2087">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="11b0c-2088">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="11b0c-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="11b0c-2089">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11b0c-2090">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="11b0c-2091">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="11b0c-2092">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11b0c-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11b0c-2093">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11b0c-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11b0c-2094">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11b0c-2095">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11b0c-2096">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11b0c-2097">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2098">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2099">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="11b0c-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11b0c-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-2100">Az.Batch</span></span>
* <span data-ttu-id="11b0c-2101">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-2102">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-2103">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-2105">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2106">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2107">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="11b0c-2108">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11b0c-2109">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="11b0c-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-2110">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-2111">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-2113">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11b0c-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11b0c-2114">Az.EventGrid</span></span>
* <span data-ttu-id="11b0c-2115">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-2116">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-2117">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11b0c-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11b0c-2118">Az.HDInsight</span></span>
* <span data-ttu-id="11b0c-2119">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-2120">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-2121">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-2122">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-2123">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11b0c-2124">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="11b0c-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="11b0c-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11b0c-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="11b0c-2126">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="11b0c-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="11b0c-2127">Az.Media</span></span>
* <span data-ttu-id="11b0c-2128">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-2129">Az.Monitor</span></span>
  * <span data-ttu-id="11b0c-2130">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="11b0c-2131">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="11b0c-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="11b0c-2132">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="11b0c-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="11b0c-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11b0c-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="11b0c-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11b0c-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="11b0c-2135">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11b0c-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="11b0c-2136">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="11b0c-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2137">Az.Network</span></span>
* <span data-ttu-id="11b0c-2138">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11b0c-2139">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="11b0c-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="11b0c-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="11b0c-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="11b0c-2141">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-2143">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="11b0c-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="11b0c-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="11b0c-2145">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-2147">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11b0c-2148">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="11b0c-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="11b0c-2149">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="11b0c-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="11b0c-2150">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="11b0c-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11b0c-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11b0c-2151">Az.RedisCache</span></span>
* <span data-ttu-id="11b0c-2152">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2153">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2154">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="11b0c-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2155">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2156">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="11b0c-2157">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11b0c-2158">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="11b0c-2159">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="11b0c-2160">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="11b0c-2161">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="11b0c-2162">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="11b0c-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2163">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2164">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="11b0c-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="11b0c-2165">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11b0c-2166">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="11b0c-2167">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="11b0c-2168">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11b0c-2169">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="11b0c-2170">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="11b0c-2171">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11b0c-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11b0c-2172">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11b0c-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11b0c-2173">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11b0c-2174">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11b0c-2175">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11b0c-2176">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2177">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2178">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11b0c-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="11b0c-2180">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="11b0c-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="11b0c-2181">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-2182">Az.Automation</span></span>
* <span data-ttu-id="11b0c-2183">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="11b0c-2184">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="11b0c-2185">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2186">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2187">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11b0c-2188">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="11b0c-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="11b0c-2190">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="11b0c-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-2191">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-2192">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="11b0c-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="11b0c-2193">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2194">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2195">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="11b0c-2196">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="11b0c-2197">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="11b0c-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="11b0c-2198">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="11b0c-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="11b0c-2199">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="11b0c-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="11b0c-2200">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="11b0c-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2201">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2202">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2203">Az.Storage</span></span>
* <span data-ttu-id="11b0c-2204">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="11b0c-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11b0c-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="11b0c-2206">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="11b0c-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="11b0c-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="11b0c-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="11b0c-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="11b0c-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="11b0c-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="11b0c-2211">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="11b0c-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="11b0c-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="11b0c-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="11b0c-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11b0c-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="11b0c-2216">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11b0c-2217">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="11b0c-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="11b0c-2218">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="11b0c-2219">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11b0c-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11b0c-2220">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11b0c-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11b0c-2221">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11b0c-2222">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11b0c-2223">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11b0c-2224">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-2225">Az.Automation</span></span>
* <span data-ttu-id="11b0c-2226">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="11b0c-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="11b0c-2227">動態分組</span><span class="sxs-lookup"><span data-stu-id="11b0c-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="11b0c-2228">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="11b0c-2228">Pre-Post script</span></span>
    * <span data-ttu-id="11b0c-2229">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="11b0c-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2230">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2231">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="11b0c-2232">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-2233">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-2234">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2235">Az.Network</span></span>
* <span data-ttu-id="11b0c-2236">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="11b0c-2237">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="11b0c-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-2239">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="11b0c-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="11b0c-2240">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2241">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2242">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="11b0c-2243">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="11b0c-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2244">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2245">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2246">Az.Storage</span></span>
* <span data-ttu-id="11b0c-2247">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="11b0c-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="11b0c-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11b0c-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11b0c-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11b0c-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="11b0c-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="11b0c-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="11b0c-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="11b0c-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2254">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2255">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="11b0c-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="11b0c-2256">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2257">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2258">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="11b0c-2259">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-2260">Az.Automation</span></span>
* <span data-ttu-id="11b0c-2261">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="11b0c-2262">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="11b0c-2263">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="11b0c-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-2264">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-2265">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2266">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2267">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-2268">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-2269">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="11b0c-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11b0c-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11b0c-2270">Az.LogicApp</span></span>
* <span data-ttu-id="11b0c-2271">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="11b0c-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2272">Az.Network</span></span>
* <span data-ttu-id="11b0c-2273">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-2275">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="11b0c-2276">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="11b0c-2276">SDK Update</span></span>
* <span data-ttu-id="11b0c-2277">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="11b0c-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="11b0c-2278">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="11b0c-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2279">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2280">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="11b0c-2281">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="11b0c-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="11b0c-2282">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="11b0c-2283">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="11b0c-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="11b0c-2284">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="11b0c-2285">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="11b0c-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2286">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2287">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="11b0c-2288">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2289">Az.Storage</span></span>
* <span data-ttu-id="11b0c-2290">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0c-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="11b0c-2291">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="11b0c-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="11b0c-2293">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-2294">Az.Automation</span></span>
* <span data-ttu-id="11b0c-2295">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="11b0c-2296">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="11b0c-2297">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-2299">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2300">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2301">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="11b0c-2302">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="11b0c-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="11b0c-2303">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="11b0c-2304">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-2306">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11b0c-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-2307">Az.EventHub</span></span>
* <span data-ttu-id="11b0c-2308">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="11b0c-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-2309">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-2310">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="11b0c-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11b0c-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11b0c-2311">Az.LogicApp</span></span>
* <span data-ttu-id="11b0c-2312">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="11b0c-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="11b0c-2313">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="11b0c-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="11b0c-2314">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="11b0c-2315">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11b0c-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11b0c-2316">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11b0c-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11b0c-2317">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11b0c-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11b0c-2318">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11b0c-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="11b0c-2319">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="11b0c-2320">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b0c-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11b0c-2321">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b0c-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11b0c-2322">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b0c-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11b0c-2323">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b0c-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="11b0c-2324">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="11b0c-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11b0c-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-2325">Az.Monitor</span></span>
* <span data-ttu-id="11b0c-2326">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2327">Az.Network</span></span>
* <span data-ttu-id="11b0c-2328">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="11b0c-2330">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="11b0c-2331">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="11b0c-2332">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2333">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2334">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="11b0c-2335">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="11b0c-2336">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="11b0c-2337">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2338">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2339">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="11b0c-2340">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="11b0c-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2341">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2342">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="11b0c-2343">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2344">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2345">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11b0c-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11b0c-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="11b0c-2347">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2348">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2349">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="11b0c-2350">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="11b0c-2351">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="11b0c-2353">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2354">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2355">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="11b0c-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="11b0c-2356">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="11b0c-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="11b0c-2357">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="11b0c-2358">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="11b0c-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2359">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2360">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="11b0c-2361">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="11b0c-2362">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="11b0c-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="11b0c-2363">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2364">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2365">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="11b0c-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11b0c-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="11b0c-2367">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="11b0c-2369">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="11b0c-2370">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2371">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2372">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="11b0c-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11b0c-2373">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11b0c-2374">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="11b0c-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11b0c-2375">Az.Aks</span></span>
* <span data-ttu-id="11b0c-2376">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11b0c-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-2377">Az.Automation</span></span>
* <span data-ttu-id="11b0c-2378">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="11b0c-2379">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11b0c-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11b0c-2380">Az.Cdn</span></span>
* <span data-ttu-id="11b0c-2381">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2382">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2383">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="11b0c-2384">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11b0c-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="11b0c-2385">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="11b0c-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="11b0c-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="11b0c-2387">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11b0c-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11b0c-2388">Az.DataFactory</span></span>
* <span data-ttu-id="11b0c-2389">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="11b0c-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-2391">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="11b0c-2392">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="11b0c-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="11b0c-2393">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-2394">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-2395">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11b0c-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-2396">Az.KeyVault</span></span>
* <span data-ttu-id="11b0c-2397">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2398">Az.Network</span></span>
* <span data-ttu-id="11b0c-2399">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2400">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2401">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="11b0c-2402">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="11b0c-2403">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="11b0c-2404">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="11b0c-2405">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="11b0c-2406">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="11b0c-2407">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="11b0c-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-2409">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="11b0c-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="11b0c-2410">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2410">Fix some error messages.</span></span>
* <span data-ttu-id="11b0c-2411">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="11b0c-2412">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11b0c-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11b0c-2413">Az.SignalR</span></span>
* <span data-ttu-id="11b0c-2414">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2415">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2416">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11b0c-2417">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="11b0c-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="11b0c-2418">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="11b0c-2419">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="11b0c-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2420">Az.Storage</span></span>
* <span data-ttu-id="11b0c-2421">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11b0c-2422">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="11b0c-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="11b0c-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="11b0c-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="11b0c-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="11b0c-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="11b0c-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="11b0c-2426">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2427">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2428">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11b0c-2429">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="11b0c-2430">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="11b0c-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="11b0c-2431">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11b0c-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2432">Az.Accounts</span></span>
* <span data-ttu-id="11b0c-2433">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="11b0c-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2434">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2435">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="11b0c-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="11b0c-2436">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="11b0c-2437">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-2439">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="11b0c-2440">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="11b0c-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11b0c-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11b0c-2441">Az.EventGrid</span></span>
* <span data-ttu-id="11b0c-2442">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="11b0c-2443">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="11b0c-2444">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="11b0c-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="11b0c-2445">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="11b0c-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="11b0c-2446">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="11b0c-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="11b0c-2447">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="11b0c-2448">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="11b0c-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="11b0c-2449">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="11b0c-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="11b0c-2450">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="11b0c-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="11b0c-2451">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="11b0c-2452">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="11b0c-2453">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11b0c-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11b0c-2454">Az.IotHub</span></span>
* <span data-ttu-id="11b0c-2455">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="11b0c-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11b0c-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11b0c-2456">Az.LogicApp</span></span>
* <span data-ttu-id="11b0c-2457">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2458">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2459">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="11b0c-2460">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="11b0c-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="11b0c-2461">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="11b0c-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="11b0c-2462">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="11b0c-2463">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="11b0c-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="11b0c-2464">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="11b0c-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11b0c-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11b0c-2465">Az.SignalR</span></span>
* <span data-ttu-id="11b0c-2466">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2467">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2468">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11b0c-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2469">Az.Storage</span></span>
* <span data-ttu-id="11b0c-2470">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="11b0c-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11b0c-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="11b0c-2472">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="11b0c-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="11b0c-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="11b0c-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2474">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2475">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="11b0c-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="11b0c-2476">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="11b0c-2477">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="11b0c-2478">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-2478">General</span></span>

- <span data-ttu-id="11b0c-2479">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="11b0c-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="11b0c-2480">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-2480">Online help for each module</span></span>
- <span data-ttu-id="11b0c-2481">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="11b0c-2482">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="11b0c-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2483">Az.Accounts</span></span>
- <span data-ttu-id="11b0c-2484">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="11b0c-2485">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="11b0c-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="11b0c-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="11b0c-2487">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="11b0c-2487">Fixes for #7002</span></span>
- <span data-ttu-id="11b0c-2488">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="11b0c-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11b0c-2489">Az.Batch</span></span>
- <span data-ttu-id="11b0c-2490">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="11b0c-2491">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="11b0c-2492">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="11b0c-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11b0c-2493">Az.Billing</span></span>
- <span data-ttu-id="11b0c-2494">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="11b0c-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="11b0c-2496">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="11b0c-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="11b0c-2497">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="11b0c-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="11b0c-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="11b0c-2499">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="11b0c-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="11b0c-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="11b0c-2501">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="11b0c-2503">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="11b0c-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11b0c-2504">Az.Monitor</span></span>
- <span data-ttu-id="11b0c-2505">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="11b0c-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11b0c-2506">Az.KeyVault</span></span>
- <span data-ttu-id="11b0c-2507">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="11b0c-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11b0c-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="11b0c-2509">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="11b0c-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="11b0c-2510">Az.Media</span></span>
- <span data-ttu-id="11b0c-2511">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="11b0c-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="11b0c-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2512">Az.Network</span></span>
<span data-ttu-id="11b0c-2513">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="11b0c-2514">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11b0c-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="11b0c-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11b0c-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11b0c-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11b0c-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11b0c-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11b0c-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="11b0c-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="11b0c-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b0c-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="11b0c-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="11b0c-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11b0c-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="11b0c-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="11b0c-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="11b0c-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="11b0c-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="11b0c-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="11b0c-2529">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="11b0c-2530">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="11b0c-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11b0c-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="11b0c-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11b0c-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="11b0c-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11b0c-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="11b0c-2534">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="11b0c-2535">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="11b0c-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="11b0c-2537">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="11b0c-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2538">Az.Profile</span></span>
- <span data-ttu-id="11b0c-2539">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11b0c-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="11b0c-2541">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="11b0c-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2542">Az.Resources</span></span>
- <span data-ttu-id="11b0c-2543">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="11b0c-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="11b0c-2545">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="11b0c-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="11b0c-2546">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="11b0c-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="11b0c-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="11b0c-2548">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="11b0c-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="11b0c-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2549">Az.Sql</span></span>
- <span data-ttu-id="11b0c-2550">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="11b0c-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="11b0c-2551">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="11b0c-2552">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="11b0c-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2553">Az.Storage</span></span>
- <span data-ttu-id="11b0c-2554">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="11b0c-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2555">Az.Websites</span></span>
- <span data-ttu-id="11b0c-2556">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="11b0c-2557">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="11b0c-2558">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-2558">General</span></span>

* <span data-ttu-id="11b0c-2559">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="11b0c-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2560">Az.Compute</span></span>

* <span data-ttu-id="11b0c-2561">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="11b0c-2563">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="11b0c-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="11b0c-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11b0c-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="11b0c-2565">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="11b0c-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="11b0c-2566">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="11b0c-2567">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="11b0c-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="11b0c-2569">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="11b0c-2570">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="11b0c-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2571">Az.Resources</span></span>

* <span data-ttu-id="11b0c-2572">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="11b0c-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="11b0c-2573">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="11b0c-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2574">Az.Sql</span></span>

* <span data-ttu-id="11b0c-2575">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="11b0c-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="11b0c-2576">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="11b0c-2577">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="11b0c-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2578">Az.Storage</span></span>

* <span data-ttu-id="11b0c-2579">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="11b0c-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="11b0c-2580">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="11b0c-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="11b0c-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="11b0c-2582">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="11b0c-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="11b0c-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11b0c-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="11b0c-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11b0c-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="11b0c-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2585">Az.Websites</span></span>

* <span data-ttu-id="11b0c-2586">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="11b0c-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="11b0c-2587">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="11b0c-2588">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="11b0c-2589">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="11b0c-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11b0c-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="11b0c-2591">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="11b0c-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11b0c-2592">Az.Automation</span></span>
* <span data-ttu-id="11b0c-2593">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="11b0c-2594">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="11b0c-2595">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="11b0c-2596">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="11b0c-2597">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="11b0c-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="11b0c-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2598">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2599">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="11b0c-2600">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="11b0c-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="11b0c-2602">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="11b0c-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="11b0c-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="11b0c-2604">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="11b0c-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="11b0c-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2605">Az.Network</span></span>
* <span data-ttu-id="11b0c-2606">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="11b0c-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="11b0c-2607">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="11b0c-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="11b0c-2608">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="11b0c-2609">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="11b0c-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="11b0c-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="11b0c-2611">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="11b0c-2612">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="11b0c-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="11b0c-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="11b0c-2614">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="11b0c-2615">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="11b0c-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="11b0c-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="11b0c-2616">Az.Relay</span></span>
* <span data-ttu-id="11b0c-2617">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="11b0c-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2618">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2619">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="11b0c-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="11b0c-2620">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="11b0c-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="11b0c-2621">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="11b0c-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="11b0c-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-2623">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="11b0c-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="11b0c-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2624">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2625">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="11b0c-2626">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11b0c-2627">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11b0c-2628">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11b0c-2629">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11b0c-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11b0c-2630">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11b0c-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11b0c-2631">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11b0c-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11b0c-2632">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11b0c-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11b0c-2633">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11b0c-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="11b0c-2634">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="11b0c-2635">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="11b0c-2636">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="11b0c-2637">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="11b0c-2638">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="11b0c-2639">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="11b0c-2640">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="11b0c-2641">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="11b0c-2642">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="11b0c-2643">一般</span><span class="sxs-lookup"><span data-stu-id="11b0c-2643">General</span></span>
* <span data-ttu-id="11b0c-2644">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="11b0c-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="11b0c-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2645">Az.Profile</span></span>
* <span data-ttu-id="11b0c-2646">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11b0c-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="11b0c-2647">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="11b0c-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="11b0c-2648">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="11b0c-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="11b0c-2649">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="11b0c-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="11b0c-2650">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="11b0c-2651">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="11b0c-2652">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-2654">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2655">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2656">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="11b0c-2657">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="11b0c-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="11b0c-2658">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-2660">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="11b0c-2661">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="11b0c-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="11b0c-2662">Az.Insights</span></span>
* <span data-ttu-id="11b0c-2663">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="11b0c-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="11b0c-2664">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="11b0c-2665">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="11b0c-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="11b0c-2666">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="11b0c-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2667">Az.Network</span></span>
* <span data-ttu-id="11b0c-2668">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="11b0c-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="11b0c-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="11b0c-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="11b0c-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11b0c-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="11b0c-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="11b0c-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="11b0c-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="11b0c-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11b0c-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11b0c-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11b0c-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="11b0c-2676">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2677">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2678">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="11b0c-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="11b0c-2679">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="11b0c-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11b0c-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11b0c-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="11b0c-2681">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11b0c-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11b0c-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="11b0c-2683">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="11b0c-2684">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="11b0c-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="11b0c-2685">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="11b0c-2686">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="11b0c-2687">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="11b0c-2688">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="11b0c-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2689">Az.Profile</span></span>
* <span data-ttu-id="11b0c-2690">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="11b0c-2691">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11b0c-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2692">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2693">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="11b0c-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="11b0c-2694">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11b0c-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11b0c-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="11b0c-2696">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="11b0c-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="11b0c-2697">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="11b0c-2698">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="11b0c-2699">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="11b0c-2700">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2701">Az.Network</span></span>
* <span data-ttu-id="11b0c-2702">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="11b0c-2703">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2704">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2705">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="11b0c-2706">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="11b0c-2707">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="11b0c-2708">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2708">Azure.Storage</span></span>
* <span data-ttu-id="11b0c-2709">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="11b0c-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="11b0c-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11b0c-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="11b0c-2712">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="11b0c-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="11b0c-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11b0c-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11b0c-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="11b0c-2715">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11b0c-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11b0c-2716">Az.Compute</span></span>
* <span data-ttu-id="11b0c-2717">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="11b0c-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="11b0c-2718">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="11b0c-2719">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="11b0c-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="11b0c-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="11b0c-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="11b0c-2721">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11b0c-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11b0c-2722">Az.Network</span></span>
* <span data-ttu-id="11b0c-2723">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="11b0c-2724">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2724">new cmdlets added</span></span>
    - <span data-ttu-id="11b0c-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="11b0c-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="11b0c-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="11b0c-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11b0c-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="11b0c-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="11b0c-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="11b0c-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="11b0c-2731">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="11b0c-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="11b0c-2732">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="11b0c-2733">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b0c-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11b0c-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11b0c-2734">Az.RedisCache</span></span>
* <span data-ttu-id="11b0c-2735">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="11b0c-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="11b0c-2736">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="11b0c-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="11b0c-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11b0c-2737">Az.Resources</span></span>
* <span data-ttu-id="11b0c-2738">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11b0c-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="11b0c-2739">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="11b0c-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="11b0c-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11b0c-2740">Az.Sql</span></span>
* <span data-ttu-id="11b0c-2741">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="11b0c-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11b0c-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11b0c-2742">Az.Websites</span></span>
* <span data-ttu-id="11b0c-2743">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="11b0c-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="11b0c-2744">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="11b0c-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="11b0c-2745">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="11b0c-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="11b0c-2746">初始版本</span><span class="sxs-lookup"><span data-stu-id="11b0c-2746">Initial Release</span></span>
