---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 249780d2bfe53929b7c50cbdc8850a01fd9b53dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001890"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="24674-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="24674-103">Azure PowerShell release notes</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="24674-104">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="24674-104">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-105">Az.Accounts</span></span>
* <span data-ttu-id="24674-106">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="24674-106">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-107">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-107">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-108">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-108">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="24674-109">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-109">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-110">Az.Compute</span></span>
* <span data-ttu-id="24674-111">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="24674-111">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="24674-112">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-112">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="24674-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="24674-113">Az.Databricks</span></span>
* <span data-ttu-id="24674-114">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="24674-114">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="24674-115">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="24674-115">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-116">Az.DataFactory</span></span>
* <span data-ttu-id="24674-117">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-117">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-118">Az.EventHub</span></span>
* <span data-ttu-id="24674-119">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-119">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-120">Az.HDInsight</span></span>
* <span data-ttu-id="24674-121">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-121">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="24674-122">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-122">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="24674-123">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-123">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="24674-124">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-124">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="24674-125">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-125">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="24674-126">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-126">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-127">Az.IotHub</span></span>
* <span data-ttu-id="24674-128">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="24674-128">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-129">Az.KeyVault</span></span>
* <span data-ttu-id="24674-130">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="24674-130">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="24674-131">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="24674-131">Az.ManagedServices</span></span>
* <span data-ttu-id="24674-132">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="24674-132">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-133">Az.Monitor</span></span>
* <span data-ttu-id="24674-134">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-134">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="24674-135">[#12889]</span><span class="sxs-lookup"><span data-stu-id="24674-135">[#12889]</span></span>
* <span data-ttu-id="24674-136">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="24674-136">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="24674-137">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="24674-137">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-138">Az.Network</span></span>
* <span data-ttu-id="24674-139">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="24674-139">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="24674-140">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-140">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-141">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-142">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="24674-142">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="24674-143">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="24674-143">Az.RedisCache</span></span>
* <span data-ttu-id="24674-144">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="24674-144">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-145">Az.Sql</span></span>
* <span data-ttu-id="24674-146">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="24674-146">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="24674-147">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="24674-147">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="24674-148">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="24674-148">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="24674-149">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="24674-149">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="24674-150">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="24674-150">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="24674-151">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="24674-151">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-152">Az.Storage</span></span>
* <span data-ttu-id="24674-153">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="24674-153">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="24674-154">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-154">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="24674-155">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-155">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="24674-156">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="24674-156">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="24674-157">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="24674-157">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="24674-158">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="24674-158">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="24674-159">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="24674-159">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="24674-160">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="24674-160">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="24674-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="24674-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="24674-163">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-163">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="24674-164">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-164">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="24674-165">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-165">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="24674-166">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="24674-166">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="24674-167">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="24674-167">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="24674-168">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="24674-168">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-169">Az.Accounts</span></span>
* <span data-ttu-id="24674-170">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="24674-170">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="24674-171">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="24674-171">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-172">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-172">Az.Aks</span></span>
* <span data-ttu-id="24674-173">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="24674-173">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="24674-174">[#12372]</span><span class="sxs-lookup"><span data-stu-id="24674-174">[#12372]</span></span>
* <span data-ttu-id="24674-175">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-175">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="24674-176">[#11239]</span><span class="sxs-lookup"><span data-stu-id="24674-176">[#11239]</span></span>
* <span data-ttu-id="24674-177">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="24674-177">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="24674-178">[#11239]</span><span class="sxs-lookup"><span data-stu-id="24674-178">[#11239]</span></span>
* <span data-ttu-id="24674-179">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="24674-179">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="24674-180">[#12371]</span><span class="sxs-lookup"><span data-stu-id="24674-180">[#12371]</span></span>
* <span data-ttu-id="24674-181">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="24674-181">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-182">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-183">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="24674-183">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-184">Az.Compute</span></span>
* <span data-ttu-id="24674-185">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-185">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="24674-186">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="24674-186">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="24674-187">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-187">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="24674-188">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-188">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="24674-189">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="24674-189">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="24674-190">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="24674-190">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="24674-191">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="24674-191">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="24674-192">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="24674-192">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="24674-193">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="24674-193">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="24674-194">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="24674-194">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-195">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-195">Az.DataFactory</span></span>
* <span data-ttu-id="24674-196">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="24674-196">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-197">Az.EventHub</span></span>
* <span data-ttu-id="24674-198">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="24674-198">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="24674-199">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-199">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="24674-200">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="24674-200">Az.Functions</span></span>
* <span data-ttu-id="24674-201">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="24674-201">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="24674-202">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="24674-202">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="24674-203">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="24674-203">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-204">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-204">Az.HDInsight</span></span>
* <span data-ttu-id="24674-205">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="24674-205">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="24674-206">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-206">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="24674-207">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="24674-207">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="24674-208">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-208">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="24674-209">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-209">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="24674-210">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-210">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="24674-211">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-211">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="24674-212">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="24674-212">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-213">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-213">Az.KeyVault</span></span>
* <span data-ttu-id="24674-214">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="24674-214">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="24674-215">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="24674-215">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="24674-216">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="24674-216">Az.Kusto</span></span>
* <span data-ttu-id="24674-217">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="24674-217">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-218">Az.Network</span></span>
* <span data-ttu-id="24674-219">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="24674-219">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="24674-220">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="24674-220">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="24674-221">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="24674-221">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="24674-222">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="24674-222">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="24674-223">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="24674-223">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="24674-224">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="24674-224">Added subscription level parameter set</span></span>
    - <span data-ttu-id="24674-225">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="24674-225">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="24674-226">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="24674-226">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="24674-227">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="24674-227">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="24674-228">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="24674-228">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="24674-229">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-229">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="24674-230">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="24674-230">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="24674-231">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="24674-231">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="24674-232">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="24674-232">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="24674-233">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="24674-233">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="24674-234">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="24674-234">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="24674-235">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="24674-235">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="24674-236">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="24674-236">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="24674-237">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="24674-237">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="24674-238">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="24674-238">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="24674-239">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="24674-239">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="24674-240">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="24674-240">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="24674-241">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-241">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="24674-242">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="24674-242">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-243">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-243">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-244">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="24674-244">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-245">Az.Resources</span></span>
* <span data-ttu-id="24674-246">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="24674-246">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="24674-247">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-247">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="24674-248">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="24674-248">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="24674-249">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="24674-249">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-250">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-250">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-251">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-251">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="24674-252">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-252">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="24674-253">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-253">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="24674-254">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-254">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="24674-255">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-255">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="24674-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="24674-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="24674-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="24674-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="24674-258">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="24674-258">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="24674-259">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="24674-259">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="24674-260">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="24674-260">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="24674-261">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="24674-261">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="24674-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="24674-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="24674-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="24674-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="24674-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="24674-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="24674-265">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="24674-265">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="24674-266">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="24674-266">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-267">Az.Sql</span></span>
* <span data-ttu-id="24674-268">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="24674-268">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="24674-269">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="24674-269">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="24674-270">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="24674-270">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="24674-271">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="24674-271">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="24674-272">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-272">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="24674-273">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="24674-273">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="24674-274">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="24674-274">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="24674-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="24674-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="24674-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="24674-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="24674-277">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="24674-277">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="24674-278">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="24674-278">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="24674-279">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="24674-279">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="24674-280">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="24674-280">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="24674-281">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="24674-281">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="24674-282">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="24674-282">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="24674-283">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="24674-283">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="24674-284">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="24674-284">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="24674-285">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="24674-285">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-286">Az.Storage</span></span>
* <span data-ttu-id="24674-287">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="24674-287">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="24674-288">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="24674-288">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="24674-289">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-289">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="24674-290">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-290">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="24674-291">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="24674-291">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="24674-292">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="24674-292">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="24674-293">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="24674-293">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="24674-294">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-294">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="24674-295">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-295">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="24674-296">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-296">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="24674-297">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-297">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="24674-298">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-298">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="24674-299">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-299">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="24674-300">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="24674-300">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="24674-301">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="24674-301">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="24674-302">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="24674-302">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="24674-303">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="24674-303">Thanks to our community contributors</span></span>
* <span data-ttu-id="24674-304">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="24674-304">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="24674-305">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="24674-305">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="24674-306">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="24674-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="24674-307">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="24674-307">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="24674-308">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="24674-308">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="24674-309">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="24674-309">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="24674-310">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="24674-310">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="24674-311">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="24674-311">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="24674-312">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="24674-312">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="24674-313">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="24674-313">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="24674-314">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="24674-314">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="24674-315">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="24674-315">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="24674-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-316">Az.Compute</span></span>
* <span data-ttu-id="24674-317">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="24674-317">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="24674-318">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="24674-318">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-319">Az.Accounts</span></span>
* <span data-ttu-id="24674-320">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="24674-320">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="24674-321">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="24674-321">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-322">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-322">Az.Automation</span></span>
* <span data-ttu-id="24674-323">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="24674-323">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-324">Az.Compute</span></span>
* <span data-ttu-id="24674-325">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="24674-325">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="24674-326">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="24674-326">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="24674-327">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="24674-327">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="24674-328">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-328">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-329">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-329">Az.DataFactory</span></span>
* <span data-ttu-id="24674-330">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="24674-330">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-331">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-331">Az.HDInsight</span></span>
* <span data-ttu-id="24674-332">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="24674-332">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-333">Az.KeyVault</span></span>
* <span data-ttu-id="24674-334">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-334">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="24674-335">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-335">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="24674-336">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="24674-336">Az.Maintenance</span></span>
* <span data-ttu-id="24674-337">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-337">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="24674-338">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-338">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="24674-339">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="24674-339">Az.ManagedServices</span></span>
* <span data-ttu-id="24674-340">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="24674-340">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-341">Az.Monitor</span></span>
* <span data-ttu-id="24674-342">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="24674-342">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="24674-343">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-343">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-344">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-344">Az.Resources</span></span>
* <span data-ttu-id="24674-345">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="24674-345">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="24674-346">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-346">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="24674-347">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="24674-347">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="24674-348">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="24674-348">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="24674-349">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="24674-349">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="24674-350">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="24674-350">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="24674-351">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="24674-351">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="24674-352">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="24674-352">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="24674-353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="24674-353">Az.SignalR</span></span>
* <span data-ttu-id="24674-354">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-354">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="24674-355">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-355">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-356">Az.Storage</span></span>
* <span data-ttu-id="24674-357">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="24674-357">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="24674-358">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="24674-358">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="24674-359">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-359">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="24674-360">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="24674-360">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="24674-361">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="24674-361">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="24674-362">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="24674-362">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="24674-363">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="24674-363">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="24674-364">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="24674-364">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="24674-365">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="24674-365">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="24674-366">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="24674-366">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="24674-367">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-367">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="24674-368">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-368">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="24674-369">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-369">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="24674-370">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="24674-370">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="24674-371">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-371">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="24674-372">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="24674-372">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-373">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-373">Az.Accounts</span></span>
* <span data-ttu-id="24674-374">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="24674-374">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="24674-375">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="24674-375">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="24674-376">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="24674-376">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="24674-377">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="24674-377">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="24674-378">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="24674-378">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-379">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-379">Az.Aks</span></span>
* <span data-ttu-id="24674-380">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="24674-380">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="24674-381">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="24674-381">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-382">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-382">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-383">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-383">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="24674-384">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-384">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="24674-385">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-385">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="24674-386">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-386">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="24674-387">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-387">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="24674-388">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-388">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="24674-389">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-389">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="24674-390">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-390">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="24674-391">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-391">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="24674-392">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-392">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="24674-393">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-393">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="24674-394">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-394">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-395">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-395">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-396">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="24674-396">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-397">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-397">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-398">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="24674-398">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-399">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-399">Az.HDInsight</span></span>
* <span data-ttu-id="24674-400">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="24674-400">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="24674-401">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-401">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="24674-402">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-402">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="24674-403">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="24674-403">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="24674-404">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="24674-404">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="24674-405">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-405">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="24674-406">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="24674-406">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-407">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-407">Az.Network</span></span>
* <span data-ttu-id="24674-408">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-408">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="24674-409">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="24674-409">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="24674-410">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="24674-410">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="24674-411">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="24674-411">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-412">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-412">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-413">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="24674-413">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="24674-414">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="24674-414">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="24674-415">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="24674-415">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-417">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="24674-417">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-418">Az.Resources</span></span>
* <span data-ttu-id="24674-419">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="24674-419">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="24674-420">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="24674-420">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-421">Az.Sql</span></span>
* <span data-ttu-id="24674-422">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-422">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="24674-423">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="24674-423">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-424">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-424">Az.Storage</span></span>
* <span data-ttu-id="24674-425">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="24674-425">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="24674-426">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="24674-426">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="24674-427">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="24674-427">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="24674-428">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="24674-428">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="24674-429">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="24674-429">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="24674-430">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="24674-430">Supported get single file share usage</span></span>
    - <span data-ttu-id="24674-431">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="24674-431">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="24674-432">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="24674-432">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-433">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-433">Az.Accounts</span></span>
* <span data-ttu-id="24674-434">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="24674-434">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="24674-435">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="24674-435">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-436">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-436">Az.Aks</span></span>
* <span data-ttu-id="24674-437">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="24674-437">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="24674-438">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="24674-438">Az.AnalysisServices</span></span>
* <span data-ttu-id="24674-439">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="24674-439">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-440">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-440">Az.Automation</span></span>
* <span data-ttu-id="24674-441">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-441">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-442">Az.Compute</span></span>
* <span data-ttu-id="24674-443">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="24674-443">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-444">Az.DataFactory</span></span>
* <span data-ttu-id="24674-445">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="24674-445">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="24674-446">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="24674-446">Az.EventGrid</span></span>
* <span data-ttu-id="24674-447">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="24674-447">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="24674-448">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="24674-448">Added new features:</span></span>
    - <span data-ttu-id="24674-449">輸入對應</span><span class="sxs-lookup"><span data-stu-id="24674-449">Input mapping</span></span>
    - <span data-ttu-id="24674-450">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-450">Event Delivery Schema</span></span>
    - <span data-ttu-id="24674-451">私人連結</span><span class="sxs-lookup"><span data-stu-id="24674-451">Private Link</span></span>
    - <span data-ttu-id="24674-452">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-452">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="24674-453">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="24674-453">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="24674-454">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="24674-454">Azure Function As Destination</span></span>
    - <span data-ttu-id="24674-455">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="24674-455">WebHook Batching</span></span>
    - <span data-ttu-id="24674-456">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="24674-456">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="24674-457">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="24674-457">IpFiltering</span></span>
* <span data-ttu-id="24674-458">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-458">Updated cmdlets:</span></span>
    - <span data-ttu-id="24674-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="24674-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="24674-460">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="24674-460">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="24674-461">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="24674-461">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="24674-462">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="24674-462">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="24674-463">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="24674-463">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="24674-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="24674-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="24674-465">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="24674-465">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="24674-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="24674-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="24674-467">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="24674-467">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-468">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-468">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-469">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="24674-469">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="24674-470">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="24674-470">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-471">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-471">Az.HDInsight</span></span>
* <span data-ttu-id="24674-472">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="24674-472">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-473">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-473">Az.Monitor</span></span>
* <span data-ttu-id="24674-474">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="24674-474">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-475">Az.Network</span></span>
* <span data-ttu-id="24674-476">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="24674-476">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="24674-477">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-477">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="24674-478">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="24674-478">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="24674-479">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="24674-479">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="24674-480">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="24674-480">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="24674-481">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="24674-481">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="24674-482">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-482">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="24674-483">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-483">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="24674-484">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="24674-484">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="24674-485">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="24674-485">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="24674-486">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="24674-486">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="24674-487">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="24674-487">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="24674-488">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="24674-488">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="24674-489">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-489">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="24674-490">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-490">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="24674-491">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-491">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="24674-492">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-492">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-493">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-493">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-494">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="24674-494">Removed project reference to Authentication</span></span>
* <span data-ttu-id="24674-495">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="24674-495">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="24674-496">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-496">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-497">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-497">Az.Resources</span></span>
* <span data-ttu-id="24674-498">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="24674-498">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="24674-499">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-499">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-500">Az.Sql</span></span>
* <span data-ttu-id="24674-501">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="24674-501">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="24674-502">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="24674-502">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="24674-503">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="24674-503">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-504">Az.Storage</span></span>
* <span data-ttu-id="24674-505">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-505">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="24674-506">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-506">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="24674-507">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-507">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="24674-508">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-508">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="24674-509">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="24674-509">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="24674-510">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="24674-510">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="24674-511">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="24674-511">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="24674-512">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="24674-512">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="24674-513">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="24674-513">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="24674-514">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="24674-514">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="24674-515">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="24674-515">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="24674-516">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="24674-516">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="24674-517">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="24674-517">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="24674-518">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="24674-518">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="24674-519">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="24674-519">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="24674-520">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="24674-520">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="24674-521">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="24674-521">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="24674-522">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="24674-522">Az.StorageSync</span></span>
* <span data-ttu-id="24674-523">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="24674-523">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="24674-524">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-524">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="24674-525">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="24674-525">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="24674-526">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-526">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-527">Az.Websites</span></span>
* <span data-ttu-id="24674-528">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="24674-528">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="24674-529">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="24674-529">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-530">Az.Accounts</span></span>
* <span data-ttu-id="24674-531">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="24674-531">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="24674-532">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="24674-532">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="24674-533">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="24674-533">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="24674-534">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="24674-534">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-535">Az.Aks</span></span>
* <span data-ttu-id="24674-536">透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="24674-536">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-537">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-537">Az.Batch</span></span>
* <span data-ttu-id="24674-538">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="24674-538">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="24674-539">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="24674-539">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-540">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-540">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-541">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="24674-541">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="24674-542">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="24674-542">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-543">Az.Compute</span></span>
* <span data-ttu-id="24674-544">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-544">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="24674-545">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="24674-545">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="24674-546">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="24674-546">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="24674-547">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="24674-547">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="24674-548">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="24674-548">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-549">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-549">Az.DataFactory</span></span>
* <span data-ttu-id="24674-550">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="24674-550">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-551">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-551">Az.EventHub</span></span>
* <span data-ttu-id="24674-552">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-552">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="24674-553">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="24674-553">Az.Functions</span></span>
* <span data-ttu-id="24674-554">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="24674-554">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-555">Az.HDInsight</span></span>
* <span data-ttu-id="24674-556">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="24674-556">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="24674-557">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="24674-557">Az.HealthcareApis</span></span>
* <span data-ttu-id="24674-558">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="24674-558">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="24674-559">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="24674-559">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-560">Az.Monitor</span></span>
* <span data-ttu-id="24674-561">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="24674-561">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="24674-562">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="24674-562">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-563">Az.Network</span></span>
* <span data-ttu-id="24674-564">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="24674-565">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-565">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="24674-566">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="24674-566">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="24674-567">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="24674-567">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="24674-568">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="24674-568">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="24674-569">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-569">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="24674-570">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="24674-570">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="24674-571">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="24674-571">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="24674-572">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="24674-572">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="24674-573">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="24674-573">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="24674-574">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="24674-574">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="24674-575">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-575">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="24674-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="24674-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="24674-577">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="24674-577">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="24674-578">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="24674-578">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="24674-579">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="24674-579">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="24674-580">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="24674-580">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="24674-581">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="24674-581">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="24674-582">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="24674-582">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="24674-583">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="24674-583">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="24674-584">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="24674-584">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="24674-585">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="24674-585">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="24674-586">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="24674-586">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="24674-587">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="24674-587">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="24674-588">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="24674-588">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="24674-589">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="24674-589">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="24674-590">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="24674-590">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="24674-591">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="24674-591">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="24674-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="24674-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="24674-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="24674-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="24674-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="24674-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="24674-598">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-598">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="24674-599">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="24674-599">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="24674-600">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="24674-600">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="24674-601">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="24674-601">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="24674-602">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="24674-602">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="24674-603">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="24674-603">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="24674-604">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="24674-604">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="24674-605">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-605">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="24674-606">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-606">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="24674-607">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-607">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="24674-608">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-608">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="24674-609">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-609">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="24674-610">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-610">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="24674-611">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="24674-611">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="24674-612">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="24674-612">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-613">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-613">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-614">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="24674-614">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="24674-615">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="24674-615">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="24674-616">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="24674-616">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="24674-617">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="24674-617">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="24674-618">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="24674-618">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-619">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-620">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-620">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="24674-621">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="24674-621">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-622">Az.Resources</span></span>
* <span data-ttu-id="24674-623">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="24674-623">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="24674-624">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="24674-624">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="24674-625">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="24674-625">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="24674-626">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-626">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="24674-627">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-627">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="24674-628">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="24674-628">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-629">Az.Sql</span></span>
* <span data-ttu-id="24674-630">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="24674-630">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="24674-631">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="24674-631">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="24674-632">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="24674-632">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-633">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-633">Az.Storage</span></span>
* <span data-ttu-id="24674-634">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-634">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="24674-635">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-635">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="24674-636">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-636">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-637">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-637">Az.Websites</span></span>
* <span data-ttu-id="24674-638">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="24674-638">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="24674-639">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="24674-639">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="24674-640">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-640">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="24674-641">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-641">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="24674-642">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-642">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="24674-643">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="24674-643">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="24674-644">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="24674-644">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-645">Az.Accounts</span></span>
* <span data-ttu-id="24674-646">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="24674-646">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="24674-647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="24674-647">Az.AnalysisServices</span></span>
* <span data-ttu-id="24674-648">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-648">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-649">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-649">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-650">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-650">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="24674-651">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="24674-651">Az.Billing</span></span>
* <span data-ttu-id="24674-652">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-652">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-653">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-654">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="24674-654">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="24674-655">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-655">Az.DataFactory</span></span>
* <span data-ttu-id="24674-656">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-656">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="24674-657">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="24674-657">Az.DataShare</span></span>
* <span data-ttu-id="24674-658">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="24674-658">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="24674-659">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="24674-659">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="24674-660">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="24674-660">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-661">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-661">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-662">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="24674-662">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="24674-663">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="24674-663">Added optional parameters to</span></span> 
    - <span data-ttu-id="24674-664">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="24674-664">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="24674-665">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="24674-665">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-667">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="24674-667">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="24674-668">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="24674-668">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="24674-669">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-669">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="24674-670">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="24674-670">Az.PrivateDns</span></span>
* <span data-ttu-id="24674-671">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="24674-671">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-673">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="24674-673">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="24674-674">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-674">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-675">Az.Resources</span></span>
* <span data-ttu-id="24674-676">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-676">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="24674-677">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="24674-677">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="24674-678">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="24674-678">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="24674-679">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-679">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="24674-680">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-680">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-681">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-681">Az.Sql</span></span>
* <span data-ttu-id="24674-682">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="24674-682">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="24674-683">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="24674-683">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="24674-684">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-684">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-685">Az.Storage</span></span>
* <span data-ttu-id="24674-686">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="24674-686">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="24674-687">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="24674-687">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="24674-688">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-688">Highlights since the last release</span></span>
* <span data-ttu-id="24674-689">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="24674-689">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="24674-690">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="24674-690">General availability of Az.Functions</span></span> 
* <span data-ttu-id="24674-691">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="24674-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-692">Az.Accounts</span></span>
* <span data-ttu-id="24674-693">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="24674-693">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="24674-694">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="24674-694">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-695">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-695">Az.Aks</span></span>
* <span data-ttu-id="24674-696">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="24674-696">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="24674-697">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="24674-697">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="24674-698">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="24674-698">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-699">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-699">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-700">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="24674-700">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="24674-701">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="24674-701">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="24674-702">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="24674-702">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="24674-703">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="24674-703">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="24674-704">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="24674-704">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="24674-705">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="24674-705">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="24674-706">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="24674-706">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="24674-707">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="24674-707">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="24674-708">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="24674-708">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="24674-709">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="24674-709">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="24674-710">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="24674-710">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="24674-711">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="24674-711">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="24674-712">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="24674-712">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="24674-713">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="24674-713">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="24674-714">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="24674-714">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="24674-715">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="24674-715">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="24674-716">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="24674-716">Az.ApplicationInsights</span></span>
* <span data-ttu-id="24674-717">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="24674-717">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="24674-718">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="24674-718">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="24674-719">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-719">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-720">Az.Batch</span></span>
* <span data-ttu-id="24674-721">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="24674-721">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="24674-722">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="24674-722">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="24674-723">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-723">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="24674-724">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="24674-724">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="24674-725">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="24674-725">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="24674-726">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="24674-726">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="24674-727">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="24674-727">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="24674-728">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="24674-728">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="24674-729">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-729">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-730">Az.Compute</span></span>
* <span data-ttu-id="24674-731">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-731">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="24674-732">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="24674-732">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="24674-733">重大變更</span><span class="sxs-lookup"><span data-stu-id="24674-733">Breaking changes</span></span>
    - <span data-ttu-id="24674-734">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="24674-734">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="24674-735">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="24674-735">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="24674-736">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="24674-736">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="24674-737">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="24674-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="24674-738">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-738">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="24674-739">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="24674-739">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="24674-740">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="24674-740">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="24674-741">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-741">Az.DataFactory</span></span>
* <span data-ttu-id="24674-742">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="24674-742">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-743">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-744">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-744">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="24674-745">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-745">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="24674-746">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="24674-746">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="24674-747">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="24674-747">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="24674-748">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="24674-748">Az.Functions</span></span>
* <span data-ttu-id="24674-749">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="24674-749">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-750">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-750">Az.HDInsight</span></span>
* <span data-ttu-id="24674-751">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="24674-751">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="24674-752">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="24674-752">Az.HealthcareApis</span></span>
* <span data-ttu-id="24674-753">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="24674-753">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-754">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-754">Az.IotHub</span></span>
* <span data-ttu-id="24674-755">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="24674-755">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="24674-756">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="24674-756">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="24674-757">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="24674-757">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="24674-758">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="24674-758">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="24674-759">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="24674-759">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="24674-760">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-760">New cmdlets are:</span></span>
    - <span data-ttu-id="24674-761">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-761">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="24674-762">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-762">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="24674-763">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-763">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="24674-764">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-764">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="24674-765">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="24674-765">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="24674-766">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="24674-766">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-767">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-767">Az.KeyVault</span></span>
* <span data-ttu-id="24674-768">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="24674-768">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="24674-769">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="24674-769">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="24674-770">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="24674-770">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="24674-771">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-771">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="24674-772">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="24674-772">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="24674-773">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="24674-773">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="24674-774">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="24674-774">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-775">Az.Monitor</span></span>
* <span data-ttu-id="24674-776">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="24674-776">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="24674-777">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="24674-777">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="24674-778">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="24674-778">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="24674-779">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="24674-779">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="24674-780">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="24674-780">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="24674-781">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="24674-781">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="24674-782">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="24674-782">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-783">Az.Network</span></span>
* <span data-ttu-id="24674-784">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="24674-784">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="24674-785">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="24674-785">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="24674-786">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="24674-786">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="24674-787">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-787">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="24674-788">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-788">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="24674-789">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-789">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-790">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="24674-790">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="24674-791">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="24674-791">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="24674-792">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="24674-792">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="24674-793">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="24674-793">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="24674-794">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="24674-794">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="24674-795">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="24674-795">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="24674-796">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="24674-796">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="24674-797">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="24674-797">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="24674-798">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="24674-798">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="24674-799">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="24674-799">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="24674-800">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-800">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="24674-801">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="24674-801">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="24674-802">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="24674-802">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="24674-803">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="24674-803">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="24674-804">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="24674-804">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="24674-805">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="24674-805">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="24674-806">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="24674-806">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="24674-807">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-807">Updated cmdlet:</span></span>
        - <span data-ttu-id="24674-808">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="24674-808">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-809">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-809">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-810">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="24674-810">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="24674-811">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-811">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="24674-812">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="24674-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="24674-813">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="24674-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="24674-814">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="24674-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="24674-815">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="24674-815">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="24674-816">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-816">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="24674-817">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-817">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-818">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-818">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-819">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="24674-819">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="24674-820">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="24674-820">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="24674-821">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="24674-821">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="24674-822">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="24674-822">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="24674-823">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="24674-823">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-824">Az.Resources</span></span>
* <span data-ttu-id="24674-825">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="24674-825">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="24674-826">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="24674-826">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="24674-827">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="24674-827">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="24674-828">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="24674-828">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="24674-829">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="24674-829">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="24674-830">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="24674-830">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="24674-831">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="24674-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="24674-832">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="24674-832">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="24674-833">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="24674-833">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="24674-834">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="24674-834">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="24674-835">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="24674-835">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="24674-836">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="24674-836">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="24674-837">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="24674-837">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="24674-838">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="24674-838">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="24674-839">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="24674-839">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="24674-840">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="24674-840">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="24674-841">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-841">'New-AzDeployment'</span></span>
    - <span data-ttu-id="24674-842">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-842">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="24674-843">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-843">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="24674-844">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="24674-844">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-845">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-845">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-846">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="24674-846">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-847">Az.Sql</span></span>
* <span data-ttu-id="24674-848">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="24674-848">Enhance performance of:</span></span>
    - <span data-ttu-id="24674-849">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="24674-849">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="24674-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="24674-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="24674-851">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="24674-851">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="24674-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="24674-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="24674-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="24674-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="24674-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="24674-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="24674-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="24674-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="24674-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="24674-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="24674-857">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="24674-857">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="24674-858">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-858">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-859">Az.Storage</span></span>
* <span data-ttu-id="24674-860">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-860">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="24674-861">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="24674-861">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="24674-862">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-862">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="24674-863">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="24674-863">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="24674-864">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="24674-864">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="24674-865">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="24674-865">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="24674-866">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="24674-866">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="24674-867">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="24674-867">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="24674-868">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="24674-868">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="24674-869">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="24674-869">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="24674-870">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="24674-870">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="24674-871">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="24674-871">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="24674-872">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="24674-872">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="24674-873">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-873">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="24674-874">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-874">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="24674-875">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-875">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="24674-876">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="24674-876">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="24674-877">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="24674-877">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="24674-878">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="24674-878">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="24674-879">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-879">Supported failover Storage account</span></span>
    - <span data-ttu-id="24674-880">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="24674-880">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="24674-881">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="24674-881">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="24674-882">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="24674-882">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="24674-883">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-883">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="24674-884">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="24674-884">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="24674-885">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="24674-885">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="24674-886">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="24674-886">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="24674-887">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="24674-887">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="24674-888">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="24674-888">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="24674-889">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="24674-889">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="24674-890">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="24674-890">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="24674-891">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="24674-891">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="24674-892">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="24674-892">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="24674-893">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="24674-893">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="24674-894">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="24674-894">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="24674-895">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="24674-895">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="24674-896">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="24674-896">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="24674-897">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="24674-897">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="24674-898">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="24674-898">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="24674-899">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="24674-899">Az.TrafficManager</span></span>
* <span data-ttu-id="24674-900">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="24674-900">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-901">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-901">Az.Websites</span></span>
* <span data-ttu-id="24674-902">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="24674-902">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="24674-903">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="24674-903">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="24674-904">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-904">Highlights since the last release</span></span>
* <span data-ttu-id="24674-905">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="24674-905">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-906">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-906">Az.Accounts</span></span>
* <span data-ttu-id="24674-907">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="24674-907">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-908">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-908">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-909">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="24674-909">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="24674-910">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="24674-910">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-911">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-911">Az.Cdn</span></span>
* <span data-ttu-id="24674-912">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="24674-912">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-913">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-913">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-914">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="24674-914">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-915">Az.Compute</span></span>
* <span data-ttu-id="24674-916">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-916">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="24674-917">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="24674-917">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-918">Az.IotHub</span></span>
* <span data-ttu-id="24674-919">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-919">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="24674-920">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="24674-920">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="24674-921">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="24674-921">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="24674-922">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="24674-922">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="24674-923">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-923">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="24674-924">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="24674-924">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="24674-925">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="24674-925">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="24674-926">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="24674-926">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="24674-927">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-927">New cmdlets are:</span></span>
    - <span data-ttu-id="24674-928">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-928">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="24674-929">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-929">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="24674-930">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-930">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="24674-931">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="24674-931">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="24674-932">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="24674-932">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-933">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-933">Az.KeyVault</span></span>
* <span data-ttu-id="24674-934">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="24674-934">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="24674-935">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="24674-935">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="24674-936">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="24674-936">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="24674-937">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="24674-937">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="24674-938">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="24674-938">Az.Maintenance</span></span>
* <span data-ttu-id="24674-939">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="24674-939">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-940">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-940">Az.Monitor</span></span>
* <span data-ttu-id="24674-941">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-941">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="24674-942">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="24674-942">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="24674-943">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="24674-943">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="24674-944">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="24674-944">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="24674-945">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="24674-945">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="24674-946">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="24674-946">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="24674-947">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="24674-947">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="24674-948">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="24674-948">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-949">Az.Network</span></span>
* <span data-ttu-id="24674-950">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="24674-950">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="24674-951">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="24674-951">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="24674-952">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="24674-952">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="24674-953">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-953">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="24674-954">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-954">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="24674-955">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="24674-955">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="24674-956">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="24674-956">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="24674-957">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="24674-957">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="24674-958">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="24674-958">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="24674-959">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-959">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="24674-960">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="24674-960">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="24674-961">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="24674-961">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="24674-962">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="24674-962">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="24674-963">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="24674-963">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="24674-964">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="24674-964">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="24674-965">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="24674-965">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-966">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-966">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-967">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-967">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="24674-968">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="24674-968">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-969">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-969">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-970">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="24674-970">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-971">Az.Sql</span></span>
* <span data-ttu-id="24674-972">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-972">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="24674-973">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="24674-973">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-974">Az.Storage</span></span>
* <span data-ttu-id="24674-975">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="24674-975">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="24674-976">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="24674-976">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="24674-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-977">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="24674-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="24674-979">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="24674-979">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="24674-980">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="24674-980">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="24674-981">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="24674-981">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="24674-982">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="24674-982">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="24674-983">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="24674-983">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="24674-984">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="24674-984">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="24674-985">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="24674-985">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="24674-986">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="24674-986">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="24674-987">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="24674-987">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="24674-988">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="24674-988">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="24674-989">一般</span><span class="sxs-lookup"><span data-stu-id="24674-989">General</span></span>
* <span data-ttu-id="24674-990">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="24674-990">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="24674-991">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="24674-991">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="24674-992">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="24674-992">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="24674-993">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="24674-993">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="24674-994">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="24674-994">Az.Billing</span></span>
  - <span data-ttu-id="24674-995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-995">Az.Compute</span></span>
  - <span data-ttu-id="24674-996">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="24674-996">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="24674-997">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-997">Az.EventHub</span></span>
  - <span data-ttu-id="24674-998">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-998">Az.IotHub</span></span>
  - <span data-ttu-id="24674-999">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-999">Az.KeyVault</span></span>
  - <span data-ttu-id="24674-1000">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1000">Az.Monitor</span></span>
  - <span data-ttu-id="24674-1001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1001">Az.Network</span></span>
  - <span data-ttu-id="24674-1002">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1002">Az.Resources</span></span>
  - <span data-ttu-id="24674-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1003">Az.Storage</span></span>
  - <span data-ttu-id="24674-1004">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1004">Az.Websites</span></span>
* <span data-ttu-id="24674-1005">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-1005">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="24674-1006">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="24674-1006">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="24674-1007">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="24674-1007">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="24674-1008">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="24674-1008">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-1009">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1009">Az.Accounts</span></span>
* <span data-ttu-id="24674-1010">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="24674-1010">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1011">Az.Compute</span></span>
* <span data-ttu-id="24674-1012">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1012">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="24674-1013">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="24674-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="24674-1014">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-1014">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="24674-1015">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="24674-1015">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="24674-1016">[#11354]</span><span class="sxs-lookup"><span data-stu-id="24674-1016">[#11354]</span></span>
* <span data-ttu-id="24674-1017">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1017">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="24674-1018">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="24674-1018">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="24674-1019">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="24674-1019">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="24674-1020">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="24674-1020">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="24674-1021">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="24674-1021">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="24674-1022">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-1022">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="24674-1023">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="24674-1023">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="24674-1024">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="24674-1024">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="24674-1025">[#11257]</span><span class="sxs-lookup"><span data-stu-id="24674-1025">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1026">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1026">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1027">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="24674-1027">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="24674-1028">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="24674-1028">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-1029">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-1029">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-1030">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="24674-1030">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="24674-1031">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="24674-1031">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-1032">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-1032">Az.HDInsight</span></span>
* <span data-ttu-id="24674-1033">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="24674-1033">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-1034">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-1034">Az.IotHub</span></span>
* <span data-ttu-id="24674-1035">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1035">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="24674-1036">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-1036">New Cmdlets are:</span></span>
    - <span data-ttu-id="24674-1037">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="24674-1037">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="24674-1038">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="24674-1038">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-1039">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-1039">Az.KeyVault</span></span>
* <span data-ttu-id="24674-1040">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="24674-1040">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1041">Az.Monitor</span></span>
* <span data-ttu-id="24674-1042">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="24674-1042">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1043">Az.Network</span></span>
* <span data-ttu-id="24674-1044">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="24674-1044">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="24674-1045">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-1045">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="24674-1046">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="24674-1046">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="24674-1047">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="24674-1047">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="24674-1048">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="24674-1048">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="24674-1049">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="24674-1049">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-1050">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-1050">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-1051">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1051">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1053">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-1053">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="24674-1054">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="24674-1054">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="24674-1055">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1055">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="24674-1056">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1056">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="24674-1057">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1057">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="24674-1058">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1058">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1059">Az.Resources</span></span>
* <span data-ttu-id="24674-1060">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="24674-1060">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="24674-1061">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="24674-1061">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="24674-1062">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="24674-1062">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="24674-1063">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="24674-1063">Added example.</span></span>
* <span data-ttu-id="24674-1064">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="24674-1064">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="24674-1065">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1065">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1066">Az.Sql</span></span>
* <span data-ttu-id="24674-1067">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="24674-1067">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="24674-1068">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="24674-1068">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="24674-1069">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="24674-1069">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="24674-1070">Az.Support</span><span class="sxs-lookup"><span data-stu-id="24674-1070">Az.Support</span></span>
* <span data-ttu-id="24674-1071">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="24674-1071">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-1072">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1072">Az.Websites</span></span>
* <span data-ttu-id="24674-1073">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1073">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="24674-1074">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="24674-1074">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="24674-1075">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="24674-1075">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="24674-1076">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="24674-1076">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="24674-1077">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="24674-1077">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="24674-1078">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="24674-1078">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1079">Az.Accounts</span></span>
* <span data-ttu-id="24674-1080">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="24674-1080">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="24674-1081">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="24674-1081">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="24674-1082">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="24674-1082">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-1083">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-1083">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-1084">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="24674-1084">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="24674-1085">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="24674-1085">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="24674-1086">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1086">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="24674-1087">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="24674-1087">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-1088">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-1088">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-1089">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="24674-1089">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-1090">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-1090">Az.IotHub</span></span>
* <span data-ttu-id="24674-1091">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1091">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="24674-1092">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-1092">New Cmdlets are:</span></span>
    - <span data-ttu-id="24674-1093">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1093">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="24674-1094">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1094">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="24674-1095">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1095">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="24674-1096">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1096">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="24674-1097">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1097">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="24674-1098">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-1098">New Cmdlets are:</span></span>
    - <span data-ttu-id="24674-1099">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="24674-1099">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="24674-1100">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="24674-1100">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="24674-1101">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="24674-1101">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="24674-1102">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="24674-1102">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="24674-1103">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="24674-1103">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="24674-1104">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="24674-1104">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="24674-1105">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1105">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="24674-1106">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-1106">New Cmdlets are:</span></span>
    - <span data-ttu-id="24674-1107">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="24674-1107">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="24674-1108">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="24674-1108">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="24674-1109">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1109">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1110">Az.Monitor</span></span>
* <span data-ttu-id="24674-1111">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="24674-1111">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1112">Az.Network</span></span>
* <span data-ttu-id="24674-1113">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="24674-1113">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="24674-1114">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="24674-1114">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="24674-1115">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="24674-1115">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="24674-1116">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="24674-1116">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1117">Az.Resources</span></span>
* <span data-ttu-id="24674-1118">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-1118">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="24674-1119">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="24674-1119">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="24674-1120">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="24674-1120">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="24674-1121">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="24674-1121">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="24674-1122">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-1122">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="24674-1123">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="24674-1123">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="24674-1124">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="24674-1124">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="24674-1125">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="24674-1125">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="24674-1126">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="24674-1126">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="24674-1127">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="24674-1127">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="24674-1128">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="24674-1128">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="24674-1129">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1129">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="24674-1130">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="24674-1130">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="24674-1131">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="24674-1131">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1132">Az.Sql</span></span>
* <span data-ttu-id="24674-1133">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="24674-1133">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="24674-1134">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1134">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="24674-1135">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="24674-1135">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="24674-1136">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="24674-1136">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="24674-1137">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="24674-1137">Remove an LTR backup</span></span>
    - <span data-ttu-id="24674-1138">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="24674-1138">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="24674-1139">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="24674-1139">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="24674-1140">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="24674-1140">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="24674-1141">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="24674-1141">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1142">Az.Storage</span></span>
* <span data-ttu-id="24674-1143">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="24674-1143">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="24674-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="24674-1145">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1145">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="24674-1146">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="24674-1146">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="24674-1147">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="24674-1147">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1148">Az.Websites</span></span>
* <span data-ttu-id="24674-1149">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="24674-1149">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="24674-1150">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1150">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="24674-1151">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="24674-1151">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="24674-1152">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="24674-1152">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="24674-1153">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="24674-1153">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="24674-1154">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="24674-1154">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="24674-1155">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-1155">Highlights since the last major release</span></span>
* <span data-ttu-id="24674-1156">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="24674-1156">Updated client side telemetry.</span></span>
* <span data-ttu-id="24674-1157">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="24674-1157">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="24674-1158">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-1158">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-1159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1159">Az.Accounts</span></span>
* <span data-ttu-id="24674-1160">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="24674-1160">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-1161">Az.Automation</span></span>
* <span data-ttu-id="24674-1162">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1162">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-1163">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-1163">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-1164">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="24674-1164">Updated SDK to 7.0</span></span>
* <span data-ttu-id="24674-1165">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1165">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1166">Az.Compute</span></span>
* <span data-ttu-id="24674-1167">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="24674-1167">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-1168">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-1168">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-1169">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="24674-1169">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-1170">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-1170">Az.IotHub</span></span>
* <span data-ttu-id="24674-1171">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1171">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="24674-1172">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-1172">New Cmdlets are:</span></span>
    - <span data-ttu-id="24674-1173">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1173">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="24674-1174">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1174">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="24674-1175">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1175">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="24674-1176">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="24674-1176">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-1177">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-1177">Az.KeyVault</span></span>
* <span data-ttu-id="24674-1178">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="24674-1178">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1179">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1179">Az.Monitor</span></span>
* <span data-ttu-id="24674-1180">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="24674-1180">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="24674-1181">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="24674-1181">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="24674-1182">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="24674-1182">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1183">Az.Network</span></span>
* <span data-ttu-id="24674-1184">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="24674-1184">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="24674-1185">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="24674-1185">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="24674-1186">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="24674-1186">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="24674-1187">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="24674-1187">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="24674-1188">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-1188">No new cmdlets are added.</span></span> <span data-ttu-id="24674-1189">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="24674-1189">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1190">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1190">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1191">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1191">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1192">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1192">Az.Resources</span></span>
* <span data-ttu-id="24674-1193">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1193">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="24674-1194">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24674-1194">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="24674-1195">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="24674-1195">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="24674-1196">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="24674-1196">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="24674-1197">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="24674-1197">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="24674-1198">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="24674-1198">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="24674-1199">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="24674-1199">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="24674-1200">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="24674-1200">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1201">Az.Sql</span></span>
* <span data-ttu-id="24674-1202">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1202">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="24674-1203">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1203">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="24674-1204">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="24674-1204">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="24674-1205">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="24674-1205">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="24674-1206">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1206">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="24674-1207">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="24674-1207">Az.StorageSync</span></span>
* <span data-ttu-id="24674-1208">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="24674-1208">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="24674-1209">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="24674-1209">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="24674-1210">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-1210">Highlights since the last major release</span></span>
* <span data-ttu-id="24674-1211">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="24674-1211">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="24674-1212">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="24674-1212">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-1213">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1213">Az.Accounts</span></span>
* <span data-ttu-id="24674-1214">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="24674-1214">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="24674-1215">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="24674-1215">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-1216">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-1216">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-1217">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="24674-1217">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="24674-1218">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="24674-1218">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="24674-1219">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="24674-1219">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="24674-1220">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="24674-1220">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1221">Az.Compute</span></span>
* <span data-ttu-id="24674-1222">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="24674-1222">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="24674-1223">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1223">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="24674-1224">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1224">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="24674-1225">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="24674-1226">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-1226">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1227">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1228">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="24674-1228">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="24674-1229">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="24674-1229">Az.DeploymentManager</span></span>
* <span data-ttu-id="24674-1230">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="24674-1230">Adds LIST operations for resources</span></span>
* <span data-ttu-id="24674-1231">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="24674-1231">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-1232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-1232">Az.HDInsight</span></span>
* <span data-ttu-id="24674-1233">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-1233">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-1234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-1234">Az.KeyVault</span></span>
* <span data-ttu-id="24674-1235">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="24674-1235">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1236">Az.Network</span></span>
* <span data-ttu-id="24674-1237">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="24674-1237">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="24674-1238">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="24674-1238">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="24674-1239">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1239">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="24674-1240">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="24674-1240">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="24674-1241">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="24674-1241">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="24674-1242">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="24674-1242">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="24674-1243">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="24674-1243">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="24674-1244">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1244">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="24674-1245">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1245">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="24674-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="24674-1247">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1247">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="24674-1248">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="24674-1248">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="24674-1249">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1249">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-1250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-1250">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-1251">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="24674-1251">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="24674-1252">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="24674-1252">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="24674-1253">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="24674-1253">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="24674-1254">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="24674-1254">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1255">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1256">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="24674-1256">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="24674-1257">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1257">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1258">Az.Resources</span></span>
* <span data-ttu-id="24674-1259">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="24674-1259">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="24674-1260">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1260">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1261">Az.Sql</span></span>
<span data-ttu-id="24674-1262">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="24674-1262">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1263">Az.Storage</span></span>
* <span data-ttu-id="24674-1264">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="24674-1264">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="24674-1265">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-1265">New-AzStorageAccount</span></span>
* <span data-ttu-id="24674-1266">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="24674-1266">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="24674-1267">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="24674-1267">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-1268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1268">Az.Websites</span></span>
* <span data-ttu-id="24674-1269">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="24674-1269">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="24674-1270">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="24674-1270">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="24674-1271">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="24674-1271">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1272">Az.Accounts</span></span>
* <span data-ttu-id="24674-1273">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="24674-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-1274">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-1274">Az.Cdn</span></span>
* <span data-ttu-id="24674-1275">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="24674-1275">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1276">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1276">Az.Compute</span></span>
* <span data-ttu-id="24674-1277">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-1277">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="24674-1278">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="24674-1278">Az.ContainerInstance</span></span>
* <span data-ttu-id="24674-1279">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="24674-1279">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="24674-1280">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="24674-1280">Az.DataBoxEdge</span></span>
* <span data-ttu-id="24674-1281">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="24674-1281">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="24674-1282">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="24674-1282">Get the Edge Storage Container</span></span>
* <span data-ttu-id="24674-1283">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="24674-1283">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="24674-1284">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="24674-1284">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="24674-1285">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="24674-1285">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="24674-1286">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="24674-1286">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="24674-1287">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="24674-1287">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="24674-1288">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="24674-1288">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="24674-1289">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-1289">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="24674-1290">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-1290">Get the Edge Storage Account</span></span>
* <span data-ttu-id="24674-1291">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-1291">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="24674-1292">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-1292">Create new Edge Storage Account</span></span>
* <span data-ttu-id="24674-1293">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="24674-1293">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="24674-1294">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-1294">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="24674-1295">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="24674-1295">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="24674-1296">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="24674-1296">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="24674-1297">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="24674-1297">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="24674-1298">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="24674-1298">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1299">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1299">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1300">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="24674-1300">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="24674-1301">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="24674-1301">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="24674-1302">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="24674-1302">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="24674-1303">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="24674-1303">Az.DevTestLabs</span></span>
* <span data-ttu-id="24674-1304">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="24674-1304">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-1305">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-1305">Az.EventHub</span></span>
* <span data-ttu-id="24674-1306">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="24674-1306">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-1307">Az.HDInsight</span></span>
* <span data-ttu-id="24674-1308">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-1308">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="24674-1309">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="24674-1309">Az.MachineLearning</span></span>
* <span data-ttu-id="24674-1310">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1310">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="24674-1311">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="24674-1311">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="24674-1312">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="24674-1312">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="24674-1313">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="24674-1313">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="24674-1314">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="24674-1314">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="24674-1315">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="24674-1315">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="24674-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="24674-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="24674-1317">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="24674-1317">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1318">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1318">Az.Network</span></span>
* <span data-ttu-id="24674-1319">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="24674-1319">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1320">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1320">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1321">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="24674-1321">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="24674-1322">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="24674-1322">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="24674-1323">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="24674-1323">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="24674-1324">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="24674-1324">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1325">Az.Resources</span></span>
* <span data-ttu-id="24674-1326">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-1326">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1327">Az.Sql</span></span>
* <span data-ttu-id="24674-1328">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="24674-1328">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="24674-1329">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-1329">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="24674-1330">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="24674-1330">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="24674-1331">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="24674-1331">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1332">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1332">Az.Storage</span></span>
* <span data-ttu-id="24674-1333">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1333">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="24674-1334">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-1334">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="24674-1335">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="24674-1335">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="24674-1336">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-1336">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="24674-1337">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="24674-1337">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="24674-1338">一般</span><span class="sxs-lookup"><span data-stu-id="24674-1338">General</span></span>
* <span data-ttu-id="24674-1339">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="24674-1339">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1340">Az.Accounts</span></span>
* <span data-ttu-id="24674-1341">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="24674-1341">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="24674-1342">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1342">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-1343">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-1343">Az.Batch</span></span>
* <span data-ttu-id="24674-1344">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="24674-1344">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1345">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1346">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="24674-1346">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-1347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-1347">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-1348">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="24674-1348">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="24674-1349">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="24674-1349">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="24674-1350">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="24674-1350">Az.HealthcareApis</span></span>
* <span data-ttu-id="24674-1351">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="24674-1351">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-1352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-1352">Az.KeyVault</span></span>
* <span data-ttu-id="24674-1353">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-1353">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="24674-1354">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="24674-1354">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="24674-1355">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1355">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1356">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1356">Az.Monitor</span></span>
* <span data-ttu-id="24674-1357">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="24674-1357">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="24674-1358">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="24674-1358">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="24674-1359">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="24674-1359">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1360">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1360">Az.Network</span></span>
* <span data-ttu-id="24674-1361">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="24674-1361">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1362">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1362">Az.Resources</span></span>
* <span data-ttu-id="24674-1363">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-1363">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="24674-1364">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1364">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1365">Az.Sql</span></span>
* <span data-ttu-id="24674-1366">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="24674-1366">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1367">Az.Storage</span></span>
* <span data-ttu-id="24674-1368">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="24674-1368">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="24674-1369">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="24674-1369">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="24674-1370">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="24674-1370">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="24674-1371">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="24674-1371">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="24674-1372">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="24674-1372">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="24674-1373">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="24674-1373">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="24674-1374">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="24674-1374">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="24674-1375">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24674-1375">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="24674-1376">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24674-1376">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="24674-1377">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="24674-1377">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="24674-1378">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="24674-1378">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="24674-1379">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-1379">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="24674-1380">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="24674-1380">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="24674-1381">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="24674-1381">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="24674-1382">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-1382">Highlights since the last major release</span></span>
* <span data-ttu-id="24674-1383">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="24674-1383">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="24674-1384">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="24674-1384">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1385">Az.Compute</span></span>
* <span data-ttu-id="24674-1386">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="24674-1386">VM Reapply feature</span></span>
    - <span data-ttu-id="24674-1387">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1387">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="24674-1388">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="24674-1388">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="24674-1389">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24674-1389">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="24674-1390">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="24674-1390">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="24674-1391">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="24674-1391">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="24674-1392">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1392">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="24674-1393">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="24674-1393">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="24674-1394">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1394">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="24674-1395">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1395">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="24674-1396">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1396">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="24674-1397">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="24674-1397">Az.DataBoxEdge</span></span>
* <span data-ttu-id="24674-1398">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="24674-1398">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="24674-1399">取得訂單</span><span class="sxs-lookup"><span data-stu-id="24674-1399">Get the Order</span></span>
* <span data-ttu-id="24674-1400">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="24674-1400">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="24674-1401">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="24674-1401">Create new Order</span></span>
* <span data-ttu-id="24674-1402">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="24674-1402">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="24674-1403">移除訂單</span><span class="sxs-lookup"><span data-stu-id="24674-1403">Remove the Order</span></span>
* <span data-ttu-id="24674-1404">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="24674-1404">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="24674-1405">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="24674-1405">Now creates Local Share</span></span>
* <span data-ttu-id="24674-1406">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="24674-1406">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="24674-1407">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="24674-1407">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="24674-1408">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="24674-1408">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="24674-1409">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="24674-1409">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="24674-1410">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="24674-1410">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="24674-1411">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="24674-1411">Gets the information about Triggers</span></span>
* <span data-ttu-id="24674-1412">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="24674-1412">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="24674-1413">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="24674-1413">Create new Triggers</span></span>
* <span data-ttu-id="24674-1414">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="24674-1414">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="24674-1415">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="24674-1415">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1416">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1416">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1417">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="24674-1417">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="24674-1418">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="24674-1418">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-1419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-1419">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-1420">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="24674-1420">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-1421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-1421">Az.EventHub</span></span>
* <span data-ttu-id="24674-1422">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="24674-1422">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-1423">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-1423">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-1424">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="24674-1424">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="24674-1425">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="24674-1425">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="24674-1426">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="24674-1426">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="24674-1427">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="24674-1427">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1428">Az.Network</span></span>
* <span data-ttu-id="24674-1429">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="24674-1429">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="24674-1430">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="24674-1430">Az.PrivateDns</span></span>
* <span data-ttu-id="24674-1431">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="24674-1431">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1432">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1433">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="24674-1433">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="24674-1434">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="24674-1434">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="24674-1435">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="24674-1435">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="24674-1436">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="24674-1436">Az.RedisCache</span></span>
* <span data-ttu-id="24674-1437">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="24674-1437">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="24674-1438">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="24674-1438">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="24674-1439">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="24674-1439">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1440">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1440">Az.Resources</span></span>
- <span data-ttu-id="24674-1441">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-1441">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="24674-1442">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="24674-1442">Updated create policy definition help example</span></span>
- <span data-ttu-id="24674-1443">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="24674-1443">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="24674-1444">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="24674-1444">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="24674-1445">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="24674-1445">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1446">Az.Sql</span></span>
* <span data-ttu-id="24674-1447">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1447">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="24674-1448">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="24674-1448">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="24674-1449">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="24674-1449">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="24674-1450">一般</span><span class="sxs-lookup"><span data-stu-id="24674-1450">General</span></span>
* <span data-ttu-id="24674-1451">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="24674-1451">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1452">Az.Accounts</span></span>
* <span data-ttu-id="24674-1453">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="24674-1453">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="24674-1454">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="24674-1454">Az.Advisor</span></span>
* <span data-ttu-id="24674-1455">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="24674-1455">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-1456">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-1456">Az.Batch</span></span>
* <span data-ttu-id="24674-1457">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="24674-1457">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="24674-1458">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="24674-1458">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="24674-1459">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="24674-1459">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="24674-1460">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="24674-1460">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="24674-1461">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="24674-1461">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="24674-1462">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="24674-1462">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="24674-1463">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="24674-1463">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="24674-1464">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="24674-1464">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="24674-1465">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="24674-1465">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="24674-1466">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-1466">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="24674-1467">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="24674-1467">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="24674-1468">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="24674-1468">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="24674-1469">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="24674-1469">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="24674-1470">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="24674-1470">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="24674-1471">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-1471">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="24674-1472">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="24674-1472">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="24674-1473">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="24674-1473">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="24674-1474">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-1474">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="24674-1475">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="24674-1475">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="24674-1476">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="24674-1476">This operation is no longer supported.</span></span>
* <span data-ttu-id="24674-1477">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="24674-1477">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="24674-1478">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="24674-1478">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="24674-1479">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="24674-1479">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="24674-1480">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="24674-1480">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="24674-1481">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="24674-1481">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="24674-1482">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="24674-1482">New non-verified images are also now returned.</span></span> <span data-ttu-id="24674-1483">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24674-1483">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="24674-1484">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="24674-1484">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="24674-1485">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="24674-1485">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="24674-1486">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="24674-1486">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="24674-1487">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="24674-1487">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="24674-1488">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="24674-1488">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="24674-1489">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="24674-1489">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="24674-1490">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="24674-1490">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="24674-1491">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="24674-1491">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="24674-1492">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="24674-1492">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-1493">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-1493">Az.Cdn</span></span>
* <span data-ttu-id="24674-1494">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="24674-1494">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="24674-1495">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="24674-1495">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1496">Az.Compute</span></span>
* <span data-ttu-id="24674-1497">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="24674-1497">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="24674-1498">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="24674-1498">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="24674-1499">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="24674-1499">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="24674-1500">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1500">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="24674-1501">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1501">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="24674-1502">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="24674-1502">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="24674-1503">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1503">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="24674-1504">重大變更</span><span class="sxs-lookup"><span data-stu-id="24674-1504">Breaking changes</span></span>
    - <span data-ttu-id="24674-1505">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="24674-1505">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="24674-1506">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="24674-1506">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1507">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1507">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1508">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="24674-1508">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-1509">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-1509">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-1510">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="24674-1510">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="24674-1511">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="24674-1511">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="24674-1512">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="24674-1512">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="24674-1513">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="24674-1513">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="24674-1514">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="24674-1514">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="24674-1515">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-1515">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-1516">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-1516">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-1517">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="24674-1517">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-1518">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-1518">Az.HDInsight</span></span>
* <span data-ttu-id="24674-1519">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="24674-1519">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="24674-1520">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="24674-1520">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="24674-1521">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="24674-1521">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="24674-1522">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1522">Removed five cmdlets:</span></span>
    - <span data-ttu-id="24674-1523">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="24674-1523">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="24674-1524">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="24674-1524">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="24674-1525">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="24674-1525">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="24674-1526">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="24674-1526">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="24674-1527">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="24674-1527">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="24674-1528">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1528">Added three cmdlets:</span></span>
    - <span data-ttu-id="24674-1529">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="24674-1529">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="24674-1530">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="24674-1530">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="24674-1531">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="24674-1531">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="24674-1532">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="24674-1532">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="24674-1533">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="24674-1533">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="24674-1534">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="24674-1534">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="24674-1535">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="24674-1535">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="24674-1536">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="24674-1536">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="24674-1537">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="24674-1537">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="24674-1538">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="24674-1538">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="24674-1539">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="24674-1539">Added some scenario test cases.</span></span>
* <span data-ttu-id="24674-1540">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="24674-1540">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-1541">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-1541">Az.IotHub</span></span>
* <span data-ttu-id="24674-1542">重大變更：</span><span class="sxs-lookup"><span data-stu-id="24674-1542">Breaking changes:</span></span>
    - <span data-ttu-id="24674-1543">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="24674-1543">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="24674-1544">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="24674-1544">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="24674-1545">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="24674-1545">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="24674-1546">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="24674-1546">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="24674-1547">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="24674-1547">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="24674-1548">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="24674-1548">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="24674-1549">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="24674-1549">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="24674-1550">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="24674-1550">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="24674-1551">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="24674-1551">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="24674-1552">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="24674-1552">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="24674-1553">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="24674-1553">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="24674-1554">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="24674-1554">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1555">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1556">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="24674-1556">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="24674-1557">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="24674-1557">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="24674-1558">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="24674-1558">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="24674-1559">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="24674-1559">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="24674-1560">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="24674-1560">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="24674-1561">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="24674-1561">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="24674-1562">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="24674-1562">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="24674-1563">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1563">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="24674-1564">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="24674-1564">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1565">Az.Resources</span></span>
* <span data-ttu-id="24674-1566">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="24674-1566">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1567">Az.Network</span></span>
* <span data-ttu-id="24674-1568">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="24674-1568">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="24674-1569">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1569">Updated cmdlet:</span></span>
        - <span data-ttu-id="24674-1570">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1570">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1571">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1571">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1572">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1572">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1573">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1573">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1574">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1574">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="24674-1575">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="24674-1575">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="24674-1576">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1576">New cmdlet:</span></span>
        - <span data-ttu-id="24674-1577">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="24674-1577">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="24674-1578">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="24674-1578">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="24674-1579">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="24674-1579">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="24674-1580">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="24674-1580">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="24674-1581">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="24674-1581">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="24674-1582">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="24674-1582">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="24674-1583">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="24674-1583">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="24674-1584">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="24674-1584">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="24674-1585">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1585">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-1586">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="24674-1586">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="24674-1587">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="24674-1587">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="24674-1588">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="24674-1588">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="24674-1589">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="24674-1589">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="24674-1590">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="24674-1590">Set-AzVirtualHub</span></span>
* <span data-ttu-id="24674-1591">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="24674-1591">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="24674-1592">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="24674-1592">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="24674-1593">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="24674-1593">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="24674-1594">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="24674-1594">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="24674-1595">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="24674-1595">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="24674-1596">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="24674-1596">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="24674-1597">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1597">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="24674-1598">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1598">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-1599">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1599">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="24674-1600">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="24674-1600">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="24674-1601">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="24674-1601">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="24674-1602">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="24674-1602">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="24674-1603">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="24674-1603">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="24674-1604">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="24674-1604">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="24674-1605">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="24674-1605">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="24674-1606">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1606">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="24674-1607">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1607">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-1608">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="24674-1608">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="24674-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="24674-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="24674-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="24674-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="24674-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="24674-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="24674-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="24674-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="24674-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="24674-1614">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="24674-1614">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="24674-1615">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="24674-1615">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="24674-1616">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1616">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="24674-1617">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="24674-1617">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="24674-1618">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1618">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="24674-1619">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="24674-1619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="24674-1620">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="24674-1620">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="24674-1621">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="24674-1621">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="24674-1622">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="24674-1622">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="24674-1623">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="24674-1623">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="24674-1624">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="24674-1624">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="24674-1625">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1625">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-1626">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="24674-1626">New-AzIpGroup</span></span>
        - <span data-ttu-id="24674-1627">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="24674-1627">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="24674-1628">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="24674-1628">Get-AzIpGroup</span></span>
        - <span data-ttu-id="24674-1629">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="24674-1629">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-1630">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-1630">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-1631">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="24674-1631">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1632">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1632">Az.Sql</span></span>
* <span data-ttu-id="24674-1633">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1633">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="24674-1634">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-1634">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="24674-1635">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="24674-1635">Removed deprecated aliases:</span></span>
* <span data-ttu-id="24674-1636">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="24674-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="24674-1637">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="24674-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="24674-1638">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1638">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="24674-1639">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="24674-1639">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="24674-1640">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1640">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="24674-1641">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="24674-1641">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1642">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1642">Az.Storage</span></span>
* <span data-ttu-id="24674-1643">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="24674-1643">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="24674-1644">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-1644">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="24674-1645">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-1645">Set-AzStorageAccount</span></span>
* <span data-ttu-id="24674-1646">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="24674-1646">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="24674-1647">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="24674-1647">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="24674-1648">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="24674-1648">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="24674-1649">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="24674-1649">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="24674-1650">一般</span><span class="sxs-lookup"><span data-stu-id="24674-1650">General</span></span>
* <span data-ttu-id="24674-1651">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="24674-1651">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-1652">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1652">Az.Accounts</span></span>
* <span data-ttu-id="24674-1653">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="24674-1653">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-1654">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-1654">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-1655">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1655">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="24674-1656">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-1656">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-1657">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-1657">Az.Automation</span></span>
* <span data-ttu-id="24674-1658">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-1658">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-1659">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-1659">Az.Batch</span></span>
* <span data-ttu-id="24674-1660">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="24674-1660">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1661">Az.Compute</span></span>
* <span data-ttu-id="24674-1662">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="24674-1662">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="24674-1663">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="24674-1663">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="24674-1664">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="24674-1664">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="24674-1665">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="24674-1665">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1666">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1666">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1667">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="24674-1667">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="24674-1668">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="24674-1668">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="24674-1669">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="24674-1669">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-1670">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-1670">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-1671">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-1671">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="24674-1672">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="24674-1672">Az.HealthcareApis</span></span>
* <span data-ttu-id="24674-1673">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="24674-1673">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="24674-1674">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="24674-1674">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="24674-1675">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="24674-1675">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="24674-1676">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="24674-1676">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-1677">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-1677">Az.IotHub</span></span>
* <span data-ttu-id="24674-1678">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="24674-1678">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="24674-1679">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="24674-1679">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1680">Az.Monitor</span></span>
* <span data-ttu-id="24674-1681">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="24674-1681">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="24674-1682">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="24674-1682">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="24674-1683">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="24674-1683">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="24674-1684">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="24674-1684">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1685">Az.Network</span></span>
* <span data-ttu-id="24674-1686">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="24674-1686">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="24674-1687">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1687">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="24674-1688">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1688">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-1689">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-1689">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="24674-1690">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1690">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="24674-1691">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1691">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="24674-1692">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1692">Updated cmdlets:</span></span>
        - <span data-ttu-id="24674-1693">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1693">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="24674-1694">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1694">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="24674-1695">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1695">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="24674-1696">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="24674-1696">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="24674-1697">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="24674-1697">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="24674-1698">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="24674-1698">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="24674-1699">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="24674-1699">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="24674-1700">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="24674-1700">Az.RedisCache</span></span>
* <span data-ttu-id="24674-1701">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="24674-1701">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1702">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1702">Az.Sql</span></span>
* <span data-ttu-id="24674-1703">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1703">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1704">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1704">Az.Storage</span></span>
* <span data-ttu-id="24674-1705">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="24674-1705">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="24674-1706">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="24674-1706">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="24674-1707">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24674-1707">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="24674-1708">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="24674-1708">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="24674-1709">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-1709">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="24674-1710">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="24674-1710">Az.StorageSync</span></span>
* <span data-ttu-id="24674-1711">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="24674-1711">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-1712">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1712">Az.Websites</span></span>
* <span data-ttu-id="24674-1713">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="24674-1713">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="24674-1714">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="24674-1714">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="24674-1715">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-1715">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-1716">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="24674-1716">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="24674-1717">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="24674-1717">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="24674-1718">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="24674-1718">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-1719">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-1719">Az.Automation</span></span>
* <span data-ttu-id="24674-1720">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="24674-1720">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="24674-1721">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="24674-1721">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="24674-1722">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="24674-1722">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1723">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1723">Az.Compute</span></span>
* <span data-ttu-id="24674-1724">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="24674-1724">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="24674-1725">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="24674-1725">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="24674-1726">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="24674-1726">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="24674-1727">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="24674-1727">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="24674-1728">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="24674-1728">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="24674-1729">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="24674-1729">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="24674-1730">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="24674-1730">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="24674-1731">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="24674-1731">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="24674-1732">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="24674-1732">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1733">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1733">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1734">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="24674-1734">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="24674-1735">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="24674-1735">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-1736">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-1736">Az.HDInsight</span></span>
* <span data-ttu-id="24674-1737">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="24674-1737">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-1738">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-1738">Az.IotHub</span></span>
* <span data-ttu-id="24674-1739">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1739">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="24674-1740">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1740">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="24674-1741">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="24674-1741">New cmdlets are:</span></span>
    - <span data-ttu-id="24674-1742">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="24674-1742">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="24674-1743">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="24674-1743">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="24674-1744">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="24674-1744">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="24674-1745">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="24674-1745">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1746">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1746">Az.Monitor</span></span>
* <span data-ttu-id="24674-1747">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="24674-1747">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="24674-1748">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="24674-1748">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="24674-1749">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="24674-1749">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="24674-1750">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="24674-1750">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="24674-1751">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="24674-1751">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="24674-1752">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="24674-1752">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="24674-1753">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="24674-1753">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="24674-1754">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="24674-1754">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="24674-1755">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="24674-1755">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="24674-1756">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="24674-1756">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="24674-1757">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="24674-1757">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="24674-1758">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="24674-1758">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="24674-1759">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="24674-1759">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="24674-1760">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="24674-1760">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="24674-1761">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="24674-1761">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="24674-1762">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="24674-1762">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="24674-1763">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="24674-1763">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="24674-1764">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="24674-1764">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="24674-1765">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1765">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="24674-1766">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="24674-1766">Overall improved help files</span></span>
* <span data-ttu-id="24674-1767">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-1767">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1768">Az.Network</span></span>
* <span data-ttu-id="24674-1769">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1769">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="24674-1770">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="24674-1770">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="24674-1771">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="24674-1771">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="24674-1772">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="24674-1772">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="24674-1773">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="24674-1773">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="24674-1774">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="24674-1774">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="24674-1775">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="24674-1775">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="24674-1776">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="24674-1776">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="24674-1777">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="24674-1777">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="24674-1778">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="24674-1778">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="24674-1779">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="24674-1779">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="24674-1780">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="24674-1780">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="24674-1781">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1781">New cmdlets</span></span>
        - <span data-ttu-id="24674-1782">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="24674-1782">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="24674-1783">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1783">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="24674-1784">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1784">Updated cmdlet:</span></span>
        - <span data-ttu-id="24674-1785">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="24674-1785">New-VpnSite</span></span>
        - <span data-ttu-id="24674-1786">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="24674-1786">Update-VpnSite</span></span>
        - <span data-ttu-id="24674-1787">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1787">New-VpnConnection</span></span>
        - <span data-ttu-id="24674-1788">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1788">Update-VpnConnection</span></span>
* <span data-ttu-id="24674-1789">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1789">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1791">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="24674-1791">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="24674-1792">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="24674-1792">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1793">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1793">Az.Resources</span></span>
* <span data-ttu-id="24674-1794">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="24674-1794">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-1795">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-1795">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-1796">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1796">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="24674-1797">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="24674-1797">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="24674-1798">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="24674-1798">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="24674-1799">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="24674-1799">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="24674-1800">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="24674-1800">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="24674-1801">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="24674-1801">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="24674-1802">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="24674-1802">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="24674-1803">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="24674-1803">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="24674-1804">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="24674-1804">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="24674-1805">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="24674-1805">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="24674-1806">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="24674-1806">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="24674-1807">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="24674-1807">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="24674-1808">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="24674-1808">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="24674-1809">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="24674-1809">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="24674-1810">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="24674-1810">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="24674-1811">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="24674-1811">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="24674-1812">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="24674-1812">Az.SignalR</span></span>
* <span data-ttu-id="24674-1813">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1813">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1814">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1814">Az.Sql</span></span>
* <span data-ttu-id="24674-1815">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1815">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="24674-1816">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="24674-1816">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="24674-1817">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="24674-1817">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="24674-1818">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="24674-1818">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="24674-1819">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="24674-1819">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1820">Az.Storage</span></span>
* <span data-ttu-id="24674-1821">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1821">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="24674-1822">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="24674-1822">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="24674-1823">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="24674-1823">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="24674-1824">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="24674-1824">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="24674-1825">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-1825">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="24674-1826">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="24674-1826">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="24674-1827">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="24674-1827">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="24674-1828">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24674-1828">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="24674-1829">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24674-1829">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="24674-1830">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24674-1830">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="24674-1831">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24674-1831">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-1832">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1832">Az.Websites</span></span>
* <span data-ttu-id="24674-1833">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="24674-1833">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="24674-1834">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="24674-1834">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="24674-1835">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1835">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="24674-1836">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="24674-1836">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="24674-1837">一般</span><span class="sxs-lookup"><span data-stu-id="24674-1837">General</span></span>
* <span data-ttu-id="24674-1838">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="24674-1838">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1839">Az.Accounts</span></span>
* <span data-ttu-id="24674-1840">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="24674-1840">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-1841">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-1841">Az.Aks</span></span>
* <span data-ttu-id="24674-1842">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="24674-1842">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="24674-1843">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="24674-1843">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-1844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-1844">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-1845">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-1845">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="24674-1846">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="24674-1846">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="24674-1847">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1847">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="24674-1848">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="24674-1848">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="24674-1849">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="24674-1849">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-1850">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-1850">Az.Batch</span></span>
* <span data-ttu-id="24674-1851">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="24674-1851">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-1852">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-1852">Az.Cdn</span></span>
* <span data-ttu-id="24674-1853">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1853">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1854">Az.Compute</span></span>
* <span data-ttu-id="24674-1855">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1855">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="24674-1856">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="24674-1856">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="24674-1857">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="24674-1857">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="24674-1858">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="24674-1858">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="24674-1859">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="24674-1859">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="24674-1860">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="24674-1860">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="24674-1861">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="24674-1861">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="24674-1862">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="24674-1862">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1863">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1863">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1864">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="24674-1864">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="24674-1865">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="24674-1865">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="24674-1866">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="24674-1866">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="24674-1867">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="24674-1867">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-1868">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-1868">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-1869">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="24674-1869">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-1870">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-1870">Az.EventHub</span></span>
* <span data-ttu-id="24674-1871">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="24674-1871">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="24674-1872">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="24674-1872">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="24674-1873">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1873">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="24674-1874">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="24674-1874">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="24674-1875">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="24674-1875">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="24674-1876">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="24674-1876">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-1877">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-1877">Az.Monitor</span></span>
* <span data-ttu-id="24674-1878">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="24674-1878">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1879">Az.Network</span></span>
* <span data-ttu-id="24674-1880">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1880">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="24674-1881">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="24674-1881">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="24674-1882">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="24674-1882">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="24674-1883">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="24674-1883">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="24674-1884">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="24674-1884">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="24674-1885">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="24674-1885">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="24674-1886">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="24674-1886">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-1888">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="24674-1888">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="24674-1889">新增了範例</span><span class="sxs-lookup"><span data-stu-id="24674-1889">Added example</span></span>
    - <span data-ttu-id="24674-1890">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="24674-1890">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="24674-1891">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="24674-1891">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="24674-1892">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="24674-1892">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1893">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1893">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1894">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1894">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1895">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1895">Az.Resources</span></span>
* <span data-ttu-id="24674-1896">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1896">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="24674-1897">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1897">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="24674-1898">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="24674-1898">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="24674-1899">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="24674-1899">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="24674-1900">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="24674-1900">Az.ServiceBus</span></span>
* <span data-ttu-id="24674-1901">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1901">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="24674-1902">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="24674-1902">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="24674-1903">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="24674-1903">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-1904">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-1904">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-1905">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="24674-1905">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="24674-1906">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="24674-1906">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="24674-1907">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="24674-1907">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="24674-1908">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="24674-1908">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="24674-1909">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="24674-1909">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="24674-1910">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1910">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1911">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1911">Az.Sql</span></span>
* <span data-ttu-id="24674-1912">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="24674-1912">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-1913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-1913">Az.Storage</span></span>
* <span data-ttu-id="24674-1914">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="24674-1914">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="24674-1915">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="24674-1915">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="24674-1916">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="24674-1916">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="24674-1917">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="24674-1917">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="24674-1918">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="24674-1918">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="24674-1919">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="24674-1919">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-1920">Az.Websites</span></span>
* <span data-ttu-id="24674-1921">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="24674-1921">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="24674-1922">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="24674-1922">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-1923">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-1923">Az.Accounts</span></span>
* <span data-ttu-id="24674-1924">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="24674-1924">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="24674-1925">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="24674-1925">Az.ApplicationInsights</span></span>
* <span data-ttu-id="24674-1926">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1926">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-1927">Az.Automation</span></span>
* <span data-ttu-id="24674-1928">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1928">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-1929">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-1929">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-1930">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="24674-1930">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-1931">Az.Compute</span></span>
* <span data-ttu-id="24674-1932">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="24674-1932">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="24674-1933">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24674-1933">Az.ContainerRegistry</span></span>
* <span data-ttu-id="24674-1934">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1934">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="24674-1935">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="24674-1935">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-1936">Az.DataFactory</span></span>
* <span data-ttu-id="24674-1937">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="24674-1937">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="24674-1938">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-1938">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-1939">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-1939">Az.EventHub</span></span>
* <span data-ttu-id="24674-1940">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="24674-1940">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="24674-1941">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1941">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-1942">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-1942">Az.KeyVault</span></span>
* <span data-ttu-id="24674-1943">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1943">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="24674-1944">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="24674-1944">Az.LogicApp</span></span>
* <span data-ttu-id="24674-1945">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="24674-1945">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="24674-1946">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="24674-1946">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="24674-1947">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="24674-1947">Az.ManagedServices</span></span>
* <span data-ttu-id="24674-1948">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1948">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-1949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-1949">Az.Network</span></span>
* <span data-ttu-id="24674-1950">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="24674-1950">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="24674-1951">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1951">New cmdlets</span></span>
        - <span data-ttu-id="24674-1952">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24674-1952">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="24674-1953">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="24674-1953">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="24674-1954">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1954">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1955">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1955">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1956">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1956">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1957">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-1957">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="24674-1958">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="24674-1958">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="24674-1959">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="24674-1959">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="24674-1960">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="24674-1960">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="24674-1961">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1961">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="24674-1962">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="24674-1962">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="24674-1963">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="24674-1963">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="24674-1964">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="24674-1964">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="24674-1965">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="24674-1965">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="24674-1966">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1966">Updated cmdlets</span></span>
        - <span data-ttu-id="24674-1967">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1967">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="24674-1968">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1968">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="24674-1969">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1969">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="24674-1970">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="24674-1970">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="24674-1971">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="24674-1971">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="24674-1972">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-1972">Updated cmdlet:</span></span>
        - <span data-ttu-id="24674-1973">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1973">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="24674-1974">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1974">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="24674-1975">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="24674-1975">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="24674-1976">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="24674-1976">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="24674-1977">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="24674-1977">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="24674-1978">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="24674-1978">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-1979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-1979">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-1980">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="24674-1980">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="24674-1981">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="24674-1981">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-1983">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1983">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="24674-1984">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1984">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="24674-1985">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1985">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="24674-1986">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1986">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="24674-1987">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1987">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="24674-1988">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1988">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="24674-1989">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1989">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="24674-1990">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1990">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="24674-1991">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="24674-1991">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="24674-1992">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="24674-1992">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-1993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-1993">Az.Resources</span></span>
- <span data-ttu-id="24674-1994">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-1994">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="24674-1995">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="24674-1995">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="24674-1996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="24674-1996">Az.ServiceBus</span></span>
* <span data-ttu-id="24674-1997">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="24674-1997">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="24674-1998">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-1998">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-1999">Az.Sql</span></span>
* <span data-ttu-id="24674-2000">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="24674-2000">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="24674-2001">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2001">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="24674-2002">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="24674-2002">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2003">Az.Storage</span></span>
* <span data-ttu-id="24674-2004">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="24674-2004">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="24674-2005">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="24674-2005">Az.StorageSync</span></span>
* <span data-ttu-id="24674-2006">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-2006">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="24674-2007">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="24674-2007">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2008">Az.Websites</span></span>
* <span data-ttu-id="24674-2009">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-2009">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="24674-2010">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="24674-2010">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="24674-2011">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-2011">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="24674-2012">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="24674-2012">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2013">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2013">Az.Accounts</span></span>
* <span data-ttu-id="24674-2014">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2014">Add support for profile cmdlets</span></span>
* <span data-ttu-id="24674-2015">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2015">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="24674-2016">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2016">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="24674-2017">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="24674-2017">Az.Advisor</span></span>
* <span data-ttu-id="24674-2018">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="24674-2018">GA release of Az.Advisor</span></span>
* <span data-ttu-id="24674-2019">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="24674-2019">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="24674-2020">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-2020">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-2021">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2021">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="24674-2022">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="24674-2022">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="24674-2023">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2023">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="24674-2024">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2024">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="24674-2025">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2025">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="24674-2026">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="24674-2026">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="24674-2027">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2027">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2028">Az.Automation</span></span>
* <span data-ttu-id="24674-2029">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="24674-2029">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2030">Az.Compute</span></span>
* <span data-ttu-id="24674-2031">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="24674-2031">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-2032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-2032">Az.DataFactory</span></span>
* <span data-ttu-id="24674-2033">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="24674-2033">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="24674-2034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="24674-2034">Az.EventGrid</span></span>
* <span data-ttu-id="24674-2035">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-2035">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-2036">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-2036">Az.IotHub</span></span>
* <span data-ttu-id="24674-2037">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2037">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2038">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2038">Az.Network</span></span>
* <span data-ttu-id="24674-2039">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="24674-2039">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="24674-2040">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="24674-2040">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-2041">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2041">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-2042">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="24674-2042">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="24674-2043">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="24674-2043">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-2045">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="24674-2045">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2046">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2047">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="24674-2047">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2048">Az.Resources</span></span>
    - <span data-ttu-id="24674-2049">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="24674-2049">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="24674-2050">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="24674-2050">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="24674-2051">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="24674-2051">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="24674-2052">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="24674-2052">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="24674-2053">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="24674-2053">Az.ServiceBus</span></span>
* <span data-ttu-id="24674-2054">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="24674-2054">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2055">Az.Sql</span></span>
* <span data-ttu-id="24674-2056">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="24674-2056">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="24674-2057">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="24674-2057">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="24674-2058">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="24674-2058">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="24674-2059">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="24674-2059">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="24674-2060">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="24674-2060">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="24674-2061">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="24674-2061">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="24674-2062">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="24674-2062">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="24674-2063">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="24674-2063">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="24674-2064">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="24674-2064">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2065">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2065">Az.Storage</span></span>
* <span data-ttu-id="24674-2066">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="24674-2066">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="24674-2067">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="24674-2067">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="24674-2068">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="24674-2068">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="24674-2069">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="24674-2069">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="24674-2070">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="24674-2070">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="24674-2071">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2071">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="24674-2072">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2072">Set-AzStorageAccount</span></span>
* <span data-ttu-id="24674-2073">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="24674-2073">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="24674-2074">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="24674-2074">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="24674-2075">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="24674-2075">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="24674-2076">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="24674-2076">Az.StorageSync</span></span>
* <span data-ttu-id="24674-2077">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="24674-2077">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="24674-2078">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="24674-2078">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2079">Az.Accounts</span></span>
* <span data-ttu-id="24674-2080">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-2080">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="24674-2081">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="24674-2081">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="24674-2082">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="24674-2082">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="24674-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="24674-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="24674-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="24674-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2085">Az.Compute</span></span>
* <span data-ttu-id="24674-2086">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="24674-2086">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="24674-2087">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-2087">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="24674-2088">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="24674-2088">Az.Dns</span></span>
* <span data-ttu-id="24674-2089">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="24674-2089">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="24674-2090">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="24674-2090">Az.EventGrid</span></span>
* <span data-ttu-id="24674-2091">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="24674-2091">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="24674-2092">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-2092">New cmdlets:</span></span>
    - <span data-ttu-id="24674-2093">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="24674-2093">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="24674-2094">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="24674-2094">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="24674-2095">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="24674-2095">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="24674-2096">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="24674-2096">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="24674-2097">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="24674-2097">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="24674-2098">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="24674-2098">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="24674-2099">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="24674-2099">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="24674-2100">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="24674-2100">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="24674-2101">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="24674-2101">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="24674-2102">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="24674-2102">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="24674-2103">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="24674-2103">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="24674-2104">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="24674-2104">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="24674-2105">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="24674-2105">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="24674-2106">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="24674-2106">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="24674-2107">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="24674-2107">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="24674-2108">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="24674-2108">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="24674-2109">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-2109">Updated cmdlets:</span></span>
    - <span data-ttu-id="24674-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="24674-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="24674-2111">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="24674-2111">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="24674-2112">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="24674-2112">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="24674-2113">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="24674-2113">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="24674-2114">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="24674-2114">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="24674-2115">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="24674-2115">Event subscription expiration date,</span></span>
            - <span data-ttu-id="24674-2116">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="24674-2116">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="24674-2117">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="24674-2117">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="24674-2118">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="24674-2118">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="24674-2119">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="24674-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="24674-2120">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="24674-2120">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="24674-2121">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="24674-2121">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="24674-2122">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="24674-2122">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="24674-2123">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="24674-2123">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-2124">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-2124">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-2125">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="24674-2125">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="24674-2126">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="24674-2126">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="24674-2127">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="24674-2127">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="24674-2128">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="24674-2128">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2129">Az.Network</span></span>
* <span data-ttu-id="24674-2130">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2130">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="24674-2131">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2131">New cmdlets</span></span>
        - <span data-ttu-id="24674-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="24674-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="24674-2133">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="24674-2133">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="24674-2134">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2134">New cmdlets</span></span>
        - <span data-ttu-id="24674-2135">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="24674-2135">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="24674-2136">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="24674-2136">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="24674-2137">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2137">New cmdlets</span></span>
        - <span data-ttu-id="24674-2138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="24674-2138">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="24674-2139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="24674-2139">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="24674-2140">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="24674-2140">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="24674-2141">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="24674-2141">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="24674-2142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="24674-2142">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="24674-2143">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24674-2143">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="24674-2144">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2144">New cmdlets</span></span>
        - <span data-ttu-id="24674-2145">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24674-2145">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="24674-2146">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24674-2146">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="24674-2147">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24674-2147">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="24674-2148">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="24674-2148">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="24674-2149">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="24674-2149">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="24674-2150">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="24674-2150">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="24674-2151">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="24674-2151">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="24674-2152">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="24674-2152">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="24674-2153">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="24674-2153">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="24674-2154">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="24674-2154">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="24674-2155">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-2155">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="24674-2156">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="24674-2156">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="24674-2157">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2157">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="24674-2158">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="24674-2158">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="24674-2159">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="24674-2159">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="24674-2160">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2160">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="24674-2161">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="24674-2161">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="24674-2162">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2162">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="24674-2163">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-2163">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="24674-2164">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="24674-2164">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="24674-2165">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="24674-2165">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="24674-2166">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="24674-2166">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="24674-2167">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="24674-2167">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="24674-2168">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="24674-2168">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="24674-2169">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="24674-2169">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="24674-2170">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="24674-2170">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="24674-2171">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="24674-2171">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-2172">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2172">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-2173">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="24674-2173">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2174">Az.Resources</span></span>
* <span data-ttu-id="24674-2175">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="24674-2175">Support for additional Template Export options</span></span>
    - <span data-ttu-id="24674-2176">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24674-2176">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="24674-2177">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24674-2177">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="24674-2178">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="24674-2178">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-2179">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-2179">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-2180">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2180">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2181">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2181">Az.Sql</span></span>
* <span data-ttu-id="24674-2182">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="24674-2182">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="24674-2183">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="24674-2183">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="24674-2184">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="24674-2184">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="24674-2185">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="24674-2185">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="24674-2186">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="24674-2186">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="24674-2187">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="24674-2187">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="24674-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="24674-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="24674-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="24674-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2190">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2190">Az.Storage</span></span>
* <span data-ttu-id="24674-2191">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="24674-2191">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="24674-2192">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2192">New-AzStorageAccount</span></span>
* <span data-ttu-id="24674-2193">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="24674-2193">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="24674-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2195">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2195">Az.Websites</span></span>
* <span data-ttu-id="24674-2196">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="24674-2196">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="24674-2197">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="24674-2197">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="24674-2198">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="24674-2198">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="24674-2199">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-2199">Az.Cdn</span></span>
* <span data-ttu-id="24674-2200">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="24674-2200">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2201">Az.Compute</span></span>
* <span data-ttu-id="24674-2202">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="24674-2202">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="24674-2203">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="24674-2203">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-2204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-2204">Az.EventHub</span></span>
* <span data-ttu-id="24674-2205">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="24674-2205">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="24674-2206">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24674-2206">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2207">Az.Network</span></span>
* <span data-ttu-id="24674-2208">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="24674-2208">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="24674-2209">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="24674-2209">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-2210">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2210">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-2211">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="24674-2211">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2212">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2212">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2213">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="24674-2213">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="24674-2214">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="24674-2214">Az.ServiceBus</span></span>
* <span data-ttu-id="24674-2215">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24674-2215">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-2216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-2216">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-2217">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-2217">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="24674-2218">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="24674-2218">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2219">Az.Sql</span></span>
* <span data-ttu-id="24674-2220">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="24674-2220">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="24674-2221">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2221">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="24674-2222">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="24674-2222">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="24674-2223">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="24674-2223">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2224">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2224">Az.Websites</span></span>
* <span data-ttu-id="24674-2225">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2225">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="24674-2226">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="24674-2226">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="24674-2227">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-2227">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-2228">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="24674-2228">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="24674-2229">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="24674-2229">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="24674-2230">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="24674-2230">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="24674-2231">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="24674-2231">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="24674-2232">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="24674-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="24674-2233">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="24674-2233">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="24674-2234">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="24674-2234">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="24674-2235">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="24674-2235">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="24674-2236">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="24674-2236">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="24674-2237">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="24674-2237">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="24674-2238">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="24674-2238">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="24674-2239">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="24674-2239">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="24674-2240">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="24674-2240">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="24674-2241">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-2241">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="24674-2242">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-2242">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="24674-2243">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-2243">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="24674-2244">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-2244">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="24674-2245">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="24674-2245">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="24674-2246">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="24674-2246">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="24674-2247">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="24674-2247">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="24674-2248">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="24674-2248">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="24674-2249">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="24674-2249">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="24674-2250">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="24674-2250">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="24674-2251">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="24674-2251">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="24674-2252">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2252">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="24674-2253">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2253">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="24674-2254">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="24674-2254">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="24674-2255">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="24674-2255">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="24674-2256">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2256">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="24674-2257">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="24674-2257">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="24674-2258">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-2258">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="24674-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="24674-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="24674-2260">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="24674-2260">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="24674-2261">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="24674-2261">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="24674-2262">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="24674-2262">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="24674-2263">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-2263">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="24674-2264">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-2264">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="24674-2265">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="24674-2265">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="24674-2266">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="24674-2266">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="24674-2267">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="24674-2267">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="24674-2268">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="24674-2268">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="24674-2269">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="24674-2269">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="24674-2270">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="24674-2270">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="24674-2271">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="24674-2271">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="24674-2272">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="24674-2272">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="24674-2273">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="24674-2273">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="24674-2274">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="24674-2274">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="24674-2275">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="24674-2275">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="24674-2276">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="24674-2276">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="24674-2277">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="24674-2277">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="24674-2278">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="24674-2278">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="24674-2279">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="24674-2279">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="24674-2280">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="24674-2280">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="24674-2281">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="24674-2281">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="24674-2282">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="24674-2282">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="24674-2283">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="24674-2283">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="24674-2284">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="24674-2284">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="24674-2285">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="24674-2285">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="24674-2286">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="24674-2286">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="24674-2287">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2287">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="24674-2288">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="24674-2288">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="24674-2289">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="24674-2289">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="24674-2290">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="24674-2290">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="24674-2291">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2291">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="24674-2292">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="24674-2292">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="24674-2293">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="24674-2293">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="24674-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="24674-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="24674-2295">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="24674-2295">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="24674-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="24674-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="24674-2297">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="24674-2297">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="24674-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="24674-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="24674-2299">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="24674-2299">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="24674-2300">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="24674-2300">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="24674-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="24674-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="24674-2302">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="24674-2302">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="24674-2303">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="24674-2303">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="24674-2304">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="24674-2304">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2305">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2305">Az.Automation</span></span>
* <span data-ttu-id="24674-2306">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="24674-2306">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="24674-2307">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2307">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="24674-2308">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2308">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="24674-2309">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="24674-2309">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="24674-2310">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2310">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="24674-2311">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2311">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="24674-2312">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="24674-2312">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2313">Az.Compute</span></span>
* <span data-ttu-id="24674-2314">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-2314">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="24674-2315">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="24674-2315">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-2316">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2316">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-2317">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="24674-2317">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-2318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-2318">Az.Monitor</span></span>
* <span data-ttu-id="24674-2319">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="24674-2319">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2320">Az.Network</span></span>
* <span data-ttu-id="24674-2321">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="24674-2321">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="24674-2322">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-2322">Updated cmdlet:</span></span>
        - <span data-ttu-id="24674-2323">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="24674-2323">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="24674-2324">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="24674-2324">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2325">Az.Resources</span></span>
* <span data-ttu-id="24674-2326">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="24674-2326">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2327">Az.Sql</span></span>
* <span data-ttu-id="24674-2328">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="24674-2328">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="24674-2329">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="24674-2329">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2330">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2330">Az.Accounts</span></span>
* <span data-ttu-id="24674-2331">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="24674-2331">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-2332">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-2332">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-2333">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="24674-2333">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="24674-2334">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-2334">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2335">Az.Compute</span></span>
* <span data-ttu-id="24674-2336">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="24674-2336">Proximity placement group feature.</span></span>
    - <span data-ttu-id="24674-2337">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="24674-2337">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="24674-2338">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="24674-2338">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="24674-2339">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="24674-2339">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="24674-2340">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="24674-2340">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="24674-2341">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24674-2341">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="24674-2342">重大變更</span><span class="sxs-lookup"><span data-stu-id="24674-2342">Breaking changes</span></span>
    - <span data-ttu-id="24674-2343">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="24674-2343">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="24674-2344">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="24674-2344">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="24674-2345">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="24674-2345">Az.DeploymentManager</span></span>
* <span data-ttu-id="24674-2346">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2346">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="24674-2347">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="24674-2347">Az.Dns</span></span>
* <span data-ttu-id="24674-2348">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="24674-2348">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="24674-2349">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="24674-2349">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="24674-2350">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24674-2350">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="24674-2351">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-2351">Az.FrontDoor</span></span>
* <span data-ttu-id="24674-2352">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2352">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="24674-2353">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="24674-2353">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="24674-2354">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-2354">Az.HDInsight</span></span>
* <span data-ttu-id="24674-2355">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-2355">Removed two cmdlets:</span></span>
    - <span data-ttu-id="24674-2356">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="24674-2356">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="24674-2357">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="24674-2357">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="24674-2358">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="24674-2358">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="24674-2359">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="24674-2359">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="24674-2360">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="24674-2360">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="24674-2361">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="24674-2361">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-2362">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-2362">Az.Monitor</span></span>
* <span data-ttu-id="24674-2363">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="24674-2363">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="24674-2364">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="24674-2364">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="24674-2365">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="24674-2365">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="24674-2366">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="24674-2366">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="24674-2367">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="24674-2367">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="24674-2368">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="24674-2368">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="24674-2369">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="24674-2369">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="24674-2370">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="24674-2370">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="24674-2371">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="24674-2371">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="24674-2372">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="24674-2372">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="24674-2373">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="24674-2373">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="24674-2374">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="24674-2374">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="24674-2375">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="24674-2375">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="24674-2376">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2376">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2377">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2377">Az.Network</span></span>
* <span data-ttu-id="24674-2378">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2378">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="24674-2379">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2379">New cmdlets</span></span>
        - <span data-ttu-id="24674-2380">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="24674-2380">New-AzNatGateway</span></span>
        - <span data-ttu-id="24674-2381">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="24674-2381">Get-AzNatGateway</span></span>
        - <span data-ttu-id="24674-2382">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="24674-2382">Set-AzNatGateway</span></span>
        - <span data-ttu-id="24674-2383">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="24674-2383">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="24674-2384">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2384">Updated cmdlets</span></span>
        - <span data-ttu-id="24674-2385">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="24674-2385">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="24674-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="24674-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="24674-2387">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="24674-2387">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="24674-2388">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="24674-2388">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="24674-2389">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="24674-2389">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-2390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2390">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-2391">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="24674-2391">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="24674-2392">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="24674-2392">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="24674-2393">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="24674-2393">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2394">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2394">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2395">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="24674-2395">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="24674-2396">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="24674-2396">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="24674-2397">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="24674-2397">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="24674-2398">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="24674-2398">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="24674-2399">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="24674-2399">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="24674-2400">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="24674-2400">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="24674-2401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="24674-2401">Az.Relay</span></span>
* <span data-ttu-id="24674-2402">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-2402">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="24674-2403">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="24674-2403">Az.ServiceBus</span></span>
* <span data-ttu-id="24674-2404">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2404">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2405">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2405">Az.Storage</span></span>
* <span data-ttu-id="24674-2406">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="24674-2406">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="24674-2407">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="24674-2407">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="24674-2408">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="24674-2408">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="24674-2409">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2409">New-AzStorageAccount</span></span>
* <span data-ttu-id="24674-2410">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="24674-2410">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="24674-2411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2411">New-AzStorageAccount</span></span>
    - <span data-ttu-id="24674-2412">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2412">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="24674-2413">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2413">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2414">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2414">Az.Websites</span></span>
* <span data-ttu-id="24674-2415">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="24674-2415">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="24674-2416">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="24674-2416">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="24674-2417">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="24674-2417">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="24674-2418">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-2418">Highlights since the last major release</span></span>
* <span data-ttu-id="24674-2419">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="24674-2419">General availability of `Az` module</span></span>
* <span data-ttu-id="24674-2420">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="24674-2420">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="24674-2421">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="24674-2421">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="24674-2422">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2422">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="24674-2423">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="24674-2423">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="24674-2424">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2424">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="24674-2425">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2425">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-2426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2426">Az.Accounts</span></span>
* <span data-ttu-id="24674-2427">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="24674-2427">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="24674-2428">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-2428">Az.Batch</span></span>
* <span data-ttu-id="24674-2429">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-2430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-2430">Az.Cdn</span></span>
* <span data-ttu-id="24674-2431">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-2432">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-2432">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-2433">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2433">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2434">Az.Compute</span></span>
* <span data-ttu-id="24674-2435">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="24674-2435">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="24674-2436">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="24674-2437">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="24674-2437">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-2438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-2438">Az.DataFactory</span></span>
* <span data-ttu-id="24674-2439">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="24674-2439">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-2441">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2441">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="24674-2442">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="24674-2442">Az.EventGrid</span></span>
* <span data-ttu-id="24674-2443">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-2443">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-2444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-2444">Az.EventHub</span></span>
* <span data-ttu-id="24674-2445">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2445">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="24674-2446">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="24674-2446">Az.HDInsight</span></span>
* <span data-ttu-id="24674-2447">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2447">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-2448">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-2448">Az.IotHub</span></span>
* <span data-ttu-id="24674-2449">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2449">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-2450">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-2450">Az.KeyVault</span></span>
* <span data-ttu-id="24674-2451">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2451">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="24674-2452">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="24674-2452">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="24674-2453">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="24674-2453">Az.MachineLearning</span></span>
* <span data-ttu-id="24674-2454">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="24674-2455">Az.Media</span><span class="sxs-lookup"><span data-stu-id="24674-2455">Az.Media</span></span>
* <span data-ttu-id="24674-2456">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-2457">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-2457">Az.Monitor</span></span>
  * <span data-ttu-id="24674-2458">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2458">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="24674-2459">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="24674-2459">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="24674-2460">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="24674-2460">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="24674-2461">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="24674-2461">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="24674-2462">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="24674-2462">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="24674-2463">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="24674-2463">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="24674-2464">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="24674-2464">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2465">Az.Network</span></span>
* <span data-ttu-id="24674-2466">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2466">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="24674-2467">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="24674-2467">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="24674-2468">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="24674-2468">Az.NotificationHubs</span></span>
* <span data-ttu-id="24674-2469">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2469">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-2470">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2470">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-2471">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2471">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="24674-2472">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="24674-2472">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="24674-2473">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2474">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2474">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2475">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="24674-2476">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="24674-2476">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="24674-2477">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="24674-2477">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="24674-2478">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="24674-2478">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="24674-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="24674-2479">Az.RedisCache</span></span>
* <span data-ttu-id="24674-2480">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2481">Az.Resources</span></span>
* <span data-ttu-id="24674-2482">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="24674-2482">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2483">Az.Sql</span></span>
* <span data-ttu-id="24674-2484">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="24674-2484">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="24674-2485">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2485">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="24674-2486">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="24674-2486">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="24674-2487">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="24674-2487">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="24674-2488">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="24674-2488">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="24674-2489">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="24674-2489">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="24674-2490">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="24674-2490">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2491">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2491">Az.Websites</span></span>
* <span data-ttu-id="24674-2492">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="24674-2492">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="24674-2493">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="24674-2494">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="24674-2494">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="24674-2495">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="24674-2495">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="24674-2496">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="24674-2496">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="24674-2497">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-2497">Highlights since the last major release</span></span>
* <span data-ttu-id="24674-2498">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="24674-2498">General availability of `Az` module</span></span>
* <span data-ttu-id="24674-2499">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="24674-2499">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="24674-2500">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="24674-2500">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="24674-2501">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2501">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="24674-2502">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="24674-2502">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="24674-2503">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2503">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="24674-2504">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2504">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="24674-2505">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2505">Az.Accounts</span></span>
* <span data-ttu-id="24674-2506">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="24674-2506">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="24674-2507">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="24674-2507">Az.AnalysisServices</span></span>
* <span data-ttu-id="24674-2508">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="24674-2508">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="24674-2509">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="24674-2509">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2510">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2510">Az.Automation</span></span>
* <span data-ttu-id="24674-2511">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="24674-2511">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="24674-2512">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="24674-2512">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="24674-2513">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="24674-2513">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2514">Az.Compute</span></span>
* <span data-ttu-id="24674-2515">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="24674-2515">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="24674-2516">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="24674-2516">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="24674-2517">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2517">Az.ContainerInstance</span></span>
* <span data-ttu-id="24674-2518">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="24674-2518">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-2519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-2519">Az.DataFactory</span></span>
* <span data-ttu-id="24674-2520">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="24674-2520">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="24674-2521">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-2521">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2522">Az.Resources</span></span>
* <span data-ttu-id="24674-2523">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="24674-2523">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="24674-2524">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="24674-2524">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="24674-2525">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="24674-2525">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="24674-2526">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="24674-2526">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="24674-2527">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="24674-2527">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="24674-2528">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="24674-2528">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2529">Az.Sql</span></span>
* <span data-ttu-id="24674-2530">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="24674-2530">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2531">Az.Storage</span></span>
* <span data-ttu-id="24674-2532">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="24674-2532">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="24674-2533">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="24674-2533">New-AzStorageContext</span></span>
* <span data-ttu-id="24674-2534">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="24674-2534">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="24674-2535">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="24674-2535">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="24674-2536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="24674-2536">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="24674-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="24674-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="24674-2539">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2539">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="24674-2540">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="24674-2540">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="24674-2541">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="24674-2541">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="24674-2542">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="24674-2542">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="24674-2543">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="24674-2543">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="24674-2544">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="24674-2544">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="24674-2545">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="24674-2545">Highlights since the last major release</span></span>
* <span data-ttu-id="24674-2546">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="24674-2546">General availability of `Az` module</span></span>
* <span data-ttu-id="24674-2547">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="24674-2547">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="24674-2548">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="24674-2548">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="24674-2549">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2549">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="24674-2550">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="24674-2550">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="24674-2551">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2551">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="24674-2552">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2552">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2553">Az.Automation</span></span>
* <span data-ttu-id="24674-2554">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="24674-2554">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="24674-2555">動態分組</span><span class="sxs-lookup"><span data-stu-id="24674-2555">Dynamic grouping</span></span>
    * <span data-ttu-id="24674-2556">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="24674-2556">Pre-Post script</span></span>
    * <span data-ttu-id="24674-2557">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="24674-2557">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2558">Az.Compute</span></span>
* <span data-ttu-id="24674-2559">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2559">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="24674-2560">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="24674-2560">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-2561">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-2561">Az.KeyVault</span></span>
* <span data-ttu-id="24674-2562">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2562">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2563">Az.Network</span></span>
* <span data-ttu-id="24674-2564">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="24674-2564">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="24674-2565">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="24674-2565">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2566">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2566">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2567">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="24674-2567">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="24674-2568">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="24674-2568">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2569">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2569">Az.Resources</span></span>
* <span data-ttu-id="24674-2570">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2570">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="24674-2571">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="24674-2571">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2572">Az.Sql</span></span>
* <span data-ttu-id="24674-2573">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="24674-2573">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2574">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2574">Az.Storage</span></span>
* <span data-ttu-id="24674-2575">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="24674-2575">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="24674-2576">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2576">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="24674-2577">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2577">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="24674-2578">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2578">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="24674-2579">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="24674-2579">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="24674-2580">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="24674-2580">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="24674-2581">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="24674-2581">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2582">Az.Websites</span></span>
* <span data-ttu-id="24674-2583">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="24674-2583">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="24674-2584">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="24674-2584">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2585">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2585">Az.Accounts</span></span>
* <span data-ttu-id="24674-2586">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2586">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="24674-2587">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="24674-2587">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2588">Az.Automation</span></span>
* <span data-ttu-id="24674-2589">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2589">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="24674-2590">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2590">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="24674-2591">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="24674-2591">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-2592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-2592">Az.Cdn</span></span>
* <span data-ttu-id="24674-2593">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2593">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2594">Az.Compute</span></span>
* <span data-ttu-id="24674-2595">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2595">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-2596">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-2596">Az.DataFactory</span></span>
* <span data-ttu-id="24674-2597">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="24674-2597">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="24674-2598">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="24674-2598">Az.LogicApp</span></span>
* <span data-ttu-id="24674-2599">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="24674-2599">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2600">Az.Network</span></span>
* <span data-ttu-id="24674-2601">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="24674-2601">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2602">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2602">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2603">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2603">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="24674-2604">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="24674-2604">SDK Update</span></span>
* <span data-ttu-id="24674-2605">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="24674-2605">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="24674-2606">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="24674-2606">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2607">Az.Resources</span></span>
* <span data-ttu-id="24674-2608">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2608">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="24674-2609">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="24674-2609">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="24674-2610">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2610">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="24674-2611">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="24674-2611">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="24674-2612">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2612">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="24674-2613">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="24674-2613">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2614">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2614">Az.Sql</span></span>
* <span data-ttu-id="24674-2615">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="24674-2615">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="24674-2616">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="24674-2616">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2617">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2617">Az.Storage</span></span>
* <span data-ttu-id="24674-2618">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24674-2618">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="24674-2619">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="24674-2619">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="24674-2620">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="24674-2620">Az.AnalysisServices</span></span>
* <span data-ttu-id="24674-2621">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2621">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2622">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2622">Az.Automation</span></span>
* <span data-ttu-id="24674-2623">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="24674-2623">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="24674-2624">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2624">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="24674-2625">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="24674-2625">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-2626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-2626">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-2627">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="24674-2627">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2628">Az.Compute</span></span>
* <span data-ttu-id="24674-2629">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="24674-2629">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="24674-2630">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="24674-2630">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="24674-2631">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2631">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="24674-2632">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="24674-2632">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-2633">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2633">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-2634">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2634">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="24674-2635">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="24674-2635">Az.EventHub</span></span>
* <span data-ttu-id="24674-2636">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="24674-2636">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-2637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-2637">Az.KeyVault</span></span>
* <span data-ttu-id="24674-2638">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="24674-2638">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="24674-2639">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="24674-2639">Az.LogicApp</span></span>
* <span data-ttu-id="24674-2640">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="24674-2640">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="24674-2641">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="24674-2641">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="24674-2642">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2642">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="24674-2643">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="24674-2643">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="24674-2644">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="24674-2644">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="24674-2645">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="24674-2645">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="24674-2646">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="24674-2646">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="24674-2647">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2647">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="24674-2648">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="24674-2648">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="24674-2649">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="24674-2649">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="24674-2650">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="24674-2650">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="24674-2651">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="24674-2651">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="24674-2652">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="24674-2652">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="24674-2653">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-2653">Az.Monitor</span></span>
* <span data-ttu-id="24674-2654">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="24674-2654">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2655">Az.Network</span></span>
* <span data-ttu-id="24674-2656">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="24674-2656">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="24674-2657">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2657">Az.OperationalInsights</span></span>
* <span data-ttu-id="24674-2658">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2658">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="24674-2659">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="24674-2659">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="24674-2660">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="24674-2660">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2661">Az.Resources</span></span>
* <span data-ttu-id="24674-2662">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2662">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="24674-2663">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2663">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="24674-2664">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2664">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="24674-2665">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-2665">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2666">Az.Sql</span></span>
* <span data-ttu-id="24674-2667">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="24674-2667">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="24674-2668">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="24674-2668">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2669">Az.Websites</span></span>
* <span data-ttu-id="24674-2670">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="24674-2670">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="24674-2671">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="24674-2671">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2672">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2672">Az.Accounts</span></span>
* <span data-ttu-id="24674-2673">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="24674-2673">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="24674-2674">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="24674-2674">Az.AnalysisServices</span></span>
<span data-ttu-id="24674-2675">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="24674-2675">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2676">Az.Compute</span></span>
* <span data-ttu-id="24674-2677">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2677">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="24674-2678">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="24674-2678">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="24674-2679">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="24674-2679">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2680">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2680">Az.RecoveryServices</span></span>
<span data-ttu-id="24674-2681">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="24674-2681">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2682">Az.Resources</span></span>
* <span data-ttu-id="24674-2683">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="24674-2683">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="24674-2684">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="24674-2684">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="24674-2685">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2685">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="24674-2686">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="24674-2686">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2687">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2687">Az.Sql</span></span>
* <span data-ttu-id="24674-2688">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24674-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="24674-2689">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2689">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="24674-2690">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="24674-2690">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="24674-2691">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="24674-2691">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2692">Az.Accounts</span></span>
* <span data-ttu-id="24674-2693">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="24674-2693">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="24674-2694">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="24674-2694">Az.AnalysisServices</span></span>
* <span data-ttu-id="24674-2695">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="24674-2695">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2696">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2696">Az.RecoveryServices</span></span>
* <span data-ttu-id="24674-2697">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="24674-2697">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="24674-2698">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="24674-2698">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2699">Az.Accounts</span></span>
* <span data-ttu-id="24674-2700">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="24674-2700">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="24674-2701">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2701">Update incorrect online help URLs</span></span>
* <span data-ttu-id="24674-2702">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-2702">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="24674-2703">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="24674-2703">Az.Aks</span></span>
* <span data-ttu-id="24674-2704">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2704">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="24674-2705">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2705">Az.Automation</span></span>
* <span data-ttu-id="24674-2706">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2706">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="24674-2707">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2707">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="24674-2708">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="24674-2708">Az.Cdn</span></span>
* <span data-ttu-id="24674-2709">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2709">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2710">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2710">Az.Compute</span></span>
* <span data-ttu-id="24674-2711">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2711">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="24674-2712">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24674-2712">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="24674-2713">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="24674-2713">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="24674-2714">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24674-2714">Az.ContainerRegistry</span></span>
* <span data-ttu-id="24674-2715">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2715">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="24674-2716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="24674-2716">Az.DataFactory</span></span>
* <span data-ttu-id="24674-2717">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="24674-2717">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-2718">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2718">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-2719">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2719">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="24674-2720">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="24674-2720">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="24674-2721">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2721">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-2722">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-2722">Az.IotHub</span></span>
* <span data-ttu-id="24674-2723">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-2723">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="24674-2724">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-2724">Az.KeyVault</span></span>
* <span data-ttu-id="24674-2725">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2725">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2726">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2726">Az.Network</span></span>
* <span data-ttu-id="24674-2727">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2727">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2728">Az.Resources</span></span>
* <span data-ttu-id="24674-2729">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="24674-2729">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="24674-2730">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2730">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="24674-2731">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="24674-2731">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="24674-2732">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2732">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="24674-2733">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2733">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="24674-2734">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2734">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="24674-2735">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="24674-2735">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-2737">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="24674-2737">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="24674-2738">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="24674-2738">Fix some error messages.</span></span>
* <span data-ttu-id="24674-2739">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2739">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="24674-2740">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2740">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="24674-2741">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="24674-2741">Az.SignalR</span></span>
* <span data-ttu-id="24674-2742">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2742">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2743">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2743">Az.Sql</span></span>
* <span data-ttu-id="24674-2744">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2744">Update incorrect online help URLs</span></span>
* <span data-ttu-id="24674-2745">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="24674-2745">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="24674-2746">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2746">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="24674-2747">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="24674-2747">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2748">Az.Storage</span></span>
* <span data-ttu-id="24674-2749">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2749">Update incorrect online help URLs</span></span>
* <span data-ttu-id="24674-2750">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="24674-2750">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="24674-2751">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="24674-2751">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="24674-2752">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="24674-2752">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="24674-2753">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="24674-2753">Az.TrafficManager</span></span>
* <span data-ttu-id="24674-2754">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2754">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2755">Az.Websites</span></span>
* <span data-ttu-id="24674-2756">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="24674-2756">Update incorrect online help URLs</span></span>
* <span data-ttu-id="24674-2757">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="24674-2757">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="24674-2758">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="24674-2758">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="24674-2759">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="24674-2759">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="24674-2760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2760">Az.Accounts</span></span>
* <span data-ttu-id="24674-2761">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="24674-2761">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2762">Az.Compute</span></span>
* <span data-ttu-id="24674-2763">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="24674-2763">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="24674-2764">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="24674-2764">Updated the description of ID in help files</span></span>
* <span data-ttu-id="24674-2765">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="24674-2765">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2766">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-2767">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2767">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="24674-2768">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="24674-2768">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="24674-2769">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="24674-2769">Az.EventGrid</span></span>
* <span data-ttu-id="24674-2770">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="24674-2770">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="24674-2771">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="24674-2771">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="24674-2772">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="24674-2772">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="24674-2773">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="24674-2773">Event Time-To-Live,</span></span>
        - <span data-ttu-id="24674-2774">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="24674-2774">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="24674-2775">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="24674-2775">Dead letter endpoint.</span></span>
    - <span data-ttu-id="24674-2776">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="24674-2776">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="24674-2777">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="24674-2777">Event Time-To-Live,</span></span>
        - <span data-ttu-id="24674-2778">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="24674-2778">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="24674-2779">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="24674-2779">Dead letter endpoint.</span></span>
* <span data-ttu-id="24674-2780">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="24674-2780">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="24674-2781">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="24674-2781">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="24674-2782">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="24674-2782">Az.IotHub</span></span>
* <span data-ttu-id="24674-2783">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="24674-2783">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="24674-2784">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="24674-2784">Az.LogicApp</span></span>
* <span data-ttu-id="24674-2785">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="24674-2785">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-2786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2786">Az.Resources</span></span>
* <span data-ttu-id="24674-2787">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="24674-2787">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="24674-2788">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="24674-2788">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="24674-2789">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="24674-2789">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="24674-2790">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-2790">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="24674-2791">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="24674-2791">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="24674-2792">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="24674-2792">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="24674-2793">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="24674-2793">Az.SignalR</span></span>
* <span data-ttu-id="24674-2794">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="24674-2794">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-2795">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2795">Az.Sql</span></span>
* <span data-ttu-id="24674-2796">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="24674-2796">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="24674-2797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2797">Az.Storage</span></span>
* <span data-ttu-id="24674-2798">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="24674-2798">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="24674-2799">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="24674-2799">New-AzStorageContext</span></span>
* <span data-ttu-id="24674-2800">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="24674-2800">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="24674-2801">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="24674-2801">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2802">Az.Websites</span></span>
* <span data-ttu-id="24674-2803">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="24674-2803">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="24674-2804">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="24674-2804">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="24674-2805">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="24674-2805">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="24674-2806">一般</span><span class="sxs-lookup"><span data-stu-id="24674-2806">General</span></span>

- <span data-ttu-id="24674-2807">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="24674-2807">General Availability of Az Module</span></span>
- <span data-ttu-id="24674-2808">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="24674-2808">Online help for each module</span></span>
- <span data-ttu-id="24674-2809">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="24674-2809">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="24674-2810">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2810">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="24674-2811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2811">Az.Accounts</span></span>
- <span data-ttu-id="24674-2812">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="24674-2812">Changed from Az.Profile</span></span>
- <span data-ttu-id="24674-2813">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="24674-2813">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="24674-2814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-2814">Az.ApiManagement</span></span>
- <span data-ttu-id="24674-2815">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="24674-2815">Fixes for #7002</span></span>
- <span data-ttu-id="24674-2816">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="24674-2817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24674-2817">Az.Batch</span></span>
- <span data-ttu-id="24674-2818">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="24674-2818">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="24674-2819">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="24674-2819">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="24674-2820">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="24674-2821">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="24674-2821">Az.Billing</span></span>
- <span data-ttu-id="24674-2822">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2822">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="24674-2823">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="24674-2823">Az.CognitivServices</span></span>
- <span data-ttu-id="24674-2824">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="24674-2824">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="24674-2825">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="24674-2825">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="24674-2826">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2826">Az.ContainerInstance</span></span>
- <span data-ttu-id="24674-2827">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="24674-2827">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="24674-2828">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="24674-2828">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="24674-2829">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2829">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="24674-2830">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2830">Az.DataLakeStore</span></span>
- <span data-ttu-id="24674-2831">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="24674-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24674-2832">Az.Monitor</span></span>
- <span data-ttu-id="24674-2833">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2833">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="24674-2834">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24674-2834">Az.KeyVault</span></span>
- <span data-ttu-id="24674-2835">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="24674-2835">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="24674-2836">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="24674-2836">Az.MachineLearning</span></span>
- <span data-ttu-id="24674-2837">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2837">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="24674-2838">Az.Media</span><span class="sxs-lookup"><span data-stu-id="24674-2838">Az.Media</span></span>
- <span data-ttu-id="24674-2839">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="24674-2839">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="24674-2840">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2840">Az.Network</span></span>
<span data-ttu-id="24674-2841">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="24674-2841">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="24674-2842">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="24674-2842">New cmdlets added:</span></span>
        - <span data-ttu-id="24674-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="24674-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="24674-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="24674-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="24674-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="24674-2848">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="24674-2848">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="24674-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="24674-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="24674-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="24674-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="24674-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24674-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="24674-2852">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24674-2852">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="24674-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="24674-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="24674-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="24674-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="24674-2855">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24674-2855">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="24674-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="24674-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="24674-2857">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="24674-2858">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2858">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="24674-2859">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="24674-2859">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="24674-2860">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="24674-2860">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="24674-2861">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="24674-2861">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="24674-2862">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2862">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="24674-2863">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2863">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="24674-2864">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24674-2864">Az.OperationalInsights</span></span>
- <span data-ttu-id="24674-2865">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2865">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="24674-2866">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="24674-2866">Az.Profile</span></span>
- <span data-ttu-id="24674-2867">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="24674-2867">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2868">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2868">Az.RecoveryServices</span></span>
- <span data-ttu-id="24674-2869">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2869">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="24674-2870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2870">Az.Resources</span></span>
- <span data-ttu-id="24674-2871">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2871">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="24674-2872">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-2872">Az.ServiceFabric</span></span>
- <span data-ttu-id="24674-2873">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="24674-2873">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="24674-2874">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2874">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="24674-2875">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="24674-2875">Az.SIgnalR</span></span>
- <span data-ttu-id="24674-2876">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="24674-2876">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="24674-2877">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2877">Az.Sql</span></span>
- <span data-ttu-id="24674-2878">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="24674-2878">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="24674-2879">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="24674-2879">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="24674-2880">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2880">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="24674-2881">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2881">Az.Storage</span></span>
- <span data-ttu-id="24674-2882">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2882">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="24674-2883">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2883">Az.Websites</span></span>
- <span data-ttu-id="24674-2884">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="24674-2884">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="24674-2885">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="24674-2885">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="24674-2886">一般</span><span class="sxs-lookup"><span data-stu-id="24674-2886">General</span></span>

* <span data-ttu-id="24674-2887">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="24674-2887">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="24674-2888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2888">Az.Compute</span></span>

* <span data-ttu-id="24674-2889">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="24674-2889">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="24674-2890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2890">Az.DataLakeStore</span></span>

* <span data-ttu-id="24674-2891">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="24674-2891">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="24674-2892">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="24674-2892">Az.FrontDoor</span></span>

* <span data-ttu-id="24674-2893">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="24674-2893">Fixed some broken links</span></span>
    - <span data-ttu-id="24674-2894">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="24674-2894">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="24674-2895">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="24674-2895">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="24674-2896">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="24674-2896">Az.RecoveryServices</span></span>

* <span data-ttu-id="24674-2897">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="24674-2897">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="24674-2898">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="24674-2898">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="24674-2899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2899">Az.Resources</span></span>

* <span data-ttu-id="24674-2900">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="24674-2900">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="24674-2901">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="24674-2901">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="24674-2902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2902">Az.Sql</span></span>

* <span data-ttu-id="24674-2903">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="24674-2903">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="24674-2904">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2904">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="24674-2905">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="24674-2905">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="24674-2906">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-2906">Az.Storage</span></span>

* <span data-ttu-id="24674-2907">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="24674-2907">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="24674-2908">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="24674-2908">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="24674-2909">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="24674-2909">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="24674-2910">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="24674-2910">Support Static Website configuration</span></span>
    - <span data-ttu-id="24674-2911">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="24674-2911">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="24674-2912">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="24674-2912">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="24674-2913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-2913">Az.Websites</span></span>

* <span data-ttu-id="24674-2914">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24674-2914">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="24674-2915">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="24674-2915">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="24674-2916">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="24674-2916">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="24674-2917">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="24674-2917">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="24674-2918">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24674-2918">Az.ApiManagement</span></span>
* <span data-ttu-id="24674-2919">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="24674-2919">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="24674-2920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="24674-2920">Az.Automation</span></span>
* <span data-ttu-id="24674-2921">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2921">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="24674-2922">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2922">Added Update Management cmdlets</span></span>
* <span data-ttu-id="24674-2923">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2923">Added Source Control cmdlets</span></span>
* <span data-ttu-id="24674-2924">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2924">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="24674-2925">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="24674-2925">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="24674-2926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2926">Az.Compute</span></span>
* <span data-ttu-id="24674-2927">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="24674-2927">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="24674-2928">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="24674-2928">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="24674-2929">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2929">Az.ContainerInstance</span></span>
* <span data-ttu-id="24674-2930">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="24674-2930">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="24674-2931">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="24674-2931">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="24674-2932">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="24674-2932">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="24674-2933">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2933">Az.Network</span></span>
* <span data-ttu-id="24674-2934">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="24674-2934">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="24674-2935">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="24674-2935">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="24674-2936">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="24674-2936">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="24674-2937">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="24674-2937">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="24674-2938">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="24674-2938">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="24674-2939">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="24674-2939">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="24674-2940">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="24674-2940">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="24674-2941">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="24674-2941">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="24674-2942">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="24674-2942">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="24674-2943">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="24674-2943">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="24674-2944">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="24674-2944">Az.Relay</span></span>
* <span data-ttu-id="24674-2945">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="24674-2945">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="24674-2946">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-2946">Az.Resources</span></span>
* <span data-ttu-id="24674-2947">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="24674-2947">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="24674-2948">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="24674-2948">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="24674-2949">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="24674-2949">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="24674-2950">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-2950">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-2951">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="24674-2951">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="24674-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-2952">Az.Sql</span></span>
* <span data-ttu-id="24674-2953">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2953">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="24674-2954">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2954">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="24674-2955">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2955">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="24674-2956">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2956">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="24674-2957">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="24674-2957">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="24674-2958">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="24674-2958">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="24674-2959">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="24674-2959">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="24674-2960">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="24674-2960">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="24674-2961">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="24674-2961">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="24674-2962">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="24674-2962">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="24674-2963">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="24674-2963">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="24674-2964">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="24674-2964">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="24674-2965">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="24674-2965">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="24674-2966">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="24674-2966">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="24674-2967">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="24674-2967">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="24674-2968">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="24674-2968">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="24674-2969">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2969">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="24674-2970">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="24674-2970">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="24674-2971">一般</span><span class="sxs-lookup"><span data-stu-id="24674-2971">General</span></span>
* <span data-ttu-id="24674-2972">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="24674-2972">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="24674-2973">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="24674-2973">Az.Profile</span></span>
* <span data-ttu-id="24674-2974">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="24674-2974">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="24674-2975">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="24674-2975">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="24674-2976">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="24674-2976">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="24674-2977">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24674-2977">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="24674-2978">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2978">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="24674-2979">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2979">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="24674-2980">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="24674-2980">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-2981">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-2981">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-2982">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="24674-2982">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-2983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-2983">Az.Compute</span></span>
* <span data-ttu-id="24674-2984">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-2984">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="24674-2985">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="24674-2985">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="24674-2986">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2986">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-2987">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-2988">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="24674-2988">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="24674-2989">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="24674-2989">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="24674-2990">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="24674-2990">Az.Insights</span></span>
* <span data-ttu-id="24674-2991">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="24674-2991">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="24674-2992">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="24674-2992">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="24674-2993">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="24674-2993">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="24674-2994">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="24674-2994">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-2995">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-2995">Az.Network</span></span>
* <span data-ttu-id="24674-2996">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="24674-2996">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="24674-2997">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="24674-2997">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="24674-2998">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="24674-2998">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="24674-2999">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="24674-2999">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="24674-3000">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="24674-3000">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="24674-3001">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="24674-3001">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="24674-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="24674-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="24674-3003">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="24674-3003">Az.PolicyInsights</span></span>
* <span data-ttu-id="24674-3004">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-3004">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-3005">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-3005">Az.Resources</span></span>
* <span data-ttu-id="24674-3006">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="24674-3006">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="24674-3007">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="24674-3007">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="24674-3008">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="24674-3008">Az.ServiceBus</span></span>
* <span data-ttu-id="24674-3009">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="24674-3009">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="24674-3010">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="24674-3010">Az.ServiceFabric</span></span>
* <span data-ttu-id="24674-3011">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="24674-3011">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="24674-3012">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="24674-3012">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="24674-3013">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="24674-3013">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="24674-3014">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="24674-3014">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="24674-3015">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="24674-3015">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="24674-3016">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="24674-3016">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="24674-3017">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="24674-3017">Az.Profile</span></span>
* <span data-ttu-id="24674-3018">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="24674-3018">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="24674-3019">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="24674-3019">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-3020">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-3020">Az.Compute</span></span>
* <span data-ttu-id="24674-3021">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="24674-3021">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="24674-3022">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-3022">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="24674-3023">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24674-3023">Az.DataLakeStore</span></span>
* <span data-ttu-id="24674-3024">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="24674-3024">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="24674-3025">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="24674-3025">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="24674-3026">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="24674-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="24674-3027">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="24674-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="24674-3028">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="24674-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-3029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-3029">Az.Network</span></span>
* <span data-ttu-id="24674-3030">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="24674-3030">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="24674-3031">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24674-3031">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-3032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-3032">Az.Resources</span></span>
* <span data-ttu-id="24674-3033">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="24674-3033">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="24674-3034">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="24674-3034">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="24674-3035">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="24674-3035">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="24674-3036">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="24674-3036">Azure.Storage</span></span>
* <span data-ttu-id="24674-3037">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="24674-3037">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="24674-3038">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="24674-3038">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="24674-3039">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="24674-3039">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="24674-3040">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="24674-3040">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="24674-3041">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="24674-3041">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="24674-3042">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="24674-3042">Az.CognitiveServices</span></span>
* <span data-ttu-id="24674-3043">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="24674-3043">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="24674-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24674-3044">Az.Compute</span></span>
* <span data-ttu-id="24674-3045">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="24674-3045">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="24674-3046">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="24674-3046">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="24674-3047">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="24674-3047">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="24674-3048">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="24674-3048">Az.DataFactoryV2</span></span>
* <span data-ttu-id="24674-3049">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="24674-3049">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="24674-3050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24674-3050">Az.Network</span></span>
* <span data-ttu-id="24674-3051">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="24674-3051">Added NetworkProfile functionality.</span></span> <span data-ttu-id="24674-3052">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-3052">new cmdlets added</span></span>
    - <span data-ttu-id="24674-3053">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="24674-3053">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="24674-3054">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="24674-3054">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="24674-3055">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="24674-3055">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="24674-3056">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="24674-3056">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="24674-3057">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="24674-3057">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="24674-3058">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="24674-3058">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="24674-3059">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="24674-3059">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="24674-3060">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-3060">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="24674-3061">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24674-3061">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="24674-3062">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="24674-3062">Az.RedisCache</span></span>
* <span data-ttu-id="24674-3063">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="24674-3063">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="24674-3064">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="24674-3064">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="24674-3065">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24674-3065">Az.Resources</span></span>
* <span data-ttu-id="24674-3066">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24674-3066">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="24674-3067">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="24674-3067">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="24674-3068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="24674-3068">Az.Sql</span></span>
* <span data-ttu-id="24674-3069">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="24674-3069">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="24674-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="24674-3070">Az.Websites</span></span>
* <span data-ttu-id="24674-3071">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="24674-3071">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="24674-3072">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="24674-3072">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="24674-3073">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="24674-3073">0.2.0 - September 2018</span></span>
 <span data-ttu-id="24674-3074">初始版本</span><span class="sxs-lookup"><span data-stu-id="24674-3074">Initial Release</span></span>
